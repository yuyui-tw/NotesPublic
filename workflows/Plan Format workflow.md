> [!info] AI Workflow History
> - 2026/7/1 下午1:05:23: Created - "[Content of workflows/Planner formatter.md]
Create a robust Obsidian workflow for formatting planning documents.

Workflow name:
Plan Formatter

Goal:
Take the currently selected text or, if no text is selected, the full current note content. Send that content to my local LM Studio model and transform it into a structured planning document in Markdown.

Variables:
- outputFolder = "30_Plans/"
- taskInstruction = "請將以下內容整理成正式規劃書，保留原意，強化結構與可執行性，不要添加未提供的背景。"

Input behavior:
- If editor.selection exists and is not empty, use editor.selection as the input.
- Otherwise, use the full current note content.
- If neither selected text nor current note content is available, stop the workflow and show this error:
  "沒有可處理的規劃內容，請先選取文字或開啟一篇筆記。"

LLM behavior:
- Send the input text together with taskInstruction to the local LM Studio model.
- This is a planning-document formatting task, not a brainstorming chat.
- Do not invent background facts, achievements, or resources.
- Keep the user's intent and reorganize it into a clearer actionable structure.
- If information is missing, preserve the section and mark it as 待補.
- Output should be Markdown only.

LLM output validation:
- After the LLM step, check whether the returned output exists and is not empty.
- If the output is missing or empty, stop the workflow and show this error:
  "模型沒有成功回傳規劃書內容，請檢查 LM Studio 連線、模型狀態或提示詞。"

User flow after valid output:
- Show a preview of the generated planning document.
- Then offer these actions:
  1. Replace current selection.
  2. Append below current note.
  3. Save as a new note in outputFolder.

Save behavior:
- When saving as a new note, use outputFolder instead of a hardcoded path.
- Prefer a filename based on the planning topic if available.
- If no title can be inferred, use a timestamp-based fallback filename.

Design notes:
- Keep the workflow concise and action-oriented.
- Use clean user-facing errors.
- Avoid any crash when editor.selection is unavailable.

Update the LLM node configuration:
- Set enableThinking to false.
- This workflow is for formatting and restructuring text, so low-latency output is preferred over extended reasoning.

Simplify the generateFilename script:
- If a title or heading can be inferred from the generated markdown, use it as the filename.
- Otherwise, use a timestamp-based fallback filename.
- If noteContent is empty or missing, still generate a safe timestamp-based filename.
- Keep the script minimal and robust.

Document that preview and save-as-new-note are the primary supported actions for now.
Replace and append options may remain visible for future expansion, but they do not need to be fully implemented yet.
[/Content]"
>   > [!note]- @workflows/Planner formatter.md
>   > ```
>   > Create a robust Obsidian workflow for formatting planning documents.
>   > 
>   > Workflow name:
>   > Plan Formatter
>   > 
>   > Goal:
>   > Take the currently selected text or, if no text is selected, the full current note content. Send that content to my local LM Studio model and transform it into a structured planning document in Markdown.
>   > 
>   > Variables:
>   > - outputFolder = "30_Plans/"
>   > - taskInstruction = "請將以下內容整理成正式規劃書，保留原意，強化結構與可執行性，不要添加未提供的背景。"
>   > 
>   > Input behavior:
>   > - If editor.selection exists and is not empty, use editor.selection as the input.
>   > - Otherwise, use the full current note content.
>   > - If neither selected text nor current note content is available, stop the workflow and show this error:
>   >   "沒有可處理的規劃內容，請先選取文字或開啟一篇筆記。"
>   > 
>   > LLM behavior:
>   > - Send the input text together with taskInstruction to the local LM Studio model.
>   > - This is a planning-document formatting task, not a brainstorming chat.
>   > - Do not invent background facts, achievements, or resources.
>   > - Keep the user's intent and reorganize it into a clearer actionable structure.
>   > - If information is missing, preserve the section and mark it as 待補.
>   > - Output should be Markdown only.
>   > 
>   > LLM output validation:
>   > - After the LLM step, check whether the returned output exists and is not empty.
>   > - If the output is missing or empty, stop the workflow and show this error:
>   >   "模型沒有成功回傳規劃書內容，請檢查 LM Studio 連線、模型狀態或提示詞。"
>   > 
>   > User flow after valid output:
>   > - Show a preview of the generated planning document.
>   > - Then offer these actions:
>   >   1. Replace current selection.
>   >   2. Append below current note.
>   >   3. Save as a new note in outputFolder.
>   > 
>   > Save behavior:
>   > - When saving as a new note, use outputFolder instead of a hardcoded path.
>   > - Prefer a filename based on the planning topic if available.
>   > - If no title can be inferred, use a timestamp-based fallback filename.
>   > 
>   > Design notes:
>   > - Keep the workflow concise and action-oriented.
>   > - Use clean user-facing errors.
>   > - Avoid any crash when editor.selection is unavailable.
>   > 
>   > Update the LLM node configuration:
>   > - Set enableThinking to false.
>   > - This workflow is for formatting and restructuring text, so low-latency output is preferred over extended reasoning.
>   > 
>   > Simplify the generateFilename script:
>   > - If a title or heading can be inferred from the generated markdown, use it as the filename.
>   > - Otherwise, use a timestamp-based fallback filename.
>   > - If noteContent is empty or missing, still generate a safe timestamp-based filename.
>   > - Keep the script minimal and robust.
>   > 
>   > Document that preview and save-as-new-note are the primary supported actions for now.
>   > Replace and append options may remain visible for future expansion, but they do not need to be fully implemented yet.
>   > ```

```llm-workflow
name: Plam Format workflow
nodes:
  - id: check-selection
    type: variable
    name: editor.selection
  - id: get-note-content
    type: note-read
    path: "{{currentNote}}"
    saveTo: noteContent
  - id: prompt-ai
    type: command
    prompt: |
      请将以下内容整理成正式规划书，保留原意，强化结构与可执行性，不要添加未提供的背景。
      {{noteContent}}
    enableThinking: "false"
    saveTo: aiOutput
  - id: validate-ai-output
    type: variable
    name: aiOutput
  - id: show-preview
    type: dialog
    title: Plan Preview
    message: "{{aiOutput}}"
    markdown: "true"
    saveTo: noData
  - id: save-plan
    type: note
    path: "{{outputFolder}}/{{generateFilename}}"
    content: "{{aiOutput}}"
    mode: overwrite
    confirm: "false"
  - id: generateFilename
    type: script
    code: |
      var title = "";
      if ({{aiOutput}} != null && {{aiOutput}} !== "") {
        // Attempt to extract a title from the AI output. This is a simplistic example.
        // You'd likely need more sophisticated logic here, parsing Markdown headings, etc.
        var headingMatch = {{aiOutput}}.match(/^#\s+(.*)$/m); // Find first heading
        if (headingMatch) {
          title = headingMatch[1];
        } else {
          // Fallback: use timestamp
          title = Date.now().toString();
        }
      } else {
        title = Date.now().toString();
      }
      return title;
    saveTo: filename
  - id: end
    type: dialog
    title: Done
    message: Plan saved to 30_Plans/
```
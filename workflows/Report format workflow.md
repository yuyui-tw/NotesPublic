> [!info] AI Workflow History
> - 2026/7/1 下午1:03:51: Created - "[Content of workflows/Report Formatter.md]
Create a robust Obsidian workflow for drafting lab reports.

Workflow name:
Lab Report Formatter

Goal:
Take the currently selected text or, if no text is selected, the full current note content. Send that content to my local LM Studio model and transform it into a structured physics lab report draft in Markdown.

Variables:
- outputFolder = "20_LabReports/"
- taskInstruction = "請將以下內容整理成實驗報告草稿，保持正式學術語氣，不可捏造數據，缺少資訊請標示待補。"

Input behavior:
- If editor.selection exists and is not empty, use editor.selection as the input.
- Otherwise, use the full current note content.
- If neither selected text nor current note content is available, stop the workflow and show this error:
  "沒有可處理的實驗內容，請先選取文字或開啟一篇筆記。"

LLM behavior:
- Send the input text together with taskInstruction to the local LM Studio model.
- This is a lab report drafting task, not a general summary task.
- Do not invent experimental data, citations, team members, or conclusions.
- If information is missing, preserve the section and mark it as 待補.
- Output should be Markdown only.

LLM output validation:
- After the LLM step, check whether the returned output exists and is not empty.
- If the output is missing or empty, stop the workflow and show this error:
  "模型沒有成功回傳實驗報告內容，請檢查 LM Studio 連線、模型狀態或提示詞。"

User flow after valid output:
- Show a preview of the generated report draft.
- Then offer these actions:
  1. Append below current note.
  2. Replace current note body.
  3. Save as a new note in outputFolder.

Save behavior:
- When saving as a new note, use outputFolder instead of a hardcoded path.
- Prefer a filename based on the experiment title if available.
- If no title can be inferred, use a timestamp-based fallback filename.

Design notes:
- Keep the workflow safe for academic use.
- Prioritize preserving original data and meaning.
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
>   > [!note]- @workflows/Report Formatter.md
>   > ```
>   > Create a robust Obsidian workflow for drafting lab reports.
>   > 
>   > Workflow name:
>   > Lab Report Formatter
>   > 
>   > Goal:
>   > Take the currently selected text or, if no text is selected, the full current note content. Send that content to my local LM Studio model and transform it into a structured physics lab report draft in Markdown.
>   > 
>   > Variables:
>   > - outputFolder = "20_LabReports/"
>   > - taskInstruction = "請將以下內容整理成實驗報告草稿，保持正式學術語氣，不可捏造數據，缺少資訊請標示待補。"
>   > 
>   > Input behavior:
>   > - If editor.selection exists and is not empty, use editor.selection as the input.
>   > - Otherwise, use the full current note content.
>   > - If neither selected text nor current note content is available, stop the workflow and show this error:
>   >   "沒有可處理的實驗內容，請先選取文字或開啟一篇筆記。"
>   > 
>   > LLM behavior:
>   > - Send the input text together with taskInstruction to the local LM Studio model.
>   > - This is a lab report drafting task, not a general summary task.
>   > - Do not invent experimental data, citations, team members, or conclusions.
>   > - If information is missing, preserve the section and mark it as 待補.
>   > - Output should be Markdown only.
>   > 
>   > LLM output validation:
>   > - After the LLM step, check whether the returned output exists and is not empty.
>   > - If the output is missing or empty, stop the workflow and show this error:
>   >   "模型沒有成功回傳實驗報告內容，請檢查 LM Studio 連線、模型狀態或提示詞。"
>   > 
>   > User flow after valid output:
>   > - Show a preview of the generated report draft.
>   > - Then offer these actions:
>   >   1. Append below current note.
>   >   2. Replace current note body.
>   >   3. Save as a new note in outputFolder.
>   > 
>   > Save behavior:
>   > - When saving as a new note, use outputFolder instead of a hardcoded path.
>   > - Prefer a filename based on the experiment title if available.
>   > - If no title can be inferred, use a timestamp-based fallback filename.
>   > 
>   > Design notes:
>   > - Keep the workflow safe for academic use.
>   > - Prioritize preserving original data and meaning.
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
name: Report format workflow
nodes:
  - id: check-selection
    type: variable
    name: "editor.selection"
  - id: retrieveNoteContent
    type: note-read
    path: "{{_currentNode.path}}"
    saveTo: "noteContent"
  - id: promptLLM
    type: command
    prompt: |
      請將以下內容整理成實驗報告草稿，保持正式學術語氣，不可捏造數據，缺少資訊請標示待補。
      {{noteContent}}
      
    enableThinking: "false"
    saveTo: "formattedReport"
  - id: validateLLMOutput
    type: variable
    name: "formattedReport"
  - id: showPreview
    type: dialog
    title: "Lab Report Draft Preview"
    message: "{{formattedReport}}"
    markdown: "true"
  - id: saveAsNewNote
    type: note
    path: "{{outputFolder}}/{{generateFilename}}"
    content: "{{formattedReport}}"
    mode: "overwrite"
    confirm: "false"
  - id: handleNoOutput
    type: dialog
    title: "Error - No AI Output"
    message: |
      模型沒有成功回傳實驗報告內容，請檢查 LM Studio 連線、模型狀態或提示詞。
      建議您重新查看LM Studio的設置。
    markdown: "true"
```

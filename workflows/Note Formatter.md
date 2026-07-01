Create a robust Obsidian workflow for note formatting.

Workflow name:
Note Formatter

Goal:
Take the currently selected text or, if no text is selected, the full current note content. Send that content to my local LM Studio model and transform it into a structured Obsidian Markdown note.

Variables:
- outputFolder = "10_Notes/"
- taskInstruction = "請將以下內容整理成 Obsidian Markdown 筆記，保留重要術語、公式與原意，使用清楚段落與條列，不要新增例題。"

Input behavior:
- If editor.selection exists and is not empty, use editor.selection as the input.
- Otherwise, use the full current note content.
- If neither selected text nor current note content is available, stop the workflow and show this error:
  "沒有可處理的文字，請先選取文字或開啟一篇筆記。"

LLM behavior:
- Send the input text together with taskInstruction to the local LM Studio model.
- This is a formatting task, not a general chat task.
- Keep the original meaning.
- Do not invent facts.
- Output should be Markdown only.

LLM output validation:
- After the LLM step, check whether the returned output exists and is not empty.
- If the output is missing or empty, stop the workflow and show this error:
  "模型沒有成功回傳內容，請檢查 LM Studio 連線、模型狀態或提示詞。"

User flow after valid output:
- Show a preview of the generated Markdown.
- Then offer these actions:
  1. Replace current selection.
  2. Append below current note.
  3. Save as a new note in outputFolder.

Save behavior:
- When saving as a new note, use outputFolder instead of a hardcoded path.
- Prefer a reasonable generated filename based on the note title or topic.
- If no title can be inferred, use a timestamp-based fallback filename.

Design notes:
- Keep the workflow simple and robust.
- Use clear user-facing error messages.
- Avoid crashing when editor.selection is unavailable.

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
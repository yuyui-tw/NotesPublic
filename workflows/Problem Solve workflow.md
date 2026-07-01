> [!info] AI Workflow History
> - 2026/7/1 下午1:26:14: Created - "Create a robust Obsidian workflow for problem solving and solution embedding.

Workflow name:
Problem Solver

Important implementation constraint:
- Do NOT use placeholder functions such as obsidian.callLLM.
- Use only built-in Local LLM Hub workflow nodes or native plugin-supported actions for:
  1. reading selected text or current note,
  2. calling the configured local LLM provider,
  3. previewing output,
  4. asking the user what to do next,
  5. saving or inserting the result.
- If a feature is not directly supported by a native node, choose the simplest supported fallback instead of inventing a custom placeholder function.

Goal:
Take the currently selected problem text or, if no text is selected, use the current note content. Send that content to the configured LM Studio model through the plugin’s native LLM node and generate a structured step-by-step solution in Markdown.

Variables:
- outputFolder = "40_Problems/"
- taskInstruction = "請解以下題目，使用標準格式輸出：題目、已知、目標、使用原理、公式、計算過程、結論、檢查/備註。不可捏造條件，若資訊不足請直接指出。"

Input behavior:
- If selected text exists and is not empty, use selected text.
- Otherwise, use the full current note content.
- If possible, prefer a section named # 例題, # Problems, or # 題目 when the current note contains multiple sections.
- If neither selected text nor current note content is available, stop the workflow and show this error:
  "沒有可處理的題目內容，請先選取題目文字或開啟一篇題目筆記。"

LLM behavior:
- Use the plugin’s native LLM invocation node to call the configured local LM Studio model.
- Pass taskInstruction together with the problem text.
- This is a problem-solving task, not a general"

```llm-workflow
name: Problem Solve workflow
nodes:
  - id: check-text-selected
    type: variable
    name: "selectedText"
    value: "{{selection}}"
  - id: select-problem-section
    type: note-list
    folder: "40_Problems/"
    recursive: "true"
    tags: "[\"#題目\"]"
    tagMatch: "any"
    saveTo: "problemSections"
  - id: read-problem-content
    type: command
    prompt: "請選擇要解決的題目：{{fileList.notes[index].path}}"
    saveTo: "problemContent"
  - id: no-problem-found
    type: dialog
    title: "沒有可處理的題目內容，請先選取題目文字或開啟一篇題目筆記。"
    message: "沒有找到問題描述。 請在 Obsidian 中選擇題目的文字，或者開啟一個包含題目的筆記。"
  - id: invoke-llm
    type: command
    prompt: |
      請解以下題目，使用標準格式輸出：題目、已知、目標、使用原理、公式、計算過程、結論、檢查/備註。不可捏造條件，若資訊不足請直接指出。
      
      {{problemContent}}
    saveTo: "solution"
  - id: save-solution
    type: note
    path: "{{outputFolder}}/solution.md"
    content: "{{solution}}"
    mode: "overwrite"
    confirm: "false"
  - id: end
    type: dialog
    title: "完成"
    message: "已將解決方案儲存到 {{outputFolder}}/"
```

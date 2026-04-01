---
name: document-to-markdown
description: >
  Convert word (.doc, .docx) or pdf files to markdown using markitdown.mcp. Use when the user requests to convert documents to markdown format.
argument-hint: 'the file path to convert — e.g., /path/to/document.docx or /path/to/file.pdf'
---

# Document to Markdown Converter

> **One-sentence summary.** Converts word and pdf files to markdown for easy reading and editing.

---

## When to Use

Use this skill when the user says something like:

- "convert this word file to markdown"
- "turn this pdf into markdown"
- "markdown this document"
- "change docx to md"
- "export pdf as markdown"

Do **not** use this skill when:

- The file is not a word (.doc, .docx) or pdf (.pdf) file
- The user does not specify conversion to markdown
- The file path is invalid or inaccessible

---

## Inputs

| Input | Source | Notes |
|-------|--------|-------|
| file_path | argument | Absolute or relative path to the word or pdf file to convert. Must exist and be readable. |

---

## Procedure

Follow these steps in order. Do not skip steps unless the condition in the step itself says it is optional.

### Step 1 — Validate input

- Check if the file_path exists using file system tools.
- Verify the file extension is .doc, .docx, or .pdf.
- If the file does not exist or is not a supported type, stop and report an error to the user.

### Step 2 — Call markitdown tool

- Invoke the markitdown/convert tool from the markitdown.mcp server, passing the file_path as input.
- Retrieve the markdown output as a string from the tool response.

### Step 3 — Save output

- Create a new file in the same directory as the input file, with the same base name but .md extension (e.g., document.docx -> document.md).
- Write the markdown string to this new file.
- Do not overwrite any existing file; if a .md file already exists, append a number (e.g., document(1).md).

### Step 4 — Validate

- Confirm the output file was created and contains content.
- If validation fails, delete the output file and report the error.

---

## Output Specification

Produces a new markdown file containing the converted content from the input document.

```
# Example Converted Markdown

This is the content extracted from the word or pdf file.

- Bullet points
- More content
```

- **Location:** New file in the same directory as the input, with .md extension (e.g., input.docx -> input.md).
- **Format:** Standard markdown (text with headers, lists, etc.).

---

## Conventions and Rules

- Never overwrite the original input file or any existing .md file without user confirmation.
- Always validate file existence and type before proceeding.
- Handle tool errors gracefully and inform the user.
- Preserve the directory structure; output in the same folder as input.

---

## Quick Example

**Input:**

```
/path/to/sample.docx
```

**Output:**

A new file `/path/to/sample.md` with the markdown content.

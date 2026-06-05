---
name: math-error-handout
description: Create printable Chinese middle-school mathematics error-review handouts as Word documents from problem images, PDFs, pasted text, or existing documents. Use when the user asks to convert math questions into 错题整理、错题复盘、打印讲义、学生练习版、教师版、步骤填空、同类变式题、混合练习, especially when diagrams must be cleaned, redrawn, or inserted into a DOCX.
version: 1.0.0
author: RenZhe0228
---

# Math Error Handout

## Purpose

Produce a classroom-printable Chinese Word handout for middle-school math error review. The default deliverable is a student practice DOCX: original questions, clean diagrams, thinking prompts, error diagnosis, answer areas, step-fill blanks, variants, self-checks, mixed practice, and final reference answers.

Use the document-generation skill or available DOCX tooling when creating the final file. If a referenced problem contains diagrams, the final Word document must contain actual diagrams, not text-only diagram descriptions.

## Required Inputs

Before generating a full handout, confirm or infer all scope fields:

- question content, image, PDF, pasted text, or source document;
- grade level;
- semester;
- region;
- textbook version.

Interpret Chinese grade shorthand:

- `7下` means Grade 7, second semester;
- `8上` means Grade 8, first semester;
- apply the same rule to other grades and semesters.

If any scope field is missing and cannot be safely inferred, stop and ask for it before creating the DOCX.

## Workflow

1. **Recognize the original questions**
   - Transcribe conditions, symbols, units, diagrams, labels, angle measures, segment relationships, and requested conclusions accurately.
   - Do not guess unclear numbers, labels, conditions, or conclusions. Report unclear parts and mark them for confirmation.
   - If text and diagram conflict, stop and explain the contradiction.

2. **Check grade scope**
   - Compare the knowledge points with the supplied grade, semester, region, and textbook version.
   - For regular Grade 7 handouts, avoid using Pythagorean theorem, similarity, quadratic functions, advanced circle properties, trigonometric functions, coordinate methods, or vectors.
   - If a problem is beyond scope, label the Word title or section as `拓展训练`, `专题拔高`, or `预习专题` instead of forcing it into regular review.

3. **Plan clean diagrams**
   - If the original image is clean and all labels are clear, crop and use it directly when appropriate.
   - If the original image has handwriting, red marks, stains, extra auxiliary lines, or cropped/missing parts, redraw a clean schematic.
   - Redraw only relationships explicitly stated in the problem. Do not add unstated parallel, perpendicular, equal-length, angle-bisector, tangent, center, ratio, or coordinate assumptions.
   - If a proof needs an auxiliary line or point, state `作……` in the explanation and distinguish the auxiliary element in the diagram.

4. **Build the student handout**
   - Default language: Chinese for all handout content.
   - Default file type: Word DOCX with an English filename.
   - Default version: student practice version, with all reference answers placed together at the end.
   - Use A4 portrait, black-and-white printable styling, clear heading hierarchy, readable Chinese fonts, moderate margins, and compact answer areas.

5. **Generate practice content**
   - For each original question, include these sections in order:
     1. 原题
     2. 图形
     3. 思路提示
     4. 易错点诊断
     5. 作答区
     6. 步骤填空
     7. 同类变式题
     8. 做完后自查
   - Generate 3 same-type variant questions per original question unless the user requests a different count.
   - Include 3-4 mixed practice questions when there are 1-2 original questions; include 4-6 when there are more.
   - If original or practice questions depend on diagrams, include actual diagrams for those questions.
   - Use underlined blanks such as `__________` for fill-in positions. Do not use square placeholder characters such as `□`, `□□□□`, or `（□□□□）`.

6. **Write solutions**
   - Put all answers, standard explanations, and `一类题通法` in the final `参考答案与解析` section.
   - Explain reasoning as: obtain relationships from conditions, then use those relationships to derive the conclusion.
   - State key justifications explicitly, such as definitions, angle relationships, congruent triangle criteria, and corresponding parts of congruent triangles.
   - Use junior-middle-school-appropriate methods unless the section is explicitly marked as extension.

7. **Validate before delivery**
   - Internally check transcription, reasoning, grade scope, formulas, diagrams, answer placement, page count, and ambiguity flags.
   - Render the DOCX as page images or PDF if possible and inspect for missing diagrams, handwriting, overlap, garbled formulas, excessive blank space, and misplaced answers.
   - If rendering is unavailable, structurally verify that images are embedded and state the limitation in the final reply.

## Diagram Failure Hard Stop

If the original question contains diagrams, the generated Word document must contain actual diagrams: either clean cropped originals or redrawn clean schematics.

Text descriptions such as `图①表示……` are not acceptable substitutes for diagrams in the student Word version.

If environment permissions, missing tools, image clarity, or missing conditions prevent actual diagram generation or insertion, do not generate the final Word document. Stop first and report:

1. which diagrams cannot be generated;
2. why they cannot be generated;
3. what permission, file, or clarification is needed.

Only after the diagram problem is resolved may the final Word document be generated.

凡原题含图，最终 Word 中必须能看到实际图形；若没有实际图形，视为生成失败，不得交付。

## Formula Standards

Use readable mathematical notation in the Word document:

- use `a²`, `(a+b)²`, `13⁄4`, `x≥0`, and `−`;
- use `×` for multiplication in junior-middle-school arithmetic;
- avoid code-style notation such as `a^2`, `(a+b)^2`, `13/4`, or `x>=0`;
- use display equations or clear Word-compatible formatting for complex fractions, radicals, systems, and long derivations.

## Detailed Standards

For full requirements on prompts, error diagnosis, variants, mixed practice, layout, diagrams, and final reply format, read `references/handout-standards.md` when creating or auditing a real handout.

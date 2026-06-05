# Math Error Handout Detailed Standards

## Language and Output

- Write all generated handout content in Chinese.
- Use English filenames only.
- Default output is a Word DOCX.
- Default version is student practice version.
- In the student version, place all reference answers and explanations at the end under `参考答案与解析`.
- Do not include full answers in the main practice section.
- Do not include proofreading notes, generation process, internal checks, or prompt text in the student handout.

## Required Confirmation

Before formal generation, confirm:

1. question content, image, PDF, pasted text, or document;
2. grade level;
3. semester;
4. region;
5. textbook version.

If any information affects scope judgment and is missing, do not generate the full Word document. Ask the user to provide the missing item.

## Grade-Level and Out-of-Scope Control

Check whether the problem knowledge points match the provided grade, semester, region, and textbook version.

If a question is beyond scope:

1. state the extension risk in the chat;
2. do not force it into a regular final-review handout;
3. title the handout or section as `拓展训练`, `专题拔高`, or `预习专题`.

For regular Grade 7 handouts, in principle do not use:

- Pythagorean theorem;
- similarity;
- quadratic functions;
- advanced circle properties;
- trigonometric functions;
- coordinate methods;
- vector methods.

Congruent triangle criteria may be used only when they have been systematically taught in the current semester textbook. Otherwise mark the problem as extension or use only learned methods.

## Original Question Recognition

- Accurately organize the original question.
- Do not arbitrarily change key conditions, diagram relationships, angle measures, segment names, symbols, units, options, or conclusions.
- If image content contains unclear numbers, labels, angle labels, segment relationships, or question requirements, state this in the chat and mark it for confirmation.
- If text and diagram contradict each other, pause and explain the contradiction.

## Diagram Handling

There are two diagram quality levels:

1. classroom handout diagram;
2. publication-clean diagram.

Default standard: publication-clean diagram.

Original diagram handling:

- If the original image has no handwriting, no red marks, no stains, no missing cropped parts, and all key labels are clear, it may be cropped and used directly.
- If the original image contains handwriting, red marks, circles, side notes, stains, or non-question auxiliary lines, do not directly insert it into the student Word version by default. Redraw a clean schematic.
- Redrawing may only retain mathematical relationships explicitly given in the problem statement.
- Do not add unstated conditions such as parallel lines, perpendicular lines, equal segments, angle bisectors, centers of circles, tangents, ratios, or coordinates.
- If an auxiliary line or point is needed in the proof, clearly state `作……` in the explanation. Use dashed or lighter lines in the diagram to distinguish auxiliary elements.

Geometry diagrams must have:

- clear point labels;
- clear intersections;
- right-angle, parallel, equal-length, and angle-bisector markings only when supported by the problem statement;
- no ambiguous auxiliary point positions.

If the original question has a diagram, diagram-dependent variants and mixed-practice questions must also include diagrams.

Captions may say:

`图形为示意图，线段长度与角度大小以题目条件为准。`

Do not write anything about AI generation or redrawing process inside the student handout.

## Diagram Failure Hard Stop

If the original question contains diagrams, the final Word document must contain actual diagrams. Text-only descriptions such as `图①表示……` are not valid substitutes.

If diagrams cannot be generated or inserted due to permissions, missing tools, image clarity, or missing conditions, do not deliver the Word document. Stop and report:

1. which diagrams cannot be generated;
2. why they cannot be generated;
3. what permission, file, or clarification is needed.

Only generate the final Word document after the diagram problem is resolved.

## Structure for Each Original Question

Each original question must follow this order:

1. 原题
2. 图形
3. 思路提示
4. 易错点诊断
5. 作答区
6. 步骤填空
7. 同类变式题
8. 做完后自查

Reference answers, standard explanations, and `一类题通法` must be placed together in the final answer section.

## Thinking Prompts

Thinking prompts must:

- explain which conditions to observe first;
- explain what mathematical relationships the keywords indicate;
- explain why the method should be considered;
- explain the breakthrough point;
- avoid directly revealing the complete answer.

## Error Diagnosis

For each original question, provide 2-4 error diagnosis points.

Diagnoses must be specific to the question conditions. Avoid vague phrases such as `读题要仔细` or `注意计算`.

## Step-Fill Blanks

Medium and difficult questions must include step-fill blanks.

- Blanks must support the key reasoning chain.
- Use underlined blanks for fill-in positions, such as `__________` or Word-underlined spaces.
- Do not use square placeholder characters such as `□`, `□□□□`, `（□□□□）`, or tofu-like boxes for blanks.
- For short formula blanks, prefer `（__________）`, `= __________`, or `∠A = ________°`.
- For step-fill blanks, keep each blank long enough for the expected answer but do not fill a whole page with underlines.
- Chinese parentheses may be used around a blank when they improve readability, but the visible fill area should still be an underline, for example `（__________）`.

## Variant Questions

Default: generate 3 variant questions per original question.

If the user asks for strengthened practice, generate 4. Generate 5 only if explicitly requested.

Variants must follow the same core model as the original and increase in difficulty:

1. basic consolidation of one key step;
2. basic consolidation with changed position, number, or wording;
3. ability improvement requiring one extra transformation, discussion, angle trace, or relationship judgment;
4. comprehensive transfer within current grade and textbook scope, when 4 variants are requested.

Do not generate unrelated new questions.

If the original question has a diagram, variants that depend on diagrams must include diagrams.

## Mixed Practice

- If there are 1-2 original questions, usually include 3-4 mixed-practice questions.
- If there are more original questions, include 4-6 mixed-practice questions.
- Do not directly label the type of each mixed-practice question.
- Cover the core models and progress from basic to medium difficulty.
- Diagram-dependent mixed-practice questions must include diagrams.
- Put answers and explanations at the end.

## Solution Standards

Explanations must follow this logic:

`由条件得到关系，再利用这些关系推出结论。`

State key justifications clearly, such as:

- definitions of perpendicular lines and angle bisectors;
- supplementary adjacent angles;
- vertical angles are equal;
- corresponding, alternate interior, and same-side interior angle relationships for parallel lines;
- congruent triangle criteria;
- corresponding sides and angles of congruent triangles;
- corresponding angles and segments after folding.

Do not replace reasoning with vague words such as `显然`, `易得`, or `不难看出`.

If congruent triangle criteria are used, confirm they fit the grade scope; otherwise mark the problem as extension or use learned methods.

## Formula Standards

Avoid code-style formulas in the Word document:

- not `a^2`, but `a²`;
- not `(a+b)^2`, but `(a+b)²`;
- not `13/4`, but `13⁄4` or a proper equation fraction;
- not `x>=0`, but `x≥0`.

Use the mathematical minus sign `−`.

Use `×` for multiplication, such as `3×7`, not `3·7`.

For complex fractions, radicals, systems, and long derivations, use Word-displayable equations or clear equivalent formatting.

## Answer Area and Layout

- A4 portrait orientation.
- Suitable for black-and-white printing.
- Chinese body font: SimSun or equivalent, 10.5-11 pt.
- Clear heading hierarchy.
- Moderate margins.
- Diagrams centered or placed close to relevant questions.
- Answer areas should use light-border boxes or appropriate blank space.
- Do not use long continuous underlines.

Blank-space standards:

- multiple-choice or fill-in-the-blank questions: 1-2 lines;
- simple calculation questions: 3-5 lines;
- proof, application, and comprehensive questions: no more than half a page;
- each original question with variants should generally fit within 3-5 pages;
- a single-question handout should generally not exceed 6 pages. If it exceeds this, compress blank space and reduce repeated prompts, but do not delete key explanations.

## Publication-Clean Requirements

The document must satisfy:

1. no handwritten notes, red marks, or stains in student-version diagrams;
2. unified diagram style;
3. no overlapping text, blocked images, or formula garbling;
4. no obvious blank pages;
5. continuous page numbers, titles, and question numbers;
6. document metadata should not display generation-tool traces;
7. images should include brief alternative text or descriptions where possible;
8. filename must be English.

## Internal Self-Check

Before generating the document, internally check:

Round 1:
question recognition, numbers, symbols, diagram conditions, and uniqueness of answers.

Round 2:
reasoning chain, justifications, skipped steps, whether the solution returns to the asked conclusion, and whether variants follow the same model.

Round 3:
grade, semester, region, textbook version, and whether anything is beyond scope.

Do not write the internal self-check process into the student document.

## Mandatory Quality Check After Generation

After generating the Word document, render it as page images or PDF when possible and check:

1. whether each page displays normally;
2. whether diagrams are clear and free of handwriting;
3. whether there is text overlap or formula garbling;
4. whether there is excessive blank space;
5. whether the page count exceeds the target;
6. whether answers are placed at the end;
7. whether the file is downloadable.

If problems are found, revise the Word document first, then deliver.

If rendering is unavailable, use structural checks such as opening the DOCX package to confirm embedded media and using Word/LibreOffice document statistics when available. State the limitation briefly in the final reply.

## Final Reply Format

Reply briefly in Chinese only:

```text
已完成 Word。
下载链接：……
图片不清或题目信息不足：无/有，具体为……
需要人工确认的题目：无/有，具体为……
可能超纲或需调整学段的内容：无/有，具体为……
```

Do not repeat the full Word document content in the chat.

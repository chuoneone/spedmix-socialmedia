---
name: mikesh-instagram-posts
description: Create Traditional Chinese Instagram carousel posts in 米克師's warm, practical special-education teacher style using a confirmation-first Markdown-to-HTML workflow. Use when given screenshots and source copy to draft carousel slide text, then after approval build precise HTML/CSS slides with the 米克師 base-image templates and print-to-PDF page breaks.
---

# 米克師 Instagram 圖文

Create helpful, visually calm carousel posts that turn one classroom problem into one immediately understandable teaching insight.

## Workflow: two stages with an approval gate

1. Identify the single teacher pain point, then write a direct first-slide hook. Prefer a concrete classroom moment or question over an abstract topic.
2. Read [style-guide.md](references/style-guide.md) and [carousel-copy-template.md](references/carousel-copy-template.md).
3. Inspect every supplied screenshot and map it to the operation or result it demonstrates. Do not invent UI states that are not visible.
4. Draft the complete slide-by-slide Traditional Chinese copy in a Markdown file named `<topic>-輪播逐頁文.md`. Include slide number, purpose, exact visible text, screenshot filename, background template, and notes about any link or QR code.
5. **Stop after Stage 1.** Show the Markdown draft and ask the user to confirm or request edits. Do not create or modify the HTML until the user explicitly confirms.
6. After confirmation, start from [carousel-template.html](assets/carousel-template.html) and use the supplied base images in `assets/templates/`: `cover.png` for the first page, `body.png` for operation pages, `penultimate.png` for the tool-access page, and `final.png` for the closing page.
7. Use [AI考卷產生器_操作教學.html](assets/examples/AI考卷產生器_操作教學/AI考卷產生器_操作教學.html) as the reference exemplar for the complete editable, print-ready carousel implementation and its local screenshot/base-image paths.
8. Build the confirmed slides as HTML/CSS at exactly 1080 × 1350 px. Keep all copy as real HTML text and place screenshots as normal `<img>` elements so browser printing preserves them even when “background graphics” is disabled.
9. Include print settings: `@page { size: 1080px 1350px; margin: 0; }`, `break-after: page`, and a final slide without a trailing break. Use a real `<img class="base-bg">` layer for every base image; do not rely only on CSS `background-image`.
10. Inspect the rendered or print-preview pages. Correct overflow, awkward wrapping, missing base images, incorrect Chinese characters, and spacing before delivery. Keep the editable HTML and the approved Markdown together.
11. Keep factual claims proportionate. State limitations and teacher judgment when discussing AI or student support.

## Output Rules

- Write Traditional Chinese for Taiwan. Use conversational teacher language, not marketing jargon.
- Lead with empathy: describe student behavior without blame.
- Make the recommendation concrete: name the design choice, then explain what it changes for the learner.
- End with a usable principle, a small next step, or a gentle call to try it.
- When screenshots are supplied, preserve their sequence and use one screenshot per operational step where possible.
- Do not overcrowd slides. Avoid more than one core idea per slide.
- Preserve the visual identity: cream background, coffee-brown typography, Emoji as an entry cue, and `@spedmix2025` at the bottom.
- Do not create slide text with a raster image generator. Render all Chinese copy from the HTML source so it stays accurate and editable.

## Default Carousel Template

1. **Hook** - a recognizable teacher problem framed as a question.
2. **Situation** - explain why the behavior happens without judging the student.
3. **Design move** - show the changed tool, prompt, or teaching step.
4. **Why it helps** - translate the change into a student learning benefit.
5. **Takeaway** - a compact visual sequence plus a memorable supportive line.

## Quality Check

- Confirm every Chinese character, punctuation mark, button label, and handle is correct.
- Keep one headline font family and weight throughout each slide; use a smaller regular weight only for body copy.
- Keep the existing headline font treatment unchanged. Render explanatory/body copy with the Iansui (芫荽體) family when available, using the documented Traditional Chinese fallback stack.
- Keep the title icon on its own line above the title; do not place it beside the title.
- For inner slides, use the vertical reading order: title, screenshot, then explanatory body copy. Do not put a subtitle directly under the title.
- On the cover slide only, render the main headline and subtitle in black; keep the coffee-brown palette for the remaining slide text unless a supplied template specifies otherwise.
- Cover copy convention: make the main headline a concrete teacher pain point; use the subtitle to name the tool, resource, or post theme.
- Cover line layout: always compose the main headline as exactly two lines and the subtitle as exactly two lines; use a deliberate line break rather than relying on automatic wrapping.
- Cover copy density: write a complete, conversational pain-point sentence and a useful tool/theme description; avoid short labels that leave the cover visually empty.
- HTML editing: mark visible copy as `contenteditable="true"` so the teacher can click and revise titles, body text, tips, and output cards directly in the browser. Keep edit outlines screen-only and hide them when printing.
- Include browser controls for per-text-block scaling (縮小／100%／放大／重設). The user clicks a specific editable text block, and only that block's font size changes; keep other blocks and the fixed print canvas unchanged.
- Inner body copy typography: use the Iansui (芫荽體) family at a consistent 35px size for explanatory text, tips, leads, and output cards. Titles use their separate headline size.
- Body copy presentation: render explanations, examples, and tips as plain text on the base image; do not put them inside colored boxes or rounded callout containers.
- Check contrast, mobile legibility, safe margins, and that the title fits on one intended line group without awkward wrapping.
- Stage 1 must deliver the editable Markdown draft only; Stage 2 must deliver the approved Markdown, editable HTML source, and any exported slide images/PDF.
- Verify that examples involving disability, attention, behavior, or mistakes are respectful and strengths-based.

# 米克師 IG 視覺與文案規格

## Visual identity

- Format: portrait Instagram carousel, 4:5.
- Background: warm cream or off-white with subtle paper texture. Leave generous space.
- Main text: dark coffee brown, bold, clean Traditional Chinese sans serif. Preserve the current headline font family and weight.
- Cover exception: the first-slide headline and subtitle are black for stronger contrast; do not apply this color change to later slides.
- Cover copy: headline = a recognizable teacher pain point or question; subtitle = the tool name or teaching theme.
- Cover line layout: use exactly two lines for the headline and exactly two lines for the subtitle, with explicit `<br>` breaks.
- Keep enough copy on the cover to match the established style: a full pain-point sentence plus a descriptive tool/theme benefit, not a one- or two-word label.
- Make visible copy directly editable in the browser with `contenteditable="true"`; use a subtle focus outline for editing and remove it in print CSS.
- Provide screen-only text-size controls (縮小、100%、放大、重設) that change the text scale while preserving the 1080×1350 canvas for printing.
- Inner body copy: all explanatory text, tips, leads, and cards use Iansui (芫荽體) at 35px consistently; do not vary body sizes between slides.
- Keep explanatory text, examples, and tips as plain text without colored backgrounds, borders, or rounded boxes.
- Supporting text: use the Iansui (芫荽體) family for explanatory/body copy, with a Traditional Chinese fallback stack. Keep it dark brown or nearly black.
- Structure: a central white, rounded paper card may be held by a beige tape strip. Use thin brown arcs or dashed dividers sparingly.
- Cues: one large Emoji near the title is enough. Use it to signal the slide function: problem, check, tools, takeaway, link, or search.
- Title cue layout: keep the icon on its own line above the title. Do not place it beside the title.
- Brand mark: place `@spedmix2025` small and centered at the bottom.
- Visuals: favor one clear screenshot, UI mockup, teaching artifact, or warm child-friendly illustration. Use images to explain, not decorate.

## HTML rendering

- Build every slide in a 1080 × 1350 px fixed canvas; do not depend on browser viewport sizing.
- Use a self-contained HTML file with inline CSS or a colocated stylesheet. Avoid external font, icon, or image URLs unless the user supplies them.
- Use CSS for the cream background, subtle texture, paper cards, tape, arcs, dividers, arrows, buttons, and layout. Keep text as real HTML text.
- Use the existing headline stack for titles. For body copy use `"Iansui", "芫荽體", "芫荽", "Noto Sans TC", "Microsoft JhengHei", sans-serif` so explanatory text is consistently rendered in 芫荽體 when installed.
- Inner-slide order: title first, screenshot second, explanatory body copy below the screenshot. Avoid a subtitle directly beneath an inner-slide title.
- Export a PNG only after browser-rendering the final HTML at 1080 × 1350 px. Keep the HTML source as the editable master.
- Use the bundled base images: `assets/templates/cover.png`, `body.png`, `penultimate.png`, and `final.png`. Add them as real `<img class="base-bg">` layers so they survive browser print preview without requiring “background graphics”.
- In the HTML print stylesheet, set `@page { size: 1080px 1350px; margin: 0; }`, apply `break-after: page` to each slide, and remove the break from the final slide.

## Voice

- Sound like a teacher sharing something tested in the classroom: plain, warm, practical, lightly playful.
- Use concise lines, small confessions, and relatable observations. Example: 「不是故意搗蛋，有時只是想趕快知道答案。」
- Avoid absolute promises. When discussing AI, include appropriate limits: it is an assistant and teachers still check results.

## Copy patterns

### Hook

- Start with the exact classroom pain point: 「學生一直亂按測驗，怎麼辦？」
- Make the benefit immediately visible: 「4 種簡化幅度、7 種輸出選項」.
- Use an approachable parenthetical only when it strengthens personality, such as 「只要 30 秒！（應該）」.

### Explanation

- Describe the learner's need before the solution.
- State the change in one action phrase: 「先選，再檢查」.
- Explain the benefit in student terms: 「讓孩子慢下來思考。」

### Closing

- Use a short principle or sequence: 「看題目 → 選答案 → 送出檢測」.
- End supportive rather than promotional: 「把第二次機會，留給每一個努力的孩子。」

## Avoid

- Dense paragraphs, multiple competing illustrations, gradients that reduce readability, or highly technical language.
- Blaming phrases about students, such as 「愛亂按」 or 「故意搗蛋」 without compassionate context.
- Inconsistent headline fonts, low-contrast text, tiny screenshots, and unverified Chinese text in generated images.

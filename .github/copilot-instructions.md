# JPMC Slide Framework — Copilot Instructions

When asked to create, write, or update presentation slides, always use this framework.
All slides are written in Marp Markdown. The theme file is `slides/jpmc-theme.css`.

---

## Brand Rules (Non-Negotiable)

- **Typography color**: Only Black, White, or Bronze (#8F5A38) — never other colors for text
- **Serif font** (Garamond/Georgia): Only for slide titles (h1), section headings (h2), and large headlines (h3)
- **Sans font** (Calibri/Segoe UI): All body copy, labels, captions, table content
- **Bronze** (#8F5A38) is the primary brand accent — use for emphasis, borders, section dividers
- **Travertine** (#F4EFE7) is the warm background — use sparingly, not on every slide
- Slides must breathe — never fill a slide with more than 4 bullet points
- Every slide must have a `#### Section Label` (bold all-caps style) unless it's a cover or section-divider

---

## File Header (always start a new deck with this)

```markdown
---
marp: true
theme: jpmc
paginate: true
header: "JPMorganChase &nbsp;&nbsp;&nbsp; JPMC INTERNAL USE ONLY — CONFIDENTIAL &nbsp;&nbsp;&nbsp; [PRESENTATION TITLE]"
---
```

---

## Slide Type Reference

### 1. COVER SLIDE
Use: First slide of any deck. Also use for Appendix dividers.
Class: `cover`

```markdown
<!-- _class: cover -->
<!-- _paginate: false -->

<div class="cover-body">

# Main Presentation Title
## Subtitle or Topic Area

<p>Version 1.0 &nbsp;|&nbsp; Month Year</p>

</div>
<div class="cover-footer">
  <span class="logo">JPMorganChase</span>
  <span class="confidential">Strictly Private and Confidential</span>
</div>
```

---

### 2. SECTION DIVIDER
Use: Between major sections. The watermark number matches the section number.
Class: `section-divider`

```markdown
<!-- _class: section-divider -->

<div class="divider-body">

## Section Name Here

<p>One or two sentences describing what this section covers and why it matters to the audience.</p>

</div>
<span class="watermark-num">1</span>
```

Change `watermark-num` content to match section number: 1, 2, 3, 4, 5, 6...

---

### 3. STANDARD CONTENT SLIDE (default)
Use: Most slides. Text, bullets, analysis, narrative.
No class needed — white background is the default.

```markdown
<div class="slide-content">

#### Page Section Label

## Optional Large Headline If Needed

Body copy goes here. Keep it concise — one idea per slide.

- Bullet point with supporting detail
- Another supporting point
- Third point maximum before splitting to two slides

<div class="highlight-box">
Key callout or purpose statement in a highlight box.
</div>

</div>
```

---

### 4. TWO-COLUMN LAYOUT
Use: Comparing two ideas, before/after, two workstreams.
Class: `two-col`

```markdown
<!-- _class: two-col -->

<div class="slide-content">

#### Section Label

<div class="col-grid">
<div class="col">

**Left Column Title**

Content for left column. Keep roughly equal in length to right column.

- Bullet one
- Bullet two

</div>
<div class="col">

**Right Column Title**

Content for right column. Parallel structure to left when possible.

- Bullet one
- Bullet two

</div>
</div>

</div>
```

---

### 5. TEXT AND IMAGE
Use: When a photo or diagram supports the narrative.
Class: `image-right`

```markdown
<!-- _class: image-right -->

<div class="slide-content">
<div class="text-area">

#### Section Label

## Optional Headline

Body copy describing the image context and key message.

- Supporting point
- Supporting point

<p class="caption">Image caption or data source</p>

</div>
<div class="image-area">
  [Replace with: <img src="path/to/image.jpg" />]
</div>
</div>
```

---

### 6. DATA / METRICS TABLE
Use: Survey results, scorecard data, comparative metrics.
Class: `data`

```markdown
<!-- _class: data -->

<div class="slide-content">

#### Data Visualization Title Goes Here

| &nbsp; | Column Header One | Column Header Two | Column Header Three |
|---|---|---|---|
| Row Label, supporting detail | <span class="metric positive">+19</span> | <span class="metric negative">-3</span> | <span class="metric">0</span> |
| Row Label, supporting detail | <span class="metric positive">+7</span> | <span class="metric negative">-5</span> | <span class="metric positive">+2</span> |

<div class="footnote">
* Footnote explaining methodology or scale<br>
Source: [data source]
</div>

</div>
```

Metric classes: `metric positive` (green border) | `metric negative` (bronze border) | `metric` (neutral)

---

### 7. LARGE HEADLINE SLIDE
Use: Key conclusions, executive takeaways, purpose statements.
No class — uses default content layout.

```markdown
<div class="slide-content">

#### Section Label

## This headline carries the entire message of the slide in one or two sentences.

<p class="muted">Supporting context sits here — brief, secondary. Never let it compete visually with the headline above.</p>

</div>
```

---

### 8. TABLE OF CONTENTS
Use: After the cover slide on longer decks (5+ sections).
Class: `toc`

```markdown
<!-- _class: toc -->

<div class="slide-content">

#### Table of Contents

<div class="toc-grid">
  <div class="toc-item">
    <span class="toc-label">1 | Section Name</span>
    <span class="toc-pages">03–05</span>
  </div>
  <div class="toc-item">
    <span class="toc-label">4 | Section Name</span>
    <span class="toc-pages">17–21</span>
  </div>
  <div class="toc-item">
    <span class="toc-label">2 | Section Name</span>
    <span class="toc-pages">06–10</span>
  </div>
  <div class="toc-item">
    <span class="toc-label">5 | Section Name</span>
    <span class="toc-pages">22–25</span>
  </div>
</div>

</div>
```

---

## Color Reference

| Name | Hex | Use |
|---|---|---|
| Bronze | `#8F5A38` | Primary accent, section dividers, borders, emphasis |
| Travertine | `#F4EFE7` | Warm background slides, highlight boxes |
| Black | `#000000` | Body text on light slides |
| White | `#FFFFFF` | Text on dark/bronze slides, default slide background |
| Sky Blue | `#A4D2F0` | Secondary accent only — data visualization, sparingly |
| Midnight | `#1D3A5F` | Dark mode slides only |

Chart colors (use in sequence for data visualizations):
1. `#8F5A38` (Bronze)
2. `#A4D2F0` (Sky Blue)
3. `#4A9B8F` (Teal)
4. `#7B68C8` (Violet)
5. `#3BAF8A` (Green)

---

## Typography Reference

| Style | Font | Size | Weight | Case | Use |
|---|---|---|---|---|---|
| Presentation Title | Garamond/Georgia | 72pt | Regular | Title | Cover h1 |
| Section Heading | Garamond/Georgia | 64pt | Regular | Sentence, Italic | Section divider h2 |
| Large Headline | Garamond/Georgia | 40pt | Regular | Sentence | Standalone statement h2 |
| Headline | Garamond/Georgia | 36pt | Regular | Sentence | Content headings h3 |
| Page Label | Calibri/Segoe UI | 10pt | Bold | ALL CAPS | Every slide's h4 label |
| Large Body | Calibri/Segoe UI | 18pt | Regular | Sentence | Primary body text |
| Body | Calibri/Segoe UI | 16pt | Regular | Sentence | Standard body text |
| Caption | Calibri/Segoe UI | 10pt | Regular | Sentence | Footnotes, image captions |

---

## Tone and Content Rules

- Write at executive level: direct, authoritative, no jargon padding
- Slide titles (h4 labels) should state the *topic* — "Q1 Performance Overview"
- Large headlines should state the *insight* — "Revenue grew 12% driven by consumer banking"
- Bullets support the headline — they do not repeat it
- Never use more than 3 nested bullet levels
- Numbers in slides: use commas for thousands ($1,200,000 not $1200000), use % not "percent"
- Dates: "Q1 2025" or "January 2025" — never "Jan '25" in formal slides
- Avoid orphan words on lines — adjust phrasing to keep text blocks clean

---

## How to Ask for a Slide Deck

When the user says "create a presentation about X" or "write slides for Y", generate a complete Marp file following this structure:

1. Frontmatter block with correct header
2. Cover slide
3. Table of Contents (if 3+ sections)
4. Section divider for each major section
5. 2–4 content slides per section (using appropriate layout types)
6. Choose layout types based on content type:
   - Narrative/analysis → standard content
   - Comparison → two-col
   - Data/metrics → data layout
   - Key message → large headline
   - Photo needed → image-right

Always end with an Appendix cover slide if the user mentions appendix content.

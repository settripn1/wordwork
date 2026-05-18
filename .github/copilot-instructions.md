# JPMC Slide Framework — Copilot Instructions

When asked to create, write, or update presentation slides, always use this framework.
All slides are written in Marp Markdown. The theme file is `slides/jpmc-theme.css`.

---

## Brand Rules (Non-Negotiable)

- **Typography color**: Only Black, White, or Bronze (#8F5A38) — never other colors for text
- **Serif font** (Tiempos Text / Georgia fallback): Only for slide titles (h1), section headings (h2), and large headlines (h3)
- **Sans font** (SOMS / Calibri fallback): All body copy, labels, captions, table content
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

### 9. NUMBERED INSIGHTS + CHART
Use: When you have 3-4 key findings alongside a bar chart.
Class: `insights-chart`

```markdown
<!-- _class: insights-chart -->

<div class="slide-content">

#### Data Visualization Title Goes Here

<div class="insights-grid">
<div class="insights-list">

**1. *First insight headline sits here***

Supporting detail for this insight. Two to three sentences maximum providing context.

**2. *Second insight headline sits here***

Supporting detail for this insight. Two to three sentences maximum providing context.

**3. *Third insight headline sits here***

Supporting detail for this insight. Keep consistent length with other insights.

**4. *Fourth insight headline sits here***

Supporting detail for this insight. Keep consistent length with other insights.

</div>
<div class="chart-box">

**Chart title goes here**

[Bar chart placeholder — replace with chart image or description of data]
Categories: Label1, Label2, Label3, Label4, Label5, Label6
Values: 22%, 18%, 16%, 16%, 17%, 11%

</div>
</div>

</div>
```

---

### 10. LARGE STATS + ICON + HORIZONTAL BAR CHART
Use: Survey results where you want the big number AND category breakdown.
Class: `stats-chart`

```markdown
<!-- _class: stats-chart -->

<div class="slide-content">

#### Data Visualization Title Goes Here

<div class="stats-chart-grid">
<div class="stat-list">

<div class="stat-row">
  <span class="stat-pct">33%</span>
  <span class="stat-icon">👥</span>
  <div class="stat-copy"><strong>Short headline</strong><br>Supporting description text here.</div>
</div>

<div class="stat-row">
  <span class="stat-pct">26%</span>
  <span class="stat-icon">🚩</span>
  <div class="stat-copy"><strong>Short headline</strong><br>Supporting description text here.</div>
</div>

<div class="stat-row">
  <span class="stat-pct">18%</span>
  <span class="stat-icon">💼</span>
  <div class="stat-copy"><strong>Short headline</strong><br>Supporting description text here.</div>
</div>

</div>
<div class="chart-box horizontal">

**Chart title goes here**

| Category | Value |
|---|---|
| Category A | 22% |
| Category B | 18% |
| Category C | 16% |
| Category D | 16% |
| Category E | 11% |

</div>
</div>

</div>
```

Notes: 
- The large % numbers render in Bronze (#8F5A38)
- Use Unicode icons as placeholders — user replaces with JPMC icons from the template
- Divider lines appear between each stat-row automatically

---

### 11. DONUT CHARTS + ICON CALLOUTS
Use: Showing 3-4 key percentages as ring/donut visuals with supporting callouts.
Class: `donut-charts`

```markdown
<!-- _class: donut-charts -->

<div class="slide-content">

#### Data Visualization Title Goes Here

<div class="donut-row">

<div class="donut-item">
<div class="donut-ring" style="--pct:88; --color:#2D7A6F;">88%</div>
<p>Label text<br>goes here</p>
</div>

<div class="donut-item">
<div class="donut-ring" style="--pct:95; --color:#7068B0;">95%</div>
<p>Label text<br>goes here</p>
</div>

<div class="donut-item">
<div class="donut-ring" style="--pct:58; --color:#AAAAAA;">58%</div>
<p>Label text<br>goes here</p>
</div>

<div class="donut-item">
<div class="donut-ring" style="--pct:48; --color:#4A9088;">48%</div>
<p>Label text<br>goes here</p>
</div>

</div>

<div class="callout-row">

<div class="icon-callout">
<div class="callout-icon">💛</div>
<p>Supporting callout text goes here. Two to three sentences providing context for the data above.</p>
</div>

<div class="icon-callout">
<div class="callout-icon">💛</div>
<p>Supporting callout text goes here. Two to three sentences providing context for the data above.</p>
</div>

</div>

</div>
```

Donut color suggestions by sentiment: positive → `#2D7A6F` (teal) or `#7068B0` (violet), neutral → `#4A9088`, muted → `#AAAAAA`

---

### 12. CLOSING / END SLIDE
Use: Final slide of any deck. Just the logo, no content.
Class: `closing`

```markdown
<!-- _class: closing -->
<!-- _paginate: false -->

<div class="closing-logo">JPMorganChase</div>
```

---

### 13. HERO SPLIT
Use: When you need a powerful visual statement — large serif title on the left with travertine background, labeled content on the right with white background. Good for vision slides, strategy intros, and "what we believe" slides.
Class: `hero-split`

```markdown
<!-- _class: hero-split -->

<div class="hero-left">

#### Section Label

## Large Impactful Headline That States the Core Message

*Bronze italic subtitle or mission statement sits here.*

</div>
<div class="hero-right">

**CATEGORY ONE**

Description of this category in two sentences. Keep it tight and direct.

**CATEGORY TWO**

Description of this category. Parallel structure helps readability.

**CATEGORY THREE**

Description of this third item. End with the key implication.

</div>
```

Note: This layout hides the header bar — the `#### Section Label` inside `.hero-left` serves as the page label.

---

### 14. ICON CARDS
Use: When you have 3–4 parallel items (pillars, capabilities, focus areas) that each need a title and supporting description. Each card gets an icon, an italic bronze title, and body text.
Class: `icon-cards`

3-column (default):
```markdown
<!-- _class: icon-cards -->

<div class="slide-content">

#### Section Label

## Optional Slide Headline

<div class="cards-grid">
<div class="card">
<div class="card-icon">◎</div>

##### Early Data Validation

Description of what this area covers. Two to three sentences of supporting detail that explain the value or approach.

</div>
<div class="card">
<div class="card-icon">⬡</div>

##### Pre-Training Assessment

Description of what this area covers. Two to three sentences of supporting detail that explain the value or approach.

</div>
<div class="card">
<div class="card-icon">△</div>

##### Measurement

Description of what this area covers. Two to three sentences of supporting detail that explain the value or approach.

</div>
</div>

</div>
```

4-column variant — add class `four-up` to the grid div:
```html
<div class="cards-grid four-up">
```

---

### 15. LABELED LIST + VISUAL
Use: When you have 4–6 named principles, pillars, or operating norms alongside a diagram or illustration. The Bronze ALL-CAPS labels create strong visual rhythm.
Class: `labeled-list`

```markdown
<!-- _class: labeled-list -->

<div class="slide-content">

#### Section Label

## Optional Headline

<div class="list-area">

<div class="list-item">
<div class="list-label">Employee Focused</div>
<div class="list-body">Develop a culture that relentlessly focuses on our employees and provides cohesive, frictionless experiences.</div>
</div>

<div class="list-item">
<div class="list-label">Work Efficiently</div>
<div class="list-body">Ensure optimal value for every dollar spent. Drive a mindset of doing more with less.</div>
</div>

<div class="list-item">
<div class="list-label">Outcome Oriented</div>
<div class="list-body">Align what we do to results that our employees value and measure progress against those outcomes.</div>
</div>

<div class="list-item">
<div class="list-label">Speed to Deliver</div>
<div class="list-body">Develop practices for teams to quickly iterate through discovery, design, and build.</div>
</div>

</div>

<div class="visual-area">
  [Diagram or illustration — replace with img tag]
</div>

</div>
```

---

### 16. FOUR QUADRANT
Use: Quarterly reviews, strategic priorities, workstream status — anything that naturally breaks into 4 named areas. Each quadrant has a bronze label, bold title, italic description, and a short list.
Class: `four-quad`

```markdown
<!-- _class: four-quad -->

<div class="slide-content">

#### Section Label — Q1 Progress

<div class="quad">
<div class="quad-label">Priority #1</div>
<div class="quad-title">New Hire Transformation</div>
<div class="quad-subtitle">Reduce time-to-competence for new banking specialists</div>

- Accelerated time to competence by 20% in Manila/Cebu
- Kicked off UK review with cross-functional team

</div>

<div class="quad">
<div class="quad-label">Priority #2</div>
<div class="quad-title">Chase Berlin</div>
<div class="quad-subtitle">Support mobilization with skilled and ready specialists</div>

- Scoped detailed project plan, removed key barriers
- Commenced build for core induction journeys

</div>

<div class="quad">
<div class="quad-label">Priority #3</div>
<div class="quad-title">Portfolio Delivery & Evolution</div>
<div class="quad-subtitle">Deliver first-class learning portfolio aligned to business priorities</div>

- Increased digital mix to 50% vs instructor-led
- Launched Excellerate Pilot in ICB for microlearning

</div>

<div class="quad">
<div class="quad-label">Priority #4</div>
<div class="quad-title">Operational Excellence</div>
<div class="quad-subtitle">Improved operational effectiveness and team capabilities</div>

- Matured leadership team through 2 new VP appointments
- Enhanced controls through JPMC Firmwide TPM governance

</div>

</div>
```

---

### 17. USE CASE
Use: AI use cases, project spotlights, or case studies where a specific person or team is featured. Person photo and bio top-left, labeled content sections top-right, three summary cards at the bottom.
Class: `use-case`

```markdown
<!-- _class: use-case -->

<div class="slide-content">

#### AI Use Case Spotlight

## Enhancing the Recruitment Intake Call

<div class="use-case-top">

<div class="person-block">
  <img src="path/to/photo.jpg" alt="Name" />
  <div class="person-name">Payal Lala</div>
  <div class="person-role">Ops Recruiting CIB<br>Mumbai, India</div>
</div>

<div class="use-case-detail">
<div class="detail-label">Problem Statement</div>
<div class="detail-body">How can we enhance alignment and communication among stakeholders to streamline the recruitment process and effectively identify qualified candidates?</div>

<div class="detail-label">LLM Prompt</div>
<div class="detail-body">Design a recruitment intake form that captures accurate details related to the role, enabling the sourcing team to find the right candidates and talent.</div>
</div>

</div>

<div class="use-case-cards">

<div class="uc-card">
<span class="card-icon">👥</span>
<div class="detail-label">User Base</div>
<p>Recruiters, Sourcers, Hiring Managers. Benefit: better matching and stronger relationships.</p>
</div>

<div class="uc-card">
<span class="card-icon">📊</span>
<div class="detail-label">Output</div>
<p>Structured intake form with skill-specific questions for hiring manager conversations.</p>
</div>

<div class="uc-card">
<span class="card-icon">✓</span>
<div class="detail-label">Impact</div>
<p>Improved efficiency. Increased quality of hire. Faster, more successful outcomes.</p>
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

## Chart Colors (use in this sequence for data visualizations)

Always use colors in this order for bars, lines, and pie/donut segments:

| Order | Color | Hex | Style |
|---|---|---|---|
| 1 | Dark Navy | `#2B4C6F` | Darkest bars, primary series |
| 2 | Lavender | `#8B7EC8` | Second series |
| 3 | Dark Teal | `#2D7055` | Third series |
| 4 | Medium Teal | `#4A9088` | Fourth series |
| 5 | Violet | `#7068B0` | Fifth series |
| 6 | Mint | `#5DC8B8` | Lightest, sixth series |

For donut/ring charts: match color to sentiment. Teal for positive, violet for notable, gray for neutral/low.
For stat percentages (large numbers): always Bronze `#8F5A38`.

---

## Complete Icon Library

Icons are line-weight, monochrome (black or white depending on background). Copy from the template's Iconography section. Available icons:

**People & Organization:**
Community, Employee Experience, Career Growth, Team Diversity, Teamwork, Collaboration/Partnership, Organization/Structure, Recruitment, Manager, Hiring/New Hires

**Actions & Process:**
Change, Processes/Mechanism, Access/Unlocking, Launching New Projects, Problem Solving/Fitting Pieces Together, Strategic Thinking, Motivation, Ideas and Innovation, Foundational Research, Surveys or Feedback

**Technology & Data:**
Desktop, Tablet, Phone, Laptop, Data Storage, Bar Chart, Pie Chart, Program Pulse, Technology, Knowledge/Learning Resources, Cognitive Processes, Search

**Finance & Business:**
General Investment, Green Investment, Finance, Commerce, Charitable Giving, Retirement, Business, Careers/Skills

**Communication & Criteria:**
Messages/Comms, Email Communication, Comments, Criteria, Calendar, Objectives, Leadership

**Wellbeing & Values:**
Wellness/Sentiment, Work-Life Balance, Fairness or Evaluation, Guidance/Direction, Sustainability, Healthcare, Financial Health

**Global & Society:**
Global/International, Agriculture, Industries, Community Development, Security, Social

**Achievement:**
Growth, Awards, Medals/Valor, Rewards, Star, Thumbs Up, Goal, Insights

**Other:**
Location, Time/Clock, Challenges, Support, Employee Experience

**Icon usage rules:**
- Use Black icons on white/travertine slides
- Use White icons on Bronze/dark slides  
- Icon color can be changed via Format → Graphics Outline in PowerPoint
- Icons are standalone decorative elements — always pair with a text label

---

## How to Choose a Layout

**RULE: First check the available layout classes below and use the closest match. Only create a new custom layout if none of the existing ones fit the content — and if you do, follow the same naming and CSS conventions as the existing classes.**

When generating slides, match content type to layout:

| Content type | Layout class |
|---|---|
| Opening slide | `cover` |
| Final slide | `closing` |
| Section break between topics | `section-divider` (watermark number = section number) |
| Navigation / agenda | `toc` |
| Single narrative point, bullets | default (no class) |
| Key conclusion, exec takeaway | default with `## large headline` |
| Two parallel ideas, before/after | `two-col` |
| Photo or imagery alongside text | `image-right` |
| Survey / scorecard table | `data` |
| 3-4 findings + bar chart | `insights-chart` |
| Large % stats + category breakdown | `stats-chart` |
| Ring / donut metric charts | `donut-charts` |
| Warm background, softer tone | `travertine` |
| Dark emphasis slide | `dark` |
| Vision statement, strategy intro | `hero-split` |
| 3–4 pillars / capabilities / focus areas | `icon-cards` |
| 4–6 named principles with diagram | `labeled-list` |
| Quarterly / priority status, 2×2 | `four-quad` |
| AI use case, project spotlight, case study | `use-case` |

---

## Typography Reference

| Style | Font | Size | Weight | Case | Use |
|---|---|---|---|---|---|
| Presentation Title | Tiempos Text / Georgia | 72pt | Regular | Title | Cover h1 |
| Section Heading | Tiempos Text / Georgia | 64pt | Regular | Sentence, Italic | Section divider h2 |
| Large Headline | Tiempos Text / Georgia | 40pt | Regular | Sentence | Standalone statement h2 |
| Headline | Tiempos Text / Georgia | 36pt | Regular | Sentence | Content headings h3 |
| Page Label | SOMS / Calibri | 10pt | Bold | ALL CAPS | Every slide's h4 label |
| Large Body | SOMS / Calibri | 18pt | Regular | Sentence | Primary body text |
| Body | SOMS / Calibri | 16pt | Regular | Sentence | Standard body text |
| Caption | SOMS / Calibri | 10pt | Regular | Sentence | Footnotes, image captions |

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

# RSM - Presentation Design System for PPT

Document for direct consumption by an AI presentation agent. Defines color palette, typography, layout rules, and canonical layouts.

---

## 1. Color palette

### 1.1 Brand colors (primary)

- rsm-blue: #009CDE
  Use: primary accent color, titles, highlights

- rsm-blue-high-contrast: #007EB4
  Use: backgrounds, charts, high-contrast elements

- rsm-midnight: #00153D
  Use: covers, closing slides, key messages

### 1.2 Secondary / semantic colors

- success: #3F9C35
- success-high-contrast: #36872E
- warning: #F1B434
- error: #E40046
- info / neutral-strong: #63666A

### 1.3 Neutrals

- white: #FFFFFF
- black: #1D1D1D
- grey-light: #F0F0F0
- grey: #C6C8C8
- grey-mid: #888B8D
- grey-dark: #515356

### 1.4 Color usage rules

- Default background: white
- Primary text: black
- Titles: rsm-midnight
- Max 1 accent color per slide
- Do not use warning or error as decoration
- Prioritize contrast and legibility over brand

---

## 2. Typography system

### 2.1 Font

- Single font: Inter
- Max 2 weights per slide (Regular + Semibold)

### 2.2 Typography hierarchy

- Main title (H1)
  Size: 42 px
  Weight: Semibold
  Color: rsm-midnight

- Subtitle / section (H2)
  Size: 36 px
  Weight: Semibold
  Color: rsm-blue

- Block header (H3)
  Size: 24 px
  Weight: Semibold
  Color: black

- Body text (Body)
  Size: 14 px
  Weight: Regular
  Color: black

- Secondary / supporting text
  Size: 12 px
  Weight: Regular
  Color: grey-dark

- Labels / footer / notes
  Size: 10 px
  Weight: Regular
  Color: grey-mid

### 2.3 Typography rules

- Body line height: 1.45
- Max 6 lines of body text per slide
- Centered text only on Cover and Highlight
- Do not mix more than one strong hierarchy per block

---

## 3. Spacing and grid

- Minimum margin per slide: 32 px
- Top and bottom safe area: 40 px
- Space between blocks: 20 px
- Max 2 columns per slide
- Left alignment by default
- Prioritize whitespace over content density

---

## 4. Canonical slide layouts

The following layouts must be treated as reusable base types by the agent.

### 4.1 Layout: Cover

Use: presentation start

- Background: grey-light
- H1 title in rsm-midnight
- H2 subtitle in rsm-blue
- Logo in bottom-right corner
- Title and subtitle location: left-aligned, top-left block
- Title position: x=32 px, vertically centered
- Subtitle position: x=32 px, 20 px below the title (block vertically centered)
- Max text block width: 70% of slide width

Elements:

- title
- subtitle

### 4.2 Layout: Section / Divider

Use: separate chapters or conceptual blocks

- Background: white
- Large title (H1)
- Accent bar: a horizontal line in rsm-blue, 6 px height, 60% of slide width, aligned left below the title

Elements:

- title
- accent_bar

### 4.3 Layout: Content - Single Column

Use: standard or conceptual explanation

- Background: white
- H3 title on top
- Accent bar below the title (see Accent bar spec)
- Body text in a single column

Elements:

- title
- body_text

### 4.4 Layout: Content - Two Columns

Use: comparison, text + chart, text + list

- Background: white
- Left column: text
- Right column: chart, bullets, or image
- Accent bar below the title (see Accent bar spec)

Elements:

- title
- left_content
- right_content

### 4.5 Layout: Bullets

Use: key points, summary, checklist

- Background: white
- Max 5 bullets
- Short bullets, ideally one line
- Accent bar below the title (see Accent bar spec)

Elements:

- title
- bullet_list

### 4.6 Layout: Data / Chart

Use: metrics, KPIs, results

- Background: white
- Chart as the dominant element
- Minimal supporting text
- Accent bar below the title (see Accent bar spec)

Elements:

- title
- primary_chart
- caption

### 4.7 Layout: Highlight / Key Message

Use: key message, conclusion, CTA

- Background: rsm-blue
- Large, short text
- Single idea

Elements:

- statement

---

## 4.8 Accent bar spec

- Color: rsm-blue
- Shape: horizontal line (rectangle)
- Height: 6 px
- Width: 10% of slide width
- Alignment: left-aligned with the title text block
- Spacing: 12 px below the title baseline

---

## 5. Global rules for the AI agent

- One main idea per slide
- Prioritize clarity over density
- Repeat layouts only when it adds consistency
- Avoid non-informative decorative elements
- If content is ambiguous, use Content - Single Column
- If there is data, prefer Data / Chart
- If there is a closing or conclusion, use Highlight
- Required header on all slides: text "Classification: Confidential" (10 px, grey-mid), centered at the top within the top safe area (40 px)
- Required page number on all slides except Cover: 10 px, grey-mid, right-aligned within the bottom safe area (40 px)

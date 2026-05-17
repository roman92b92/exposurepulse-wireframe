---
name: ExposurePulse Design System
colors:
  surface: '#f9f9ff'
  surface-dim: '#d7dae4'
  surface-bright: '#f9f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f1f3fe'
  surface-container: '#ebedf8'
  surface-container-high: '#e6e8f3'
  surface-container-highest: '#e0e2ed'
  on-surface: '#181c23'
  on-surface-variant: '#414754'
  inverse-surface: '#2d3038'
  inverse-on-surface: '#eef0fb'
  outline: '#717786'
  outline-variant: '#c1c6d7'
  surface-tint: '#005cbb'
  primary: '#005ab6'
  on-primary: '#ffffff'
  primary-container: '#0072e4'
  on-primary-container: '#fefcff'
  inverse-primary: '#abc7ff'
  secondary: '#565f69'
  on-secondary: '#ffffff'
  secondary-container: '#dae3ef'
  on-secondary-container: '#5c656f'
  tertiary: '#9b4000'
  on-tertiary: '#ffffff'
  tertiary-container: '#c25200'
  on-tertiary-container: '#fffbff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d7e3ff'
  primary-fixed-dim: '#abc7ff'
  on-primary-fixed: '#001b3f'
  on-primary-fixed-variant: '#00458f'
  secondary-fixed: '#dae3ef'
  secondary-fixed-dim: '#bec7d3'
  on-secondary-fixed: '#141c25'
  on-secondary-fixed-variant: '#3f4851'
  tertiary-fixed: '#ffdbcb'
  tertiary-fixed-dim: '#ffb692'
  on-tertiary-fixed: '#341100'
  on-tertiary-fixed-variant: '#793100'
  background: '#f9f9ff'
  on-background: '#181c23'
  surface-variant: '#e0e2ed'
  orca-blue: '#0080FF'
  orca-black: '#101921'
  blue-ada-light: '#0073E5'
  blue-5: '#0360C5'
  blue-ada-dark: '#AFCFEE'
  cyan-accent: '#02D6FF'
  gray-50: '#FDFDFF'
  gray-100: '#F9F9FC'
  gray-150: '#F3F4F9'
  gray-175: '#E8E9F1'
  gray-200: '#E0E2EC'
  gray-400: '#A9B2C7'
  gray-500: '#8693B2'
  gray-600: '#5F6D8F'
  severity-critical: '#E2005E'
  severity-high: '#FF3342'
  severity-medium: '#FE7B1F'
  severity-low: '#F8CD39'
  success-green: '#50C878'
  bg-highlight-blue: '#E6F1FB'
  bg-highlight-red: '#FFF0F0'
typography:
  page-title:
    fontFamily: Montserrat
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.2'
  kpi-metric:
    fontFamily: Montserrat
    fontSize: 32px
    fontWeight: '500'
    lineHeight: '1.2'
  section-header:
    fontFamily: Mulish
    fontSize: 16px
    fontWeight: '600'
    lineHeight: '1.2'
  table-primary:
    fontFamily: Mulish
    fontSize: 13px
    fontWeight: '600'
    lineHeight: '1.4'
  table-secondary:
    fontFamily: Mulish
    fontSize: 11px
    fontWeight: '400'
    lineHeight: '1.4'
  body-standard:
    fontFamily: Mulish
    fontSize: 13px
    fontWeight: '400'
    lineHeight: '1.5'
  label-caps:
    fontFamily: Mulish
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: 0.05em
  monospace-data:
    fontFamily: Courier New
    fontSize: 11px
    fontWeight: '400'
    lineHeight: '1.2'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  micro: 4px
  small: 8px
  compact: 12px
  standard: 16px
  large: 24px
  section: 32px
  page: 48px
---

# ExposurePulse — Design System & Component Guide
## For Stitch / AI Design Agent

---

## 1. PRODUCT CONTEXT

**Product:** ExposurePulse
**Platform:** Orca Security (CNAPP — Cloud Native Application Protection Platform)
**Feature type:** Vulnerability prioritization dashboard
**Users:** Security Engineers (daily triage), SOC Analysts, CISOs
**Core value:** Consolidates 800+ CVEs into 37 actionable exploitable vulnerabilities in one screen

**Three views to design:**
1. Exposure List (default analyst view)
2. Vulnerability Detail (drill-down)
3. Exposure Summary (executive/CISO view)

---

## 2. DESIGN PRINCIPLES

### 2.1 Visual Hierarchy Rules
- **Information density:** High. Security analysts work with data-heavy interfaces. Do not simplify to the point of losing utility.
- **Signal over noise:** The most critical information (exposure state, severity, exploitability) must be immediately visible without scrolling or hovering.
- **Action-first:** Every row, every card, every section must have a clear next action visible.
- **Trust through transparency:** Show the underlying signals that drove each classification. Users must be able to audit the reasoning.

### 2.2 Design Language
- Clean, clinical, professional
- Light mode only (no dark mode for this feature)
- Minimal use of color — reserve color for meaning (red = critical, blue = action, yellow = mitigated)
- No decorative elements, gradients, or illustrations
- White space is used for breathing room, not decoration

### 2.3 Interaction Patterns
- Hover states on all interactive rows
- Clickable rows navigate to detail view
- Filter chips are toggleable
- Tabs switch between views without page reload
- Action buttons are always visible (not hidden in menus)

---

## 3. BRAND COLORS

### 3.1 Primary Palette
| Name | Hex | Usage |
|---|---|---|
| Orca Blue | #0080FF | Primary actions, active states, links, highlights |
| Orca Black | #101921 | Primary text, headers |
| White | #FFFFFF | Page background, card backgrounds |

### 3.2 Secondary Palette
| Name | Hex | Usage |
|---|---|---|
| Blue ADA Lightmode | #0073E5 | Hover state on blue elements |
| Blue 5 | #0360C5 | Pressed/active state on blue |
| Blue ADA Darkmode | #AFCFEE | Funnel level 2, light blue backgrounds |
| Cyan | #02D6FF | Accent only, use sparingly |

### 3.3 Neutral Palette
| Name | Hex | Usage |
|---|---|---|
| Gray 50 | #FDFDFF | Alternating table rows |
| Gray 100 | #F9F9FC | Secondary card backgrounds |
| Gray 150 | #F3F4F9 | Table headers, filter chip backgrounds |
| Gray 175 | #E8E9F1 | Row dividers, inner borders |
| Gray 200 | #E0E2EC | Card borders, section dividers |
| Gray 300 | #CACFDB | Disabled borders, subtle separators |
| Gray 400 | #A9B2C7 | Placeholder text, inactive icons |
| Gray 500 | #8693B2 | Secondary labels, subtitles |
| Gray 600 | #5F6D8F | Body text, table column headers |
| Gray 700 | #4D5875 | Strong body text |
| Gray 800 | #3C465F | Dark body text |
| Gray 900 | #272E3F | Near-black text |

### 3.4 Risk / Severity Palette
| Severity | Hex | Text Color | Usage |
|---|---|---|---|
| Critical | #E2005E | #FFFFFF | Critical severity badge |
| High | #FF3342 | #FFFFFF | High severity, Externally Exploitable state |
| Medium | #FE7B1F | #FFFFFF | Medium severity badge |
| Low | #F8CD39 | #101921 | Low severity, Mitigated state |
| Informational | #A9B2C7 | #101921 | Info, Not Reachable state |

### 3.5 Semantic Colors
| Name | Hex | Usage |
|---|---|---|
| Light Blue Background | #E6F1FB | Highlighted KPI tile, callout boxes |
| Light Red Background | #FFF0F0 | Exposure state banner (critical) |
| Success Green | #50C878 | Small effort badge, confirmed signals |
| Warning Orange | #FE7B1F | Medium effort badge |

---

## 4. TYPOGRAPHY

### 4.1 Font Families
| Font | Usage |
|---|---|
| Montserrat | Page titles (H1), KPI numbers, metric numbers |
| Mulish | All body text, labels, table content, badges, buttons |

### 4.2 Type Scale
| Element | Font | Weight | Size | Color | Usage |
|---|---|---|---|---|---|
| Page Title H1 | Montserrat | Medium (500) | 24px | #101921 | "ExposurePulse" |
| Section Header H2 | Mulish | Semi Bold (600) | 16px | #101921 | Card headers |
| Section Header H3 | Mulish | Semi Bold (600) | 14px | #101921 | Sub-section headers |
| KPI Number | Montserrat | Medium (500) | 28-32px | #101921 or #0080FF | Tile numbers |
| Table Column Header | Mulish | Semi Bold (600) | 12px | #5F6D8F | Column labels |
| Table Row Primary | Mulish | Semi Bold (600) | 13px | #101921 | CVE ID, asset name |
| Table Row Secondary | Mulish | Regular (400) | 11px | #8693B2 | CVE description, subtitles |
| Body Text | Mulish | Regular (400) | 13px | #5F6D8F | Descriptions, paragraphs |
| Small Label | Mulish | Regular (400) | 12px | #8693B2 | Secondary info |
| Badge / Pill Text | Mulish | Semi Bold (600) | 10-11px | varies | Severity, state badges |
| Button Primary | Mulish | Semi Bold (600) | 13px | #FFFFFF | Primary CTA |
| Button Secondary | Mulish | Semi Bold (600) | 13px | #0080FF | Secondary CTA |
| Eyebrow Label | Mulish | Semi Bold (600) | 11px | #0080FF | Section category labels |
| Monospace Path | Courier New | Regular | 11px | #8693B2 | Exposure paths |

### 4.3 Line Heights
| Context | Line Height |
|---|---|
| Headings | 1.2 |
| Body text | 1.5 |
| Table rows | 1.4 |
| Labels | 1.2 |

---

## 5. COMPONENT LIBRARY

### 5.1 Top Navigation Bar
```
Height: 56px
Background: #FFFFFF
Border bottom: 1px solid #E0E2EC
Box shadow: 0 1px 3px rgba(0,0,0,0.06)
Padding: 0 24px

Left section:
- Orca logo: "orca" Montserrat Bold 20px #101921 
  + sonar icon in #0080FF
- Spacing after logo: 24px

Center section:
- Search bar: 380px wide
- Background: #F3F4F9
- Border: 1px solid #E0E2EC
- Border radius: 6px
- Padding: 8px 12px
- Placeholder: "Search Assets, Alerts, Vulnerabilities"
  Mulish Regular 13px #A9B2C7
- Magnifier icon: #A9B2C7 left side
- Keyboard shortcut badge: "⌘K" right side
  #E0E2EC bg #8693B2 text 11px

Right section:
- "Ask Orca" button: 
  Border 1px #0080FF, #FFFFFF bg, #0080FF text
  Border radius 6px, padding 6px 12px
  Mulish Semi Bold 13px
  Star/AI icon before text
- Bell icon: #8693B2, 20px
- Question icon: #8693B2, 20px  
- User avatar: 32px circle, #0080FF bg, 
  "H" white Mulish Bold 14px
- User name: "Hello World" Mulish Semi Bold 13px #101921
  "Orca Demo" Mulish Regular 11px #8693B2
```

### 5.2 Left Sidebar
```
Width: 56px
Background: #FFFFFF
Border right: 1px solid #E0E2EC
Padding: 16px 0

Icon container:
Width: 40px, Height: 40px
Border radius: 8px
Centered in sidebar

Active icon:
Background: #0080FF
Icon color: #FFFFFF

Inactive icon:
Background: transparent
Icon color: #8693B2
Hover: #F3F4F9 background

Icons (top to bottom):
1. Grid/Dashboard
2. Alert triangle
3. Layers/Assets
4. Shield (ExposurePulse - ACTIVE)
5. Clipboard/Compliance
6. Settings (bottom, separated)

Spacing between icons: 8px
```

### 5.3 Tab Navigation
```
Pattern: Identical to Orca Missions tabs

Height: 48px
Border bottom: 1px solid #E0E2EC
Background: #FFFFFF
Padding: 0 24px

Tab item:
Padding: 0 16px
Height: 100%
Display: flex align-items center

Active tab:
Color: #0080FF
Font: Mulish Semi Bold 14px
Border bottom: 2px solid #0080FF (sits on top of row border)

Inactive tab:
Color: #8693B2
Font: Mulish Regular 14px
Hover: #101921 color

Spacing between tabs: 0 (tabs are adjacent)
```

### 5.4 Filter Chips
```
Height: 32px
Background: #F3F4F9
Border: 1px solid #CACFDB
Border radius: 6px
Padding: 0 12px
Margin right: 8px

Text: Mulish Semi Bold 12px #5F6D8F
Caret: ▼ 10px #8693B2, margin left 6px

Active/Selected state:
Background: #E6F1FB
Border: 1px solid #0080FF
Text: #0080FF

Hover state:
Background: #E8E9F1
Border: 1px solid #A9B2C7

"Reset to Default" link:
Color: #0080FF
Mulish Regular 13px
Margin left: auto (pushes to right)
```

### 5.5 KPI Tiles
```
Container: flex row, 4 equal tiles
Gap: 16px
Margin bottom: 24px

Each tile:
Background: #F9F9FC
Border: 1px solid #E0E2EC
Border radius: 8px
Padding: 20px 24px
Flex: 1

Number:
Font: Montserrat Medium 28px
Color: #101921 (default) or #0080FF (highlighted)
Margin bottom: 4px

Label:
Font: Mulish Regular 12px
Color: #8693B2

Sub-label:
Font: Mulish Regular 11px
Color: #A9B2C7 (default) or #0080FF (highlighted)
Margin top: 2px

Highlighted tile (4th - Externally Exploitable):
Background: #E6F1FB
Border: 1px solid #0080FF
Number color: #0080FF
Label color: #0080FF
Sub-label color: #0080FF
```

### 5.6 Data Table
```
Container:
Background: #FFFFFF
Border: 1px solid #E0E2EC
Border radius: 8px
Overflow: hidden

Section header row:
Background: #FFFFFF
Padding: 16px 20px
Border bottom: 1px solid #E0E2EC
Text: Mulish Semi Bold 14px #101921
Sort icon: right aligned, #8693B2

Table header row:
Background: #F3F4F9
Border bottom: 1px solid #CACFDB
Padding: 10px 16px per cell
Text: Mulish Semi Bold 12px #5F6D8F uppercase tracking

Table body rows:
Height: 56px minimum
Padding: 14px 16px per cell
Border bottom: 1px solid #E8E9F1
Alternating: #FFFFFF and #FDFDFF
Hover: #F3F4F9 background (full row)
Cursor: pointer

Primary cell text:
Mulish Semi Bold 13px #101921

Secondary cell text (subtitle):
Mulish Regular 11px #8693B2
Margin top: 2px

Monospace path text:
Courier New Regular 11px #8693B2
```

### 5.7 Severity / State Badges (Pills)
```
Display: inline-flex
Align-items: center
Border radius: 4px
Padding: 3px 8px
Font: Mulish Semi Bold 10px
White-space: nowrap

CRITICAL badge:
Background: #E2005E
Text: #FFFFFF

HIGH badge:
Background: #FF3342
Text: #FFFFFF

MEDIUM badge:
Background: #FE7B1F
Text: #FFFFFF

LOW badge:
Background: #F8CD39
Text: #101921

Externally Exploitable state:
Background: #FF3342
Text: #FFFFFF

Reachable, Mitigated state:
Background: #F8CD39
Text: #101921

Not Externally Reachable state:
Background: #A9B2C7
Text: #101921

EPSS badge:
Background: #0080FF
Text: #FFFFFF

KEV Listed badge:
Background: #FE7B1F
Text: #FFFFFF

Effort Small:
Background: #50C878
Text: #FFFFFF

Effort Medium:
Background: #FE7B1F
Text: #FFFFFF

Effort Large:
Background: #FF3342
Text: #FFFFFF

Environment PROD:
Background: #FE7B1F opacity 15%
Text: #FE7B1F
Border: 1px solid #FE7B1F opacity 30%

Environment STAGING:
Background: #0080FF opacity 10%
Text: #0080FF
Border: 1px solid #0080FF opacity 20%
```

### 5.8 Cards
```
Standard card:
Background: #FFFFFF
Border: 1px solid #E0E2EC
Border radius: 8px
Padding: 16px 20px
Box shadow: 0 1px 3px rgba(0,0,0,0.06)

Card with left accent (Network/App layer):
Border left: 4px solid [severity color]
Padding left: 16px (adjusted for border)

Card header:
Font: Mulish Semi Bold 13px #101921
Margin bottom: 12px
Padding bottom: 12px
Border bottom: 1px solid #E8E9F1

Card body rows:
Padding: 8px 0
Border bottom: 1px solid #E8E9F1
Last child: no border

Row label:
Mulish Regular 12px #8693B2
Min-width: 140px

Row value:
Mulish Regular 12px #101921

Verdict badge (inside card header):
Float right
Standard pill styling
```

### 5.9 Buttons
```
Primary button:
Background: #0080FF
Text: #FFFFFF
Border: none
Border radius: 6px
Padding: 8px 16px
Font: Mulish Semi Bold 13px
Hover: background #0073E5
Active: background #0360C5
Box shadow: 0 1px 2px rgba(0,128,255,0.3)

Secondary button (blue outline):
Background: #FFFFFF
Text: #0080FF
Border: 1px solid #0080FF
Border radius: 6px
Padding: 8px 16px
Font: Mulish Semi Bold 13px
Hover: background #E6F1FB

Tertiary button (gray outline):
Background: #FFFFFF
Text: #5F6D8F
Border: 1px solid #CACFDB
Border radius: 6px
Padding: 8px 16px
Font: Mulish Semi Bold 13px
Hover: background #F3F4F9

Button spacing in a row: 12px gap
```

### 5.10 Attack Path Visualization
```
Container:
Background: #F3F4F9
Border: 1px solid #E0E2EC
Border radius: 8px
Padding: 16px 20px

Header: Mulish Semi Bold 13px #101921
Margin bottom: 12px

Path nodes: flex row, align-items center, flex-wrap wrap
Gap: 8px

Node pill (default):
Background: #E0E2EC
Text: #5F6D8F
Font: Mulish Regular 11px
Padding: 4px 10px
Border radius: 4px

Node pill (vulnerable - last):
Background: #FFFFFF
Text: #FF3342
Border: 2px solid #FF3342
Font: Mulish Semi Bold 11px

Arrow separator:
Text: ">"
Color: #A9B2C7
Font: 14px
Padding: 0 2px
```

### 5.11 Signal Sources List
```
Container:
Background: #F9F9FC
Border: 1px solid #E0E2EC
Border radius: 8px
Padding: 16px

Header: Mulish Semi Bold 13px #101921
Margin bottom: 12px
Padding bottom: 12px
Border bottom: 1px solid #E8E9F1

Each signal row:
Display: flex
Align-items: center
Padding: 10px 0
Border bottom: 1px solid #E8E9F1
Gap: 10px

Icon (16px):
Confirmed: green checkmark #50C878
Not found: red X #FF3342
Partial: orange warning #FE7B1F

Signal label:
Mulish Regular 12px #5F6D8F
Flex: 1

Status text:
Mulish Semi Bold 12px
Confirmed: #50C878
Not active/None: #FF3342
Partial/Warning: #FE7B1F
```

### 5.12 Exposure Funnel
```
Container: flex column, align-items center
Width: 100%

Each funnel level:
Display: flex
Align-items: center
Justify-content: space-between
Padding: 0 20px
Height: 60px
Border radius: 6px
Margin bottom: 2px (overlap slightly)

Level widths (percentage of container):
Level 1: 100%
Level 2: 80%
Level 3: 58%
Level 4: 38%

Level colors:
Level 1: #E0E2EC (light gray)
Level 2: #AFCFEE (light blue)
Level 3: rgba(0,115,229,0.7) (medium blue)
Level 4: #0080FF (Orca Blue)

Text on levels 1-2: #101921
Text on levels 3-4: #FFFFFF

Label: Mulish Regular 12px left aligned
Number: Montserrat Medium 18-22px left of label
Percentage/reduction: Mulish Regular 11px right aligned

Connecting arrows:
Width: 20px
Color matches level below
Simple triangle/caret shape
Centered between levels

Callout box below funnel:
Background: #E6F1FB
Border left: 3px solid #0080FF
Border radius: 6px
Padding: 10px 14px
Text: Mulish Italic 12px #0080FF
Margin top: 16px
```

### 5.13 Line Chart (Trend)
```
Container:
Background: #FFFFFF
Border: 1px solid #E0E2EC
Border radius: 8px
Padding: 16px 20px

Chart area:
Height: 220px
Width: 100%

Line:
Color: #0080FF
Stroke width: 2px
Smooth curve (bezier)

Area fill:
#0080FF at 8% opacity
Below the line to x-axis

Data point dots:
Radius: 5px
Fill: #0080FF
Stroke: #FFFFFF 2px

Grid lines:
Color: #E8E9F1
Width: 1px
Style: dashed

Axis labels:
Font: Mulish Regular 11px #8693B2

Annotation lines:
Color: #CACFDB
Style: dashed 1px
Label: Mulish Regular 10px #8693B2
  positioned above line

GA annotation:
Line color: #0080FF
Label: Mulish Semi Bold 10px #0080FF
```

### 5.14 Progress Bars (Asset Table)
```
Container:
Height: 6px
Background: #E0E2EC
Border radius: 3px
Width: 80px

Fill:
Border radius: 3px
Heights match container

Colors by score:
High risk (>70%): #FF3342
Medium risk (40-70%): #FE7B1F
Low risk (<40%): #F8CD39

Trend indicators:
Worsening: ↑ #FF3342
Stable: → #A9B2C7
Improving: ↓ #50C878
Font: Mulish Semi Bold 11px
```

---

## 6. SPACING SYSTEM

```
4px  — micro spacing (badge padding, icon gaps)
8px  — small spacing (between related elements)
12px — button padding, inner card spacing
16px — standard padding (cards, rows)
20px — card padding large
24px — section spacing
32px — major section breaks
48px — page-level spacing
```

---

## 7. LAYOUT GRID

```
Page layout:
- Left sidebar: 56px fixed
- Top nav: 56px fixed
- Content area: remaining width
- Content padding: 24px all sides

Content max-width: none (full width)

Two-column layouts:
- Equal: 50% / 50%
- Sidebar: 65% / 35%
- Wide-left: 45% / 55%

Column gap: 20px
```

---

## 8. ELEVATION / SHADOWS

```
Level 0 (flat): no shadow
Level 1 (cards): 0 1px 3px rgba(0,0,0,0.06)
Level 2 (dropdowns): 0 4px 12px rgba(0,0,0,0.10)
Level 3 (modals): 0 8px 24px rgba(0,0,0,0.14)
```

---

## 9. BORDER RADIUS

```
4px  — pills, badges, small chips
6px  — buttons, filter chips, small inputs
8px  — cards, containers, input fields
12px — large cards, modals
50%  — avatars, circular icons
```

---

## 10. DO / DO NOT

### DO:
- Use color exclusively to convey meaning (not decoration)
- Show real data in every field (no "Lorem ipsum" or gray boxes)
- Make every row hoverable and clickable
- Show exposure state with equal visual weight to severity
- Use the exact Orca colors from this guide only
- Keep typography tight and professional
- Use Mulish for all UI text and Montserrat only for large numbers/titles

### DO NOT:
- Use dark mode or dark backgrounds
- Use gradients or decorative patterns
- Use colors outside the defined palette
- Add illustrations or icons that are not functional
- Use em dashes anywhere
- Create placeholder grey boxes instead of real content
- Use more than 3 colors in a single component
- Use font sizes smaller than 10px
- Add animations or transitions in the wireframe
- Use any typography other than Montserrat and Mulish

---

## 11. REFERENCE SCREENSHOTS

The following Orca product screenshots define the visual standard:

### Screenshot 1: Orca Compliance Dashboard
Defines the pattern for:
- Top navigation bar layout and styling
- Filter chip row
- KPI score tiles
- Data table with columns, rows, alternating backgrounds
- Section headers above tables
- Overall page layout and spacing

### Screenshot 2: Orca Missions
Defines the pattern for:
- Tab navigation (Suggested / Active / Completed)
- List rows with title, description, domain tag, effort badge, score
- Left sidebar filter panel
- Action-oriented row design
- This is the closest existing Orca feature to ExposurePulse

**The final output must be indistinguishable from these reference screenshots in visual quality, spacing, and component styling.**

---

## 12. PAGE-SPECIFIC NOTES

### Page 1: Exposure List
- Most important page — analysts use this daily
- KPI tiles must convert 850 to 37 visually (the funnel story in numbers)
- Exposure State column must have equal visual weight to Severity
- Exposure Path column uses monospace font (like a terminal path)
- "View Detail" button visible on row hover (not always visible)
- Table shows exactly 5 rows

### Page 2: Vulnerability Detail
- Two-column layout: 65% main, 35% sidebar
- Attack path is the hero element (top of main content)
- Network + App exposure cards must be side-by-side (not stacked)
- Remediation items are numbered (1, 2, 3) not bulleted
- Signal Sources sidebar shows which signals are confirmed vs missing
- Action buttons are always visible (Create Jira, Mark In Progress, Acknowledge)

### Page 3: Exposure Summary
- This is the CISO/executive view and the sales demo asset
- Funnel must be a real visual shape (each level narrower, centered, like a funnel)
- Trend chart shows beta baseline and GA annotation
- "Design partner beta begins Mar 2026 (confidential)" annotation on chart
- Bottom asset table shows trend direction per asset
- The 99.6% number must be the most visually prominent stat on the page

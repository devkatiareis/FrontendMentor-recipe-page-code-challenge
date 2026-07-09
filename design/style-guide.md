# Front-end Style Guide – Recipe Page

This document details the design specifications, CSS variables, typography, accessibility enhancements, and responsive techniques implemented in the final version of the Recipe Page project.

## 🛠️ Structural and Visual Analysis

The recipe page was developed using semantic HTML5 and modern CSS with a strong emphasis on readability, accessibility, and responsive design.

### Semantic Structure

The document is organized using meaningful HTML elements to improve accessibility and document hierarchy:

* `<main>` as the primary content landmark
* `<article>` containing the complete recipe
* `<figure>` for the featured recipe image
* `<section>` elements grouping recipe information
* `<table>` for nutritional values
* Ordered and unordered lists for recipe instructions and ingredients

### Responsive Card Layout

The recipe is displayed inside a centered card using Flexbox for page alignment. The layout adapts smoothly across different viewport sizes while maintaining comfortable reading width and spacing.

### Accessibility Features

The project includes several accessibility improvements beyond the original challenge requirements:

* Semantic HTML5 landmarks
* Skip Link for keyboard navigation
* Custom keyboard focus styles using `:focus-visible`
* Descriptive alternative text for images
* Proper heading hierarchy
* Native list markers
* `aria-labelledby` associations for grouped content and data tables

---

# 🎨 Color Palette and Design

The interface follows a soft, editorial-inspired color palette focused on readability and visual hierarchy.

### Primary Surface

* **White (Recipe Card Background):** `hsl(0, 0%, 100%)`

### Neutral Palette

* **Stone 100 (Page Background):** `hsl(30, 54%, 90%)`
* **Stone 150 (Dividers):** `hsl(30, 18%, 87%)`
* **Stone 600 (Body Text):** `hsl(30, 10%, 34%)`
* **Stone 900 (Primary Headings):** `hsl(24, 5%, 18%)`

### Accent Colors

* **Brown 800 (Section Titles & Nutrition Values):** `hsl(14, 45%, 36%)`
* **Rose 800 (Preparation Title):** `hsl(332, 51%, 32%)`
* **Rose 50 (Preparation Background):** `hsl(330, 100%, 98%)`

### Accessibility

A custom keyboard focus indicator improves navigation visibility:

* **Focus Outline:** `3px solid var(--brown-800)`
* **Outline Offset:** `4px`

---

# 📱 Layout & Responsiveness

The project follows a responsive layout while preserving the proportions of the original Frontend Mentor design.

### Design Targets

* **Mobile Design:** 375px
* **Desktop Design:** 1440px

### Component Layout

* **Maximum Card Width:** 736px (`46rem`)
* **Centered Layout:** Flexbox
* **Fluid Width:** `width: 100%`

### Responsive Strategy

The layout adapts to small screens by:

* Removing outer page padding
* Removing desktop border radius
* Expanding the featured image to the viewport edges
* Adjusting typography and spacing for improved readability

The project remains usable from 320px mobile devices through ultra-wide desktop displays.

---

# 🎨 CSS Design Tokens

All reusable values are centralized using CSS Custom Properties.

## Color Variables

```css
--white
--stone-100
--stone-150
--stone-600
--stone-900

--brown-800

--rose-50
--rose-800
```

## Typography Variables

```css
--font-heading
--font-body
```

## Spacing Scale

```css
--space-100
--space-200
--space-300
--space-400
--space-500
--space-600
```

## Border Radius

```css
--radius-sm
--radius-lg
```

---

## 🔤 Typography

### Font Families

### Headings

* **Young Serif**
* Weight: **400**

Used for:

* Main recipe title
* Section headings

### Body Text

* **Outfit**
* Weights:

  * 400 (Regular)
  * 600 (Semi Bold)
  * 700 (Bold)

Used for:

* Body paragraphs
* Lists
* Table content
* Preparation panel

---

## Typography Scale

| Element           | Font        | Weight |      Size |
| ----------------- | ----------- | -----: | --------: |
| Recipe Title      | Young Serif |    400 |    2.5rem |
| Section Titles    | Young Serif |    400 |   1.75rem |
| Preparation Title | Outfit      |    700 |   1.25rem |
| Body Copy         | Outfit      |    400 |      1rem |
| Nutrition Values  | Outfit      |    700 |      1rem |
| Attribution       | Outfit      |    400 | 0.6875rem |

---

# ♿ Accessibility Features

The project includes several accessibility improvements following modern web standards.

### Skip Link

A keyboard-accessible skip link allows users to jump directly to the main content.

```html
<a href="#main-content" class="skip-link">
  Skip to main content
</a>
```

### Keyboard Focus

Custom focus styles are applied only for keyboard users using the `:focus-visible` pseudo-class.

```css
:focus-visible {
  outline: 3px solid var(--brown-800);
  outline-offset: 4px;
}
```

### Semantic HTML

The page makes extensive use of semantic elements including:

* `<main>`
* `<article>`
* `<figure>`
* `<section>`
* `<table>`
* `<ol>`
* `<ul>`
* `<footer>`

### Data Tables

Nutrition values are presented using semantic table markup with row headers (`scope="row"`), improving compatibility with screen readers.

---

# 💻 Layout Techniques

The project uses modern CSS features including:

* CSS Custom Properties
* Flexbox
* Responsive Media Queries
* Relative Units (`rem`)
* Native List Markers (`::marker`)
* Accessible Focus Indicators (`:focus-visible`)

---

# 🚀 Performance Considerations

The project was optimized by:

* Loading only the required Google Font weights
* Using semantic HTML instead of unnecessary wrapper elements
* Leveraging CSS Custom Properties for maintainability
* Keeping the stylesheet lightweight without external frameworks

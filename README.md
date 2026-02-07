# Reflex (Prefixed) CSS Framework

A lightweight, builder-safe CSS grid and utility framework designed to work cleanly with **Elementor, Divi, and WordPress themes**. All layout classes are **prefixed with `rf-`** to prevent conflicts. Spacing utilities are global for convenience.

---

## Features

- 📐 **12-column Flexbox grid** (responsive, mobile-first)
- 🧱 **Safe prefixed classes** (`rf-*`) for layout
- 🧭 **Offsets & ordering** for layout control
- 🧩 **Flex helpers** (align, justify, wrap, direction)
- 📊 **Bootstrap-style tables (prefixed)**
- 🧰 **Global spacing utilities** (`m-*`, `p-*`, etc.)

---

## Installation

Include the CSS file in your theme, child theme, or sitewide stylesheet.

```html
<link rel="stylesheet" href="reflex.css">
```

No JavaScript required.

---

## Core Concepts

Layouts are built using three main building blocks:

- **Containers** → `.rf-container`, `.rf-container-full`
- **Rows (Grids)** → `.rf-grid`
- **Columns** → `.rf-col-*` and responsive variants

All layout-related classes are prefixed with `rf-` to avoid conflicts with themes, plugins, and page builders.

---

## Containers

### Fixed-width Container
Centers content and applies responsive max-widths.

```html
<div class="rf-container">
  ...
</div>
```

### Full-width Container
Spans full width but keeps left/right padding.

```html
<div class="rf-container-full">
  ...
</div>
```

---

## Grid System

### Basic Layout

```html
<div class="rf-container">
  <div class="rf-grid">
    <div class="rf-col-6">Left</div>
    <div class="rf-col-6">Right</div>
  </div>
</div>
```

### Responsive Columns
Stack on mobile, split on desktop:

```html
<div class="rf-grid">
  <div class="rf-col-12 rf-col-md-6">Left</div>
  <div class="rf-col-12 rf-col-md-6">Right</div>
</div>
```

### Column Sizes

| Class | Width |
|-------|--------|
| `rf-col-1` | 8.33% |
| `rf-col-2` | 16.66% |
| `rf-col-3` | 25% |
| `rf-col-4` | 33.33% |
| `rf-col-6` | 50% |
| `rf-col-12` | 100% |

---

## Breakpoints

| Prefix | Min Width |
|--------|------------|
| `xs` | ≥ 576px |
| `sm` | ≥ 768px |
| `md` | ≥ 992px |
| `lg` | ≥ 1200px |
| `xlg` | ≥ 1600px |

### Example

```html
<div class="rf-col-12 rf-col-sm-6 rf-col-lg-4">Card</div>
```

---

## Auto Columns

Let a column grow to fill available space:

```html
<div class="rf-grid">
  <div class="rf-col-3">Sidebar</div>
  <div class="rf-col-auto">Flexible Content</div>
</div>
```

Responsive versions are also available:

- `rf-col-sm-auto`
- `rf-col-md-auto`
- `rf-col-lg-auto`
- `rf-col-xlg-auto`

---

## Offsets

Push a column to the right by column width.

```html
<div class="rf-grid">
  <div class="rf-col-4 rf-offset-4">Centered</div>
</div>
```

Responsive:

```html
<div class="rf-col-6 rf-offset-md-3">Centered on desktop</div>
```

---

## Ordering

Reorder columns visually using Flexbox.

```html
<div class="rf-grid">
  <div class="rf-col-6 rf-order-2 rf-order-md-1">Text</div>
  <div class="rf-col-6 rf-order-1 rf-order-md-2">Image</div>
</div>
```

---

## Flex Helpers

Apply these to `.rf-grid`:

### Wrapping
- `rf-wrap`
- `rf-no-wrap`
- `rf-wrap-reverse`

### Direction
- `rf-direction-row`
- `rf-direction-column`
- `rf-direction-row-reverse`
- `rf-direction-column-reverse`

### Alignment
- `rf-align-start`
- `rf-align-center`
- `rf-align-end`
- `rf-align-baseline`

### Justification
- `rf-justify-start`
- `rf-justify-center`
- `rf-justify-end`
- `rf-justify-space-between`
- `rf-justify-space-around`

### Example

```html
<div class="rf-grid rf-align-center rf-justify-space-between">
  ...
</div>
```

---

## Gutter Control (Bleed)

Remove column padding when needed.

### Remove gutters for entire grid

```html
<div class="rf-grid rf-grid-bleed">
  <div class="rf-col-6">No padding</div>
  <div class="rf-col-6">No padding</div>
</div>
```

### Per-column

- `rf-col-bleed` → no padding
- `rf-col-bleed-x` → vertical padding only
- `rf-col-bleed-y` → horizontal padding only

---

## Tables (Prefixed)

Tables are Bootstrap-style but **use `rf-` prefixes** to avoid conflicts.

```html
<div class="rf-table-responsive">
  <table class="rf-table rf-table-striped rf-table-hover">
    ...
  </table>
</div>
```

### Options

- `rf-table-striped`
- `rf-table-hover`
- `rf-table-bordered`
- `rf-table-borderless`
- `rf-table-sm`

### Contextual Colors

- `rf-table-primary`
- `rf-table-secondary`
- `rf-table-success`
- `rf-table-info`
- `rf-table-warning`
- `rf-table-danger`
- `rf-table-light`
- `rf-table-dark`

---

## Spacing Utilities (Global)

These classes work **anywhere on the site**.

### Margin

- `m-0` → `m-5`
- `mt-*`, `mb-*`, `ml-*`, `mr-*`
- `mx-*` (left/right)
- `my-*` (top/bottom)

### Padding

- `p-0` → `p-5`
- `pt-*`, `pb-*`
- `px-*` (left/right)
- `py-*` (top/bottom)

### Example

```html
<div class="p-4 mb-3">
  Spaced content
</div>
```

### Responsive Spacing

- `sm-*` → ≥576px
- `md-*` → ≥768px
- `lg-*` → ≥992px
- `xl-*` → ≥1200px

Example:

```html
<div class="p-2 lg-p-5">Responsive padding</div>
```

---

## Best Practices

- Always use **`rf-` prefixed classes for layout**
- Use global spacing utilities for fast spacing control
- Avoid mixing `.rf-grid` with other grid systems in the same section
- Use `rf-col-auto` for flexible layouts

---

## Example Layout

```html
<div class="rf-container">
  <div class="rf-grid rf-align-center">
    <div class="rf-col-12 rf-col-md-6">
      <h2>Content</h2>
      <p>This stacks on mobile and splits on desktop.</p>
    </div>
    <div class="rf-col-12 rf-col-md-6">
      <img src="image.jpg" alt="" style="width:100%;">
    </div>
  </div>
</div>
```

---

## License

Free to use in personal and commercial projects.

---

## Notes

This framework is designed to coexist safely with:

- Elementor
- Divi
- Most WordPress themes and plugins

By keeping all layout classes prefixed, it avoids common class-name collisions while still giving you fast, utility-style development.


# OpenCloudHub – Design & Style Guide

> Version 1.0\
> This document defines the visual identity and design system of the OpenCloudHub project. It ensures consistency across platforms, repos, documentation, UIs, and marketing material.

______________________________________________________________________

## 🎨 Color Strategy

A modern, tech-focused palette conveying trust, innovation, and professionalism.

### Primary Brand Colors

```css
/* CSS Custom Properties */
:root {
  --color-deep-slate: #34374c;
  --color-charcoal: #1f212e;
  --color-slate-blue: #494d6a;
  --color-cloud-teal: #00d4aa;
  --color-tech-blue: #0ea5e9;
  --color-alert-orange: #f97316;
  --color-error-red: #ef4444;
}
```

| Name       | Hex       | Preview                                                                                                                              | RGB           | Usage                          |
| ---------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------- | ------------------------------ |
| Deep Slate | `#34374c` | <div style="width: 24px; height: 24px; background:#34374c; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `52, 55, 76`  | Primary brand color, headings  |
| Charcoal   | `#1f212e` | <div style="width: 24px; height: 24px; background:#1f212e; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `31, 33, 46`  | Backgrounds, contrast text     |
| Slate Blue | `#494d6a` | <div style="width: 24px; height: 24px; background:#494d6a; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `73, 77, 106` | Borders, icons, secondary text |

### Neutral Colors

| Name        | Hex       | Preview                                                                                                                              | RGB             | Usage                    |
| ----------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------ | --------------- | ------------------------ |
| Pure White  | `#ffffff` | <div style="width: 24px; height: 24px; background:#ffffff; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `255, 255, 255` | Backgrounds, whitespace  |
| Light Grey  | `#f6f6f6` | <div style="width: 24px; height: 24px; background:#f6f6f6; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `246, 246, 246` | Card backgrounds         |
| Medium Grey | `#dcdcdc` | <div style="width: 24px; height: 24px; background:#dcdcdc; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `220, 220, 220` | Dividers, subtle borders |

### Accent Colors

| Name         | Hex       | Preview                                                                                                                              | RGB            | Usage                            |
| ------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------ | -------------- | -------------------------------- |
| Cloud Teal   | `#00d4aa` | <div style="width: 24px; height: 24px; background:#00d4aa; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `0, 212, 170`  | CTAs, highlights, success states |
| Tech Blue    | `#0ea5e9` | <div style="width: 24px; height: 24px; background:#0ea5e9; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `14, 165, 233` | Links, active components         |
| Alert Orange | `#f97316` | <div style="width: 24px; height: 24px; background:#f97316; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `249, 115, 22` | Warnings, system notifications   |
| Error Red    | `#ef4444` | <div style="width: 24px; height: 24px; background:#ef4444; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `239, 68, 68`  | Errors, destructive actions      |

______________________________________________________________________

## 🔡 Typography System

Clean, modern typography prioritizing readability and performance.

### Font Stack

```css
font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
```

### Type Scale Examples

# Display Large (48px)

Main hero titles and landing headers

## Heading 1 (36px)

Major sections and page titles

### Heading 2 (24px)

Subsections and card headers

#### Heading 3 (20px)

Secondary titles and widget headers

##### Heading 4 (16px)

Labels and UI section headers

**Body Text (16px)** - This is the standard paragraph text used throughout the interface. It should be highly readable and comfortable for extended reading sessions.

*Small Text (14px)* - Used for captions, hints, and metadata information.

### Typography Hierarchy

| Element        | Size | Weight | Color     | Line Height |
| -------------- | ---- | ------ | --------- | ----------- |
| Display Large  | 48px | 600    | `#1f212e` | 1.2         |
| Heading 1 (H1) | 36px | 600    | `#1f212e` | 1.3         |
| Heading 2 (H2) | 24px | 500    | `#34374c` | 1.4         |
| Heading 3 (H3) | 20px | 500    | `#34374c` | 1.4         |
| Heading 4 (H4) | 16px | 500    | `#494d6a` | 1.5         |
| Body Text      | 16px | 400    | `#1f212e` | 1.6         |
| Small Text     | 14px | 400    | `#494d6a` | 1.5         |

______________________________________________________________________

## 🧩 Component Guidelines

### Spacing System

Based on **8px grid system**:

```css
/* Spacing tokens */
:root {
  --space-xs: 4px;   /* 0.5 units */
  --space-sm: 8px;   /* 1 unit */
  --space-md: 16px;  /* 2 units */
  --space-lg: 24px;  /* 3 units */
  --space-xl: 32px;  /* 4 units */
  --space-2xl: 48px; /* 6 units */
  --space-3xl: 64px; /* 8 units */
}
```

### Interactive States

| State    | CSS Example                                  |
| -------- | -------------------------------------------- |
| Default  | `background: var(--color-cloud-teal)`        |
| Hover    | `opacity: 0.9; transform: translateY(-1px)`  |
| Active   | `transform: translateY(0); opacity: 0.95`    |
| Disabled | `opacity: 0.5; cursor: not-allowed`          |
| Focus    | `outline: 2px solid var(--color-cloud-teal)` |

______________________________________________________________________

## 🏷️ Status & Semantic Colors

### Status Indicators

| Status     | Color        | Preview                                                                                                                              | Hex       | Usage                             |
| ---------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------ | --------- | --------------------------------- |
| ✅ Success | Cloud Teal   | <div style="width: 24px; height: 24px; background:#00d4aa; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `#00d4aa` | Success states, completed actions |
| ⚠️ Warning | Alert Orange | <div style="width: 24px; height: 24px; background:#f97316; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `#f97316` | Warnings, caution states          |
| ❌ Error   | Error Red    | <div style="width: 24px; height: 24px; background:#ef4444; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `#ef4444` | Error states, destructive actions |
| ℹ️ Info    | Tech Blue    | <div style="width: 24px; height: 24px; background:#0ea5e9; border-radius: 4px; border:1px solid #aaa; display: inline-block;"></div> | `#0ea5e9` | Information, neutral states       |

### Usage in Components

```css
/* Alert components */
.alert-success { border-left: 4px solid var(--color-cloud-teal); }
.alert-warning { border-left: 4px solid var(--color-alert-orange); }
.alert-error { border-left: 4px solid var(--color-error-red); }
.alert-info { border-left: 4px solid var(--color-tech-blue); }
```

______________________________________________________________________

## 📱 Responsive Guidelines

### Breakpoints

| Name    | Min Width | Usage                |
| ------- | --------- | -------------------- |
| Mobile  | 320px     | Small screens        |
| Tablet  | 768px     | Medium screens       |
| Desktop | 1024px    | Large screens        |
| Wide    | 1440px    | Extra large displays |

### Typography Scaling

```css
/* Responsive typography */
@media (max-width: 768px) {
  h1 { font-size: 28px; }
  h2 { font-size: 20px; }
  .display-large { font-size: 36px; }
}
```

______________________________________________________________________

## 🔖 Logo & Brand Assets

### File Naming Convention

```
opencloudhub-icon-mark-light.svg
opencloudhub-monogram-light.svg
opencloudhub-primary-logo-light.svg
opencloudhub-stacked-logo-light.svg
opencloudhub-icon-mark-dark.svg
opencloudhub-monogram-dark.svg
opencloudhub-primary-logo-dark.svg
opencloudhub-stacked-logo-dark.svg
```

> [!NOTE]
> Minimum 1x logo height on all sides

### Usage Guidelines

- **Minimum size**: 24px height (digital), 0.5" (print)
- **Clear space**: 1× logo height on all sides
- **Background**: Test on both light and dark surfaces

______________________________________________________________________

## ⚙️ Implementation

### CSS Custom Properties

```css
:root {
  /* Colors */
  --color-primary: #34374c;
  --color-secondary: #1f212e;
  --color-accent: #00d4aa;

  /* Typography */
  --font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-size-base: 16px;
  --line-height-base: 1.6;

  /* Spacing */
  --border-radius: 8px;
  --border-width: 1px;
  --focus-ring: 2px solid var(--color-accent);
}
```

### Dark Mode Support

```css
@media (prefers-color-scheme: dark) {
  :root {
    --color-primary: #ffffff;
    --color-secondary: #f6f6f6;
    --bg-primary: #1f212e;
    --bg-secondary: #34374c;
  }
}
```

______________________________________________________________________

## 📋 Checklist for New Components

- [ ] Uses 8px grid spacing
- [ ] Minimum 44×44px touch targets
- [ ] Proper color contrast (3:1 minimum)
- [ ] Focus indicators implemented
- [ ] Responsive behavior defined
- [ ] Dark mode considered
- [ ] Accessibility tested

______________________________________________________________________

## 🔗 Resources

- [Color Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [Colorblind Simulator](https://www.color-blindness.com/coblis-color-blindness-simulator/)
- [CSS Custom Properties Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)

______________________________________________________________________

*Last updated: [Current Date] | Version 1.0*

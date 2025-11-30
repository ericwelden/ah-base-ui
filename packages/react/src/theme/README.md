# Design System 2.0 - Brand Styles for Base UI

This directory contains a comprehensive styling system for Base UI components following your Design System 2.0 brand guidelines.

## 📋 Table of Contents

- [Overview](#overview)
- [Icons](#icons)
- [Installation](#installation)
- [Design Tokens](#design-tokens)
- [Components](#components)
- [Usage Examples](#usage-examples)
- [Customization](#customization)

## Overview

The styling system includes:

- **Design Tokens**: CSS custom properties for colors, typography, spacing, shadows, and more
- **Base Styles**: Global resets and utility classes
- **Component Styles**: Pre-styled components following brand guidelines

### Color Palette

- **Primary**: Blue scale (50-900)
- **Neutral**: Gray scale (50-900)
- **Surface**: Beige tones (0-500)
- **Semantic Colors**:
  - Success: Green
  - Warning: Yellow/Gold
  - Error: Orange/Red
  - Info: Purple
  - Danger: Pink/Red

### Typography

- **Font Family**: Inter
- **Styles**: Display, Headline, Title, Body, Label, Eyebrow
- **Weights**: Regular (400), Medium (500), Demibold/Bold (600)

### Icons

- **Material Symbols**: Google's icon font with 300 weight
- **Variants**: Rounded (default) and Outlined
- **Sizes**: XS to 3XL
- **2,500+ icons** available including healthcare-specific icons

## Icons

The theme includes **Material Symbols** from Google with 300 weight in both Rounded and Outlined variants.

### Basic Usage

```html
<!-- Rounded variant (default) -->
<span class="icon">home</span>
<span class="icon icon-rounded">settings</span>

<!-- Outlined variant -->
<span class="icon icon-outlined">favorite</span>

<!-- Different sizes -->
<span class="icon icon-xs">star</span>      <!-- 14px -->
<span class="icon icon-sm">star</span>      <!-- 16px -->
<span class="icon icon-md">star</span>      <!-- 20px - default -->
<span class="icon icon-lg">star</span>      <!-- 24px -->
<span class="icon icon-xl">star</span>      <!-- 32px -->
<span class="icon icon-2xl">star</span>     <!-- 40px -->
<span class="icon icon-3xl">star</span>     <!-- 48px -->
```

### Icons in Components

#### Buttons with Icons

```html
<!-- Icon before text -->
<button class="btn btn-primary">
  <span class="icon">download</span>
  Download
</button>

<!-- Icon after text -->
<button class="btn btn-primary">
  Upload
  <span class="icon">upload</span>
</button>

<!-- Icon-only button -->
<button class="btn btn-primary btn-icon-only">
  <span class="icon">add</span>
</button>
```

#### Form Inputs with Icons

```html
<div style="position: relative;">
  <input type="text" class="input" placeholder="Search..." style="padding-left: 2.5rem;" />
  <span class="icon" style="position: absolute; left: 0.75rem; top: 50%; transform: translateY(-50%); color: var(--color-neutral-500);">
    search
  </span>
</div>
```

#### Menu Items with Icons

```html
<button class="menu-item">
  <span class="icon menu-item-icon">home</span>
  Home
</button>
```

#### Navigation Items with Icons

```html
<a href="#" class="sidebar-nav-item">
  <span class="icon sidebar-nav-item-icon">dashboard</span>
  Dashboard
</a>
```

### Common Icons

The theme includes helper classes for frequently used icons:

```html
<span class="icon icon-menu"></span>        <!-- menu -->
<span class="icon icon-close"></span>       <!-- close -->
<span class="icon icon-check"></span>       <!-- check -->
<span class="icon icon-add"></span>         <!-- add -->
<span class="icon icon-edit"></span>        <!-- edit -->
<span class="icon icon-delete"></span>      <!-- delete -->
<span class="icon icon-search"></span>      <!-- search -->
<span class="icon icon-settings"></span>    <!-- settings -->
<span class="icon icon-home"></span>        <!-- home -->
<span class="icon icon-person"></span>      <!-- person -->
<span class="icon icon-notifications"></span> <!-- notifications -->
<span class="icon icon-mail"></span>        <!-- mail -->
<span class="icon icon-calendar"></span>    <!-- calendar_today -->
<span class="icon icon-download"></span>    <!-- download -->
<span class="icon icon-upload"></span>      <!-- upload -->
<span class="icon icon-share"></span>       <!-- share -->
```

### Healthcare-Specific Icons

```html
<span class="icon icon-medical"></span>     <!-- medical_services -->
<span class="icon icon-health"></span>      <!-- health_and_safety -->
<span class="icon icon-medication"></span>  <!-- medication -->
<span class="icon icon-emergency"></span>   <!-- emergency -->
<span class="icon icon-accessible"></span>  <!-- accessible -->
<span class="icon icon-elderly"></span>     <!-- elderly -->
<span class="icon icon-bed"></span>         <!-- bed -->
<span class="icon icon-vital-signs"></span> <!-- vital_signs -->
```

### Finding More Icons

Browse all available icons at:
- **Material Symbols**: https://fonts.google.com/icons

Simply use the icon name as the content:
```html
<span class="icon">icon_name_here</span>
```

## Installation

### Import All Styles

```css
/* In your main CSS file */
@import '@base-ui-components/react/theme';
```

Or in JavaScript/TypeScript:

```typescript
import '@base-ui-components/react/theme';
```

### Import Individual Components

```css
/* Import only specific component styles */
@import '@base-ui-components/react/theme/components/button.css';
@import '@base-ui-components/react/theme/components/forms.css';
```

## Design Tokens

All design tokens are available as CSS custom properties:

```css
/* Colors */
var(--color-primary-500)
var(--color-neutral-900)
var(--color-surface-100)
var(--color-success-600)

/* Typography */
var(--font-family-base)
var(--font-size-body-medium)
var(--font-weight-medium)

/* Spacing */
var(--spacing-4)  /* 16px */
var(--spacing-6)  /* 24px */

/* Shadows */
var(--shadow-md)
var(--shadow-lg)

/* Border Radius */
var(--radius-md)
var(--radius-lg)
```

## Components

### Button

Pre-styled button variants following brand guidelines:

```tsx
import { Button } from '@base-ui-components/react';
import '@base-ui-components/react/theme';

// Primary button
<Button className="btn btn-primary">Click me</Button>

// Primary outlined button
<Button className="btn btn-primary-outline">Click me</Button>

// Secondary button
<Button className="btn btn-secondary">Click me</Button>

// Ghost/text button
<Button className="btn btn-ghost">Click me</Button>

// Sizes
<Button className="btn btn-primary btn-sm">Small</Button>
<Button className="btn btn-primary btn-md">Medium</Button>
<Button className="btn btn-primary btn-lg">Large</Button>

// With icon
<Button className="btn btn-primary">
  <IconComponent className="btn-icon" />
  With Icon
</Button>

// Icon only
<Button className="btn btn-primary btn-icon-only">
  <IconComponent className="btn-icon" />
</Button>

// States
<Button className="btn btn-primary" disabled>Disabled</Button>
<Button className="btn btn-primary" data-loading="true">Loading</Button>
```

### Form Components

#### Input

```tsx
import { Input } from '@base-ui-components/react';

<Input className="input" placeholder="Enter text..." />
<Input className="input input-sm" placeholder="Small input" />
<Input className="input input-lg" placeholder="Large input" />
<Input className="input input-error" placeholder="Error state" />
<Input className="input input-success" placeholder="Success state" />
```

#### Checkbox

```tsx
import { Checkbox } from '@base-ui-components/react';

<label className="checkbox-wrapper">
  <input type="checkbox" className="checkbox" />
  <span className="checkbox-indicator" />
  <span className="checkbox-label">Accept terms</span>
</label>
```

#### Radio

```tsx
<label className="radio-wrapper">
  <input type="radio" name="option" className="radio" />
  <span className="radio-indicator" />
  <span className="radio-label">Option 1</span>
</label>
```

#### Switch/Toggle

```tsx
<label className="switch-wrapper">
  <input type="checkbox" className="switch" />
  <span className="switch-track">
    <span className="switch-thumb" />
  </span>
  <span className="switch-label">Enable notifications</span>
</label>
```

#### Field (Form Group)

```tsx
<div className="field">
  <label className="field-label" data-required="true">
    Email address
  </label>
  <p className="field-description">
    We'll never share your email with anyone else.
  </p>
  <input type="email" className="input" />
  <p className="field-error">Please enter a valid email address.</p>
</div>
```

### Navigation

#### Menu

```tsx
import { Menu } from '@base-ui-components/react';

<div className="menu">
  <button className="menu-item">
    <IconComponent className="menu-item-icon" />
    Profile
  </button>
  <button className="menu-item" data-active="true">
    <IconComponent className="menu-item-icon" />
    Settings
  </button>
  <div className="menu-separator" />
  <button className="menu-item">
    <IconComponent className="menu-item-icon" />
    Logout
  </button>
</div>
```

#### Sidebar Navigation

```tsx
<nav className="sidebar">
  <div className="sidebar-header">
    <div className="sidebar-user">
      <div className="sidebar-user-avatar">SS</div>
      <span className="sidebar-user-name">Shasta Senior Living</span>
    </div>
  </div>

  <div className="sidebar-content">
    <a href="/inbox" className="sidebar-nav-item">
      <IconComponent className="sidebar-nav-item-icon" />
      Inbox
      <span className="sidebar-nav-item-badge">44</span>
    </a>
    <a href="/residents" className="sidebar-nav-item" data-active="true">
      <IconComponent className="sidebar-nav-item-icon" />
      Residents
      <span className="sidebar-nav-item-badge">5</span>
    </a>
  </div>

  <div className="sidebar-footer">
    <button className="sidebar-nav-item">
      <IconComponent className="sidebar-nav-item-icon" />
      Help & Support
    </button>
  </div>
</nav>
```

#### Tabs

```tsx
<div className="tabs-root">
  <div className="tabs-list">
    <button className="tabs-trigger" data-active="true">Overview</button>
    <button className="tabs-trigger">Details</button>
    <button className="tabs-trigger">Settings</button>
  </div>
  <div className="tabs-content">
    Content goes here
  </div>
</div>

<!-- Pill variant -->
<div className="tabs-list tabs-list-pill">
  <button className="tabs-trigger tabs-trigger-pill" data-active="true">
    Tab 1
  </button>
  <button className="tabs-trigger tabs-trigger-pill">Tab 2</button>
</div>
```

### Dialog/Modal

```tsx
import { Dialog } from '@base-ui-components/react';

<Dialog.Root>
  <Dialog.Backdrop className="dialog-backdrop" />
  <Dialog.Viewport className="dialog-viewport">
    <Dialog.Popup className="dialog-popup">
      <div className="dialog-header">
        <Dialog.Title className="dialog-title">
          Dialog Title
        </Dialog.Title>
        <Dialog.Close className="dialog-close">
          <CloseIcon />
        </Dialog.Close>
      </div>

      <div className="dialog-body">
        <Dialog.Description className="dialog-description">
          Dialog content goes here.
        </Dialog.Description>
      </div>

      <div className="dialog-footer">
        <button className="btn btn-secondary">Cancel</button>
        <button className="btn btn-primary">Confirm</button>
      </div>
    </Dialog.Popup>
  </Dialog.Viewport>
</Dialog.Root>
```

### Other Components

#### Progress

```tsx
<div className="progress-root progress-md">
  <div className="progress-indicator" style={{ width: '60%' }} />
</div>

<!-- Variants -->
<div className="progress-root">
  <div className="progress-indicator progress-indicator-success" style={{ width: '80%' }} />
</div>
```

#### Avatar

```tsx
<div className="avatar avatar-md">
  <img src="..." alt="..." className="avatar-image" />
  <span className="avatar-fallback">JD</span>
  <span className="avatar-status avatar-status-online" />
</div>
```

#### Badge

```tsx
<span className="badge badge-primary">New</span>
<span className="badge badge-success">Active</span>
<span className="badge badge-error">Error</span>
<span className="badge badge-dot badge-primary" />
```

#### Accordion

```tsx
<div className="accordion-root">
  <div className="accordion-item">
    <button className="accordion-trigger">
      <span>Section 1</span>
      <ChevronDownIcon className="accordion-trigger-icon" />
    </button>
    <div className="accordion-content">
      Content for section 1
    </div>
  </div>
</div>
```

## Typography Utilities

Use typography utility classes for consistent text styling:

```tsx
<h1 className="text-display-large">Display Large</h1>
<h2 className="text-headline-medium">Headline Medium</h2>
<p className="text-body-medium">Body text</p>
<span className="text-label-small text-emphasis">Small emphasized label</span>
```

## Surface & Elevation Utilities

```tsx
<!-- Surface colors -->
<div className="surface-0">White surface</div>
<div className="surface-100">Light beige surface</div>
<div className="surface-200">Medium beige surface</div>

<!-- Elevation/shadows -->
<div className="elevation-sm">Small shadow</div>
<div className="elevation-md">Medium shadow</div>
<div className="elevation-lg">Large shadow</div>
```

## Customization

### Override Design Tokens

You can override any design token by redefining the CSS custom property:

```css
:root {
  /* Override primary color */
  --color-primary-500: #FF0000;

  /* Override font family */
  --font-family-base: 'Roboto', sans-serif;

  /* Override spacing */
  --spacing-4: 1.5rem;
}
```

### Extend Component Styles

```css
/* Add custom button variant */
.btn-custom {
  background-color: var(--color-info-500);
  color: white;
}

.btn-custom:hover:not(:disabled) {
  background-color: var(--color-info-600);
}
```

## Best Practices

1. **Import once**: Import the theme CSS at the root of your application
2. **Use design tokens**: Reference CSS custom properties instead of hardcoding values
3. **Combine classes**: Use multiple classes to compose component variants
4. **Accessibility**: The styles include focus states and ARIA attribute support
5. **Dark mode**: Consider adding dark mode variants using CSS custom properties

## File Structure

```
theme/
├── index.css                    # Main entry point
├── design-tokens.css            # All CSS custom properties
├── base-styles.css              # Global styles and utilities
├── components/
│   ├── button.css              # Button component styles
│   ├── forms.css               # Form components (Input, Checkbox, etc.)
│   ├── navigation.css          # Navigation components (Menu, Tabs, etc.)
│   ├── dialog.css              # Dialog, Modal, Popover, Tooltip
│   └── misc.css                # Accordion, Progress, Avatar, Badge, etc.
└── README.md                   # This file
```

## Support

For questions or issues with the styling system, please refer to:
- Base UI documentation: https://base-ui.com
- Design System 2.0 Figma file (internal)

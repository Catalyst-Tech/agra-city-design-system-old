# AgraCity Design System

## Naming Convention Hierarchy & Legend
1. `theme`: Light / Dark.
2. `component`: Button, Card, Chip, etc.
3. `category`: Color, Font, Space, Radius, etc.
4. `property`: Actual CSS properties, e.g. Background, Size, Weight, etc.
5. `variant`: Primary, Secondary, Neutral, etc.
6. `state`: Hover, Active, Disabled, etc.
7. `scale`: 100, 200, 300, etc.

💡 Not all variables names must include all of the above. Each design token list will mention a naming convention pattern that makes sense within its context.

##  Primitives Variables
Primitives in CSS refer to low-level design tokens that represent fundamental values like colors, spacing, typography, etc. These are the raw, unprocessed values used throughout the design system.

These variables act as building blocks, making it easier to maintain and update the styles consistently across the project.
### Design Tokens
```css
/* Primitive variables */

/* Naming convention  */
/* --[category]-[variant]-[scale]  */

/* Color primitives */
/* 🚫 AVOID using color primitives directly to style components */

/* Brand blues */
--color-blue-50: #E3F5FE;
--color-blue-100: #C9EDFF;
--color-blue-200: #92CEFF;
--color-blue-300: #56AFFC;
--color-blue-400: #338FDA;
--color-blue-500: #0071BA;
--color-blue-600: #00539A;
--color-blue-700: #003870;
--color-blue-800: #012039;

/* Brand Greens */
--color-green-50: #F0F8E8;
--color-green-100: #DDF1C6;
--color-green-200: #B0D87D;
--color-green-300: #84BD00;
--color-green-400: #679D00;
--color-green-500: #4A7E00; 
--color-green-600: #2F6000;
--color-green-700: #234000;
--color-green-800: #152200;

/* Neutrals */
--color-neutral-50: #FFFFFF;
--color-neutral-100: #E2E9F0;
--color-neutral-200: #C0C9D2;
--color-neutral-300: #9FAAB5;
--color-neutral-400: #808B96;
--color-neutral-500: #636E78;
--color-neutral-600: #48525B;
--color-neutral-700: #2E3740;
--color-neutral-800: #161E26;

/* Warning */
--color-yellow-50: #FFF1CB;
--color-yellow-100: #FFE6A2;
--color-yellow-200: #E8C356;
--color-yellow-300: #CBA201;
--color-yellow-400: #A78502;
--color-yellow-500: #846802;
--color-yellow-600: #624D02;
--color-yellow-700: #423301;
--color-yellow-800: #251C00;

/* Error */
--color-red-50: #FFEDEA;
--color-red-100: #FEE0DA;
--color-red-200: #FFB0A3;
--color-red-300: #FF7966;
--color-red-400: #F13B29;
--color-red-500: #CA0F01;
--color-red-600: #980901;
--color-red-700: #690400;
--color-red-800: #3E0200;

/* ✅ Primitives below this line are okay to use directly */

/* Font primitives */
--font-size-50: 14px;
--font-size-100: 16px;
--font-size-200: 20px;
--font-size-300: 25px;
--font-size-400: 32px;
--font-size-500: 40px;
--font-size-600: 51px;

/* space primitives */
--space-50: 2px;
--space-100: 4px;
--space-200: 8px;
--space-300: 12px;
--space-400: 16px;
--space-500: 20px;
--space-600: 24px;
--space-700: 32px;
--space-800: 64px;
--space-900: 96px;
--space-1000: 128px;

/* Radius size primitives */
--radius-100: 2px;
--radius-100: 4px;
--radius-200: 8px;
--radius-300: 12px;
--radius-400: 16px;
```

## Semantic Variables
Semantic CSS variables are higher-level variables that map to primitives, providing meaningful names that reflect their use in the UI context. They enhance readability and maintainability by abstracting away the underlying values.

Using semantic variables helps in understanding the purpose of a style at a glance and makes it easier to make global changes based on the UI's needs

Use these semantic variables to style components.
### Design Tokens
```css
/* Semantic variables */

/* Colors */
/* Naming convention  */
/* [theme]-color-[concept]-[variant?]-[property]-[variant?]  */

/* Light theme */
/* 🚫 Don't use these tokens directly */
--light-color-primary-background: var(--color-blue-500);
--light-color-primary-text: var(--color-neutral-50);
--light-color-primary-link: var(--color-neutral-50);
--light-color-primary-border: var(--color-blue-500);

--light-color-secondary-background: var(--color-green-300);
--light-color-secondary-text: var(--color-neutral-800);
--light-color-secondary-link: var(--color-neutral-50);
--light-color-secondary-border: var(--color-green-300);

--light-color-default-background: var(--color-neutral-50);
--light-color-default-text: var(--color-neutral-800);
--light-color-default-text-dim: var(--color-neutral-600);
--light-color-default-link: var(--color-blue-500);
--light-color-default-border: var(--color-neutral-200);

--light-color-default-dim-background: var(--color-neutral-100);
--light-color-default-dim-text: var(--color-neutral-800);
--light-color-default-dim-link: var(--color-neutral-600);
--light-color-default-dim-border: var(--color-neutral-300);

--light-color-inverse-background: var(--color-neutral-800);
--light-color-inverse-text: var(--color-neutral-50);
--light-color-inverse-text-dim: var(--color-neutral-200);
--light-color-inverse-link: var(--color-green-300);
--light-color-inverse-border: var(--color-neutral-600);

--light-color-inverse-dim-background: var(--color-neutral-700);
--light-color-inverse-dim-text: var(--color-neutral-50);
--light-color-inverse-dim-link: var(--color-green-300);
--light-color-inverse-dim-border: var(--color-neutral-500);

--light-color-info-background: var(--color-blue-50);
--light-color-info-text: var(--color-blue-600);
--light-color-info-link: var(--color-neutral-800);
--light-color-info-border: var(--color-blue-200);

--light-color-success-background: var(--color-green-50);
--light-color-success-text: var(--color-green-600);
--light-color-success-link: var(--color-neutral-800);
--light-color-success-border: var(--color-green-200);

--light-color-warning-background: var(--color-yellow-50);
--light-color-warning-text: var(--color-warning-600);
--light-color-warning-link: var(--color-neutral-800);
--light-color-warning-border: var(--color-yellow-200);

--light-color-error-dim-background: var(--color-red-500);
--light-color-error-dim-text: var(--color-red-600);
--light-color-error-dim-link: var(--color-neutral-800);
--light-color-error-dim-border: var(--color-red-200);


/* Dark Theme */
/* 🚫 Don't use these tokens directly */
--dark-color-primary-background: var(--color-green-300);
--dark-color-primary-text: var(--color-neutral-800);
--dark-color-primary-link: var(--color-neutral-50);
--dark-color-primary-border: var(--color-green-300);

--dark-color-secondary-background: var(--color-blue-500);
--dark-color-secondary-text: var(--color-neutral-50);
--dark-color-secondary-link: var(--color-neutral-50);
--dark-color-secondary-border: var(--color-blue-500);

--dark-color-default-background: var(--color-neutral-800);
--dark-color-default-text: var(--color-neutral-50);
--dark-color-default-text-dim: var(--color-neutral-200);
--dark-color-default-link: var(--color-green-300);
--dark-color-default-border: var(--color-neutral-600);

--dark-color-default-dim-background: var(--color-neutral-700);
--dark-color-default-dim-text: var(--color-neutral-50);
--dark-color-default-dim-link: var(--color-green-300);
--dark-color-default-dim-border: var(--color-neutral-500);

--dark-color-inverse-background: var(--color-neutral-50);
--dark-color-inverse-text: var(--color-neutral-800);
--dark-color-inverse-text-dim: var(--color-neutral-600);
--dark-color-inverse-link: var(--color-blue-500);
--dark-color-inverse-border: var(--color-neutral-200);

--dark-color-inverse-dim-background: var(--color-neutral-100);
--dark-color-inverse-dim-text: var(--color-neutral-50);
--dark-color-inverse-dim-link: var(--color-green-300);
--dark-color-inverse-dim-border: var(--color-neutral-300);

--dark-color-info-background: var(--color-neutral-800);
--dark-color-info-text: var(--color-blue-300);
--dark-color-info-link: var(--color-neutral-50);
--dark-color-info-border: var(--color-blue-300);

--dark-color-success-background: var(--color-green-50);
--dark-color-success-text: var(--color-green-300);
--dark-color-success-link: var(--color-neutral-50);
--dark-color-success-border: var(--color-green-300);

--dark-color-warning-background: var(--color-yellow-50);
--dark-color-warning-text: var(--color-warning-300);
--dark-color-warning-link: var(--color-neutral-50);
--dark-color-warning-border: var(--color-yellow-300);

--dark-color-error-dim-background: var(--color-red-500);
--dark-color-error-dim-text: var(--color-red-300);
--dark-color-error-dim-link: var(--color-neutral-50);
--dark-color-error-dim-border: var(--color-red-300);

/* Set default theme */
/* ✅ Use these tokens to style components */
--color-primary-background: var(--light-color-primary-background);
--color-primary-text: var(--light-color-primary-text);
--color-primary-link: var(--light-color-primary-link);
--color-primary-border: var(--light-color-primary-border);

--color-secondary-background: var(--light-color-secondary-background);
--color-secondary-text: var(--light-color-secondary-text);
--color-secondary-link: var(--light-color-secondary-link);
--color-secondary-border: var(--light-color-secondary-border);

--color-default-background: var(--light-color-default-background);
--color-default-text: var(--light-color-default-text);
--color-default-text-dim: var(--light-color-default-text-dim);
--color-default-link: var(--light-color-default-link);
--color-default-border: var(--light-color-default-border);

--color-default-dim-background: var(--light-color-default-dim-background);
--color-default-dim-text: var(--light-color-default-dim-text);
--color-default-dim-link: var(--light-color-default-dim-link);
--color-default-dim-border: var(--light-color-default-dim-border);

--color-inverse-background: var(--light-color-inverse-background);
--color-inverse-text: var(--light-color-inverse-text);
--color-inverse-text-dim: var(--light-color-inverse-text-dim);
--color-inverse-link: var(--light-color-inverse-link);
--color-inverse-border: var(--light-color-inverse-border);

--color-inverse-dim-background: var(--light-color-inverse-dim-background);
--color-inverse-dim-text: var(--light-color-inverse-dim-text);
--color-inverse-dim-link: var(--light-color-inverse-dim-link);
--color-inverse-dim-border: var(--light-color-inverse-dim-border);

--color-info-background: var(--light-color-info-background);
--color-info-text: var(--light-color-info-text);
--color-info-link: var(--light-color-info-link);
--color-info-border: var(--light-color-info-border);

--color-success-background: var(--light-color-success-background);
--color-success-text: var(--light-color-success-text);
--color-success-link: var(--light-color-success-link);
--color-success-border: var(--light-color-success-border);

--color-warning-background: var(--light-color-warning-background);
--color-warning-text: var(--light-color-warning-text);
--color-warning-link: var(--light-color-warning-link);
--color-warning-border: var(--light-color-warning-border);

--color-error-dim-background: var(--light-color-error-dim-background);
--color-error-dim-text: var(--light-color-error-dim-text);
--color-error-dim-link: var(--light-color-error-dim-link);
--color-error-dim-border: var(--light-color-error-dim-border);


@media (prefers-color-scheme: dark) {
  :root {
    color-scheme: dark;
    /* Set alternative styles for dark theme */
    --color-primary-background: var(--dark-color-primary-background);
    --color-primary-text: var(--dark-color-primary-text);
    --color-primary-link: var(--dark-color-primary-link);
    --color-primary-border: var(--dark-color-primary-border);

    --color-secondary-background: var(--dark-color-secondary-background);
    --color-secondary-text: var(--dark-color-secondary-text);
    --color-secondary-link: var(--dark-color-secondary-link);
    --color-secondary-border: var(--dark-color-secondary-border);

    --color-default-background: var(--dark-color-default-background);
    --color-default-text: var(--dark-color-default-text);
    --color-default-text-dim: var(--dark-color-default-text-dim);
    --color-default-link: var(--dark-color-default-link);
    --color-default-border: var(--dark-color-default-border);

    --color-default-dim-background: var(--dark-color-default-dim-background);
    --color-default-dim-text: var(--dark-color-default-dim-text);
    --color-default-dim-link: var(--dark-color-default-dim-link);
    --color-default-dim-border: var(--dark-color-default-dim-border);

    --color-inverse-background: var(--dark-color-inverse-background);
    --color-inverse-text: var(--dark-color-inverse-text);
    --color-inverse-text-dim: var(--dark-color-inverse-text-dim);
    --color-inverse-link: var(--dark-color-inverse-link);
    --color-inverse-border: var(--dark-color-inverse-border);

    --color-inverse-dim-background: var(--dark-color-inverse-dim-background);
    --color-inverse-dim-text: var(--dark-color-inverse-dim-text);
    --color-inverse-dim-link: var(--dark-color-inverse-dim-link);
    --color-inverse-dim-border: var(--dark-color-inverse-dim-border);

    --color-info-background: var(--dark-color-info-background);
    --color-info-text: var(--dark-color-info-text);
    --color-info-link: var(--dark-color-info-link);
    --color-info-border: var(--dark-color-info-border);

    --color-success-background: var(--dark-color-success-background);
    --color-success-text: var(--dark-color-success-text);
    --color-success-link: var(--dark-color-success-link);
    --color-success-border: var(--dark-color-success-border);

    --color-warning-background: var(--dark-color-warning-background);
    --color-warning-text: var(--dark-color-warning-text);
    --color-warning-link: var(--dark-color-warning-link);
    --color-warning-border: var(--dark-color-warning-border);

    --color-error-dim-background: var(--dark-color-error-dim-background);
    --color-error-dim-text: var(--dark-color-error-dim-text);
    --color-error-dim-link: var(--dark-color-error-dim-link);
    --color-error-dim-border: var(--dark-color-error-dim-border);
  }
}
```

## Component Specific Styles
Component CSS variables are specific to individual UI components, encapsulating styles that are unique to that component.

These variables make it easy to customize and manage the look and feel of each component independently, promoting reusability and consistency throughout the application.

Use these component variables to style specific components.
### Buttons
```css
/* Naming convention  */
/* [theme]-button-[variant]  */

/* Primary Button */
--light-button-color-background-primary-: var(--color-blue-500);
--light-button-color-background-primary-hover: var(--color-blue-400);
--light-button-color-background-primary-active: var(--color-blue-500);
/* Secondary Button */
--light-button-color-background-secondary-: var(--color-green-300);
--light-button-color-background-secondary-hover: var(--color-green-200);
--light-button-color-background-secondary-active: var(--color-green-300);
```
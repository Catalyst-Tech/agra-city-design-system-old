# agra-city-design-system
## CSS

### Naming Convention Hierarchy & Legend
1. `theme`: Light / Dark.
2. `component`: Button, Card, Chip, etc.
3. `category`: Color, Font, Space, Radius, etc.
4. `property`: Actual CSS properties, e.g. Background, Size, Weight, etc.
5. `variant`: Primary, Secondary, Neutral, etc.
6. `state`: Hover, Active, Disabled, etc.
7. `scale`: 100, 200, 300, etc.

💡 Not all variables names must include all of the above. Each design token list will mention a naming convention pattern that makes sense within its context.

###  Primitives Variables
Primitives in CSS refer to low-level design tokens that represent fundamental values like colors, spacing, typography, etc. These are the raw, unprocessed values used throughout the design system.

These variables act as building blocks, making it easier to maintain and update the styles consistently across the project.

🚫 AVOID using color primitives directly to style components. Color primitives are used to drive the *Semantic Variables*. Use the semantic variables to style components.

💡 While using `blue` as a variant name is generally not recommended, these are primitive tokens that can be bound to a specific color. This is why you shouldn't use these directly in your design.
#### Design Tokens
```css
/* Primitive variables */

/* Naming convention  */
/* --[category]-[variant]-[scale]  */

--color-blue-100: #C9EDFF;
--color-blue-200: #92CEFF;
--color-blue-300: #56AFFC;
--color-blue-400: #338FDA;
--color-blue-500: #0071BA;
--color-blue-600: #00539A;
--color-blue-700: #003870;
--color-blue-800: #012039;

--color-green-50: #F0F8E8;
--color-green-100: #DDF1C6;
--color-green-200: #B0D87D;
--color-green-300: #84BD00;
--color-green-400: #679D00;
--color-green-500: #4A7E00; 
--color-green-600: #2F6000;
--color-green-700: #234000;
--color-green-800: #152200;

--color-neutral-50: #FFFFFF;
--color-neutral-100: #E2E9F0;
--color-neutral-200: #C0C9D2;
--color-neutral-300: #9FAAB5;
--color-neutral-400: #808B96;
--color-neutral-500: #636E78;
--color-neutral-600: #48525B;
--color-neutral-700: #2E3740;
--color-neutral-800: #161E26;
```

### Semantic Variables
Semantic CSS variables are higher-level variables that map to primitives, providing meaningful names that reflect their use in the UI context. They enhance readability and maintainability by abstracting away the underlying values.

Using semantic variables helps in understanding the purpose of a style at a glance and makes it easier to make global changes based on the UI's needs

Use these semantic variables to style components.
#### Design Tokens
```css
/* Semantic variables */

/* Colors */
/* Naming convention  */
/* [theme]-color-background-[background-variant]-[category?]-[variant?]  */
--light-color-background-brand-1: var(--color-blue-500);
--light-color-background-brand-1-text: var(--color-blue-500);
--light-color-background-brand-1-text-dim: var(--color-blue-500);
--light-color-background-brand-1-link: var(--color-blue-500);
--light-color-background-brand-1-border: var(--color-blue-500);

--light-color-background-brand-2: var(--color-blue-500);
--light-color-background-brand-2-text: var(--color-blue-500);
--light-color-background-brand-2-text-dim: var(--color-blue-500);
--light-color-background-brand-2-link: var(--color-blue-500);
--light-color-background-brand-2-border: var(--color-blue-500);

--light-color-background-default: var(--color-blue-500);
--light-color-background-default-text: var(--color-blue-500);
--light-color-background-default-text-dim: var(--color-blue-500);
--light-color-background-default-link: var(--color-blue-500);
--light-color-background-default-border: var(--color-blue-500);

--light-color-background-default-dim: var(--color-blue-500);
--light-color-background-default-dim-text: var(--color-blue-500);
--light-color-background-default-dim-link: var(--color-blue-500);
--light-color-background-default-dim-border: var(--color-blue-500);

--light-color-background-inverse: var(--color-blue-500);
--light-color-background-inverse-text: var(--color-blue-500);
--light-color-background-inverse-text-dim: var(--color-blue-500);
--light-color-background-inverse-link: var(--color-blue-500);
--light-color-background-inverse-border: var(--color-blue-500);

--light-color-background-inverse-dim: var(--color-blue-500);
--light-color-background-inverse-dim-text: var(--color-blue-500);
--light-color-background-inverse-dim-link: var(--color-blue-500);
--light-color-background-inverse-dim-border: var(--color-blue-500);

--light-color-background-info: var(--color-blue-500);
--light-color-background-info-text: var(--color-blue-500);
--light-color-background-info-link: var(--color-blue-500);
--light-color-background-info-border: var(--color-blue-500);

--light-color-background-success: var(--color-blue-500);
--light-color-background-success-text: var(--color-blue-500);
--light-color-background-success-link: var(--color-blue-500);
--light-color-background-success-border: var(--color-blue-500);

--light-color-background-warning: var(--color-blue-500);
--light-color-background-warning-text: var(--color-blue-500);
--light-color-background-warning-link: var(--color-blue-500);
--light-color-background-warning-border: var(--color-blue-500);

--light-color-background-error-dim: var(--color-blue-500);
--light-color-background-error-dim-text: var(--color-blue-500);
--light-color-background-error-dim-link: var(--color-blue-500);
--light-color-background-error-dim-border: var(--color-blue-500);
```

### Component Variables
Component CSS variables are specific to individual UI components, encapsulating styles that are unique to that component.

These variables make it easy to customize and manage the look and feel of each component independently, promoting reusability and consistency throughout the application.

Use these component variables to style specific components.
#### Naming Convention

#### Design Tokens
##### Buttons
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
# agra-city-design-system
## CSS

###  Primitives Variables
```css
/*

Primitives in CSS refer to low-level design tokens that
represent fundamental values like colors, spacing,
typography, etc. They are the raw, unprocessed
values used throughout your styles.

These variables act as building blocks, making it
easier to maintain and update your styles 
consistently across a project.

AVOID using these to style components.
Primitives are used to drive the Semantic Variables.
Use the semantic variables to style components.

*/

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
```css
/*

Semantic CSS variables are higher-level variables that
map to primitives, providing meaningful names that reflect
their use in the UI context. They enhance readability and
maintainability by abstracting away the underlying values.

Using semantic variables helps in understanding the
purpose of a style at a glance and makes it easier to
make global changes based on the UI's needs

Use these semantic variables to style components.

*/

/* Background colors */
/* Naming convention  */
/* color-[optional adjective]-background-[name]-[light/dark]  */
--color-background-brand-1-light: var(--color-blue-500);
--color-background-brand-2-light: var(--color-green-300);
--color-background-default-1-light: var(--color-neutral-50);
--color-background-default-2-light: var(--color-neutral-100);
--color-background-inverse-1-light: var(--color-neutral-800);
--color-background-inverse-2-light: var(--color-neutral-700);

/* Text colors */
/* Naming convention  */
/* color-[optional adjective]-text-on-[background name]-[light/dark]  */
--color-text-on-brand-1-light: var(--color-blue-500);
--color-dim-text-on-brand-1-light: var(--color-blue-500);
--color-link-text-on-brand-1-light: var(--color-blue-500);

--color-text-on-brand-2-light: var(--color-green-300);
--color-dim-text-on-brand-2-light: var(--color-green-300);
--color-link-text-on-brand-2-light: var(--color-green-300);

--color-text-on-default-1-light: var(--color-neutral-50);
--color-dim-text-on-default-1-light: var(--color-neutral-50);
--color-link-text-on-default-1-light: var(--color-neutral-50);

--color-text-on-default-2-light: var(--color-neutral-100);
--color-dim-text-on-default-2-light: var(--color-neutral-100);
--color-link-text-on-default-2-light: var(--color-neutral-100);

--color-text-on-inverse-1-light: var(--color-neutral-800);
--color-dim-text-on-inverse-1-light: var(--color-neutral-800);
--color-link-text-on-inverse-1-light: var(--color-neutral-800);

--color-text-on-inverse-2-light: var(--color-neutral-800);
--color-dim-text-on-inverse-2-light: var(--color-neutral-800);
--color-link-text-on-inverse-2-light: var(--color-neutral-800);
```

### Component Variables
Component CSS variables are specific to individual UI components, encapsulating styles that are unique to that component.

These variables make it easy to customize and manage the look and feel of each component independently, promoting reusability and consistency throughout the application.

Use these component variables to style specific components.
#### Naming Convention
`color-[component]-[variant]-[object]-[optional state]-[light/dark]`
#### Design Tokens
##### Buttons
```css
/* Primary Button */
--color-button-primary-background-light: var(--color-blue-500);
--color-button-primary-background-hover-light: var(--color-blue-400);
--color-button-primary-background-active-light: var(--color-blue-500);
/* Secondary Button */
--color-button-secondary-background-light: var(--color-green-300);
--color-button-secondary-background-hover-light: var(--color-green-200);
--color-button-secondary-background-active-light: var(--color-green-300);
```
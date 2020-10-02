# Boost's Bread and Butter

## Installation

```js
yarn add b3
```

## Usage

### SCSS

In your application SCSS File

```scss
@import "b3/src/scss/init";

// override b3 core variables (like colors and sizes and fonts)
@import "variables";
// override uikit variables for components
@import "themes/base";
@import "themes/text";

@import "b3/src/scss/variables";
@import "b3/src/scss/mixins";

// define uikit mixins to customize uikit to your project
@import "themes/base_mixins";
@import "themes/text_mixins";

@import "b3/src/scss/finalize";

// your blocks / other scss
@import "blocks/whatever"; 
```

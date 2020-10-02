# Boost's Bread and Butter

## Installation

```js
yarn add b3
```

## Usage

### SCSS

In your application SCSS File

```scss
@import "b3/src/scss/initialize";

// ==================================================
// Setup application scss variables here
// e.g. @import 'variables/palette';
// ==================================================

// ==================================================
// Override B3 core variables here
// e.g. @import 'core-variables';
// ==================================================

// ==================================================
// Override UIkit component variables here
// e.g. @import 'themes/button';
// ==================================================

@import "b3/src/scss/variables";
@import "b3/src/scss/mixins";

// ==================================================
// Override UIkit component mixins here
// e.g. @import 'themes/button-mixins';
// ==================================================

@import 'b3/src/scss/finalize';

// ==================================================
// Import any extra application scss last
// e.g. @import 'blocks/footer';
// ==================================================
```

# Boost's Bread and Butter

A design system staple for Boost's design process. Based on UIKit.

## Installation & usage

```js
yarn add https://github.com/boost/b3.git
```

Create the following directory structure in you stylesheets folder.

```bash
stylesheets/
  b3-config.scss # here is where you override B3 variables

  theme/
    ... # place your UIKit component overrides here (variables & mixins)

  ... # place another other code in folders at the root, e.g. blocks/footer.scss

  application.scss
```

Copy this scss into your `application.scss`.

```scss
// application.scss

// 1. Import B3 functions
@import 'b3/src/scss/core/functions';

// 2. Optionally import Open Sans font from CDN
// If you don't want to use a CDN, exclude this step and setup Open Sans as part
// of your projects asset pipeline.
@import 'b3/src/scss/fonts/open-sans';

// 3. Configure B3 variables
@import 'b3-config';
// 4. Import B3 config, which sets up the variables using your provided config.
@import 'b3/src/scss/config';

// 5. Configure any specific UIKit component variables here.
// e.g.
// @import 'theme/base';
// @import 'theme/button';
// @import 'theme/form';
// @import 'theme/badge';

// 6. Import the B3 UIKit config.
@import 'b3/src/scss/uikit-config';

// 7. Override any specific UIKit component mixins here.
// e.g.
// @import 'theme/base-mixins';
// @import 'theme/button-mixins';
// @import 'theme/form-mixins';
// @import 'theme/badge-mixins';
// If B3 provides it's own definition of the UIkit mixin you want to extend,
// you'll need to re-include it when you define it.
// i.e. if you define `hook-button`, you may want to include `b3-hook-button`.

// 8. Import UIKit using B3.
@import 'b3/src/scss/uikit';
// 9. Import b3's extra utilities and grid etc.
@import 'b3/src/scss/core/utilities/all';
@import 'b3/src/scss/core/grid';

// 10. Import any extra application scss last.
// e.g.
// @import 'blocks/footer';
// @import 'functions/conversions;
```

```scss
// b3-config.scss

// Override any b3 core variables using the mixins defined in the B3 configs,
// in `b3/src/scss/config.scss`. They include your overrides in the correct
// place so that dependant variables are caclulated correctly.
@include b3-config-spacing {}
@include b3-config-colors {}
@include b3-config-typography {}
@include b3-config-borders {}
@include b3-config-forms {}
@include b3-config-shadows {}
```

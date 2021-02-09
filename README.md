# Boost's Bread and Butter

## Installation & usage

```js
yarn add https://github.com/boost/b3.git
```

Create the following directory structure in you stylesheets folder.

```bash
stylesheets/
  core/
    variables.scss # here is where you override B3 variables

  variables/
    ... # place your own variables in here

  theme/
    ... # place your UIKit component code here (variables & mixins)

  ... # place another other code in folders at the root, e.g. blocks/footer.scss

  application.scss
```

Copy this scss into your `application.scss`.

```scss
// 1. Import B3 initialization
@import 'b3/src/scss/initialize';

// 2. Setup all application scss variables here.
// e.g.
// @import 'variables/palette';
// @import 'variables/spacing';
// @import 'variables/fonts';

// 3. Configure/override B3 core variables here
// You'll need to make this core/variables.scss file. This is where you
// configure/override all the core b3 variables. B3 has an equivalent file that
// you can look at to see what variables you can override.
// See: `b3/src/scss/core/variables.scss`.
@import 'core/variables';

// 4. Override UIkit component variables here
// e.g.
// @import 'theme/base';
// @import 'theme/button';
// @import 'theme/form';
// @import 'theme/badge';

// 5. Import B3 variables (includes UIKit variables)
@import 'b3/src/scss/variables';

// 6. Import B3 mixins (includes UIKit mixins)
@import 'b3/src/scss/mixins';

// 7. Override UIkit component mixins here
// e.g.
// @import 'theme/base-mixins';
// @import 'theme/button-mixins';
// @import 'theme/form-mixins';
// @import 'theme/badge-mixins';

@import 'b3/src/scss/finalize';

// 8. Import any extra application scss last
// e.g.
// @import 'blocks/footer';
// @import 'functions/conversions;
```

# Boost's Bread and Butter

A design system staple for Boost's design process. Based on UIKit.

## Installation & usage

```js
yarn add https://github.com/boost/b3.git
```

Create the following directory/file structure in you stylesheets folder.

```bash
stylesheets/
  b3-config/ # here is where you override B3 variables
    borders.scss
    colors.scss
    forms.scss
    shadows.scss
    spacing.scss
    typography.scss

  theme/ # place your UIKit component overrides here (variables & mixins)
    _import-mixins.scss # include your mixins here
    _import-variables.scss # include your variables here

  ... # place another other code in folders at the root, e.g. blocks/footer.scss

  application.scss
```

Add this scss into your `application.scss`.
```scss
@import 'b3/src/scss/b3'
```

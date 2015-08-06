# Material Design Lite for Sass

[![Gem Version](https://badge.fury.io/rb/material_design_lite-sass.svg)](http://badge.fury.io/rb/material_design_lite-sass)
[![Build Status](https://travis-ci.org/rubysamurai/material_design_lite-sass.svg?branch=master)](https://travis-ci.org/rubysamurai/material_design_lite-sass)

[Material Design Lite](http://www.getmdl.io/) (MDL) is a library of CSS and JavaScript components, that lets you add Material Design look to your websites. Material Design Lite is maintained by [Google](https://github.com/google/material-design-lite).

`material_design_lite-sass` is a Sass-powered version of Material Design Lite for your applications. It allows to include all of Material Design Lite components at once or load them individually.

## Installation

Material Design Lite website uses Material Icons and Roboto font for some code examples, these icons and font are not included with `material_design_lite-sass` at this time.

### Ruby on Rails

Open your Rails application's `Gemfile` and add this line:

```ruby
gem 'material_design_lite-sass'
```

Save `Gemfile` and execute `bundle` command to install the gem.

Open  `/app/assets/stylesheets/application.scss` file and add this line:

```scss
@import 'material';
```

> **Note:** Default Rails installation comes with `.css` file extension for stylesheet assests files, make sure you change it to `.scss` and remove all the `//= require` and `//= require_tree` statements from file. Alternatively, to keep original `application.css` file, you can create `custom.scss` file in the same folder and import `material` there.

Open  `app/assets/javascripts/application.js` file and add this line:

```
//= require material
```
Restart Rails web server if it was running and now your Rails application is powered by Sass version of Material Design Lite.

## Usage

By default, using `@import 'material';` and `//= require material`, all of Material Design Lite components are imported. You can also import components individually.

To import specific JavaScript components, first you need to include support components:

```
//= require material/mdlComponentHandler
//= require material/rAF
```

Then include desired Material Design Lite JavaScript component:

```
//= require material/button
//= require material/checkbox
//= require material/data-table
//= require material/icon-toggle
//= require material/layout
//= require material/menu
//= require material/progress
//= require material/radio
//= require material/ripple
//= require material/slider
//= require material/spinner
//= require material/switch
//= require material/tabs
//= require material/textfield
//= require material/tooltip
```

Individual Sass components can be included like this:

```scss
@import 'material/animation';
@import 'material/badge';
@import 'material/button';
@import 'material/card';
@import 'material/checkbox';
@import 'material/color-definitions';
@import 'material/data-tables';
@import 'material/functions';
@import 'material/grid';
@import 'material/icon-toggle';
@import 'material/layout';
@import 'material/mega_footer';
@import 'material/mini_footer';
@import 'material/menu';
@import 'material/palette';
@import 'material/progress';
@import 'material/radio';
@import 'material/resets';
@import 'material/ripple';
@import 'material/shadow';
@import 'material/slider';
@import 'material/spinner';
@import 'material/switch';
@import 'material/tabs';
@import 'material/textfield';
@import 'material/tooltip';
@import 'material/typography';
```

### Variables

Sass version provides many variables to make customization process convenient. The full set of Material Design Lite variables can be found [here](https://github.com/rubysamurai/material_design_lite-sass/blob/master/vendor/assets/stylesheets/material/_variables.scss).

To override the variable it must be redefined before the `@import` directive, like this:

```scss
$layout-header-bg-color: #000 !default;
@import 'material';
```

## Versioning

Material Design Lite for Sass follows the upstream version of Google's Material Design Lite. But last version number may be ahead, in case there is a need to release project specific changes.

Please always refer to the [CHANGELOG](https://github.com/rubysamurai/material_design_lite-sass/blob/master/CHANGELOG.md) when upgrading.

## Contributing

Anyone is welcome to contribute to Material Design Lite for Sass. Please [raise an issue](https://github.com/rubysamurai/material_design_lite-sass/issues), fork the project, make changes to your forked repository and submit a pull request.

## Credits

Material Design Lite for Sass is inspired from [bootstrap-sass](https://github.com/twbs/bootstrap-sass) by Twitter Bootstrap team.

## License

Material Design Lite © Google, 2015. Licensed under an [Apache-2](https://github.com/google/material-design-lite/blob/master/LICENSE) license.

`material_design_lite-sass` © Dmitriy Tarasov, 2015. Released under a [MIT](https://github.com/rubysamurai/material_design_lite-sass/blob/master/LICENSE.txt) licence.

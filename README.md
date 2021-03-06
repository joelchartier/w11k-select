# w11k-select - Single- and Multi-Select Directive for AngularJS

w11k-select is an AngularJS directive created to replace the default HTML select element which has a poor usability for most use cases particularly in desktop browsers.

Features:

* Single- and multi-select
* High performance and usability even with hundreds of options
* Filter options to find the right one quickly
* Uses Twitter Bootstrap markup / styling, comes with default css but easy to adjust / override
* Disabled state and required-validation
* Customisable texts (placeholders and selected representation)


## Documentation and Demo

See Project Website at http://w11k.github.com/w11k-select
 

## Installation

* Install via Bower (w11k-select) or download manually from our release repository (https://github.com/w11k/w11k-select-bower)
* Include scripts into your application (w11k-select and dependencies):
  * AngularJS
  * bind-once
  * w11k-dropdownToggle
  * w11k-select
  * font-awesome (optional)
* Add dependency to w11k-select to your angular module


## Usage

```
<div w11k-select
     w11k-select-config="config"
     w11k-select-options="option.value as option.label for option in options.data"
     ng-model="selected.data"
     >
</div>
```    
w11k-select-config is optional and takes a config object or an array with config objects. The value is evaluated against the surrounding scope. If an array is given, all contained config object will be merged into one config object internally. Later config objects override values of previous config objects (like jQuery.extend or _.merge).

You can use different formats to specify the configuration. Some examples:

    // reference an object or array from scope:
    w11k-select-config="config"
  
    // define an object with an object literal:
    w11k-select-config="{ required: true }"
  
    // define an array via literal referencing an object from scope and define an object
    w11k-select-config="[commonConfig, { multiple: false }]" 


### Usage without font-awesome

font-awesome is an optional dependency of w11k-select. w11k-select uses font-awesome classes to show icons. If you don't want to include font-awesome in your project, you can use the following classes to style the icons / define their content. Otherwise they will be empty.

This is a sass example to reproduce the default icons. Notice: You don't need this code if you use font-awesome. The font-awesome classes are already included in the template of the directive.

    .w11k-select .icon-deselect-all {
      @extend .fa;
      @extend .fa-times;
    }
    .w11k-select .icon-dropdown-open {
      @extend .fa;
      @extend .fa-chevron-up;
    }
    .w11k-select .icon-dropdown-closed {
      @extend .fa;
      @extend .fa-chevron-down;
    }
    .w11k-select .icon-select-filtered {
      @extend .fa;
      @extend .fa-check-square-o;
    }
    .w11k-select .icon-deselect-filtered {
      @extend .fa;
      @extend .fa-square-o;
    }


## Roadmap

see milestones and issues at https://github.com/w11k/w11k-select/issues


## License

MIT - see LICENSE file

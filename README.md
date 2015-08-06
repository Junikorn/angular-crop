Angular-crop
========

Angular directive that brings jCrop into Angular.

**Table of Contents**  *generated with [DocToc](http://doctoc.herokuapp.com/)*

-  [Angular-crop](#user-content-angular-crop)
    - [Installing](#user-content-installing)
    - [Usage](#user-content-usage)
    - [Configuration](#user-content-configuration)
        - [Settings](#user-content-settings)
        - [Events](#user-content-events)
    - [Contributing](#user-content-contributing)
    - [Legacy notes](#user-content-legacy-notes)
        - [Licence](#user-content-licence)
        - [History](#user-content-history)

### Installing

Currently **WIP**, will be published to `bower` soon.

### Usage

First of all, add `angular-crop` as dependency to your existing application by doing the following:

```js
var yourModule = angular.module("yourModule", ['angular-crop']);
```

Next, apply `angular-crop` directive on any `<img>` element inside your template, like so:

```html
<img ng-src="{{ imageUrl }}" angular-crop></div>
````

### Configuration

#### Settings

All the attributes specified by `jcrop` docs are available.

For further explanation please refer to its documentation [here](http://deepliquid.com/content/Jcrop_Manual.html#Setting_Options).

#### Events

Same as above.

- Following callbacks are available:
    - onChange - *called on every crop change*
    - onRelease - *called on focus out when cropping is finished*
    - onSelect - *called when cropping has stopped but area is still focused*

Callbacks should be passed as e.g. `data-on-change="myScopeOnChangeMethod"`. Every callback receives `coordinates` argument that looks like below:

```js
{
    h: 149
    w: 187
    x: 201
    x2: 388
    y: 52
    y2: 201
}
```

### Contributing

This repository uses [**Airbnb** javascript](https://github.com/airbnb/javascript) style guide along with `jscs` tests to make sure all the requirements are fulfilled. Before doing a pull request, please double check your code.

### Legacy notes

#### Licence

As original repository has been licensed under GPL license and that was changed here to MIT, the whole project has been rewritten from scratch to avoid any legacy issues that may occur in the future. Although to appreciate original author efforts and in order to say thank you for inspiration he gave me I've decided to fork his repository instead of creating a new one.

#### History

As original repository seems to be abandoned, the purpose of this fork is to carry on further development to allow easy usage of JCrop in other projects.

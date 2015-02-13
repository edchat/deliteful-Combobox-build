# deliteful-Combobox-build

Build version of [ibm-js/deliteful/Combobox](https://github.com/ibm-js/deliteful/Combobox).

## Status

No official release yet.

## Installation

_Bower_ release installation:

    $ bower install "https://github.com/edchat/deliteful-Combobox-build.git"

In the future (after it is published) it will be:

    $ bower install deliteful-Combobox-build


## How to use

To load the minified layer you have two options, you can include the layer with a script tag, or you can wrap your main `require`
call with another `require`, requiring `"deliteful-Combobox-build/layer"`. Then you should continue to refer to modules
with `"deliteful/Combobox"`.

For example, to wrap the main require with another require, this code:
```js
require(["app/main", "deliteful/Combobox"], function() {
	...
});
```
Becomes:
```js
require(["deliteful-Combobox-build/layer"], function() {
	require(["app/main", "deliteful/Combobox"], function() {
		...
	});
});
```

Or you can load the "deliteful-Combobox-build/layer" with a script tag, without the extra require for `"deliteful-Combobox-build/layer"` like this:
```
<script src="bower_components/deliteful-Combobox-build/layer.js"></script>
```

Then to use the Combobox widget with a declarative instantiation, add this to your html:
```
  <label>
    <d-Combobox name="option1" checked="true"></d-Combobox>
    Option 1
  </label>
  <label>
    <d-Combobox name="option2"></d-Combobox>
    Option 2
  </label>
  <label>
    <d-Combobox disabled="true" name="option3"></d-Combobox>
    Option 3
  </label>
```
See [`deliteful/Combobox`](https://github.com/ibm-js/deliteful/blob/master/docs/Combobox.md) for full details on how instantiate a Combobox widget.

## Licensing

This project is distributed by the Dojo Foundation and licensed under the ["New" BSD License](./LICENSE).
All contributions require a [Dojo Foundation CLA](http://dojofoundation.org/about/claForm).

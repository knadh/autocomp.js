# autocomp.js

A super tiny Javascript autocomplete / autosuggestion library. Zero dependencies and ~800 bytes minified + gzipped.

[**View demo**](https://knadh.github.io/autocomp.js)

[![demo](https://github.com/knadh/autocomp.js/assets/547147/8bfaa03c-46a0-4e4e-a127-914120265009)](https://knadh.github.io/autocomp.js)


## Usage

### Node
```shell
npm install @knadh/autocomp
```

```javascript
import { autocomp } from @knadh/autocomp;

autocomp(document.querySelector("#q"), {
	onQuery: async (val) => {
		// fetch() or whatever that fetches/generates results.
		return ["results", "here"];
	},

	onSelect: (val, items) => {
		alert(val);
		return val;
	}
});
```

Check the [demo source](https://github.com/knadh/autocomp.js/blob/master/index.html) to see advanced usage and basic CSS styles.

### ES6 module
Check the [demo source](https://github.com/knadh/autocomp.js/blob/master/index.html) to use the lib in `<script>` directly on an HTML page.

Licensed under the MIT License.

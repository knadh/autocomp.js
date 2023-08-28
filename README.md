# autocomp.js

A super tiny Javascript autocomplete / autosuggestion library. Zero dependencies and ~800 bytes minified + gzipped.

[**View demo**](https://knadh.github.io/autocomp.js)

[![demo](https://github.com/knadh/autocomp.js/assets/547147/c241f264-3a8e-4c2c-a1a4-4a01d077b09f)](https://knadh.github.io/autocomp.js)

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

	onSelect: (val) => {
		alert(val);
		return val;
	}
});
```

Check the [demo source](https://github.com/knadh/autocomp.js/blob/master/docs/index.html) to see advanced usage and basic CSS styles.

### ES6 module
Check the [demo source](https://github.com/knadh/autocomp.js/blob/master/docs/index.html) to use the lib in `<script>` directly on an HTML page.

Licensed under the MIT License.

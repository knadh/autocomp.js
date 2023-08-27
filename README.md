# autocomp.js

A super tiny Javascript autocomplete / autosuggestions library. 

Zero dependencies and ~800 bytes Gzipped.

[**View demo**](https://knadh.github.io/autocomp.js/docs/).

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

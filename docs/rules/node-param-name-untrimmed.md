[//]: # "File generated from a template. Do not edit this file directly."

# node-param-name-untrimmed

`name` in node parameter or in fixed collection section must be trimmed.

📋 This rule is part of the `plugin:flowease-nodes-base/nodes` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
const test = {
	displayName: "Operation",
	name: "operation  ",
	type: "string",
	default: "",
};

const test = {
	displayName: "Test",
	name: "test",
	type: "fixedCollection",
	default: "a",
	options: [
		{
			displayName: "Details",
			name: "   details    ",
			values: [
				{
					displayName: "A",
					name: "a",
					type: "string",
					default: "",
				},
			],
		},
	],
};
```

✅ Example of **correct** code:

```js
const test = {
	displayName: "Operation",
	name: "operation",
	type: "string",
	default: "",
};
```

## Links

- [Rule source](../../lib/rules/node-param-name-untrimmed.ts)
- [Test source](../../tests/node-param-name-untrimmed.test.ts)
[//]: # "File generated from a template. Do not edit this file directly."

# node-param-description-identical-to-display-name

`description` in node parameter must not be identical to `displayName`.

📋 This rule is part of the `plugin:flowease-nodes-base/nodes` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
const test = {
	displayName: "Test",
	name: "test",
	type: "string",
	default: "",
	description: "The test",
};
```

✅ Example of **correct** code:

```js
const test = {
	displayName: "Test",
	name: "test",
	type: "string",
	default: "",
	description: "This is a test",
};
```

## Links

- [Rule source](../../lib/rules/node-param-description-identical-to-display-name.ts)
- [Test source](../../tests/node-param-description-identical-to-display-name.test.ts)

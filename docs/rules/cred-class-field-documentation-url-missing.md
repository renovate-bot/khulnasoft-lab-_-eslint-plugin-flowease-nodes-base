[//]: # "File generated from a template. Do not edit this file directly."

# cred-class-field-documentation-url-missing

`documentationUrl` field in credential class must be present.

📋 This rule is part of the `plugin:flowease-nodes-base/credentials` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
class TestApi implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
}
```

✅ Example of **correct** code:

```js
class MyTestApi implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
    documentationUrl = 'myTest';
}
```

## Links

- [Rule source](../../lib/rules/cred-class-field-documentation-url-missing.ts)
- [Test source](../../tests/cred-class-field-documentation-url-missing.test.ts)

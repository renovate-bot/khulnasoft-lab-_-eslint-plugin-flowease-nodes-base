[//]: # "File generated from a template. Do not edit this file directly."

# cred-class-field-documentation-url-miscased

`documentationUrl` field in credential class must be camel cased. Only applicable to nodes in the main repository.

📋 This rule is part of the `plugin:flowease-nodes-base/credentials` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
class TestApi implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
    documentationUrl = 'MyTest';
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

- [Rule source](../../lib/rules/cred-class-field-documentation-url-miscased.ts)
- [Test source](../../tests/cred-class-field-documentation-url-miscased.test.ts)
[//]: # "File generated from a template. Do not edit this file directly."

# cred-class-name-unsuffixed

Credential class name must be suffixed with `-Api`.

📋 This rule is part of the `plugin:flowease-nodes-base/credentials` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
class MyTest implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
    documentationUrl = 'myTest';
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

- [Rule source](../../lib/rules/cred-class-name-unsuffixed.ts)
- [Test source](../../tests/cred-class-name-unsuffixed.test.ts)

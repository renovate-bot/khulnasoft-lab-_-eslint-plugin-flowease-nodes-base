[//]: # "File generated from a template. Do not edit this file directly."

# cred-class-field-placeholder-url-missing-eg

`placeholder` for a URL in credential class must be prepended with `e.g.`.

📋 This rule is part of the `plugin:flowease-nodes-base/credentials` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
class MyTestOAuth2Api implements ICredentialType {
    name = 'myTestOAuth2Api';
    displayName = 'My Test OAuth2 API';
    documentationUrl = 'myTest';
    extends = [
        'oAuth2Api',
    ];
    placeholder = 'https://flowease.io';
}
```

✅ Example of **correct** code:

```js
class MyTestOAuth2Api implements ICredentialType {
    name = 'myTestOAuth2Api';
    displayName = 'My Test OAuth2 API';
    documentationUrl = 'myTest';
    extends = [
        'oAuth2Api',
    ];
    placeholder = 'e.g. https://flowease.io';
}
```

## Links

- [Rule source](../../lib/rules/cred-class-field-placeholder-url-missing-eg.ts)
- [Test source](../../tests/cred-class-field-placeholder-url-missing-eg.test.ts)

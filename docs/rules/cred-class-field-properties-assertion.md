[//]: # "File generated from a template. Do not edit this file directly."

# cred-class-field-properties-assertion

In a credential class, the field `properties` must be typed `INodeProperties` and individual properties must have no assertions.

📋 This rule is part of the `plugin:flowease-nodes-base/credentials` config.

🔧 Run ESLint with `--fix` option to autofix the issue flagged by this rule.

## Examples

❌ Example of **incorrect** code:

```js
class TestApi implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
    documentationUrl = 'myTest';
    properties = [
        {
            displayName: 'API Root URL',
            name: 'URL',
            type: 'string' as NodePropertyTypes,
            default: 'https://kf.kobotoolbox.org/',
        },
    ];
}

class TestApi implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
    documentationUrl = 'myTest';
    properties: INodeProperties[] = [
        {
            displayName: 'API Root URL',
            name: 'URL',
            type: 'string' as NodePropertyTypes,
            default: 'https://kf.kobotoolbox.org/',
        },
    ];
}
```

✅ Example of **correct** code:

```js
class TestApi implements ICredentialType {
    name = 'myTestApi';
    displayName = 'My Test API';
    documentationUrl = 'myTest';
    properties: INodeProperties[] = [
        {
            displayName: 'API Root URL',
            name: 'URL',
            type: 'string',
            default: 'https://kf.kobotoolbox.org/',
        },
    ];
}
```

## Links

- [Rule source](../../lib/rules/cred-class-field-properties-assertion.ts)
- [Test source](../../tests/cred-class-field-properties-assertion.test.ts)

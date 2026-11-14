# MockAccountManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockAccountManager

Kotlin| [Java](MockAccountManager.md) 
| --- | --- |

```
open class MockAccountManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.mock.MockAccountManager](MockAccountManager.md) |

| **This class was deprecated in API level 28.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/ tools/testing-support-library/index.html).

A mock [android.accounts.AccountManager](../android.accounts/AccountManager.md) class.

Provided for use by`android.test.IsolatedContext`.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [AccountManager](../android.accounts/AccountManager.md)! | [newMockAccountManager](MockAccountManager.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Create a new mock [AccountManager](../android.accounts/AccountManager.md) instance. |

## Public methods

### newMockAccountManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newMockAccountManager(context: Context!): AccountManager!
```

**Deprecated:** *Deprecated in Java.*

Create a new mock [AccountManager](../android.accounts/AccountManager.md) instance.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the [Context](../android.content/Context.md) to which the returned object belongs. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------|
| [AccountManager](../android.accounts/AccountManager.md)! | the new instance. |

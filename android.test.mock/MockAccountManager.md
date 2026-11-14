# MockAccountManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MockAccountManager

Kotlin| [Java](https://developer.android.com/reference/android/test/mock/MockAccountManager "View this page in Java") 

```
open class MockAccountManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.mock.MockAccountManager](https://developer.android.com/reference/kotlin/android/test/mock/MockAccountManager#) |

| **This class was deprecated in API level 28.**
|
| Use a mocking framework like [Mockito](https://github.com/mockito/mockito). New tests should be written using the [Android Testing Support Library](https://developer.android.com/ tools/testing-support-library/index.html).

A mock [android.accounts.AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#) class.

Provided for use by`android.test.IsolatedContext`.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#)! | [newMockAccountManager](https://developer.android.com/reference/kotlin/android/test/mock/MockAccountManager#newMockAccountManager(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Create a new mock [AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#) instance. |

## Public methods

### newMockAccountManager

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newMockAccountManager(context: Context!): AccountManager!
```

**Deprecated:** *Deprecated in Java.*

Create a new mock [AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#) instance.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) to which the returned object belongs. |

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------|
| [AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager.html#)! | the new instance. |

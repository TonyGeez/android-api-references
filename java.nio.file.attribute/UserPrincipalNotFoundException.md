# UserPrincipalNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UserPrincipalNotFoundException

```
open class UserPrincipalNotFoundException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.attribute.UserPrincipalNotFoundException](UserPrincipalNotFoundException.md) |

Checked exception thrown when a lookup of [UserPrincipal](UserPrincipal.md) fails because the principal does not exist.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UserPrincipalNotFoundException](UserPrincipalNotFoundException.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](UserPrincipalNotFoundException.md))`()` Returns the user principal name if this exception was created with the user principal name that was not found, otherwise`null`. |

## Public constructors

### UserPrincipalNotFoundException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UserPrincipalNotFoundException(name: String!)
```

Constructs an instance of this class.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the principal name; may be`null` |

## Public methods

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the user principal name if this exception was created with the user principal name that was not found, otherwise`null`.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the user principal name or`null` |

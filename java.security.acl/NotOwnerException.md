# NotOwnerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NotOwnerException

```
open class NotOwnerException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.security.acl.NotOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/NotOwnerException#) |
| --- | --- | --- | --- |

| **This exception was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

This is an exception that is thrown whenever the modification of an object (such as an Access Control List) is only allowed to be done by an owner of the object, but the Principal attempting the modification is not an owner.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NotOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/NotOwnerException#NotOwnerException())`()` Constructs a NotOwnerException. |

## Public constructors

### NotOwnerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NotOwnerException()
```

Constructs a NotOwnerException.

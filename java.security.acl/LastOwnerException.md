# LastOwnerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LastOwnerException

```
open class LastOwnerException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.security.acl.LastOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/LastOwnerException#) |
| --- | --- | --- | --- |

| **This exception was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

This is an exception that is thrown whenever an attempt is made to delete the last owner of an Access Control List.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LastOwnerException](https://developer.android.com/reference/kotlin/java/security/acl/LastOwnerException#LastOwnerException())`()` Constructs a LastOwnerException. |

## Public constructors

### LastOwnerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LastOwnerException()
```

Constructs a LastOwnerException.

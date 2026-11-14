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
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [java.security.acl.LastOwnerException](LastOwnerException.md) |
| --- | --- | --- | --- |

| **This exception was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

This is an exception that is thrown whenever an attempt is made to delete the last owner of an Access Control List.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LastOwnerException](LastOwnerException.md))`()` Constructs a LastOwnerException. |

## Public constructors

### LastOwnerException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LastOwnerException()
```

Constructs a LastOwnerException.

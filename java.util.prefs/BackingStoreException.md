# BackingStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackingStoreException

```
open class BackingStoreException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.util.prefs.BackingStoreException](https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException#) |
| --- | --- | --- | --- |

Thrown to indicate that a preferences operation could not complete because of a failure in the backing store, or a failure to contact the backing store.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BackingStoreException](https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException#BackingStoreException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a BackingStoreException with the specified detail message. |
| [BackingStoreException](https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException#BackingStoreException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a BackingStoreException with the specified cause. |

## Public constructors

### BackingStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackingStoreException(s: String!)
```

Constructs a BackingStoreException with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### BackingStoreException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackingStoreException(cause: Throwable!)
```

Constructs a BackingStoreException with the specified cause.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause |

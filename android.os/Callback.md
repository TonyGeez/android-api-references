# Handler.Callback

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](https://developer.android.com/reference/android/os/Handler.Callback "View this page in Java") 
| --- | --- |

```
interface Callback
```

| [android.os.Handler.Callback](https://developer.android.com/reference/kotlin/android/os/Handler.Callback#) |

Callback interface you can use when instantiating a Handler to avoid having to implement your own subclass of Handler.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMessage](https://developer.android.com/reference/kotlin/android/os/Handler.Callback#handleMessage(android.os.Message))`(`msg:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message)`)` <br /> |

## Public methods

### handleMessage

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun handleMessage(msg: Message): Boolean
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [Message](https://developer.android.com/reference/kotlin/android/os/Message):A [Message](https://developer.android.com/reference/kotlin/android/os/Message) object This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if no further handling is desired |

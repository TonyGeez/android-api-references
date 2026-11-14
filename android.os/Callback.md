# Handler.Callback

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](../android/os/Handler.Callback.md) 
| --- | --- |

```
interface Callback
```

| [android.os.Handler.Callback](../android/os/Handler.Callback.md) |

Callback interface you can use when instantiating a Handler to avoid having to implement your own subclass of Handler.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMessage](../android/os/Handler.Callback.md))`(`msg:` ` [Message](../android/os/Message.md)`)` <br /> |

## Public methods

### handleMessage

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun handleMessage(msg: Message): Boolean
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `msg` | [Message](../android/os/Message.md):A [Message](../android/os/Message.md) object This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if no further handling is desired |

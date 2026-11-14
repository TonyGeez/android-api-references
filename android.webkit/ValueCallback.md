# ValueCallback

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueCallback

Kotlin| [Java](../android/webkit/ValueCallback.md) 
| --- | --- |

```
interface ValueCallback<T : Any!>
```

| [android.webkit.ValueCallback](../android/webkit/ValueCallback.md) |

A callback interface used to provide values asynchronously.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceiveValue](../android/webkit/ValueCallback.md))`(`value:` `T`)` Invoked when the value is available. |

## Public methods

### onReceiveValue

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onReceiveValue(value: T): Unit
```

Invoked when the value is available.

| Parameters ||
|---------|--------------|
| `value` | T:The value. |

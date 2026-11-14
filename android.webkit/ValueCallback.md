# ValueCallback

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ValueCallback

Kotlin| [Java](https://developer.android.com/reference/android/webkit/ValueCallback "View this page in Java") 
| --- | --- |

```
interface ValueCallback<T : Any!>
```

| [android.webkit.ValueCallback](https://developer.android.com/reference/kotlin/android/webkit/ValueCallback#) |

A callback interface used to provide values asynchronously.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceiveValue](https://developer.android.com/reference/kotlin/android/webkit/ValueCallback#onReceiveValue(android.webkit.ValueCallback.T))`(`value:` `T`)` Invoked when the value is available. |

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

# ContextParams

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContextParams

Kotlin| [Java](ContextParams.md) 
| --- | --- |

```
class ContextParams
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.ContextParams](ContextParams.md) |

This class represents rules around how a context being created via [Context.createContext](Context.md))should behave.

One of the dimensions to customize is how permissions should behave. For example, you can specify how permission accesses from a context should be attributed in the platform's permission tracking system.

The two main types of attribution are: against an attribution tag which is an arbitrary string your app specifies for the purposes of tracking permission accesses from a given portion of your app; against another package and optionally its attribution tag if you are accessing the data on behalf of another app and you will be passing that data to this app, recursively. Both attributions are not mutually exclusive.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/content/ContextParams.Builder.md) Builder for creating a [ContextParams](ContextParams.md). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getAttributionTag](ContextParams.md))`()` <br /> |
| [AttributionSource](AttributionSource.md)? | [getNextAttributionSource](ContextParams.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldRegisterAttributionSource](ContextParams.md))`()` <br /> |
| --- | --- |

## Public methods

### getAttributionTag

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAttributionTag(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The attribution tag. This value may be`null`. |

### getNextAttributionSource

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNextAttributionSource(): AttributionSource?
```

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [AttributionSource](AttributionSource.md)? | The receiving attribution source. This value may be`null`. |

### shouldRegisterAttributionSource

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldRegisterAttributionSource(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the attribution source associated with the Context being created should be registered. This value cannot be`null`. |

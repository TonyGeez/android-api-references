# AdServicesOutcomeReceiver

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdServicesOutcomeReceiver

Kotlin| [Java](AdServicesOutcomeReceiver.md) 
| --- | --- |

```
interface AdServicesOutcomeReceiver<R : Any!, E : Throwable!>
```

| [android.adservices.common.AdServicesOutcomeReceiver](AdServicesOutcomeReceiver.md) |

| **This interface was deprecated in API level 36.**
|
| use [android.os.OutcomeReceiver](../android.os/OutcomeReceiver.md) instead. Android R is no longer supported.

Callback interface intended for use when an asynchronous operation may result in a failure. Exact copy of the [android.os.OutcomeReceiver](../android.os/OutcomeReceiver.md) class, re-defined in the AdServices package for backwards compatibility to Android R.

This interface may be used in cases where an asynchronous API may complete either with a value or with a [Throwable](../java.lang/Throwable.md) that indicates an error.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](AdServicesOutcomeReceiver.md))`(`error:` `E`)` Called when the asynchronous operation fails. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResult](AdServicesOutcomeReceiver.md))`(`result:` `R`)` Called when the asynchronous operation succeeds and delivers a result value. |

## Public methods

### onError

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(error: E): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the asynchronous operation fails. The mode of failure is indicated by the [Throwable](../java.lang/Throwable.md) passed as an argument to this method.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | E:A subclass of [Throwable](../java.lang/Throwable.md) with more details about the error that occurred. This value cannot be`null`. |

### onResult

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onResult(result: R): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the asynchronous operation succeeds and delivers a result value.

| Parameters ||
|----------|------------------------------------------------------|
| `result` | R:The value delivered by the asynchronous operation. |

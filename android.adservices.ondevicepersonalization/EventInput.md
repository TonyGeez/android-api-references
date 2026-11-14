# EventInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventInput

Kotlin| [Java](../android/adservices/ondevicepersonalization/EventInput.md) 
| --- | --- |

```
class EventInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.EventInput](../android/adservices/ondevicepersonalization/EventInput.md) |

The input data for [android.adservices.ondevicepersonalization.IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventInput](../android/adservices/ondevicepersonalization/EventInput.md))`(`requestLogRecord:` ` [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md)?`, `parameters:` ` [PersistableBundle](../android/os/PersistableBundle.md)`)` Creates a new EventInput. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/adservices/ondevicepersonalization/EventInput.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [PersistableBundle](../android/os/PersistableBundle.md) | [getParameters](../android/adservices/ondevicepersonalization/EventInput.md))`()` The Event URL parameters that the service passed to[android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,byte[],java.lang.String)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,%20kotlin.ByteArray,%20kotlin.String))or android. |
| [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md)? | [getRequestLogRecord](../android/adservices/ondevicepersonalization/EventInput.md))`()` The [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md) that was returned as a result of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/adservices/ondevicepersonalization/EventInput.md))`()` <br /> |

## Public constructors

### EventInput

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EventInput(
    requestLogRecord: RequestLogRecord?, 
    parameters: PersistableBundle)
```

Creates a new EventInput.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestLogRecord` | [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md)?:The [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md) that was returned as a result of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md)). This value may be`null`. |
| `parameters` | [PersistableBundle](../android/os/PersistableBundle.md):The Event URL parameters that the service passed to[android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,byte[],java.lang.String)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,%20kotlin.ByteArray,%20kotlin.String))or android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithRedirect(android.os.PersistableBundle,Uri). This value cannot be`null`. |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getParameters

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameters(): PersistableBundle
```

The Event URL parameters that the service passed to[android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,byte[],java.lang.String)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,%20kotlin.ByteArray,%20kotlin.String))or android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithRedirect(android.os.PersistableBundle,Uri).

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------|
| [PersistableBundle](../android/os/PersistableBundle.md) | This value cannot be`null`. |

### getRequestLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestLogRecord(): RequestLogRecord?
```

The [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md) that was returned as a result of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md)? | This value may be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

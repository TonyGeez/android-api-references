# EventInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventInput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/EventInput "View this page in Java") 

```
class EventInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.ondevicepersonalization.EventInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput#) |

The input data for [android.adservices.ondevicepersonalization.IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onEvent(android.adservices.ondevicepersonalization.EventInput,%20android.os.OutcomeReceiver)).

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EventInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput#EventInput(android.adservices.ondevicepersonalization.RequestLogRecord,%20android.os.PersistableBundle))`(`requestLogRecord:` ` [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)?`, `parameters:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)`)` Creates a new EventInput. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | [getParameters](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput#getParameters())`()` The Event URL parameters that the service passed to[android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,byte[],java.lang.String)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,%20kotlin.ByteArray,%20kotlin.String))or android. |
| [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)? | [getRequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput#getRequestLogRecord())`()` The [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that was returned as a result of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventInput#hashCode())`()` <br /> |

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
| `requestLogRecord` | [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)?:The [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that was returned as a result of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)). This value may be`null`. |
| `parameters` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#):The Event URL parameters that the service passed to[android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,byte[],java.lang.String)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventUrlProvider#createEventTrackingUrlWithResponse(android.os.PersistableBundle,%20kotlin.ByteArray,%20kotlin.String))or android.adservices.ondevicepersonalization.EventUrlProvider#createEventTrackingUrlWithRedirect(android.os.PersistableBundle,Uri). This value cannot be`null`. |

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
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | This value cannot be`null`. |

### getRequestLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestLogRecord(): RequestLogRecord?
```

The [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) that was returned as a result of [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)? | This value may be`null`. |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

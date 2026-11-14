# ExecuteOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteOutput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/ExecuteOutput "View this page in Java") 
| --- | --- |

```
class ExecuteOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.ExecuteOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#) |

The result returned by [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver))in response to a call to`OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)`from a client app.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput.Builder) A builder for [ExecuteOutput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#) |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBestValue](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getBestValue())`()` An integer value that an [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) may optionally return to a calling app, by setting this field to the value between 0 and [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord)!\> | [getEventLogRecords](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getEventLogRecords())`()` A list of [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord) objects to be written to the EVENTS table. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getOutputData](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getOutputData())`()` A byte array that an [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) may optionally return to a calling app, by setting this field to a non-null value. |
| [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig)? | [getRenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getRenderingConfig())`()` A [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig) object that contains information about the content to be rendered in the client app view. |
| [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord)? | [getRequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#getRequestLogRecord())`()` Persistent data to be written to the REQUESTS table after [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver))completes. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteOutput#hashCode())`()` <br /> |

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

### getBestValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBestValue(): Int
```

An integer value that an [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) may optionally return to a calling app, by setting this field to the value between 0 and [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()). The noise will be added to the value of this field before returned to the caller of [android.adservices.ondevicepersonalization.OnDevicePersonalizationManager#executeInIsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#executeInIsolatedService(android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). In order to get this field, the (calling app package, isolated service package) pair must be present in an allowlist that permits data to be returned and [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest.OutputSpec#buildBestValueSpec](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec#buildBestValueSpec(kotlin.Int))is set.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE:kotlin.Int) or greater |

### getEventLogRecords

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventLogRecords(): MutableList<EventLogRecord!>
```

A list of [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord) objects to be written to the EVENTS table. Each [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord) must be associated with an existing [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) in the REQUESTS table, specified using [EventLogRecord.Builder.setRequestLogRecord(RequestLogRecord)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord.Builder#setRequestLogRecord(android.adservices.ondevicepersonalization.RequestLogRecord)). If the [RequestLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord) is not specified, the [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord) will not be written.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EventLogRecord](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord)!> | This value cannot be`null`. |

### getOutputData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputData(): ByteArray?
```

A byte array that an [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) may optionally return to a calling app, by setting this field to a non-null value. The contents of this array will be returned to the caller of [OnDevicePersonalizationManager.execute](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationManager#execute(android.content.ComponentName,%20android.os.PersistableBundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))if returning data from isolated processes is allowed by policy and the (calling app package, isolated service package) pair is present in an allowlist that permits data to be returned. 

### getRenderingConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRenderingConfig(): RenderingConfig?
```

A [RenderingConfig](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RenderingConfig) object that contains information about the content to be rendered in the client app view. Can be null if no content is to be rendered. 

### getRequestLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestLogRecord(): RequestLogRecord?
```

Persistent data to be written to the REQUESTS table after [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver))completes. If null, no persistent data will be written. 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

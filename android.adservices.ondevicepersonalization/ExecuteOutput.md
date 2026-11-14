# ExecuteOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteOutput

Kotlin| [Java](../android/adservices/ondevicepersonalization/ExecuteOutput.md) 
| --- | --- |

```
class ExecuteOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.ExecuteOutput](../android/adservices/ondevicepersonalization/ExecuteOutput.md) |

The result returned by [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md))in response to a call to`OnDevicePersonalizationManager#execute(ComponentName, PersistableBundle, java.util.concurrent.Executor, OutcomeReceiver)`from a client app.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/ondevicepersonalization/ExecuteOutput.Builder.md) A builder for [ExecuteOutput](../android/adservices/ondevicepersonalization/ExecuteOutput.md) |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBestValue](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`()` An integer value that an [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) may optionally return to a calling app, by setting this field to the value between 0 and [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec.md)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md)!\> | [getEventLogRecords](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`()` A list of [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md) objects to be written to the EVENTS table. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getOutputData](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`()` A byte array that an [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) may optionally return to a calling app, by setting this field to a non-null value. |
| [RenderingConfig](../android/adservices/ondevicepersonalization/RenderingConfig.md)? | [getRenderingConfig](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`()` A [RenderingConfig](../android/adservices/ondevicepersonalization/RenderingConfig.md) object that contains information about the content to be rendered in the client app view. |
| [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md)? | [getRequestLogRecord](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`()` Persistent data to be written to the REQUESTS table after [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md))completes. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/adservices/ondevicepersonalization/ExecuteOutput.md))`()` <br /> |

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

An integer value that an [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) may optionally return to a calling app, by setting this field to the value between 0 and [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest.OutputSpec#getMaxIntValue()](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec.md)). The noise will be added to the value of this field before returned to the caller of [android.adservices.ondevicepersonalization.OnDevicePersonalizationManager#executeInIsolatedService](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.md)). In order to get this field, the (calling app package, isolated service package) pair must be present in an allowlist that permits data to be returned and [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceRequest.OutputSpec#buildBestValueSpec](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceRequest.OutputSpec.md))is set.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.adservices.ondevicepersonalization.ExecuteInIsolatedServiceResponse#DEFAULT_BEST_VALUE](../android/adservices/ondevicepersonalization/ExecuteInIsolatedServiceResponse.md) or greater |

### getEventLogRecords

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventLogRecords(): MutableList<EventLogRecord!>
```

A list of [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md) objects to be written to the EVENTS table. Each [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md) must be associated with an existing [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md) in the REQUESTS table, specified using [EventLogRecord.Builder.setRequestLogRecord(RequestLogRecord)](../android/adservices/ondevicepersonalization/EventLogRecord.Builder.md)). If the [RequestLogRecord](../android/adservices/ondevicepersonalization/RequestLogRecord.md) is not specified, the [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md) will not be written.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [EventLogRecord](../android/adservices/ondevicepersonalization/EventLogRecord.md)!> | This value cannot be`null`. |

### getOutputData

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputData(): ByteArray?
```

A byte array that an [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) may optionally return to a calling app, by setting this field to a non-null value. The contents of this array will be returned to the caller of [OnDevicePersonalizationManager.execute](../android/adservices/ondevicepersonalization/OnDevicePersonalizationManager.md))if returning data from isolated processes is allowed by policy and the (calling app package, isolated service package) pair is present in an allowlist that permits data to be returned. 

### getRenderingConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRenderingConfig(): RenderingConfig?
```

A [RenderingConfig](../android/adservices/ondevicepersonalization/RenderingConfig.md) object that contains information about the content to be rendered in the client app view. Can be null if no content is to be rendered. 

### getRequestLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestLogRecord(): RequestLogRecord?
```

Persistent data to be written to the REQUESTS table after [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md))completes. If null, no persistent data will be written. 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

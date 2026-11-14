Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebTriggerOutput

```
class WebTriggerOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.WebTriggerOutput](WebTriggerOutput.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The ODP APIs are deprecated and will not be supported in future Android releases. There is no direct replacement API available. Developers currently integrated with these APIs must cease further integration efforts. For comprehensive details regarding this deprecation and the future roadmap of Privacy Sandbox on Android, please consult the official Privacy Sandbox developer documentation and announcements: <https://privacysandbox.google.com>

The result that should be returned by `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)`. This class contains data that should be written to the REQUESTS or EVENTS tables. The contents of these tables can be consumed by Federated Learning facilitated model training, or Federated Analytics facilitated cross-device statistical analysis.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput.Builder` A builder for `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput#` |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [EventLogRecord](EventLogRecord.md)!\> | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput#getEventLogRecords()()` A list of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord` objects to be written to the EVENTS table. |
| [RequestLogRecord](RequestLogRecord.md)? | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput#getRequestLogRecord()()` Persistent data to be written to the REQUESTS table after `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)` completes. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/WebTriggerOutput#hashCode()()` Returns a hash code value for the object. |

## Public methods

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getEventLogRecords

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEventLogRecords(): MutableList<EventLogRecord!>
```

**Deprecated:** *Deprecated in Java.*

A list of `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord` objects to be written to the EVENTS table. Each `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord` must be associated with an existing `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord` in the REQUESTS table, specified using `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord.Builder#setRequestLogRecord(android.adservices.ondevicepersonalization.RequestLogRecord)`. If the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/RequestLogRecord` is not specified, the `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord` will not be written. The list can be empty if no data needs to be written to the EVENTS table.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/EventLogRecord!>` | This value cannot be `null`. |

### getRequestLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRequestLogRecord(): RequestLogRecord?
```

**Deprecated:** *Deprecated in Java.*

Persistent data to be written to the REQUESTS table after `https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onWebTrigger(android.adservices.ondevicepersonalization.WebTriggerInput,%20android.os.OutcomeReceiver)` completes. This can be `null` if no data needs to be written to the REQUESTS table.

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

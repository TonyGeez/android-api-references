# EventOutput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EventOutput

Kotlin| [Java](EventOutput.md) 
| --- | --- |

```
class EventOutput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.EventOutput](EventOutput.md) |

The result returned by [IsolatedWorker.onEvent(EventInput, android.os.OutcomeReceiver)](IsolatedWorker.md)).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/adservices/ondevicepersonalization/EventOutput.Builder.md) A builder for [EventOutput](EventOutput.md) |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](EventOutput.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [EventLogRecord](EventLogRecord.md)? | [getEventLogRecord](EventOutput.md))`()` An [EventLogRecord](EventLogRecord.md) to be written to the EVENTS table, if not null. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](EventOutput.md))`()` <br /> |
| --- | --- |

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

### getEventLogRecord

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventLogRecord(): EventLogRecord?
```

An [EventLogRecord](EventLogRecord.md) to be written to the EVENTS table, if not null. Each [EventLogRecord](EventLogRecord.md) is associated with a row in an existing [RequestLogRecord](RequestLogRecord.md) that has been written to the REQUESTS table. 

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

# PrintJob

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintJob

Kotlin| [Java](PrintJob.md) 
| --- | --- |

```
class PrintJob
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.print.PrintJob](PrintJob.md) |

This class represents a print job from the perspective of an application. It contains behavior methods for performing operations on it as well as methods for querying its state. A snapshot of the print job state is represented by the [PrintJobInfo](PrintJobInfo.md) class. The state of a print job may change over time. An application receives instances of this class when creating a print job or querying for its print jobs.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](PrintJob.md))`()` Cancels this print job. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PrintJob.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [PrintJobId](PrintJobId.md)? | [getId](PrintJob.md))`()` Gets the unique print job id. |
| --- | --- |
| [PrintJobInfo](PrintJobInfo.md) | [getInfo](PrintJob.md))`()` Gets the [PrintJobInfo](PrintJobInfo.md) that describes this job. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](PrintJob.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocked](PrintJob.md))`()` Gets whether this print job is blocked. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](PrintJob.md))`()` Gets whether this print job is cancelled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompleted](PrintJob.md))`()` Gets whether this print job is completed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFailed](PrintJob.md))`()` Gets whether this print job is failed. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isQueued](PrintJob.md))`()` Gets whether this print job is queued. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](PrintJob.md))`()` Gets whether this print job is started. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restart](PrintJob.md))`()` Restarts this print job. |
| --- | --- |

## Public methods

### cancel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Unit
```

Cancels this print job. You can request cancellation of a queued, started, blocked, or failed print job. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/print/PrintJob#isQueued()>
- <https://developer.android.com/reference/kotlin/android/print/PrintJob#isStarted()>
- <https://developer.android.com/reference/kotlin/android/print/PrintJob#isBlocked()>
- <https://developer.android.com/reference/kotlin/android/print/PrintJob#isFailed()> 

### equals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): PrintJobId?
```

Gets the unique print job id.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------|
| [PrintJobId](PrintJobId.md)? | The id. This value may be`null`. |

### getInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInfo(): PrintJobInfo
```

Gets the [PrintJobInfo](PrintJobInfo.md) that describes this job.

**Node:**The returned info object is a snapshot of the current print job state. Every call to this method returns a fresh info object that reflects the current print job state.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| [PrintJobInfo](PrintJobInfo.md) | The print job info. This value cannot be`null`. |

### hashCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isBlocked

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBlocked(): Boolean
```

Gets whether this print job is blocked. Such a print job is halted due to an abnormal condition. You can request a cancellation via [cancel()](PrintJob.md)).

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is blocked. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/print/PrintJob#cancel()> 

### isCancelled

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCancelled(): Boolean
```

Gets whether this print job is cancelled. Such a print job was cancelled as a result of a user request. This is a final state. You cannot restart such a print job.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is cancelled. |

### isCompleted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCompleted(): Boolean
```

Gets whether this print job is completed. Such a print job is successfully printed. You can neither cancel nor restart such a print job.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is completed. |

### isFailed

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFailed(): Boolean
```

Gets whether this print job is failed. Such a print job is not successfully printed due to an error. You can request a restart via [restart()](PrintJob.md))or cancel via [cancel()](PrintJob.md)).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is failed. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/print/PrintJob#restart()>
- <https://developer.android.com/reference/kotlin/android/print/PrintJob#cancel()> 

### isQueued

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isQueued(): Boolean
```

Gets whether this print job is queued. Such a print job is ready to be printed. You can request a cancellation via [cancel()](PrintJob.md)).

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is queued. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/print/PrintJob#cancel()> 

### isStarted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStarted(): Boolean
```

Gets whether this print job is started. Such a print job is being printed. You can request a cancellation via [cancel()](PrintJob.md)).

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is started. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/print/PrintJob#cancel()> 

### restart

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun restart(): Unit
```

Restarts this print job. You can request restart of a failed print job. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/print/PrintJob#isFailed()>

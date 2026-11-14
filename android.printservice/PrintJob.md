# PrintJob

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintJob

Kotlin| [Java](https://developer.android.com/reference/android/printservice/PrintJob "View this page in Java") 
| --- | --- |

```
class PrintJob
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.printservice.PrintJob](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#) |

This class represents a print job from the perspective of a print service. It provides APIs for observing the print job state and performing operations on the print job.

**Note:**All methods of this class must be invoked on the main application thread.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [block](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#block(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Blocks the print job. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#cancel())`()` Cancels the print job. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [complete](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#complete())`()` Completes the print job. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [fail](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#fail(kotlin.String))`(`error:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Fails the print job. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvancedIntOption](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#getAdvancedIntOption(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of an advanced (printer specific) print option. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAdvancedStringOption](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#getAdvancedStringOption(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of an advanced (printer specific) print option. |
| [PrintDocument](https://developer.android.com/reference/kotlin/android/printservice/PrintDocument) | [getDocument](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#getDocument())`()` Gets the printed document. |
| [PrintJobId](https://developer.android.com/reference/kotlin/android/print/PrintJobId.html#)! | [getId](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#getId())`()` Gets the unique print job id. |
| --- | --- |
| [PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo.html#) | [getInfo](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#getInfo())`()` Gets the [PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo.html#) that describes this job. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getTag](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#getTag())`()` Gets the print job tag. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAdvancedOption](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#hasAdvancedOption(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets whether this job has a given advanced (printer specific) print option. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocked](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked())`()` Gets whether this print job is blocked. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isCancelled())`()` Gets whether this print job is cancelled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCompleted](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isCompleted())`()` Gets whether this print job is completed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFailed](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isFailed())`()` Gets whether this print job is failed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isQueued](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued())`()` Gets whether this print job is queued. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted())`()` Gets whether this print job is started. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProgress](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setProgress(kotlin.Float))`(`progress:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the progress of this print job as a fraction of 1. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStatus](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.Int))`(`statusResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the status of this print job as a string resource. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStatus](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.CharSequence))`(`status:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Sets the status of this print job. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setTag](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setTag(kotlin.String))`(`tag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets a tag that is valid in the context of a [PrintService](https://developer.android.com/reference/kotlin/android/printservice/PrintService) and is not interpreted by the system. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [start](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#start())`()` Starts the print job. |
| --- | --- |

## Public methods

### block

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun block(reason: String?): Boolean
```

Blocks the print job. You should call this method if [isStarted()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted())returns true and you need to block the print job. For example, the user has to add some paper to continue printing. To resume the print job call [start()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#start()). To change the reason call [setStatus(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.CharSequence)). 
This method must be called from the main thread of your app.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The human readable, short, and translated reason why the print job is blocked. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the job was blocked. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked()> 

### cancel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Boolean
```

Cancels the print job. You should call this method if [isQueued()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued())or [or #isBlocked()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted())returns true and you canceled the print job as a response to a call to [PrintService.onRequestCancelPrintJob(PrintJob)](https://developer.android.com/reference/kotlin/android/printservice/PrintService#onRequestCancelPrintJob(android.printservice.PrintJob)). 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the job is canceled. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked()> 

### complete

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun complete(): Boolean
```

Completes the print job. You should call this method if [isStarted()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted())returns true and you are done printing. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the job as completed. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted()> 

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

### fail

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun fail(error: String?): Boolean
```

Fails the print job. You should call this method if [isQueued()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued())or [isStarted()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted())or [isBlocked()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked())returns true you failed while printing. 
This method must be called from the main thread of your app.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The human readable, short, and translated reason for the failure. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the job was failed. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isStarted()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked()> 

### getAdvancedIntOption

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvancedIntOption(key: String!): Int
```

Gets the value of an advanced (printer specific) print option. 
This method must be called from the main thread of your app.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The option key. |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The option value. |

### getAdvancedStringOption

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvancedStringOption(key: String!): String!
```

Gets the value of an advanced (printer specific) print option. 
This method must be called from the main thread of your app.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The option key. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The option value. |

### getDocument

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDocument(): PrintDocument
```

Gets the printed document. 
This method must be called from the main thread of your app.

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------|
| [PrintDocument](https://developer.android.com/reference/kotlin/android/printservice/PrintDocument) | The document. This value cannot be`null`. |

### getId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): PrintJobId!
```

Gets the unique print job id. 
This method must be called from the main thread of your app.

| Return ||
|----------------------------------------------------------------------------------------------|---------|
| [PrintJobId](https://developer.android.com/reference/kotlin/android/print/PrintJobId.html#)! | The id. |

### getInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInfo(): PrintJobInfo
```

Gets the [PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo.html#) that describes this job.

**Node:**The returned info object is a snapshot of the current print job state. Every call to this method returns a fresh info object that reflects the current print job state.

This method must be called from the main thread of your app.

| Return ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo.html#) | The print job info. This value cannot be`null`. |

### getTag

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): String?
```

Gets the print job tag. 
This method must be called from the main thread of your app.

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The tag or null. |

**See Also**

- [#setTag(String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setTag(kotlin.String)) 

### hasAdvancedOption

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAdvancedOption(key: String!): Boolean
```

Gets whether this job has a given advanced (printer specific) print option. 
This method must be called from the main thread of your app.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The option key. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the option is present. |

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

Gets whether this print job is blocked. Such a print job is halted due to an abnormal condition and can be started or canceled or failed. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is blocked. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#start()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#cancel()>
- [#fail(String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#fail(kotlin.String)) 

### isCancelled

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCancelled(): Boolean
```

Gets whether this print job is cancelled. Such a print job was cancelled as a result of a user request. This is a final state. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is cancelled. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#cancel()> 

### isCompleted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCompleted(): Boolean
```

Gets whether this print job is completed. Such a print job is successfully printed. This is a final state. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is completed. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#complete()> 

### isFailed

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFailed(): Boolean
```

Gets whether this print job is failed. Such a print job is not successfully printed due to an error. This is a final state. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is failed. |

**See Also**

- [#fail(String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#fail(kotlin.String)) 

### isQueued

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isQueued(): Boolean
```

Gets whether this print job is queued. Such a print job is ready to be printed and can be started or cancelled. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is queued. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#start()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#cancel()> 

### isStarted

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isStarted(): Boolean
```

Gets whether this print job is started. Such a print job is being printed and can be completed or canceled or failed. 
This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the print job is started. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#complete()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#cancel()>
- [#fail(String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#fail(kotlin.String)) 

### setProgress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setProgress(progress: Float): Unit
```

Sets the progress of this print job as a fraction of 1. 
This method must be called from the main thread of your app.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `progress` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The new progress Value is between 0.0f and 1.0f inclusive |

### setStatus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setStatus(statusResId: Int): Unit
```

Sets the status of this print job as a string resource.

<br />

This overrides any previously set status set via [setStatus(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.CharSequence)), [setStatus(int)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.Int)), [block(java.lang.String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#block(kotlin.String)), or [fail(java.lang.String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#fail(kotlin.String)), 
This method must be called from the main thread of your app.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new status as a String resource. If 0 the status will be empty. |

### setStatus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setStatus(status: CharSequence?): Unit
```

Sets the status of this print job. This should be a human readable, short, and translated description of the current state of the print job.

<br />

This overrides any previously set status set via [setStatus(java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.CharSequence)), [setStatus(int)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#setStatus(kotlin.Int)), [block(java.lang.String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#block(kotlin.String)), or [fail(java.lang.String)](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#fail(kotlin.String)), 
This method must be called from the main thread of your app.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The new status. If null the status will be empty. |

### setTag

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTag(tag: String): Boolean
```

Sets a tag that is valid in the context of a [PrintService](https://developer.android.com/reference/kotlin/android/printservice/PrintService) and is not interpreted by the system. For example, a print service may set as a tag the key of the print job returned by a remote print server, if the printing is off handed to a cloud based service. 
This method must be called from the main thread of your app.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The tag. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the tag was set, false otherwise. |

### start

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(): Boolean
```

Starts the print job. You should call this method if [isQueued()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued())or [isBlocked()](https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked())returns true and you started resumed printing.

This resets the print status to null. Set the new status by using #setStatus.

This method must be called from the main thread of your app.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the job was started. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isQueued()>
- <https://developer.android.com/reference/kotlin/android/printservice/PrintJob#isBlocked()>

# PrintJobInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintJobInfo

Kotlin| [Java](https://developer.android.com/reference/android/print/PrintJobInfo "View this page in Java") 

```
class PrintJobInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.print.PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#) |

This class represents the description of a print job. The print job state includes properties such as its id, print attributes used for generating the content, and so on. Note that the print jobs state may change over time and this class represents a snapshot of this state.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo.Builder) Builder for creating a [PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#). |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_BLOCKED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_BLOCKED:kotlin.Int) Print job state: The print job is blocked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int) Print job state: The print job is canceled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_COMPLETED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_COMPLETED:kotlin.Int) Print job state: The print job is successfully printed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CREATED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CREATED:kotlin.Int) Print job state: The print job is being created but not yet ready to be printed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_FAILED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_FAILED:kotlin.Int) Print job state: The print job was printing but printing failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_QUEUED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_QUEUED:kotlin.Int) Print job state: The print jobs is created, it is ready to be printed and should be processed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STARTED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_STARTED:kotlin.Int) Print job state: The print job is being printed. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvancedIntOption](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getAdvancedIntOption(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of an advanced (printer specific) print option. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAdvancedStringOption](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getAdvancedStringOption(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of an advanced (printer specific) print option. |
| [PrintAttributes](https://developer.android.com/reference/kotlin/android/print/PrintAttributes) | [getAttributes](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getAttributes())`()` Gets the print job attributes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCopies](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getCopies())`()` Gets the number of copies. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCreationTime](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getCreationTime())`()` Gets the wall time in millisecond when this print job was created. |
| [PrintJobId](https://developer.android.com/reference/kotlin/android/print/PrintJobId)? | [getId](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getId())`()` Gets the unique print job id. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLabel](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getLabel())`()` Gets the human readable job label. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PageRange](https://developer.android.com/reference/kotlin/android/print/PageRange)!\>? | [getPages](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getPages())`()` Gets the included pages. |
| [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId)? | [getPrinterId](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getPrinterId())`()` Gets the unique target printer id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#getState())`()` Gets the current job state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAdvancedOption](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#hasAdvancedOption(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets whether this job has a given advanced (printer specific) print option. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PrintJobInfo](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### STATE_BLOCKED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_BLOCKED: Int
```

Print job state: The print job is blocked.

Next valid states: [STATE_FAILED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_FAILED:kotlin.Int), [STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int), [STATE_STARTED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_STARTED:kotlin.Int) 

 Value: 4

### STATE_CANCELED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CANCELED: Int
```

Print job state: The print job is canceled. This is a terminal state.

Next valid states: None 

 Value: 7

### STATE_COMPLETED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_COMPLETED: Int
```

Print job state: The print job is successfully printed. This is a terminal state.

Next valid states: None 

 Value: 5

### STATE_CREATED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CREATED: Int
```

Print job state: The print job is being created but not yet ready to be printed.

Next valid states: [STATE_QUEUED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_QUEUED:kotlin.Int) 

 Value: 1

### STATE_FAILED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_FAILED: Int
```

Print job state: The print job was printing but printing failed.

Next valid states: [STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int), [STATE_STARTED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_STARTED:kotlin.Int) 

 Value: 6

### STATE_QUEUED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_QUEUED: Int
```

Print job state: The print jobs is created, it is ready to be printed and should be processed.

Next valid states: [STATE_STARTED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_STARTED:kotlin.Int), [STATE_FAILED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_FAILED:kotlin.Int), [STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int) 

 Value: 2

### STATE_STARTED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STARTED: Int
```

Print job state: The print job is being printed.

Next valid states: [STATE_COMPLETED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_COMPLETED:kotlin.Int), [STATE_FAILED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_FAILED:kotlin.Int), [STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int), [STATE_BLOCKED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_BLOCKED:kotlin.Int) 

 Value: 3

## Public methods

### describeContents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAdvancedIntOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvancedIntOption(key: String!): Int
```

Gets the value of an advanced (printer specific) print option.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The option key. |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The option value. |

### getAdvancedStringOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvancedStringOption(key: String!): String!
```

Gets the value of an advanced (printer specific) print option.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The option key. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The option value. |

### getAttributes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAttributes(): PrintAttributes
```

Gets the print job attributes.

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| [PrintAttributes](https://developer.android.com/reference/kotlin/android/print/PrintAttributes) | The attributes. This value cannot be`null`. |

### getCopies

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCopies(): Int
```

Gets the number of copies.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of copies or zero if not set. Value is 0 or greater |

### getCreationTime

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCreationTime(): Long
```

Gets the wall time in millisecond when this print job was created.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The creation time in milliseconds. |

### getId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): PrintJobId?
```

Gets the unique print job id.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------|
| [PrintJobId](https://developer.android.com/reference/kotlin/android/print/PrintJobId)? | The id. This value may be`null`. |

### getLabel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLabel(): String
```

Gets the human readable job label.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The label. This value cannot be`null`. |

### getPages

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPages(): Array<PageRange!>?
```

Gets the included pages.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PageRange](https://developer.android.com/reference/kotlin/android/print/PageRange)!>? | The included pages or`null`if not set. |

### getPrinterId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrinterId(): PrinterId?
```

Gets the unique target printer id.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------|
| [PrinterId](https://developer.android.com/reference/kotlin/android/print/PrinterId)? | The target printer id. This value may be`null`. |

### getState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Gets the current job state.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The job state. Value is [android.print.PrintJobInfo#STATE_CREATED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CREATED:kotlin.Int), [android.print.PrintJobInfo#STATE_QUEUED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_QUEUED:kotlin.Int), [android.print.PrintJobInfo#STATE_STARTED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_STARTED:kotlin.Int), [android.print.PrintJobInfo#STATE_BLOCKED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_BLOCKED:kotlin.Int), [android.print.PrintJobInfo#STATE_COMPLETED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_COMPLETED:kotlin.Int), [android.print.PrintJobInfo#STATE_FAILED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_FAILED:kotlin.Int), or [android.print.PrintJobInfo#STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int) |

**See Also**

- [#STATE_CREATED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CREATED:kotlin.Int)
- [#STATE_QUEUED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_QUEUED:kotlin.Int)
- [#STATE_STARTED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_STARTED:kotlin.Int)
- [#STATE_COMPLETED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_COMPLETED:kotlin.Int)
- [#STATE_BLOCKED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_BLOCKED:kotlin.Int)
- [#STATE_FAILED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_FAILED:kotlin.Int)
- [#STATE_CANCELED](https://developer.android.com/reference/kotlin/android/print/PrintJobInfo#STATE_CANCELED:kotlin.Int) 

### hasAdvancedOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasAdvancedOption(key: String!): Boolean
```

Gets whether this job has a given advanced (printer specific) print option.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The option key. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the option is present. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PrintJobInfo!>
```

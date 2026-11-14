# PrintJobInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrintJobInfo

Kotlin| [Java](PrintJobInfo.md) 
| --- | --- |

```
class PrintJobInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.print.PrintJobInfo](PrintJobInfo.md) |

This class represents the description of a print job. The print job state includes properties such as its id, print attributes used for generating the content, and so on. Note that the print jobs state may change over time and this class represents a snapshot of this state.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/print/PrintJobInfo.Builder.md) Builder for creating a [PrintJobInfo](PrintJobInfo.md). |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_BLOCKED](PrintJobInfo.md) Print job state: The print job is blocked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CANCELED](PrintJobInfo.md) Print job state: The print job is canceled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_COMPLETED](PrintJobInfo.md) Print job state: The print job is successfully printed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CREATED](PrintJobInfo.md) Print job state: The print job is being created but not yet ready to be printed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_FAILED](PrintJobInfo.md) Print job state: The print job was printing but printing failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_QUEUED](PrintJobInfo.md) Print job state: The print jobs is created, it is ready to be printed and should be processed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STARTED](PrintJobInfo.md) Print job state: The print job is being printed. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](PrintJobInfo.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvancedIntOption](PrintJobInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of an advanced (printer specific) print option. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAdvancedStringOption](PrintJobInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of an advanced (printer specific) print option. |
| --- | --- |
| [PrintAttributes](PrintAttributes.md) | [getAttributes](PrintJobInfo.md))`()` Gets the print job attributes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCopies](PrintJobInfo.md))`()` Gets the number of copies. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCreationTime](PrintJobInfo.md))`()` Gets the wall time in millisecond when this print job was created. |
| --- | --- |
| [PrintJobId](PrintJobId.md)? | [getId](PrintJobInfo.md))`()` Gets the unique print job id. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLabel](PrintJobInfo.md))`()` Gets the human readable job label. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [PageRange](PageRange.md)!\>? | [getPages](PrintJobInfo.md))`()` Gets the included pages. |
| --- | --- |
| [PrinterId](PrinterId.md)? | [getPrinterId](PrintJobInfo.md))`()` Gets the unique target printer id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](PrintJobInfo.md))`()` Gets the current job state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasAdvancedOption](PrintJobInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets whether this job has a given advanced (printer specific) print option. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PrintJobInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PrintJobInfo.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PrintJobInfo](PrintJobInfo.md)!\> | [CREATOR](PrintJobInfo.md) <br /> |

## Constants

### STATE_BLOCKED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_BLOCKED: Int
```

Print job state: The print job is blocked.

Next valid states: [STATE_FAILED](PrintJobInfo.md), [STATE_CANCELED](PrintJobInfo.md), [STATE_STARTED](PrintJobInfo.md) 

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

Next valid states: [STATE_QUEUED](PrintJobInfo.md) 

 Value: 1

### STATE_FAILED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_FAILED: Int
```

Print job state: The print job was printing but printing failed.

Next valid states: [STATE_CANCELED](PrintJobInfo.md), [STATE_STARTED](PrintJobInfo.md) 

 Value: 6

### STATE_QUEUED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_QUEUED: Int
```

Print job state: The print jobs is created, it is ready to be printed and should be processed.

Next valid states: [STATE_STARTED](PrintJobInfo.md), [STATE_FAILED](PrintJobInfo.md), [STATE_CANCELED](PrintJobInfo.md) 

 Value: 2

### STATE_STARTED

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STARTED: Int
```

Print job state: The print job is being printed.

Next valid states: [STATE_COMPLETED](PrintJobInfo.md), [STATE_FAILED](PrintJobInfo.md), [STATE_CANCELED](PrintJobInfo.md), [STATE_BLOCKED](PrintJobInfo.md) 

 Value: 3

## Public methods

### describeContents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [PrintAttributes](PrintAttributes.md) | The attributes. This value cannot be`null`. |

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
| [PrintJobId](PrintJobId.md)? | The id. This value may be`null`. |

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
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PageRange](PageRange.md)!>? | The included pages or`null`if not set. |

### getPrinterId

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrinterId(): PrinterId?
```

Gets the unique target printer id.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------|
| [PrinterId](PrinterId.md)? | The target printer id. This value may be`null`. |

### getState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Gets the current job state.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The job state. Value is [android.print.PrintJobInfo#STATE_CREATED](PrintJobInfo.md), [android.print.PrintJobInfo#STATE_QUEUED](PrintJobInfo.md), [android.print.PrintJobInfo#STATE_STARTED](PrintJobInfo.md), [android.print.PrintJobInfo#STATE_BLOCKED](PrintJobInfo.md), [android.print.PrintJobInfo#STATE_COMPLETED](PrintJobInfo.md), [android.print.PrintJobInfo#STATE_FAILED](PrintJobInfo.md), or [android.print.PrintJobInfo#STATE_CANCELED](PrintJobInfo.md) |

**See Also**

- [#STATE_CREATED](PrintJobInfo.md)
- [#STATE_QUEUED](PrintJobInfo.md)
- [#STATE_STARTED](PrintJobInfo.md)
- [#STATE_COMPLETED](PrintJobInfo.md)
- [#STATE_BLOCKED](PrintJobInfo.md)
- [#STATE_FAILED](PrintJobInfo.md)
- [#STATE_CANCELED](PrintJobInfo.md) 

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PrintJobInfo!>
```

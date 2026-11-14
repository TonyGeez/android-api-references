# ResultReceiver

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResultReceiver

Kotlin| [Java](https://developer.android.com/reference/android/os/ResultReceiver "View this page in Java") 
| --- | --- |

```
open class ResultReceiver : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#) |

Generic interface for receiving a callback result from someone. Use this by creating a subclass and implement [onReceiveResult](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#onReceiveResult(kotlin.Int,%20android.os.Bundle)), which you can then pass to others and send through IPC, and receive results they supply with [send](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#send(kotlin.Int,%20android.os.Bundle)).

Note: the implementation underneath is just a simple wrapper around a [Binder](https://developer.android.com/reference/kotlin/android/os/Binder) that is used to perform the communication. This means semantically you should treat it as such: this class does not impact process lifecycle management (you must be using some higher-level component to tell the system that your process needs to continue running), the connection will break if your process goes away for any reason, etc.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#ResultReceiver(android.os.Handler))`(`handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler)!`)` Create a new ResultReceive to receive results. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#describeContents())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#send(kotlin.Int,%20android.os.Bundle))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)!`)` Deliver a result to this receiver. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceiveResult](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#onReceiveResult(kotlin.Int,%20android.os.Bundle))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)!`)` Override to receive results delivered to this object. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator)\< [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### ResultReceiver

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResultReceiver(handler: Handler!)
```

Create a new ResultReceive to receive results. Your [onReceiveResult](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#onReceiveResult(kotlin.Int,%20android.os.Bundle))method will be called from the thread running handler if given, or from an arbitrary thread if null.

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### send

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun send(
    resultCode: Int, 
    resultData: Bundle!
): Unit
```

Deliver a result to this receiver. Will call [onReceiveResult](https://developer.android.com/reference/kotlin/android/os/ResultReceiver#onReceiveResult(kotlin.Int,%20android.os.Bundle)), always asynchronously if the receiver has supplied a Handler in which to dispatch the result.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Arbitrary result code to deliver, as defined by you. |
| `resultData` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)!:Any additional data provided by you. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Protected methods

### onReceiveResult

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onReceiveResult(
    resultCode: Int, 
    resultData: Bundle!
): Unit
```

Override to receive results delivered to this object.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Arbitrary result code delivered by the sender, as defined by the sender. |
| `resultData` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle)!:Any additional data provided by the sender. |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ResultReceiver!>
```

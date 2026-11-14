# CallException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallException

Kotlin| [Java](../android/telecom/CallException.md) 
| --- | --- |

```
class CallException : RuntimeException, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.telecom.CallException](../android/telecom/CallException.md) |

This class defines exceptions that can be thrown when using Telecom APIs with [android.os.OutcomeReceiver](../android/os/OutcomeReceiver.md) s. Most of these exceptions are thrown when changing a call state with [CallControl](../android/telecom/CallControl.md) s or [CallControlCallback](../android/telecom/CallControlCallback.md) s.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_CALL_CANNOT_BE_SET_TO_ACTIVE](../android/telecom/CallException.md) The operation has failed because Telecom cannot set the requested call as the current active call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_CALL_IS_NOT_BEING_TRACKED](../android/telecom/CallException.md) The operation has failed because Telecom has already removed the call from the server side and destroyed all the objects associated with it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_CALL_NOT_PERMITTED_AT_PRESENT_TIME](../android/telecom/CallException.md) The operation has failed because there is either no PhoneAccount registered with Telecom for the given operation, or the limit of calls has been reached. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_CANNOT_HOLD_CURRENT_ACTIVE_CALL](../android/telecom/CallException.md) The operation has failed due to Telecom failing to hold the current active call for the call attempting to become the new active call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_ERROR_UNKNOWN](../android/telecom/CallException.md) The operation has failed due to an unknown or unspecified error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CODE_OPERATION_TIMED_OUT](../android/telecom/CallException.md) The operation has failed because the operation failed to complete before the timeout |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CallException](../android/telecom/CallException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor for a new CallException that has a defined error code in this class |

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telecom/CallException.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCode](../android/telecom/CallException.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telecom/CallException.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CallException](../android/telecom/CallException.md)!\> | [CREATOR](../android/telecom/CallException.md) Responsible for creating CallAttribute objects for deserialized Parcels. |

## Constants

### CODE_CALL_CANNOT_BE_SET_TO_ACTIVE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_CALL_CANNOT_BE_SET_TO_ACTIVE: Int
```

The operation has failed because Telecom cannot set the requested call as the current active call. The client should end the current active call and re-try the operation. 

 Value: 4

### CODE_CALL_IS_NOT_BEING_TRACKED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_CALL_IS_NOT_BEING_TRACKED: Int
```

The operation has failed because Telecom has already removed the call from the server side and destroyed all the objects associated with it. The client should re-add the call. 

 Value: 3

### CODE_CALL_NOT_PERMITTED_AT_PRESENT_TIME

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_CALL_NOT_PERMITTED_AT_PRESENT_TIME: Int
```

The operation has failed because there is either no PhoneAccount registered with Telecom for the given operation, or the limit of calls has been reached. The client should end the current active call and re-try the failed operation. 

 Value: 5

### CODE_CANNOT_HOLD_CURRENT_ACTIVE_CALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_CANNOT_HOLD_CURRENT_ACTIVE_CALL: Int
```

The operation has failed due to Telecom failing to hold the current active call for the call attempting to become the new active call. The client should end the current active call and re-try the failed operation. 

 Value: 2

### CODE_ERROR_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_ERROR_UNKNOWN: Int
```

The operation has failed due to an unknown or unspecified error. 

 Value: 1

### CODE_OPERATION_TIMED_OUT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CODE_OPERATION_TIMED_OUT: Int
```

The operation has failed because the operation failed to complete before the timeout 

 Value: 6

## Public constructors

### CallException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CallException(
    message: String?, 
    code: Int)
```

Constructor for a new CallException that has a defined error code in this class

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:related to why the exception was created This value may be`null`. |
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):defined above that caused this exception to be created Value is [android.telecom.CallException#CODE_ERROR_UNKNOWN](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CANNOT_HOLD_CURRENT_ACTIVE_CALL](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CALL_IS_NOT_BEING_TRACKED](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CALL_CANNOT_BE_SET_TO_ACTIVE](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CALL_NOT_PERMITTED_AT_PRESENT_TIME](../android/telecom/CallException.md), or [android.telecom.CallException#CODE_OPERATION_TIMED_OUT](../android/telecom/CallException.md) |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of the error codes defined in this class that was passed into the constructor Value is [android.telecom.CallException#CODE_ERROR_UNKNOWN](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CANNOT_HOLD_CURRENT_ACTIVE_CALL](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CALL_IS_NOT_BEING_TRACKED](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CALL_CANNOT_BE_SET_TO_ACTIVE](../android/telecom/CallException.md), [android.telecom.CallException#CODE_CALL_NOT_PERMITTED_AT_PRESENT_TIME](../android/telecom/CallException.md), or [android.telecom.CallException#CODE_OPERATION_TIMED_OUT](../android/telecom/CallException.md) |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CallException!>
```

Responsible for creating CallAttribute objects for deserialized Parcels.

# CallAttributes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallAttributes

Kotlin| [Java](https://developer.android.com/reference/android/telecom/CallAttributes "View this page in Java") 
| --- | --- |

```
class CallAttributes : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.CallAttributes](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#) |

CallAttributes represents a set of properties that define a new Call. Apps should build an instance of this class and use [TelecomManager.addCall](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#addCall(android.telecom.CallAttributes,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver,%20android.telecom.CallControlCallback,%20android.telecom.CallEventCallback))to start a new call with Telecom.

Apps should first register a [PhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount) via [TelecomManager.registerPhoneAccount](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager#registerPhoneAccount(android.telecom.PhoneAccount))and use the same [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) registered with Telecom when creating an instance of CallAttributes.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes.Builder) Build an instance of [CallAttributes](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#). |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AUDIO_CALL](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#AUDIO_CALL:kotlin.Int) Used when answering or dialing a call to indicate that the call does not have a video component |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_INCOMING](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#DIRECTION_INCOMING:kotlin.Int) Indicates that the call is an incoming call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_OUTGOING](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#DIRECTION_OUTGOING:kotlin.Int) Indicates that the call is an outgoing call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTS_SET_INACTIVE](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_SET_INACTIVE:kotlin.Int) The call being created can be set to inactive (traditionally referred to as hold). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTS_STREAM](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_STREAM:kotlin.Int) The call can be streamed from a root device to another device to continue the call without completely transferring it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTS_TRANSFER](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_TRANSFER:kotlin.Int) The call can be completely transferred from one endpoint to another. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTS_VIDEO_CALLING](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_VIDEO_CALLING:kotlin.Int) The call supports video calling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIDEO_CALL](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#VIDEO_CALL:kotlin.Int) Indicates video transmission is supported |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getAddress](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#getAddress())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallCapabilities](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#getCallCapabilities())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallType](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#getCallType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirection](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#getDirection())`()` <br /> |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [getDisplayName](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#getDisplayName())`()` <br /> |
| [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) | [getPhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#getPhoneAccountHandle())`()` The [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) that should be registered to Telecom to allow calls. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#hashCode())`()` Returns a hash code value for the object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLogExcluded](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#isLogExcluded())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CallAttributes](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#CREATOR:android.os.Parcelable.Creator) Responsible for creating CallAttribute objects for deserialized Parcels. |

## Constants

### AUDIO_CALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUDIO_CALL: Int
```

Used when answering or dialing a call to indicate that the call does not have a video component 

 Value: 1

### DIRECTION_INCOMING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_INCOMING: Int
```

Indicates that the call is an incoming call. 

 Value: 1

### DIRECTION_OUTGOING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_OUTGOING: Int
```

Indicates that the call is an outgoing call. 

 Value: 2

### SUPPORTS_SET_INACTIVE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPORTS_SET_INACTIVE: Int
```

The call being created can be set to inactive (traditionally referred to as hold). This means that once a new call goes active, if the active call needs to be held in order to place or receive an incoming call, the active call will be placed on hold. otherwise, the active call may be disconnected. 

 Value: 2

### SUPPORTS_STREAM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPORTS_STREAM: Int
```

The call can be streamed from a root device to another device to continue the call without completely transferring it. 

 Value: 4

### SUPPORTS_TRANSFER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPORTS_TRANSFER: Int
```

The call can be completely transferred from one endpoint to another. 

 Value: 8

### SUPPORTS_VIDEO_CALLING

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPORTS_VIDEO_CALLING: Int
```

The call supports video calling. This allows clients to gate video calling on a per call basis as opposed to re-registering the phone account. 

 Value: 16

### VIDEO_CALL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIDEO_CALL: Int
```

Indicates video transmission is supported 

 Value: 2

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAddress

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddress(): Uri
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | address of the incoming caller or the address of the person being called for an outgoing call This value cannot be`null`. |

### getCallCapabilities

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallCapabilities(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The allowed capabilities of the new call Value is either`0`or a combination of [android.telecom.CallAttributes#SUPPORTS_SET_INACTIVE](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_SET_INACTIVE:kotlin.Int), [android.telecom.CallAttributes#SUPPORTS_STREAM](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_STREAM:kotlin.Int), [android.telecom.CallAttributes#SUPPORTS_TRANSFER](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_TRANSFER:kotlin.Int), and [android.telecom.CallAttributes#SUPPORTS_VIDEO_CALLING](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#SUPPORTS_VIDEO_CALLING:kotlin.Int) |

### getCallType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallType(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Information related to data being transmitted (voice, video, etc. ) Value is [android.telecom.CallAttributes#AUDIO_CALL](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#AUDIO_CALL:kotlin.Int), or [android.telecom.CallAttributes#VIDEO_CALL](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#VIDEO_CALL:kotlin.Int) |

### getDirection

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDirection(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the direction of the new call. Value is [android.telecom.CallAttributes#DIRECTION_INCOMING](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#DIRECTION_INCOMING:kotlin.Int), or [android.telecom.CallAttributes#DIRECTION_OUTGOING](https://developer.android.com/reference/kotlin/android/telecom/CallAttributes#DIRECTION_OUTGOING:kotlin.Int) |

### getDisplayName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(): CharSequence
```

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | display name of the incoming caller or the person being called for an outgoing call This value cannot be`null`. |

### getPhoneAccountHandle

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhoneAccountHandle(): PhoneAccountHandle
```

The [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) that should be registered to Telecom to allow calls. The [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) should be registered before creating a CallAttributes instance.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) | the [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle) for this package that allows this call to be created This value cannot be`null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isLogExcluded

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLogExcluded(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the call is excluded from system call logs |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel!, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!:This value may be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CallAttributes!>
```

Responsible for creating CallAttribute objects for deserialized Parcels.

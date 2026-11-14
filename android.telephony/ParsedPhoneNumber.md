# ParsedPhoneNumber

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParsedPhoneNumber

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ParsedPhoneNumber "View this page in Java") 
| --- | --- |

```
class ParsedPhoneNumber : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ParsedPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#) |

Handles the results from PhoneNumberManager by providing Phone number, error code, and is valid number.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER:kotlin.Int) The phone number failed to be validated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_NONE:kotlin.Int) No error seen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_NUMBER_PARSE_EXCEPTION](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_NUMBER_PARSE_EXCEPTION:kotlin.Int) There was an error when trying to extract the phone number. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_UNKNOWN:kotlin.Int) Failed to extract phone number for unknown reason. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ParsedPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ParsedPhoneNumber(kotlin.String,%20kotlin.Int,%20kotlin.Boolean))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isValidPhoneNumber:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#getErrorCode())`()` If no phone number was able to be extracted this will report the failure reason to the user. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getParsedPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#getParsedPhoneNumber())`()` Parsed phone number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#isValidPhoneNumber())`()` Whether or not we were able to extract a valid phone number |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ParsedPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER: Int
```

The phone number failed to be validated. 

 Value: 1

### ERROR_TYPE_NONE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_NONE: Int
```

No error seen. 

 Value: 0

### ERROR_TYPE_NUMBER_PARSE_EXCEPTION

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_NUMBER_PARSE_EXCEPTION: Int
```

There was an error when trying to extract the phone number. 

 Value: 2

### ERROR_TYPE_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_TYPE_UNKNOWN: Int
```

Failed to extract phone number for unknown reason. 

 Value: -1

## Public constructors

### ParsedPhoneNumber

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ParsedPhoneNumber(
    phoneNumber: String, 
    errorCode: Int, 
    isValidPhoneNumber: Boolean)
```

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the phone number extracted. Empty if we weren't successful in parsing. This value cannot be`null`. |
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):ErrorType seen when trying to extract phone number. Value is [android.telephony.ParsedPhoneNumber#ERROR_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_UNKNOWN:kotlin.Int), [android.telephony.ParsedPhoneNumber#ERROR_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_NONE:kotlin.Int), [android.telephony.ParsedPhoneNumber#ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER:kotlin.Int), or [android.telephony.ParsedPhoneNumber#ERROR_TYPE_NUMBER_PARSE_EXCEPTION](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_NUMBER_PARSE_EXCEPTION:kotlin.Int) |
| `isValidPhoneNumber` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not we succeeded in retrieving the number. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getErrorCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorCode(): Int
```

If no phone number was able to be extracted this will report the failure reason to the user.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.ParsedPhoneNumber#ERROR_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_UNKNOWN:kotlin.Int), [android.telephony.ParsedPhoneNumber#ERROR_TYPE_NONE](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_NONE:kotlin.Int), [android.telephony.ParsedPhoneNumber#ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_FAILED_TO_VALIDATE_EXTRACTED_PHONE_NUMER:kotlin.Int), or [android.telephony.ParsedPhoneNumber#ERROR_TYPE_NUMBER_PARSE_EXCEPTION](https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber#ERROR_TYPE_NUMBER_PARSE_EXCEPTION:kotlin.Int) |

### getParsedPhoneNumber

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParsedPhoneNumber(): String
```

Parsed phone number.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------|
| `java.lang.IllegalStateException` | if isValidPhoneNumber is false. |

### hashCode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isValidPhoneNumber

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isValidPhoneNumber(): Boolean
```

Whether or not we were able to extract a valid phone number 

### toString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ParsedPhoneNumber!>
```

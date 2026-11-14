# AppSearchResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppSearchResult

Kotlin| [Java](AppSearchResult.md) 
| --- | --- |

```
class AppSearchResult<ValueType : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.AppSearchResult](AppSearchResult.md) |

Information about the success or failure of an AppSearch call.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_ALREADY_EXISTS](AppSearchResult.md) The operation is invalid because the resource already exists and can't be replaced. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_DENIED](AppSearchResult.md) The requested operation is denied for the caller. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_INTERNAL_ERROR](AppSearchResult.md) An internal error occurred within AppSearch, which the caller cannot address. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_INVALID_ARGUMENT](AppSearchResult.md) The caller supplied invalid arguments to the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_INVALID_SCHEMA](AppSearchResult.md) The caller supplied a schema which is invalid or incompatible with the previous schema. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_IO_ERROR](AppSearchResult.md) An issue occurred reading or writing to storage. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_NOT_FOUND](AppSearchResult.md) An entity the caller requested to interact with does not exist in the system. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_OK](AppSearchResult.md) The call was successful. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_OUT_OF_SPACE](AppSearchResult.md) Storage is out of space, and no more space could be reclaimed. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_RATE_LIMITED](AppSearchResult.md) The caller has hit AppSearch's rate limit and the requested operation has been rejected. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_SECURITY_ERROR](AppSearchResult.md) The caller requested an operation it does not have privileges for. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESULT_UNKNOWN_ERROR](AppSearchResult.md) An unknown error occurred while processing the call. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AppSearchResult.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getErrorMessage](AppSearchResult.md))`()` Returns the error message associated with this result. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](AppSearchResult.md))`()` Returns one of the`RESULT`constants defined in [AppSearchResult](AppSearchResult.md). |
| --- | --- |
| ValueType? | [getResultValue](AppSearchResult.md))`()` Returns the result value associated with this result, if it was successful. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AppSearchResult.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSuccess](AppSearchResult.md))`()` Returns`true`if [getResultCode](AppSearchResult.md))equals [AppSearchResult.RESULT_OK](AppSearchResult.md). |
| --- | --- |
| static [AppSearchResult](AppSearchResult.md)\<ValueType\> | [newFailedResult](AppSearchResult.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Creates a new failed [AppSearchResult](AppSearchResult.md). |
| static [AppSearchResult](AppSearchResult.md)\<ValueType\> | [newSuccessfulResult](AppSearchResult.md))`(`value:` `ValueType?`)` Creates a new successful [AppSearchResult](AppSearchResult.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AppSearchResult.md))`()` Returns a string representation of the object. |
| --- | --- |

## Constants

### RESULT_ALREADY_EXISTS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
static val RESULT_ALREADY_EXISTS: Int
```

The operation is invalid because the resource already exists and can't be replaced. 

 Value: 12

### RESULT_DENIED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
static val RESULT_DENIED: Int
```

The requested operation is denied for the caller. This error is logged and returned for denylist rejections. 

 Value: 9

### RESULT_INTERNAL_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_INTERNAL_ERROR: Int
```

An internal error occurred within AppSearch, which the caller cannot address.

This error may be considered similar to [IllegalStateException](../java.lang/IllegalStateException.md) 

 Value: 2

### RESULT_INVALID_ARGUMENT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_INVALID_ARGUMENT: Int
```

The caller supplied invalid arguments to the call.

This error may be considered similar to [IllegalArgumentException](../java.lang/IllegalArgumentException.md). 

 Value: 3

### RESULT_INVALID_SCHEMA

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_INVALID_SCHEMA: Int
```

The caller supplied a schema which is invalid or incompatible with the previous schema. 

 Value: 7

### RESULT_IO_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_IO_ERROR: Int
```

An issue occurred reading or writing to storage. The call might succeed if repeated.

This error may be considered similar to [java.io.IOException](../java.io/IOException.md). 

 Value: 4

### RESULT_NOT_FOUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_NOT_FOUND: Int
```

An entity the caller requested to interact with does not exist in the system. 

 Value: 6

### RESULT_OK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_OK: Int
```

The call was successful. 

 Value: 0

### RESULT_OUT_OF_SPACE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_OUT_OF_SPACE: Int
```

Storage is out of space, and no more space could be reclaimed. 

 Value: 5

### RESULT_RATE_LIMITED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
static val RESULT_RATE_LIMITED: Int
```

The caller has hit AppSearch's rate limit and the requested operation has been rejected. The caller is recommended to reschedule tasks with exponential backoff. 

 Value: 10

### RESULT_SECURITY_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_SECURITY_ERROR: Int
```

The caller requested an operation it does not have privileges for. 

 Value: 8

### RESULT_UNKNOWN_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESULT_UNKNOWN_ERROR: Int
```

An unknown error occurred while processing the call. 

 Value: 1

## Public methods

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|---------|------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getErrorMessage

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorMessage(): String?
```

Returns the error message associated with this result.

If [isSuccess](AppSearchResult.md))is`true`, the error message is always`null`. The error message may be`null`even if [isSuccess](AppSearchResult.md))is`false`. See the documentation of the particular [AppSearchSession](AppSearchSession.md) call producing this [AppSearchResult](AppSearchResult.md) for what is returned by [getErrorMessage](AppSearchResult.md)). 

### getResultCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultCode(): Int
```

Returns one of the`RESULT`constants defined in [AppSearchResult](AppSearchResult.md).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.app.appsearch.AppSearchResult#RESULT_OK](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_UNKNOWN_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INTERNAL_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_ARGUMENT](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_IO_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_OUT_OF_SPACE](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_NOT_FOUND](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_SCHEMA](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_SECURITY_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_DENIED](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_RATE_LIMITED](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_ALREADY_EXISTS](AppSearchResult.md), android.app.appsearch.AppSearchResult.RESULT_ABORTED, or android.app.appsearch.AppSearchResult.RESULT_UNAVAILABLE |

### getResultValue

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultValue(): ValueType?
```

Returns the result value associated with this result, if it was successful.

See the documentation of the particular [AppSearchSession](AppSearchSession.md) call producing this [AppSearchResult](AppSearchResult.md) for what is placed in the result value by that call.

| Return ||
|------------|--------------------------|
| ValueType? | This value may be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this [AppSearchResult](AppSearchResult.md) is not successful. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isSuccess

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSuccess(): Boolean
```

Returns`true`if [getResultCode](AppSearchResult.md))equals [AppSearchResult.RESULT_OK](AppSearchResult.md). 

### newFailedResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <ValueType : Any!> newFailedResult(
    resultCode: Int, 
    errorMessage: String?
): AppSearchResult<ValueType>
```

Creates a new failed [AppSearchResult](AppSearchResult.md).

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the constants documented in [AppSearchResult.getResultCode](AppSearchResult.md)). Value is [android.app.appsearch.AppSearchResult#RESULT_OK](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_UNKNOWN_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INTERNAL_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_ARGUMENT](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_IO_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_OUT_OF_SPACE](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_NOT_FOUND](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_INVALID_SCHEMA](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_SECURITY_ERROR](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_DENIED](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_RATE_LIMITED](AppSearchResult.md), [android.app.appsearch.AppSearchResult#RESULT_ALREADY_EXISTS](AppSearchResult.md), android.app.appsearch.AppSearchResult.RESULT_ABORTED, or android.app.appsearch.AppSearchResult.RESULT_UNAVAILABLE |
| `errorMessage` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:An optional string describing the reason or nature of the failure. This value may be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [AppSearchResult](AppSearchResult.md)<ValueType> | This value cannot be`null`. |

### newSuccessfulResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <ValueType : Any!> newSuccessfulResult(value: ValueType?): AppSearchResult<ValueType>
```

Creates a new successful [AppSearchResult](AppSearchResult.md).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------|
| `value` | ValueType?:An optional value to associate with the successful result of the operation being performed. This value may be`null`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [AppSearchResult](AppSearchResult.md)<ValueType> | This value cannot be`null`. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

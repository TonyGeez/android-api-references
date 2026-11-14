Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteAppFunctionResponse

```
class ExecuteAppFunctionResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appfunctions.ExecuteAppFunctionResponse](../android/app/appfunctions/ExecuteAppFunctionResponse.md) |

The response to an app function execution, returned by android.app.appfunctions.AppFunctionManager#executeAppFunction.

Use `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata` to determine the expected structure of the response.

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#PROPERTY_RETURN_VALUE:kotlin.String` The name of the property that stores the function return value within the `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()`. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#ExecuteAppFunctionResponse(android.app.appsearch.GenericDocument)(resultDocument: https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#)` Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#`. |
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#ExecuteAppFunctionResponse(android.app.appsearch.GenericDocument,%20android.os.Bundle)(resultDocument: https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#` with an additional `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`. |
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#ExecuteAppFunctionResponse(android.app.appsearch.GenericDocument,%20android.os.Bundle,%20kotlin.collections.MutableList)(resultDocument: https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, uriGrants: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant!>)` Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#` with an additional `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` and `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant`s. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Bundle](../android/os/Bundle.md) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getExtras()()` Returns the additional metadata for this function execution response. |
| [GenericDocument](../android/app/appsearch/GenericDocument.md) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()()` Returns a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` containing the return value of the executed function. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppFunctionUriGrant](../android/app/appfunctions/AppFunctionUriGrant.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getUriGrants()()` The list of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant` to which the caller of this app function execution should have temporary access granted. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ExecuteAppFunctionResponse](../android/app/appfunctions/ExecuteAppFunctionResponse.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### PROPERTY_RETURN_VALUE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_RETURN_VALUE: String
```

The name of the property that stores the function return value within the `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()`.

If the function returns `void` or throws an error, this property will not be set.

 Value: "androidAppfunctionsReturnValue"

## Public constructors

### ExecuteAppFunctionResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ExecuteAppFunctionResponse(resultDocument: GenericDocument)
```

Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#`.

| Parameters ||
|---|---|
| `resultDocument` | [GenericDocument](../android/app/appsearch/GenericDocument.md): The return value of the executed function, see `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()`. This value cannot be `null`. |

### ExecuteAppFunctionResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ExecuteAppFunctionResponse(
    resultDocument: GenericDocument, 
    extras: Bundle)
```

Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#` with an additional `https://developer.android.com/reference/kotlin/android/os/Bundle.html#`.

| Parameters ||
|---|---|
| `resultDocument` | [GenericDocument](../android/app/appsearch/GenericDocument.md): The return value of the executed function, see `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()`. This value cannot be `null`. |
| `extras` | [Bundle](../android/os/Bundle.md): The additional metadata for this function execution response, see `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getExtras()`. This value cannot be `null`. |

### ExecuteAppFunctionResponse

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ExecuteAppFunctionResponse(
    resultDocument: GenericDocument, 
    extras: Bundle, 
    uriGrants: MutableList<AppFunctionUriGrant!>)
```

Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#` with an additional `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` and `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant`s.

| Parameters ||
|---|---|
| `resultDocument` | [GenericDocument](../android/app/appsearch/GenericDocument.md): The return value of the executed function, see `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()`. This value cannot be `null`. |
| `extras` | [Bundle](../android/os/Bundle.md): The additional metadata for this function execution response, see `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getExtras()`. This value cannot be `null`. |
| `uriGrants` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppFunctionUriGrant](../android/app/appfunctions/AppFunctionUriGrant.md)!\>: The list of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant` to which the caller of this app function execution should have temporary access granted. This value cannot be `null`. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getExtras

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns the additional metadata for this function execution response.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### getResultDocument

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultDocument(): GenericDocument
```

Returns a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` containing the return value of the executed function.

The `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#PROPERTY_RETURN_VALUE:kotlin.String` key can be used to obtain the return value.

Example of extracting the return value:

```kotlin
<code>GenericDocument resultDocument = response.getResultDocument();
  Object returnValue = resultDocument.getProperty(PROPERTY_RETURN_VALUE);
  if (returnValue != null) {
    // Cast returnValue to expected type, or use GenericDocument#getPropertyString,
    // GenericDocument#getPropertyLong, etc.
  }
  </code>
```

Use `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata` to determine the expected structure of this document.

### getUriGrants

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUriGrants(): MutableList<AppFunctionUriGrant!>
```

The list of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant` to which the caller of this app function execution should have temporary access granted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant!>` | This value cannot be `null`. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ExecuteAppFunctionResponse!>
```

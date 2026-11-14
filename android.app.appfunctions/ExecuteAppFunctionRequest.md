Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteAppFunctionRequest

```
class ExecuteAppFunctionRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appfunctions.ExecuteAppFunctionRequest](https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#) |

A request to execute an app function, provided to android.app.appfunctions.AppFunctionManager#executeAppFunction.

Use `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata` to construct a `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#` that correctly targets an app function.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#`. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [AppFunctionActivityId](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionActivityId)? | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getActivityId()()` Returns the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionActivityId` for this request. |
| [AppInteractionAttribution](https://developer.android.com/reference/kotlin/android/app/AppInteractionAttribution.html#)? | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getAttribution()()` Returns the `https://developer.android.com/reference/kotlin/android/app/AppInteractionAttribution.html#` for the `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#`. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getExtras()()` Returns the additional values for this function execution request. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getFunctionIdentifier()()` Returns the unique identifier of the app function to be executed. |
| [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getParameters()()` Returns the function parameters as a key-value `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#getTargetPackageName()()` Returns the package name of the app that hosts the app function. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ExecuteAppFunctionRequest](https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#)!\> | `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#CREATOR:android.os.Parcelable.Creator` <br /> |

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

### getActivityId

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActivityId(): AppFunctionActivityId?
```

Returns the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionActivityId` for this request.

This identifier is used to disambiguate between instances of the same app function running in different activities when the function's `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getScope()` is `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int`.

If this returns `null`, the request targets an app function that is not `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int`.

### getAttribution

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAttribution(): AppInteractionAttribution?
```

Returns the `https://developer.android.com/reference/kotlin/android/app/AppInteractionAttribution.html#` for the `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest#`.

This information can be used by the privacy setting to provide transparency to the user about why an app function was invoked.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/AppInteractionAttribution.html#?` | This value may be `null`. |

### getExtras

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns the additional values for this function execution request.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### getFunctionIdentifier

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFunctionIdentifier(): String
```

Returns the unique identifier of the app function to be executed.

See `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getName()` for how to determine this value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getParameters

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParameters(): GenericDocument
```

Returns the function parameters as a key-value `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#`.

The `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` may have missing parameters. Developers are advised to implement defensive handling measures.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` | This value cannot be `null`. |

### getTargetPackageName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTargetPackageName(): String
```

Returns the package name of the app that hosts the app function.

See `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getName()` for how to determine this value.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ExecuteAppFunctionRequest!>
```

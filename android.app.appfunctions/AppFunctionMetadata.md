Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionMetadata

```
class AppFunctionMetadata : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appfunctions.AppFunctionMetadata](AppFunctionMetadata.md) |

Contains an app function's metadata, essential for its invocation and discovery, retrieved using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#searchAppFunctions(android.app.appfunctions.AppFunctionSearchSpec,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

This metadata is defined in an XML asset file and does not change at runtime. The XML file is referenced from the app's `AndroidManifest.xml`. How it's referenced depends on whether the app function is implemented using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionService` or `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`.

The XML schema consists of a root `<appfunctions>` element that can contain one or more `<appfunction>` elements. The XML tags used within the `<appfunction>` element directly correspond to the property names defined by the `PROPERTY_*` constants in this class. All properties in the XML (including unknown properties) are made available through the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getMetadataDocument()` method.

**Example `assets/app_functions.xml` declaration:**

```kotlin
<code>&lt;appfunctions&gt;
      &lt;appfunction&gt;
          &lt;id&gt;createNote&lt;/id&gt;
          &lt;enabledByDefault&gt;true&lt;/enabledByDefault&gt;
          &lt;scope&gt;global&lt;/scope&gt;
          ...
      &lt;/appfunction&gt;
  &lt;/appfunctions&gt;
  </code>
```

See `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionStates(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` for details on retrieving the runtime state of the app functions.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_ANDROID_TRUSTED:kotlin.Int` A constant indicating that the app function is accessible by any caller certified by Android that holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` permission. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SELF:kotlin.Int` A constant indicating that the app function is strictly restricted to the app itself. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SYSTEM:kotlin.Int` A constant indicating that the app function is accessible by holders of the android. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_ACCESS_LEVEL:kotlin.String` Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getAccessLevel()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_ENABLED_BY_DEFAULT:kotlin.String` Property name for the XML tag that defines the default value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState#isEnabled()`, before calling `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#setAppFunctionEnabled(kotlin.String,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_FUNCTION_ID:kotlin.String` Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName#getFunctionIdentifier()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getName()`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCHEMA_CATEGORY:kotlin.String` Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata#getCategory()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCHEMA_NAME:kotlin.String` Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata#getName()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCHEMA_VERSION:kotlin.String` Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata#getVersion()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCOPE:kotlin.String` Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getScope()`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_ANDROID_TRUSTED:kotlin.String` Property value for #PROPERTY_REQUIRED_ACCESS_LEVEL representing that the function is accessible by any caller certified by Android that holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` permission. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_SELF:kotlin.String` Property value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_ACCESS_LEVEL:kotlin.String` representing that the function is strictly restricted to the app itself. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_SYSTEM:kotlin.String` Property value for #PROPERTY_REQUIRED_ACCESS_LEVEL representing that the function is accessible by holders of the `"android.permission.EXECUTE_APP_FUNCTIONS_SYSTEM"` permission. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_SCOPE_ACTIVITY:kotlin.String` Property value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCOPE:kotlin.String` in the XML representing `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_SCOPE_GLOBAL:kotlin.String` Property value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCOPE:kotlin.String` in the XML representing `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int` A constant indicating an app function is activity-scoped. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int` A constant indicating an app function is globally-scoped. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getAccessLevel()()` Returns the minimum access level required to call the function. |
| --- | --- |
| [GenericDocument](../android.app.appsearch/GenericDocument.md) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getMetadataDocument()()` Returns the app function's metadata as a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#`. |
| [AppFunctionName](../android/app/appfunctions/AppFunctionName.md) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getName()()` Returns the qualified name of the app function. |
| [AppFunctionPackageMetadata](../android/app/appfunctions/AppFunctionPackageMetadata.md) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getPackageMetadata()()` Returns the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionPackageMetadata` of the enclosing package. |
| --- | --- |
| [AppFunctionSchemaMetadata](AppFunctionSchemaMetadata.md)? | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()()` Returns the identifying metadata for a pre-defined schema which this app function implements. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getScope()()` Returns the scope of the app function. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AppFunctionMetadata](AppFunctionMetadata.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ACCESS_LEVEL_ANDROID_TRUSTED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_LEVEL_ANDROID_TRUSTED: Int
```

A constant indicating that the app function is accessible by any caller certified by Android that holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` permission.

This is the broadest access level. It includes access for all narrower levels: `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SYSTEM:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SELF:kotlin.Int`.

 Value: 300

### ACCESS_LEVEL_SELF

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_LEVEL_SELF: Int
```

A constant indicating that the app function is strictly restricted to the app itself.

 Value: 100

### ACCESS_LEVEL_SYSTEM

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_LEVEL_SYSTEM: Int
```

A constant indicating that the app function is accessible by holders of the android.Manifest.permission#EXECUTE_APP_FUNCTIONS_SYSTEM permission.

Includes access for: `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SELF:kotlin.Int`.

 Value: 200

### PROPERTY_ACCESS_LEVEL

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_ACCESS_LEVEL: String
```

Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getAccessLevel()`.

If unspecified, this defaults to `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_ANDROID_TRUSTED:kotlin.String`.

 Value: "accessLevel"

### PROPERTY_ENABLED_BY_DEFAULT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_ENABLED_BY_DEFAULT: String
```

Property name for the XML tag that defines the default value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionState#isEnabled()`, before calling `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#setAppFunctionEnabled(kotlin.String,%20kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

 Value: "enabledByDefault"

### PROPERTY_FUNCTION_ID

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_FUNCTION_ID: String
```

Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName#getFunctionIdentifier()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getName()`.

 Value: "id"

### PROPERTY_SCHEMA_CATEGORY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SCHEMA_CATEGORY: String
```

Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata#getCategory()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()`.

 Value: "schemaCategory"

### PROPERTY_SCHEMA_NAME

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SCHEMA_NAME: String
```

Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata#getName()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()`.

 Value: "schemaName"

### PROPERTY_SCHEMA_VERSION

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SCHEMA_VERSION: String
```

Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata#getVersion()` returned by `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getSchemaMetadata()`.

 Value: "schemaVersion"

### PROPERTY_SCOPE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_SCOPE: String
```

Property name for the XML tag that defines the value of `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getScope()`.

This property is should not be used for XML assets referenced by an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionService` declaration in the manifest, which are always `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int`.

 Value: "scope"

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#getScope()`

### PROPERTY_VALUE_ACCESS_LEVEL_ANDROID_TRUSTED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_VALUE_ACCESS_LEVEL_ANDROID_TRUSTED: String
```

Property value for #PROPERTY_REQUIRED_ACCESS_LEVEL representing that the function is accessible by any caller certified by Android that holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#EXECUTE_APP_FUNCTIONS:kotlin.String` permission.

This is the broadest access level. It includes access for all narrower levels: `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_SYSTEM:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_SELF:kotlin.String`.

 Value: "androidTrusted"

### PROPERTY_VALUE_ACCESS_LEVEL_SELF

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_VALUE_ACCESS_LEVEL_SELF: String
```

Property value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_ACCESS_LEVEL:kotlin.String` representing that the function is strictly restricted to the app itself.

 Value: "self"

### PROPERTY_VALUE_ACCESS_LEVEL_SYSTEM

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_VALUE_ACCESS_LEVEL_SYSTEM: String
```

Property value for #PROPERTY_REQUIRED_ACCESS_LEVEL representing that the function is accessible by holders of the `"android.permission.EXECUTE_APP_FUNCTIONS_SYSTEM"` permission.

Includes access for: `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_VALUE_ACCESS_LEVEL_SELF:kotlin.String`.

 Value: "system"

### PROPERTY_VALUE_SCOPE_ACTIVITY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_VALUE_SCOPE_ACTIVITY: String
```

Property value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCOPE:kotlin.String` in the XML representing `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int`.

 Value: "activity"

### PROPERTY_VALUE_SCOPE_GLOBAL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PROPERTY_VALUE_SCOPE_GLOBAL: String
```

Property value for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_SCOPE:kotlin.String` in the XML representing `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int`.

 Value: "global"

### SCOPE_ACTIVITY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCOPE_ACTIVITY: Int
```

A constant indicating an app function is activity-scoped.

Multiple app function implementations with the same `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName` can exist simultaneously, each registered from a different `https://developer.android.com/reference/kotlin/android/app/Activity.html#` instance, which is identified by an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionActivityId`.

Functions with this scope must be registered using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`, and must be called from an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context. Calling it from any other context will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

To execute an activity-scoped function, the caller of android.app.appfunctions.AppFunctionManager#executeAppFunction must use `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest.Builder#setActivityId(android.app.appfunctions.AppFunctionActivityId)`, otherwise `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_FUNCTION_NOT_FOUND:kotlin.Int` will be returned.

To discover the specific activities where an activity-scoped function is currently registered, see `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionStates(kotlin.collections.MutableList,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` and `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#getAppFunctionActivityStates(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`.

The function remains registered until it is explicitly unregistered or the activity is destroyed.

**IMPORTANT:** Functions provided with `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)` called from an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context should prefer `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int`. Only use `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int` for such functions if you are absolutely sure there can be only one instance of that activity.

 Value: 1

### SCOPE_GLOBAL

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCOPE_GLOBAL: Int
```

A constant indicating an app function is globally-scoped.

There can be at most one app function implementation with the same `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName` available with this scope. This is useful for functions that are tied to a singleton component, such as a foreground service.

When using `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)`, the function remains registered until it is explicitly unregistered or the calling context is destroyed.

To execute a globally-scoped function, the caller of android.app.appfunctions.AppFunctionManager#executeAppFunction must not use `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionRequest.Builder#setActivityId(android.app.appfunctions.AppFunctionActivityId)` (or set it to null), otherwise `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionException#ERROR_FUNCTION_NOT_FOUND:kotlin.Int` will be returned.

This is always the scope for `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionService`-based functions.

**IMPORTANT:** Functions provided with `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionManager#registerAppFunction(kotlin.String,%20java.util.concurrent.Executor,%20android.app.appfunctions.AppFunction)` called from an `https://developer.android.com/reference/kotlin/android/app/Activity.html#` context should prefer `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int`. Only use `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int` for such functions if you are absolutely sure there can be only one instance of that activity.

 Value: 0

## Public methods

### describeContents

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAccessLevel

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccessLevel(): Int
```

Returns the minimum access level required to call the function.

Access levels are hierarchical; granting a broader access level implicitly grants access to all narrower levels.

If unspecified, this defaults to `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_ANDROID_TRUSTED:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SELF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#ACCESS_LEVEL_ANDROID_TRUSTED:kotlin.Int` |

### getMetadataDocument

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMetadataDocument(): GenericDocument
```

Returns the app function's metadata as a `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#`.

Client-defined properties can be retrieved using the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` property getters.

Properties that are not defined in this class (see `PROPERTY_*` constants) are not guaranteed to be available or consistent across devices and versions.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#` | This value cannot be `null`. |

### getName

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): AppFunctionName
```

Returns the qualified name of the app function.

The `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName` is composed of the app's package name and the function's identifier.

This is defined by the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#PROPERTY_FUNCTION_ID:kotlin.String` tag in the XML.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName` | This value cannot be `null`. |

### getPackageMetadata

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageMetadata(): AppFunctionPackageMetadata
```

Returns the `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionPackageMetadata` of the enclosing package.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionPackageMetadata` | This value cannot be `null`. |

### getSchemaMetadata

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSchemaMetadata(): AppFunctionSchemaMetadata?
```

Returns the identifying metadata for a pre-defined schema which this app function implements.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionSchemaMetadata?` | This value may be `null`. |

### getScope

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScope(): Int
```

Returns the scope of the app function.

The scope determines the function's lifecycle and uniqueness rules. Depending on the scope, there could be at most one or multiple functions registered in the system with the same `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionName`.

See values below for more details on each scope.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_GLOBAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionMetadata#SCOPE_ACTIVITY:kotlin.Int` |

### hashCode

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AppFunctionMetadata!>
```

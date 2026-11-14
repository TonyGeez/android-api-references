Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetSchemaResponse

```
class GetSchemaResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.GetSchemaResponse](GetSchemaResponse.md) |

The response class of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#getSchema(java.util.concurrent.Executor,%20java.util.function.Consumer)`

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#` objects. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [PackageIdentifier](PackageIdentifier.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getPubliclyVisibleSchemas()()` Returns a mapping of publicly visible schemas to the `https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier` specifying the package the schemas are from. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getRequiredPermissionsForSchemaTypeVisibility()()` Returns a mapping of schema types to the set of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#` combination sets that querier must hold to access that schema type. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getSchemaTypesNotDisplayedBySystem()()` Returns all the schema types that are opted out of being displayed and visible on any system UI surface. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SchemaVisibilityConfig](SchemaVisibilityConfig.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getSchemaTypesVisibleToConfigs()()` Returns a mapping of schema types to the set of `https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig` that have access to that schema type. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PackageIdentifier](PackageIdentifier.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getSchemaTypesVisibleToPackages()()` Returns a mapping of schema types to the set of packages that have access to that schema type. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchSchema](AppSearchSchema.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getSchemas()()` Return the schemas most recently successfully provided to `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PropertyPath](PropertyPath.md)!\>!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getSchemasWipeoutAccountPropertyPaths()()` Returns a map containing all schema types that have been configured for account wipeout, mapped to the specific property paths within those schemas that hold the account identifiers. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#getVersion()()` Returns the overall database schema version. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GetSchemaResponse](GetSchemaResponse.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/GetSchemaResponse#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getPubliclyVisibleSchemas

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getPubliclyVisibleSchemas(): MutableMap<String!, PackageIdentifier!>
```

Returns a mapping of publicly visible schemas to the `https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier` specifying the package the schemas are from.

If no schemas have been set as publicly visible, an empty set will be returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier!>` | This value cannot be `null`. |

### getRequiredPermissionsForSchemaTypeVisibility

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun getRequiredPermissionsForSchemaTypeVisibility(): MutableMap<String!, MutableSet<MutableSet<Int!>!>!>
```

Returns a mapping of schema types to the set of `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#` combination sets that querier must hold to access that schema type.

The querier could read the `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` objects under the `schemaType` if they holds ALL required permissions of ANY of the individual value sets.

For example, if the Map contains `{{permissionA, PermissionB}, { PermissionC, PermissionD}, {PermissionE}}`.

- A querier holding both PermissionA and PermissionB has access.
- A querier holding both PermissionC and PermissionD has access.
- A querier holding only PermissionE has access.
- A querier holding both PermissionA and PermissionE has access.
- A querier holding only PermissionA doesn't have access.
- A querier holding only PermissionA and PermissionC doesn't have access.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!>!>` | The map contains schema type and all combinations of required permission for querier to access it. The supported Permission are `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_SMS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_CALENDAR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_CONTACTS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_EXTERNAL_STORAGE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_HOME_APP_SEARCH_DATA:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_ASSISTANT_APP_SEARCH_DATA:kotlin.Int`. This value cannot be `null`. |

### getSchemaTypesNotDisplayedBySystem

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun getSchemaTypesNotDisplayedBySystem(): MutableSet<String!>
```

Returns all the schema types that are opted out of being displayed and visible on any system UI surface.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getSchemaTypesVisibleToConfigs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getSchemaTypesVisibleToConfigs(): MutableMap<String!, MutableSet<SchemaVisibilityConfig!>!>
```

Returns a mapping of schema types to the set of `https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig` that have access to that schema type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig!>!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addSchemaTypeVisibleToConfig(kotlin.String,%20android.app.appsearch.SchemaVisibilityConfig)`

### getSchemaTypesVisibleToPackages

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

```
fun getSchemaTypesVisibleToPackages(): MutableMap<String!, MutableSet<PackageIdentifier!>!>
```

Returns a mapping of schema types to the set of packages that have access to that schema type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier!>!>` | This value cannot be `null`. |

### getSchemas

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSchemas(): MutableSet<AppSearchSchema!>
```

Return the schemas most recently successfully provided to `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema!>` | This value cannot be `null`. |

### getSchemasWipeoutAccountPropertyPaths

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 22](https://developer.android.com/sdkExtensions)

```
fun getSchemasWipeoutAccountPropertyPaths(): MutableMap<String!, MutableSet<PropertyPath!>!>
```

Returns a map containing all schema types that have been configured for account wipeout, mapped to the specific property paths within those schemas that hold the account identifiers.

This method performs a deep copy to ensure the returned map and its contained sets are immutable from external modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath!>!>` | A map where keys are schema type names, and values are sets of `https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath` strings configured for account wipeout for that schema type. This value cannot be `null`. |

### getVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVersion(): Int
```

Returns the overall database schema version.

If the database is empty, 0 will be returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 0 or greater |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<GetSchemaResponse!>
```

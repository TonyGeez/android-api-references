Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SetSchemaResponse

```
class SetSchemaResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.SetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#) |

The response class of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#` objects. |
| | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure` The class represents a post-migrated `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` that failed to be saved by `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getDeletedTypes()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` of deleted schema types. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getIncompatibleTypes()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` of schema type whose new definitions set in the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` call were incompatible with the pre-existing schema. |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getMigratedTypes()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` of schema type that were migrated by the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` call. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SetSchemaResponse.MigrationFailure](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getMigrationFailures()()` Returns a `https://developer.android.com/reference/kotlin/java/util/List.html#` of all failed `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SetSchemaResponse](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#CREATOR:android.os.Parcelable.Creator` <br /> |

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

### getDeletedTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeletedTypes(): MutableSet<String!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` of deleted schema types.

A "deleted" type is a schema type that was previously a part of the database schema but was not present in the `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest` object provided in the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` call.

Documents for a deleted type are removed from the database.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getIncompatibleTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIncompatibleTypes(): MutableSet<String!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` of schema type whose new definitions set in the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` call were incompatible with the pre-existing schema.

If a `https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator` is provided for this type and the migration is success triggered. The type will also appear in `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getMigratedTypes()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest`
- `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`
- `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setForceOverride(kotlin.Boolean)`

### getMigratedTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMigratedTypes(): MutableSet<String!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` of schema type that were migrated by the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer)` call.

A "migrated" type is a schema type that has triggered a `https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator` instance to migrate documents of the schema type to another schema type, or to another version of the schema type.

If a document fails to be migrated, a `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure` will be generated for that document.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator`

### getMigrationFailures

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMigrationFailures(): MutableList<SetSchemaResponse.MigrationFailure!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/List.html#` of all failed `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure`.

A `https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure` will be generated if the system trying to save a post-migrated `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` but fail.

`https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure` contains the namespace, id and schemaType of the post-migrated `https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument` and the error reason. Mostly it will be mismatch the schema it migrated to.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse.MigrationFailure!>` | This value cannot be `null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<SetSchemaResponse!>
```

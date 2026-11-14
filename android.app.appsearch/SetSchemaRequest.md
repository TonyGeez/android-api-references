# SetSchemaRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SetSchemaRequest

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/SetSchemaRequest "View this page in Java") 

```
class SetSchemaRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.SetSchemaRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#) |

Encapsulates a request to update the schema of an [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession) database.

The schema is composed of a collection of [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) objects, each of which defines a unique type of data.

The first call to SetSchemaRequest will set the provided schema and store it within the [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession) database.

Subsequent calls will compare the provided schema to the previously saved schema, to determine how to treat existing documents.

The following types of schema modifications are always safe and are made without deleting any existing documents:

- Addition of new [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) types
- Addition of new properties to an existing [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) type
- Changing the cardinality of a property to be less restrictive

The following types of schema changes are not backwards compatible:

- Removal of an existing [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) type
- Removal of a property from an existing [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) type
- Changing the data type of an existing property
- Changing the cardinality of a property to be more restrictive

Providing a schema with incompatible changes, will throw an , with a message describing the incompatibility. As a result, the previously set schema will remain unchanged.

Backward incompatible changes can be made by :

- setting [SetSchemaRequest.Builder.setForceOverride](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#setForceOverride(kotlin.Boolean))method to`true`. This deletes all documents that are incompatible with the new schema. The new schema is then saved and persisted to disk.
- Add a [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator) for each incompatible type and make no deletion. The migrator will migrate documents from its old schema version to the new version. Migrated types will be set into both [SetSchemaResponse.getIncompatibleTypes()](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getIncompatibleTypes())and [android.app.appsearch.SetSchemaResponse#getMigratedTypes()](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaResponse#getMigratedTypes()). See the migration section below.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder) Builder for [SetSchemaRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_ASSISTANT_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_ASSISTANT_APP_SEARCH_DATA:kotlin.Int) The [android.Manifest.permission#READ_ASSISTANT_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_ASSISTANT_APP_SEARCH_DATA:kotlin.String) AppSearch supported in [SetSchemaRequest.Builder.addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_CALENDAR](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_CALENDAR:kotlin.Int) The [android.Manifest.permission#READ_CALENDAR](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CALENDAR:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_CONTACTS](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_CONTACTS:kotlin.Int) The [android.Manifest.permission#READ_CONTACTS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CONTACTS:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_EXTERNAL_STORAGE:kotlin.Int) The [android.Manifest.permission#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_HOME_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_HOME_APP_SEARCH_DATA:kotlin.Int) The [android.Manifest.permission#READ_HOME_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_HOME_APP_SEARCH_DATA:kotlin.String) AppSearch supported in [SetSchemaRequest.Builder.addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [READ_SMS](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_SMS:kotlin.Int) The [android.Manifest.permission#READ_SMS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SMS:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator)!\> | [getMigrators](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getMigrators())`()` Returns the map of [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator), the key will be the schema type of the [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator) associated with. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier)!\> | [getPubliclyVisibleSchemas](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getPubliclyVisibleSchemas())`()` Returns a mapping of publicly visible schemas to the [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier) specifying the package the schemas are from. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>!\> | [getRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getRequiredPermissionsForSchemaTypeVisibility())`()` Returns a mapping of schema types to the Map of [android.Manifest.permission](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#) combinations that querier must hold to access that schema type. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema)!\> | [getSchemas](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getSchemas())`()` Returns the [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) types that are part of this request. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSchemasNotDisplayedBySystem](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getSchemasNotDisplayedBySystem())`()` Returns all the schema types that are opted out of being displayed and visible on any system UI surface. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig)!\>!\> | [getSchemasVisibleToConfigs](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getSchemasVisibleToConfigs())`()` Returns a mapping of schema types to the set of [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) that have access to that schema type. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier)!\>!\> | [getSchemasVisibleToPackages](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getSchemasVisibleToPackages())`()` Returns a mapping of schema types to the set of packages that have access to that schema type. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#getVersion())`()` Returns the database overall schema version. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForceOverride](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#isForceOverride())`()` Returns whether this request will force the schema to be overridden. |

## Constants

### READ_ASSISTANT_APP_SEARCH_DATA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
static val READ_ASSISTANT_APP_SEARCH_DATA: Int
```

The [android.Manifest.permission#READ_ASSISTANT_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_ASSISTANT_APP_SEARCH_DATA:kotlin.String) AppSearch supported in [SetSchemaRequest.Builder.addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) 

 Value: 6

### READ_CALENDAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
static val READ_CALENDAR: Int
```

The [android.Manifest.permission#READ_CALENDAR](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CALENDAR:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) 

 Value: 2

### READ_CONTACTS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
static val READ_CONTACTS: Int
```

The [android.Manifest.permission#READ_CONTACTS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_CONTACTS:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) 

 Value: 3

### READ_EXTERNAL_STORAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
static val READ_EXTERNAL_STORAGE: Int
```

The [android.Manifest.permission#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) 

 Value: 4

### READ_HOME_APP_SEARCH_DATA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
static val READ_HOME_APP_SEARCH_DATA: Int
```

The [android.Manifest.permission#READ_HOME_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_HOME_APP_SEARCH_DATA:kotlin.String) AppSearch supported in [SetSchemaRequest.Builder.addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) 

 Value: 5

### READ_SMS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
static val READ_SMS: Int
```

The [android.Manifest.permission#READ_SMS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_SMS:kotlin.String) AppSearch supported in [android.app.appsearch.SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addRequiredPermissionsForSchemaTypeVisibility(kotlin.String,%20kotlin.collections.MutableSet)) 

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

### getMigrators

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMigrators(): MutableMap<String!, Migrator!>
```

Returns the map of [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator), the key will be the schema type of the [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator) associated with.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Migrator](https://developer.android.com/reference/kotlin/android/app/appsearch/Migrator)!> | This value cannot be`null`. |

### getPubliclyVisibleSchemas

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPubliclyVisibleSchemas(): MutableMap<String!, PackageIdentifier!>
```

Returns a mapping of publicly visible schemas to the [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier) specifying the package the schemas are from.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier)!> | This value cannot be`null`. |

### getRequiredPermissionsForSchemaTypeVisibility

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getRequiredPermissionsForSchemaTypeVisibility(): MutableMap<String!, MutableSet<MutableSet<Int!>!>!>
```

Returns a mapping of schema types to the Map of [android.Manifest.permission](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#) combinations that querier must hold to access that schema type.

The querier could read the [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) objects under the`schemaType`if they holds ALL required permissions of ANY of the individual value sets.

For example, if the Map contains`{{permissionA, PermissionB}, {PermissionC, PermissionD}, {PermissionE}}`.

- A querier holds both PermissionA and PermissionB has access.
- A querier holds both PermissionC and PermissionD has access.
- A querier holds only PermissionE has access.
- A querier holds both PermissionA and PermissionE has access.
- A querier holds only PermissionA doesn't have access.
- A querier holds both PermissionA and PermissionC doesn't have access.

It's inefficient to call this method repeatedly.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!>!> | The map contains schema type and all combinations of required permission for querier to access it. The supported Permission are [SetSchemaRequest.READ_SMS](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_SMS:kotlin.Int), [android.app.appsearch.SetSchemaRequest#READ_CALENDAR](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_CALENDAR:kotlin.Int), [SetSchemaRequest.READ_CONTACTS](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_CONTACTS:kotlin.Int), [android.app.appsearch.SetSchemaRequest#READ_EXTERNAL_STORAGE](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_EXTERNAL_STORAGE:kotlin.Int), [android.app.appsearch.SetSchemaRequest#READ_HOME_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_HOME_APP_SEARCH_DATA:kotlin.Int) and [android.app.appsearch.SetSchemaRequest#READ_ASSISTANT_APP_SEARCH_DATA](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest#READ_ASSISTANT_APP_SEARCH_DATA:kotlin.Int). This value cannot be`null`. |

### getSchemas

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSchemas(): MutableSet<AppSearchSchema!>
```

Returns the [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema) types that are part of this request.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [AppSearchSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSchema)!> | This value cannot be`null`. |

### getSchemasNotDisplayedBySystem

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSchemasNotDisplayedBySystem(): MutableSet<String!>
```

Returns all the schema types that are opted out of being displayed and visible on any system UI surface.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getSchemasVisibleToConfigs

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getSchemasVisibleToConfigs(): MutableMap<String!, MutableSet<SchemaVisibilityConfig!>!>
```

Returns a mapping of schema types to the set of [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig) that have access to that schema type.

It's inefficient to call this method repeatedly.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SchemaVisibilityConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SchemaVisibilityConfig)!>!> | This value cannot be`null`. |

**See Also**

- [android.app.appsearch.SetSchemaRequest.Builder#addSchemaTypeVisibleToConfig](https://developer.android.com/reference/kotlin/android/app/appsearch/SetSchemaRequest.Builder#addSchemaTypeVisibleToConfig(kotlin.String,%20android.app.appsearch.SchemaVisibilityConfig)) 

### getSchemasVisibleToPackages

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSchemasVisibleToPackages(): MutableMap<String!, MutableSet<PackageIdentifier!>!>
```

Returns a mapping of schema types to the set of packages that have access to that schema type.

It's inefficient to call this method repeatedly.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PackageIdentifier](https://developer.android.com/reference/kotlin/android/app/appsearch/PackageIdentifier)!>!> | This value cannot be`null`. |

### getVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Returns the database overall schema version.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isForceOverride

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isForceOverride(): Boolean
```

Returns whether this request will force the schema to be overridden.

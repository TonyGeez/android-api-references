# SchemaChangeInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

# SchemaChangeInfo

Kotlin| [Java](SchemaChangeInfo.md) 
| --- | --- |

```
class SchemaChangeInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.observer.SchemaChangeInfo](SchemaChangeInfo.md) |

Contains information about a schema change detected by an [ObserverCallback](ObserverCallback.md).

This object will be sent when a schema type having a name matching an observer's schema filters (as determined by [ObserverSpec.getFilterSchemas](ObserverSpec.md))) has been added, updated, or removed.

Note that schema changes may cause documents to be migrated or removed. When this happens, individual document updates will NOT be dispatched via [DocumentChangeInfo](DocumentChangeInfo.md). The only notification will be of the schema type change via [SchemaChangeInfo](SchemaChangeInfo.md). Depending on your use case, you may need to re-query the whole schema type when this happens.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SchemaChangeInfo](SchemaChangeInfo.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `changedSchemaNames:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Constructs a new [SchemaChangeInfo](SchemaChangeInfo.md). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](SchemaChangeInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getChangedSchemaNames](SchemaChangeInfo.md))`()` Returns the names of schema types affected by this change notification. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDatabaseName](SchemaChangeInfo.md))`()` Returns the database in which the schema that was changed resides. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](SchemaChangeInfo.md))`()` Returns the package name of the app which owns the schema that changed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](SchemaChangeInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SchemaChangeInfo.md))`()` Returns a string representation of the object. |
| --- | --- |

## Public constructors

### SchemaChangeInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
SchemaChangeInfo(
    packageName: String, 
    databaseName: String, 
    changedSchemaNames: MutableSet<String!>)
```

Constructs a new [SchemaChangeInfo](SchemaChangeInfo.md).

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package name of the app which owns the schema that changed. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The database in which the schema that changed resides. This value cannot be`null`. |
| `changedSchemaNames` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:Names of schemas that have changed as part of this notification. This value cannot be`null`. |
| --- | --- |

## Public methods

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getChangedSchemaNames

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getChangedSchemaNames(): MutableSet<String!>
```

Returns the names of schema types affected by this change notification.

This will never be empty.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getDatabaseName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getDatabaseName(): String
```

Returns the database in which the schema that was changed resides.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getPackageName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getPackageName(): String
```

Returns the package name of the app which owns the schema that changed.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

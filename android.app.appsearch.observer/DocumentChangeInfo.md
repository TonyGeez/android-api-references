# DocumentChangeInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

# DocumentChangeInfo

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/observer/DocumentChangeInfo "View this page in Java") 

```
class DocumentChangeInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.observer.DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#) |

Contains information about an individual change detected by an [ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback).

This class reports information about document changes, that is, when documents were added, updated or removed.

Changes are grouped by package, database, schema type and namespace. Each unique combination of these items will generate a unique [DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#).

Notifications are only sent for documents whose schema type matches an observer's schema filters (as determined by [ObserverSpec.getFilterSchemas](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverSpec#getFilterSchemas())).

Note that document changes that happen during schema migration from calling [android.app.appsearch.AppSearchSession#setSchema](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession.html#setSchema(android.app.appsearch.SetSchemaRequest,%20java.util.concurrent.Executor,%20java.util.concurrent.Executor,%20java.util.function.Consumer))are not reported via this class. Such changes are reported through [SchemaChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/SchemaChangeInfo).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#DocumentChangeInfo(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.collections.MutableSet))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `database:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `schemaName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `changedDocumentIds:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Constructs a new [DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getChangedDocumentIds](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#getChangedDocumentIds())`()` Returns the set of document IDs that have been changed as part of this notification. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDatabaseName](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#getDatabaseName())`()` Returns the database in which the documents that was changed reside. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getNamespace](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#getNamespace())`()` Returns the namespace of the documents that changed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getPackageName](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#getPackageName())`()` Returns the package name of the app which owns the documents that changed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getSchemaName](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#getSchemaName())`()` Returns the name of the schema type that contains the changed documents. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#toString())`()` Returns a string representation of the object. |

## Public constructors

### DocumentChangeInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
DocumentChangeInfo(
    packageName: String, 
    database: String, 
    namespace: String, 
    schemaName: String, 
    changedDocumentIds: MutableSet<String!>)
```

Constructs a new [DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo#).

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package name of the app which owns the documents that changed. This value cannot be`null`. |
| `database` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The database in which the documents that changed reside. This value cannot be`null`. |
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The namespace in which the documents that changed reside. This value cannot be`null`. |
| `schemaName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the schema type that contains the changed documents. This value cannot be`null`. |
| `changedDocumentIds` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:The set of document IDs that have been changed as part of this notification. This value cannot be`null`. |

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

### getChangedDocumentIds

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getChangedDocumentIds(): MutableSet<String!>
```

Returns the set of document IDs that have been changed as part of this notification.

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

Returns the database in which the documents that was changed reside.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getNamespace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getNamespace(): String
```

Returns the namespace of the documents that changed.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getPackageName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getPackageName(): String
```

Returns the package name of the app which owns the documents that changed.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getSchemaName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getSchemaName(): String
```

Returns the name of the schema type that contains the changed documents.

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

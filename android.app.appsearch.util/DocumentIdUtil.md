# DocumentIdUtil

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# DocumentIdUtil

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/util/DocumentIdUtil "View this page in Java") 

```
open class DocumentIdUtil
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.appsearch.util.DocumentIdUtil](https://developer.android.com/reference/kotlin/android/app/appsearch/util/DocumentIdUtil#) |

A util class with methods for working with document ids.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [createQualifiedId](https://developer.android.com/reference/kotlin/android/app/appsearch/util/DocumentIdUtil#createQualifiedId(kotlin.String,%20kotlin.String,%20android.app.appsearch.GenericDocument))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `document:` ` [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#)`)` Generates a qualified id based on package, database, and a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#). |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [createQualifiedId](https://developer.android.com/reference/kotlin/android/app/appsearch/util/DocumentIdUtil#createQualifiedId(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Generates a qualified id based on package, database, namespace, and doc id. |

## Public methods

### createQualifiedId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
open static fun createQualifiedId(
    packageName: String, 
    databaseName: String, 
    document: GenericDocument
): String
```

Generates a qualified id based on package, database, and a [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package the document belongs to. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The database containing the document. This value cannot be`null`. |
| `document` | [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument.html#):The document to generate a qualified id for. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the qualified id of a document. This value cannot be`null`. |

**See Also**

- [#createQualifiedId(String, String, String, String)](https://developer.android.com/reference/kotlin/android/app/appsearch/util/DocumentIdUtil#createQualifiedId(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String)) 

### createQualifiedId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
open static fun createQualifiedId(
    packageName: String, 
    databaseName: String, 
    namespace: String, 
    id: String
): String
```

Generates a qualified id based on package, database, namespace, and doc id.

A qualified id is a String referring to the combined package name, database name, namespace, and id of the document. It is useful for linking one document to another in order to perform a join operation with [JoinSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec.html#).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package the document belongs to. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The database containing the document. This value cannot be`null`. |
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The namespace of the document. This value cannot be`null`. |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the document. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the qualified id of a document This value cannot be`null`. |

**See Also**

- [android.app.appsearch.JoinSpec](https://developer.android.com/reference/kotlin/android/app/appsearch/JoinSpec.html#)

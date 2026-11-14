# DocumentIdUtil

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# DocumentIdUtil

Kotlin| [Java](../android/app/appsearch/util/DocumentIdUtil.md) 
| --- | --- |

```
open class DocumentIdUtil
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.util.DocumentIdUtil](../android/app/appsearch/util/DocumentIdUtil.md) |

A util class with methods for working with document ids.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [createQualifiedId](../android/app/appsearch/util/DocumentIdUtil.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `document:` ` [GenericDocument](../android/app/appsearch/GenericDocument.md)`)` Generates a qualified id based on package, database, and a [GenericDocument](../android/app/appsearch/GenericDocument.md). |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [createQualifiedId](../android/app/appsearch/util/DocumentIdUtil.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `databaseName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Generates a qualified id based on package, database, namespace, and doc id. |

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

Generates a qualified id based on package, database, and a [GenericDocument](../android/app/appsearch/GenericDocument.md).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package the document belongs to. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The database containing the document. This value cannot be`null`. |
| `document` | [GenericDocument](../android/app/appsearch/GenericDocument.md):The document to generate a qualified id for. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the qualified id of a document. This value cannot be`null`. |

**See Also**

- [#createQualifiedId(String, String, String, String)](../android/app/appsearch/util/DocumentIdUtil.md)) 

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

A qualified id is a String referring to the combined package name, database name, namespace, and id of the document. It is useful for linking one document to another in order to perform a join operation with [JoinSpec](../android/app/appsearch/JoinSpec.md).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package the document belongs to. This value cannot be`null`. |
| `databaseName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The database containing the document. This value cannot be`null`. |
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The namespace of the document. This value cannot be`null`. |
| --- | --- |
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The id of the document. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the qualified id of a document This value cannot be`null`. |

**See Also**

- [android.app.appsearch.JoinSpec](../android/app/appsearch/JoinSpec.md)

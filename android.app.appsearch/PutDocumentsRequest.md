# PutDocumentsRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PutDocumentsRequest

Kotlin| [Java](../android/app/appsearch/PutDocumentsRequest.md) 
| --- | --- |

```
class PutDocumentsRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.PutDocumentsRequest](../android/app/appsearch/PutDocumentsRequest.md) |

Encapsulates a request to index documents into an [AppSearchSession](../android/app/appsearch/AppSearchSession.md) database.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/app/appsearch/PutDocumentsRequest.Builder.md) Builder for [PutDocumentsRequest](../android/app/appsearch/PutDocumentsRequest.md) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GenericDocument](../android/app/appsearch/GenericDocument.md)!\> | [getGenericDocuments](../android/app/appsearch/PutDocumentsRequest.md))`()` Returns a list of [GenericDocument](../android/app/appsearch/GenericDocument.md) objects that are part of this request. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GenericDocument](../android/app/appsearch/GenericDocument.md)!\> | [getTakenActionGenericDocuments](../android/app/appsearch/PutDocumentsRequest.md))`()` Returns a list of [GenericDocument](../android/app/appsearch/GenericDocument.md) objects containing taken action metrics that are part of this request. |

## Public methods

### getGenericDocuments

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericDocuments(): MutableList<GenericDocument!>
```

Returns a list of [GenericDocument](../android/app/appsearch/GenericDocument.md) objects that are part of this request.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GenericDocument](../android/app/appsearch/GenericDocument.md)!> | This value cannot be`null`. |

### getTakenActionGenericDocuments

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getTakenActionGenericDocuments(): MutableList<GenericDocument!>
```

Returns a list of [GenericDocument](../android/app/appsearch/GenericDocument.md) objects containing taken action metrics that are part of this request.

See [Builder.addTakenActionGenericDocuments(GenericDocument...)](../android/app/appsearch/PutDocumentsRequest.Builder.md)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GenericDocument](../android/app/appsearch/GenericDocument.md)!> | This value cannot be`null`. |

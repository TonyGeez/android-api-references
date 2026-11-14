# PutDocumentsRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PutDocumentsRequest

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/PutDocumentsRequest "View this page in Java") 
| --- | --- |

```
class PutDocumentsRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.PutDocumentsRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest#) |

Encapsulates a request to index documents into an [AppSearchSession](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession) database.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest.Builder) Builder for [PutDocumentsRequest](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest#) objects. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!\> | [getGenericDocuments](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest#getGenericDocuments())`()` Returns a list of [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) objects that are part of this request. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!\> | [getTakenActionGenericDocuments](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest#getTakenActionGenericDocuments())`()` Returns a list of [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) objects containing taken action metrics that are part of this request. |

## Public methods

### getGenericDocuments

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericDocuments(): MutableList<GenericDocument!>
```

Returns a list of [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) objects that are part of this request.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!> | This value cannot be`null`. |

### getTakenActionGenericDocuments

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getTakenActionGenericDocuments(): MutableList<GenericDocument!>
```

Returns a list of [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument) objects containing taken action metrics that are part of this request.

See [Builder.addTakenActionGenericDocuments(GenericDocument...)](https://developer.android.com/reference/kotlin/android/app/appsearch/PutDocumentsRequest.Builder#addTakenActionGenericDocuments(android.app.appsearch.GenericDocument)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [GenericDocument](https://developer.android.com/reference/kotlin/android/app/appsearch/GenericDocument)!> | This value cannot be`null`. |

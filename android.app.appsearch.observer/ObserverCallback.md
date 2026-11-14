# ObserverCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

# ObserverCallback

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/observer/ObserverCallback "View this page in Java") 
| --- | --- |

```
interface ObserverCallback
```

| [android.app.appsearch.observer.ObserverCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback#) |

An interface which apps can implement to subscribe to notifications of changes to AppSearch data.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDocumentChanged](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback#onDocumentChanged(android.app.appsearch.observer.DocumentChangeInfo))`(`changeInfo:` ` [DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo)`)` Callback to trigger after document changes (documents added, updated or removed). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSchemaChanged](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/ObserverCallback#onSchemaChanged(android.app.appsearch.observer.SchemaChangeInfo))`(`changeInfo:` ` [SchemaChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/SchemaChangeInfo)`)` Callback to trigger after schema changes (schema type added, updated or removed). |

## Public methods

### onDocumentChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
abstract fun onDocumentChanged(changeInfo: DocumentChangeInfo): Unit
```

Callback to trigger after document changes (documents added, updated or removed).

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `changeInfo` | [DocumentChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/DocumentChangeInfo):Information about the nature of the change. This value cannot be`null`. |

### onSchemaChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
abstract fun onSchemaChanged(changeInfo: SchemaChangeInfo): Unit
```

Callback to trigger after schema changes (schema type added, updated or removed).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `changeInfo` | [SchemaChangeInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/observer/SchemaChangeInfo):Information about the nature of the change. This value cannot be`null`. |

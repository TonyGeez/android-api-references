# ObserverCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions)

# ObserverCallback

Kotlin| [Java](../android/app/appsearch/observer/ObserverCallback.md) 
| --- | --- |

```
interface ObserverCallback
```

| [android.app.appsearch.observer.ObserverCallback](../android/app/appsearch/observer/ObserverCallback.md) |

An interface which apps can implement to subscribe to notifications of changes to AppSearch data.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDocumentChanged](../android/app/appsearch/observer/ObserverCallback.md))`(`changeInfo:` ` [DocumentChangeInfo](../android/app/appsearch/observer/DocumentChangeInfo.md)`)` Callback to trigger after document changes (documents added, updated or removed). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSchemaChanged](../android/app/appsearch/observer/ObserverCallback.md))`(`changeInfo:` ` [SchemaChangeInfo](../android/app/appsearch/observer/SchemaChangeInfo.md)`)` Callback to trigger after schema changes (schema type added, updated or removed). |

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
| `changeInfo` | [DocumentChangeInfo](../android/app/appsearch/observer/DocumentChangeInfo.md):Information about the nature of the change. This value cannot be`null`. |

### onSchemaChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
abstract fun onSchemaChanged(changeInfo: SchemaChangeInfo): Unit
```

Callback to trigger after schema changes (schema type added, updated or removed).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `changeInfo` | [SchemaChangeInfo](../android/app/appsearch/observer/SchemaChangeInfo.md):Information about the nature of the change. This value cannot be`null`. |

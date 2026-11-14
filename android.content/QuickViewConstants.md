# QuickViewConstants

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QuickViewConstants

Kotlin| [Java](../android/content/QuickViewConstants.md) 
| --- | --- |

```
open class QuickViewConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.QuickViewConstants](../android/content/QuickViewConstants.md) |

Constants for [Intent.ACTION_QUICK_VIEW](../android/content/Intent.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_DELETE](../android/content/QuickViewConstants.md) Feature to delete an individual document. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_DOWNLOAD](../android/content/QuickViewConstants.md) Feature to download a document to the local file system. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_EDIT](../android/content/QuickViewConstants.md) Feature to edit a document using system standard editing mechanism, like [Intent.ACTION_EDIT](../android/content/Intent.md). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_PRINT](../android/content/QuickViewConstants.md) Feature to print a document. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_SEND](../android/content/QuickViewConstants.md) Feature to view a document using system standard sending mechanism, like [Intent.ACTION_SEND](../android/content/Intent.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_VIEW](../android/content/QuickViewConstants.md) Feature to view a document using system standard viewing mechanism, like [Intent.ACTION_VIEW](../android/content/Intent.md). |
| --- | --- |

## Constants

### FEATURE_DELETE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_DELETE: String
```

Feature to delete an individual document. Quick viewer implementations must use Storage Access Framework to both verify delete permission and to delete content. 

 Value: "android:delete"

**See Also**

- [android.provider.DocumentsContract.Document#FLAG_SUPPORTS_DELETE](../android/provider/DocumentsContract.Document.md)
- [android.provider.DocumentsContract#deleteDocument(ContentResolver, android.net.Uri)](../android/provider/DocumentsContract.md)) 

### FEATURE_DOWNLOAD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_DOWNLOAD: String
```

Feature to download a document to the local file system. 

 Value: "android:download"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](../android/content/Intent.md)
- [android.content.Intent#ACTION_QUICK_VIEW](../android/content/Intent.md) 

### FEATURE_EDIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_EDIT: String
```

Feature to edit a document using system standard editing mechanism, like [Intent.ACTION_EDIT](../android/content/Intent.md). 

 Value: "android:edit"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](../android/content/Intent.md)
- [android.content.Intent#ACTION_QUICK_VIEW](../android/content/Intent.md) 

### FEATURE_PRINT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_PRINT: String
```

Feature to print a document. 

 Value: "android:print"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](../android/content/Intent.md)
- [android.content.Intent#ACTION_QUICK_VIEW](../android/content/Intent.md) 

### FEATURE_SEND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_SEND: String
```

Feature to view a document using system standard sending mechanism, like [Intent.ACTION_SEND](../android/content/Intent.md). 

 Value: "android:send"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](../android/content/Intent.md)
- [android.content.Intent#ACTION_QUICK_VIEW](../android/content/Intent.md) 

### FEATURE_VIEW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_VIEW: String
```

Feature to view a document using system standard viewing mechanism, like [Intent.ACTION_VIEW](../android/content/Intent.md). 

 Value: "android:view"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](../android/content/Intent.md)
- [android.content.Intent#ACTION_QUICK_VIEW](../android/content/Intent.md)

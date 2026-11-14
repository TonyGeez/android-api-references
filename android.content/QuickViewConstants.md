# QuickViewConstants

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QuickViewConstants

Kotlin| [Java](https://developer.android.com/reference/android/content/QuickViewConstants "View this page in Java") 

```
open class QuickViewConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.QuickViewConstants](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#) |

Constants for [Intent.ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_DELETE](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#FEATURE_DELETE:kotlin.String) Feature to delete an individual document. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_DOWNLOAD](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#FEATURE_DOWNLOAD:kotlin.String) Feature to download a document to the local file system. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_EDIT](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#FEATURE_EDIT:kotlin.String) Feature to edit a document using system standard editing mechanism, like [Intent.ACTION_EDIT](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_EDIT:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_PRINT](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#FEATURE_PRINT:kotlin.String) Feature to print a document. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_SEND](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#FEATURE_SEND:kotlin.String) Feature to view a document using system standard sending mechanism, like [Intent.ACTION_SEND](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_SEND:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_VIEW](https://developer.android.com/reference/kotlin/android/content/QuickViewConstants#FEATURE_VIEW:kotlin.String) Feature to view a document using system standard viewing mechanism, like [Intent.ACTION_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_VIEW:kotlin.String). |

## Constants

### FEATURE_DELETE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_DELETE: String
```

Feature to delete an individual document. Quick viewer implementations must use Storage Access Framework to both verify delete permission and to delete content. 

 Value: "android:delete"

**See Also**

- [android.provider.DocumentsContract.Document#FLAG_SUPPORTS_DELETE](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.Document.html#FLAG_SUPPORTS_DELETE:kotlin.Int)
- [android.provider.DocumentsContract#deleteDocument(ContentResolver, android.net.Uri)](https://developer.android.com/reference/kotlin/android/provider/DocumentsContract.html#deleteDocument(android.content.ContentResolver,%20android.net.Uri)) 

### FEATURE_DOWNLOAD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_DOWNLOAD: String
```

Feature to download a document to the local file system. 

 Value: "android:download"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](https://developer.android.com/reference/kotlin/android/content/Intent#EXTRA_QUICK_VIEW_FEATURES:kotlin.String)
- [android.content.Intent#ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String) 

### FEATURE_EDIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_EDIT: String
```

Feature to edit a document using system standard editing mechanism, like [Intent.ACTION_EDIT](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_EDIT:kotlin.String). 

 Value: "android:edit"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](https://developer.android.com/reference/kotlin/android/content/Intent#EXTRA_QUICK_VIEW_FEATURES:kotlin.String)
- [android.content.Intent#ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String) 

### FEATURE_PRINT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_PRINT: String
```

Feature to print a document. 

 Value: "android:print"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](https://developer.android.com/reference/kotlin/android/content/Intent#EXTRA_QUICK_VIEW_FEATURES:kotlin.String)
- [android.content.Intent#ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String) 

### FEATURE_SEND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_SEND: String
```

Feature to view a document using system standard sending mechanism, like [Intent.ACTION_SEND](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_SEND:kotlin.String). 

 Value: "android:send"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](https://developer.android.com/reference/kotlin/android/content/Intent#EXTRA_QUICK_VIEW_FEATURES:kotlin.String)
- [android.content.Intent#ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String) 

### FEATURE_VIEW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_VIEW: String
```

Feature to view a document using system standard viewing mechanism, like [Intent.ACTION_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_VIEW:kotlin.String). 

 Value: "android:view"

**See Also**

- [android.content.Intent#EXTRA_QUICK_VIEW_FEATURES](https://developer.android.com/reference/kotlin/android/content/Intent#EXTRA_QUICK_VIEW_FEATURES:kotlin.String)
- [android.content.Intent#ACTION_QUICK_VIEW](https://developer.android.com/reference/kotlin/android/content/Intent#ACTION_QUICK_VIEW:kotlin.String)

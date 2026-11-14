# ClipboardManager.OnPrimaryClipChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPrimaryClipChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/content/ClipboardManager.OnPrimaryClipChangedListener "View this page in Java") 

```
interface OnPrimaryClipChangedListener
```

| [android.content.ClipboardManager.OnPrimaryClipChangedListener](https://developer.android.com/reference/kotlin/android/content/ClipboardManager.OnPrimaryClipChangedListener#) |

Defines a listener callback that is invoked when the primary clip on the clipboard changes. Objects that want to register a listener call [addPrimaryClipChangedListener()](https://developer.android.com/reference/kotlin/android/content/ClipboardManager#addPrimaryClipChangedListener(android.content.ClipboardManager.OnPrimaryClipChangedListener))with an object that implements OnPrimaryClipChangedListener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrimaryClipChanged](https://developer.android.com/reference/kotlin/android/content/ClipboardManager.OnPrimaryClipChangedListener#onPrimaryClipChanged())`()` Callback that is invoked by [android.content.ClipboardManager](https://developer.android.com/reference/kotlin/android/content/ClipboardManager) when the primary clip changes. |

## Public methods

### onPrimaryClipChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPrimaryClipChanged(): Unit
```

Callback that is invoked by [android.content.ClipboardManager](https://developer.android.com/reference/kotlin/android/content/ClipboardManager) when the primary clip changes.

This is called when the result of [ClipDescription.getClassificationStatus()](https://developer.android.com/reference/kotlin/android/content/ClipDescription#getClassificationStatus())changes, as well as when new clip data is set. So in cases where text classification is performed, this callback may be invoked multiple times for the same clip.

# ClipboardManager.OnPrimaryClipChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPrimaryClipChangedListener

Kotlin| [Java](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md) 
| --- | --- |

```
interface OnPrimaryClipChangedListener
```

| [android.content.ClipboardManager.OnPrimaryClipChangedListener](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md) |

Defines a listener callback that is invoked when the primary clip on the clipboard changes. Objects that want to register a listener call [addPrimaryClipChangedListener()](ClipboardManager.md))with an object that implements OnPrimaryClipChangedListener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrimaryClipChanged](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md))`()` Callback that is invoked by [android.content.ClipboardManager](ClipboardManager.md) when the primary clip changes. |

## Public methods

### onPrimaryClipChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPrimaryClipChanged(): Unit
```

Callback that is invoked by [android.content.ClipboardManager](ClipboardManager.md) when the primary clip changes.

This is called when the result of [ClipDescription.getClassificationStatus()](ClipDescription.md))changes, as well as when new clip data is set. So in cases where text classification is performed, this callback may be invoked multiple times for the same clip.

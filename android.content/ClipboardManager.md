# ClipboardManager

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClipboardManager

Kotlin| [Java](ClipboardManager.md) 
| --- | --- |

```
open class ClipboardManager : ClipboardManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.ClipboardManager](../android.text/ClipboardManager.md) ||
| | ↳ | [android.content.ClipboardManager](ClipboardManager.md) |

Interface to the clipboard service, for placing and retrieving text in the global clipboard.

The ClipboardManager API itself is very simple: it consists of methods to atomically get and set the current primary clipboard data. That data is expressed as a [ClipData](ClipData.md) object, which defines the protocol for data exchange between applications.
|
| ### Developer Guides
|
| For more information about using the clipboard framework, read the [Copy and Paste](https://developer.android.com/guide/topics/clipboard/copy-paste.html) developer guide.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnPrimaryClipChangedListener](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md) Defines a listener callback that is invoked when the primary clip on the clipboard changes. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPrimaryClipChangedListener](ClipboardManager.md))`(`what:` ` [ClipboardManager.OnPrimaryClipChangedListener](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearPrimaryClip](ClipboardManager.md))`()` Clears any current primary clip on the clipboard. |
| open [ClipData](ClipData.md)? | [getPrimaryClip](ClipboardManager.md))`()` Returns the current primary clip on the clipboard. |
| --- | --- |
| open [ClipDescription](ClipDescription.md)? | [getPrimaryClipDescription](ClipboardManager.md))`()` Returns a description of the current primary clip on the clipboard but not a copy of its data. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](ClipboardManager.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPrimaryClip](ClipboardManager.md))`()` Returns true if there is currently a primary clip on the clipboard. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasText](ClipboardManager.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePrimaryClipChangedListener](ClipboardManager.md))`(`what:` ` [ClipboardManager.OnPrimaryClipChangedListener](../android/content/ClipboardManager.OnPrimaryClipChangedListener.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrimaryClip](ClipboardManager.md))`(`clip:` ` [ClipData](ClipData.md)`)` Sets the current primary clip on the clipboard. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](ClipboardManager.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |

## Public methods

### addPrimaryClipChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPrimaryClipChangedListener(what: ClipboardManager.OnPrimaryClipChangedListener!): Unit
```  

### clearPrimaryClip

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearPrimaryClip(): Unit
```

Clears any current primary clip on the clipboard. 
**See Also**

- [#setPrimaryClip(ClipData)](ClipboardManager.md)) 

### getPrimaryClip

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryClip(): ClipData?
```

Returns the current primary clip on the clipboard.*If the application is not the default IME or does not have input focus this return`null`.* 
**See Also**

- [#setPrimaryClip(ClipData)](ClipboardManager.md)) 

### getPrimaryClipDescription

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryClipDescription(): ClipDescription?
```

Returns a description of the current primary clip on the clipboard but not a copy of its data.

*If the application is not the default IME or does not have input focus this return`null`.* 
**See Also**

- [#setPrimaryClip(ClipData)](ClipboardManager.md)) 

### getText

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(): CharSequence!
```

**Deprecated:** *Use [getPrimaryClip()](ClipboardManager.md))instead. This retrieves the primary clip and tries to coerce it to a string.* 

### hasPrimaryClip

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasPrimaryClip(): Boolean
```

Returns true if there is currently a primary clip on the clipboard.*If the application is not the default IME or the does not have input focus this will return`false`.* 

### hasText

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasText(): Boolean
```

**Deprecated:** *Use [hasPrimaryClip()](ClipboardManager.md))instead.* 

### removePrimaryClipChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePrimaryClipChangedListener(what: ClipboardManager.OnPrimaryClipChangedListener!): Unit
```  

### setPrimaryClip

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPrimaryClip(clip: ClipData): Unit
```

Sets the current primary clip on the clipboard. This is the clip that is involved in normal cut and paste operations.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `clip` | [ClipData](ClipData.md):The clipped data item to set. This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/content/ClipboardManager#getPrimaryClip()>
- <https://developer.android.com/reference/kotlin/android/content/ClipboardManager#clearPrimaryClip()> 

### setText

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setText(text: CharSequence!): Unit
```

**Deprecated:** *Use [setPrimaryClip(android.content.ClipData)](ClipboardManager.md))instead. This creates a ClippedItem holding the given text and sets it as the primary clip. It has no label or icon.*

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContentCaptureNodeProperties

```
open class ContentCaptureNodeProperties
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.contentcapture.ContentCaptureNodeProperties](../android/view/contentcapture/ContentCaptureNodeProperties.md) |

Properties of a Node for Content Capture.

Used to provide changes from a UI node (e.g. a View or a virtual view) to the Content Capture System efficiently. An instance of this class should be reused during view tree traversal to minimize memory allocations.

To use this class:

1. Obtain the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the node. For virtual views, use `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#newAutofillId(android.view.autofill.AutofillId,%20kotlin.Long)`.
2. Set the desired properties on an instance of this class (e.g., `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#setText(kotlin.CharSequence)`, `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)`).
3. Pass the ID and this properties instance to `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureSession#notifyNodeAppearedOrChanged(android.view.autofill.AutofillId,%20android.view.contentcapture.ContentCaptureNodeProperties)`.
4. Call `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#clear()` to reset the properties before reusing the instance for the next node.

<br />

To track which properties have been modified explicitly this class offers methods like `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasBounds()`, `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasText()` that will return `true` only if the corresponding property was explicitly set. Calling `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#clear()` removes all set fields and brings back this class to its initial state to be reused.

Calling a getter method when the corresponding property has not been set (i.e. when `has*()` returns `false`) will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. Callers should check `has*()` prior to calling the getter.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#ContentCaptureNodeProperties()()` <br /> |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#clear()()` Clears the entire properties object for reuse. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#getBounds(android.graphics.Rect)(outBounds: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)` Copies the relative boundaries of this node into the provided `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#`. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#getContentDescription()()` Gets the content description of the node. |
| --- | --- |
| open [AutofillId](../android/view/autofill/AutofillId.md)? | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#getParentId()()` Gets the parent ID of the node. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#getText()()` Gets the text of the node. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasBounds()()` Checks if the bounds have been explicitly set. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasContentDescription()()` Checks if the content description has been explicitly set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasParentId()()` Checks if the parent ID has been explicitly set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasText()()` Checks if the text has been explicitly set. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#setBounds(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(left: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, right: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the boundaries for this node relative to the parent node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#setContentDescription(kotlin.CharSequence)(contentDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the content description for this node. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#setParentId(android.view.autofill.AutofillId)(parentId: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#?)` Sets the parent ID for this node. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#setText(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the text for this node. |

## Public constructors

### ContentCaptureNodeProperties

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ContentCaptureNodeProperties()
```

## Public methods

### clear

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Clears the entire properties object for reuse. This resets all properties to their default unspecified state, meaning all "has\*" methods will subsequently return false.

### getBounds

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBounds(outBounds: Rect): Unit
```

Copies the relative boundaries of this node into the provided `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#`.

| Parameters ||
|---|---|
| `outBounds` | [Rect](../android/graphics/Rect.md): The mutable `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#` to receive the bounds. Must not be null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasBounds()` is `false`. |

### getContentDescription

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContentDescription(): CharSequence?
```

Gets the content description of the node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the content description of the node, or `null` if explicitly set to `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasContentDescription()` is `false`. |

### getParentId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParentId(): AutofillId?
```

Gets the parent ID of the node.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#?` | The parent ID of the node, or `null` if explicitly set to `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasParentId()` is `false`. |

### getText

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getText(): CharSequence?
```

Gets the text of the node.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text of the node, or `null` if explicitly set to `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if `https://developer.android.com/reference/kotlin/android/view/contentcapture/ContentCaptureNodeProperties#hasText()` is `false`. |

### hasBounds

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasBounds(): Boolean
```

Checks if the bounds have been explicitly set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the bounds were modified, false otherwise. |

### hasContentDescription

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasContentDescription(): Boolean
```

Checks if the content description has been explicitly set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the content description was modified, false otherwise. |

### hasParentId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasParentId(): Boolean
```

Checks if the parent ID has been explicitly set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the parent ID was modified, false otherwise. |

### hasText

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasText(): Boolean
```

Checks if the text has been explicitly set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the text was modified, false otherwise. |

### setBounds

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBounds(
    left: Int, 
    top: Int, 
    right: Int, 
    bottom: Int
): Unit
```

Sets the boundaries for this node relative to the parent node.

| Parameters ||
|---|---|
| `left` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): left bound |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): top bound |
| `right` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): right bound |
| --- | --- |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bottom bound |

### setContentDescription

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setContentDescription(contentDescription: CharSequence?): Unit
```

Sets the content description for this node.

| Parameters ||
|---|---|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The content description to set, or null. |

### setParentId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParentId(parentId: AutofillId?): Unit
```

Sets the parent ID for this node.

| Parameters ||
|---|---|
| `parentId` | [AutofillId](../android/view/autofill/AutofillId.md)?: The parent ID to set, or null if the node has no parent. |

### setText

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setText(text: CharSequence?): Unit
```

Sets the text for this node.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The text to set, or null to remove current text. |

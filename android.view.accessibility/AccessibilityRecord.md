# AccessibilityRecord

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityRecord

Kotlin| [Java](../android/view/accessibility/AccessibilityRecord.md) 
| --- | --- |

```
open class AccessibilityRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) |

| Known Direct Subclasses [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) |--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------| | [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) | This class represents accessibility events that are sent by the system when something notable happens in the user interface. | |
| --- | --- | --- | --- | --- | --- | --- |

Represents a record in an [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md) and contains information about state change of its source [android.view.View](../android/view/View.md). When a view fires an accessibility event it requests from its parent to dispatch the constructed event. The parent may optionally append a record for itself for providing more context to [android.accessibilityservice.AccessibilityService](../android/accessibilityservice/AccessibilityService.md) s. Hence, accessibility services can facilitate additional accessibility records to enhance feedback.

<br />

Once the accessibility event containing a record is dispatched the record is made immutable and calling a state mutation method generates an error.

**Note:** Not all properties are applicable to all accessibility event types. For detailed information please refer to [AccessibilityEvent](../android/view/accessibility/AccessibilityEvent.md).
|
| ### Developer Guides
|
| For more information about creating and processing AccessibilityRecords, read the [Accessibility](https://developer.android.com/guide/topics/ui/accessibility/index.html) developer guide.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md))`()` Creates a new [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md). |
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md))`(`record:` ` [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)`)` Copy constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAddedCount](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the number of added characters. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getBeforeText](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the text before a change. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getClassName](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the class name of the source. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContentDescription](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the description of the source. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCurrentItemIndex](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the index of the source in the list of items the can be visited. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDisplayId](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the id of the display from which the event comes from. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFromIndex](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the index of the first character of the changed sequence, or the beginning of a text selection or the index of the first visible item when scrolling. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemCount](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the number of items that can be visited. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxScrollX](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the max scroll offset of the source left edge in pixels. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxScrollY](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the max scroll offset of the source top edge in pixels. |
| open [Parcelable](../android/os/Parcelable.md)? | [getParcelableData](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the [Parcelable](../android/os/Parcelable.md) data. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRemovedCount](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the number of removed characters. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollDeltaX](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the difference in pixels between the horizontal position before the scroll and the current horizontal position |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollDeltaY](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the difference in pixels between the vertical position before the scroll and the current vertical position |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollX](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the scroll offset of the source left edge in pixels. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScrollY](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the scroll offset of the source top edge in pixels. |
| open [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | [getSource](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) of the event source. |
| open [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | [getSource](../android/view/accessibility/AccessibilityRecord.md))`(`prefetchingStrategy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) of the event source. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\> | [getText](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the text of the event. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getToIndex](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the index of text selection end or the index of the last visible item when scrolling. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWindowId](../android/view/accessibility/AccessibilityRecord.md))`()` Gets the id of the window from which the event comes from. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](../android/view/accessibility/AccessibilityRecord.md))`()` Gets if the source is checked. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/view/accessibility/AccessibilityRecord.md))`()` Gets if the source is enabled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFullScreen](../android/view/accessibility/AccessibilityRecord.md))`()` Gets if the source is taking the entire screen. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPassword](../android/view/accessibility/AccessibilityRecord.md))`()` Gets if the source is a password field. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isScrollable](../android/view/accessibility/AccessibilityRecord.md))`()` Gets if the source is scrollable. |
| openstatic [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) | [obtain](../android/view/accessibility/AccessibilityRecord.md))`()` Instantiates a new record. |
| --- | --- |
| openstatic [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) | [obtain](../android/view/accessibility/AccessibilityRecord.md))`(`record:` ` [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md)`)` Instantiates a new record initialized with data from the given record. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](../android/view/accessibility/AccessibilityRecord.md))`()` Would previously return an instance back to be reused. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAddedCount](../android/view/accessibility/AccessibilityRecord.md))`(`addedCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of added characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBeforeText](../android/view/accessibility/AccessibilityRecord.md))`(`beforeText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Sets the text before a change. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChecked](../android/view/accessibility/AccessibilityRecord.md))`(`isChecked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets if the source is checked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClassName](../android/view/accessibility/AccessibilityRecord.md))`(`className:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Sets the class name of the source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentDescription](../android/view/accessibility/AccessibilityRecord.md))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Sets the description of the source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentItemIndex](../android/view/accessibility/AccessibilityRecord.md))`(`currentItemIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the index of the source in the list of items that can be visited. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/view/accessibility/AccessibilityRecord.md))`(`isEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets if the source is enabled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFromIndex](../android/view/accessibility/AccessibilityRecord.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the index of the first character of the changed sequence or the beginning of a text selection or the index of the first visible item when scrolling. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFullScreen](../android/view/accessibility/AccessibilityRecord.md))`(`isFullScreen:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets if the source is taking the entire screen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setItemCount](../android/view/accessibility/AccessibilityRecord.md))`(`itemCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of items that can be visited. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxScrollX](../android/view/accessibility/AccessibilityRecord.md))`(`maxScrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the max scroll offset of the source left edge in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxScrollY](../android/view/accessibility/AccessibilityRecord.md))`(`maxScrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the max scroll offset of the source top edge in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParcelableData](../android/view/accessibility/AccessibilityRecord.md))`(`parcelableData:` ` [Parcelable](../android/os/Parcelable.md)?`)` Sets the [Parcelable](../android/os/Parcelable.md) data of the event. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPassword](../android/view/accessibility/AccessibilityRecord.md))`(`isPassword:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets if the source is a password field. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRemovedCount](../android/view/accessibility/AccessibilityRecord.md))`(`removedCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of removed characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollDeltaX](../android/view/accessibility/AccessibilityRecord.md))`(`scrollDeltaX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the difference in pixels between the horizontal position before the scroll and the current horizontal position |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollDeltaY](../android/view/accessibility/AccessibilityRecord.md))`(`scrollDeltaY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the difference in pixels between the vertical position before the scroll and the current vertical position |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollX](../android/view/accessibility/AccessibilityRecord.md))`(`scrollX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the scroll offset of the source left edge in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollY](../android/view/accessibility/AccessibilityRecord.md))`(`scrollY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the scroll offset of the source top edge in pixels. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScrollable](../android/view/accessibility/AccessibilityRecord.md))`(`scrollable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets if the source is scrollable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](../android/view/accessibility/AccessibilityRecord.md))`(`source:` ` [View](../android/view/View.md)?`)` Sets the event source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSource](../android/view/accessibility/AccessibilityRecord.md))`(`root:` ` [View](../android/view/View.md)?`, `virtualDescendantId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the source to be a virtual descendant of the given`root`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToIndex](../android/view/accessibility/AccessibilityRecord.md))`(`toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the index of text selection end or the index of the last visible item when scrolling. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/accessibility/AccessibilityRecord.md))`()` <br /> |

## Public constructors

### AccessibilityRecord

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityRecord()
```

Creates a new [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md). 

### AccessibilityRecord

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityRecord(record: AccessibilityRecord)
```

Copy constructor. Creates a new [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md), and this instance is initialized with data from the given`record`.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md):The other record. This value cannot be`null`. |

## Public methods

### getAddedCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAddedCount(): Int
```

Gets the number of added characters.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of added characters. |

### getBeforeText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBeforeText(): CharSequence?
```

Gets the text before a change.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The text before the change. This value may be`null`. |

### getClassName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClassName(): CharSequence?
```

Gets the class name of the source.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The class name. This value may be`null`. |

### getContentDescription

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentDescription(): CharSequence?
```

Gets the description of the source.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The description. This value may be`null`. |

### getCurrentItemIndex

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrentItemIndex(): Int
```

Gets the index of the source in the list of items the can be visited.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The current item index. |

### getDisplayId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayId(): Int
```

Gets the id of the display from which the event comes from.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The display id. |

### getFromIndex

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFromIndex(): Int
```

Gets the index of the first character of the changed sequence, or the beginning of a text selection or the index of the first visible item when scrolling.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the first character or selection start or the first visible item. |

### getItemCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getItemCount(): Int
```

Gets the number of items that can be visited.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of items. |

### getMaxScrollX

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxScrollX(): Int
```

Gets the max scroll offset of the source left edge in pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The max scroll. |

### getMaxScrollY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxScrollY(): Int
```

Gets the max scroll offset of the source top edge in pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The max scroll. |

### getParcelableData

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParcelableData(): Parcelable?
```

Gets the [Parcelable](../android/os/Parcelable.md) data.

| Return ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Parcelable](../android/os/Parcelable.md)? | The parcelable data. This value may be`null`. |

### getRemovedCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemovedCount(): Int
```

Gets the number of removed characters.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of removed characters. |

### getScrollDeltaX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScrollDeltaX(): Int
```

Gets the difference in pixels between the horizontal position before the scroll and the current horizontal position

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the scroll delta x |

### getScrollDeltaY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScrollDeltaY(): Int
```

Gets the difference in pixels between the vertical position before the scroll and the current vertical position

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the scroll delta y |

### getScrollX

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScrollX(): Int
```

Gets the scroll offset of the source left edge in pixels.

| Return ||
|----------------------------------------------------------------------------|-------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The scroll. |

### getScrollY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScrollY(): Int
```

Gets the scroll offset of the source top edge in pixels.

| Return ||
|----------------------------------------------------------------------------|-------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The scroll. |

### getSource

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSource(): AccessibilityNodeInfo?
```

Gets the [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) of the event source.

**Note:** It is a client responsibility to recycle the received info by calling [AccessibilityNodeInfo#recycle()](../android/view/accessibility/AccessibilityNodeInfo.md))to avoid creating of multiple instances.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | The info of the source. This value may be`null`. |

### getSource

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSource(prefetchingStrategy: Int): AccessibilityNodeInfo?
```

Gets the [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md) of the event source.

| Parameters ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prefetchingStrategy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the prefetching strategy. Value is either`0`or a combination of [android.view.accessibility.AccessibilityNodeInfo#FLAG_PREFETCH_ANCESTORS](../android/view/accessibility/AccessibilityNodeInfo.md), [android.view.accessibility.AccessibilityNodeInfo#FLAG_PREFETCH_SIBLINGS](../android/view/accessibility/AccessibilityNodeInfo.md), [android.view.accessibility.AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_HYBRID](../android/view/accessibility/AccessibilityNodeInfo.md), [android.view.accessibility.AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_DEPTH_FIRST](../android/view/accessibility/AccessibilityNodeInfo.md), [android.view.accessibility.AccessibilityNodeInfo#FLAG_PREFETCH_DESCENDANTS_BREADTH_FIRST](../android/view/accessibility/AccessibilityNodeInfo.md), and [android.view.accessibility.AccessibilityNodeInfo#FLAG_PREFETCH_UNINTERRUPTIBLE](../android/view/accessibility/AccessibilityNodeInfo.md) |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [AccessibilityNodeInfo](../android/view/accessibility/AccessibilityNodeInfo.md)? | The info of the source. This value may be`null`. |

**See Also**

- [android.view.accessibility.AccessibilityNodeInfo#getParent(int)](../android/view/accessibility/AccessibilityNodeInfo.md)) 

### getText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(): MutableList<CharSequence!>
```

Gets the text of the event. The index in the list represents the priority of the text. Specifically, the lower the index the higher the priority.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!> | The text. This value cannot be`null`. |

### getToIndex

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getToIndex(): Int
```

Gets the index of text selection end or the index of the last visible item when scrolling.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of selection end or last item index. |

### getWindowId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWindowId(): Int
```

Gets the id of the window from which the event comes from.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The window id. |

### isChecked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isChecked(): Boolean
```

Gets if the source is checked.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the view is checked, false otherwise. |

### isEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEnabled(): Boolean
```

Gets if the source is enabled.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the view is enabled, false otherwise. |

### isFullScreen

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFullScreen(): Boolean
```

Gets if the source is taking the entire screen.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the source is full screen, false otherwise. |

### isPassword

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPassword(): Boolean
```

Gets if the source is a password field.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the view is a password field, false otherwise. |

### isScrollable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isScrollable(): Boolean
```

Gets if the source is scrollable.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the source is scrollable, false otherwise. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun obtain(): AccessibilityRecord
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityRecord()](../android/view/accessibility/AccessibilityRecord.md))instead.*

Instantiates a new record.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) | An instance. This value cannot be`null`. |

### obtain

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun obtain(record: AccessibilityRecord): AccessibilityRecord
```

**Deprecated:** *Object pooling has been discontinued. Create a new instance using the constructor [AccessibilityRecord()](../android/view/accessibility/AccessibilityRecord.md))instead.*

Instantiates a new record initialized with data from the given record.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `record` | [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md):This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [AccessibilityRecord](../android/view/accessibility/AccessibilityRecord.md) | An instance. This value cannot be`null`. |

### recycle

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun recycle(): Unit
```

**Deprecated:** *Object pooling has been discontinued. Calling this function now will have no effect.*

Would previously return an instance back to be reused. 

### setAddedCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAddedCount(addedCount: Int): Unit
```

Sets the number of added characters.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------|
| `addedCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of added characters. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setBeforeText

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBeforeText(beforeText: CharSequence?): Unit
```

Sets the text before a change.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `beforeText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The text before the change. This value may be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setChecked

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setChecked(isChecked: Boolean): Unit
```

Sets if the source is checked.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `isChecked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the view is checked, false otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setClassName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClassName(className: CharSequence?): Unit
```

Sets the class name of the source.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `className` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The lass name. This value may be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setContentDescription

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentDescription(contentDescription: CharSequence?): Unit
```

Sets the description of the source.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The description. This value may be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setCurrentItemIndex

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrentItemIndex(currentItemIndex: Int): Unit
```

Sets the index of the source in the list of items that can be visited.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------|
| `currentItemIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current item index. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnabled(isEnabled: Boolean): Unit
```

Sets if the source is enabled.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `isEnabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the view is enabled, false otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setFromIndex

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFromIndex(fromIndex: Int): Unit
```

Sets the index of the first character of the changed sequence or the beginning of a text selection or the index of the first visible item when scrolling.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the first character or selection start or the first visible item. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setFullScreen

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFullScreen(isFullScreen: Boolean): Unit
```

Sets if the source is taking the entire screen.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `isFullScreen` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the source is full screen, false otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setItemCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setItemCount(itemCount: Int): Unit
```

Sets the number of items that can be visited.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------|
| `itemCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of items. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setMaxScrollX

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaxScrollX(maxScrollX: Int): Unit
```

Sets the max scroll offset of the source left edge in pixels.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------|
| `maxScrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The max scroll. |

### setMaxScrollY

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaxScrollY(maxScrollY: Int): Unit
```

Sets the max scroll offset of the source top edge in pixels.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------|
| `maxScrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The max scroll. |

### setParcelableData

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParcelableData(parcelableData: Parcelable?): Unit
```

Sets the [Parcelable](../android/os/Parcelable.md) data of the event.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `parcelableData` | [Parcelable](../android/os/Parcelable.md)?:The parcelable data. This value may be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setPassword

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPassword(isPassword: Boolean): Unit
```

Sets if the source is a password field.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `isPassword` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the view is a password field, false otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setRemovedCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRemovedCount(removedCount: Int): Unit
```

Sets the number of removed characters.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------|
| `removedCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of removed characters. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setScrollDeltaX

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScrollDeltaX(scrollDeltaX: Int): Unit
```

Sets the difference in pixels between the horizontal position before the scroll and the current horizontal position

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------|
| `scrollDeltaX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the scroll delta x |

### setScrollDeltaY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScrollDeltaY(scrollDeltaY: Int): Unit
```

Sets the difference in pixels between the vertical position before the scroll and the current vertical position

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------|
| `scrollDeltaY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the scroll delta y |

### setScrollX

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScrollX(scrollX: Int): Unit
```

Sets the scroll offset of the source left edge in pixels.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------|
| `scrollX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The scroll. |

### setScrollY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScrollY(scrollY: Int): Unit
```

Sets the scroll offset of the source top edge in pixels.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------|
| `scrollY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The scroll. |

### setScrollable

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScrollable(scrollable: Boolean): Unit
```

Sets if the source is scrollable.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `scrollable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the source is scrollable, false otherwise. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setSource

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSource(source: View?): Unit
```

Sets the event source.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `source` | [View](../android/view/View.md)?:The source. This value may be`null`. |

| Exceptions ||
|-----------------------------------|-----------------------------------------|
| `java.lang.IllegalStateException` | If called from an AccessibilityService. |

### setSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSource(
    root: View?, 
    virtualDescendantId: Int
): Unit
```

Sets the source to be a virtual descendant of the given`root`. If`virtualDescendantId`equals to [View.NO_ID](../android/view/View.md) the root is set as the source.

A virtual descendant is an imaginary View that is reported as a part of the view hierarchy for accessibility purposes. This enables custom views that draw complex content to report them selves as a tree of virtual views, thus conveying their logical structure.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `root` | [View](../android/view/View.md)?:The root of the virtual subtree. This value may be`null`. |
| `virtualDescendantId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id of the virtual descendant. |

### setToIndex

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setToIndex(toIndex: Int): Unit
```

Sets the index of text selection end or the index of the last visible item when scrolling.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of selection end or last item index. |

### toString

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

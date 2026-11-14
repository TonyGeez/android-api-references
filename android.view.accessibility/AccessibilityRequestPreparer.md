# AccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityRequestPreparer

Kotlin| [Java](../android/view/accessibility/AccessibilityRequestPreparer.md) 
| --- | --- |

```
abstract class AccessibilityRequestPreparer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityRequestPreparer](../android/view/accessibility/AccessibilityRequestPreparer.md) |

Object responsible to ensuring that a [View](../android/view/View.md) is prepared to meet a synchronous request for accessibility data.

Because accessibility requests arrive to [View](../android/view/View.md) s synchronously on the UI thread, a View that requires information from other processes can struggle to meet those requests. Registering an instance of this class with [AccessibilityManager](../android/view/accessibility/AccessibilityManager.md) allows a View to be notified when a request is about to be made, and to asynchronously inform the accessibility system when it is ready to meet the request.

**Note:** This class should only be needed in exceptional situations where a [View](../android/view/View.md) cannot otherwise synchronously meet the request for accessibility data.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_EXTRA_DATA](../android/view/accessibility/AccessibilityRequestPreparer.md) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityRequestPreparer](../android/view/accessibility/AccessibilityRequestPreparer.md))`(`view:` ` [View](../android/view/View.md)!`, `requestTypes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](../android/view/View.md)? | [getView](../android/view/accessibility/AccessibilityRequestPreparer.md))`()` Get the view this object was created with. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareExtraData](../android/view/accessibility/AccessibilityRequestPreparer.md))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extraDataKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `args:` ` [Bundle](../android/os/Bundle.md)!`, `preparationFinishedMessage:` ` [Message](../android/os/Message.md)!`)` Callback to allow preparation for filling extra data. |

## Constants

### REQUEST_TYPE_EXTRA_DATA

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_EXTRA_DATA: Int
```  

 Value: 1

## Public constructors

### AccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AccessibilityRequestPreparer(
    view: View!, 
    requestTypes: Int)
```

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The view whose requests need preparation. It must be attached to a window. This object will retain a weak reference to this view, and will unregister itself from AccessibilityManager if the view is detached from a window. It will not re-register itself. |
| `requestTypes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The types of requests that require preparation. Different types may be ORed together. Value is either`0`or [android.view.accessibility.AccessibilityRequestPreparer#REQUEST_TYPE_EXTRA_DATA](../android/view/accessibility/AccessibilityRequestPreparer.md) |

| Exceptions ||
|-----------------------------------|------------------------------------------|
| `java.lang.IllegalStateException` | if the view is not attached to a window. |

## Public methods

### getView

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(): View?
```

Get the view this object was created with.

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)? | The view this object was created with, or`null`if the weak reference held to the view is no longer valid. |

### onPrepareExtraData

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPrepareExtraData(
    virtualViewId: Int, 
    extraDataKey: String!, 
    args: Bundle!, 
    preparationFinishedMessage: Message!
): Unit
```

Callback to allow preparation for filling extra data. Only called back if REQUEST_TYPE_EXTRA_DATA is requested.

| Parameters ||
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of a virtual child node, if the [View](../android/view/View.md) for this preparer supports virtual descendents, or [AccessibilityNodeProvider.HOST_VIEW_ID](../android/view/accessibility/AccessibilityNodeProvider.md) if the request is for the view itself. |
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The extra data key for the request |
| `args` | [Bundle](../android/os/Bundle.md)!:The arguments for the request |
| --- | --- |
| `preparationFinishedMessage` | [Message](../android/os/Message.md)!:A message that must be sent to its target when preparations are complete. |

**See Also**

- [android.view.View#addExtraDataToAccessibilityNodeInfo(AccessibilityNodeInfo, String, Bundle)](../android/view/View.md))
- [android.view.View.AccessibilityDelegate#addExtraDataToAccessibilityNodeInfo(
 * View, AccessibilityNodeInfo, String, Bundle)](../android/view/View.AccessibilityDelegate.md))
- [android.view.accessibility.AccessibilityNodeProvider#addExtraDataToAccessibilityNodeInfo(
 * int, AccessibilityNodeInfo, String, Bundle)](../android/view/accessibility/AccessibilityNodeProvider.md))

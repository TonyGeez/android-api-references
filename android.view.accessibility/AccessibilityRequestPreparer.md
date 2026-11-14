# AccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityRequestPreparer

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityRequestPreparer "View this page in Java") 
| --- | --- |

```
abstract class AccessibilityRequestPreparer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer#) |

Object responsible to ensuring that a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) is prepared to meet a synchronous request for accessibility data.

Because accessibility requests arrive to [View](https://developer.android.com/reference/kotlin/android/view/View.html#) s synchronously on the UI thread, a View that requires information from other processes can struggle to meet those requests. Registering an instance of this class with [AccessibilityManager](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager) allows a View to be notified when a request is about to be made, and to asynchronously inform the accessibility system when it is ready to meet the request.

**Note:** This class should only be needed in exceptional situations where a [View](https://developer.android.com/reference/kotlin/android/view/View.html#) cannot otherwise synchronously meet the request for accessibility data.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_EXTRA_DATA](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer#REQUEST_TYPE_EXTRA_DATA:kotlin.Int) <br /> |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer#AccessibilityRequestPreparer(android.view.View,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `requestTypes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | [getView](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer#getView())`()` Get the view this object was created with. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareExtraData](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer#onPrepareExtraData(kotlin.Int,%20kotlin.String,%20android.os.Bundle,%20android.os.Message))`(`virtualViewId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extraDataKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`, `preparationFinishedMessage:` ` [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!`)` Callback to allow preparation for filling extra data. |

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
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view whose requests need preparation. It must be attached to a window. This object will retain a weak reference to this view, and will unregister itself from AccessibilityManager if the view is detached from a window. It will not re-register itself. |
| `requestTypes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The types of requests that require preparation. Different types may be ORed together. Value is either`0`or [android.view.accessibility.AccessibilityRequestPreparer#REQUEST_TYPE_EXTRA_DATA](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer#REQUEST_TYPE_EXTRA_DATA:kotlin.Int) |

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
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)? | The view this object was created with, or`null`if the weak reference held to the view is no longer valid. |

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
| `virtualViewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ID of a virtual child node, if the [View](https://developer.android.com/reference/kotlin/android/view/View.html#) for this preparer supports virtual descendents, or [AccessibilityNodeProvider.HOST_VIEW_ID](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#HOST_VIEW_ID:kotlin.Int) if the request is for the view itself. |
| `extraDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The extra data key for the request |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The arguments for the request |
| --- | --- |
| `preparationFinishedMessage` | [Message](https://developer.android.com/reference/kotlin/android/os/Message.html#)!:A message that must be sent to its target when preparations are complete. |

**See Also**

- [android.view.View#addExtraDataToAccessibilityNodeInfo(AccessibilityNodeInfo, String, Bundle)](https://developer.android.com/reference/kotlin/android/view/View.html#addExtraDataToAccessibilityNodeInfo(android.view.accessibility.AccessibilityNodeInfo,%20kotlin.String,%20android.os.Bundle))
- [android.view.View.AccessibilityDelegate#addExtraDataToAccessibilityNodeInfo(
 * View, AccessibilityNodeInfo, String, Bundle)](https://developer.android.com/reference/kotlin/android/view/View.AccessibilityDelegate.html#addExtraDataToAccessibilityNodeInfo(android.view.View,%20android.view.accessibility.AccessibilityNodeInfo,%20kotlin.String,%20android.os.Bundle))
- [android.view.accessibility.AccessibilityNodeProvider#addExtraDataToAccessibilityNodeInfo(
 * int, AccessibilityNodeInfo, String, Bundle)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider#addExtraDataToAccessibilityNodeInfo(kotlin.Int,%20android.view.accessibility.AccessibilityNodeInfo,%20kotlin.String,%20android.os.Bundle))

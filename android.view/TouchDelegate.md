# TouchDelegate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TouchDelegate

Kotlin| [Java](../android/view/TouchDelegate.md) 
| --- | --- |

```
open class TouchDelegate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.TouchDelegate](../android/view/TouchDelegate.md) |

Helper class to handle situations where you want a view to have a larger touch area than its actual view bounds. The view whose touch area is changed is called the delegate view. This class should be used by an ancestor of the delegate. To use a TouchDelegate, first create an instance that specifies the bounds that should be mapped to the delegate and the delegate view itself.

The ancestor should then forward all of its touch events received in its [android.view.View#onTouchEvent(MotionEvent)](../android/view/View.md))to [onTouchEvent(android.view.MotionEvent)](../android/view/TouchDelegate.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ABOVE](../android/view/TouchDelegate.md) The touchable region of the View extends above its actual extent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BELOW](../android/view/TouchDelegate.md) The touchable region of the View extends below its actual extent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_LEFT](../android/view/TouchDelegate.md) The touchable region of the View extends to the left of its actual extent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TO_RIGHT](../android/view/TouchDelegate.md) The touchable region of the View extends to the right of its actual extent. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TouchDelegate](../android/view/TouchDelegate.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)!`, `delegateView:` ` [View](../android/view/View.md)!`)` Constructor |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AccessibilityNodeInfo.TouchDelegateInfo](../android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo.md) | [getTouchDelegateInfo](../android/view/TouchDelegate.md))`()` Return a [TouchDelegateInfo](../android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo.md) mapping from regions (in view coordinates) to delegated views for accessibility usage. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](../android/view/TouchDelegate.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Forward touch events to the delegate view if the event is within the bounds specified in the constructor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchExplorationHoverEvent](../android/view/TouchDelegate.md))`(`event:` ` [MotionEvent](../android/view/MotionEvent.md)`)` Forward hover events to the delegate view if the event is within the bounds specified in the constructor and touch exploration is enabled. |
| --- | --- |

## Constants

### ABOVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ABOVE: Int
```

The touchable region of the View extends above its actual extent. 

 Value: 1

### BELOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BELOW: Int
```

The touchable region of the View extends below its actual extent. 

 Value: 2

### TO_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_LEFT: Int
```

The touchable region of the View extends to the left of its actual extent. 

 Value: 4

### TO_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TO_RIGHT: Int
```

The touchable region of the View extends to the right of its actual extent. 

 Value: 8

## Public constructors

### TouchDelegate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TouchDelegate(
    bounds: Rect!, 
    delegateView: View!)
```

Constructor

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android/graphics/Rect.md)!:Bounds in local coordinates of the containing view that should be mapped to the delegate view |
| `delegateView` | [View](../android/view/View.md)!:The view that should receive motion events |

## Public methods

### getTouchDelegateInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTouchDelegateInfo(): AccessibilityNodeInfo.TouchDelegateInfo
```

Return a [TouchDelegateInfo](../android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo.md) mapping from regions (in view coordinates) to delegated views for accessibility usage.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [AccessibilityNodeInfo.TouchDelegateInfo](../android/view/accessibility/AccessibilityNodeInfo.TouchDelegateInfo.md) | A TouchDelegateInfo. This value cannot be`null`. |

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(event: MotionEvent): Boolean
```

Forward touch events to the delegate view if the event is within the bounds specified in the constructor.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](../android/view/MotionEvent.md):The touch event to forward This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was consumed by the delegate, false otherwise. |

### onTouchExplorationHoverEvent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchExplorationHoverEvent(event: MotionEvent): Boolean
```

Forward hover events to the delegate view if the event is within the bounds specified in the constructor and touch exploration is enabled.

This method is provided for accessibility purposes so touch exploration, which is commonly used by screen readers, can properly place accessibility focus on views that use touch delegates. Therefore, touch exploration must be enabled for hover events to be dispatched through the delegate.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](../android/view/MotionEvent.md):The hover event to forward This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was consumed by the delegate, false otherwise. |

**See Also**

- [android.view.accessibility.AccessibilityManager#isTouchExplorationEnabled](../android/view/accessibility/AccessibilityManager.md))

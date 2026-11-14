# AccessibilityManager

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityManager

Kotlin| [Java](AccessibilityManager.md) 
| --- | --- |

```
class AccessibilityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityManager](AccessibilityManager.md) |

System level service that serves as an event dispatch for [AccessibilityEvent](AccessibilityEvent.md) s, and provides facilities for querying the accessibility state of the system. Accessibility events are generated when something notable happens in the user interface, for example an [android.app.Activity](../android.app/Activity.md) starts, the focus or selection of a [android.view.View](../android.view/View.md) changes etc. Parties interested in handling accessibility events implement and register an accessibility service which extends [android.accessibilityservice.AccessibilityService](../android.accessibilityservice/AccessibilityService.md).

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md) Listener for changes to the state of accessibility services. |
| abstract | [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) Listener for the system accessibility state. |
| abstract | [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) Listener for the audio description by default state. |
| --- | --- |
| abstract | [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) Listener for the system high contrast text state. |
| abstract | [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) Listener for the system touch exploration state. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CONTENT_CONTROLS](AccessibilityManager.md) Use this flag to indicate the content of a UI that times out contains interactive controls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CONTENT_ICONS](AccessibilityManager.md) Use this flag to indicate the content of a UI that times out contains icons. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CONTENT_TEXT](AccessibilityManager.md) Use this flag to indicate the content of a UI that times out contains text. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityRequestPreparer](AccessibilityManager.md))`(`preparer:` ` [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md)!`)` Registers a [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityServicesStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md)`)` Registers a [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityServicesStateChangeListener](AccessibilityManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md)`)` Registers a [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAccessibilityStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md)`)` Registers an [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) for changes in the global accessibility state of the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Registers an [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) for changes in the global accessibility state of the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAudioDescriptionRequestedChangeListener](AccessibilityManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [AccessibilityManager.AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md)`)` Registers a [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) for changes in the audio description by default state of the system. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addHighContrastTextStateChangeListener](AccessibilityManager.md))`(`executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `listener:` ` [AccessibilityManager.HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md)`)` Registers a [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) for changes in the global high contrast text state of the system. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addTouchExplorationStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md)`)` Registers a [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) for changes in the global touch exploration state of the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTouchExplorationStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md)`, `handler:` ` [Handler](../android.os/Handler.md)?`)` Registers an [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) for changes in the global touch exploration state of the system. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccessibilityFocusColor](AccessibilityManager.md))`()` Gets the color of the focus rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccessibilityFocusStrokeWidth](AccessibilityManager.md))`()` Gets the strokeWidth of the focus rectangle. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ServiceInfo](../android.content.pm/ServiceInfo.md)!\>! | [getAccessibilityServiceList](AccessibilityManager.md))`()` Returns the [ServiceInfo](../android.content.pm/ServiceInfo.md) s of the installed accessibility services. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md)!\>! | [getEnabledAccessibilityServiceList](AccessibilityManager.md))`(`feedbackTypeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) s of the enabled accessibility services for a given feedback type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md)!\>! | [getInstalledAccessibilityServiceList](AccessibilityManager.md))`()` Returns the [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) s of the installed accessibility services. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecommendedTimeoutMillis](AccessibilityManager.md))`(`originalTimeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uiContentFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the recommended timeout for changes to the UI needed by this user. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [interrupt](AccessibilityManager.md))`()` Requests feedback interruption from all accessibility services. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessibilityButtonSupported](AccessibilityManager.md))`()` Determines if the accessibility button within the system navigation area is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAudioDescriptionRequested](AccessibilityManager.md))`()` Determines if users want to select sound track with audio description by default. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](AccessibilityManager.md))`()` Returns if the accessibility in the system is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHighContrastTextEnabled](AccessibilityManager.md))`()` Returns if high contrast text in the system is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRequestFromAccessibilityTool](AccessibilityManager.md))`()` Whether the current accessibility request comes from an [AccessibilityService](../android.accessibilityservice/AccessibilityService.md) with the [AccessibilityServiceInfo.isAccessibilityTool](../android.accessibilityservice/AccessibilityServiceInfo.md))property set to true. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTouchExplorationEnabled](AccessibilityManager.md))`()` Returns if the touch exploration in the system is enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAccessibilityRequestPreparer](AccessibilityManager.md))`(`preparer:` ` [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md)!`)` Unregisters a [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAccessibilityServicesStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md)`)` Unregisters a [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAccessibilityStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md)`)` Unregisters an [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAudioDescriptionRequestedChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md)`)` Unregisters a [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeHighContrastTextStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md)`)` Unregisters a [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeTouchExplorationStateChangeListener](AccessibilityManager.md))`(`listener:` ` [AccessibilityManager.TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md)`)` Unregisters a [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendAccessibilityEvent](AccessibilityManager.md))`(`event:` ` [AccessibilityEvent](AccessibilityEvent.md)!`)` Sends an [AccessibilityEvent](AccessibilityEvent.md). |

## Constants

### FLAG_CONTENT_CONTROLS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CONTENT_CONTROLS: Int
```

Use this flag to indicate the content of a UI that times out contains interactive controls. 

 Value: 4

**See Also**

- [#getRecommendedTimeoutMillis(int, int)](AccessibilityManager.md)) 

### FLAG_CONTENT_ICONS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CONTENT_ICONS: Int
```

Use this flag to indicate the content of a UI that times out contains icons. 

 Value: 1

**See Also**

- [#getRecommendedTimeoutMillis(int, int)](AccessibilityManager.md)) 

### FLAG_CONTENT_TEXT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CONTENT_TEXT: Int
```

Use this flag to indicate the content of a UI that times out contains text. 

 Value: 2

**See Also**

- [#getRecommendedTimeoutMillis(int, int)](AccessibilityManager.md))

## Public methods

### addAccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityRequestPreparer(preparer: AccessibilityRequestPreparer!): Unit
```

Registers a [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md). 

### addAccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityServicesStateChangeListener(listener: AccessibilityManager.AccessibilityServicesStateChangeListener): Unit
```

Registers a [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md). This will execute a callback on the process's main handler.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md):The listener. This value cannot be`null`. |

### addAccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityServicesStateChangeListener(
    executor: Executor, 
    listener: AccessibilityManager.AccessibilityServicesStateChangeListener
): Unit
```

Registers a [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md):The listener. This value cannot be`null`. |

### addAccessibilityStateChangeListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityStateChangeListener(listener: AccessibilityManager.AccessibilityStateChangeListener): Boolean
```

Registers an [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) for changes in the global accessibility state of the system. Equivalent to calling [addAccessibilityStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener,android.os.Handler)](AccessibilityManager.md))with a null handler.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Always returns`true`. |

### addAccessibilityStateChangeListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityStateChangeListener(
    listener: AccessibilityManager.AccessibilityStateChangeListener, 
    handler: Handler?
): Unit
```

Registers an [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md) for changes in the global accessibility state of the system. If the listener has already been registered, the handler used to call it back is updated.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md):The listener. This value cannot be`null`. |
| `handler` | [Handler](../android.os/Handler.md)?:The handler on which the listener should be called back, or`null`for a callback on the process's main handler. |

### addAudioDescriptionRequestedChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAudioDescriptionRequestedChangeListener(
    executor: Executor, 
    listener: AccessibilityManager.AudioDescriptionRequestedChangeListener
): Unit
```

Registers a [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md) for changes in the audio description by default state of the system. The value could be read via [isAudioDescriptionRequested](AccessibilityManager.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):The executor on which the listener should be called back. This value cannot be`null`. |
| `listener` | [AccessibilityManager.AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md):The listener. This value cannot be`null`. |

### addHighContrastTextStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addHighContrastTextStateChangeListener(
    executor: Executor, 
    listener: AccessibilityManager.HighContrastTextStateChangeListener
): Unit
```

Registers a [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md) for changes in the global high contrast text state of the system.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java.util.concurrent/Executor.md):a executor to call the listener from This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `listener` | [AccessibilityManager.HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md):The listener to be called This value cannot be`null`. |

### addTouchExplorationStateChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addTouchExplorationStateChangeListener(listener: AccessibilityManager.TouchExplorationStateChangeListener): Boolean
```

Registers a [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) for changes in the global touch exploration state of the system. Equivalent to calling [addTouchExplorationStateChangeListener(android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener,android.os.Handler)](AccessibilityManager.md))with a null handler.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Always returns`true`. |

### addTouchExplorationStateChangeListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addTouchExplorationStateChangeListener(
    listener: AccessibilityManager.TouchExplorationStateChangeListener, 
    handler: Handler?
): Unit
```

Registers an [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md) for changes in the global touch exploration state of the system. If the listener has already been registered, the handler used to call it back is updated.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md):The listener. This value cannot be`null`. |
| `handler` | [Handler](../android.os/Handler.md)?:The handler on which the listener should be called back, or`null`for a callback on the process's main handler. |

### getAccessibilityFocusColor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessibilityFocusColor(): Int
```

Gets the color of the focus rectangle. This value can be set by [AccessibilityService](../android.accessibilityservice/AccessibilityService.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color of the focus rectangle. |

### getAccessibilityFocusStrokeWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessibilityFocusStrokeWidth(): Int
```

Gets the strokeWidth of the focus rectangle. This value can be set by [AccessibilityService](../android.accessibilityservice/AccessibilityService.md).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The strokeWidth of the focus rectangle in pixels. |

### getAccessibilityServiceList

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessibilityServiceList(): MutableList<ServiceInfo!>!
```

**Deprecated:** *Use [getInstalledAccessibilityServiceList()](AccessibilityManager.md))*

Returns the [ServiceInfo](../android.content.pm/ServiceInfo.md) s of the installed accessibility services.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ServiceInfo](../android.content.pm/ServiceInfo.md)!>! | An unmodifiable list with [ServiceInfo](../android.content.pm/ServiceInfo.md) s. |

### getEnabledAccessibilityServiceList

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEnabledAccessibilityServiceList(feedbackTypeFlags: Int): MutableList<AccessibilityServiceInfo!>!
```

Returns the [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) s of the enabled accessibility services for a given feedback type.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------|
| `feedbackTypeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The feedback type flags. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md)!>! | An unmodifiable list with [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) s. |

**See Also**

- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_AUDIBLE](../android.accessibilityservice/AccessibilityServiceInfo.md)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_GENERIC](../android.accessibilityservice/AccessibilityServiceInfo.md)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_HAPTIC](../android.accessibilityservice/AccessibilityServiceInfo.md)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_SPOKEN](../android.accessibilityservice/AccessibilityServiceInfo.md)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_VISUAL](../android.accessibilityservice/AccessibilityServiceInfo.md)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_BRAILLE](../android.accessibilityservice/AccessibilityServiceInfo.md) 

### getInstalledAccessibilityServiceList

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInstalledAccessibilityServiceList(): MutableList<AccessibilityServiceInfo!>!
```

Returns the [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) s of the installed accessibility services.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md)!>! | An unmodifiable list with [AccessibilityServiceInfo](../android.accessibilityservice/AccessibilityServiceInfo.md) s. |

### getRecommendedTimeoutMillis

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecommendedTimeoutMillis(
    originalTimeout: Int, 
    uiContentFlags: Int
): Int
```

Get the recommended timeout for changes to the UI needed by this user. Controls should remain on the screen for at least this long to give users time to react. Some users may need extra time to review the controls, or to reach them, or to activate assistive technology to activate the controls automatically.

Use the combination of content flags to indicate contents of UI. For example, use`FLAG_CONTENT_ICONS | FLAG_CONTENT_TEXT`for message notification which contains icons and text, or use`FLAG_CONTENT_TEXT | FLAG_CONTENT_CONTROLS`for button dialog which contains text and button controls.
| --- | --- | --- |

<br />

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `originalTimeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The timeout appropriate for users with no accessibility needs. |
| `uiContentFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The combination of flags [FLAG_CONTENT_ICONS](AccessibilityManager.md), [FLAG_CONTENT_TEXT](AccessibilityManager.md) or [FLAG_CONTENT_CONTROLS](AccessibilityManager.md) to indicate the contents of UI. Value is either`0`or a combination of [android.view.accessibility.AccessibilityManager#FLAG_CONTENT_ICONS](AccessibilityManager.md), [android.view.accessibility.AccessibilityManager#FLAG_CONTENT_TEXT](AccessibilityManager.md), and [android.view.accessibility.AccessibilityManager#FLAG_CONTENT_CONTROLS](AccessibilityManager.md) |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The recommended UI timeout for the current user in milliseconds. |

### interrupt

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun interrupt(): Unit
```

Requests feedback interruption from all accessibility services. 

### isAccessibilityButtonSupported

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isAccessibilityButtonSupported(): Boolean
```

Determines if the accessibility button within the system navigation area is supported.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the accessibility button is supported on this device,`false`otherwise |

### isAudioDescriptionRequested

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAudioDescriptionRequested(): Boolean
```

Determines if users want to select sound track with audio description by default.

Audio description, also referred to as a video description, described video, or more precisely called a visual description, is a form of narration used to provide information surrounding key visual elements in a media work for the benefit of blind and visually impaired consumers.

The method provides the preference value to content provider apps to select the default sound track during playing a video or movie.

Add listener to detect the state change via [addAudioDescriptionRequestedChangeListener](AccessibilityManager.md))

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the audio description is enabled,`false`otherwise. |

### isEnabled

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

Returns if the accessibility in the system is enabled.

**Note:** This query is used for sending [AccessibilityEvent](AccessibilityEvent.md) s, since events are only needed if accessibility is on. Avoid changing UI or app behavior based on the state of accessibility. While well-intentioned, doing this creates brittle, less well-maintained code that works for some users but not others. Shared code leads to more equitable experiences and less technical debt.

For example, if you want to expose a unique interaction with your app, use ViewCompat#addAccessibilityAction in AndroidX to make this interaction - ideally with the same code path used for non-accessibility users - available to accessibility services. Services can then expose this action in the way best fit for their users.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if accessibility is enabled, false otherwise. |

### isHighContrastTextEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHighContrastTextEnabled(): Boolean
```

Returns if high contrast text in the system is enabled.

**Note:**You need to query this only if you application is doing its own rendering and does not rely on the platform rendering pipeline.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if high contrast text is enabled, false otherwise. |

### isRequestFromAccessibilityTool

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRequestFromAccessibilityTool(): Boolean
```

Whether the current accessibility request comes from an [AccessibilityService](../android.accessibilityservice/AccessibilityService.md) with the [AccessibilityServiceInfo.isAccessibilityTool](../android.accessibilityservice/AccessibilityServiceInfo.md))property set to true.

You can use this method inside [AccessibilityNodeProvider](AccessibilityNodeProvider.md) to decide how to populate your nodes.

**Note:** The return value is valid only when an [AccessibilityNodeInfo](AccessibilityNodeInfo.md) request is in progress, can change from one request to another, and has no meaning when a request is not in progress.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the current request is from a tool that sets isAccessibilityTool. |

### isTouchExplorationEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isTouchExplorationEnabled(): Boolean
```

Returns if the touch exploration in the system is enabled.

**Note:** This query is used for dispatching hover events, such as [android.view.MotionEvent#ACTION_HOVER_ENTER](../android.view/MotionEvent.md), to accessibility services to manage touch exploration. Avoid changing UI or app behavior based on the state of accessibility. While well-intentioned, doing this creates brittle, less well-maintained code that works for som users but not others. Shared code leads to more equitable experiences and less technical debt.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if touch exploration is enabled, false otherwise. |

### removeAccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAccessibilityRequestPreparer(preparer: AccessibilityRequestPreparer!): Unit
```

Unregisters a [AccessibilityRequestPreparer](AccessibilityRequestPreparer.md). 

### removeAccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAccessibilityServicesStateChangeListener(listener: AccessibilityManager.AccessibilityServicesStateChangeListener): Boolean
```

Unregisters a [AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityServicesStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener.md):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the listener was previously registered. |

### removeAccessibilityStateChangeListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAccessibilityStateChangeListener(listener: AccessibilityManager.AccessibilityStateChangeListener): Boolean
```

Unregisters an [AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityStateChangeListener](../android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener.md):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener was previously registered. |

### removeAudioDescriptionRequestedChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAudioDescriptionRequestedChangeListener(listener: AccessibilityManager.AudioDescriptionRequestedChangeListener): Boolean
```

Unregisters a [AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AudioDescriptionRequestedChangeListener](../android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener.md):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if listener was previously registered. |

### removeHighContrastTextStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeHighContrastTextStateChangeListener(listener: AccessibilityManager.HighContrastTextStateChangeListener): Unit
```

Unregisters a [HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.HighContrastTextStateChangeListener](../android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener.md):The listener. This value cannot be`null`. |

### removeTouchExplorationStateChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeTouchExplorationStateChangeListener(listener: AccessibilityManager.TouchExplorationStateChangeListener): Boolean
```

Unregisters a [TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.TouchExplorationStateChangeListener](../android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener.md):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if listener was previously registered. |

### sendAccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendAccessibilityEvent(event: AccessibilityEvent!): Unit
```

Sends an [AccessibilityEvent](AccessibilityEvent.md).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](AccessibilityEvent.md)!:The event to send. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if accessibility is not enabled.**Note:** The preferred mechanism for sending custom accessibility events is through calling [android.view.ViewParent#requestSendAccessibilityEvent(View, AccessibilityEvent)](../android.view/ViewParent.md))instead of this method to allow predecessors to augment/filter events sent by their descendants. |

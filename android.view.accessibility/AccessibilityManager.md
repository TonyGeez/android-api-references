# AccessibilityManager

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibilityManager

Kotlin| [Java](https://developer.android.com/reference/android/view/accessibility/AccessibilityManager "View this page in Java") 
| --- | --- |

```
class AccessibilityManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.accessibility.AccessibilityManager](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#) |

System level service that serves as an event dispatch for [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent) s, and provides facilities for querying the accessibility state of the system. Accessibility events are generated when something notable happens in the user interface, for example an [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) starts, the focus or selection of a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#) changes etc. Parties interested in handling accessibility events implement and register an accessibility service which extends [android.accessibilityservice.AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#).

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener) Listener for changes to the state of accessibility services. |
| abstract | [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener) Listener for the system accessibility state. |
| abstract | [AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener) Listener for the audio description by default state. |
| --- | --- |
| abstract | [HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener) Listener for the system high contrast text state. |
| abstract | [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener) Listener for the system touch exploration state. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CONTENT_CONTROLS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_CONTROLS:kotlin.Int) Use this flag to indicate the content of a UI that times out contains interactive controls. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CONTENT_ICONS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_ICONS:kotlin.Int) Use this flag to indicate the content of a UI that times out contains icons. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CONTENT_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_TEXT:kotlin.Int) Use this flag to indicate the content of a UI that times out contains text. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAccessibilityRequestPreparer(android.view.accessibility.AccessibilityRequestPreparer))`(`preparer:` ` [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer)!`)` Registers a [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAccessibilityServicesStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityServicesStateChangeListener))`(`listener:` ` [AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener)`)` Registers a [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAccessibilityServicesStateChangeListener(java.util.concurrent.Executor,%20android.view.accessibility.AccessibilityManager.AccessibilityServicesStateChangeListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener)`)` Registers a [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAccessibilityStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener))`(`listener:` ` [AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener)`)` Registers an [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener) for changes in the global accessibility state of the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAccessibilityStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener,%20android.os.Handler))`(`listener:` ` [AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Registers an [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener) for changes in the global accessibility state of the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addAudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAudioDescriptionRequestedChangeListener(java.util.concurrent.Executor,%20android.view.accessibility.AccessibilityManager.AudioDescriptionRequestedChangeListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [AccessibilityManager.AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener)`)` Registers a [AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener) for changes in the audio description by default state of the system. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addHighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addHighContrastTextStateChangeListener(java.util.concurrent.Executor,%20android.view.accessibility.AccessibilityManager.HighContrastTextStateChangeListener))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `listener:` ` [AccessibilityManager.HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener)`)` Registers a [HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener) for changes in the global high contrast text state of the system. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addTouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addTouchExplorationStateChangeListener(android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener))`(`listener:` ` [AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener)`)` Registers a [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener) for changes in the global touch exploration state of the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addTouchExplorationStateChangeListener(android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener,%20android.os.Handler))`(`listener:` ` [AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Registers an [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener) for changes in the global touch exploration state of the system. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccessibilityFocusColor](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getAccessibilityFocusColor())`()` Gets the color of the focus rectangle. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAccessibilityFocusStrokeWidth](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getAccessibilityFocusStrokeWidth())`()` Gets the strokeWidth of the focus rectangle. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#)!\>! | [getAccessibilityServiceList](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getAccessibilityServiceList())`()` Returns the [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#) s of the installed accessibility services. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#)!\>! | [getEnabledAccessibilityServiceList](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getEnabledAccessibilityServiceList(kotlin.Int))`(`feedbackTypeFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#) s of the enabled accessibility services for a given feedback type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#)!\>! | [getInstalledAccessibilityServiceList](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getInstalledAccessibilityServiceList())`()` Returns the [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#) s of the installed accessibility services. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecommendedTimeoutMillis](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getRecommendedTimeoutMillis(kotlin.Int,%20kotlin.Int))`(`originalTimeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uiContentFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the recommended timeout for changes to the UI needed by this user. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [interrupt](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#interrupt())`()` Requests feedback interruption from all accessibility services. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessibilityButtonSupported](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isAccessibilityButtonSupported())`()` Determines if the accessibility button within the system navigation area is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAudioDescriptionRequested](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isAudioDescriptionRequested())`()` Determines if users want to select sound track with audio description by default. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isEnabled())`()` Returns if the accessibility in the system is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHighContrastTextEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isHighContrastTextEnabled())`()` Returns if high contrast text in the system is enabled. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRequestFromAccessibilityTool](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isRequestFromAccessibilityTool())`()` Whether the current accessibility request comes from an [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) with the [AccessibilityServiceInfo.isAccessibilityTool](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool())property set to true. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTouchExplorationEnabled](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isTouchExplorationEnabled())`()` Returns if the touch exploration in the system is enabled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#removeAccessibilityRequestPreparer(android.view.accessibility.AccessibilityRequestPreparer))`(`preparer:` ` [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer)!`)` Unregisters a [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#removeAccessibilityServicesStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityServicesStateChangeListener))`(`listener:` ` [AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener)`)` Unregisters a [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#removeAccessibilityStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener))`(`listener:` ` [AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener)`)` Unregisters an [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#removeAudioDescriptionRequestedChangeListener(android.view.accessibility.AccessibilityManager.AudioDescriptionRequestedChangeListener))`(`listener:` ` [AccessibilityManager.AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener)`)` Unregisters a [AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeHighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#removeHighContrastTextStateChangeListener(android.view.accessibility.AccessibilityManager.HighContrastTextStateChangeListener))`(`listener:` ` [AccessibilityManager.HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener)`)` Unregisters a [HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeTouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#removeTouchExplorationStateChangeListener(android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener))`(`listener:` ` [AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener)`)` Unregisters a [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendAccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#sendAccessibilityEvent(android.view.accessibility.AccessibilityEvent))`(`event:` ` [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent)!`)` Sends an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent). |

## Constants

### FLAG_CONTENT_CONTROLS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CONTENT_CONTROLS: Int
```

Use this flag to indicate the content of a UI that times out contains interactive controls. 

 Value: 4

**See Also**

- [#getRecommendedTimeoutMillis(int, int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getRecommendedTimeoutMillis(kotlin.Int,%20kotlin.Int)) 

### FLAG_CONTENT_ICONS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CONTENT_ICONS: Int
```

Use this flag to indicate the content of a UI that times out contains icons. 

 Value: 1

**See Also**

- [#getRecommendedTimeoutMillis(int, int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getRecommendedTimeoutMillis(kotlin.Int,%20kotlin.Int)) 

### FLAG_CONTENT_TEXT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CONTENT_TEXT: Int
```

Use this flag to indicate the content of a UI that times out contains text. 

 Value: 2

**See Also**

- [#getRecommendedTimeoutMillis(int, int)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getRecommendedTimeoutMillis(kotlin.Int,%20kotlin.Int))

## Public methods

### addAccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityRequestPreparer(preparer: AccessibilityRequestPreparer!): Unit
```

Registers a [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer). 

### addAccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityServicesStateChangeListener(listener: AccessibilityManager.AccessibilityServicesStateChangeListener): Unit
```

Registers a [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener). This will execute a callback on the process's main handler.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener):The listener. This value cannot be`null`. |

### addAccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityServicesStateChangeListener(
    executor: Executor, 
    listener: AccessibilityManager.AccessibilityServicesStateChangeListener
): Unit
```

Registers a [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener):The listener. This value cannot be`null`. |

### addAccessibilityStateChangeListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAccessibilityStateChangeListener(listener: AccessibilityManager.AccessibilityStateChangeListener): Boolean
```

Registers an [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener) for changes in the global accessibility state of the system. Equivalent to calling [addAccessibilityStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAccessibilityStateChangeListener(android.view.accessibility.AccessibilityManager.AccessibilityStateChangeListener,%20android.os.Handler))with a null handler.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener):The listener. This value cannot be`null`. |

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

Registers an [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener) for changes in the global accessibility state of the system. If the listener has already been registered, the handler used to call it back is updated.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener):The listener. This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The handler on which the listener should be called back, or`null`for a callback on the process's main handler. |

### addAudioDescriptionRequestedChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAudioDescriptionRequestedChangeListener(
    executor: Executor, 
    listener: AccessibilityManager.AudioDescriptionRequestedChangeListener
): Unit
```

Registers a [AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener) for changes in the audio description by default state of the system. The value could be read via [isAudioDescriptionRequested](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#isAudioDescriptionRequested()).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The executor on which the listener should be called back. This value cannot be`null`. |
| `listener` | [AccessibilityManager.AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener):The listener. This value cannot be`null`. |

### addHighContrastTextStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addHighContrastTextStateChangeListener(
    executor: Executor, 
    listener: AccessibilityManager.HighContrastTextStateChangeListener
): Unit
```

Registers a [HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener) for changes in the global high contrast text state of the system.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):a executor to call the listener from This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `listener` | [AccessibilityManager.HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener):The listener to be called This value cannot be`null`. |

### addTouchExplorationStateChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addTouchExplorationStateChangeListener(listener: AccessibilityManager.TouchExplorationStateChangeListener): Boolean
```

Registers a [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener) for changes in the global touch exploration state of the system. Equivalent to calling [addTouchExplorationStateChangeListener(android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addTouchExplorationStateChangeListener(android.view.accessibility.AccessibilityManager.TouchExplorationStateChangeListener,%20android.os.Handler))with a null handler.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener):The listener. This value cannot be`null`. |

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

Registers an [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener) for changes in the global touch exploration state of the system. If the listener has already been registered, the handler used to call it back is updated.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener):The listener. This value cannot be`null`. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The handler on which the listener should be called back, or`null`for a callback on the process's main handler. |

### getAccessibilityFocusColor

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessibilityFocusColor(): Int
```

Gets the color of the focus rectangle. This value can be set by [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color of the focus rectangle. |

### getAccessibilityFocusStrokeWidth

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessibilityFocusStrokeWidth(): Int
```

Gets the strokeWidth of the focus rectangle. This value can be set by [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The strokeWidth of the focus rectangle in pixels. |

### getAccessibilityServiceList

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessibilityServiceList(): MutableList<ServiceInfo!>!
```

**Deprecated:** *Use [getInstalledAccessibilityServiceList()](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#getInstalledAccessibilityServiceList())*

Returns the [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#) s of the installed accessibility services.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#)!>! | An unmodifiable list with [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#) s. |

### getEnabledAccessibilityServiceList

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEnabledAccessibilityServiceList(feedbackTypeFlags: Int): MutableList<AccessibilityServiceInfo!>!
```

Returns the [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#) s of the enabled accessibility services for a given feedback type.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------|
| `feedbackTypeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The feedback type flags. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#)!>! | An unmodifiable list with [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#) s. |

**See Also**

- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_AUDIBLE](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FEEDBACK_AUDIBLE:kotlin.Int)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_GENERIC](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FEEDBACK_GENERIC:kotlin.Int)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_HAPTIC](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FEEDBACK_HAPTIC:kotlin.Int)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_SPOKEN](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FEEDBACK_SPOKEN:kotlin.Int)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_VISUAL](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FEEDBACK_VISUAL:kotlin.Int)
- [android.accessibilityservice.AccessibilityServiceInfo#FEEDBACK_BRAILLE](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#FEEDBACK_BRAILLE:kotlin.Int) 

### getInstalledAccessibilityServiceList

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInstalledAccessibilityServiceList(): MutableList<AccessibilityServiceInfo!>!
```

Returns the [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#) s of the installed accessibility services.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#)!>! | An unmodifiable list with [AccessibilityServiceInfo](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#) s. |

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
| `uiContentFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The combination of flags [FLAG_CONTENT_ICONS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_ICONS:kotlin.Int), [FLAG_CONTENT_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_TEXT:kotlin.Int) or [FLAG_CONTENT_CONTROLS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_CONTROLS:kotlin.Int) to indicate the contents of UI. Value is either`0`or a combination of [android.view.accessibility.AccessibilityManager#FLAG_CONTENT_ICONS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_ICONS:kotlin.Int), [android.view.accessibility.AccessibilityManager#FLAG_CONTENT_TEXT](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_TEXT:kotlin.Int), and [android.view.accessibility.AccessibilityManager#FLAG_CONTENT_CONTROLS](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#FLAG_CONTENT_CONTROLS:kotlin.Int) |

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

Add listener to detect the state change via [addAudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager#addAudioDescriptionRequestedChangeListener(java.util.concurrent.Executor,%20android.view.accessibility.AccessibilityManager.AudioDescriptionRequestedChangeListener))

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the audio description is enabled,`false`otherwise. |

### isEnabled

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnabled(): Boolean
```

Returns if the accessibility in the system is enabled.

**Note:** This query is used for sending [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent) s, since events are only needed if accessibility is on. Avoid changing UI or app behavior based on the state of accessibility. While well-intentioned, doing this creates brittle, less well-maintained code that works for some users but not others. Shared code leads to more equitable experiences and less technical debt.

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

Whether the current accessibility request comes from an [AccessibilityService](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityService.html#) with the [AccessibilityServiceInfo.isAccessibilityTool](https://developer.android.com/reference/kotlin/android/accessibilityservice/AccessibilityServiceInfo.html#isAccessibilityTool())property set to true.

You can use this method inside [AccessibilityNodeProvider](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeProvider) to decide how to populate your nodes.

**Note:** The return value is valid only when an [AccessibilityNodeInfo](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityNodeInfo) request is in progress, can change from one request to another, and has no meaning when a request is not in progress.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the current request is from a tool that sets isAccessibilityTool. |

### isTouchExplorationEnabled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isTouchExplorationEnabled(): Boolean
```

Returns if the touch exploration in the system is enabled.

**Note:** This query is used for dispatching hover events, such as [android.view.MotionEvent#ACTION_HOVER_ENTER](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_HOVER_ENTER:kotlin.Int), to accessibility services to manage touch exploration. Avoid changing UI or app behavior based on the state of accessibility. While well-intentioned, doing this creates brittle, less well-maintained code that works for som users but not others. Shared code leads to more equitable experiences and less technical debt.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if touch exploration is enabled, false otherwise. |

### removeAccessibilityRequestPreparer

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAccessibilityRequestPreparer(preparer: AccessibilityRequestPreparer!): Unit
```

Unregisters a [AccessibilityRequestPreparer](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityRequestPreparer). 

### removeAccessibilityServicesStateChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAccessibilityServicesStateChangeListener(listener: AccessibilityManager.AccessibilityServicesStateChangeListener): Boolean
```

Unregisters a [AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityServicesStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityServicesStateChangeListener):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the listener was previously registered. |

### removeAccessibilityStateChangeListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAccessibilityStateChangeListener(listener: AccessibilityManager.AccessibilityStateChangeListener): Boolean
```

Unregisters an [AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AccessibilityStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AccessibilityStateChangeListener):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener was previously registered. |

### removeAudioDescriptionRequestedChangeListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAudioDescriptionRequestedChangeListener(listener: AccessibilityManager.AudioDescriptionRequestedChangeListener): Boolean
```

Unregisters a [AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.AudioDescriptionRequestedChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.AudioDescriptionRequestedChangeListener):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if listener was previously registered. |

### removeHighContrastTextStateChangeListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeHighContrastTextStateChangeListener(listener: AccessibilityManager.HighContrastTextStateChangeListener): Unit
```

Unregisters a [HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.HighContrastTextStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.HighContrastTextStateChangeListener):The listener. This value cannot be`null`. |

### removeTouchExplorationStateChangeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeTouchExplorationStateChangeListener(listener: AccessibilityManager.TouchExplorationStateChangeListener): Boolean
```

Unregisters a [TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AccessibilityManager.TouchExplorationStateChangeListener](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityManager.TouchExplorationStateChangeListener):The listener. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if listener was previously registered. |

### sendAccessibilityEvent

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendAccessibilityEvent(event: AccessibilityEvent!): Unit
```

Sends an [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [AccessibilityEvent](https://developer.android.com/reference/kotlin/android/view/accessibility/AccessibilityEvent)!:The event to send. |

| Exceptions ||
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if accessibility is not enabled.**Note:** The preferred mechanism for sending custom accessibility events is through calling [android.view.ViewParent#requestSendAccessibilityEvent(View, AccessibilityEvent)](https://developer.android.com/reference/kotlin/android/view/ViewParent.html#requestSendAccessibilityEvent(android.view.View,%20android.view.accessibility.AccessibilityEvent))instead of this method to allow predecessors to augment/filter events sent by their descendants. |

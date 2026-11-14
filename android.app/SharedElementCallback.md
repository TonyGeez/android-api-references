# SharedElementCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SharedElementCallback

Kotlin| [Java](../android/app/SharedElementCallback.md) 
| --- | --- |

```
abstract class SharedElementCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.SharedElementCallback](../android/app/SharedElementCallback.md) |

Listener provided in [Activity.setEnterSharedElementCallback(SharedElementCallback)](../android/app/Activity.md))and [Activity.setExitSharedElementCallback(SharedElementCallback)](../android/app/Activity.md))as well as [Fragment.setEnterSharedElementCallback(SharedElementCallback)](../android/app/Fragment.md))and [Fragment.setExitSharedElementCallback(SharedElementCallback)](../android/app/Fragment.md))to monitor the Shared element transitions. The events can be used to customize Activity and Fragment Transition behavior.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnSharedElementsReadyListener](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md) Listener to be called after [android.app.SharedElementCallback#onSharedElementsArrived(java.util.List,java.util.List,android.app.SharedElementCallback.OnSharedElementsReadyListener)](../android/app/SharedElementCallback.md))when the shared elements are ready to be hidden in the source Activity and shown in the destination Activity. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SharedElementCallback](../android/app/SharedElementCallback.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Parcelable](../android/os/Parcelable.md)! | [onCaptureSharedElementSnapshot](../android/app/SharedElementCallback.md))`(`sharedElement:` ` [View](../android/view/View.md)!`, `viewToGlobalMatrix:` ` [Matrix](../android/graphics/Matrix.md)!`, `screenBounds:` ` [RectF](../android/graphics/RectF.md)!`)` Creates a snapshot of a shared element to be used by the remote Activity and reconstituted with [onCreateSnapshotView(android.content.Context,android.os.Parcelable)](../android/app/SharedElementCallback.md)). |
| open [View](../android/view/View.md)! | [onCreateSnapshotView](../android/app/SharedElementCallback.md))`(`context:` ` [Context](../android/content/Context.md)!`, `snapshot:` ` [Parcelable](../android/os/Parcelable.md)!`)` Reconstitutes a snapshot View from a Parcelable returned in [onCaptureSharedElementSnapshot(android.view.View,android.graphics.Matrix,android.graphics.RectF)](../android/app/SharedElementCallback.md))to be used in [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))and [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMapSharedElements](../android/app/SharedElementCallback.md))`(`names:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sharedElements:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [View](../android/view/View.md)!>!`)` Lets the SharedElementCallback adjust the mapping of shared element names to Views. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRejectSharedElements](../android/app/SharedElementCallback.md))`(`rejectedSharedElements:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android/view/View.md)!>!`)` Called after [onMapSharedElements(java.util.List,java.util.Map)](../android/app/SharedElementCallback.md))when transferring shared elements in. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSharedElementEnd](../android/app/SharedElementCallback.md))`(`sharedElementNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sharedElements:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android/view/View.md)!>!`, `sharedElementSnapshots:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android/view/View.md)!>!`)` In Activity Transitions, onSharedElementEnd is called immediately before capturing the end of the shared element state on enter and reenter transitions and immediately before capturing the start of the shared element state for exit and return transitions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSharedElementStart](../android/app/SharedElementCallback.md))`(`sharedElementNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sharedElements:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android/view/View.md)!>!`, `sharedElementSnapshots:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android/view/View.md)!>!`)` In Activity Transitions, onSharedElementStart is called immediately before capturing the start of the shared element state on enter and reenter transitions and immediately before capturing the end of the shared element state for exit and return transitions. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSharedElementsArrived](../android/app/SharedElementCallback.md))`(`sharedElementNames:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `sharedElements:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [View](../android/view/View.md)!>!`, `listener:` ` [SharedElementCallback.OnSharedElementsReadyListener](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md)!`)` Called during an Activity Transition when the shared elements have arrived at the final location and are ready to be transferred. |

## Public constructors

### SharedElementCallback

```
SharedElementCallback()
```

## Public methods

### onCaptureSharedElementSnapshot

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCaptureSharedElementSnapshot(
    sharedElement: View!, 
    viewToGlobalMatrix: Matrix!, 
    screenBounds: RectF!
): Parcelable!
```

Creates a snapshot of a shared element to be used by the remote Activity and reconstituted with [onCreateSnapshotView(android.content.Context,android.os.Parcelable)](../android/app/SharedElementCallback.md)). A null return value will mean that the remote Activity will have a null snapshot View in [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))and [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)).

This is not called for Fragment Transitions.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedElement` | [View](../android/view/View.md)!:The shared element View to create a snapshot for. |
| `viewToGlobalMatrix` | [Matrix](../android/graphics/Matrix.md)!:A matrix containing a transform from the view to the screen coordinates. |
| `screenBounds` | [RectF](../android/graphics/RectF.md)!:The bounds of shared element in screen coordinate space. This is the bounds of the view with the viewToGlobalMatrix applied. |
| --- | --- |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Parcelable](../android/os/Parcelable.md)! | A snapshot to send to the remote Activity to be reconstituted with [onCreateSnapshotView(android.content.Context,android.os.Parcelable)](../android/app/SharedElementCallback.md))and passed into [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))and [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)). |

### onCreateSnapshotView

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateSnapshotView(
    context: Context!, 
    snapshot: Parcelable!
): View!
```

Reconstitutes a snapshot View from a Parcelable returned in [onCaptureSharedElementSnapshot(android.view.View,android.graphics.Matrix,android.graphics.RectF)](../android/app/SharedElementCallback.md))to be used in [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))and [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)). The returned View will be sized and positioned after this call so that it is ready to be added to the decor View's overlay.

This is not called for Fragment Transitions.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context used to create the snapshot View. |
| `snapshot` | [Parcelable](../android/os/Parcelable.md)!:The Parcelable returned by [onCaptureSharedElementSnapshot(android.view.View,android.graphics.Matrix,android.graphics.RectF)](../android/app/SharedElementCallback.md)). |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)! | A View to be sent in [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))and [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)). A null value will produce a null snapshot value for those two methods. |

### onMapSharedElements

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMapSharedElements(
    names: MutableList<String!>!, 
    sharedElements: MutableMap<String!, View!>!
): Unit
```

Lets the SharedElementCallback adjust the mapping of shared element names to Views.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `names` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The names of all shared elements transferred from the calling Activity or Fragment in the order they were provided. |
| `sharedElements` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [View](../android/view/View.md)!\>!:The mapping of shared element names to Views. The best guess will be filled into sharedElements based on the transitionNames. |

### onRejectSharedElements

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRejectSharedElements(rejectedSharedElements: MutableList<View!>!): Unit
```

Called after [onMapSharedElements(java.util.List,java.util.Map)](../android/app/SharedElementCallback.md))when transferring shared elements in. Any shared elements that have no mapping will be in rejectedSharedElements. The elements remaining in rejectedSharedElements will be transitioned out of the Scene. If a View is removed from rejectedSharedElements, it must be handled by the`SharedElementCallback`.

Views in rejectedSharedElements will have their position and size set to the position of the calling shared element, relative to the Window decor View and contain snapshots of the View from the calling Activity or Fragment. This view may be safely added to the decor View's overlay to remain in position.

This method is not called for Fragment Transitions. All rejected shared elements will be handled by the exit transition.

| Parameters ||
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rejectedSharedElements` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android/view/View.md)!\>!:Views containing visual information of shared elements that are not part of the entering scene. These Views are positioned relative to the Window decor View. A View removed from this list will not be transitioned automatically. |

### onSharedElementEnd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSharedElementEnd(
    sharedElementNames: MutableList<String!>!, 
    sharedElements: MutableList<View!>!, 
    sharedElementSnapshots: MutableList<View!>!
): Unit
```

In Activity Transitions, onSharedElementEnd is called immediately before capturing the end of the shared element state on enter and reenter transitions and immediately before capturing the start of the shared element state for exit and return transitions.

In Fragment Transitions, onSharedElementEnd is called immediately before capturing the end state of all shared element transitions.

This call can be used to adjust the transition end state by modifying the shared element Views. Note that no layout step will be executed between onSharedElementEnd and the transition state capture.

Any changes made in [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))that are not updated during layout should be corrected in onSharedElementEnd. For example, rotation or scale will not be affected by layout and if changed in [onSharedElementStart(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)), it will also have to be reset in onSharedElementEnd again to correct the end state.

| Parameters ||
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedElementNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The names of the shared elements that were accepted into the View hierarchy. |
| `sharedElements` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android/view/View.md)!\>!:The shared elements that are part of the View hierarchy. |
| `sharedElementSnapshots` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android/view/View.md)!\>!:The Views containing snap shots of the shared element from the launching Window. These elements will not be part of the scene, but will be positioned relative to the Window decor View. This list will be null for Fragment Transitions. |
| --- | --- |

### onSharedElementStart

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSharedElementStart(
    sharedElementNames: MutableList<String!>!, 
    sharedElements: MutableList<View!>!, 
    sharedElementSnapshots: MutableList<View!>!
): Unit
```

In Activity Transitions, onSharedElementStart is called immediately before capturing the start of the shared element state on enter and reenter transitions and immediately before capturing the end of the shared element state for exit and return transitions.

In Fragment Transitions, onSharedElementStart is called immediately before capturing the start state of all shared element transitions.

This call can be used to adjust the transition start state by modifying the shared element Views. Note that no layout step will be executed between onSharedElementStart and the transition state capture.

For Activity Transitions, any changes made in [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md))that are not updated during by layout should be corrected in onSharedElementStart for exit and return transitions. For example, rotation or scale will not be affected by layout and if changed in [onSharedElementEnd(java.util.List,java.util.List,java.util.List)](../android/app/SharedElementCallback.md)), it will also have to be reset in onSharedElementStart again to correct the end state.

| Parameters ||
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedElementNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The names of the shared elements that were accepted into the View hierarchy. |
| `sharedElements` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android/view/View.md)!\>!:The shared elements that are part of the View hierarchy. |
| `sharedElementSnapshots` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android/view/View.md)!\>!:The Views containing snap shots of the shared element from the launching Window. These elements will not be part of the scene, but will be positioned relative to the Window decor View. This list is null for Fragment Transitions. |
| --- | --- |

### onSharedElementsArrived

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSharedElementsArrived(
    sharedElementNames: MutableList<String!>!, 
    sharedElements: MutableList<View!>!, 
    listener: SharedElementCallback.OnSharedElementsReadyListener!
): Unit
```

Called during an Activity Transition when the shared elements have arrived at the final location and are ready to be transferred. This method is called for both the source and destination Activities.

When the shared elements are ready to be transferred, [OnSharedElementsReadyListener.onSharedElementsReady()](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md))must be called to trigger the transfer.

The default behavior is to trigger the transfer immediately.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedElementNames` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The names of the shared elements that are being transferred.. |
| `sharedElements` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](../android/view/View.md)!\>!:The shared elements that are part of the View hierarchy. |
| `listener` | [SharedElementCallback.OnSharedElementsReadyListener](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md)!:The listener to call when the shared elements are ready to be hidden in the source Activity or shown in the destination Activity. |
| --- | --- |

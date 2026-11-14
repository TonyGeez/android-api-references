# android.transition

# android.transition

Kotlin| [Java](../android/transition/_package.md)
| --- | --- |

## Interfaces

| [TransitionListener](../android/transition/Transition.TransitionListener.md) | A transition listener receives notifications from a transition. |
| --- | --- |

## Classes

| [ArcMotion](../android/transition/ArcMotion.md) | A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. |
| --- | --- |
| [AutoTransition](../android/transition/AutoTransition.md) | Utility class for creating a default transition that automatically fades, moves, and resizes views during a scene change. |
| [ChangeBounds](../android/transition/ChangeBounds.md) | This transition captures the layout bounds of target views before and after the scene change and animates those changes during the transition. |
| [ChangeClipBounds](../android/transition/ChangeClipBounds.md) | ChangeClipBounds captures the [android.view.View#getClipBounds()](../android/view/View.md))before and after the scene change and animates those changes during the transition. |
| --- | --- |
| [ChangeImageTransform](../android/transition/ChangeImageTransform.md) | This Transition captures an ImageView's matrix before and after the scene change and animates it during the transition. |
| [ChangeScroll](../android/transition/ChangeScroll.md) | This transition captures the scroll properties of targets before and after the scene change and animates any changes. |
| [ChangeTransform](../android/transition/ChangeTransform.md) | This Transition captures scale and rotation for Views before and after the scene change and animates those changes during the transition. |
| --- | --- |
| [CircularPropagation](../android/transition/CircularPropagation.md) | A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. |
| [Explode](../android/transition/Explode.md) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from the edges of the scene. |
| [Fade](../android/transition/Fade.md) | This transition tracks changes to the visibility of target views in the start and end scenes and fades views in or out when they become visible or non-visible. |
| --- | --- |
| [PathMotion](../android/transition/PathMotion.md) | This base class can be extended to provide motion along a Path to Transitions. |
| [PatternPathMotion](../android/transition/PatternPathMotion.md) | A PathMotion that takes a Path pattern and applies it to the separation between two points. |
| [Scene](../android/transition/Scene.md) | A scene represents the collection of values that various properties in the View hierarchy will have when the scene is applied. |
| --- | --- |
| [SidePropagation](../android/transition/SidePropagation.md) | A`TransitionPropagation`that propagates based on the distance to the side and, orthogonally, the distance to epicenter. |
| [Slide](../android/transition/Slide.md) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from one of the edges of the scene. |
| [Transition](../android/transition/Transition.md) | A Transition holds information about animations that will be run on its targets during a scene change. |
| --- | --- |
| [TransitionInflater](../android/transition/TransitionInflater.md) | This class inflates scenes and transitions from resource files. |
| [TransitionListenerAdapter](../android/transition/TransitionListenerAdapter.md) | This adapter class provides empty implementations of the methods from . |
| [TransitionManager](../android/transition/TransitionManager.md) | This class manages the set of transitions that fire when there is a change of [Scene](../android/transition/Scene.md). |
| --- | --- |
| [TransitionPropagation](../android/transition/TransitionPropagation.md) | Extend`TransitionPropagation`to customize start delays for Animators created in [android.transition.Transition#createAnimator(ViewGroup, * TransitionValues, TransitionValues)](../android/transition/Transition.md)). |
| [TransitionSet](../android/transition/TransitionSet.md) | A TransitionSet is a parent of child transitions (including other TransitionSets). |
| [TransitionValues](../android/transition/TransitionValues.md) | Data structure which holds cached values for the transition. |
| --- | --- |
| [Visibility](../android/transition/Visibility.md) | This transition tracks changes to the visibility of target views in the start and end scenes. |
| [VisibilityPropagation](../android/transition/VisibilityPropagation.md) | Base class for`TransitionPropagation`s that care about View Visibility and the center position of the View. |

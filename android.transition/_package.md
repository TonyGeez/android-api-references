# android.transition

# android.transition

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [TransitionListener](../android/transition/Transition.TransitionListener.md) | A transition listener receives notifications from a transition. |
| --- | --- |

## Classes

| [ArcMotion](ArcMotion.md) | A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. |
| --- | --- |
| [AutoTransition](AutoTransition.md) | Utility class for creating a default transition that automatically fades, moves, and resizes views during a scene change. |
| [ChangeBounds](ChangeBounds.md) | This transition captures the layout bounds of target views before and after the scene change and animates those changes during the transition. |
| [ChangeClipBounds](ChangeClipBounds.md) | ChangeClipBounds captures the [android.view.View#getClipBounds()](../android.view/View.md))before and after the scene change and animates those changes during the transition. |
| --- | --- |
| [ChangeImageTransform](ChangeImageTransform.md) | This Transition captures an ImageView's matrix before and after the scene change and animates it during the transition. |
| [ChangeScroll](ChangeScroll.md) | This transition captures the scroll properties of targets before and after the scene change and animates any changes. |
| [ChangeTransform](ChangeTransform.md) | This Transition captures scale and rotation for Views before and after the scene change and animates those changes during the transition. |
| --- | --- |
| [CircularPropagation](CircularPropagation.md) | A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. |
| [Explode](Explode.md) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from the edges of the scene. |
| [Fade](Fade.md) | This transition tracks changes to the visibility of target views in the start and end scenes and fades views in or out when they become visible or non-visible. |
| --- | --- |
| [PathMotion](PathMotion.md) | This base class can be extended to provide motion along a Path to Transitions. |
| [PatternPathMotion](PatternPathMotion.md) | A PathMotion that takes a Path pattern and applies it to the separation between two points. |
| [Scene](Scene.md) | A scene represents the collection of values that various properties in the View hierarchy will have when the scene is applied. |
| --- | --- |
| [SidePropagation](SidePropagation.md) | A`TransitionPropagation`that propagates based on the distance to the side and, orthogonally, the distance to epicenter. |
| [Slide](Slide.md) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from one of the edges of the scene. |
| [Transition](Transition.md) | A Transition holds information about animations that will be run on its targets during a scene change. |
| --- | --- |
| [TransitionInflater](TransitionInflater.md) | This class inflates scenes and transitions from resource files. |
| [TransitionListenerAdapter](TransitionListenerAdapter.md) | This adapter class provides empty implementations of the methods from . |
| [TransitionManager](TransitionManager.md) | This class manages the set of transitions that fire when there is a change of [Scene](Scene.md). |
| --- | --- |
| [TransitionPropagation](TransitionPropagation.md) | Extend`TransitionPropagation`to customize start delays for Animators created in [android.transition.Transition#createAnimator(ViewGroup, * TransitionValues, TransitionValues)](Transition.md)). |
| [TransitionSet](TransitionSet.md) | A TransitionSet is a parent of child transitions (including other TransitionSets). |
| [TransitionValues](TransitionValues.md) | Data structure which holds cached values for the transition. |
| --- | --- |
| [Visibility](Visibility.md) | This transition tracks changes to the visibility of target views in the start and end scenes. |
| [VisibilityPropagation](VisibilityPropagation.md) | Base class for`TransitionPropagation`s that care about View Visibility and the center position of the View. |

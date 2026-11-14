# android.transition

# android.transition

Kotlin| [Java](https://developer.android.com/reference/android/transition/package-summary "View this page in Java")

## Interfaces

| [TransitionListener](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener) | A transition listener receives notifications from a transition. |

## Classes

| [ArcMotion](https://developer.android.com/reference/kotlin/android/transition/ArcMotion) | A PathMotion that generates a curved path along an arc on an imaginary circle containing the two points. |
| [AutoTransition](https://developer.android.com/reference/kotlin/android/transition/AutoTransition) | Utility class for creating a default transition that automatically fades, moves, and resizes views during a scene change. |
| [ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds) | This transition captures the layout bounds of target views before and after the scene change and animates those changes during the transition. |
| [ChangeClipBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeClipBounds) | ChangeClipBounds captures the [android.view.View#getClipBounds()](https://developer.android.com/reference/kotlin/android/view/View.html#getClipBounds())before and after the scene change and animates those changes during the transition. |
| [ChangeImageTransform](https://developer.android.com/reference/kotlin/android/transition/ChangeImageTransform) | This Transition captures an ImageView's matrix before and after the scene change and animates it during the transition. |
| [ChangeScroll](https://developer.android.com/reference/kotlin/android/transition/ChangeScroll) | This transition captures the scroll properties of targets before and after the scene change and animates any changes. |
| [ChangeTransform](https://developer.android.com/reference/kotlin/android/transition/ChangeTransform) | This Transition captures scale and rotation for Views before and after the scene change and animates those changes during the transition. |
| [CircularPropagation](https://developer.android.com/reference/kotlin/android/transition/CircularPropagation) | A propagation that varies with the distance to the epicenter of the Transition or center of the scene if no epicenter exists. |
| [Explode](https://developer.android.com/reference/kotlin/android/transition/Explode) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from the edges of the scene. |
| [Fade](https://developer.android.com/reference/kotlin/android/transition/Fade) | This transition tracks changes to the visibility of target views in the start and end scenes and fades views in or out when they become visible or non-visible. |
| [PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion) | This base class can be extended to provide motion along a Path to Transitions. |
| [PatternPathMotion](https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion) | A PathMotion that takes a Path pattern and applies it to the separation between two points. |
| [Scene](https://developer.android.com/reference/kotlin/android/transition/Scene) | A scene represents the collection of values that various properties in the View hierarchy will have when the scene is applied. |
| [SidePropagation](https://developer.android.com/reference/kotlin/android/transition/SidePropagation) | A`TransitionPropagation`that propagates based on the distance to the side and, orthogonally, the distance to epicenter. |
| [Slide](https://developer.android.com/reference/kotlin/android/transition/Slide) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from one of the edges of the scene. |
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition) | A Transition holds information about animations that will be run on its targets during a scene change. |
| [TransitionInflater](https://developer.android.com/reference/kotlin/android/transition/TransitionInflater) | This class inflates scenes and transitions from resource files. |
| [TransitionListenerAdapter](https://developer.android.com/reference/kotlin/android/transition/TransitionListenerAdapter) | This adapter class provides empty implementations of the methods from . |
| [TransitionManager](https://developer.android.com/reference/kotlin/android/transition/TransitionManager) | This class manages the set of transitions that fire when there is a change of [Scene](https://developer.android.com/reference/kotlin/android/transition/Scene). |
| [TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation) | Extend`TransitionPropagation`to customize start delays for Animators created in [android.transition.Transition#createAnimator(ViewGroup, * TransitionValues, TransitionValues)](https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)). |
| [TransitionSet](https://developer.android.com/reference/kotlin/android/transition/TransitionSet) | A TransitionSet is a parent of child transitions (including other TransitionSets). |
| [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues) | Data structure which holds cached values for the transition. |
| [Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility) | This transition tracks changes to the visibility of target views in the start and end scenes. |
| [VisibilityPropagation](https://developer.android.com/reference/kotlin/android/transition/VisibilityPropagation) | Base class for`TransitionPropagation`s that care about View Visibility and the center position of the View. |

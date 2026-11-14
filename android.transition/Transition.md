Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transition

Kotlin | [Java](https://developer.android.com/reference/android/transition/Transition "View this page in Java")
| --- | --- |

```
abstract class Transition : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#) |

| Known Direct Subclasses [ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds), [ChangeClipBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeClipBounds), [ChangeImageTransform](https://developer.android.com/reference/kotlin/android/transition/ChangeImageTransform), [ChangeScroll](https://developer.android.com/reference/kotlin/android/transition/ChangeScroll), [ChangeTransform](https://developer.android.com/reference/kotlin/android/transition/ChangeTransform), [TransitionSet](https://developer.android.com/reference/kotlin/android/transition/TransitionSet), [Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility) |---|---| | [ChangeBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeBounds) | This transition captures the layout bounds of target views before and after the scene change and animates those changes during the transition. | | [ChangeClipBounds](https://developer.android.com/reference/kotlin/android/transition/ChangeClipBounds) | ChangeClipBounds captures the `https://developer.android.com/reference/kotlin/android/view/View.html#getClipBounds()` before and after the scene change and animates those changes during the transition. | | [ChangeImageTransform](https://developer.android.com/reference/kotlin/android/transition/ChangeImageTransform) | This Transition captures an ImageView's matrix before and after the scene change and animates it during the transition. | | [ChangeScroll](https://developer.android.com/reference/kotlin/android/transition/ChangeScroll) | This transition captures the scroll properties of targets before and after the scene change and animates any changes. | | [ChangeTransform](https://developer.android.com/reference/kotlin/android/transition/ChangeTransform) | This Transition captures scale and rotation for Views before and after the scene change and animates those changes during the transition. | | [TransitionSet](https://developer.android.com/reference/kotlin/android/transition/TransitionSet) | A TransitionSet is a parent of child transitions (including other TransitionSets). | | [Visibility](https://developer.android.com/reference/kotlin/android/transition/Visibility) | This transition tracks changes to the visibility of target views in the start and end scenes. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AutoTransition](https://developer.android.com/reference/kotlin/android/transition/AutoTransition), [Explode](https://developer.android.com/reference/kotlin/android/transition/Explode), [Fade](https://developer.android.com/reference/kotlin/android/transition/Fade), [Slide](https://developer.android.com/reference/kotlin/android/transition/Slide) |---|---| | [AutoTransition](https://developer.android.com/reference/kotlin/android/transition/AutoTransition) | Utility class for creating a default transition that automatically fades, moves, and resizes views during a scene change. | | [Explode](https://developer.android.com/reference/kotlin/android/transition/Explode) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from the edges of the scene. | | [Fade](https://developer.android.com/reference/kotlin/android/transition/Fade) | This transition tracks changes to the visibility of target views in the start and end scenes and fades views in or out when they become visible or non-visible. | | [Slide](https://developer.android.com/reference/kotlin/android/transition/Slide) | This transition tracks changes to the visibility of target views in the start and end scenes and moves views in or out from one of the edges of the scene. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A Transition holds information about animations that will be run on its targets during a scene change. Subclasses of this abstract class may choreograph several child transitions (`https://developer.android.com/reference/kotlin/android/transition/TransitionSet` or they may perform custom animations themselves. Any Transition has two main jobs: (1) capture property values, and (2) play animations based on changes to captured property values. A custom transition knows what property values on View objects are of interest to it, and also knows how to animate changes to those values. For example, the `https://developer.android.com/reference/kotlin/android/transition/Fade` transition tracks changes to visibility-related properties and is able to construct and run animations that fade items in or out based on changes to those properties.

Note: Transitions may not work correctly with either `https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#` or `https://developer.android.com/reference/kotlin/android/view/TextureView.html#`, due to the way that these views are displayed on the screen. For SurfaceView, the problem is that the view is updated from a non-UI thread, so changes to the view due to transitions (such as moving and resizing the view) may be out of sync with the display inside those bounds. TextureView is more compatible with transitions in general, but some specific transitions (such as `https://developer.android.com/reference/kotlin/android/transition/Fade`) may not be compatible with TextureView because they rely on `https://developer.android.com/reference/kotlin/android/view/ViewOverlay.html#` functionality, which does not currently work with TextureView.

Transitions can be declared in XML resource files inside the `res/transition` directory. Transition resources consist of a tag name for one of the Transition subclasses along with attributes to define some of the attributes of that transition. For example, here is a minimal resource file that declares a `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds` transition:

This TransitionSet contains `https://developer.android.com/reference/kotlin/android/transition/Explode` for visibility, `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds`, `https://developer.android.com/reference/kotlin/android/transition/ChangeTransform`, and `https://developer.android.com/reference/kotlin/android/transition/ChangeClipBounds` and `https://developer.android.com/reference/kotlin/android/transition/ChangeImageTransform`:

Custom transition classes may be instantiated with a `transition` tag:

```kotlin
<transition class="my.app.transition.CustomTransition"/>
```

Custom transition classes loaded from XML should have a public constructor taking a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and `https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#`.

Note that attributes for the transition are not required, just as they are optional when declared in code; Transitions created from XML resources will use the same defaults as their code-created equivalents. Here is a slightly more elaborate example which declares a `https://developer.android.com/reference/kotlin/android/transition/TransitionSet` transition with `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds` and `https://developer.android.com/reference/kotlin/android/transition/Fade` child transitions:

In this example, the transitionOrdering attribute is used on the TransitionSet object to change from the default `https://developer.android.com/reference/kotlin/android/transition/TransitionSet#ORDERING_TOGETHER:kotlin.Int` behavior to be `https://developer.android.com/reference/kotlin/android/transition/TransitionSet#ORDERING_SEQUENTIAL:kotlin.Int` instead. Also, the `https://developer.android.com/reference/kotlin/android/transition/Fade` transition uses a fadingMode of `https://developer.android.com/reference/kotlin/android/transition/Fade#OUT:kotlin.Int` instead of the default out-in behavior. Finally, note the use of the `targets` sub-tag, which takes a set of `https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionTarget:kotlin.IntArray` tags, each of which lists a specific `targetId`, `targetClass`, `targetName`, `excludeId`, `excludeClass`, or `excludeName`, which this transition acts upon. Use of targets is optional, but can be used to either limit the time spent checking attributes on unchanging views, or limiting the types of animations run on specific views. In this case, we know that only the `grayscaleContainer` will be disappearing, so we choose to limit the `https://developer.android.com/reference/kotlin/android/transition/Fade` transition to only that view.
Further information on XML resource descriptions for transitions can be found for `https://developer.android.com/reference/kotlin/android/R.styleable.html#Transition:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionSet:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionTarget:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#Fade:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#Slide:kotlin.IntArray`, and `https://developer.android.com/reference/kotlin/android/R.styleable.html#ChangeTransform:kotlin.IntArray`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback` Class to get the epicenter of Transition. |
| abstract | `https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener` A transition listener receives notifications from a transition. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_ID:kotlin.Int` With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by `https://developer.android.com/reference/kotlin/android/view/View.html#getId()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_INSTANCE:kotlin.Int` With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by View instance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_ITEM_ID:kotlin.Int` With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by the `https://developer.android.com/reference/kotlin/android/widget/Adapter.html#` item id. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_NAME:kotlin.Int` With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by `https://developer.android.com/reference/kotlin/android/view/View.html#getTransitionName()`. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#Transition()()` Constructs a Transition object with no target objects. |
| `https://developer.android.com/reference/kotlin/android/transition/Transition#Transition(android.content.Context,%20android.util.AttributeSet)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!)` Perform inflation from XML and apply a class-specific base style from a theme attribute or style resource. |

| Public methods ||
|---|---|
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#addListener(android.transition.Transition.TransitionListener)(listener: https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener!)` Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(android.view.View)(target: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Sets the target view instances that this Transition is interested in animating. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(kotlin.Int)(targetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adds the id of a target view that this Transition is interested in animating. |
| --- | --- |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(java.lang.Class)(targetType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!)` Adds the Class of a target view that this Transition is interested in animating. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(kotlin.String)(targetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Adds the transitionName of a target view that this Transition is interested in animating. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#canRemoveViews()()` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#captureEndValues(android.transition.TransitionValues)(transitionValues: https://developer.android.com/reference/kotlin/android/transition/TransitionValues!)` Captures the values in the end scene for the properties that this transition monitors. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#captureStartValues(android.transition.TransitionValues)(transitionValues: https://developer.android.com/reference/kotlin/android/transition/TransitionValues!)` Captures the values in the start scene for the properties that this transition monitors. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#) | `https://developer.android.com/reference/kotlin/android/transition/Transition#clone()()` Creates and returns a copy of this object. |
| --- | --- |
| open [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator.html#)? | `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)(sceneRoot: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#, startValues: https://developer.android.com/reference/kotlin/android/transition/TransitionValues?, endValues: https://developer.android.com/reference/kotlin/android/transition/TransitionValues?)` This method creates an animation that will be run for this transition given the information in the startValues and endValues structures captured earlier for the start and end scenes. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(android.view.View,%20kotlin.Boolean)(target: https://developer.android.com/reference/kotlin/android/view/View.html#!, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the children of given target to the list of target children to exclude from this transition. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(kotlin.Int,%20kotlin.Boolean)(targetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the children of the given id to the list of targets to exclude from this transition. |
| --- | --- |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(java.lang.Class,%20kotlin.Boolean)(type: https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the given type to the list of types whose children should be excluded from this transition. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(android.view.View,%20kotlin.Boolean)(target: https://developer.android.com/reference/kotlin/android/view/View.html#!, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the given target to the list of targets to exclude from this transition. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(kotlin.Int,%20kotlin.Boolean)(targetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the given id to the list of target ids to exclude from this transition. |
| --- | --- |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(java.lang.Class,%20kotlin.Boolean)(type: https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the given type to the list of types to exclude from this transition. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(kotlin.String,%20kotlin.Boolean)(targetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, exclude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to add the given transitionName to the list of target transitionNames to exclude from this transition. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#getDuration()()` Returns the duration set on this transition. |
| --- | --- |
| open [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getEpicenter()()` Returns the epicenter as specified by the `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback` or null if no callback exists. |
| open [Transition.EpicenterCallback](https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getEpicenterCallback()()` Returns the callback used to find the epicenter of the Transition. |
| open [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getInterpolator()()` Returns the interpolator set on this transition. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getName()()` Returns the name of this Transition. |
| open [PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getPathMotion()()` Returns the algorithm object used to interpolate along two dimensions. |
| open [TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getPropagation()()` Returns the `https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation` used to calculate Animator start delays. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#getStartDelay()()` Returns the startDelay set on this transition. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetIds()()` Returns the list of target IDs that this transition limits itself to tracking and animating. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetNames()()` Returns the list of target transitionNames that this transition limits itself to tracking and animating. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetTypes()()` Returns the list of target transitionNames that this transition limits itself to tracking and animating. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!\>! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargets()()` Returns the list of target views that this transition limits itself to tracking and animating. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getTransitionProperties()()` Returns the set of property names used stored in the `https://developer.android.com/reference/kotlin/android/transition/TransitionValues` object passed into `https://developer.android.com/reference/kotlin/android/transition/Transition#captureStartValues(android.transition.TransitionValues)` that this transition cares about for the purposes of canceling overlapping animations. |
| --- | --- |
| open [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#getTransitionValues(android.view.View,%20kotlin.Boolean)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` This method can be called by transitions to get the TransitionValues for any particular view during the transition-playing process. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#isTransitionRequired(android.transition.TransitionValues,%20android.transition.TransitionValues)(startValues: https://developer.android.com/reference/kotlin/android/transition/TransitionValues?, endValues: https://developer.android.com/reference/kotlin/android/transition/TransitionValues?)` Returns whether or not the transition should create an Animator, based on the values captured during `https://developer.android.com/reference/kotlin/android/transition/Transition#captureStartValues(android.transition.TransitionValues)` and `https://developer.android.com/reference/kotlin/android/transition/Transition#captureEndValues(android.transition.TransitionValues)`. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#removeListener(android.transition.Transition.TransitionListener)(listener: https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener!)` Removes a listener from the set listening to this animation. |
| --- | --- |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#removeTarget(android.view.View)(target: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Removes the given target from the list of targets that this Transition is interested in animating. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#removeTarget(kotlin.Int)(targetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the given targetId from the list of ids that this Transition is interested in animating. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#removeTarget(java.lang.Class)(target: https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!)` Removes the given target from the list of targets that this Transition is interested in animating. |
| --- | --- |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#removeTarget(kotlin.String)(targetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Removes the given targetName from the list of transitionNames that this Transition is interested in animating. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#setDuration(kotlin.Long)(duration: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the duration of this transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#setEpicenterCallback(android.transition.Transition.EpicenterCallback)(epicenterCallback: https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback!)` Sets the callback to use to find the epicenter of a Transition. |
| --- | --- |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#setInterpolator(android.animation.TimeInterpolator)(interpolator: https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#!)` Sets the interpolator of this transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)(vararg matches: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the order in which Transition matches View start and end values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#setPathMotion(android.transition.PathMotion)(pathMotion: https://developer.android.com/reference/kotlin/android/transition/PathMotion!)` Sets the algorithm used to calculate two-dimensional interpolation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#setPropagation(android.transition.TransitionPropagation)(transitionPropagation: https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation!)` Sets the method for determining Animator start delays. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition#)! | `https://developer.android.com/reference/kotlin/android/transition/Transition#setStartDelay(kotlin.Long)(startDelay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the startDelay of this transition. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/transition/Transition#toString()()` Returns a string representation of the object. |
| --- | --- |

## Constants

### MATCH_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ID: Int
```

With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by `https://developer.android.com/reference/kotlin/android/view/View.html#getId()`. Negative IDs will not be matched.

 Value: 3

### MATCH_INSTANCE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_INSTANCE: Int
```

With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by View instance.

 Value: 1

### MATCH_ITEM_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_ITEM_ID: Int
```

With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by the `https://developer.android.com/reference/kotlin/android/widget/Adapter.html#` item id. When `https://developer.android.com/reference/kotlin/android/widget/Adapter.html#hasStableIds()` returns false, no match will be made for items.

 Value: 4

### MATCH_NAME

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATCH_NAME: Int
```

With `https://developer.android.com/reference/kotlin/android/transition/Transition#setMatchOrder(kotlin.Int)`, chooses to match by `https://developer.android.com/reference/kotlin/android/view/View.html#getTransitionName()`. Null names will not be matched.

 Value: 2

## Public constructors

### Transition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Transition()
```

Constructs a Transition object with no target objects. A transition with no targets defaults to running on all target objects in the scene hierarchy (if the transition is not contained in a TransitionSet), or all target objects passed down from its parent (if it is in a TransitionSet).

### Transition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Transition(
    context: Context!, 
    attrs: AttributeSet!)
```

Perform inflation from XML and apply a class-specific base style from a theme attribute or style resource. This constructor of Transition allows subclasses to use their own base style when they are inflating.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: The Context the transition is running in, through which it can access the current theme, resources, etc. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: The attributes of the XML tag that is inflating the transition. |

## Public methods

### addListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addListener(listener: Transition.TransitionListener!): Transition!
```

Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end.

| Parameters ||
|---|---|
| `listener` | [Transition.TransitionListener](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener)!: the listener to be added to the current set of listeners for this animation. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

### addTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addTarget(target: View!): Transition!
```

Sets the target view instances that this Transition is interested in animating. By default, there are no targets, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targets constrains the Transition to only listen for, and act on, these views. All other views will be ignored.

The target list is like the `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(kotlin.Int)` list except this list specifies the actual View instances, not the ids of the views. This is an important distinction when scene changes involve view hierarchies which have been inflated separately; different views may share the same id but not actually be the same instance. If the transition should treat those views as the same, then `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(kotlin.Int)` should be used instead of `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(android.view.View)`. If, on the other hand, scene changes involve changes all within the same view hierarchy, among views which do not necessarily have ids set on them, then the target list of views may be more convenient.

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: A View on which the Transition will act, must be non-null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | The Transition to which the target is added. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).addTarget(someView);` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(kotlin.Int)`

### addTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addTarget(targetId: Int): Transition!
```

Adds the id of a target view that this Transition is interested in animating. By default, there are no targetIds, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targetIds constrains the Transition to only listen for, and act on, views with these IDs. Views with different IDs, or no IDs whatsoever, will be ignored.

Note that using ids to specify targets implies that ids should be unique within the view hierarchy underneath the scene root.

| Parameters ||
|---|---|
| `targetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a target view, must be a positive number. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | The Transition to which the targetId is added. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).addTarget(someId);` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#getId()`

### addTarget

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addTarget(targetType: Class<Any!>!): Transition!
```

Adds the Class of a target view that this Transition is interested in animating. By default, there are no targetTypes, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targetTypes constrains the Transition to only listen for, and act on, views with these classes. Views with different classes will be ignored.

Note that any View that can be cast to targetType will be included, so if targetType is `View.class`, all Views will be included.

| Parameters ||
|---|---|
| `targetType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The type to include when running this transition. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | The Transition to which the target class was added. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).addTarget(ImageView.class);` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#addTarget(android.view.View)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(java.lang.Class,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(java.lang.Class,%20kotlin.Boolean)`

### addTarget

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addTarget(targetName: String!): Transition!
```

Adds the transitionName of a target view that this Transition is interested in animating. By default, there are no targetNames, and a Transition will listen for changes on every view in the hierarchy below the sceneRoot of the Scene being transitioned into. Setting targetNames constrains the Transition to only listen for, and act on, views with these transitionNames. Views with different transitionNames, or no transitionName whatsoever, will be ignored.

Note that transitionNames should be unique within the view hierarchy.

| Parameters ||
|---|---|
| `targetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The transitionName of a target view, must be non-null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | The Transition to which the target transitionName is added. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).addTarget(someName);` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#getTransitionName()`

### canRemoveViews

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canRemoveViews(): Boolean
```

### captureEndValues

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun captureEndValues(transitionValues: TransitionValues!): Unit
```

Captures the values in the end scene for the properties that this transition monitors. These values are then passed as the endValues structure in a later call to `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)`. The main concern for an implementation is what the properties are that the transition cares about and what the values are for all of those properties. The start and end values will be compared later during the `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)` method to determine what, if any, animations, should be run.

Subclasses must implement this method. The method should only be called by the transition system; it is not intended to be called from external classes.

| Parameters ||
|---|---|
| `transitionValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!: The holder for any values that the Transition wishes to store. Values are stored in the `values` field of this TransitionValues object and are keyed from a String value. For example, to store a view's rotation value, a transition might call `transitionValues.values.put("appname:transitionname:rotation", view.getRotation())`. The target view will already be stored in the transitionValues structure when this method is called. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#captureStartValues(android.transition.TransitionValues)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)`

### captureStartValues

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun captureStartValues(transitionValues: TransitionValues!): Unit
```

Captures the values in the start scene for the properties that this transition monitors. These values are then passed as the startValues structure in a later call to `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)`. The main concern for an implementation is what the properties are that the transition cares about and what the values are for all of those properties. The start and end values will be compared later during the `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)` method to determine what, if any, animations, should be run.

Subclasses must implement this method. The method should only be called by the transition system; it is not intended to be called from external classes.

| Parameters ||
|---|---|
| `transitionValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)!: The holder for any values that the Transition wishes to store. Values are stored in the `values` field of this TransitionValues object and are keyed from a String value. For example, to store a view's rotation value, a transition might call `transitionValues.values.put("appname:transitionname:rotation", view.getRotation())`. The target view will already be stored in the transitionValues structure when this method is called. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#captureEndValues(android.transition.TransitionValues)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#createAnimator(android.view.ViewGroup,%20android.transition.TransitionValues,%20android.transition.TransitionValues)`

### clone

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Transition
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### createAnimator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createAnimator(
    sceneRoot: ViewGroup, 
    startValues: TransitionValues?, 
    endValues: TransitionValues?
): Animator?
```

This method creates an animation that will be run for this transition given the information in the startValues and endValues structures captured earlier for the start and end scenes. Subclasses of Transition should override this method. The method should only be called by the transition system; it is not intended to be called from external classes.

This method is called by the transition's parent (all the way up to the topmost Transition in the hierarchy) with the sceneRoot and start/end values that the transition may need to set up initial target values and construct an appropriate animation. For example, if an overall Transition is a `https://developer.android.com/reference/kotlin/android/transition/TransitionSet` consisting of several child transitions in sequence, then some of the child transitions may want to set initial values on target views prior to the overall Transition commencing, to put them in an appropriate state for the delay between that start and the child Transition start time. For example, a transition that fades an item in may wish to set the starting alpha value to 0, to avoid it blinking in prior to the transition actually starting the animation. This is necessary because the scene change that triggers the Transition will automatically set the end-scene on all target views, so a Transition that wants to animate from a different value should set that value prior to returning from this method.

Additionally, a Transition can perform logic to determine whether the transition needs to run on the given target and start/end values. For example, a transition that resizes objects on the screen may wish to avoid running for views which are not present in either the start or end scenes.

If there is an animator created and returned from this method, the transition mechanism will apply any applicable duration, startDelay, and interpolator to that animation and start it. A return value of `null` indicates that no animation should run. The default implementation returns null.

The method is called for every applicable target object, which is stored in the `https://developer.android.com/reference/kotlin/android/transition/TransitionValues#view:android.view.View` field.

| Parameters ||
|---|---|
| `sceneRoot` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#): The root of the transition hierarchy. This value cannot be `null`. |
| `startValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)?: The values for a specific target in the start scene, or `null` if the target doesn't exist in the start scene. |
| `endValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)?: The values for the target in the end scene, or `null` if the target doesn't exist in the end scene. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/Animator.html#?` | an `https://developer.android.com/reference/kotlin/android/animation/Animator.html#` to be started at the appropriate time in the overall transition for this scene change. A `null` value means no animation should be run. |

### excludeChildren

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeChildren(
    target: View!, 
    exclude: Boolean
): Transition!
```

Whether to add the children of given target to the list of target children to exclude from this transition. The `exclude` parameter specifies whether the target should be added to or removed from the excluded list.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The target to ignore when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target to or remove the target from the current list of excluded targets. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(android.view.View,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(java.lang.Class,%20kotlin.Boolean)`

### excludeChildren

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeChildren(
    targetId: Int, 
    exclude: Boolean
): Transition!
```

Whether to add the children of the given id to the list of targets to exclude from this transition. The `exclude` parameter specifies whether the children of the target should be added to or removed from the excluded list. Excluding children in this way provides a simple mechanism for excluding all children of specific targets, rather than individually excluding each child individually.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `targetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a target whose children should be ignored when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target to or remove the target from the current list of excluded-child targets. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(android.view.View,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(java.lang.Class,%20kotlin.Boolean)`

### excludeChildren

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeChildren(
    type: Class<Any!>!, 
    exclude: Boolean
): Transition!
```

Whether to add the given type to the list of types whose children should be excluded from this transition. The `exclude` parameter specifies whether the target type should be added to or removed from the excluded list.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The type to ignore when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target type to or remove it from the current list of excluded target types. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(java.lang.Class,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(android.view.View,%20kotlin.Boolean)`

### excludeTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeTarget(
    target: View!, 
    exclude: Boolean
): Transition!
```

Whether to add the given target to the list of targets to exclude from this transition. The `exclude` parameter specifies whether the target should be added to or removed from the excluded list.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The target to ignore when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target to or remove the target from the current list of excluded targets. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(android.view.View,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(java.lang.Class,%20kotlin.Boolean)`

### excludeTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeTarget(
    targetId: Int, 
    exclude: Boolean
): Transition!
```

Whether to add the given id to the list of target ids to exclude from this transition. The `exclude` parameter specifies whether the target should be added to or removed from the excluded list.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `targetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a target to ignore when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target to or remove the target from the current list of excluded targets. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(android.view.View,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(java.lang.Class,%20kotlin.Boolean)`

### excludeTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeTarget(
    type: Class<Any!>!, 
    exclude: Boolean
): Transition!
```

Whether to add the given type to the list of types to exclude from this transition. The `exclude` parameter specifies whether the target type should be added to or removed from the excluded list.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded either by their id, or by their instance reference, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The type to ignore when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target type to or remove it from the current list of excluded target types. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeChildren(java.lang.Class,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(android.view.View,%20kotlin.Boolean)`

### excludeTarget

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun excludeTarget(
    targetName: String!, 
    exclude: Boolean
): Transition!
```

Whether to add the given transitionName to the list of target transitionNames to exclude from this transition. The `exclude` parameter specifies whether the target should be added to or removed from the excluded list.

Excluding targets is a general mechanism for allowing transitions to run on a view hierarchy while skipping target views that should not be part of the transition. For example, you may want to avoid animating children of a specific ListView or Spinner. Views can be excluded by their id, their instance reference, their transitionName, or by the Class of that view (eg, `https://developer.android.com/reference/kotlin/android/widget/Spinner.html#`).

| Parameters ||
|---|---|
| `targetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of a target to ignore when running this transition. |
| `exclude` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to add the target to or remove the target from the current list of excluded targets. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(android.view.View,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(kotlin.Int,%20kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/transition/Transition#excludeTarget(java.lang.Class,%20kotlin.Boolean)`

### getDuration

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDuration(): Long
```

Returns the duration set on this transition. If no duration has been set, the returned value will be negative, indicating that resulting animators will retain their own durations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The duration set on this transition, in milliseconds, if one has been set, otherwise returns a negative number. |

### getEpicenter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEpicenter(): Rect!
```

Returns the epicenter as specified by the `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback` or null if no callback exists.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!` | the epicenter as specified by the `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback` or null if no callback exists. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/Transition#setEpicenterCallback(android.transition.Transition.EpicenterCallback)`

### getEpicenterCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getEpicenterCallback(): Transition.EpicenterCallback!
```

Returns the callback used to find the epicenter of the Transition. Transitions like `https://developer.android.com/reference/kotlin/android/transition/Explode` use a point or Rect to orient the direction of travel. This is called the epicenter of the Transition and is typically centered on a touched View. The `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback` allows a Transition to dynamically retrieve the epicenter during a Transition.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback!` | the callback used to find the epicenter of the Transition. |

### getInterpolator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInterpolator(): TimeInterpolator!
```

Returns the interpolator set on this transition. If no interpolator has been set, the returned value will be null, indicating that resulting animators will retain their own interpolators.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#!` | The interpolator set on this transition, if one has been set, otherwise returns null. |

### getName

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String!
```

Returns the name of this Transition. This name is used internally to distinguish between different transitions to determine when interrupting transitions overlap. For example, a ChangeBounds running on the same target view as another ChangeBounds should determine whether the old transition is animating to different end values and should be canceled in favor of the new transition.

By default, a Transition's name is simply the value of `https://developer.android.com/reference/kotlin/java/lang/Class.html#getName()`, but subclasses are free to override and return something different.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The name of this transition. |

### getPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPathMotion(): PathMotion!
```

Returns the algorithm object used to interpolate along two dimensions. This is typically used to determine the View motion between two points.

When describing in XML, use a nested XML tag for the path motion. It can be one of the built-in tags `arcMotion` or `patternPathMotion` or it can be a custom PathMotion using `pathMotion` with the `class` attributed with the fully-described class name. For example:

```kotlin
<code>&lt;changeBounds&gt;
      &lt;pathMotion class="my.app.transition.MyPathMotion"/&gt;
  &lt;/changeBounds&gt;</code>
```

or

```kotlin
<code>&lt;changeBounds&gt;
    &lt;arcMotion android:minimumHorizontalAngle="15"
               android:minimumVerticalAngle="0"
               android:maximumAngle="90"/&gt;
  &lt;/changeBounds&gt;</code>
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/PathMotion!` | The algorithm object used to interpolate along two dimensions. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/ArcMotion`
- `https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion`
- `https://developer.android.com/reference/kotlin/android/transition/PathMotion`

### getPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPropagation(): TransitionPropagation!
```

Returns the `https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation` used to calculate Animator start delays. When a Transition affects several Views like `https://developer.android.com/reference/kotlin/android/transition/Explode` or `https://developer.android.com/reference/kotlin/android/transition/Slide`, there may be a desire to have a "wave-front" effect such that the Animator start delay depends on position of the View. The TransitionPropagation specifies how the start delays are calculated.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation!` | the `https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation` used to calculate Animator start delays. This is null by default. |

### getStartDelay

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStartDelay(): Long
```

Returns the startDelay set on this transition. If no startDelay has been set, the returned value will be negative, indicating that resulting animators will retain their own startDelays.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The startDelay set on this transition, in milliseconds, if one has been set, otherwise returns a negative number. |

### getTargetIds

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetIds(): MutableList<Int!>!
```

Returns the list of target IDs that this transition limits itself to tracking and animating. If the list is null or empty for `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetIds()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargets()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetNames()`, and `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetTypes()` then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | the list of target IDs |

### getTargetNames

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetNames(): MutableList<String!>!
```

Returns the list of target transitionNames that this transition limits itself to tracking and animating. If the list is null or empty for `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetIds()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargets()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetNames()`, and `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetTypes()` then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the list of target transitionNames |

### getTargetTypes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetTypes(): MutableList<Class<Any!>!>!
```

Returns the list of target transitionNames that this transition limits itself to tracking and animating. If the list is null or empty for `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetIds()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargets()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetNames()`, and `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetTypes()` then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!>!` | the list of target Types |

### getTargets

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargets(): MutableList<View!>!
```

Returns the list of target views that this transition limits itself to tracking and animating. If the list is null or empty for `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetIds()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargets()`, `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetNames()`, and `https://developer.android.com/reference/kotlin/android/transition/Transition#getTargetTypes()` then this transition is not limited to specific views, and will handle changes to any views in the hierarchy of a scene change.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/view/View.html#!>!` | the list of target views |

### getTransitionProperties

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransitionProperties(): Array<String!>!
```

Returns the set of property names used stored in the `https://developer.android.com/reference/kotlin/android/transition/TransitionValues` object passed into `https://developer.android.com/reference/kotlin/android/transition/Transition#captureStartValues(android.transition.TransitionValues)` that this transition cares about for the purposes of canceling overlapping animations. When any transition is started on a given scene root, all transitions currently running on that same scene root are checked to see whether the properties on which they based their animations agree with the end values of the same properties in the new transition. If the end values are not equal, then the old animation is canceled since the new transition will start a new animation to these new values. If the values are equal, the old animation is allowed to continue and no new animation is started for that transition.

A transition does not need to override this method. However, not doing so will mean that the cancellation logic outlined in the previous paragraph will be skipped for that transition, possibly leading to artifacts as old transitions and new transitions on the same targets run in parallel, animating views toward potentially different end values.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | An array of property names as described in the class documentation for `https://developer.android.com/reference/kotlin/android/transition/TransitionValues`. The default implementation returns `null`. |

### getTransitionValues

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTransitionValues(
    view: View!, 
    start: Boolean
): TransitionValues!
```

This method can be called by transitions to get the TransitionValues for any particular view during the transition-playing process. This might be necessary, for example, to query the before/after state of related views for a given transition.

### isTransitionRequired

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isTransitionRequired(
    startValues: TransitionValues?, 
    endValues: TransitionValues?
): Boolean
```

Returns whether or not the transition should create an Animator, based on the values captured during `https://developer.android.com/reference/kotlin/android/transition/Transition#captureStartValues(android.transition.TransitionValues)` and `https://developer.android.com/reference/kotlin/android/transition/Transition#captureEndValues(android.transition.TransitionValues)`. The default implementation compares the property values returned from `https://developer.android.com/reference/kotlin/android/transition/Transition#getTransitionProperties()`, or all property values if `getTransitionProperties()` returns null. Subclasses may override this method to provide logic more specific to the transition implementation.

| Parameters ||
|---|---|
| `startValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)?: the values from captureStartValues, This may be `null` if the View did not exist in the start state. |
| `endValues` | [TransitionValues](https://developer.android.com/reference/kotlin/android/transition/TransitionValues)?: the values from captureEndValues. This may be `null` if the View did not exist in the end state. |

### removeListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeListener(listener: Transition.TransitionListener!): Transition!
```

Removes a listener from the set listening to this animation.

| Parameters ||
|---|---|
| `listener` | [Transition.TransitionListener](https://developer.android.com/reference/kotlin/android/transition/Transition.TransitionListener)!: the listener to be removed from the current set of listeners for this transition. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

### removeTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTarget(target: View!): Transition!
```

Removes the given target from the list of targets that this Transition is interested in animating.

| Parameters ||
|---|---|
| `target` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The target view, must be non-null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | Transition The Transition from which the target is removed. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).removeTarget(someView);` |

### removeTarget

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTarget(targetId: Int): Transition!
```

Removes the given targetId from the list of ids that this Transition is interested in animating.

| Parameters ||
|---|---|
| `targetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The id of a target view, must be a positive number. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | The Transition from which the targetId is removed. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).removeTargetId(someId);` |

### removeTarget

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTarget(target: Class<Any!>!): Transition!
```

Removes the given target from the list of targets that this Transition is interested in animating.

| Parameters ||
|---|---|
| `target` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: The type of the target view, must be non-null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | Transition The Transition from which the target is removed. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).removeTarget(someType);` |

### removeTarget

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTarget(targetName: String!): Transition!
```

Removes the given targetName from the list of transitionNames that this Transition is interested in animating.

| Parameters ||
|---|---|
| `targetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The transitionName of a target view, must not be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | The Transition from which the targetName is removed. Returning the same object makes it easier to chain calls during construction, such as `transitionSet.addTransitions(new Fade()).removeTargetName(someName);` |

### setDuration

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDuration(duration: Long): Transition!
```

Sets the duration of this transition. By default, there is no duration (indicated by a negative number), which means that the Animator created by the transition will have its own specified duration. If the duration of a Transition is set, that duration will override the Animator duration.

| Parameters ||
|---|---|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The length of the animation, in milliseconds. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

### setEpicenterCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setEpicenterCallback(epicenterCallback: Transition.EpicenterCallback!): Unit
```

Sets the callback to use to find the epicenter of a Transition. A null value indicates that there is no epicenter in the Transition and onGetEpicenter() will return null. Transitions like `https://developer.android.com/reference/kotlin/android/transition/Explode` use a point or Rect to orient the direction of travel. This is called the epicenter of the Transition and is typically centered on a touched View. The `https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback` allows a Transition to dynamically retrieve the epicenter during a Transition.

| Parameters ||
|---|---|
| `epicenterCallback` | [Transition.EpicenterCallback](https://developer.android.com/reference/kotlin/android/transition/Transition.EpicenterCallback)!: The callback to use to find the epicenter of the Transition. |

### setInterpolator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInterpolator(interpolator: TimeInterpolator!): Transition!
```

Sets the interpolator of this transition. By default, the interpolator is null, which means that the Animator created by the transition will have its own specified interpolator. If the interpolator of a Transition is set, that interpolator will override the Animator interpolator.

| Parameters ||
|---|---|
| `interpolator` | [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#)!: The time interpolator used by the transition |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

### setMatchOrder

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMatchOrder(vararg matches: Int): Unit
```

Sets the order in which Transition matches View start and end values.

The default behavior is to match first by `https://developer.android.com/reference/kotlin/android/view/View.html#getTransitionName()`, then by View instance, then by `https://developer.android.com/reference/kotlin/android/view/View.html#getId()` and finally by its item ID if it is in a direct child of ListView. The caller can choose to have only some or all of the values of `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_INSTANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_NAME:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_ITEM_ID:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_ID:kotlin.Int`. Only the match algorithms supplied will be used to determine whether Views are the the same in both the start and end Scene. Views that do not match will be considered as entering or leaving the Scene.

| Parameters ||
|---|---|
| `matches` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A list of zero or more of `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_INSTANCE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_NAME:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_ITEM_ID:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/transition/Transition#MATCH_ID:kotlin.Int`. If none are provided, then the default match order will be set. |

### setPathMotion

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPathMotion(pathMotion: PathMotion!): Unit
```

Sets the algorithm used to calculate two-dimensional interpolation.

Transitions such as `https://developer.android.com/reference/kotlin/android/transition/ChangeBounds` move Views, typically in a straight path between the start and end positions. Applications that desire to have these motions move in a curve can change how Views interpolate in two dimensions by extending PathMotion and implementing `https://developer.android.com/reference/kotlin/android/transition/PathMotion#getPath(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)`.

When describing in XML, use a nested XML tag for the path motion. It can be one of the built-in tags `arcMotion` or `patternPathMotion` or it can be a custom PathMotion using `pathMotion` with the `class` attributed with the fully-described class name. For example:

```kotlin
<code>&lt;changeBounds&gt;
      &lt;pathMotion class="my.app.transition.MyPathMotion"/&gt;
  &lt;/changeBounds&gt;
  </code>
```

or

```kotlin
<code>&lt;changeBounds&gt;
    &lt;arcMotion android:minimumHorizontalAngle="15"
      android:minimumVerticalAngle="0" android:maximumAngle="90"/&gt;
  &lt;/changeBounds&gt;
  </code>
```

| Parameters ||
|---|---|
| `pathMotion` | [PathMotion](https://developer.android.com/reference/kotlin/android/transition/PathMotion)!: Algorithm object to use for determining how to interpolate in two dimensions. If null, a straight-path algorithm will be used. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/transition/ArcMotion`
- `https://developer.android.com/reference/kotlin/android/transition/PatternPathMotion`
- `https://developer.android.com/reference/kotlin/android/transition/PathMotion`

### setPropagation

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPropagation(transitionPropagation: TransitionPropagation!): Unit
```

Sets the method for determining Animator start delays. When a Transition affects several Views like `https://developer.android.com/reference/kotlin/android/transition/Explode` or `https://developer.android.com/reference/kotlin/android/transition/Slide`, there may be a desire to have a "wave-front" effect such that the Animator start delay depends on position of the View. The TransitionPropagation specifies how the start delays are calculated.

| Parameters ||
|---|---|
| `transitionPropagation` | [TransitionPropagation](https://developer.android.com/reference/kotlin/android/transition/TransitionPropagation)!: The class used to determine the start delay of Animators created by this Transition. A null value indicates that no delay should be used. |

### setStartDelay

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStartDelay(startDelay: Long): Transition!
```

Sets the startDelay of this transition. By default, there is no delay (indicated by a negative number), which means that the Animator created by the transition will have its own specified startDelay. If the delay of a Transition is set, that delay will override the Animator delay.

| Parameters ||
|---|---|
| `startDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The length of the delay, in milliseconds. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/Transition#!` | This transition object. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

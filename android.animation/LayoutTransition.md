# LayoutTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayoutTransition

Kotlin| [Java](https://developer.android.com/reference/android/animation/LayoutTransition "View this page in Java") 
| --- | --- |

```
open class LayoutTransition
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#) |

This class enables automatic animations on layout changes in ViewGroup objects. To enable transitions for a layout container, create a LayoutTransition object and set it on any ViewGroup by calling [ViewGroup.setLayoutTransition(LayoutTransition)](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#setLayoutTransition(android.animation.LayoutTransition)). This will cause default animations to run whenever items are added to or removed from that container. To specify custom animations, use the [setAnimator()](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setAnimator(kotlin.Int,%20android.animation.Animator))method.

One of the core concepts of these transition animations is that there are two types of changes that cause the transition and four different animations that run because of those changes. The changes that trigger the transition are items being added to a container (referred to as an "appearing" transition) or removed from a container (also known as "disappearing"). Setting the visibility of views (between GONE and VISIBLE) will trigger the same add/remove logic. The animations that run due to those events are one that animates items being added, one that animates items being removed, and two that animate the other items in the container that change due to the add/remove occurrence. Users of the transition may want different animations for the changing items depending on whether they are changing due to an appearing or disappearing event, so there is one animation for each of these variations of the changing event. Most of the API of this class is concerned with setting up the basic properties of the animations used in these four situations, or with setting up custom animations for any or all of the four.

By default, the DISAPPEARING animation begins immediately, as does the CHANGE_APPEARING animation. The other animations begin after a delay that is set to the default duration of the animations. This behavior facilitates a sequence of animations in transitions as follows: when an item is being added to a layout, the other children of that container will move first (thus creating space for the new item), then the appearing animation will run to animate the item being added. Conversely, when an item is removed from a container, the animation to remove it will run first, then the animations of the other children in the layout will run (closing the gap created in the layout when the item was removed). If this default choreography behavior is not desired, the [setDuration(int,long)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setDuration(kotlin.Int,%20kotlin.Long))and [setStartDelay(int,long)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setStartDelay(kotlin.Int,%20kotlin.Long))of any or all of the animations can be changed as appropriate. Keep in mind, however, that if you start an APPEARING animation before a DISAPPEARING animation is completed, the DISAPPEARING animation stops, and any effects from the DISAPPEARING animation are reverted. If you instead start a DISAPPEARING animation before an APPEARING animation is completed, a similar set of effects occurs for the APPEARING animation.

The animations specified for the transition, both the defaults and any custom animations set on the transition object, are templates only. That is, these animations exist to hold the basic animation properties, such as the duration, start delay, and properties being animated. But the actual target object, as well as the start and end values for those properties, are set automatically in the process of setting up the transition each time it runs. Each of the animations is cloned from the original copy and the clone is then populated with the dynamic values of the target being animated (such as one of the items in a layout container that is moving as a result of the layout event) as well as the values that are changing (such as the position and size of that object). The actual values that are pushed to each animation depends on what properties are specified for the animation. For example, the default CHANGE_APPEARING animation animates the`left`,`top`,`right`,`bottom`,`scrollX`, and`scrollY`properties. Values for these properties are updated with the pre- and post-layout values when the transition begins. Custom animations will be similarly populated with the target and values being animated, assuming they use ObjectAnimator objects with property names that are known on the target object.

This class, and the associated XML flag for containers, animateLayoutChanges="true", provides a simple utility meant for automating changes in straightforward situations. Using LayoutTransition at multiple levels of a nested view hierarchy may not work due to the interrelationship of the various levels of layout. Also, a container that is being scrolled at the same time as items are being added or removed is probably not a good candidate for this utility, because the before/after locations calculated by LayoutTransition may not match the actual locations when the animations finish due to the container being scrolled as the animations are running. You can work around that particular issue by disabling the 'changing' animations by setting the CHANGE_APPEARING and CHANGE_DISAPPEARING animations to null, and setting the startDelay of the other animations appropriately.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener) This interface is used for listening to starting and ending events for transitions. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int) A flag indicating the animation that runs on those items that are appearing in the container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int) A flag indicating the animation that runs on those items that are changing due to a new item appearing in the container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int) A flag indicating the animation that runs on those items that are changing due to an item disappearing from the container. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int) A flag indicating the animation that runs on those items that are changing due to a layout change not caused by items being added to or removed from the container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int) A flag indicating the animation that runs on those items that are disappearing from the container. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#LayoutTransition())`()` Constructs a LayoutTransition object. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addChild](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#addChild(android.view.ViewGroup,%20android.view.View))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` This method is called by ViewGroup when a child view is about to be added to the container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#addTransitionListener(android.animation.LayoutTransition.TransitionListener))`(`listener:` ` [LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener)!`)` Add a listener that will be called when the bounds of the view change due to layout processing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disableTransitionType](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#disableTransitionType(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Disables the specified transitionType for this LayoutTransition object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableTransitionType](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#enableTransitionType(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enables the specified transitionType for this LayoutTransition object. |
| open [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)! | [getAnimator](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#getAnimator(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the animation used during one of the transition types that may run. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#getDuration(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the duration on one of the animation objects used by this transition. |
| --- | --- |
| open [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | [getInterpolator](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#getInterpolator(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the interpolator on one of the animation objects used by this transition. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStagger](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#getStagger(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the length of time to delay between starting each animation during one of the change animations. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#getStartDelay(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the start delay on one of the animation objects used by this transition. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener)!\>! | [getTransitionListeners](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#getTransitionListeners())`()` Gets the current list of listeners for layout changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hideChild](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#hideChild(android.view.ViewGroup,%20android.view.View))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [hideChild](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#hideChild(android.view.ViewGroup,%20android.view.View,%20kotlin.Int))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `newVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called by ViewGroup when a child view is about to be hidden in container. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChangingLayout](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#isChangingLayout())`()` Returns true if animations are running which animate layout-related properties. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#isRunning())`()` Returns true if any of the animations in this transition are currently running. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isTransitionTypeEnabled](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#isTransitionTypeEnabled(kotlin.Int))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns whether the specified transitionType is enabled for this LayoutTransition object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeChild](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#removeChild(android.view.ViewGroup,%20android.view.View))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` This method is called by ViewGroup when a child view is about to be removed from the container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeTransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#removeTransitionListener(android.animation.LayoutTransition.TransitionListener))`(`listener:` ` [LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener)!`)` Remove a listener for layout changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimateParentHierarchy](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setAnimateParentHierarchy(kotlin.Boolean))`(`animateParentHierarchy:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` This flag controls whether CHANGE_APPEARING or CHANGE_DISAPPEARING animations will cause the default changing animation to be run on the parent hierarchy as well. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimator](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setAnimator(kotlin.Int,%20android.animation.Animator))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `animator:` ` [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)!`)` Sets the animation used during one of the transition types that may run. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDuration](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setDuration(kotlin.Int,%20kotlin.Long))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration on one of the animation objects used by this transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDuration](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setDuration(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration to be used by all animations of this transition object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setInterpolator(kotlin.Int,%20android.animation.TimeInterpolator))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `interpolator:` ` [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)!`)` Sets the interpolator on one of the animation objects used by this transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStagger](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setStagger(kotlin.Int,%20kotlin.Long))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the length of time to delay between starting each animation during one of the change animations. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartDelay](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setStartDelay(kotlin.Int,%20kotlin.Long))`(`transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the start delay on one of the animation objects used by this transition. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showChild](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#showChild(android.view.ViewGroup,%20android.view.View))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showChild](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#showChild(android.view.ViewGroup,%20android.view.View,%20kotlin.Int))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `oldVisibility:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called by ViewGroup when a child view is about to be made visible in the container. |

## Constants

### APPEARING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPEARING: Int
```

A flag indicating the animation that runs on those items that are appearing in the container. 

 Value: 2

### CHANGE_APPEARING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGE_APPEARING: Int
```

A flag indicating the animation that runs on those items that are changing due to a new item appearing in the container. 

 Value: 0

### CHANGE_DISAPPEARING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGE_DISAPPEARING: Int
```

A flag indicating the animation that runs on those items that are changing due to an item disappearing from the container. 

 Value: 1

### CHANGING

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANGING: Int
```

A flag indicating the animation that runs on those items that are changing due to a layout change not caused by items being added to or removed from the container. This transition type is not enabled by default; it can be enabled via [enableTransitionType(int)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#enableTransitionType(kotlin.Int)). 

 Value: 4

### DISAPPEARING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISAPPEARING: Int
```

A flag indicating the animation that runs on those items that are disappearing from the container. 

 Value: 3

## Public constructors

### LayoutTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LayoutTransition()
```

Constructs a LayoutTransition object. By default, the object will listen to layout events on any ViewGroup that it is set on and will run default animations for each type of layout event.

## Public methods

### addChild

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addChild(
    parent: ViewGroup!, 
    child: View!
): Unit
```

This method is called by ViewGroup when a child view is about to be added to the container. This callback starts the process of a transition; we grab the starting values, listen for changes to all of the children of the container, and start appropriate animations.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup to which the View is being added. |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View being added to the ViewGroup. |

### addTransitionListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTransitionListener(listener: LayoutTransition.TransitionListener!): Unit
```

Add a listener that will be called when the bounds of the view change due to layout processing.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener)!:The listener that will be called when layout bounds change. |

### disableTransitionType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun disableTransitionType(transitionType: Int): Unit
```

Disables the specified transitionType for this LayoutTransition object. By default, all transition types except [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int) are enabled.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int). |

### enableTransitionType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun enableTransitionType(transitionType: Int): Unit
```

Enables the specified transitionType for this LayoutTransition object. By default, a LayoutTransition listens for changes in children being added/remove/hidden/shown in the container, and runs the animations associated with those events. That is, all transition types besides [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int) are enabled by default. You can also enable [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int) animations by calling this method with the [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int) transitionType.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int). |

### getAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimator(transitionType: Int): Animator!
```

Gets the animation used during one of the transition types that may run.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose animator is being returned. |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)! | Animator The animation being used for the given transition type. |

**See Also**

- [#setAnimator(int, Animator)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setAnimator(kotlin.Int,%20android.animation.Animator)) 

### getDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(transitionType: Int): Long
```

Gets the duration on one of the animation objects used by this transition. The`transitionType`parameter determines the animation whose duration is returned.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose duration is returned. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | long The duration of the specified animation. |

**See Also**

- [android.animation.Animator#getDuration()](https://developer.android.com/reference/kotlin/android/animation/Animator#getDuration()) 

### getInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(transitionType: Int): TimeInterpolator!
```

Gets the interpolator on one of the animation objects used by this transition. The`transitionType`parameter determines the animation whose interpolator is returned.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose interpolator is being returned. |

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | TimeInterpolator The interpolator that the specified animation uses. |

**See Also**

- [android.animation.Animator#setInterpolator(TimeInterpolator)](https://developer.android.com/reference/kotlin/android/animation/Animator#setInterpolator(android.animation.TimeInterpolator)) 

### getStagger

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStagger(transitionType: Int): Long
```

Gets the length of time to delay between starting each animation during one of the change animations.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A value of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), or [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int). |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | long The length of time, in milliseconds, to delay before launching the next animation in the sequence. |

### getStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartDelay(transitionType: Int): Long
```

Gets the start delay on one of the animation objects used by this transition. The`transitionType`parameter determines the animation whose start delay is returned.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose start delay is returned. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | long The start delay of the specified animation. |

**See Also**

- [android.animation.Animator#getStartDelay()](https://developer.android.com/reference/kotlin/android/animation/Animator#getStartDelay()) 

### getTransitionListeners

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransitionListeners(): MutableList<LayoutTransition.TransitionListener!>!
```

Gets the current list of listeners for layout changes.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener)!>! | |

### hideChild

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hideChild(
    parent: ViewGroup!, 
    child: View!
): Unit
```

**Deprecated:** *Use [hideChild(android.view.ViewGroup,android.view.View,int)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#hideChild(android.view.ViewGroup,%20android.view.View,%20kotlin.Int)).* 

### hideChild

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hideChild(
    parent: ViewGroup!, 
    child: View!, 
    newVisibility: Int
): Unit
```

This method is called by ViewGroup when a child view is about to be hidden in container. This callback starts the process of a transition; we grab the starting values, listen for changes to all of the children of the container, and start appropriate animations.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The parent ViewGroup of the View being hidden. |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View being hidden. |
| `newVisibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new visibility value of the child View, either [View.GONE](https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int) or [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). |
| --- | --- |

### isChangingLayout

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isChangingLayout(): Boolean
```

Returns true if animations are running which animate layout-related properties. This essentially means that either CHANGE_APPEARING or CHANGE_DISAPPEARING animations are running, since these animations operate on layout-related properties.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if CHANGE_APPEARING or CHANGE_DISAPPEARING animations are currently running. |

### isRunning

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRunning(): Boolean
```

Returns true if any of the animations in this transition are currently running.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any animations in the transition are running. |

### isTransitionTypeEnabled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isTransitionTypeEnabled(transitionType: Int): Boolean
```

Returns whether the specified transitionType is enabled for this LayoutTransition object. By default, all transition types except [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int) are enabled.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int). |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified transitionType is currently enabled, false otherwise. |

### removeChild

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeChild(
    parent: ViewGroup!, 
    child: View!
): Unit
```

This method is called by ViewGroup when a child view is about to be removed from the container. This callback starts the process of a transition; we grab the starting values, listen for changes to all of the children of the container, and start appropriate animations.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup from which the View is being removed. |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View being removed from the ViewGroup. |

### removeTransitionListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeTransitionListener(listener: LayoutTransition.TransitionListener!): Unit
```

Remove a listener for layout changes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener)!:The listener for layout bounds change. |

### setAnimateParentHierarchy

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnimateParentHierarchy(animateParentHierarchy: Boolean): Unit
```

This flag controls whether CHANGE_APPEARING or CHANGE_DISAPPEARING animations will cause the default changing animation to be run on the parent hierarchy as well. This allows containers of transitioning views to also transition, which may be necessary in situations where the containers bounds change between the before/after states and may clip their children during the transition animations. For example, layouts with wrap_content will adjust their bounds according to the dimensions of their children.

The default changing transitions animate the bounds and scroll positions of the target views. These are the animations that will run on the parent hierarchy, not the custom animations that happen to be set on the transition. This allows custom behavior for the children of the transitioning container, but uses standard behavior of resizing/rescrolling on any changing parents.

| Parameters ||
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `animateParentHierarchy` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):A boolean value indicating whether the parents of transitioning views should also be animated during the transition. Default value is true. |

### setAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnimator(
    transitionType: Int, 
    animator: Animator!
): Unit
```

Sets the animation used during one of the transition types that may run. Any Animator object can be used, but to be most useful in the context of layout transitions, the animation should either be a ObjectAnimator or a AnimatorSet of animations including PropertyAnimators. Also, these ObjectAnimator objects should be able to get and set values on their target objects automatically. For example, a ObjectAnimator that animates the property "left" is able to set and get the`left`property from the View objects being animated by the layout transition. The transition works by setting target objects and properties dynamically, according to the pre- and post-layoout values of those objects, so having animations that can handle those properties appropriately will work best for custom animation. The dynamic setting of values is only the case for the CHANGE animations; the APPEARING and DISAPPEARING animations are simply run with the values they have.

It is also worth noting that any and all animations (and their underlying PropertyValuesHolder objects) will have their start and end values set according to the pre- and post-layout values. So, for example, a custom animation on "alpha" as the CHANGE_APPEARING animation will inherit the real value of alpha on the target object (presumably 1) as its starting and ending value when the animation begins. Animations which need to use values at the beginning and end that may not match the values queried when the transition begins may need to use a different mechanism than a standard ObjectAnimator object.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose animator is being set. |
| `animator` | [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)!:The animation being assigned. A value of`null`means that no animation will be run for the specified transitionType. |

### setDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(
    transitionType: Int, 
    duration: Long
): Unit
```

Sets the duration on one of the animation objects used by this transition. The`transitionType`parameter determines the animation whose duration is being set.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose duration is being set. |
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of time, in milliseconds, that the specified animation should run. |

**See Also**

- [android.animation.Animator#setDuration(long)](https://developer.android.com/reference/kotlin/android/animation/Animator#setDuration(kotlin.Long)) 

### setDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(duration: Long): Unit
```

Sets the duration to be used by all animations of this transition object. If you want to set the duration of just one of the animations in particular, use the [setDuration(int,long)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#setDuration(kotlin.Int,%20kotlin.Long))method.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of time, in milliseconds, that the transition animations should last. |

### setInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(
    transitionType: Int, 
    interpolator: TimeInterpolator!
): Unit
```

Sets the interpolator on one of the animation objects used by this transition. The`transitionType`parameter determines the animation whose interpolator is being set.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose interpolator is being set. |
| `interpolator` | [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)!:The interpolator that the specified animation should use. |

**See Also**

- [android.animation.Animator#setInterpolator(TimeInterpolator)](https://developer.android.com/reference/kotlin/android/animation/Animator#setInterpolator(android.animation.TimeInterpolator)) 

### setStagger

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStagger(
    transitionType: Int, 
    duration: Long
): Unit
```

Sets the length of time to delay between starting each animation during one of the change animations.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A value of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), or [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int). |
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of time, in milliseconds, to delay before launching the next animation in the sequence. |

### setStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartDelay(
    transitionType: Int, 
    delay: Long
): Unit
```

Sets the start delay on one of the animation objects used by this transition. The`transitionType`parameter determines the animation whose start delay is being set.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of [CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), [CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int), [CHANGING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGING:kotlin.Int), [APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), or [DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), which determines the animation whose start delay is being set. |
| `delay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of time, in milliseconds, to delay before starting the animation. |

**See Also**

- [android.animation.Animator#setStartDelay(long)](https://developer.android.com/reference/kotlin/android/animation/Animator#setStartDelay(kotlin.Long)) 

### showChild

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun showChild(
    parent: ViewGroup!, 
    child: View!
): Unit
```

**Deprecated:** *Use [showChild(android.view.ViewGroup,android.view.View,int)](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#showChild(android.view.ViewGroup,%20android.view.View,%20kotlin.Int)).* 

### showChild

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun showChild(
    parent: ViewGroup!, 
    child: View!, 
    oldVisibility: Int
): Unit
```

This method is called by ViewGroup when a child view is about to be made visible in the container. This callback starts the process of a transition; we grab the starting values, listen for changes to all of the children of the container, and start appropriate animations.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup in which the View is being made visible. |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View being made visible. |
| `oldVisibility` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous visibility value of the child View, either [View.GONE](https://developer.android.com/reference/kotlin/android/view/View.html#GONE:kotlin.Int) or [View.INVISIBLE](https://developer.android.com/reference/kotlin/android/view/View.html#INVISIBLE:kotlin.Int). |
| --- | --- |

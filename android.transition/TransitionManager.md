Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionManager

```
open class TransitionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.TransitionManager](../android/transition/TransitionManager.md) |

This class manages the set of transitions that fire when there is a change of `https://developer.android.com/reference/kotlin/android/transition/Scene`. To use the manager, add scenes along with transition objects with calls to `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#setTransition(android.transition.Scene,%20android.transition.Transition)` or `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#setTransition(android.transition.Scene,%20android.transition.Scene,%20android.transition.Transition)`. Setting specific transitions for scene changes is not required; by default, a Scene change will use `https://developer.android.com/reference/kotlin/android/transition/AutoTransition` to do something reasonable for most situations. Specifying other transitions for particular scene changes is only necessary if the application wants different transition behavior in these situations.

TransitionManagers can be declared in XML resource files inside the `res/transition` directory. TransitionManager resources consist of the `transitionManager`tag name, containing one or more `transition` tags, each of which describe the relationship of that transition to the from/to scene information in that tag. For example, here is a resource file that declares several scene transitions:

For each of the `fromScene` and `toScene` attributes, there is a reference to a standard XML layout file. This is equivalent to creating a scene from a layout in code by calling `https://developer.android.com/reference/kotlin/android/transition/Scene#getSceneForLayout(android.view.ViewGroup,%20kotlin.Int,%20android.content.Context)`. For the `transition` attribute, there is a reference to a resource file in the `res/transition` directory which describes that transition.
Information on XML resource descriptions for transitions can be found for `https://developer.android.com/reference/kotlin/android/R.styleable.html#Transition:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionSet:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionTarget:kotlin.IntArray`, `https://developer.android.com/reference/kotlin/android/R.styleable.html#Fade:kotlin.IntArray`, and `https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionManager:kotlin.IntArray`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#TransitionManager()()` <br /> |

| Public methods ||
|---|---|
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#beginDelayedTransition(android.view.ViewGroup)(sceneRoot: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Convenience method to animate, using the default transition, to a new scene defined by all changes within the given scene root between calling this method and the next rendering frame. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#beginDelayedTransition(android.view.ViewGroup,%20android.transition.Transition)(sceneRoot: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!, transition: https://developer.android.com/reference/kotlin/android/transition/Transition!)` Convenience method to animate to a new scene defined by all changes within the given scene root between calling this method and the next rendering frame. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#endTransitions(android.view.ViewGroup)(sceneRoot: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Ends all pending and ongoing transitions on the specified scene root. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#go(android.transition.Scene)(scene: https://developer.android.com/reference/kotlin/android/transition/Scene!)` Convenience method to simply change to the given scene using the default transition for TransitionManager. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#go(android.transition.Scene,%20android.transition.Transition)(scene: https://developer.android.com/reference/kotlin/android/transition/Scene!, transition: https://developer.android.com/reference/kotlin/android/transition/Transition!)` Convenience method to simply change to the given scene using the given transition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#setTransition(android.transition.Scene,%20android.transition.Scene,%20android.transition.Transition)(fromScene: https://developer.android.com/reference/kotlin/android/transition/Scene!, toScene: https://developer.android.com/reference/kotlin/android/transition/Scene!, transition: https://developer.android.com/reference/kotlin/android/transition/Transition!)` Sets a specific transition to occur when the given pair of scenes is exited/entered. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#setTransition(android.transition.Scene,%20android.transition.Transition)(scene: https://developer.android.com/reference/kotlin/android/transition/Scene!, transition: https://developer.android.com/reference/kotlin/android/transition/Transition!)` Sets a specific transition to occur when the given scene is entered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#transitionTo(android.transition.Scene)(scene: https://developer.android.com/reference/kotlin/android/transition/Scene!)` Change to the given scene, using the appropriate transition for this particular scene change (as specified to the TransitionManager, or the default if no such transition exists). |

## Public constructors

### TransitionManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TransitionManager()
```

## Public methods

### beginDelayedTransition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun beginDelayedTransition(sceneRoot: ViewGroup!): Unit
```

Convenience method to animate, using the default transition, to a new scene defined by all changes within the given scene root between calling this method and the next rendering frame. Equivalent to calling `https://developer.android.com/reference/kotlin/android/transition/TransitionManager#beginDelayedTransition(android.view.ViewGroup,%20android.transition.Transition)` with a value of `null` for the `transition` parameter.

| Parameters ||
|---|---|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!: The root of the View hierarchy to run the transition on. |

### beginDelayedTransition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun beginDelayedTransition(
    sceneRoot: ViewGroup!, 
    transition: Transition!
): Unit
```

Convenience method to animate to a new scene defined by all changes within the given scene root between calling this method and the next rendering frame. Calling this method causes TransitionManager to capture current values in the scene root and then post a request to run a transition on the next frame. At that time, the new values in the scene root will be captured and changes will be animated. There is no need to create a Scene; it is implied by changes which take place between calling this method and the next frame when the transition begins.

Calling this method several times before the next frame (for example, if unrelated code also wants to make dynamic changes and run a transition on the same scene root), only the first call will trigger capturing values and exiting the current scene. Subsequent calls to the method with the same scene root during the same frame will be ignored.

Passing in `null` for the transition parameter will cause the TransitionManager to use its default transition.

| Parameters ||
|---|---|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!: The root of the View hierarchy to run the transition on. |
| `transition` | [Transition](../android/transition/Transition.md)!: The transition to use for this change. A value of null causes the TransitionManager to use the default transition. |

### endTransitions

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun endTransitions(sceneRoot: ViewGroup!): Unit
```

Ends all pending and ongoing transitions on the specified scene root.

| Parameters ||
|---|---|
| `sceneRoot` | [ViewGroup](../android/view/ViewGroup.md)!: The root of the View hierarchy to end transitions on. |

### go

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun go(scene: Scene!): Unit
```

Convenience method to simply change to the given scene using the default transition for TransitionManager.

| Parameters ||
|---|---|
| `scene` | [Scene](../android/transition/Scene.md)!: The Scene to change to |

### go

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun go(
    scene: Scene!, 
    transition: Transition!
): Unit
```

Convenience method to simply change to the given scene using the given transition.

Passing in `null` for the transition parameter will result in the scene changing without any transition running, and is equivalent to calling `https://developer.android.com/reference/kotlin/android/transition/Scene#exit()` on the scene root's current scene, followed by `https://developer.android.com/reference/kotlin/android/transition/Scene#enter()` on the scene specified by the `scene` parameter.

| Parameters ||
|---|---|
| `scene` | [Scene](../android/transition/Scene.md)!: The Scene to change to |
| `transition` | [Transition](../android/transition/Transition.md)!: The transition to use for this scene change. A value of null causes the scene change to happen with no transition. |

### setTransition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransition(
    fromScene: Scene!, 
    toScene: Scene!, 
    transition: Transition!
): Unit
```

Sets a specific transition to occur when the given pair of scenes is exited/entered.

| Parameters ||
|---|---|
| `fromScene` | [Scene](../android/transition/Scene.md)!: The scene being exited when the given transition will be run |
| `toScene` | [Scene](../android/transition/Scene.md)!: The scene being entered when the given transition will be run |
| `transition` | [Transition](../android/transition/Transition.md)!: The transition that will play when the given scene is entered. A value of null will result in the default behavior of using the default transition instead. |
| --- | --- |

### setTransition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTransition(
    scene: Scene!, 
    transition: Transition!
): Unit
```

Sets a specific transition to occur when the given scene is entered.

| Parameters ||
|---|---|
| `scene` | [Scene](../android/transition/Scene.md)!: The scene which, when applied, will cause the given transition to run. |
| `transition` | [Transition](../android/transition/Transition.md)!: The transition that will play when the given scene is entered. A value of null will result in the default behavior of using the default transition instead. |

### transitionTo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun transitionTo(scene: Scene!): Unit
```

Change to the given scene, using the appropriate transition for this particular scene change (as specified to the TransitionManager, or the default if no such transition exists).

| Parameters ||
|---|---|
| `scene` | [Scene](../android/transition/Scene.md)!: The Scene to change to |

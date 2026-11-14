# TransitionInflater

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionInflater

Kotlin| [Java](https://developer.android.com/reference/android/transition/TransitionInflater "View this page in Java") 
| --- | --- |

```
open class TransitionInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.TransitionInflater](https://developer.android.com/reference/kotlin/android/transition/TransitionInflater#) |

This class inflates scenes and transitions from resource files. Information on XML resource descriptions for transitions can be found for [android.R.styleable#Transition](https://developer.android.com/reference/kotlin/android/R.styleable.html#Transition:kotlin.IntArray), [android.R.styleable#TransitionSet](https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionSet:kotlin.IntArray), [android.R.styleable#TransitionTarget](https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionTarget:kotlin.IntArray), [android.R.styleable#Fade](https://developer.android.com/reference/kotlin/android/R.styleable.html#Fade:kotlin.IntArray), and [android.R.styleable#TransitionManager](https://developer.android.com/reference/kotlin/android/R.styleable.html#TransitionManager:kotlin.IntArray).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [TransitionInflater](https://developer.android.com/reference/kotlin/android/transition/TransitionInflater#)! | [from](https://developer.android.com/reference/kotlin/android/transition/TransitionInflater#from(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Obtains the TransitionInflater from the given context. |
| open [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)! | [inflateTransition](https://developer.android.com/reference/kotlin/android/transition/TransitionInflater#inflateTransition(kotlin.Int))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Loads a [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition) object from a resource |
| open [TransitionManager](https://developer.android.com/reference/kotlin/android/transition/TransitionManager)! | [inflateTransitionManager](https://developer.android.com/reference/kotlin/android/transition/TransitionInflater#inflateTransitionManager(kotlin.Int,%20android.view.ViewGroup))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sceneRoot:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Loads a [TransitionManager](https://developer.android.com/reference/kotlin/android/transition/TransitionManager) object from a resource |
| --- | --- |

## Public methods

### from

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun from(context: Context!): TransitionInflater!
```

Obtains the TransitionInflater from the given context. 

### inflateTransition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflateTransition(resource: Int): Transition!
```

Loads a [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition) object from a resource

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the transition to load |

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------|
| [Transition](https://developer.android.com/reference/kotlin/android/transition/Transition)! | The loaded Transition object |

| Exceptions ||
|---------------------------------------------------|--------------------------------------|
| `android.content.res.Resources.NotFoundException` | when the transition cannot be loaded |

### inflateTransitionManager

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflateTransitionManager(
    resource: Int, 
    sceneRoot: ViewGroup!
): TransitionManager!
```

Loads a [TransitionManager](https://developer.android.com/reference/kotlin/android/transition/TransitionManager) object from a resource

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the transition manager to load |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------|
| [TransitionManager](https://developer.android.com/reference/kotlin/android/transition/TransitionManager)! | The loaded TransitionManager object |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------|
| `android.content.res.Resources.NotFoundException` | when the transition manager cannot be loaded |

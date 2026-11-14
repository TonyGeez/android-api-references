# TransitionInflater

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionInflater

Kotlin| [Java](../android/transition/TransitionInflater.md) 
| --- | --- |

```
open class TransitionInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.transition.TransitionInflater](../android/transition/TransitionInflater.md) |

This class inflates scenes and transitions from resource files. Information on XML resource descriptions for transitions can be found for [android.R.styleable#Transition](../android/R.styleable.md), [android.R.styleable#TransitionSet](../android/R.styleable.md), [android.R.styleable#TransitionTarget](../android/R.styleable.md), [android.R.styleable#Fade](../android/R.styleable.md), and [android.R.styleable#TransitionManager](../android/R.styleable.md).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [TransitionInflater](../android/transition/TransitionInflater.md)! | [from](../android/transition/TransitionInflater.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Obtains the TransitionInflater from the given context. |
| open [Transition](../android/transition/Transition.md)! | [inflateTransition](../android/transition/TransitionInflater.md))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Loads a [Transition](../android/transition/Transition.md) object from a resource |
| open [TransitionManager](../android/transition/TransitionManager.md)! | [inflateTransitionManager](../android/transition/TransitionInflater.md))`(`resource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sceneRoot:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Loads a [TransitionManager](../android/transition/TransitionManager.md) object from a resource |
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

Loads a [Transition](../android/transition/Transition.md) object from a resource

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the transition to load |

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------|
| [Transition](../android/transition/Transition.md)! | The loaded Transition object |

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

Loads a [TransitionManager](../android/transition/TransitionManager.md) object from a resource

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `resource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the transition manager to load |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------|
| [TransitionManager](../android/transition/TransitionManager.md)! | The loaded TransitionManager object |

| Exceptions ||
|---------------------------------------------------|----------------------------------------------|
| `android.content.res.Resources.NotFoundException` | when the transition manager cannot be loaded |

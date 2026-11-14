# AnimatorInflater

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorInflater

Kotlin| [Java](https://developer.android.com/reference/android/animation/AnimatorInflater "View this page in Java") 
| --- | --- |

```
open class AnimatorInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.AnimatorInflater](https://developer.android.com/reference/kotlin/android/animation/AnimatorInflater#) |

This class is used to instantiate animator XML files into Animator objects.

For performance reasons, inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use this inflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something*file.)

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatorInflater](https://developer.android.com/reference/kotlin/android/animation/AnimatorInflater#AnimatorInflater())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)! | [loadAnimator](https://developer.android.com/reference/kotlin/android/animation/AnimatorInflater#loadAnimator(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Loads an [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) object from a resource |
| openstatic [StateListAnimator](https://developer.android.com/reference/kotlin/android/animation/StateListAnimator)! | [loadStateListAnimator](https://developer.android.com/reference/kotlin/android/animation/AnimatorInflater#loadStateListAnimator(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Public constructors

### AnimatorInflater

```
AnimatorInflater()
```

## Public methods

### loadAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun loadAnimator(
    context: Context!, 
    id: Int
): Animator!
```

Loads an [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) object from a resource

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Application context used to access resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the animation to load |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator)! | The animator object reference by the specified id |

| Exceptions ||
|---------------------------------------------------|-------------------------------------|
| `android.content.res.Resources.NotFoundException` | when the animation cannot be loaded |

### loadStateListAnimator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun loadStateListAnimator(
    context: Context!, 
    id: Int
): StateListAnimator!
```

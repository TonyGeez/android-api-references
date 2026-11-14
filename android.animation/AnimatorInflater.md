# AnimatorInflater

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorInflater

Kotlin| [Java](AnimatorInflater.md) 
| --- | --- |

```
open class AnimatorInflater
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.AnimatorInflater](AnimatorInflater.md) |

This class is used to instantiate animator XML files into Animator objects.

For performance reasons, inflation relies heavily on pre-processing of XML files that is done at build time. Therefore, it is not currently possible to use this inflater with an XmlPullParser over a plain XML file at runtime; it only works with an XmlPullParser returned from a compiled resource (R.*something*file.)

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [AnimatorInflater](AnimatorInflater.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Animator](Animator.md)! | [loadAnimator](AnimatorInflater.md))`(`context:` ` [Context](../android.content/Context.md)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Loads an [Animator](Animator.md) object from a resource |
| openstatic [StateListAnimator](StateListAnimator.md)! | [loadStateListAnimator](AnimatorInflater.md))`(`context:` ` [Context](../android.content/Context.md)!`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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

Loads an [Animator](Animator.md) object from a resource

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:Application context used to access resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the animation to load |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [Animator](Animator.md)! | The animator object reference by the specified id |

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

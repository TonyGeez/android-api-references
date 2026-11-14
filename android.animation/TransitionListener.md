# LayoutTransition.TransitionListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionListener

Kotlin| [Java](https://developer.android.com/reference/android/animation/LayoutTransition.TransitionListener "View this page in Java") 
| --- | --- |

```
interface TransitionListener
```

| [android.animation.LayoutTransition.TransitionListener](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener#) |

This interface is used for listening to starting and ending events for transitions.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener#endTransition(android.animation.LayoutTransition,%20android.view.ViewGroup,%20android.view.View,%20kotlin.Int))`(`transition:` ` [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition)!`, `container:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This event is sent to listeners when any type of transition animation ends. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition.TransitionListener#startTransition(android.animation.LayoutTransition,%20android.view.ViewGroup,%20android.view.View,%20kotlin.Int))`(`transition:` ` [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition)!`, `container:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This event is sent to listeners when any type of transition animation begins. |

## Public methods

### endTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun endTransition(
    transition: LayoutTransition!, 
    container: ViewGroup!, 
    view: View!, 
    transitionType: Int
): Unit
```

This event is sent to listeners when any type of transition animation ends.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition)!:The LayoutTransition sending out the event. |
| `container` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup on which the transition is playing. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View object being affected by the transition animation. |
| --- | --- |
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of transition that is ending, [android.animation.LayoutTransition#APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), [android.animation.LayoutTransition#DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), [android.animation.LayoutTransition#CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), or [android.animation.LayoutTransition#CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int). |

### startTransition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startTransition(
    transition: LayoutTransition!, 
    container: ViewGroup!, 
    view: View!, 
    transitionType: Int
): Unit
```

This event is sent to listeners when any type of transition animation begins.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transition` | [LayoutTransition](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition)!:The LayoutTransition sending out the event. |
| `container` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup on which the transition is playing. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View object being affected by the transition animation. |
| --- | --- |
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of transition that is beginning, [android.animation.LayoutTransition#APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#APPEARING:kotlin.Int), [android.animation.LayoutTransition#DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#DISAPPEARING:kotlin.Int), [android.animation.LayoutTransition#CHANGE_APPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_APPEARING:kotlin.Int), or [android.animation.LayoutTransition#CHANGE_DISAPPEARING](https://developer.android.com/reference/kotlin/android/animation/LayoutTransition#CHANGE_DISAPPEARING:kotlin.Int). |

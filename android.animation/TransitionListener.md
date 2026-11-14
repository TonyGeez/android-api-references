# LayoutTransition.TransitionListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransitionListener

Kotlin| [Java](../android/animation/LayoutTransition.TransitionListener.md) 
| --- | --- |

```
interface TransitionListener
```

| [android.animation.LayoutTransition.TransitionListener](../android/animation/LayoutTransition.TransitionListener.md) |

This interface is used for listening to starting and ending events for transitions.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [endTransition](../android/animation/LayoutTransition.TransitionListener.md))`(`transition:` ` [LayoutTransition](LayoutTransition.md)!`, `container:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `view:` ` [View](../android.view/View.md)!`, `transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This event is sent to listeners when any type of transition animation ends. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startTransition](../android/animation/LayoutTransition.TransitionListener.md))`(`transition:` ` [LayoutTransition](LayoutTransition.md)!`, `container:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `view:` ` [View](../android.view/View.md)!`, `transitionType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This event is sent to listeners when any type of transition animation begins. |

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
| `transition` | [LayoutTransition](LayoutTransition.md)!:The LayoutTransition sending out the event. |
| `container` | [ViewGroup](../android.view/ViewGroup.md)!:The ViewGroup on which the transition is playing. |
| `view` | [View](../android.view/View.md)!:The View object being affected by the transition animation. |
| --- | --- |
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of transition that is ending, [android.animation.LayoutTransition#APPEARING](LayoutTransition.md), [android.animation.LayoutTransition#DISAPPEARING](LayoutTransition.md), [android.animation.LayoutTransition#CHANGE_APPEARING](LayoutTransition.md), or [android.animation.LayoutTransition#CHANGE_DISAPPEARING](LayoutTransition.md). |

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
| `transition` | [LayoutTransition](LayoutTransition.md)!:The LayoutTransition sending out the event. |
| `container` | [ViewGroup](../android.view/ViewGroup.md)!:The ViewGroup on which the transition is playing. |
| `view` | [View](../android.view/View.md)!:The View object being affected by the transition animation. |
| --- | --- |
| `transitionType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of transition that is beginning, [android.animation.LayoutTransition#APPEARING](LayoutTransition.md), [android.animation.LayoutTransition#DISAPPEARING](LayoutTransition.md), [android.animation.LayoutTransition#CHANGE_APPEARING](LayoutTransition.md), or [android.animation.LayoutTransition#CHANGE_DISAPPEARING](LayoutTransition.md). |

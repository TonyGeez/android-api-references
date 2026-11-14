# ViewAnimationUtils

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewAnimationUtils

Kotlin| [Java](ViewAnimationUtils.md) 
| --- | --- |

```
class ViewAnimationUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewAnimationUtils](ViewAnimationUtils.md) |

Defines common utilities for working with View's animations.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Animator](../android.animation/Animator.md)! | [createCircularReveal](ViewAnimationUtils.md))`(`view:` ` [View](View.md)!`, `centerX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `centerY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `endRadius:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Returns an Animator which can animate a clipping circle. |

## Public methods

### createCircularReveal

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createCircularReveal(
    view: View!, 
    centerX: Int, 
    centerY: Int, 
    startRadius: Float, 
    endRadius: Float
): Animator!
```

Returns an Animator which can animate a clipping circle.

Any shadow cast by the View will respect the circular clip from this animator.

Only a single non-rectangular clip can be applied on a View at any time. Views clipped by a circular reveal animation take priority over [View Outline clipping](View.md)).

Note that the animation returned here is a one-shot animation. It cannot be re-used, and once started it cannot be paused or resumed. It is also an asynchronous animation that automatically runs off of the UI thread. As a result [AnimatorListener.onAnimationEnd(Animator)](../android/animation/Animator.AnimatorListener.md))will occur after the animation has ended, but it may be delayed depending on thread responsiveness.

Note that if any start delay is set on the reveal animator, the start radius will not be applied to the reveal circle until the start delay has passed. If it's desired to set a start radius on the reveal circle during the start delay, one workaround could be adding an animator with the same start and end radius. For example: 

```kotlin
<code>
  public static Animator createRevealWithDelay(View view, int centerX, int centerY, float startRadius, float endRadius) {
      Animator delayAnimator = ViewAnimationUtils.createCircularReveal(view, centerX, centerY, startRadius, startRadius);
      delayAnimator.setDuration(delayTimeMS);
      Animator revealAnimator = ViewAnimationUtils.createCircularReveal(view, centerX, centerY, startRadius, endRadius);
      AnimatorSet set = new AnimatorSet();
      set.playSequentially(delayAnimator, revealAnimator);
      return set;
  }
  </code>
```

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](View.md)!:The View will be clipped to the animating circle. |
| `centerX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The x coordinate of the center of the animating circle, relative to`view`. |
| `centerY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The y coordinate of the center of the animating circle, relative to`view`. |
| --- | --- |
| `startRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The starting radius of the animating circle. |
| `endRadius` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The ending radius of the animating circle. |

# TouchUtils

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TouchUtils

Kotlin| [Java](https://developer.android.com/reference/android/test/TouchUtils "View this page in Java") 
| --- | --- |

```
open class TouchUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.TouchUtils](https://developer.android.com/reference/kotlin/android/test/TouchUtils#) |

| **This class was deprecated in API level 24.**
|
| Use [Espresso UI testing framework](https://developer.android.com/training/testing/ui-testing/espresso-testing.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Reusable methods for generating touch events. These methods can be used with InstrumentationTestCase or ActivityInstrumentationTestCase2 to simulate user interaction with the application through a touch screen.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [TouchUtils](https://developer.android.com/reference/kotlin/android/test/TouchUtils#TouchUtils())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clickView](https://developer.android.com/reference/kotlin/android/test/TouchUtils#clickView(android.test.InstrumentationTestCase,%20android.view.View))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and releasing. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drag](https://developer.android.com/reference/kotlin/android/test/TouchUtils#drag(android.test.ActivityInstrumentationTestCase,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `fromX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fromY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stepCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a specific location and dragging to a new location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drag](https://developer.android.com/reference/kotlin/android/test/TouchUtils#drag(android.test.InstrumentationTestCase,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `fromX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toX:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `fromY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `toY:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `stepCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a specific location and dragging to a new location. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragQuarterScreenDown](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenDown(android.test.ActivityInstrumentationTestCase))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`)` Simulate touching in the center of the screen and dragging one quarter of the way down |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragQuarterScreenDown](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenDown(android.test.InstrumentationTestCase,%20android.app.Activity))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` Simulate touching in the center of the screen and dragging one quarter of the way down |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragQuarterScreenUp](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenUp(android.test.ActivityInstrumentationTestCase))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`)` Simulate touching in the center of the screen and dragging one quarter of the way up |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragQuarterScreenUp](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenUp(android.test.InstrumentationTestCase,%20android.app.Activity))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`)` Simulate touching in the center of the screen and dragging one quarter of the way up |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewBy](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewBy(android.test.ActivityInstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `deltaX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `deltaY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it by the specified amount. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewBy](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewBy(android.test.InstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `deltaX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `deltaY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it by the specified amount. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewTo](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewTo(android.test.ActivityInstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it to a specified location. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewTo](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewTo(android.test.InstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it to a specified location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToBottom](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToBottom(android.test.ActivityInstrumentationTestCase,%20android.view.View))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and dragging to the bottom of the screen. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToBottom](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToBottom(android.test.ActivityInstrumentationTestCase,%20android.view.View,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `stepCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching the center of a view and dragging to the bottom of the screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToBottom](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToBottom(android.test.InstrumentationTestCase,%20android.app.Activity,%20android.view.View))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and dragging to the bottom of the screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToBottom](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToBottom(android.test.InstrumentationTestCase,%20android.app.Activity,%20android.view.View,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `stepCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching the center of a view and dragging to the bottom of the screen. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToTop](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToTop(android.test.ActivityInstrumentationTestCase,%20android.view.View))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and dragging to the top of the screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToTop](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToTop(android.test.ActivityInstrumentationTestCase,%20android.view.View,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `stepCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching the center of a view and dragging to the top of the screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToTop](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToTop(android.test.InstrumentationTestCase,%20android.view.View))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and dragging to the top of the screen. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dragViewToTop](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToTop(android.test.InstrumentationTestCase,%20android.view.View,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `stepCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching the center of a view and dragging to the top of the screen. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewToX](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToX(android.test.ActivityInstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it to a specified location. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewToX](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToX(android.test.InstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toX:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it to a specified location. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewToY](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToY(android.test.ActivityInstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it to a specified location. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [dragViewToY](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragViewToY(android.test.InstrumentationTestCase,%20android.view.View,%20kotlin.Int,%20kotlin.Int))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toY:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Simulate touching a view and dragging it to a specified location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [longClickView](https://developer.android.com/reference/kotlin/android/test/TouchUtils#longClickView(android.test.ActivityInstrumentationTestCase,%20android.view.View))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view, holding until it is a long press, and then releasing. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [longClickView](https://developer.android.com/reference/kotlin/android/test/TouchUtils#longClickView(android.test.InstrumentationTestCase,%20android.view.View))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view, holding until it is a long press, and then releasing. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrollToBottom](https://developer.android.com/reference/kotlin/android/test/TouchUtils#scrollToBottom(android.test.ActivityInstrumentationTestCase,%20android.view.ViewGroup))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Scroll a ViewGroup to the bottom by repeatedly calling [dragQuarterScreenUp(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenUp(android.test.InstrumentationTestCase,%20android.app.Activity)) |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrollToBottom](https://developer.android.com/reference/kotlin/android/test/TouchUtils#scrollToBottom(android.test.InstrumentationTestCase,%20android.app.Activity,%20android.view.ViewGroup))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `v:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Scroll a ViewGroup to the bottom by repeatedly calling [dragQuarterScreenUp(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenUp(android.test.InstrumentationTestCase,%20android.app.Activity)) |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrollToTop](https://developer.android.com/reference/kotlin/android/test/TouchUtils#scrollToTop(android.test.ActivityInstrumentationTestCase,%20android.view.ViewGroup))`(`test:` ` [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!>!`, `v:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Scroll a ViewGroup to the top by repeatedly calling [dragQuarterScreenDown(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenDown(android.test.InstrumentationTestCase,%20android.app.Activity)) |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrollToTop](https://developer.android.com/reference/kotlin/android/test/TouchUtils#scrollToTop(android.test.InstrumentationTestCase,%20android.app.Activity,%20android.view.ViewGroup))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!`, `v:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Scroll a ViewGroup to the top by repeatedly calling [dragQuarterScreenDown(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenDown(android.test.InstrumentationTestCase,%20android.app.Activity)) |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [tapView](https://developer.android.com/reference/kotlin/android/test/TouchUtils#tapView(android.test.InstrumentationTestCase,%20android.view.View))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and releasing quickly (before the tap timeout). |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [touchAndCancelView](https://developer.android.com/reference/kotlin/android/test/TouchUtils#touchAndCancelView(android.test.InstrumentationTestCase,%20android.view.View))`(`test:` ` [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!`, `v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Simulate touching the center of a view and cancelling (so no onClick should fire, etc). |

## Public constructors

### TouchUtils

```
TouchUtils()
```

## Public methods

### clickView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun clickView(
    test: InstrumentationTestCase!, 
    v: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and releasing.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be clicked |

### drag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun drag(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    fromX: Float, 
    toX: Float, 
    fromY: Float, 
    toY: Float, 
    stepCount: Int
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching a specific location and dragging to a new location.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `fromX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X coordinate of the initial touch, in screen coordinates |
| `toX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Xcoordinate of the drag destination, in screen coordinates |
| --- | --- |
| `fromY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X coordinate of the initial touch, in screen coordinates |
| `toY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Y coordinate of the drag destination, in screen coordinates |
| `stepCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How many move steps to include in the drag |
| --- | --- |

### drag

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun drag(
    test: InstrumentationTestCase!, 
    fromX: Float, 
    toX: Float, 
    fromY: Float, 
    toY: Float, 
    stepCount: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching a specific location and dragging to a new location.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `fromX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X coordinate of the initial touch, in screen coordinates |
| `toX` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Xcoordinate of the drag destination, in screen coordinates |
| --- | --- |
| `fromY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):X coordinate of the initial touch, in screen coordinates |
| `toY` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Y coordinate of the drag destination, in screen coordinates |
| `stepCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How many move steps to include in the drag |
| --- | --- |

### dragQuarterScreenDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragQuarterScreenDown(test: ActivityInstrumentationTestCase<Activity!>!): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching in the center of the screen and dragging one quarter of the way down

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |

### dragQuarterScreenDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragQuarterScreenDown(
    test: InstrumentationTestCase!, 
    activity: Activity!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching in the center of the screen and dragging one quarter of the way down

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!:The activity that is in the foreground of the test case |

### dragQuarterScreenUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragQuarterScreenUp(test: ActivityInstrumentationTestCase<Activity!>!): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching in the center of the screen and dragging one quarter of the way up

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |

### dragQuarterScreenUp

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragQuarterScreenUp(
    test: InstrumentationTestCase!, 
    activity: Activity!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching in the center of the screen and dragging one quarter of the way up

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!:The activity that is in the foreground of the test case |

### dragViewBy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewBy(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!, 
    gravity: Int, 
    deltaX: Int, 
    deltaY: Int
): Int
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching a view and dragging it by the specified amount.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `deltaX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Amount to drag horizontally in pixels |
| `deltaY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Amount to drag vertically in pixels |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewBy

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewBy(
    test: InstrumentationTestCase!, 
    v: View!, 
    gravity: Int, 
    deltaX: Int, 
    deltaY: Int
): Int
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching a view and dragging it by the specified amount.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `deltaX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Amount to drag horizontally in pixels |
| `deltaY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Amount to drag vertically in pixels |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewTo(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!, 
    gravity: Int, 
    toX: Int, 
    toY: Int
): Int
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching a view and dragging it to a specified location.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `toX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |
| `toY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewTo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewTo(
    test: InstrumentationTestCase!, 
    v: View!, 
    gravity: Int, 
    toX: Int, 
    toY: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Simulate touching a view and dragging it to a specified location.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `toX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |
| `toY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewToBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToBottom(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching the center of a view and dragging to the bottom of the screen.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |

### dragViewToBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToBottom(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!, 
    stepCount: Int
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching the center of a view and dragging to the bottom of the screen.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `stepCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How many move steps to include in the drag |
| --- | --- |

### dragViewToBottom

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToBottom(
    test: InstrumentationTestCase!, 
    activity: Activity!, 
    v: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and dragging to the bottom of the screen.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!:The activity that is in the foreground of the test case |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| --- | --- |

### dragViewToBottom

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToBottom(
    test: InstrumentationTestCase!, 
    activity: Activity!, 
    v: View!, 
    stepCount: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and dragging to the bottom of the screen.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!:The activity that is in the foreground of the test case |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| --- | --- |
| `stepCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How many move steps to include in the drag |

### dragViewToTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToTop(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching the center of a view and dragging to the top of the screen.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |

### dragViewToTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToTop(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!, 
    stepCount: Int
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching the center of a view and dragging to the top of the screen.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `stepCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How many move steps to include in the drag |
| --- | --- |

### dragViewToTop

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToTop(
    test: InstrumentationTestCase!, 
    v: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and dragging to the top of the screen.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |

### dragViewToTop

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToTop(
    test: InstrumentationTestCase!, 
    v: View!, 
    stepCount: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and dragging to the top of the screen.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `stepCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How many move steps to include in the drag |
| --- | --- |

### dragViewToX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToX(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!, 
    gravity: Int, 
    toX: Int
): Int
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching a view and dragging it to a specified location. Only moves horizontally.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `toX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewToX

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToX(
    test: InstrumentationTestCase!, 
    v: View!, 
    gravity: Int, 
    toX: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Simulate touching a view and dragging it to a specified location. Only moves horizontally.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `toX` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewToY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToY(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!, 
    gravity: Int, 
    toY: Int
): Int
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching a view and dragging it to a specified location. Only moves vertically.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `toY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### dragViewToY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dragViewToY(
    test: InstrumentationTestCase!, 
    v: View!, 
    gravity: Int, 
    toY: Int
): Int
```

**Deprecated:** *Deprecated in Java.*

Simulate touching a view and dragging it to a specified location. Only moves vertically.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be dragged |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Which part of the view to use for the initial down event. A combination of (TOP, CENTER_VERTICAL, BOTTOM) and (LEFT, CENTER_HORIZONTAL, RIGHT) |
| --- | --- |
| `toY` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Final location of the view after dragging |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | distance in pixels covered by the drag |

### longClickView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun longClickView(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: View!
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Simulate touching the center of a view, holding until it is a long press, and then releasing.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be clicked |

### longClickView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun longClickView(
    test: InstrumentationTestCase!, 
    v: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view, holding until it is a long press, and then releasing.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be clicked |

### scrollToBottom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scrollToBottom(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: ViewGroup!
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Scroll a ViewGroup to the bottom by repeatedly calling [dragQuarterScreenUp(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenUp(android.test.InstrumentationTestCase,%20android.app.Activity))

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup that should be dragged |

### scrollToBottom

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scrollToBottom(
    test: InstrumentationTestCase!, 
    activity: Activity!, 
    v: ViewGroup!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Scroll a ViewGroup to the bottom by repeatedly calling [dragQuarterScreenUp(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenUp(android.test.InstrumentationTestCase,%20android.app.Activity))

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!:The activity that is in the foreground of the test case |
| `v` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup that should be dragged |
| --- | --- |

### scrollToTop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scrollToTop(
    test: ActivityInstrumentationTestCase<Activity!>!, 
    v: ViewGroup!
): Unit
```

**Deprecated:** * [android.test.ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase) is deprecated in favor of [android.test.ActivityInstrumentationTestCase2](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase2), which provides more options for configuring the Activity under test*

Scroll a ViewGroup to the top by repeatedly calling [dragQuarterScreenDown(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenDown(android.test.InstrumentationTestCase,%20android.app.Activity))

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [ActivityInstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/ActivityInstrumentationTestCase)\< [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!\>!:The test case that is being run |
| `v` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup that should be dragged |

### scrollToTop

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scrollToTop(
    test: InstrumentationTestCase!, 
    activity: Activity!, 
    v: ViewGroup!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Scroll a ViewGroup to the top by repeatedly calling [dragQuarterScreenDown(android.test.InstrumentationTestCase,android.app.Activity)](https://developer.android.com/reference/kotlin/android/test/TouchUtils#dragQuarterScreenDown(android.test.InstrumentationTestCase,%20android.app.Activity))

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)!:The activity that is in the foreground of the test case |
| `v` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The ViewGroup that should be dragged |
| --- | --- |

### tapView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tapView(
    test: InstrumentationTestCase!, 
    v: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and releasing quickly (before the tap timeout).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be clicked |

### touchAndCancelView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun touchAndCancelView(
    test: InstrumentationTestCase!, 
    v: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Simulate touching the center of a view and cancelling (so no onClick should fire, etc).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)!:The test case that is being run |
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be clicked |

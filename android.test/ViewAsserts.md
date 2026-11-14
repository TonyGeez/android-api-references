# ViewAsserts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewAsserts

Kotlin| [Java](https://developer.android.com/reference/android/test/ViewAsserts "View this page in Java") 

```
open class ViewAsserts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.ViewAsserts](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#) |

| **This class was deprecated in API level 24.**
|
| Use [Espresso View Matchers](https://developer.android.com/reference/android/support/test/espresso/matcher/ViewMatchers.html) instead. New test should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html). For more information about UI testing, take the [Espresso UI testing](https://developer.android.com/tools/testing-support-library/index.html) training.

Some useful assertions about views.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertBaselineAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertBaselineAligned(android.view.View,%20android.view.View))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that two views are aligned on their baseline, that is that their baselines are on the same y location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertBottomAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertBottomAligned(android.view.View,%20android.view.View))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that two views are bottom aligned, that is that their bottom edges are on the same y location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertBottomAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertBottomAligned(android.view.View,%20android.view.View,%20kotlin.Int))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are bottom aligned, that is that their bottom edges are on the same y location, with respect to the specified margin. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertGroupContains](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertGroupContains(android.view.ViewGroup,%20android.view.View))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that the specified group contains a specific child once and only once. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertGroupIntegrity](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertGroupIntegrity(android.view.ViewGroup))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Assert the specified group's integrity. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertGroupNotContains](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertGroupNotContains(android.view.ViewGroup,%20android.view.View))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`, `child:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that the specified group does not contain a specific child. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertHasScreenCoordinates](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertHasScreenCoordinates(android.view.View,%20android.view.View,%20kotlin.Int,%20kotlin.Int))`(`origin:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that a view has a particular x and y position on the visible screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertHorizontalCenterAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertHorizontalCenterAligned(android.view.View,%20android.view.View))`(`reference:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `test:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that the`test`view is horizontally center aligned with respect to the`reference`view. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertLeftAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertLeftAligned(android.view.View,%20android.view.View))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that two views are left aligned, that is that their left edges are on the same x location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertLeftAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertLeftAligned(android.view.View,%20android.view.View,%20kotlin.Int))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are left aligned, that is that their left edges are on the same x location, with respect to the specified margin. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertOffScreenAbove](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertOffScreenAbove(android.view.View,%20android.view.View))`(`origin:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that view is above the visible screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertOffScreenBelow](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertOffScreenBelow(android.view.View,%20android.view.View))`(`origin:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that view is below the visible screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertOnScreen](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertOnScreen(android.view.View,%20android.view.View))`(`origin:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that view is on the screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertRightAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertRightAligned(android.view.View,%20android.view.View))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that two views are right aligned, that is that their right edges are on the same x location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertRightAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertRightAligned(android.view.View,%20android.view.View,%20kotlin.Int))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are right aligned, that is that their right edges are on the same x location, with respect to the specified margin. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertTopAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertTopAligned(android.view.View,%20android.view.View))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that two views are top aligned, that is that their top edges are on the same y location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertTopAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertTopAligned(android.view.View,%20android.view.View,%20kotlin.Int))`(`first:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `second:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are top aligned, that is that their top edges are on the same y location, with respect to the specified margin. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertVerticalCenterAligned](https://developer.android.com/reference/kotlin/android/test/ViewAsserts#assertVerticalCenterAligned(android.view.View,%20android.view.View))`(`reference:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `test:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Assert that the`test`view is vertically center aligned with respect to the`reference`view. |

## Public methods

### assertBaselineAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertBaselineAligned(
    first: View!, 
    second: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are aligned on their baseline, that is that their baselines are on the same y location.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |

### assertBottomAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertBottomAligned(
    first: View!, 
    second: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are bottom aligned, that is that their bottom edges are on the same y location.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |

### assertBottomAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertBottomAligned(
    first: View!, 
    second: View!, 
    margin: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are bottom aligned, that is that their bottom edges are on the same y location, with respect to the specified margin.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |

### assertGroupContains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertGroupContains(
    parent: ViewGroup!, 
    child: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that the specified group contains a specific child once and only once.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The group |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The child that should belong to group |

### assertGroupIntegrity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertGroupIntegrity(parent: ViewGroup!): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert the specified group's integrity. The children count should be \>= 0 and each child should be non-null.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The group whose integrity to check |

### assertGroupNotContains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertGroupNotContains(
    parent: ViewGroup!, 
    child: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that the specified group does not contain a specific child.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The group |
| `child` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The child that should not belong to group |

### assertHasScreenCoordinates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertHasScreenCoordinates(
    origin: View!, 
    view: View!, 
    x: Int, 
    y: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that a view has a particular x and y position on the visible screen.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `origin` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The root view of the screen. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The expected x coordinate. |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The expected y coordinate. |

### assertHorizontalCenterAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertHorizontalCenterAligned(
    reference: View!, 
    test: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that the`test`view is horizontally center aligned with respect to the`reference`view.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `reference` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The reference view |
| `test` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be center aligned with the reference view |

### assertLeftAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertLeftAligned(
    first: View!, 
    second: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are left aligned, that is that their left edges are on the same x location.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |

### assertLeftAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertLeftAligned(
    first: View!, 
    second: View!, 
    margin: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are left aligned, that is that their left edges are on the same x location, with respect to the specified margin.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |

### assertOffScreenAbove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertOffScreenAbove(
    origin: View!, 
    view: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that view is above the visible screen.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `origin` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:Te root view of the screen. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view |

### assertOffScreenBelow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertOffScreenBelow(
    origin: View!, 
    view: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that view is below the visible screen.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `origin` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The root view of the screen. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view |

### assertOnScreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertOnScreen(
    origin: View!, 
    view: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that view is on the screen.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `origin` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The root view of the screen. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view. |

### assertRightAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertRightAligned(
    first: View!, 
    second: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are right aligned, that is that their right edges are on the same x location.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |

### assertRightAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertRightAligned(
    first: View!, 
    second: View!, 
    margin: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are right aligned, that is that their right edges are on the same x location, with respect to the specified margin.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |

### assertTopAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertTopAligned(
    first: View!, 
    second: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are top aligned, that is that their top edges are on the same y location.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |

### assertTopAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertTopAligned(
    first: View!, 
    second: View!, 
    margin: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that two views are top aligned, that is that their top edges are on the same y location, with respect to the specified margin.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `first` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The first view |
| `second` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |

### assertVerticalCenterAligned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertVerticalCenterAligned(
    reference: View!, 
    test: View!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert that the`test`view is vertically center aligned with respect to the`reference`view.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `reference` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The reference view |
| `test` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view that should be center aligned with the reference view |

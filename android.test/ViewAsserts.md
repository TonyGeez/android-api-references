# ViewAsserts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewAsserts

Kotlin| [Java](ViewAsserts.md) 
| --- | --- |

```
open class ViewAsserts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.ViewAsserts](ViewAsserts.md) |

| **This class was deprecated in API level 24.**
|
| Use [Espresso View Matchers](../android/support/test/espresso/matcher/ViewMatchers.md) instead. New test should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html). For more information about UI testing, take the [Espresso UI testing](https://developer.android.com/tools/testing-support-library/index.html) training.

Some useful assertions about views.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertBaselineAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`)` Assert that two views are aligned on their baseline, that is that their baselines are on the same y location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertBottomAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`)` Assert that two views are bottom aligned, that is that their bottom edges are on the same y location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertBottomAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are bottom aligned, that is that their bottom edges are on the same y location, with respect to the specified margin. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertGroupContains](ViewAsserts.md))`(`parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `child:` ` [View](../android.view/View.md)!`)` Assert that the specified group contains a specific child once and only once. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertGroupIntegrity](ViewAsserts.md))`(`parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Assert the specified group's integrity. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertGroupNotContains](ViewAsserts.md))`(`parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`, `child:` ` [View](../android.view/View.md)!`)` Assert that the specified group does not contain a specific child. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertHasScreenCoordinates](ViewAsserts.md))`(`origin:` ` [View](../android.view/View.md)!`, `view:` ` [View](../android.view/View.md)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that a view has a particular x and y position on the visible screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertHorizontalCenterAligned](ViewAsserts.md))`(`reference:` ` [View](../android.view/View.md)!`, `test:` ` [View](../android.view/View.md)!`)` Assert that the`test`view is horizontally center aligned with respect to the`reference`view. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertLeftAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`)` Assert that two views are left aligned, that is that their left edges are on the same x location. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertLeftAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are left aligned, that is that their left edges are on the same x location, with respect to the specified margin. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertOffScreenAbove](ViewAsserts.md))`(`origin:` ` [View](../android.view/View.md)!`, `view:` ` [View](../android.view/View.md)!`)` Assert that view is above the visible screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertOffScreenBelow](ViewAsserts.md))`(`origin:` ` [View](../android.view/View.md)!`, `view:` ` [View](../android.view/View.md)!`)` Assert that view is below the visible screen. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertOnScreen](ViewAsserts.md))`(`origin:` ` [View](../android.view/View.md)!`, `view:` ` [View](../android.view/View.md)!`)` Assert that view is on the screen. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertRightAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`)` Assert that two views are right aligned, that is that their right edges are on the same x location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertRightAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are right aligned, that is that their right edges are on the same x location, with respect to the specified margin. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertTopAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`)` Assert that two views are top aligned, that is that their top edges are on the same y location. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertTopAligned](ViewAsserts.md))`(`first:` ` [View](../android.view/View.md)!`, `second:` ` [View](../android.view/View.md)!`, `margin:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Assert that two views are top aligned, that is that their top edges are on the same y location, with respect to the specified margin. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertVerticalCenterAligned](ViewAsserts.md))`(`reference:` ` [View](../android.view/View.md)!`, `test:` ` [View](../android.view/View.md)!`)` Assert that the`test`view is vertically center aligned with respect to the`reference`view. |
| --- | --- |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |
| --- | --- |

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
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:The group |
| `child` | [View](../android.view/View.md)!:The child that should belong to group |

### assertGroupIntegrity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun assertGroupIntegrity(parent: ViewGroup!): Unit
```

**Deprecated:** *Deprecated in Java.*

Assert the specified group's integrity. The children count should be \>= 0 and each child should be non-null.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:The group whose integrity to check |

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
| `parent` | [ViewGroup](../android.view/ViewGroup.md)!:The group |
| `child` | [View](../android.view/View.md)!:The child that should not belong to group |

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
| `origin` | [View](../android.view/View.md)!:The root view of the screen. |
| `view` | [View](../android.view/View.md)!:The view. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The expected x coordinate. |
| --- | --- |
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
| `reference` | [View](../android.view/View.md)!:The reference view |
| `test` | [View](../android.view/View.md)!:The view that should be center aligned with the reference view |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |
| --- | --- |

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
| `origin` | [View](../android.view/View.md)!:Te root view of the screen. |
| `view` | [View](../android.view/View.md)!:The view |

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
| `origin` | [View](../android.view/View.md)!:The root view of the screen. |
| `view` | [View](../android.view/View.md)!:The view |

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
| `origin` | [View](../android.view/View.md)!:The root view of the screen. |
| `view` | [View](../android.view/View.md)!:The view. |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |
| --- | --- |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |

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
| `first` | [View](../android.view/View.md)!:The first view |
| `second` | [View](../android.view/View.md)!:The second view |
| `margin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The margin between the first view and the second view |
| --- | --- |

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
| `reference` | [View](../android.view/View.md)!:The reference view |
| `test` | [View](../android.view/View.md)!:The view that should be center aligned with the reference view |

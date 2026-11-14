# GridLayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GridLayoutAnimationController

Kotlin | [Java](../android/view/animation/GridLayoutAnimationController.md) 
| --- | --- |

```
open class GridLayoutAnimationController : LayoutAnimationController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.animation.LayoutAnimationController](../android/view/animation/LayoutAnimationController.md) ||
| | ↳ | [android.view.animation.GridLayoutAnimationController](../android/view/animation/GridLayoutAnimationController.md) |

A layout animation controller is used to animated a grid layout's children. While [LayoutAnimationController](../android/view/animation/LayoutAnimationController.md) relies only on the index of the child in the view group to compute the animation delay, this class uses both the X and Y coordinates of the child within a grid. In addition, the animation direction can be controlled. The default direction is `DIRECTION_LEFT_TO_RIGHT | DIRECTION_TOP_TO_BOTTOM`. You can also set the animation priority to columns or rows. The default priority is none. Information used to compute the animation delay of each child are stored in an instance of [android.view.animation.GridLayoutAnimationController.AnimationParameters](../android/view/animation/GridLayoutAnimationController.AnimationParameters.md), itself stored in the [android.view.ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md) of the view.
| --- | --- |

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AnimationParameters](../android/view/animation/GridLayoutAnimationController.AnimationParameters.md) The set of parameters that has to be attached to each view contained in the view group animated by the grid layout animation controller. |

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [`android:columnDelay`](../android/view/animation/GridLayoutAnimationController.md) | Fraction of the animation duration used to delay the beginning of the animation of each column. |
| [`android:direction`](../android/view/animation/GridLayoutAnimationController.md) | Direction of the animation in the grid. |
| [`android:directionPriority`](../android/view/animation/GridLayoutAnimationController.md) | Priority of the rows and columns. |
| --- | --- |
| [`android:rowDelay`](../android/view/animation/GridLayoutAnimationController.md) | Fraction of the animation duration used to delay the beginning of the animation of each row. |

| Inherited XML attributes ||
|---|---|
| From class [LayoutAnimationController](../android/view/animation/LayoutAnimationController.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:animation](../android/view/animation/LayoutAnimationController.md) | Animation to use on each child. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:animationOrder](../android/view/animation/LayoutAnimationController.md) | The order in which the animations will be started. Must be one of the following constant values. | Constant | Value | Description | |----------|-------|----------------------------------------------| | normal | 0 | Animations are started in the natural order. | | random | 2 | Animations are started randomly. | | reverse | 1 | Animations are started in the reverse order. | <br /> | | [android:delay](../android/view/animation/LayoutAnimationController.md) | Fraction of the animation duration used to delay the beginning of the animation of each child. May be a floating point value, such as "`1.2`". May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. <br /> | | [android:interpolator](../android/view/animation/LayoutAnimationController.md) | Interpolator used to interpolate the delay between the start of each animation. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | ||

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_BOTTOM_TO_TOP](../android/view/animation/GridLayoutAnimationController.md) Animates the children starting from the bottom of the grid to the top. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_HORIZONTAL_MASK](../android/view/animation/GridLayoutAnimationController.md) Bitmask used to retrieve the horizontal component of the direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_LEFT_TO_RIGHT](../android/view/animation/GridLayoutAnimationController.md) Animates the children starting from the left of the grid to the right. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_RIGHT_TO_LEFT](../android/view/animation/GridLayoutAnimationController.md) Animates the children starting from the right of the grid to the left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_TOP_TO_BOTTOM](../android/view/animation/GridLayoutAnimationController.md) Animates the children starting from the top of the grid to the bottom. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_VERTICAL_MASK](../android/view/animation/GridLayoutAnimationController.md) Bitmask used to retrieve the vertical component of the direction. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_COLUMN](../android/view/animation/GridLayoutAnimationController.md) Columns are animated first. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_NONE](../android/view/animation/GridLayoutAnimationController.md) Rows and columns are animated at the same time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_ROW](../android/view/animation/GridLayoutAnimationController.md) Rows are animated first. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [LayoutAnimationController](../android/view/animation/LayoutAnimationController.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_NORMAL](../android/view/animation/LayoutAnimationController.md) Distributes the animation delays in the order in which view were added to their view group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_RANDOM](../android/view/animation/LayoutAnimationController.md) Randomly distributes the animation delays. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_REVERSE](../android/view/animation/LayoutAnimationController.md) Distributes the animation delays in the reverse order in which view were added to their view group. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GridLayoutAnimationController](../android/view/animation/GridLayoutAnimationController.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` Creates a new grid layout animation controller from external resources. |
| [GridLayoutAnimationController](../android/view/animation/GridLayoutAnimationController.md))`(`animation:` ` [Animation](../android/view/animation/Animation.md)!`)` Creates a new layout animation controller with a delay of 50% for both rows and columns and the specified animation. |
| [GridLayoutAnimationController](../android/view/animation/GridLayoutAnimationController.md))`(`animation:` ` [Animation](../android/view/animation/Animation.md)!`, `columnDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `rowDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new layout animation controller with the specified delays and the specified animation. |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getColumnDelay](../android/view/animation/GridLayoutAnimationController.md))`()` Returns the delay by which the children's animation are offset from one column to the other. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirection](../android/view/animation/GridLayoutAnimationController.md))`()` Returns the direction of the animation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirectionPriority](../android/view/animation/GridLayoutAnimationController.md))`()` Returns the direction priority for the animation. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRowDelay](../android/view/animation/GridLayoutAnimationController.md))`()` Returns the delay by which the children's animation are offset from one row to the other. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnDelay](../android/view/animation/GridLayoutAnimationController.md))`(`columnDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset from one column to the other. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDirection](../android/view/animation/GridLayoutAnimationController.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the direction of the animation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDirectionPriority](../android/view/animation/GridLayoutAnimationController.md))`(`directionPriority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the direction priority of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowDelay](../android/view/animation/GridLayoutAnimationController.md))`(`rowDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset from one row to the other. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willOverlap](../android/view/animation/GridLayoutAnimationController.md))`()` Indicates whether two children's animations will overlap. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDelayForView](../android/view/animation/GridLayoutAnimationController.md))`(`view:` ` [View](../android/view/View.md)!`)` Returns the amount of milliseconds by which the specified view's animation must be delayed or offset. |

| Inherited functions ||
|---|---|
| From class [LayoutAnimationController](../android/view/animation/LayoutAnimationController.md) |-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Animation](../android/view/animation/Animation.md)! | [getAnimation](../android/view/animation/LayoutAnimationController.md))`()` Returns the animation applied to each child of the view group on which this controller is set. <br /> | | [Animation](../android/view/animation/Animation.md)! | [getAnimationForView](../android/view/animation/LayoutAnimationController.md))`(`view:` ` [View](../android/view/View.md)!`)` Returns the animation to be applied to the specified view. The returned animation is delayed by an offset computed according to the information provided by [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md). This method is called by view groups to obtain the animation to set on a specific child. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDelay](../android/view/animation/LayoutAnimationController.md))`()` Returns the delay by which the children's animation are offset. The delay is expressed as a fraction of the animation duration. <br /> | | [Interpolator](../android/view/animation/Interpolator.md)! | [getInterpolator](../android/view/animation/LayoutAnimationController.md))`()` Returns the interpolator used to interpolate the delays between the children. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](../android/view/animation/LayoutAnimationController.md))`()` Returns the order used to compute the delay of each child's animation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransformedIndex](../android/view/animation/LayoutAnimationController.md))`(`params:` ` [LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md)!`)` Transforms the index stored in [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md) by the order returned by [getOrder()](../android/view/animation/LayoutAnimationController.md)). Subclasses should override this method to provide additional support for other types of ordering. This method should be invoked by [getDelayForView(android.view.View)](../android/view/animation/LayoutAnimationController.md)) prior to any computation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](../android/view/animation/LayoutAnimationController.md))`()` Indicates whether the layout animation is over or not. A layout animation is considered done when the animation with the longest delay is done. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimation](../android/view/animation/LayoutAnimationController.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resourceID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the animation to be run on each child of the view group on which this layout animation controller is . <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimation](../android/view/animation/LayoutAnimationController.md))`(`animation:` ` [Animation](../android/view/animation/Animation.md)!`)` Sets the animation to be run on each child of the view group on which this layout animation controller is . <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDelay](../android/view/animation/LayoutAnimationController.md))`(`delay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset. The general formula is: ```kotlin child animation delay = child index * delay * animation duration ``` <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](../android/view/animation/LayoutAnimationController.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resourceID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the interpolator used to interpolate the delays between the children. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](../android/view/animation/LayoutAnimationController.md))`(`interpolator:` ` [Interpolator](../android/view/animation/Interpolator.md)!`)` Sets the interpolator used to interpolate the delays between the children. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](../android/view/animation/LayoutAnimationController.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the order used to compute the delay of each child's animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](../android/view/animation/LayoutAnimationController.md))`()` Starts the animation. <br /> | ||

| Inherited properties ||
|---|---|
| From class [LayoutAnimationController](../android/view/animation/LayoutAnimationController.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Animation](../android/view/animation/Animation.md)! | [mAnimation](../android/view/animation/LayoutAnimationController.md) The animation applied on each child of the view group on which this layout animation controller is set. <br /> | | [Interpolator](../android/view/animation/Interpolator.md)! | [mInterpolator](../android/view/animation/LayoutAnimationController.md) The interpolator used to interpolate the delays. <br /> | | [Random](../java/util/Random.md)! | [mRandomizer](../android/view/animation/LayoutAnimationController.md) The randomizer used when the order is set to random. Subclasses should use this object to avoid creating their own. <br /> | ||

## XML attributes

### android:columnDelay

```
android:columnDelay
```
Fraction of the animation duration used to delay the beginning of the animation of each column.

May be a floating point value, such as "`1.2`".

May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. 

### android:direction

```
android:direction
```
Direction of the animation in the grid.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---------------|-------|--------------------------------------|
| bottom_to_top | 2 | Animates rows from bottom to top. |
| left_to_right | 0 | Animates columns from left to right. |
| right_to_left | 1 | Animates columns from right to left. |
| --- | --- | --- |
| top_to_bottom | 0 | Animates rows from top to bottom. |

### android:directionPriority

```
android:directionPriority
```
Priority of the rows and columns. When the priority is none, both rows and columns have the same priority. When the priority is column, the animations will be applied on the columns first. The same goes for rows.

Must be one of the following constant values.

| Constant | Value | Description |
|----------|-------|-------------------------------------------------|
| column | 1 | Columns are animated first. |
| none | 0 | Rows and columns are animated at the same time. |
| row | 2 | Rows are animated first. |
| --- | --- | --- |

### android:rowDelay

```
android:rowDelay
```
Fraction of the animation duration used to delay the beginning of the animation of each row.

May be a floating point value, such as "`1.2`".

May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container.

## Constants

### DIRECTION_BOTTOM_TO_TOP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_BOTTOM_TO_TOP: Int
```

Animates the children starting from the bottom of the grid to the top. 

 Value: 2

### DIRECTION_HORIZONTAL_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_HORIZONTAL_MASK: Int
```

Bitmask used to retrieve the horizontal component of the direction. 

 Value: 1

### DIRECTION_LEFT_TO_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_LEFT_TO_RIGHT: Int
```

Animates the children starting from the left of the grid to the right. 

 Value: 0

### DIRECTION_RIGHT_TO_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_RIGHT_TO_LEFT: Int
```

Animates the children starting from the right of the grid to the left. 

 Value: 1

### DIRECTION_TOP_TO_BOTTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_TOP_TO_BOTTOM: Int
```

Animates the children starting from the top of the grid to the bottom. 

 Value: 0

### DIRECTION_VERTICAL_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_VERTICAL_MASK: Int
```

Bitmask used to retrieve the vertical component of the direction. 

 Value: 2

### PRIORITY_COLUMN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_COLUMN: Int
```

Columns are animated first. 

 Value: 1

### PRIORITY_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_NONE: Int
```

Rows and columns are animated at the same time. 

 Value: 0

### PRIORITY_ROW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY_ROW: Int
```

Rows are animated first. 

 Value: 2

## Public constructors

### GridLayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GridLayoutAnimationController(
    context: Context!, 
    attrs: AttributeSet!)
```

Creates a new grid layout animation controller from external resources.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!: the Context the view group is running in, through which it can access the resources |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)!: the attributes of the XML tag that is inflating the layout animation controller |

### GridLayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GridLayoutAnimationController(animation: Animation!)
```

Creates a new layout animation controller with a delay of 50% for both rows and columns and the specified animation.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](../android/view/animation/Animation.md)!: the animation to use on each child of the view group |

### GridLayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GridLayoutAnimationController(
    animation: Animation!, 
    columnDelay: Float, 
    rowDelay: Float)
```

Creates a new layout animation controller with the specified delays and the specified animation.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](../android/view/animation/Animation.md)!: the animation to use on each child of the view group |
| `columnDelay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the delay by which each column animation must be offset |
| `rowDelay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the delay by which each row animation must be offset |
| --- | --- |

## Public methods

### getColumnDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColumnDelay(): Float
```

Returns the delay by which the children's animation are offset from one column to the other. The delay is expressed as a fraction of the animation duration.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a fraction of the animation duration |

**See Also**

- [#setColumnDelay(float)](../android/view/animation/GridLayoutAnimationController.md))
- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getRowDelay()>
- [#setRowDelay(float)](../android/view/animation/GridLayoutAnimationController.md)) 

### getDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDirection(): Int
```

Returns the direction of the animation. [DIRECTION_HORIZONTAL_MASK](../android/view/animation/GridLayoutAnimationController.md) and [DIRECTION_VERTICAL_MASK](../android/view/animation/GridLayoutAnimationController.md) can be used to retrieve the horizontal and vertical components of the direction.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the direction of the animation |

**See Also**

- [#setDirection(int)](../android/view/animation/GridLayoutAnimationController.md))
- [#DIRECTION_BOTTOM_TO_TOP](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_TOP_TO_BOTTOM](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_LEFT_TO_RIGHT](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_RIGHT_TO_LEFT](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_HORIZONTAL_MASK](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_VERTICAL_MASK](../android/view/animation/GridLayoutAnimationController.md) 

### getDirectionPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDirectionPriority(): Int
```

Returns the direction priority for the animation. The priority can be either [PRIORITY_NONE](../android/view/animation/GridLayoutAnimationController.md), [PRIORITY_COLUMN](../android/view/animation/GridLayoutAnimationController.md) or [PRIORITY_ROW](../android/view/animation/GridLayoutAnimationController.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the priority of the animation direction |

**See Also**

- [#setDirectionPriority(int)](../android/view/animation/GridLayoutAnimationController.md))
- [#PRIORITY_COLUMN](../android/view/animation/GridLayoutAnimationController.md)
- [#PRIORITY_NONE](../android/view/animation/GridLayoutAnimationController.md)
- [#PRIORITY_ROW](../android/view/animation/GridLayoutAnimationController.md) 

### getRowDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRowDelay(): Float
```

Returns the delay by which the children's animation are offset from one row to the other. The delay is expressed as a fraction of the animation duration.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a fraction of the animation duration |

**See Also**

- [#setRowDelay(float)](../android/view/animation/GridLayoutAnimationController.md))
- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getColumnDelay()>
- [#setColumnDelay(float)](../android/view/animation/GridLayoutAnimationController.md)) 

### setColumnDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setColumnDelay(columnDelay: Float): Unit
```

Sets the delay, as a fraction of the animation duration, by which the children's animations are offset from one column to the other.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------|
| `columnDelay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a fraction of the animation duration |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getColumnDelay()>
- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getRowDelay()>
- [#setRowDelay(float)](../android/view/animation/GridLayoutAnimationController.md)) 

### setDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDirection(direction: Int): Unit
```

Sets the direction of the animation. The direction is expressed as an integer containing a horizontal and vertical component. For instance, `DIRECTION_BOTTOM_TO_TOP | DIRECTION_RIGHT_TO_LEFT`.
| --- | --- |

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction of the animation |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDirection()>
- [#DIRECTION_BOTTOM_TO_TOP](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_TOP_TO_BOTTOM](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_LEFT_TO_RIGHT](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_RIGHT_TO_LEFT](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_HORIZONTAL_MASK](../android/view/animation/GridLayoutAnimationController.md)
- [#DIRECTION_VERTICAL_MASK](../android/view/animation/GridLayoutAnimationController.md) 

### setDirectionPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDirectionPriority(directionPriority: Int): Unit
```

Specifies the direction priority of the animation. For instance, [PRIORITY_COLUMN](../android/view/animation/GridLayoutAnimationController.md) will give priority to columns: the animation will first play on the column, then on the rows.Z

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------|
| `directionPriority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction priority of the animation |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDirectionPriority()>
- [#PRIORITY_COLUMN](../android/view/animation/GridLayoutAnimationController.md)
- [#PRIORITY_NONE](../android/view/animation/GridLayoutAnimationController.md)
- [#PRIORITY_ROW](../android/view/animation/GridLayoutAnimationController.md) 

### setRowDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRowDelay(rowDelay: Float): Unit
```

Sets the delay, as a fraction of the animation duration, by which the children's animations are offset from one row to the other.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `rowDelay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a fraction of the animation duration |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getRowDelay()>
- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getColumnDelay()>
- [#setColumnDelay(float)](../android/view/animation/GridLayoutAnimationController.md)) 

### willOverlap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun willOverlap(): Boolean
```

Indicates whether two children's animations will overlap. Animations overlap when the delay is lower than 100% (or 1.0).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if animations will overlap, false otherwise |

## Protected methods

### getDelayForView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getDelayForView(view: View!): Long
```

Returns the amount of milliseconds by which the specified view's animation must be delayed or offset. Subclasses should override this method to return a suitable value. This implementation returns `child animation delay` milliseconds where: 

```kotlin
child animation delay = child index * delay
  
```
The index is retrieved from the [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md) found in the view's [android.view.ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md).

<br />

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!: the view for which to obtain the animation's delay |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a delay in milliseconds |

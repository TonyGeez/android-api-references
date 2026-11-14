# GridLayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GridLayoutAnimationController

Kotlin | [Java](https://developer.android.com/reference/android/view/animation/GridLayoutAnimationController "View this page in Java") 

```
open class GridLayoutAnimationController : LayoutAnimationController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.animation.LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController) ||
| | ↳ | [android.view.animation.GridLayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#) |

A layout animation controller is used to animated a grid layout's children. While [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController) relies only on the index of the child in the view group to compute the animation delay, this class uses both the X and Y coordinates of the child within a grid. In addition, the animation direction can be controlled. The default direction is `DIRECTION_LEFT_TO_RIGHT | DIRECTION_TOP_TO_BOTTOM`. You can also set the animation priority to columns or rows. The default priority is none. Information used to compute the animation delay of each child are stored in an instance of [android.view.animation.GridLayoutAnimationController.AnimationParameters](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController.AnimationParameters), itself stored in the [android.view.ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#) of the view.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AnimationParameters](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController.AnimationParameters) The set of parameters that has to be attached to each view contained in the view group animated by the grid layout animation controller. |

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [`android:columnDelay`](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#attr_GridLayoutAnimationController) | Fraction of the animation duration used to delay the beginning of the animation of each column. |
| [`android:direction`](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#attr_GridLayoutAnimationController) | Direction of the animation in the grid. |
| [`android:directionPriority`](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#attr_GridLayoutAnimationController) | Priority of the rows and columns. |
| [`android:rowDelay`](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#attr_GridLayoutAnimationController) | Fraction of the animation duration used to delay the beginning of the animation of each row. |

| Inherited XML attributes ||
|---|---|
| From class [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController) |----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:animation](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#attr_LayoutAnimationController) | Animation to use on each child. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:animationOrder](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#attr_LayoutAnimationController) | The order in which the animations will be started. Must be one of the following constant values. | Constant | Value | Description | |----------|-------|----------------------------------------------| | normal | 0 | Animations are started in the natural order. | | random | 2 | Animations are started randomly. | | reverse | 1 | Animations are started in the reverse order. | <br /> | | [android:delay](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#attr_LayoutAnimationController) | Fraction of the animation duration used to delay the beginning of the animation of each child. May be a floating point value, such as "`1.2`". May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. <br /> | | [android:interpolator](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#attr_LayoutAnimationController) | Interpolator used to interpolate the delay between the start of each animation. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | ||

| Constants ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_BOTTOM_TO_TOP](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_BOTTOM_TO_TOP:kotlin.Int) Animates the children starting from the bottom of the grid to the top. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_HORIZONTAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_HORIZONTAL_MASK:kotlin.Int) Bitmask used to retrieve the horizontal component of the direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_LEFT_TO_RIGHT:kotlin.Int) Animates the children starting from the left of the grid to the right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_RIGHT_TO_LEFT:kotlin.Int) Animates the children starting from the right of the grid to the left. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_TOP_TO_BOTTOM](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_TOP_TO_BOTTOM:kotlin.Int) Animates the children starting from the top of the grid to the bottom. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_VERTICAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_VERTICAL_MASK:kotlin.Int) Bitmask used to retrieve the vertical component of the direction. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_COLUMN](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_COLUMN:kotlin.Int) Columns are animated first. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_NONE](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_NONE:kotlin.Int) Rows and columns are animated at the same time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIORITY_ROW](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_ROW:kotlin.Int) Rows are animated first. |

| Inherited constants ||
|---|---|
| From class [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_NORMAL](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#ORDER_NORMAL:kotlin.Int) Distributes the animation delays in the order in which view were added to their view group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_RANDOM](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#ORDER_RANDOM:kotlin.Int) Randomly distributes the animation delays. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_REVERSE](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#ORDER_REVERSE:kotlin.Int) Distributes the animation delays in the reverse order in which view were added to their view group. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GridLayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#GridLayoutAnimationController(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Creates a new grid layout animation controller from external resources. |
| [GridLayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#GridLayoutAnimationController(android.view.animation.Animation))`(`animation:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`)` Creates a new layout animation controller with a delay of 50% for both rows and columns and the specified animation. |
| [GridLayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#GridLayoutAnimationController(android.view.animation.Animation,%20kotlin.Float,%20kotlin.Float))`(`animation:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`, `columnDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `rowDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new layout animation controller with the specified delays and the specified animation. |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getColumnDelay](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getColumnDelay())`()` Returns the delay by which the children's animation are offset from one column to the other. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirection](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDirection())`()` Returns the direction of the animation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDirectionPriority](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDirectionPriority())`()` Returns the direction priority for the animation. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRowDelay](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getRowDelay())`()` Returns the delay by which the children's animation are offset from one row to the other. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnDelay](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setColumnDelay(kotlin.Float))`(`columnDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset from one column to the other. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDirection](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setDirection(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the direction of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDirectionPriority](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setDirectionPriority(kotlin.Int))`(`directionPriority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specifies the direction priority of the animation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRowDelay](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setRowDelay(kotlin.Float))`(`rowDelay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset from one row to the other. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willOverlap](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#willOverlap())`()` Indicates whether two children's animations will overlap. |

| Protected methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDelayForView](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDelayForView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Returns the amount of milliseconds by which the specified view's animation must be delayed or offset. |

| Inherited functions ||
|---|---|
| From class [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController) |-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | [getAnimation](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getAnimation())`()` Returns the animation applied to each child of the view group on which this controller is set. <br /> | | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | [getAnimationForView](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getAnimationForView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Returns the animation to be applied to the specified view. The returned animation is delayed by an offset computed according to the information provided by [android.view.animation.LayoutAnimationController.AnimationParameters](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController.AnimationParameters). This method is called by view groups to obtain the animation to set on a specific child. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDelay](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getDelay())`()` Returns the delay by which the children's animation are offset. The delay is expressed as a fraction of the animation duration. <br /> | | [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)! | [getInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getInterpolator())`()` Returns the interpolator used to interpolate the delays between the children. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getOrder())`()` Returns the order used to compute the delay of each child's animation. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransformedIndex](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getTransformedIndex(android.view.animation.LayoutAnimationController.AnimationParameters))`(`params:` ` [LayoutAnimationController.AnimationParameters](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController.AnimationParameters)!`)` Transforms the index stored in [android.view.animation.LayoutAnimationController.AnimationParameters](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController.AnimationParameters) by the order returned by [getOrder()](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getOrder()). Subclasses should override this method to provide additional support for other types of ordering. This method should be invoked by [getDelayForView(android.view.View)](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getDelayForView(android.view.View)) prior to any computation. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#isDone())`()` Indicates whether the layout animation is over or not. A layout animation is considered done when the animation with the longest delay is done. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimation](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#setAnimation(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resourceID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the animation to be run on each child of the view group on which this layout animation controller is . <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimation](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#setAnimation(android.view.animation.Animation))`(`animation:` ` [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!`)` Sets the animation to be run on each child of the view group on which this layout animation controller is . <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDelay](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#setDelay(kotlin.Float))`(`delay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset. The general formula is: ```kotlin child animation delay = child index * delay * animation duration ``` <br /> <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#setInterpolator(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resourceID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the interpolator used to interpolate the delays between the children. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#setInterpolator(android.view.animation.Interpolator))`(`interpolator:` ` [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)!`)` Sets the interpolator used to interpolate the delays between the children. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#setOrder(kotlin.Int))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the order used to compute the delay of each child's animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#start())`()` Starts the animation. <br /> | ||

| Inherited properties ||
|---|---|
| From class [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | [mAnimation](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#mAnimation:android.view.animation.Animation) The animation applied on each child of the view group on which this layout animation controller is set. <br /> | | [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)! | [mInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#mInterpolator:android.view.animation.Interpolator) The interpolator used to interpolate the delays. <br /> | | [Random](https://developer.android.com/reference/kotlin/java/util/Random.html#)! | [mRandomizer](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#mRandomizer:java.util.Random) The randomizer used when the order is set to random. Subclasses should use this object to avoid creating their own. <br /> | ||

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

| Constant | Value | Description |
|---------------|-------|--------------------------------------|
| bottom_to_top | 2 | Animates rows from bottom to top. |
| left_to_right | 0 | Animates columns from left to right. |
| right_to_left | 1 | Animates columns from right to left. |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: the Context the view group is running in, through which it can access the resources |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!: the attributes of the XML tag that is inflating the layout animation controller |

### GridLayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GridLayoutAnimationController(animation: Animation!)
```

Creates a new layout animation controller with a delay of 50% for both rows and columns and the specified animation.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!: the animation to use on each child of the view group |

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
| `animation` | [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)!: the animation to use on each child of the view group |
| `columnDelay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the delay by which each column animation must be offset |
| `rowDelay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the delay by which each row animation must be offset |

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

- [#setColumnDelay(float)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setColumnDelay(kotlin.Float))
- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getRowDelay()>
- [#setRowDelay(float)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setRowDelay(kotlin.Float)) 

### getDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDirection(): Int
```

Returns the direction of the animation. [DIRECTION_HORIZONTAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_HORIZONTAL_MASK:kotlin.Int) and [DIRECTION_VERTICAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_VERTICAL_MASK:kotlin.Int) can be used to retrieve the horizontal and vertical components of the direction.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the direction of the animation |

**See Also**

- [#setDirection(int)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setDirection(kotlin.Int))
- [#DIRECTION_BOTTOM_TO_TOP](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_BOTTOM_TO_TOP:kotlin.Int)
- [#DIRECTION_TOP_TO_BOTTOM](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_TOP_TO_BOTTOM:kotlin.Int)
- [#DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_LEFT_TO_RIGHT:kotlin.Int)
- [#DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_RIGHT_TO_LEFT:kotlin.Int)
- [#DIRECTION_HORIZONTAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_HORIZONTAL_MASK:kotlin.Int)
- [#DIRECTION_VERTICAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_VERTICAL_MASK:kotlin.Int) 

### getDirectionPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDirectionPriority(): Int
```

Returns the direction priority for the animation. The priority can be either [PRIORITY_NONE](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_NONE:kotlin.Int), [PRIORITY_COLUMN](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_COLUMN:kotlin.Int) or [PRIORITY_ROW](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_ROW:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the priority of the animation direction |

**See Also**

- [#setDirectionPriority(int)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setDirectionPriority(kotlin.Int))
- [#PRIORITY_COLUMN](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_COLUMN:kotlin.Int)
- [#PRIORITY_NONE](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_NONE:kotlin.Int)
- [#PRIORITY_ROW](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_ROW:kotlin.Int) 

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

- [#setRowDelay(float)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setRowDelay(kotlin.Float))
- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getColumnDelay()>
- [#setColumnDelay(float)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setColumnDelay(kotlin.Float)) 

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
- [#setRowDelay(float)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setRowDelay(kotlin.Float)) 

### setDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDirection(direction: Int): Unit
```

Sets the direction of the animation. The direction is expressed as an integer containing a horizontal and vertical component. For instance, `DIRECTION_BOTTOM_TO_TOP | DIRECTION_RIGHT_TO_LEFT`.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction of the animation |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDirection()>
- [#DIRECTION_BOTTOM_TO_TOP](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_BOTTOM_TO_TOP:kotlin.Int)
- [#DIRECTION_TOP_TO_BOTTOM](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_TOP_TO_BOTTOM:kotlin.Int)
- [#DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_LEFT_TO_RIGHT:kotlin.Int)
- [#DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_RIGHT_TO_LEFT:kotlin.Int)
- [#DIRECTION_HORIZONTAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_HORIZONTAL_MASK:kotlin.Int)
- [#DIRECTION_VERTICAL_MASK](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#DIRECTION_VERTICAL_MASK:kotlin.Int) 

### setDirectionPriority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDirectionPriority(directionPriority: Int): Unit
```

Specifies the direction priority of the animation. For instance, [PRIORITY_COLUMN](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_COLUMN:kotlin.Int) will give priority to columns: the animation will first play on the column, then on the rows.Z

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------|
| `directionPriority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction priority of the animation |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#getDirectionPriority()>
- [#PRIORITY_COLUMN](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_COLUMN:kotlin.Int)
- [#PRIORITY_NONE](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_NONE:kotlin.Int)
- [#PRIORITY_ROW](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#PRIORITY_ROW:kotlin.Int) 

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
- [#setColumnDelay(float)](https://developer.android.com/reference/kotlin/android/view/animation/GridLayoutAnimationController#setColumnDelay(kotlin.Float)) 

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
The index is retrieved from the [android.view.animation.LayoutAnimationController.AnimationParameters](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController.AnimationParameters) found in the view's [android.view.ViewGroup.LayoutParams](https://developer.android.com/reference/kotlin/android/view/ViewGroup.LayoutParams.html#).

<br />

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: the view for which to obtain the animation's delay |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a delay in milliseconds |

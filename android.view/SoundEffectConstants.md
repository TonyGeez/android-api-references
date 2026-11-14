# SoundEffectConstants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SoundEffectConstants

Kotlin | [Java](https://developer.android.com/reference/android/view/SoundEffectConstants "View this page in Java") 
| --- | --- |

```
open class SoundEffectConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SoundEffectConstants](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#) |

Constants to be used to play sound effects via [View.playSoundEffect(int)](https://developer.android.com/reference/kotlin/android/view/View#playSoundEffect(kotlin.Int))

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLICK](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#CLICK:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_DOWN](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_DOWN:kotlin.Int) Effect id for a navigation down |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_LEFT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_LEFT:kotlin.Int) Effect id for a navigation left |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_DOWN](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_DOWN:kotlin.Int) Effect id for a repeatedly triggered navigation down, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_LEFT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_LEFT:kotlin.Int) Effect id for a repeatedly triggered navigation left, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_RIGHT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_RIGHT:kotlin.Int) Effect id for a repeatedly triggered navigation right, e. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_UP](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_UP:kotlin.Int) Effect id for a repeatedly triggered navigation up, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_RIGHT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_RIGHT:kotlin.Int) Effect id for a navigation right |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_UP](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_UP:kotlin.Int) Effect id for a navigation up |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConstantForFocusDirection](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#getConstantForFocusDirection(kotlin.Int,%20kotlin.Boolean))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeating:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Get the sonification constant for the focus directions |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContantForFocusDirection](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#getContantForFocusDirection(kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the sonification constant for the focus directions. |

## Constants

### CLICK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLICK: Int
```  

 Value: 0

### NAVIGATION_DOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_DOWN: Int
```

Effect id for a navigation down 

 Value: 4

### NAVIGATION_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_LEFT: Int
```

Effect id for a navigation left 

 Value: 1

### NAVIGATION_REPEAT_DOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_REPEAT_DOWN: Int
```

Effect id for a repeatedly triggered navigation down, e.g. due to long pressing a button 

 Value: 8

### NAVIGATION_REPEAT_LEFT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_REPEAT_LEFT: Int
```

Effect id for a repeatedly triggered navigation left, e.g. due to long pressing a button 

 Value: 5

### NAVIGATION_REPEAT_RIGHT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_REPEAT_RIGHT: Int
```

Effect id for a repeatedly triggered navigation right, e.g. due to long pressing a button 

 Value: 7

### NAVIGATION_REPEAT_UP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_REPEAT_UP: Int
```

Effect id for a repeatedly triggered navigation up, e.g. due to long pressing a button 

 Value: 6

### NAVIGATION_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_RIGHT: Int
```

Effect id for a navigation right 

 Value: 3

### NAVIGATION_UP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAVIGATION_UP: Int
```

Effect id for a navigation up 

 Value: 2

## Public methods

### getConstantForFocusDirection

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getConstantForFocusDirection(
    direction: Int, 
    repeating: Boolean
): Int
```

Get the sonification constant for the focus directions

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is [android.view.View#FOCUS_BACKWARD](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int), [android.view.View#FOCUS_FORWARD](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int), [android.view.View#FOCUS_LEFT](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int), [android.view.View#FOCUS_UP](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int), [android.view.View#FOCUS_RIGHT](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int), or [android.view.View#FOCUS_DOWN](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int) |
| `repeating` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the user long-presses a direction |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The appropriate sonification constant Value is [android.view.SoundEffectConstants#NAVIGATION_LEFT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_LEFT:kotlin.Int), [android.view.SoundEffectConstants#NAVIGATION_UP](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_UP:kotlin.Int), [android.view.SoundEffectConstants#NAVIGATION_RIGHT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_RIGHT:kotlin.Int), [android.view.SoundEffectConstants#NAVIGATION_DOWN](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_DOWN:kotlin.Int), [android.view.SoundEffectConstants#NAVIGATION_REPEAT_LEFT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_LEFT:kotlin.Int), [android.view.SoundEffectConstants#NAVIGATION_REPEAT_UP](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_UP:kotlin.Int), [android.view.SoundEffectConstants#NAVIGATION_REPEAT_RIGHT](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_RIGHT:kotlin.Int), or [android.view.SoundEffectConstants#NAVIGATION_REPEAT_DOWN](https://developer.android.com/reference/kotlin/android/view/SoundEffectConstants#NAVIGATION_REPEAT_DOWN:kotlin.Int) |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when the passed direction is not one of the documented values. |

### getContantForFocusDirection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getContantForFocusDirection(direction: Int): Int
```

Get the sonification constant for the focus directions.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is [android.view.View#FOCUS_BACKWARD](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_BACKWARD:kotlin.Int), [android.view.View#FOCUS_FORWARD](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_FORWARD:kotlin.Int), [android.view.View#FOCUS_LEFT](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_LEFT:kotlin.Int), [android.view.View#FOCUS_UP](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_UP:kotlin.Int), [android.view.View#FOCUS_RIGHT](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_RIGHT:kotlin.Int), or [android.view.View#FOCUS_DOWN](https://developer.android.com/reference/kotlin/android/view/View#FOCUS_DOWN:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The appropriate sonification constant. |

| Exceptions ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) when the passed direction is not one of the documented values. |

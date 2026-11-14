# SoundEffectConstants

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SoundEffectConstants

Kotlin | [Java](SoundEffectConstants.md) 
| --- | --- |

```
open class SoundEffectConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.SoundEffectConstants](SoundEffectConstants.md) |

Constants to be used to play sound effects via [View.playSoundEffect(int)](View.md))

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLICK](SoundEffectConstants.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_DOWN](SoundEffectConstants.md) Effect id for a navigation down |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_LEFT](SoundEffectConstants.md) Effect id for a navigation left |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_DOWN](SoundEffectConstants.md) Effect id for a repeatedly triggered navigation down, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_LEFT](SoundEffectConstants.md) Effect id for a repeatedly triggered navigation left, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_RIGHT](SoundEffectConstants.md) Effect id for a repeatedly triggered navigation right, e. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_REPEAT_UP](SoundEffectConstants.md) Effect id for a repeatedly triggered navigation up, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_RIGHT](SoundEffectConstants.md) Effect id for a navigation right |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NAVIGATION_UP](SoundEffectConstants.md) Effect id for a navigation up |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConstantForFocusDirection](SoundEffectConstants.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeating:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Get the sonification constant for the focus directions |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContantForFocusDirection](SoundEffectConstants.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the sonification constant for the focus directions. |

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
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is [android.view.View#FOCUS_BACKWARD](View.md), [android.view.View#FOCUS_FORWARD](View.md), [android.view.View#FOCUS_LEFT](View.md), [android.view.View#FOCUS_UP](View.md), [android.view.View#FOCUS_RIGHT](View.md), or [android.view.View#FOCUS_DOWN](View.md) |
| `repeating` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if the user long-presses a direction |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The appropriate sonification constant Value is [android.view.SoundEffectConstants#NAVIGATION_LEFT](SoundEffectConstants.md), [android.view.SoundEffectConstants#NAVIGATION_UP](SoundEffectConstants.md), [android.view.SoundEffectConstants#NAVIGATION_RIGHT](SoundEffectConstants.md), [android.view.SoundEffectConstants#NAVIGATION_DOWN](SoundEffectConstants.md), [android.view.SoundEffectConstants#NAVIGATION_REPEAT_LEFT](SoundEffectConstants.md), [android.view.SoundEffectConstants#NAVIGATION_REPEAT_UP](SoundEffectConstants.md), [android.view.SoundEffectConstants#NAVIGATION_REPEAT_RIGHT](SoundEffectConstants.md), or [android.view.SoundEffectConstants#NAVIGATION_REPEAT_DOWN](SoundEffectConstants.md) |

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
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The direction of the focus. Value is [android.view.View#FOCUS_BACKWARD](View.md), [android.view.View#FOCUS_FORWARD](View.md), [android.view.View#FOCUS_LEFT](View.md), [android.view.View#FOCUS_UP](View.md), [android.view.View#FOCUS_RIGHT](View.md), or [android.view.View#FOCUS_DOWN](View.md) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The appropriate sonification constant. |

| Exceptions ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [IllegalArgumentException](../java.lang/IllegalArgumentException.md) when the passed direction is not one of the documented values. |

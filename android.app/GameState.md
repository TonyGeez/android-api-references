# GameState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GameState

Kotlin| [Java](https://developer.android.com/reference/android/app/GameState "View this page in Java") 

```
class GameState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.GameState](https://developer.android.com/reference/kotlin/android/app/GameState#) |

State of the game passed to the GameManager. This includes a top-level state for the game (indicating if the game can be interrupted without interfering with content that can't be paused). Since content can be loaded in any state, it includes an independent boolean flag to indicate loading status. Free-form metadata (as a Bundle) and a string description can also be specified by the application.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_CONTENT](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_CONTENT:kotlin.Int) Indicates that the current content shown is not gameplay related. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_GAMEPLAY_INTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_INTERRUPTIBLE:kotlin.Int) Indicates if the game is in active, but interruptible, game play. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_GAMEPLAY_UNINTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE:kotlin.Int) Indicates if the game is in active user play mode, which is real time and cannot be interrupted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_NONE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_NONE:kotlin.Int) No mode means that the game is not in active play, for example the user is using the game menu. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_UNKNOWN:kotlin.Int) Default Game mode is unknown. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GameState](https://developer.android.com/reference/kotlin/android/app/GameState#GameState(kotlin.Boolean,%20kotlin.Int))`(`isLoading:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a GameState with the specified loading status. |
| [GameState](https://developer.android.com/reference/kotlin/android/app/GameState#GameState(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`isLoading:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `label:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `quality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a GameState with the given state variables. |

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/GameState#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLabel](https://developer.android.com/reference/kotlin/android/app/GameState#getLabel())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMode](https://developer.android.com/reference/kotlin/android/app/GameState#getMode())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQuality](https://developer.android.com/reference/kotlin/android/app/GameState#getQuality())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoading](https://developer.android.com/reference/kotlin/android/app/GameState#isLoading())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/GameState#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GameState](https://developer.android.com/reference/kotlin/android/app/GameState#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/GameState#CREATOR:android.os.Parcelable.Creator) Implement the parcelable interface. |

## Constants

### MODE_CONTENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_CONTENT: Int
```

Indicates that the current content shown is not gameplay related. For example it can be an ad, a web page, a text, or a video. 

 Value: 4

### MODE_GAMEPLAY_INTERRUPTIBLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_GAMEPLAY_INTERRUPTIBLE: Int
```

Indicates if the game is in active, but interruptible, game play. 

 Value: 2

### MODE_GAMEPLAY_UNINTERRUPTIBLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_GAMEPLAY_UNINTERRUPTIBLE: Int
```

Indicates if the game is in active user play mode, which is real time and cannot be interrupted. 

 Value: 3

### MODE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_NONE: Int
```

No mode means that the game is not in active play, for example the user is using the game menu. 

 Value: 1

### MODE_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODE_UNKNOWN: Int
```

Default Game mode is unknown. 

 Value: 0

## Public constructors

### GameState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GameState(
    isLoading: Boolean, 
    mode: Int)
```

Create a GameState with the specified loading status.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isLoading` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the game is in the loading state. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The game state mode of type @GameStateMode. Value is [android.app.GameState#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_UNKNOWN:kotlin.Int), [android.app.GameState#MODE_NONE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_NONE:kotlin.Int), [android.app.GameState#MODE_GAMEPLAY_INTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_INTERRUPTIBLE:kotlin.Int), [android.app.GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE:kotlin.Int), or [android.app.GameState#MODE_CONTENT](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_CONTENT:kotlin.Int) |

### GameState

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GameState(
    isLoading: Boolean, 
    mode: Int, 
    label: Int, 
    quality: Int)
```

Create a GameState with the given state variables.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isLoading` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the game is in the loading state. |
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The game state mode. Value is [android.app.GameState#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_UNKNOWN:kotlin.Int), [android.app.GameState#MODE_NONE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_NONE:kotlin.Int), [android.app.GameState#MODE_GAMEPLAY_INTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_INTERRUPTIBLE:kotlin.Int), [android.app.GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE:kotlin.Int), or [android.app.GameState#MODE_CONTENT](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_CONTENT:kotlin.Int) |
| `label` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An optional developer-supplied enum e.g. for the current level. |
| `quality` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An optional developer-supplied enum, e.g. for the current quality level. |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getLabel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLabel(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The developer-supplied enum, e.g. to indicate level or scene. The default value (if not supplied) is -1. |

### getMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMode(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The game state mode. Value is [android.app.GameState#MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_UNKNOWN:kotlin.Int), [android.app.GameState#MODE_NONE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_NONE:kotlin.Int), [android.app.GameState#MODE_GAMEPLAY_INTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_INTERRUPTIBLE:kotlin.Int), [android.app.GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_GAMEPLAY_UNINTERRUPTIBLE:kotlin.Int), or [android.app.GameState#MODE_CONTENT](https://developer.android.com/reference/kotlin/android/app/GameState#MODE_CONTENT:kotlin.Int) |

### getQuality

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQuality(): Int
```

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The developer-supplied enum, e.g. to indicate the current quality level. The default value (if not suplied) is -1. |

### isLoading

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLoading(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If the game is loading assets/resources/compiling/etc. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
| `parcel` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GameState!>
```

Implement the parcelable interface.

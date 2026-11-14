# Gesture

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Gesture

Kotlin| [Java](https://developer.android.com/reference/android/gesture/Gesture "View this page in Java") 

```
open class Gesture : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.gesture.Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture#) |

A gesture is a hand-drawn shape on a touch screen. It can have one or multiple strokes. Each stroke is a sequence of timed points. A user-defined gesture can be recognized by a GestureLibrary.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------|---|
| [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture#Gesture())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addStroke](https://developer.android.com/reference/kotlin/android/gesture/Gesture#addStroke(android.gesture.GestureStroke))`(`stroke:` ` [GestureStroke](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke)!`)` Adds a stroke to the gesture. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/android/gesture/Gesture#clone())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/gesture/Gesture#describeContents())`()` <br /> |
| open [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)! | [getBoundingBox](https://developer.android.com/reference/kotlin/android/gesture/Gesture#getBoundingBox())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getID](https://developer.android.com/reference/kotlin/android/gesture/Gesture#getID())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getLength](https://developer.android.com/reference/kotlin/android/gesture/Gesture#getLength())`()` Calculates the total length of the gesture. |
| open [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [GestureStroke](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke)!\>! | [getStrokes](https://developer.android.com/reference/kotlin/android/gesture/Gesture#getStrokes())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokesCount](https://developer.android.com/reference/kotlin/android/gesture/Gesture#getStrokesCount())`()` <br /> |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | [toBitmap](https://developer.android.com/reference/kotlin/android/gesture/Gesture#toBitmap(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a bitmap of the gesture with a transparent background. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | [toBitmap](https://developer.android.com/reference/kotlin/android/gesture/Gesture#toBitmap(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edge:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numSample:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a bitmap of the gesture with a transparent background. |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [toPath](https://developer.android.com/reference/kotlin/android/gesture/Gesture#toPath())`()` <br /> |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [toPath](https://developer.android.com/reference/kotlin/android/gesture/Gesture#toPath(android.graphics.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` <br /> |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [toPath](https://developer.android.com/reference/kotlin/android/gesture/Gesture#toPath(android.graphics.Path,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edge:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numSample:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)! | [toPath](https://developer.android.com/reference/kotlin/android/gesture/Gesture#toPath(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `edge:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numSample:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/gesture/Gesture#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/gesture/Gesture#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### Gesture

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Gesture()
```

## Public methods

### addStroke

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addStroke(stroke: GestureStroke!): Unit
```

Adds a stroke to the gesture.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `stroke` | [GestureStroke](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke)!: |

### clone

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any!
```

| Return ||
|-----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### describeContents

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBoundingBox

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBoundingBox(): RectF!
```

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------|
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)! | the bounding box of the gesture |

### getID

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getID(): Long
```

| Return ||
|------------------------------------------------------------------------------|-----------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the id of the gesture |

### getLength

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Float
```

Calculates the total length of the gesture. When there are multiple strokes in the gesture, this returns the sum of the lengths of all the strokes.

| Return ||
|--------------------------------------------------------------------------------|---------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the length of the gesture |

### getStrokes

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStrokes(): ArrayList<GestureStroke!>!
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [GestureStroke](https://developer.android.com/reference/kotlin/android/gesture/GestureStroke)!>! | all the strokes of the gesture |

### getStrokesCount

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStrokesCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of strokes included by this gesture |

### toBitmap

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toBitmap(
    width: Int, 
    height: Int, 
    inset: Int, 
    color: Int
): Bitmap!
```

Creates a bitmap of the gesture with a transparent background.

| Parameters ||
|----------|-----------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `inset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

| Return ||
|-----------------------------------------------------------------------------------------|------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | the bitmap |

### toBitmap

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toBitmap(
    width: Int, 
    height: Int, 
    edge: Int, 
    numSample: Int, 
    color: Int
): Bitmap!
```

Creates a bitmap of the gesture with a transparent background.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):width of the target bitmap |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):height of the target bitmap |
| `edge` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the edge |
| `numSample` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

| Return ||
|-----------------------------------------------------------------------------------------|------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)! | the bitmap |

### toPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPath(): Path!
```  

### toPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPath(path: Path!): Path!
```  

### toPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPath(
    path: Path!, 
    width: Int, 
    height: Int, 
    edge: Int, 
    numSample: Int
): Path!
```  

### toPath

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPath(
    width: Int, 
    height: Int, 
    edge: Int, 
    numSample: Int
): Path!
```  

### writeToParcel

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<Gesture!>
```

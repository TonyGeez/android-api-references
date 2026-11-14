# GestureStore

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureStore

Kotlin | [Java](https://developer.android.com/reference/android/gesture/GestureStore "View this page in Java") 

```
open class GestureStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.gesture.GestureStore](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#) |

GestureLibrary maintains gesture examples and makes predictions on a new gesture

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_INVARIANT](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#ORIENTATION_INVARIANT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_SENSITIVE](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#ORIENTATION_SENSITIVE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEQUENCE_INVARIANT](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#SEQUENCE_INVARIANT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEQUENCE_SENSITIVE](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#SEQUENCE_SENSITIVE:kotlin.Int) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------|---|
| [GestureStore](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#GestureStore())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addGesture](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#addGesture(kotlin.String,%20android.gesture.Gesture))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!`)` Add a gesture for the entry |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getGestureEntries](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#getGestureEntries())`()` Get all the gesture entry names in the library |
| open [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!\>! | [getGestures](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#getGestures(kotlin.String))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get all the gestures of an entry |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrientationStyle](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#getOrientationStyle())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequenceType](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#getSequenceType())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChanged](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#hasChanged())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#load(java.io.InputStream))`(`stream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Load the gesture library |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#load(java.io.InputStream,%20kotlin.Boolean))`(`stream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `closeStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Prediction](https://developer.android.com/reference/kotlin/android/gesture/Prediction)!\>! | [recognize](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#recognize(android.gesture.Gesture))`(`gesture:` ` [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!`)` Recognize a gesture |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeEntry](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#removeEntry(kotlin.String))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove a entry of gestures |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGesture](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#removeGesture(kotlin.String,%20android.gesture.Gesture))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!`)` Remove a gesture from the library. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [save](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#save(java.io.OutputStream))`(`stream:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` Save the gesture library |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [save](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#save(java.io.OutputStream,%20kotlin.Boolean))`(`stream:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`, `closeStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientationStyle](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#setOrientationStyle(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify how the gesture library will handle orientation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSequenceType](https://developer.android.com/reference/kotlin/android/gesture/GestureStore#setSequenceType(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Constants

### ORIENTATION_INVARIANT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_INVARIANT: Int
```  

 Value: 1

### ORIENTATION_SENSITIVE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORIENTATION_SENSITIVE: Int
```  

 Value: 2

### SEQUENCE_INVARIANT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEQUENCE_INVARIANT: Int
```  

 Value: 1

### SEQUENCE_SENSITIVE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEQUENCE_SENSITIVE: Int
```  

 Value: 2

## Public constructors

### GestureStore

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GestureStore()
```

## Public methods

### addGesture

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addGesture(
    entryName: String!, 
    gesture: Gesture!
): Unit
```

Add a gesture for the entry

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------|
| `entryName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: entry name |
| `gesture` | [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!: |

### getGestureEntries

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGestureEntries(): MutableSet<String!>!
```

Get all the gesture entry names in the library

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a set of strings |

### getGestures

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGestures(entryName: String!): ArrayList<Gesture!>!
```

Get all the gestures of an entry

| Parameters ||
|-------------|------------------------------------------------------------------------------------|
| `entryName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!>! | the list of gestures that is under this name |

### getOrientationStyle

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrientationStyle(): Int
```  

### getSequenceType

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSequenceType(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | SEQUENCE_INVARIANT or SEQUENCE_SENSITIVE |

### hasChanged

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasChanged(): Boolean
```  

### load

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(stream: InputStream!): Unit
```

Load the gesture library 

### load

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun load(
    stream: InputStream!, 
    closeStream: Boolean
): Unit
```  

### recognize

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun recognize(gesture: Gesture!): ArrayList<Prediction!>!
```

Recognize a gesture

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------|
| `gesture` | [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!: the query |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [Prediction](https://developer.android.com/reference/kotlin/android/gesture/Prediction)!>! | a list of predictions of possible entries for a given gesture |

### removeEntry

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeEntry(entryName: String!): Unit
```

Remove a entry of gestures

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------|
| `entryName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the entry name |

### removeGesture

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeGesture(
    entryName: String!, 
    gesture: Gesture!
): Unit
```

Remove a gesture from the library. If there are no more gestures for the given entry, the gesture entry will be removed.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------|
| `entryName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: entry name |
| `gesture` | [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!: |

### save

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun save(stream: OutputStream!): Unit
```

Save the gesture library 

### save

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun save(
    stream: OutputStream!, 
    closeStream: Boolean
): Unit
```  

### setOrientationStyle

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrientationStyle(style: Int): Unit
```

Specify how the gesture library will handle orientation. Use ORIENTATION_INVARIANT or ORIENTATION_SENSITIVE

| Parameters ||
|---------|-----------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

### setSequenceType

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSequenceType(type: Int): Unit
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): SEQUENCE_INVARIANT or SEQUENCE_SENSITIVE |

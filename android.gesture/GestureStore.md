# GestureStore

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureStore

Kotlin | [Java](GestureStore.md) 
| --- | --- |

```
open class GestureStore
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.gesture.GestureStore](GestureStore.md) |

GestureLibrary maintains gesture examples and makes predictions on a new gesture

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_INVARIANT](GestureStore.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORIENTATION_SENSITIVE](GestureStore.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEQUENCE_INVARIANT](GestureStore.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEQUENCE_SENSITIVE](GestureStore.md) <br /> |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------|---|
| [GestureStore](GestureStore.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addGesture](GestureStore.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](Gesture.md)!`)` Add a gesture for the entry |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getGestureEntries](GestureStore.md))`()` Get all the gesture entry names in the library |
| open [ArrayList](../java.util/ArrayList.md)\< [Gesture](Gesture.md)!\>! | [getGestures](GestureStore.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get all the gestures of an entry |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrientationStyle](GestureStore.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequenceType](GestureStore.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChanged](GestureStore.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](GestureStore.md))`(`stream:` ` [InputStream](../java.io/InputStream.md)!`)` Load the gesture library |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [load](GestureStore.md))`(`stream:` ` [InputStream](../java.io/InputStream.md)!`, `closeStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [ArrayList](../java.util/ArrayList.md)\< [Prediction](Prediction.md)!\>! | [recognize](GestureStore.md))`(`gesture:` ` [Gesture](Gesture.md)!`)` Recognize a gesture |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeEntry](GestureStore.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove a entry of gestures |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGesture](GestureStore.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](Gesture.md)!`)` Remove a gesture from the library. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [save](GestureStore.md))`(`stream:` ` [OutputStream](../java.io/OutputStream.md)!`)` Save the gesture library |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [save](GestureStore.md))`(`stream:` ` [OutputStream](../java.io/OutputStream.md)!`, `closeStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientationStyle](GestureStore.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify how the gesture library will handle orientation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSequenceType](GestureStore.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

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
| `gesture` | [Gesture](Gesture.md)!: |

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
| [ArrayList](../java.util/ArrayList.md)< [Gesture](Gesture.md)!>! | the list of gestures that is under this name |

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
| `gesture` | [Gesture](Gesture.md)!: the query |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ArrayList](../java.util/ArrayList.md)< [Prediction](Prediction.md)!>! | a list of predictions of possible entries for a given gesture |

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
| `gesture` | [Gesture](Gesture.md)!: |

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

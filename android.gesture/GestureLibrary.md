# GestureLibrary

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureLibrary

Kotlin| [Java](../android/gesture/GestureLibrary.md) 
| --- | --- |

```
abstract class GestureLibrary
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.gesture.GestureLibrary](../android/gesture/GestureLibrary.md) |

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [GestureLibrary](../android/gesture/GestureLibrary.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addGesture](../android/gesture/GestureLibrary.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](../android/gesture/Gesture.md)!`)` <br /> |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getGestureEntries](../android/gesture/GestureLibrary.md))`()` <br /> |
| open [ArrayList](../java/util/ArrayList.md)\< [Gesture](../android/gesture/Gesture.md)!\>! | [getGestures](../android/gesture/GestureLibrary.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrientationStyle](../android/gesture/GestureLibrary.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequenceType](../android/gesture/GestureLibrary.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../android/gesture/GestureLibrary.md))`()` <br /> |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [load](../android/gesture/GestureLibrary.md))`()` <br /> |
| open [ArrayList](../java/util/ArrayList.md)\< [Prediction](../android/gesture/Prediction.md)!\>! | [recognize](../android/gesture/GestureLibrary.md))`(`gesture:` ` [Gesture](../android/gesture/Gesture.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeEntry](../android/gesture/GestureLibrary.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGesture](../android/gesture/GestureLibrary.md))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](../android/gesture/Gesture.md)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [save](../android/gesture/GestureLibrary.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientationStyle](../android/gesture/GestureLibrary.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSequenceType](../android/gesture/GestureLibrary.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [GestureStore](../android/gesture/GestureStore.md)! | [mStore](../android/gesture/GestureLibrary.md) <br /> |

## Protected constructors

### GestureLibrary

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected GestureLibrary()
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

### getGestureEntries

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGestureEntries(): MutableSet<String!>!
```  

### getGestures

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGestures(entryName: String!): ArrayList<Gesture!>!
```  

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

### isReadOnly

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReadOnly(): Boolean
```  

### load

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun load(): Boolean
```  

### recognize

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun recognize(gesture: Gesture!): ArrayList<Prediction!>!
```  

### removeEntry

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeEntry(entryName: String!): Unit
```  

### removeGesture

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeGesture(
    entryName: String!, 
    gesture: Gesture!
): Unit
```  

### save

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun save(): Boolean
```  

### setOrientationStyle

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrientationStyle(style: Int): Unit
```  

### setSequenceType

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSequenceType(type: Int): Unit
```

## Properties

### mStore

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected val mStore: GestureStore!
```

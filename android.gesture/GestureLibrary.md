# GestureLibrary

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureLibrary

Kotlin| [Java](https://developer.android.com/reference/android/gesture/GestureLibrary "View this page in Java") 

```
abstract class GestureLibrary
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.gesture.GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#) |

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#GestureLibrary())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addGesture](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#addGesture(kotlin.String,%20android.gesture.Gesture))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!`)` <br /> |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getGestureEntries](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#getGestureEntries())`()` <br /> |
| open [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!\>! | [getGestures](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#getGestures(kotlin.String))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrientationStyle](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#getOrientationStyle())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequenceType](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#getSequenceType())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#isReadOnly())`()` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [load](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#load())`()` <br /> |
| open [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Prediction](https://developer.android.com/reference/kotlin/android/gesture/Prediction)!\>! | [recognize](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#recognize(android.gesture.Gesture))`(`gesture:` ` [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeEntry](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#removeEntry(kotlin.String))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGesture](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#removeGesture(kotlin.String,%20android.gesture.Gesture))`(`entryName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `gesture:` ` [Gesture](https://developer.android.com/reference/kotlin/android/gesture/Gesture)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [save](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#save())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrientationStyle](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#setOrientationStyle(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSequenceType](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#setSequenceType(kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [GestureStore](https://developer.android.com/reference/kotlin/android/gesture/GestureStore)! | [mStore](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary#mStore:android.gesture.GestureStore) <br /> |

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

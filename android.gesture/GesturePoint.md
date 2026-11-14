# GesturePoint

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GesturePoint

Kotlin| [Java](https://developer.android.com/reference/android/gesture/GesturePoint "View this page in Java") 

```
open class GesturePoint
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.gesture.GesturePoint](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint#) |

A timed point of a gesture stroke. Multiple points form a stroke.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GesturePoint](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint#GesturePoint(kotlin.Float,%20kotlin.Float,%20kotlin.Long))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `t:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint#clone())`()` <br /> |

| Properties ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [timestamp](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint#timestamp:kotlin.Long) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [x](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint#x:kotlin.Float) <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [y](https://developer.android.com/reference/kotlin/android/gesture/GesturePoint#y:kotlin.Float) <br /> |

## Public constructors

### GesturePoint

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GesturePoint(
    x: Float, 
    y: Float, 
    t: Long)
```

## Public methods

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

## Properties

### timestamp

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val timestamp: Long
```  

### x

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val x: Float
```  

### y

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val y: Float
```

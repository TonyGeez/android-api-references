# OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OperationApplicationException

Kotlin| [Java](https://developer.android.com/reference/android/content/OperationApplicationException "View this page in Java") 

```
open class OperationApplicationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.content.OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#) |

Thrown when an application of a [ContentProviderOperation](https://developer.android.com/reference/kotlin/android/content/ContentProviderOperation) fails due the specified constraints.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#OperationApplicationException())`()` <br /> |
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#OperationApplicationException(kotlin.Int))`(`numSuccessfulYieldPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#OperationApplicationException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#OperationApplicationException(kotlin.String,%20kotlin.Int))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `numSuccessfulYieldPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#OperationApplicationException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [OperationApplicationException](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#OperationApplicationException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumSuccessfulYieldPoints](https://developer.android.com/reference/kotlin/android/content/OperationApplicationException#getNumSuccessfulYieldPoints())`()` <br /> |

## Public constructors

### OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OperationApplicationException()
```  

### OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OperationApplicationException(numSuccessfulYieldPoints: Int)
```  

### OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OperationApplicationException(message: String!)
```  

### OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OperationApplicationException(
    message: String!, 
    numSuccessfulYieldPoints: Int)
```  

### OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OperationApplicationException(
    message: String!, 
    cause: Throwable!)
```  

### OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OperationApplicationException(cause: Throwable!)
```

## Public methods

### getNumSuccessfulYieldPoints

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumSuccessfulYieldPoints(): Int
```

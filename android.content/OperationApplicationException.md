# OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OperationApplicationException

Kotlin| [Java](../android/content/OperationApplicationException.md) 
| --- | --- |

```
open class OperationApplicationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.content.OperationApplicationException](../android/content/OperationApplicationException.md) |
| --- | --- | --- | --- |

Thrown when an application of a [ContentProviderOperation](../android/content/ContentProviderOperation.md) fails due the specified constraints.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OperationApplicationException](../android/content/OperationApplicationException.md))`()` <br /> |
| [OperationApplicationException](../android/content/OperationApplicationException.md))`(`numSuccessfulYieldPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OperationApplicationException](../android/content/OperationApplicationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [OperationApplicationException](../android/content/OperationApplicationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `numSuccessfulYieldPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OperationApplicationException](../android/content/OperationApplicationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [OperationApplicationException](../android/content/OperationApplicationException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumSuccessfulYieldPoints](../android/content/OperationApplicationException.md))`()` <br /> |

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

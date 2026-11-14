# OperationApplicationException

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OperationApplicationException

Kotlin| [Java](OperationApplicationException.md) 
| --- | --- |

```
open class OperationApplicationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.content.OperationApplicationException](OperationApplicationException.md) |
| --- | --- | --- | --- |

Thrown when an application of a [ContentProviderOperation](ContentProviderOperation.md) fails due the specified constraints.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OperationApplicationException](OperationApplicationException.md))`()` <br /> |
| [OperationApplicationException](OperationApplicationException.md))`(`numSuccessfulYieldPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OperationApplicationException](OperationApplicationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [OperationApplicationException](OperationApplicationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `numSuccessfulYieldPoints:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OperationApplicationException](OperationApplicationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| [OperationApplicationException](OperationApplicationException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumSuccessfulYieldPoints](OperationApplicationException.md))`()` <br /> |

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

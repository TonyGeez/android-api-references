# BatchUpdateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BatchUpdateException

```
open class BatchUpdateException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.sql.SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) ||
| | | | ↳ | [java.sql.BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#) |

The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) thrown when an error occurs during a batch update operation. In addition to the information provided by [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException), a`BatchUpdateException`provides the update counts for all commands that were executed successfully during the batch update, that is, all commands that were executed before the error occurred. The order of elements in an array of update counts corresponds to the order in which commands were added to the batch.

After a command in a batch update fails to execute properly and a`BatchUpdateException`is thrown, the driver may or may not continue to process the remaining commands in the batch. If the driver continues processing after a failure, the array returned by the method`BatchUpdateException.getUpdateCounts`will have an element for every command in the batch rather than only elements for the commands that executed successfully before the error. In the case where the driver continues processing commands, the array element for any command that failed is`Statement.EXECUTE_FAILED`.

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException())`()` Constructs a`BatchUpdateException`object. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.IntArray))`(`updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.IntArray,%20kotlin.Throwable))`(`updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`cause`and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.String,%20kotlin.IntArray))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`reason`and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.String,%20kotlin.IntArray,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`reason`,`cause`and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.IntArray))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`,`vendorCode`and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`,`vendorCode``cause`and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.String,%20kotlin.String,%20kotlin.IntArray))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.String,%20kotlin.String,%20kotlin.IntArray,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `updateCounts:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`,`cause`, and`updateCounts`. |
| [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#BatchUpdateException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`BatchUpdateException`object initialized with a given`cause`. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getUpdateCounts](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException#getUpdateCounts())`()` Retrieves the update count for each update statement in the batch update that executed successfully before this exception occurred. |

| Inherited functions ||
|---|---|
| From class [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/java/sql/SQLException#getErrorCode())`()` <br /> Retrieves the vendor-specific exception code for this`SQLException`object. <br /> | | [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException)! | [getNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#getNextException())`()` <br /> Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](https://developer.android.com/reference/kotlin/java/sql/SQLException#getSQLState())`()` <br /> Retrieves the SQLState for this`SQLException`object. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | [iterator](https://developer.android.com/reference/kotlin/java/sql/SQLException#iterator())`()` <br /> Returns an iterator over the chained SQLExceptions. The iterator will be used to iterate over each SQLException and its underlying cause (if any). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#setNextException(java.sql.SQLException))`(`ex:` ` [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException)!`)` <br /> Adds an`SQLException`object to the end of the chain. <br /> | ||

## Public constructors

### BatchUpdateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException()
```

Constructs a`BatchUpdateException`object. The`reason`,`SQLState`and`updateCounts`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

### BatchUpdateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(updateCounts: IntArray!)
```

Constructs a`BatchUpdateException`object initialized with a given`updateCounts`. initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method. The`reason`and`SQLState`are initialized to null and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |

### BatchUpdateException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    updateCounts: IntArray!, 
    cause: Throwable!)
```

Constructs a`BatchUpdateException`object initialized with a given`cause`and`updateCounts`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### BatchUpdateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    reason: String!, 
    updateCounts: IntArray!)
```

Constructs a`BatchUpdateException`object initialized with a given`reason`and`updateCounts`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method. The`SQLState`is initialized to`null`and the vender code is initialized to 0.

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |

### BatchUpdateException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    reason: String!, 
    updateCounts: IntArray!, 
    cause: Throwable!)
```

Constructs a`BatchUpdateException`object initialized with a given`reason`,`cause`and`updateCounts`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### BatchUpdateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    updateCounts: IntArray!)
```

Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`,`vendorCode`and`updateCounts`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the error |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an exception code used by a particular database vendor |
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |

### BatchUpdateException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    updateCounts: IntArray!, 
    cause: Throwable!)
```

Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`,`vendorCode``cause`and`updateCounts`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the error |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an exception code used by a particular database vendor |
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### BatchUpdateException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    reason: String!, 
    SQLState: String!, 
    updateCounts: IntArray!)
```

Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`and`updateCounts`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |

### BatchUpdateException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(
    reason: String!, 
    SQLState: String!, 
    updateCounts: IntArray!, 
    cause: Throwable!)
```

Constructs a`BatchUpdateException`object initialized with a given`reason`,`SQLState`,`cause`, and`updateCounts`. The vendor code is initialized to 0.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `updateCounts` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array of`int`, with each element indicating the update count,`Statement.SUCCESS_NO_INFO`or`Statement.EXECUTE_FAILED`for each SQL command in the batch for JDBC drivers that continue processing after a command failure; an update count or`Statement.SUCCESS_NO_INFO`for each SQL command in the batch prior to the failure for JDBC drivers that stop processing after a command failure |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### BatchUpdateException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BatchUpdateException(cause: Throwable!)
```

Constructs a`BatchUpdateException`object initialized with a given`cause`. The`SQLState`and`updateCounts`are initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

## Public methods

### getUpdateCounts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUpdateCounts(): IntArray!
```

Retrieves the update count for each update statement in the batch update that executed successfully before this exception occurred. A driver that implements batch updates may or may not continue to process the remaining commands in a batch when one of the commands fails to execute properly. If the driver continues processing commands, the array returned by this method will have as many elements as there are commands in the batch; otherwise, it will contain an update count for each command that executed successfully before the`BatchUpdateException`was thrown.

The possible return values for this method were modified for the Java 2 SDK, Standard Edition, version 1.3. This was done to accommodate the new option of continuing to process commands in a batch update after a`BatchUpdateException`object has been thrown.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array of`int`containing the update counts for the updates that were executed successfully before this error occurred. Or, if the driver continues to process commands after an error, one of the following for every command in the batch: 1. an update count 2. `Statement.SUCCESS_NO_INFO`to indicate that the command executed successfully but the number of rows affected is unknown 3. `Statement.EXECUTE_FAILED`to indicate that the command failed to execute successfully |

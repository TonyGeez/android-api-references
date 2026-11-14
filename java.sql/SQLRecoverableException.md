# SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLRecoverableException

```
open class SQLRecoverableException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.sql.SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#) |

The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) thrown in situations where a previously failed operation might be able to succeed if the application performs some recovery steps and retries the entire transaction or in the case of a distributed transaction, the transaction branch. At a minimum, the recovery operation must include closing the current connection and getting a new connection.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException())`()` Constructs a`SQLRecoverableException`object. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLRecoverableException`object with a given`reason`. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.String,%20kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLRecoverableException`object with a given`reason`and`SQLState`. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.String,%20kotlin.String,%20kotlin.Int))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLRecoverableException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLRecoverableException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLRecoverableException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.String,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLRecoverableException`object with a given`reason`and`cause`. |
| [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException#SQLRecoverableException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLRecoverableException`object with a given`cause`. |

| Inherited functions ||
|---|---|
| From class [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/java/sql/SQLException#getErrorCode())`()` <br /> Retrieves the vendor-specific exception code for this`SQLException`object. <br /> | | [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException)! | [getNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#getNextException())`()` <br /> Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](https://developer.android.com/reference/kotlin/java/sql/SQLException#getSQLState())`()` <br /> Retrieves the SQLState for this`SQLException`object. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | [iterator](https://developer.android.com/reference/kotlin/java/sql/SQLException#iterator())`()` <br /> Returns an iterator over the chained SQLExceptions. The iterator will be used to iterate over each SQLException and its underlying cause (if any). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#setNextException(java.sql.SQLException))`(`ex:` ` [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException)!`)` <br /> Adds an`SQLException`object to the end of the chain. <br /> | ||

## Public constructors

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException()
```

Constructs a`SQLRecoverableException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(reason: String!)
```

Constructs a`SQLRecoverableException`object with a given`reason`. The`SQLState`is initialized to`null`and the vender code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(
    reason: String!, 
    SQLState: String!)
```

Constructs a`SQLRecoverableException`object with a given`reason`and`SQLState`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a`SQLRecoverableException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor specific exception code |
| --- | --- |

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a`SQLRecoverableException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`.

<br />

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(
    reason: String!, 
    SQLState: String!, 
    cause: Throwable!)
```

Constructs a`SQLRecoverableException`object with a given`reason`,`SQLState`and`cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a`SQLRecoverableException`object with a given`reason`and`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLRecoverableException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLRecoverableException(cause: Throwable!)
```

Constructs a`SQLRecoverableException`object with a given`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

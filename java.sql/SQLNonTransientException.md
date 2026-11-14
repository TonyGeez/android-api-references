# SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLNonTransientException

```
open class SQLNonTransientException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.sql.SQLException](SQLException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLNonTransientException](SQLNonTransientException.md) |

| Known Direct Subclasses [SQLDataException](SQLDataException.md), [SQLFeatureNotSupportedException](SQLFeatureNotSupportedException.md), [SQLIntegrityConstraintViolationException](SQLIntegrityConstraintViolationException.md), [SQLInvalidAuthorizationSpecException](SQLInvalidAuthorizationSpecException.md), [SQLNonTransientConnectionException](SQLNonTransientConnectionException.md), [SQLSyntaxErrorException](SQLSyntaxErrorException.md) |----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLDataException](SQLDataException.md) | The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*22*', or under vendor-specified conditions. | | [SQLFeatureNotSupportedException](SQLFeatureNotSupportedException.md) | The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*0A*' ( the value is 'zero' A). | | [SQLIntegrityConstraintViolationException](SQLIntegrityConstraintViolationException.md) | The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*23*', or under vendor-specified conditions. | | [SQLInvalidAuthorizationSpecException](SQLInvalidAuthorizationSpecException.md) | The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*28*', or under vendor-specified conditions. | | [SQLNonTransientConnectionException](SQLNonTransientConnectionException.md) | The subclass of [SQLException](SQLException.md) thrown for the SQLState class value '*08*', or under vendor-specified conditions. | | [SQLSyntaxErrorException](SQLSyntaxErrorException.md) | The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*42*', or under vendor-specified conditions. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The subclass of [SQLException](SQLException.md) thrown when an instance where a retry of the same operation would fail unless the cause of the`SQLException`is corrected.

<br />

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLNonTransientException](SQLNonTransientException.md))`()` Constructs a`SQLNonTransientException`object. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLNonTransientException`object with a given`reason`. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLNonTransientException`object with a given`reason`and`SQLState`. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLNonTransientException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLNonTransientException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLNonTransientException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLTransientException`object with a given`reason`and`cause`. |
| [SQLNonTransientException](SQLNonTransientException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLNonTransientException`object with a given`cause`. |

| Inherited functions ||
|---|---|
| From class [SQLException](SQLException.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](SQLException.md))`()` <br /> Retrieves the vendor-specific exception code for this`SQLException`object. <br /> | | [SQLException](SQLException.md)! | [getNextException](SQLException.md))`()` <br /> Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](SQLException.md))`()` <br /> Retrieves the SQLState for this`SQLException`object. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | [iterator](SQLException.md))`()` <br /> Returns an iterator over the chained SQLExceptions. The iterator will be used to iterate over each SQLException and its underlying cause (if any). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](SQLException.md))`(`ex:` ` [SQLException](SQLException.md)!`)` <br /> Adds an`SQLException`object to the end of the chain. <br /> | ||

## Public constructors

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException()
```

Constructs a`SQLNonTransientException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(reason: String!)
```

Constructs a`SQLNonTransientException`object with a given`reason`. The`SQLState`is initialized to`null`and the vender code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(
    reason: String!, 
    SQLState: String!)
```

Constructs a`SQLNonTransientException`object with a given`reason`and`SQLState`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a`SQLNonTransientException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor specific exception code |
| --- | --- |

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a`SQLNonTransientException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`.

<br />

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(
    reason: String!, 
    SQLState: String!, 
    cause: Throwable!)
```

Constructs a`SQLNonTransientException`object with a given`reason`,`SQLState`and`cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a`SQLTransientException`object with a given`reason`and`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLNonTransientException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLNonTransientException(cause: Throwable!)
```

Constructs a`SQLNonTransientException`object with a given`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

# SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLException

```
open class SQLException : Exception, MutableIterable<Throwable!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.sql.SQLException](../java/sql/SQLException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [BatchUpdateException](../java/sql/BatchUpdateException.md), [SQLClientInfoException](../java/sql/SQLClientInfoException.md), [SQLNonTransientException](../java/sql/SQLNonTransientException.md), [SQLRecoverableException](../java/sql/SQLRecoverableException.md), [SQLTransientException](../java/sql/SQLTransientException.md), [SQLWarning](../java/sql/SQLWarning.md) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BatchUpdateException](../java/sql/BatchUpdateException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when an error occurs during a batch update operation. | | [SQLClientInfoException](../java/sql/SQLClientInfoException.md) | The subclass of [SQLException](../java/sql/SQLException.md) is thrown when one or more client info properties could not be set on a`Connection`. | | [SQLNonTransientException](../java/sql/SQLNonTransientException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when an instance where a retry of the same operation would fail unless the cause of the`SQLException`is corrected. | | [SQLRecoverableException](../java/sql/SQLRecoverableException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown in situations where a previously failed operation might be able to succeed if the application performs some recovery steps and retries the entire transaction or in the case of a distributed transaction, the transaction branch. | | [SQLTransientException](../java/sql/SQLTransientException.md) | The subclass of [SQLException](../java/sql/SQLException.md) is thrown in situations where a previoulsy failed operation might be able to succeed when the operation is retried without any intervention by application-level functionality. | | [SQLWarning](../java/sql/SQLWarning.md) | An exception that provides information on database access warnings. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DataTruncation](../java/sql/DataTruncation.md), [SQLDataException](../java/sql/SQLDataException.md), [SQLFeatureNotSupportedException](../java/sql/SQLFeatureNotSupportedException.md), [SQLIntegrityConstraintViolationException](../java/sql/SQLIntegrityConstraintViolationException.md), [SQLInvalidAuthorizationSpecException](../java/sql/SQLInvalidAuthorizationSpecException.md), [SQLNonTransientConnectionException](../java/sql/SQLNonTransientConnectionException.md), [SQLSyntaxErrorException](../java/sql/SQLSyntaxErrorException.md), [SQLTimeoutException](../java/sql/SQLTimeoutException.md), [SQLTransactionRollbackException](../java/sql/SQLTransactionRollbackException.md), [SQLTransientConnectionException](../java/sql/SQLTransientConnectionException.md) |----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DataTruncation](../java/sql/DataTruncation.md) | An exception thrown as a`DataTruncation`exception (on writes) or reported as a`DataTruncation`warning (on reads) when a data values is unexpectedly truncated for reasons other than its having execeeded`MaxFieldSize`. | | [SQLDataException](../java/sql/SQLDataException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the SQLState class value is '*22*', or under vendor-specified conditions. | | [SQLFeatureNotSupportedException](../java/sql/SQLFeatureNotSupportedException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the SQLState class value is '*0A*' ( the value is 'zero' A). | | [SQLIntegrityConstraintViolationException](../java/sql/SQLIntegrityConstraintViolationException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the SQLState class value is '*23*', or under vendor-specified conditions. | | [SQLInvalidAuthorizationSpecException](../java/sql/SQLInvalidAuthorizationSpecException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the SQLState class value is '*28*', or under vendor-specified conditions. | | [SQLNonTransientConnectionException](../java/sql/SQLNonTransientConnectionException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown for the SQLState class value '*08*', or under vendor-specified conditions. | | [SQLSyntaxErrorException](../java/sql/SQLSyntaxErrorException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the SQLState class value is '*42*', or under vendor-specified conditions. | | [SQLTimeoutException](../java/sql/SQLTimeoutException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the timeout specified by`Statement`has expired. | | [SQLTransactionRollbackException](../java/sql/SQLTransactionRollbackException.md) | The subclass of [SQLException](../java/sql/SQLException.md) thrown when the SQLState class value is '*40*', or under vendor-specified conditions. | | [SQLTransientConnectionException](../java/sql/SQLTransientConnectionException.md) | The subclass of [SQLException](../java/sql/SQLException.md) for the SQLState class value '*08*', or under vendor-specified conditions. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An exception that provides information on a database access error or other errors.

Each`SQLException`provides several kinds of information:

- a string describing the error. This is used as the Java Exception message, available via the method`getMesasge`.
- a "SQLstate" string, which follows either the XOPEN SQLstate conventions or the SQL:2003 conventions. The values of the SQLState string are described in the appropriate spec. The`DatabaseMetaData`method`getSQLStateType`can be used to discover whether the driver returns the XOPEN type or the SQL:2003 type.
- an integer error code that is specific to each vendor. Normally this will be the actual error code returned by the underlying database.
- a chain to a next Exception. This can be used to provide additional error information.
- the causal relationship, if any for this`SQLException`.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLException](../java/sql/SQLException.md))`()` Constructs a`SQLException`object. |
| [SQLException](../java/sql/SQLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLException`object with a given`reason`. |
| [SQLException](../java/sql/SQLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLException`object with a given`reason`and`SQLState`. |
| [SQLException](../java/sql/SQLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLException](../java/sql/SQLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLException](../java/sql/SQLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLException](../java/sql/SQLException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`reason`and`cause`. |
| [SQLException](../java/sql/SQLException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`cause`. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../java/sql/SQLException.md))`()` Retrieves the vendor-specific exception code for this`SQLException`object. |
| open [SQLException](../java/sql/SQLException.md)! | [getNextException](../java/sql/SQLException.md))`()` Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](../java/sql/SQLException.md))`()` Retrieves the SQLState for this`SQLException`object. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\> | [iterator](../java/sql/SQLException.md))`()` Returns an iterator over the chained SQLExceptions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](../java/sql/SQLException.md))`(`ex:` ` [SQLException](../java/sql/SQLException.md)!`)` Adds an`SQLException`object to the end of the chain. |

## Public constructors

### SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException()
```

Constructs a`SQLException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

### SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(reason: String!)
```

Constructs a`SQLException`object with a given`reason`. The`SQLState`is initialized to`null`and the vender code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |

### SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(
    reason: String!, 
    SQLState: String!)
```

Constructs a`SQLException`object with a given`reason`and`SQLState`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |

### SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a`SQLException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |

### SQLException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(
    reason: String!, 
    sqlState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a`SQLException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`.

<br />

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `sqlState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(
    reason: String!, 
    sqlState: String!, 
    cause: Throwable!)
```

Constructs a`SQLException`object with a given`reason`,`SQLState`and`cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `sqlState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a`SQLException`object with a given`reason`and`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(cause: Throwable!)
```

Constructs a`SQLException`object with a given`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

## Public methods

### getErrorCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorCode(): Int
```

Retrieves the vendor-specific exception code for this`SQLException`object.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the vendor's error code |

### getNextException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNextException(): SQLException!
```

Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex).

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [SQLException](../java/sql/SQLException.md)! | the next`SQLException`object in the chain;`null`if there are none |

**See Also**

- [#setNextException](../java/sql/SQLException.md)) 

### getSQLState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSQLState(): String!
```

Retrieves the SQLState for this`SQLException`object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the SQLState value |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<Throwable!>
```

Returns an iterator over the chained SQLExceptions. The iterator will be used to iterate over each SQLException and its underlying cause (if any).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | an iterator over the chained SQLExceptions and causes in the proper order |

### setNextException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNextException(ex: SQLException!): Unit
```

Adds an`SQLException`object to the end of the chain.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ex` | [SQLException](../java/sql/SQLException.md)!:the new exception that will be added to the end of the`SQLException`chain |

**See Also**

- [#getNextException](../java/sql/SQLException.md))

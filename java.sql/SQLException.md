# SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLException

```
open class SQLException : Exception, MutableIterable<Throwable!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.sql.SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) |
| --- | --- | --- | --- |

| Known Direct Subclasses [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException), [SQLClientInfoException](https://developer.android.com/reference/kotlin/java/sql/SQLClientInfoException), [SQLNonTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientException), [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException), [SQLTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLTransientException), [SQLWarning](https://developer.android.com/reference/kotlin/java/sql/SQLWarning) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BatchUpdateException](https://developer.android.com/reference/kotlin/java/sql/BatchUpdateException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when an error occurs during a batch update operation. | | [SQLClientInfoException](https://developer.android.com/reference/kotlin/java/sql/SQLClientInfoException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) is thrown when one or more client info properties could not be set on a`Connection`. | | [SQLNonTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when an instance where a retry of the same operation would fail unless the cause of the`SQLException`is corrected. | | [SQLRecoverableException](https://developer.android.com/reference/kotlin/java/sql/SQLRecoverableException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown in situations where a previously failed operation might be able to succeed if the application performs some recovery steps and retries the entire transaction or in the case of a distributed transaction, the transaction branch. | | [SQLTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLTransientException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) is thrown in situations where a previoulsy failed operation might be able to succeed when the operation is retried without any intervention by application-level functionality. | | [SQLWarning](https://developer.android.com/reference/kotlin/java/sql/SQLWarning) | An exception that provides information on database access warnings. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DataTruncation](https://developer.android.com/reference/kotlin/java/sql/DataTruncation), [SQLDataException](https://developer.android.com/reference/kotlin/java/sql/SQLDataException), [SQLFeatureNotSupportedException](https://developer.android.com/reference/kotlin/java/sql/SQLFeatureNotSupportedException), [SQLIntegrityConstraintViolationException](https://developer.android.com/reference/kotlin/java/sql/SQLIntegrityConstraintViolationException), [SQLInvalidAuthorizationSpecException](https://developer.android.com/reference/kotlin/java/sql/SQLInvalidAuthorizationSpecException), [SQLNonTransientConnectionException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientConnectionException), [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException), [SQLTimeoutException](https://developer.android.com/reference/kotlin/java/sql/SQLTimeoutException), [SQLTransactionRollbackException](https://developer.android.com/reference/kotlin/java/sql/SQLTransactionRollbackException), [SQLTransientConnectionException](https://developer.android.com/reference/kotlin/java/sql/SQLTransientConnectionException) |----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DataTruncation](https://developer.android.com/reference/kotlin/java/sql/DataTruncation) | An exception thrown as a`DataTruncation`exception (on writes) or reported as a`DataTruncation`warning (on reads) when a data values is unexpectedly truncated for reasons other than its having execeeded`MaxFieldSize`. | | [SQLDataException](https://developer.android.com/reference/kotlin/java/sql/SQLDataException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the SQLState class value is '*22*', or under vendor-specified conditions. | | [SQLFeatureNotSupportedException](https://developer.android.com/reference/kotlin/java/sql/SQLFeatureNotSupportedException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the SQLState class value is '*0A*' ( the value is 'zero' A). | | [SQLIntegrityConstraintViolationException](https://developer.android.com/reference/kotlin/java/sql/SQLIntegrityConstraintViolationException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the SQLState class value is '*23*', or under vendor-specified conditions. | | [SQLInvalidAuthorizationSpecException](https://developer.android.com/reference/kotlin/java/sql/SQLInvalidAuthorizationSpecException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the SQLState class value is '*28*', or under vendor-specified conditions. | | [SQLNonTransientConnectionException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientConnectionException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown for the SQLState class value '*08*', or under vendor-specified conditions. | | [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the SQLState class value is '*42*', or under vendor-specified conditions. | | [SQLTimeoutException](https://developer.android.com/reference/kotlin/java/sql/SQLTimeoutException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the timeout specified by`Statement`has expired. | | [SQLTransactionRollbackException](https://developer.android.com/reference/kotlin/java/sql/SQLTransactionRollbackException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) thrown when the SQLState class value is '*40*', or under vendor-specified conditions. | | [SQLTransientConnectionException](https://developer.android.com/reference/kotlin/java/sql/SQLTransientConnectionException) | The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#) for the SQLState class value '*08*', or under vendor-specified conditions. | |
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
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException())`()` Constructs a`SQLException`object. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLException`object with a given`reason`. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.String,%20kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLException`object with a given`reason`and`SQLState`. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.String,%20kotlin.String,%20kotlin.Int))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sqlState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.String,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`reason`and`cause`. |
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#SQLException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLException`object with a given`cause`. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/java/sql/SQLException#getErrorCode())`()` Retrieves the vendor-specific exception code for this`SQLException`object. |
| open [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#)! | [getNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#getNextException())`()` Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](https://developer.android.com/reference/kotlin/java/sql/SQLException#getSQLState())`()` Retrieves the SQLState for this`SQLException`object. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\> | [iterator](https://developer.android.com/reference/kotlin/java/sql/SQLException#iterator())`()` Returns an iterator over the chained SQLExceptions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#setNextException(java.sql.SQLException))`(`ex:` ` [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#)!`)` Adds an`SQLException`object to the end of the chain. |

## Public constructors

### SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException()
```

Constructs a`SQLException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

### SQLException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLException(reason: String!)
```

Constructs a`SQLException`object with a given`reason`. The`SQLState`is initialized to`null`and the vender code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

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

Constructs a`SQLException`object with a given`reason`and`SQLState`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method. The vendor code is initialized to 0.

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

Constructs a`SQLException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

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
| [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#)! | the next`SQLException`object in the chain;`null`if there are none |

**See Also**

- [#setNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#setNextException(java.sql.SQLException)) 

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
| `ex` | [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException#)!:the new exception that will be added to the end of the`SQLException`chain |

**See Also**

- [#getNextException](https://developer.android.com/reference/kotlin/java/sql/SQLException#getNextException())

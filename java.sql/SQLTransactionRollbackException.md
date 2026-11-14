# SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLTransactionRollbackException

```
open class SQLTransactionRollbackException : SQLTransientException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.sql.SQLException](SQLException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLTransientException](SQLTransientException.md) ||
| | | | | ↳ | [java.sql.SQLTransactionRollbackException](SQLTransactionRollbackException.md) |

The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*40*', or under vendor-specified conditions. This indicates that the current statement was automatically rolled back by the database because of deadlock or other transaction serialization failures.

Please consult your driver vendor documentation for the vendor-specified conditions for which this`Exception`may be thrown.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`()` Constructs a`SQLTransactionRollbackException`object. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLTransactionRollbackException`object with a given`reason`. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLTransactionRollbackException`object with a given`reason`and`SQLState`. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLTransactionRollbackException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLTransactionRollbackException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLTransactionRollbackException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLTransactionRollbackException`object with a given`reason`and`cause`. |
| [SQLTransactionRollbackException](SQLTransactionRollbackException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLTransactionRollbackException`object with a given`cause`. |

## Public constructors

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException()
```

Constructs a`SQLTransactionRollbackException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(reason: String!)
```

Constructs a`SQLTransactionRollbackException`object with a given`reason`. The`SQLState`is initialized to`null`and the vender code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(
    reason: String!, 
    SQLState: String!)
```

Constructs a`SQLTransactionRollbackException`object with a given`reason`and`SQLState`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a`SQLTransactionRollbackException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor specific exception code |
| --- | --- |

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a`SQLTransactionRollbackException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`.

<br />

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(
    reason: String!, 
    SQLState: String!, 
    cause: Throwable!)
```

Constructs a`SQLTransactionRollbackException`object with a given`reason`,`SQLState`and`cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a`SQLTransactionRollbackException`object with a given`reason`and`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLTransactionRollbackException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTransactionRollbackException(cause: Throwable!)
```

Constructs a`SQLTransactionRollbackException`object with a given`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

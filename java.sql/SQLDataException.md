# SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLDataException

```
open class SQLDataException : SQLNonTransientException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.sql.SQLException](SQLException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLNonTransientException](SQLNonTransientException.md) ||
| | | | | ↳ | [java.sql.SQLDataException](SQLDataException.md) |

The subclass of [SQLException](SQLException.md) thrown when the SQLState class value is '*22*', or under vendor-specified conditions. This indicates various data errors, including but not limited to data conversion errors, division by 0, and invalid arguments to functions.

Please consult your driver vendor documentation for the vendor-specified conditions for which this`Exception`may be thrown.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLDataException](SQLDataException.md))`()` Constructs a`SQLDataException`object. |
| [SQLDataException](SQLDataException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLDataException`object with a given`reason`. |
| [SQLDataException](SQLDataException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLDataException`object with a given`reason`and`SQLState`. |
| [SQLDataException](SQLDataException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLDataException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLDataException](SQLDataException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLDataException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLDataException](SQLDataException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLDataException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLDataException](SQLDataException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLDataException`object with a given`reason`and`cause`. |
| [SQLDataException](SQLDataException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLDataException`object with a given`cause`. |

## Public constructors

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException()
```

Constructs a`SQLDataException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(reason: String!)
```

Constructs a`SQLDataException`object with a given`reason`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(
    reason: String!, 
    SQLState: String!)
```

Constructs a`SQLDataException`object with a given`reason`and`SQLState`. The vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a`SQLDataException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to [Throwable.initCause(java.lang.Throwable)](../java.lang/Throwable.md))method.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor specific exception code |
| --- | --- |

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a`SQLDataException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`.

<br />

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(
    reason: String!, 
    SQLState: String!, 
    cause: Throwable!)
```

Constructs a`SQLDataException`object with a given`reason`,`SQLState`and`cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a`SQLDataException`object with a given`reason`and`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLDataException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLDataException(cause: Throwable!)
```

Constructs a`SQLDataException`object with a given`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

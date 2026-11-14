# SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLTimeoutException

```
open class SQLTimeoutException : SQLTransientException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.sql.SQLException](../java/sql/SQLException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLTransientException](../java/sql/SQLTransientException.md) ||
| | | | | ↳ | [java.sql.SQLTimeoutException](../java/sql/SQLTimeoutException.md) |

The subclass of [SQLException](../java/sql/SQLException.md) thrown when the timeout specified by `Statement` has expired.

This exception does not correspond to a standard SQLState.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`()` Constructs a `SQLTimeoutException` object. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `SQLTimeoutException` object with a given `reason`. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `SQLTimeoutException` object with a given `reason` and `SQLState`. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a `SQLTimeoutException` object with a given `reason`, `SQLState` and `vendorCode`. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `SQLTimeoutException` object with a given `reason`, `SQLState`, `vendorCode` and `cause`. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `SQLTimeoutException` object with a given `reason`, `SQLState` and `cause`. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `SQLTimeoutException` object with a given `reason` and `cause`. |
| [SQLTimeoutException](../java/sql/SQLTimeoutException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a `SQLTimeoutException` object with a given `cause`. |

## Public constructors

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException()
```

Constructs a `SQLTimeoutException` object. The `reason`, `SQLState` are initialized to `null` and the vendor code is initialized to 0. The `cause` is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md)) method.

<br />

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(reason: String!)
```

Constructs a `SQLTimeoutException` object with a given `reason`. The `SQLState` is initialized to `null` and the vender code is initialized to 0. The `cause` is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md)) method.

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the exception |

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(
    reason: String!, 
    SQLState: String!)
```

Constructs a `SQLTimeoutException` object with a given `reason` and `SQLState`. The `cause` is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md)) method. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: an XOPEN or SQL:2003 code identifying the exception |

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a `SQLTimeoutException` object with a given `reason`, `SQLState` and `vendorCode`. The `cause` is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md)) method.

<br />

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a database vendor specific exception code |
| --- | --- |

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a `SQLTimeoutException` object with a given `reason`, `SQLState`, `vendorCode` and `cause`.

<br />

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the underlying reason for this `SQLException` (which is saved for later retrieval by the `getCause()` method); may be null indicating the cause is non-existent or unknown. |

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(
    reason: String!, 
    SQLState: String!, 
    cause: Throwable!)
```

Constructs a `SQLTimeoutException` object with a given `reason`, `SQLState` and `cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the exception. |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the underlying reason for this `SQLException` (which is saved for later retrieval by the `getCause()` method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a `SQLTimeoutException` object with a given `reason` and `cause`. The `SQLState` is initialized to `null` and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the underlying reason for this `SQLException` (which is saved for later retrieval by the `getCause()` method); may be null indicating the cause is non-existent or unknown. |

### SQLTimeoutException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLTimeoutException(cause: Throwable!)
```

Constructs a `SQLTimeoutException` object with a given `cause`. The `SQLState` is initialized to `null` and the vendor code is initialized to 0. The `reason` is initialized to `null` if `cause==null` or to `cause.toString()` if `cause!=null`.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the underlying reason for this `SQLException` (which is saved for later retrieval by the `getCause()` method); may be null indicating the cause is non-existent or unknown. |

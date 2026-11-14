# SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLSyntaxErrorException

```
open class SQLSyntaxErrorException : SQLNonTransientException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.sql.SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLNonTransientException](https://developer.android.com/reference/kotlin/java/sql/SQLNonTransientException) ||
| | | | | ↳ | [java.sql.SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#) |

The subclass of [SQLException](https://developer.android.com/reference/kotlin/java/sql/SQLException) thrown when the SQLState class value is '*42*', or under vendor-specified conditions. This indicates that the in-progress query has violated SQL syntax rules.

Please consult your driver vendor documentation for the vendor-specified conditions for which this`Exception`may be thrown.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException())`()` Constructs a`SQLSyntaxErrorException`object. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLSyntaxErrorException`object with a given`reason`. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.String,%20kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`SQLSyntaxErrorException`object with a given`reason`and`SQLState`. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.String,%20kotlin.String,%20kotlin.Int))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`SQLSyntaxErrorException`object with a given`reason`,`SQLState`and`vendorCode`. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLSyntaxErrorException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLSyntaxErrorException`object with a given`reason`,`SQLState`and`cause`. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.String,%20kotlin.Throwable))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLSyntaxErrorException`object with a given`reason`and`cause`. |
| [SQLSyntaxErrorException](https://developer.android.com/reference/kotlin/java/sql/SQLSyntaxErrorException#SQLSyntaxErrorException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLSyntaxErrorException`object with a given`cause`. |

## Public constructors

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException()
```

Constructs a`SQLSyntaxErrorException`object. The`reason`,`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(reason: String!)
```

Constructs a`SQLSyntaxErrorException`object with a given`reason`. The`SQLState`is initialized to`null`and the vender code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(
    reason: String!, 
    SQLState: String!)
```

Constructs a`SQLSyntaxErrorException`object with a given`reason`and`SQLState`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int)
```

Constructs a`SQLSyntaxErrorException`object with a given`reason`,`SQLState`and`vendorCode`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#initCause(kotlin.Throwable))method.

<br />

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor specific exception code |
| --- | --- |

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    cause: Throwable!)
```

Constructs a`SQLSyntaxErrorException`object with a given`reason`,`SQLState`,`vendorCode`and`cause`.

<br />

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(
    reason: String!, 
    SQLState: String!, 
    cause: Throwable!)
```

Constructs a`SQLSyntaxErrorException`object with a given`reason`,`SQLState`and`cause`. The vendor code is initialized to 0.

<br />

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the (which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(
    reason: String!, 
    cause: Throwable!)
```

Constructs a`SQLSyntaxErrorException`object with a given`reason`and`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |

### SQLSyntaxErrorException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLSyntaxErrorException(cause: Throwable!)
```

Constructs a`SQLSyntaxErrorException`object with a given`cause`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval bythe`getCause()`method); may be null indicating the cause is non-existent or unknown. |

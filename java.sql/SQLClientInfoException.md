# SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLClientInfoException

```
open class SQLClientInfoException : SQLException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) |||
| | | ↳ | [java.sql.SQLException](../java/sql/SQLException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLClientInfoException](../java/sql/SQLClientInfoException.md) |

The subclass of [SQLException](../java/sql/SQLException.md) is thrown when one or more client info properties could not be set on a`Connection`. In addition to the information provided by`SQLException`, a`SQLClientInfoException`provides a list of client info properties that were not set. Some databases do not allow multiple client info properties to be set atomically. For those databases, it is possible that some of the client info properties had been set even though the`Connection.setClientInfo`method threw an exception. An application can use the`getFailedProperties `method to retrieve a list of client info properties that were not set. The properties are identified by passing a`Map<String,ClientInfoStatus>`to the appropriate`SQLClientInfoException`constructor.

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`()` Constructs a`SQLClientInfoException`Object. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`)` Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`,`vendorCode`and`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vendorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`,`cause`,`vendorCode`and`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`)` Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`and`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `SQLState:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`,`cause`and`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`)` Constructs a`SQLClientInfoException`object initialized with a given`reason`and`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLClientInfoException`object initialized with a given`reason`,`cause`and`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`)` Constructs a`SQLClientInfoException`object initialized with a given`failedProperties`. |
| [SQLClientInfoException](../java/sql/SQLClientInfoException.md))`(`failedProperties:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`SQLClientInfoException`object initialized with a given`cause`and`failedProperties`. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>! | [getFailedProperties](../java/sql/SQLClientInfoException.md))`()` Returns the list of client info properties that could not be set. |

| Inherited functions ||
|---|---|
| From class [SQLException](../java/sql/SQLException.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../java/sql/SQLException.md))`()` <br /> Retrieves the vendor-specific exception code for this`SQLException`object. <br /> | | [SQLException](../java/sql/SQLException.md)! | [getNextException](../java/sql/SQLException.md))`()` <br /> Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](../java/sql/SQLException.md))`()` <br /> Retrieves the SQLState for this`SQLException`object. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | [iterator](../java/sql/SQLException.md))`()` <br /> Returns an iterator over the chained SQLExceptions. The iterator will be used to iterate over each SQLException and its underlying cause (if any). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](../java/sql/SQLException.md))`(`ex:` ` [SQLException](../java/sql/SQLException.md)!`)` <br /> Adds an`SQLException`object to the end of the chain. <br /> | ||

## Public constructors

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException()
```

Constructs a`SQLClientInfoException`Object. The`reason`,`SQLState`, and failedProperties list are initialized to` null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    failedProperties: MutableMap<String!, ClientInfoStatus!>!)
```

Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`,`vendorCode`and`failedProperties`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` <br /> |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    reason: String!, 
    SQLState: String!, 
    vendorCode: Int, 
    failedProperties: MutableMap<String!, ClientInfoStatus!>!, 
    cause: Throwable!)
```

Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`,`cause`,`vendorCode`and`failedProperties`.

<br />

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `vendorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a database vendor-specific exception code |
| --- | --- |
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. <br /> |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    reason: String!, 
    SQLState: String!, 
    failedProperties: MutableMap<String!, ClientInfoStatus!>!)
```

Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`and`failedProperties`. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method. The vendor code is initialized to 0.

<br />

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` <br /> |
| --- | --- |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    reason: String!, 
    SQLState: String!, 
    failedProperties: MutableMap<String!, ClientInfoStatus!>!, 
    cause: Throwable!)
```

Constructs a`SQLClientInfoException`object initialized with a given`reason`,`SQLState`,`cause`and`failedProperties`. The vendor code is initialized to 0.

<br />

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `SQLState` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an XOPEN or SQL:2003 code identifying the exception |
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` |
| --- | --- |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. <br /> |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    reason: String!, 
    failedProperties: MutableMap<String!, ClientInfoStatus!>!)
```

Constructs a`SQLClientInfoException`object initialized with a given`reason`and`failedProperties`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` <br /> |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    reason: String!, 
    failedProperties: MutableMap<String!, ClientInfoStatus!>!, 
    cause: Throwable!)
```

Constructs a`SQLClientInfoException`object initialized with a given`reason`,`cause`and`failedProperties`. The`SQLState`is initialized to`null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a description of the exception |
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`SQLException`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. <br /> |
| --- | --- |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(failedProperties: MutableMap<String!, ClientInfoStatus!>!)
```

Constructs a`SQLClientInfoException`object initialized with a given`failedProperties`. The`reason`and`SQLState`are initialized to`null`and the vendor code is initialized to 0. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` <br /> |

### SQLClientInfoException

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SQLClientInfoException(
    failedProperties: MutableMap<String!, ClientInfoStatus!>!, 
    cause: Throwable!)
```

Constructs a`SQLClientInfoException`object initialized with a given`cause`and`failedProperties`. The`reason`is initialized to`null`if`cause==null`or to`cause.toString()`if`cause!=null`and the vendor code is initialized to 0.

<br />

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `failedProperties` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!\>!:A Map containing the property values that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus` |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the (which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. <br /> |

## Public methods

### getFailedProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFailedProperties(): MutableMap<String!, ClientInfoStatus!>!
```

Returns the list of client info properties that could not be set. The keys in the Map contain the names of the client info properties that could not be set and the values contain one of the reason codes defined in`ClientInfoStatus`

<br />

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [ClientInfoStatus](../java/sql/ClientInfoStatus.md)!>! | Map list containing the client info properties that could not be set <br /> |

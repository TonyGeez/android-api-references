# DataTruncation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataTruncation

```
open class DataTruncation : SQLWarning
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.sql.SQLException](../java/sql/SQLException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.sql.SQLWarning](../java/sql/SQLWarning.md) ||
| | | | | ↳ | [java.sql.DataTruncation](../java/sql/DataTruncation.md) |

An exception thrown as a`DataTruncation`exception (on writes) or reported as a`DataTruncation`warning (on reads) when a data values is unexpectedly truncated for reasons other than its having execeeded`MaxFieldSize`.

The SQLstate for a`DataTruncation`during read is`01004`.

The SQLstate for a`DataTruncation`during write is`22001`.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DataTruncation](../java/sql/DataTruncation.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parameter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `read:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `dataSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `transferSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`DataTruncation`object with the SQLState initialized to 01004 when`read`is set to`true`and 22001 when`read`is set to`false`, the reason set to "Data truncation", the vendor code set to 0, and the other fields set to the given values. |
| [DataTruncation](../java/sql/DataTruncation.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `parameter:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `read:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `dataSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `transferSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Creates a`DataTruncation`object with the SQLState initialized to 01004 when`read`is set to`true`and 22001 when`read`is set to`false`, the reason set to "Data truncation", the vendor code set to 0, and the other fields set to the given values. |

| Public methods ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataSize](../java/sql/DataTruncation.md))`()` Gets the number of bytes of data that should have been transferred. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../java/sql/DataTruncation.md))`()` Retrieves the index of the column or parameter that was truncated. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getParameter](../java/sql/DataTruncation.md))`()` Indicates whether the value truncated was a parameter value or a column value. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getRead](../java/sql/DataTruncation.md))`()` Indicates whether or not the value was truncated on a read. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransferSize](../java/sql/DataTruncation.md))`()` Gets the number of bytes of data actually transferred. |

| Inherited functions ||
|---|---|
| From class [SQLException](../java/sql/SQLException.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../java/sql/SQLException.md))`()` <br /> Retrieves the vendor-specific exception code for this`SQLException`object. <br /> | | [SQLException](../java/sql/SQLException.md)! | [getNextException](../java/sql/SQLException.md))`()` <br /> Retrieves the exception chained to this`SQLException`object by setNextException(SQLException ex). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSQLState](../java/sql/SQLException.md))`()` <br /> Retrieves the SQLState for this`SQLException`object. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!> | [iterator](../java/sql/SQLException.md))`()` <br /> Returns an iterator over the chained SQLExceptions. The iterator will be used to iterate over each SQLException and its underlying cause (if any). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextException](../java/sql/SQLException.md))`(`ex:` ` [SQLException](../java/sql/SQLException.md)!`)` <br /> Adds an`SQLException`object to the end of the chain. <br /> | ||
| From class [SQLWarning](../java/sql/SQLWarning.md) |-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLWarning](../java/sql/SQLWarning.md)! | [getNextWarning](../java/sql/SQLWarning.md))`()` <br /> Retrieves the warning chained to this`SQLWarning`object by`setNextWarning`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNextWarning](../java/sql/SQLWarning.md))`(`w:` ` [SQLWarning](../java/sql/SQLWarning.md)!`)` <br /> Adds a`SQLWarning`object to the end of the chain. <br /> | ||

## Public constructors

### DataTruncation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DataTruncation(
    index: Int, 
    parameter: Boolean, 
    read: Boolean, 
    dataSize: Int, 
    transferSize: Int)
```

Creates a`DataTruncation`object with the SQLState initialized to 01004 when`read`is set to`true`and 22001 when`read`is set to`false`, the reason set to "Data truncation", the vendor code set to 0, and the other fields set to the given values. The`cause`is not initialized, and may subsequently be initialized by a call to the [Throwable.initCause(java.lang.Throwable)](../java/lang/Throwable.md))method.

<br />

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the parameter or column value |
| `parameter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a parameter value was truncated |
| `read` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a read was truncated |
| --- | --- |
| `dataSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the original size of the data |
| `transferSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size after truncation |

### DataTruncation

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DataTruncation(
    index: Int, 
    parameter: Boolean, 
    read: Boolean, 
    dataSize: Int, 
    transferSize: Int, 
    cause: Throwable!)
```

Creates a`DataTruncation`object with the SQLState initialized to 01004 when`read`is set to`true`and 22001 when`read`is set to`false`, the reason set to "Data truncation", the vendor code set to 0, and the other fields set to the given values.

<br />

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the parameter or column value |
| `parameter` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a parameter value was truncated |
| `read` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a read was truncated |
| --- | --- |
| `dataSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the original size of the data |
| `transferSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the size after truncation |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the underlying reason for this`DataTruncation`(which is saved for later retrieval by the`getCause()`method); may be null indicating the cause is non-existent or unknown. |
| --- | --- |

## Public methods

### getDataSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDataSize(): Int
```

Gets the number of bytes of data that should have been transferred. This number may be approximate if data conversions were being performed. The value may be`-1`if the size is unknown.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes of data that should have been transferred |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIndex(): Int
```

Retrieves the index of the column or parameter that was truncated.

This may be -1 if the column or parameter index is unknown, in which case the`parameter`and`read`fields should be ignored.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the truncated paramter or column value |

### getParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParameter(): Boolean
```

Indicates whether the value truncated was a parameter value or a column value.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value truncated was a parameter;`false`if it was a column value |

### getRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRead(): Boolean
```

Indicates whether or not the value was truncated on a read.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the value was truncated when read from the database;`false`if the data was truncated on a write |

### getTransferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransferSize(): Int
```

Gets the number of bytes of data actually transferred. The value may be`-1`if the size is unknown.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes of data actually transferred |

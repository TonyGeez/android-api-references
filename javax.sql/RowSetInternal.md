# RowSetInternal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSetInternal

```
interface RowSetInternal
```

| [javax.sql.RowSetInternal](RowSetInternal.md) |

The interface that a`RowSet`object implements in order to present itself to a`RowSetReader`or`RowSetWriter`object. The`RowSetInternal`interface contains methods that let the reader or writer access and modify the internal state of the rowset.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Connection](../java.sql/Connection.md)! | [getConnection](RowSetInternal.md))`()` Retrieves the`Connection`object that was passed to this`RowSet`object. |
| abstract [ResultSet](../java.sql/ResultSet.md)! | [getOriginal](RowSetInternal.md))`()` Retrieves a`ResultSet`object containing the original value of this`RowSet`object. |
| abstract [ResultSet](../java.sql/ResultSet.md)! | [getOriginalRow](RowSetInternal.md))`()` Retrieves a`ResultSet`object containing the original value of the current row only. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getParams](RowSetInternal.md))`()` Retrieves the parameters that have been set for this`RowSet`object's command. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMetaData](RowSetInternal.md))`(`md:` ` [RowSetMetaData](RowSetMetaData.md)!`)` Sets the given`RowSetMetaData`object as the`RowSetMetaData`object for this`RowSet`object. |

## Public methods

### getConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnection(): Connection!
```

Retrieves the`Connection`object that was passed to this`RowSet`object.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Connection](../java.sql/Connection.md)! | the`Connection`object passed to the rowset or`null`if none was passed |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getOriginal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOriginal(): ResultSet!
```

Retrieves a`ResultSet`object containing the original value of this`RowSet`object.

The cursor is positioned before the first row in the result set. Only rows contained in the result set returned by the method`getOriginal`are said to have an original value.

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------|
| [ResultSet](../java.sql/ResultSet.md)! | the original value of the rowset |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getOriginalRow

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOriginalRow(): ResultSet!
```

Retrieves a`ResultSet`object containing the original value of the current row only. If the current row has no original value, an empty result set is returned. If there is no current row, an exception is thrown.

| Return ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ResultSet](../java.sql/ResultSet.md)! | the original value of the current row as a`ResultSet`object |

| Exceptions ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if a database access error occurs or this method is called while the cursor is on the insert row, before the first row, or after the last row |

### getParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getParams(): Array<Any!>!
```

Retrieves the parameters that have been set for this`RowSet`object's command.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | an array of the current parameter values for this`RowSet`object's command |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setMetaData(md: RowSetMetaData!): Unit
```

Sets the given`RowSetMetaData`object as the`RowSetMetaData`object for this`RowSet`object. The`RowSetReader`object associated with the rowset will use`RowSetMetaData`methods to set the values giving information about the rowset's columns.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `md` | [RowSetMetaData](RowSetMetaData.md)!:the`RowSetMetaData`object that will be set with information about the rowset's columns |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

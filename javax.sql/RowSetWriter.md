# RowSetWriter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSetWriter

```
interface RowSetWriter
```

| [javax.sql.RowSetWriter](https://developer.android.com/reference/kotlin/javax/sql/RowSetWriter#) |

An object that implements the`RowSetWriter`interface, called a*writer* . A writer may be registered with a`RowSet`object that supports the reader/writer paradigm.

If a disconnected`RowSet`object modifies some of its data, and it has a writer associated with it, it may be implemented so that it calls on the writer's`writeData`method internally to write the updates back to the data source. In order to do this, the writer must first establish a connection with the rowset's data source.

If the data to be updated has already been changed in the data source, there is a conflict, in which case the writer will not write the changes to the data source. The algorithm the writer uses for preventing or limiting conflicts depends entirely on its implementation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [writeData](https://developer.android.com/reference/kotlin/javax/sql/RowSetWriter#writeData(javax.sql.RowSetInternal))`(`caller:` ` [RowSetInternal](https://developer.android.com/reference/kotlin/javax/sql/RowSetInternal)!`)` Writes the changes in this`RowSetWriter`object's rowset back to the data source from which it got its data. |

## Public methods

### writeData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeData(caller: RowSetInternal!): Boolean
```

Writes the changes in this`RowSetWriter`object's rowset back to the data source from which it got its data.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [RowSetInternal](https://developer.android.com/reference/kotlin/javax/sql/RowSetInternal)!:the`RowSet`object (1) that has implemented the`RowSetInternal`interface, (2) with which this writer is registered, and (3) that called this method internally |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the modified data was written;`false`if not, which will be the case if there is a conflict |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

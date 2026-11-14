# RowId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowId

```
interface RowId
```

| [java.sql.RowId](https://developer.android.com/reference/kotlin/java/sql/RowId#) |

The representation (mapping) in the Java programming language of an SQL ROWID value. An SQL ROWID is a built-in type, a value of which can be thought of as an address for its identified row in a database table. Whether that address is logical or, in any respects, physical is determined by its originating data source.

Methods in the interfaces`ResultSet`,`CallableStatement`, and`PreparedStatement`, such as`getRowId`and`setRowId`allow a programmer to access a SQL`ROWID`value. The`RowId`interface provides a method for representing the value of the`ROWID`as a byte array or as a`String`.

The method`getRowIdLifetime`in the interface`DatabaseMetaData`, can be used to determine if a`RowId`object remains valid for the duration of the transaction in which the`RowId`was created, the duration of the session in which the`RowId`was created, or, effectively, for as long as its identified row is not deleted. In addition to specifying the duration of its valid lifetime outside its originating data source,`getRowIdLifetime`specifies the duration of a`ROWID`value's valid lifetime within its originating data source. In this, it differs from a large object, because there is no limit on the valid lifetime of a large object within its originating data source.

All methods on the`RowId`interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getBytes](https://developer.android.com/reference/kotlin/java/sql/RowId#getBytes())`()` Returns an array of bytes representing the value of the SQL`ROWID`designated by this`java.sql.RowId`object. |

## Public methods

### getBytes

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBytes(): ByteArray!
```

Returns an array of bytes representing the value of the SQL`ROWID`designated by this`java.sql.RowId`object.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | an array of bytes, whose length is determined by the driver supplying the connection, representing the value of the ROWID designated by this java.sql.RowId object. |

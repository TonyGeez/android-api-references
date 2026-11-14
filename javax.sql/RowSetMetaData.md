# RowSetMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RowSetMetaData

```
interface RowSetMetaData : ResultSetMetaData
```

| [javax.sql.RowSetMetaData](RowSetMetaData.md) |

An object that contains information about the columns in a`RowSet`object. This interface is an extension of the`ResultSetMetaData`interface with methods for setting the values in a`RowSetMetaData`object. When a`RowSetReader`object reads data into a`RowSet`object, it creates a`RowSetMetaData`object and initializes it using the methods in the`RowSetMetaData`interface. Then the reader passes the`RowSetMetaData`object to the rowset.

The methods in this interface are invoked internally when an application calls the method`RowSet.execute`; an application programmer would not use them directly.

## Summary

| Inherited constants ||
|---|---|
| From class [ResultSetMetaData](../java.sql/ResultSetMetaData.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNoNulls](../java.sql/ResultSetMetaData.md) <br /> The constant indicating that a column does not allow`NULL`values. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNullable](../java.sql/ResultSetMetaData.md) <br /> The constant indicating that a column allows`NULL`values. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNullableUnknown](../java.sql/ResultSetMetaData.md) <br /> The constant indicating that the nullability of a column's values is unknown. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoIncrement](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the designated column is automatically numbered, The default is for a`RowSet`object's columns not to be automatically numbered. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCaseSensitive](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the designated column is case sensitive. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCatalogName](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `catalogName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated column's table's catalog name, if any, to the given`String`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnCount](RowSetMetaData.md))`(`columnCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the number of columns in the`RowSet`object to the given number. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnDisplaySize](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated column's normal maximum width in chars to the given`int`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnLabel](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `label:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the suggested column title for use in printouts and displays, if any, to the given`String`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnName](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `columnName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of the designated column to the given`String`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnType](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `SQLType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated column's SQL type to the one given. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setColumnTypeName](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `typeName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated column's type name that is specific to the data source, if any, to the given`String`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the designated column is a cash value. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNullable](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets whether the designated column's value can be set to`NULL`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPrecision](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `precision:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated column's number of decimal digits to the given`int`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScale](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scale:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the designated column's number of digits to the right of the decimal point to the given`int`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSchemaName](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `schemaName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of the designated column's table's schema, if any, to the given`String`. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSearchable](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the designated column can be used in a where clause. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSigned](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `property:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the designated column is a signed number. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTableName](RowSetMetaData.md))`(`columnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the designated column's table name, if any, to the given`String`. |

| Inherited functions ||
|---|---|
| From class [ResultSetMetaData](../java.sql/ResultSetMetaData.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCatalogName](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the designated column's table's catalog name. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnClassName](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the fully-qualified name of the Java class whose instances are manufactured if the method`ResultSet.getObject`is called to retrieve a value from the column.`ResultSet.getObject`may return a subclass of the class returned by this method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](../java.sql/ResultSetMetaData.md))`()` <br /> Returns the number of columns in this`ResultSet`object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnDisplaySize](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates the designated column's normal maximum width in characters. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnLabel](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the designated column's suggested title for use in printouts and displays. The suggested title is usually specified by the SQL`AS`clause. If a SQL`AS`is not specified, the value returned from`getColumnLabel`will be the same as the value returned by the`getColumnName`method. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the designated column's name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnType](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the designated column's SQL type. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnTypeName](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Retrieves the designated column's database-specific type name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecision](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the designated column's specified column size. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. 0 is returned for data types where the column size is not applicable. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScale](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the designated column's number of digits to right of the decimal point. 0 is returned for data types where the scale is not applicable. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSchemaName](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the designated column's table's schema. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTableName](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the designated column's table name. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoIncrement](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether the designated column is automatically numbered. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCaseSensitive](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether a column's case matters. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCurrency](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether the designated column is a cash value. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefinitelyWritable](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether a write on the designated column will definitely succeed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [isNullable](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates the nullability of values in the designated column. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether the designated column is definitely not writable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSearchable](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether the designated column can be used in a where clause. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSigned](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether values in the designated column are signed numbers. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWritable](../java.sql/ResultSetMetaData.md))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Indicates whether it is possible for a write on the designated column to succeed. <br /> | ||
| From class [Wrapper](../java.sql/Wrapper.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](../java.sql/Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](../java.sql/Wrapper.md))`(`iface:` ` [Class](../java.lang/Class.md)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Public methods

### setAutoIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAutoIncrement(
    columnIndex: Int, 
    property: Boolean
): Unit
```

Sets whether the designated column is automatically numbered, The default is for a`RowSet`object's columns not to be automatically numbered.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `property` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the column is automatically numbered;`false`if it is not |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setCaseSensitive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCaseSensitive(
    columnIndex: Int, 
    property: Boolean
): Unit
```

Sets whether the designated column is case sensitive. The default is`false`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `property` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the column is case sensitive;`false`if it is not |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setCatalogName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCatalogName(
    columnIndex: Int, 
    catalogName: String!
): Unit
```

Sets the designated column's table's catalog name, if any, to the given`String`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `catalogName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the column's catalog name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setColumnCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setColumnCount(columnCount: Int): Unit
```

Sets the number of columns in the`RowSet`object to the given number.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `columnCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of columns in the`RowSet`object |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setColumnDisplaySize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setColumnDisplaySize(
    columnIndex: Int, 
    size: Int
): Unit
```

Sets the designated column's normal maximum width in chars to the given`int`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the normal maximum number of characters for the designated column |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setColumnLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setColumnLabel(
    columnIndex: Int, 
    label: String!
): Unit
```

Sets the suggested column title for use in printouts and displays, if any, to the given`String`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `label` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the column title |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setColumnName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setColumnName(
    columnIndex: Int, 
    columnName: String!
): Unit
```

Sets the name of the designated column to the given`String`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `columnName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the designated column's name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setColumnType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setColumnType(
    columnIndex: Int, 
    SQLType: Int
): Unit
```

Sets the designated column's SQL type to the one given.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `SQLType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the column's SQL type |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Types](../java.sql/Types.md) 

### setColumnTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setColumnTypeName(
    columnIndex: Int, 
    typeName: String!
): Unit
```

Sets the designated column's type name that is specific to the data source, if any, to the given`String`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `typeName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:data source specific type name. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCurrency(
    columnIndex: Int, 
    property: Boolean
): Unit
```

Sets whether the designated column is a cash value. The default is`false`.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `property` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the column is a cash value;`false`if it is not |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNullable(
    columnIndex: Int, 
    property: Int
): Unit
```

Sets whether the designated column's value can be set to`NULL`. The default is`ResultSetMetaData.columnNullableUnknown`

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `property` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the following constants:`ResultSetMetaData.columnNoNulls`,`ResultSetMetaData.columnNullable`, or`ResultSetMetaData.columnNullableUnknown` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPrecision(
    columnIndex: Int, 
    precision: Int
): Unit
```

Sets the designated column's number of decimal digits to the given`int`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `precision` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the total number of decimal digits |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setScale(
    columnIndex: Int, 
    scale: Int
): Unit
```

Sets the designated column's number of digits to the right of the decimal point to the given`int`.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `scale` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of digits to right of decimal point |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setSchemaName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSchemaName(
    columnIndex: Int, 
    schemaName: String!
): Unit
```

Sets the name of the designated column's table's schema, if any, to the given`String`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `schemaName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the schema name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setSearchable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSearchable(
    columnIndex: Int, 
    property: Boolean
): Unit
```

Sets whether the designated column can be used in a where clause. The default is`false`.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `property` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the column can be used in a`WHERE`clause;`false`if it cannot |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setSigned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSigned(
    columnIndex: Int, 
    property: Boolean
): Unit
```

Sets whether the designated column is a signed number. The default is`false`.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `property` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the column is a signed number;`false`if it is not |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### setTableName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTableName(
    columnIndex: Int, 
    tableName: String!
): Unit
```

Sets the designated column's table name, if any, to the given`String`.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------|
| `columnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |
| `tableName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the column's table name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

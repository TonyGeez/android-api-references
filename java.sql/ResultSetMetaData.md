# ResultSetMetaData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResultSetMetaData

```
interface ResultSetMetaData : Wrapper
```

| [java.sql.ResultSetMetaData](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#) |

| Known Direct Subclasses [RowSetMetaData](https://developer.android.com/reference/kotlin/javax/sql/RowSetMetaData.html#) |-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------| | [RowSetMetaData](https://developer.android.com/reference/kotlin/javax/sql/RowSetMetaData.html#) | An object that contains information about the columns in a`RowSet`object. | |
| --- | --- | --- | --- | --- | --- | --- |

An object that can be used to get information about the types and properties of the columns in a`ResultSet`object. The following code fragment creates the`ResultSet`object rs, creates the`ResultSetMetaData`object rsmd, and uses rsmd to find out how many columns rs has and whether the first column in rs can be used in a`WHERE`clause. 

```kotlin
ResultSet rs = stmt.executeQuery("SELECT a, b, c FROM TABLE2");
      ResultSetMetaData rsmd = rs.getMetaData();
      int numberOfColumns = rsmd.getColumnCount();
      boolean b = rsmd.isSearchable(1);
 
  
```

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNoNulls](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#columnNoNulls:kotlin.Int) The constant indicating that a column does not allow`NULL`values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNullable](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#columnNullable:kotlin.Int) The constant indicating that a column allows`NULL`values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [columnNullableUnknown](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#columnNullableUnknown:kotlin.Int) The constant indicating that the nullability of a column's values is unknown. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCatalogName](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getCatalogName(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the designated column's table's catalog name. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnClassName](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnClassName(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the fully-qualified name of the Java class whose instances are manufactured if the method`ResultSet.getObject`is called to retrieve a value from the column. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnCount](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnCount())`()` Returns the number of columns in this`ResultSet`object. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnDisplaySize](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnDisplaySize(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the designated column's normal maximum width in characters. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnLabel](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnLabel(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the designated column's suggested title for use in printouts and displays. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnName](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnName(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the designated column's name. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnType](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnType(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated column's SQL type. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getColumnTypeName](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getColumnTypeName(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the designated column's database-specific type name. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrecision](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getPrecision(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the designated column's specified column size. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScale](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getScale(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the designated column's number of digits to right of the decimal point. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSchemaName](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getSchemaName(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the designated column's table's schema. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTableName](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#getTableName(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the designated column's table name. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAutoIncrement](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isAutoIncrement(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the designated column is automatically numbered. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCaseSensitive](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isCaseSensitive(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether a column's case matters. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCurrency](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isCurrency(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the designated column is a cash value. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefinitelyWritable](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isDefinitelyWritable(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether a write on the designated column will definitely succeed. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [isNullable](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isNullable(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates the nullability of values in the designated column. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadOnly](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isReadOnly(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the designated column is definitely not writable. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSearchable](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isSearchable(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether the designated column can be used in a where clause. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSigned](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isSigned(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether values in the designated column are signed numbers. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWritable](https://developer.android.com/reference/kotlin/java/sql/ResultSetMetaData#isWritable(kotlin.Int))`(`column:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates whether it is possible for a write on the designated column to succeed. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Wrapper](https://developer.android.com/reference/kotlin/java/sql/Wrapper) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWrapperFor](https://developer.android.com/reference/kotlin/java/sql/Wrapper#isWrapperFor(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> Returns true if this either implements the interface argument or is directly or indirectly a wrapper for an object that does. Returns false otherwise. If this implements the interface then return true, else if this is a wrapper then return the result of recursively calling`isWrapperFor`on the wrapped object. If this does not implement the interface and is not a wrapper, return false. This method should be implemented as a low-cost operation compared to`unwrap`so that callers can use this method to avoid expensive`unwrap`calls that may fail. If this method returns true then calling`unwrap`with the same argument should succeed. <br /> | | T | [unwrap](https://developer.android.com/reference/kotlin/java/sql/Wrapper#unwrap(java.lang.Class))`(`iface:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> Returns an object that implements the given interface to allow access to non-standard methods, or standard methods not exposed by the proxy. If the receiver implements the interface then the result is the receiver or a proxy for the receiver. If the receiver is a wrapper and the wrapped object implements the interface then the result is the wrapped object or a proxy for the wrapped object. Otherwise return the the result of calling`unwrap`recursively on the wrapped object or a proxy for that result. If the receiver is not a wrapper and does not implement the interface, then an`SQLException`is thrown. <br /> | ||

## Constants

### columnNoNulls

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val columnNoNulls: Int
```

The constant indicating that a column does not allow`NULL`values. 

 Value: 0

### columnNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val columnNullable: Int
```

The constant indicating that a column allows`NULL`values. 

 Value: 1

### columnNullableUnknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val columnNullableUnknown: Int
```

The constant indicating that the nullability of a column's values is unknown. 

 Value: 2

## Public methods

### getCatalogName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCatalogName(column: Int): String!
```

Gets the designated column's table's catalog name.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the catalog for the table in which the given column appears or "" if not applicable |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getColumnClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnClassName(column: Int): String!
```

Returns the fully-qualified name of the Java class whose instances are manufactured if the method`ResultSet.getObject`is called to retrieve a value from the column.`ResultSet.getObject`may return a subclass of the class returned by this method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the fully-qualified name of the class in the Java programming language that would be used by the method`ResultSet.getObject`to retrieve the value in the specified column. This is the class name used for custom mapping. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getColumnCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnCount(): Int
```

Returns the number of columns in this`ResultSet`object.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of columns |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getColumnDisplaySize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnDisplaySize(column: Int): Int
```

Indicates the designated column's normal maximum width in characters.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the normal maximum number of characters allowed as the width of the designated column |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getColumnLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnLabel(column: Int): String!
```

Gets the designated column's suggested title for use in printouts and displays. The suggested title is usually specified by the SQL`AS`clause. If a SQL`AS`is not specified, the value returned from`getColumnLabel`will be the same as the value returned by the`getColumnName`method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the suggested column title |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getColumnName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnName(column: Int): String!
```

Get the designated column's name.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | column name |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getColumnType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnType(column: Int): Int
```

Retrieves the designated column's SQL type.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | SQL type from java.sql.Types |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

**See Also**

- [java.sql.Types](https://developer.android.com/reference/kotlin/java/sql/Types) 

### getColumnTypeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnTypeName(column: Int): String!
```

Retrieves the designated column's database-specific type name.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | type name used by the database. If the column type is a user-defined type, then a fully-qualified type name is returned. |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getPrecision

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrecision(column: Int): Int
```

Get the designated column's specified column size. For numeric data, this is the maximum precision. For character data, this is the length in characters. For datetime datatypes, this is the length in characters of the String representation (assuming the maximum allowed precision of the fractional seconds component). For binary data, this is the length in bytes. For the ROWID datatype, this is the length in bytes. 0 is returned for data types where the column size is not applicable.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | precision |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getScale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getScale(column: Int): Int
```

Gets the designated column's number of digits to right of the decimal point. 0 is returned for data types where the scale is not applicable.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|-------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | scale |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getSchemaName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSchemaName(column: Int): String!
```

Get the designated column's table's schema.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | schema name or "" if not applicable |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### getTableName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTableName(column: Int): String!
```

Gets the designated column's table name.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | table name or "" if not applicable |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isAutoIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isAutoIncrement(column: Int): Boolean
```

Indicates whether the designated column is automatically numbered.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isCaseSensitive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCaseSensitive(column: Int): Boolean
```

Indicates whether a column's case matters.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCurrency(column: Int): Boolean
```

Indicates whether the designated column is a cash value.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isDefinitelyWritable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDefinitelyWritable(column: Int): Boolean
```

Indicates whether a write on the designated column will definitely succeed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isNullable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNullable(column: Int): Int
```

Indicates the nullability of values in the designated column.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the nullability status of the given column; one of`columnNoNulls`,`columnNullable`or`columnNullableUnknown` |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReadOnly(column: Int): Boolean
```

Indicates whether the designated column is definitely not writable.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isSearchable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSearchable(column: Int): Boolean
```

Indicates whether the designated column can be used in a where clause.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isSigned

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSigned(column: Int): Boolean
```

Indicates whether values in the designated column are signed numbers.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

### isWritable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isWritable(column: Int): Boolean
```

Indicates whether it is possible for a write on the designated column to succeed.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `column` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first column is 1, the second is 2, ... |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if so;`false`otherwise |

| Exceptions ||
|-------------------------|-----------------------------------|
| `java.sql.SQLException` | if a database access error occurs |

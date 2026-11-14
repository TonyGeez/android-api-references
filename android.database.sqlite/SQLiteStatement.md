# SQLiteStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteStatement

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteStatement "View this page in Java") 
| --- | --- |

```
class SQLiteStatement : SQLiteProgram
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) |||
| | ↳ | [android.database.sqlite.SQLiteProgram](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram) ||
| | | ↳ | [android.database.sqlite.SQLiteStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#) |
| --- | --- | --- | --- |

Represents a statement that can be executed against a database. The statement cannot return multiple rows or columns, but single value (1 x 1) result sets are supported.

This class is not thread-safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#execute())`()` Execute this SQL statement, if it is not a SELECT / INSERT / DELETE / UPDATE, for example CREATE / DROP table, view, trigger, index etc. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [executeInsert](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#executeInsert())`()` Execute this SQL statement and return the ID of the row inserted due to this call. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdateDelete](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#executeUpdateDelete())`()` Execute this SQL statement, if the number of rows affected by execution of this SQL statement is of any importance to the caller - for example, UPDATE / DELETE SQL statements. |
| --- | --- |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | [simpleQueryForBlobFileDescriptor](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#simpleQueryForBlobFileDescriptor())`()` Executes a statement that returns a 1 by 1 table with a blob value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [simpleQueryForLong](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#simpleQueryForLong())`()` Execute a statement that returns a 1 by 1 table with a numeric value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [simpleQueryForString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#simpleQueryForString())`()` Execute a statement that returns a 1 by 1 table with a text value. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement#toString())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#acquireReference())`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#close())`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleasedFromContainer())`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference())`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer())`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||
| From class [SQLiteProgram](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllArgsAsStrings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindAllArgsAsStrings(kotlin.Array))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Given an array of String bindArgs, this method binds all of them in one single call. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindBlob](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindBlob(kotlin.Int,%20kotlin.ByteArray))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Bind a byte array value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindDouble](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindDouble(kotlin.Int,%20kotlin.Double))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Bind a double value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindLong](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindLong(kotlin.Int,%20kotlin.Long))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Bind a long value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called. addToBindArgs <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindNull](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindNull(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Bind a NULL value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindString(kotlin.Int,%20kotlin.String))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Bind a String value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())`()` <br /> Clears all existing bindings. Unset bindings are treated as NULL. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#getUniqueId())`()` <br /> Unimplemented. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#onAllReferencesReleased())`()` <br /> | ||

## Public methods

### execute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun execute(): Unit
```

Execute this SQL statement, if it is not a SELECT / INSERT / DELETE / UPDATE, for example CREATE / DROP table, view, trigger, index etc.

| Exceptions ||
|---------------------------------|----------------------------------------------|
| `android.database.SQLException` | If the SQL string is invalid for some reason |

### executeInsert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun executeInsert(): Long
```

Execute this SQL statement and return the ID of the row inserted due to this call. The SQL statement should be an INSERT for this to be a useful call.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the row ID of the last row inserted, if this insert is successful. -1 otherwise. |

| Exceptions ||
|---------------------------------|----------------------------------------------|
| `android.database.SQLException` | If the SQL string is invalid for some reason |

### executeUpdateDelete

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun executeUpdateDelete(): Int
```

Execute this SQL statement, if the number of rows affected by execution of this SQL statement is of any importance to the caller - for example, UPDATE / DELETE SQL statements.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of rows affected by this SQL statement execution. |

| Exceptions ||
|---------------------------------|----------------------------------------------|
| `android.database.SQLException` | If the SQL string is invalid for some reason |

### simpleQueryForBlobFileDescriptor

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun simpleQueryForBlobFileDescriptor(): ParcelFileDescriptor!
```

Executes a statement that returns a 1 by 1 table with a blob value.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | A read-only file descriptor for a copy of the blob value, or`null`if the value is null or could not be read for some reason. |

| Exceptions ||
|-----------------------------------------------|--------------------------------|
| `android.database.sqlite.SQLiteDoneException` | if the query returns zero rows |

### simpleQueryForLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun simpleQueryForLong(): Long
```

Execute a statement that returns a 1 by 1 table with a numeric value. For example, SELECT COUNT(\*) FROM table;

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The result of the query. |

| Exceptions ||
|-----------------------------------------------|--------------------------------|
| `android.database.sqlite.SQLiteDoneException` | if the query returns zero rows |

### simpleQueryForString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun simpleQueryForString(): String!
```

Execute a statement that returns a 1 by 1 table with a text value. For example, SELECT COUNT(\*) FROM table;

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The result of the query. |

| Exceptions ||
|-----------------------------------------------|--------------------------------|
| `android.database.sqlite.SQLiteDoneException` | if the query returns zero rows |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

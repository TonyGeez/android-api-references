# SQLiteStatement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteStatement

Kotlin| [Java](SQLiteStatement.md) 
| --- | --- |

```
class SQLiteStatement : SQLiteProgram
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](SQLiteClosable.md) |||
| | ↳ | [android.database.sqlite.SQLiteProgram](SQLiteProgram.md) ||
| | | ↳ | [android.database.sqlite.SQLiteStatement](SQLiteStatement.md) |
| --- | --- | --- | --- |

Represents a statement that can be executed against a database. The statement cannot return multiple rows or columns, but single value (1 x 1) result sets are supported.

This class is not thread-safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [execute](SQLiteStatement.md))`()` Execute this SQL statement, if it is not a SELECT / INSERT / DELETE / UPDATE, for example CREATE / DROP table, view, trigger, index etc. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [executeInsert](SQLiteStatement.md))`()` Execute this SQL statement and return the ID of the row inserted due to this call. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [executeUpdateDelete](SQLiteStatement.md))`()` Execute this SQL statement, if the number of rows affected by execution of this SQL statement is of any importance to the caller - for example, UPDATE / DELETE SQL statements. |
| --- | --- |
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | [simpleQueryForBlobFileDescriptor](SQLiteStatement.md))`()` Executes a statement that returns a 1 by 1 table with a blob value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [simpleQueryForLong](SQLiteStatement.md))`()` Execute a statement that returns a 1 by 1 table with a numeric value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [simpleQueryForString](SQLiteStatement.md))`()` Execute a statement that returns a 1 by 1 table with a text value. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SQLiteStatement.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](SQLiteClosable.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](SQLiteClosable.md))`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](SQLiteClosable.md))`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](SQLiteClosable.md))`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||
| From class [SQLiteProgram](SQLiteProgram.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllArgsAsStrings](SQLiteProgram.md))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Given an array of String bindArgs, this method binds all of them in one single call. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindBlob](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Bind a byte array value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindDouble](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Bind a double value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindLong](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Bind a long value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. addToBindArgs <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindNull](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Bind a NULL value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindString](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Bind a String value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBindings](SQLiteProgram.md))`()` <br /> Clears all existing bindings. Unset bindings are treated as NULL. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](SQLiteProgram.md))`()` <br /> Unimplemented. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](SQLiteProgram.md))`()` <br /> | ||

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
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | A read-only file descriptor for a copy of the blob value, or`null`if the value is null or could not be read for some reason. |

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

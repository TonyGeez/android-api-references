# SQLiteQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteQuery

Kotlin| [Java](../android/database/sqlite/SQLiteQuery.md) 
| --- | --- |

```
class SQLiteQuery : SQLiteProgram
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) |||
| | ↳ | [android.database.sqlite.SQLiteProgram](../android/database/sqlite/SQLiteProgram.md) ||
| | | ↳ | [android.database.sqlite.SQLiteQuery](../android/database/sqlite/SQLiteQuery.md) |
| --- | --- | --- | --- |

Represents a query that reads the resulting rows into a [SQLiteQuery](../android/database/sqlite/SQLiteQuery.md). This class is used by [SQLiteCursor](../android/database/sqlite/SQLiteCursor.md) and isn't useful itself.

This class is not thread-safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/database/sqlite/SQLiteQuery.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](../android/database/sqlite/SQLiteClosable.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](../android/database/sqlite/SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](../android/database/sqlite/SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](../android/database/sqlite/SQLiteClosable.md))`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||
| From class [SQLiteProgram](../android/database/sqlite/SQLiteProgram.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllArgsAsStrings](../android/database/sqlite/SQLiteProgram.md))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Given an array of String bindArgs, this method binds all of them in one single call. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindBlob](../android/database/sqlite/SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Bind a byte array value to this statement. The value remains bound until [clearBindings](../android/database/sqlite/SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindDouble](../android/database/sqlite/SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Bind a double value to this statement. The value remains bound until [clearBindings](../android/database/sqlite/SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindLong](../android/database/sqlite/SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Bind a long value to this statement. The value remains bound until [clearBindings](../android/database/sqlite/SQLiteProgram.md))is called. addToBindArgs <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindNull](../android/database/sqlite/SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Bind a NULL value to this statement. The value remains bound until [clearBindings](../android/database/sqlite/SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindString](../android/database/sqlite/SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Bind a String value to this statement. The value remains bound until [clearBindings](../android/database/sqlite/SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBindings](../android/database/sqlite/SQLiteProgram.md))`()` <br /> Clears all existing bindings. Unset bindings are treated as NULL. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](../android/database/sqlite/SQLiteProgram.md))`()` <br /> Unimplemented. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](../android/database/sqlite/SQLiteProgram.md))`()` <br /> | ||

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

# SQLiteQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteQuery

Kotlin| [Java](SQLiteQuery.md) 
| --- | --- |

```
class SQLiteQuery : SQLiteProgram
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](SQLiteClosable.md) |||
| | ↳ | [android.database.sqlite.SQLiteProgram](SQLiteProgram.md) ||
| | | ↳ | [android.database.sqlite.SQLiteQuery](SQLiteQuery.md) |
| --- | --- | --- | --- |

Represents a query that reads the resulting rows into a [SQLiteQuery](SQLiteQuery.md). This class is used by [SQLiteCursor](SQLiteCursor.md) and isn't useful itself.

This class is not thread-safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SQLiteQuery.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](SQLiteClosable.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](SQLiteClosable.md))`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](SQLiteClosable.md))`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](SQLiteClosable.md))`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||
| From class [SQLiteProgram](SQLiteProgram.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllArgsAsStrings](SQLiteProgram.md))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Given an array of String bindArgs, this method binds all of them in one single call. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindBlob](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Bind a byte array value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindDouble](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Bind a double value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindLong](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Bind a long value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. addToBindArgs <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindNull](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Bind a NULL value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindString](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Bind a String value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBindings](SQLiteProgram.md))`()` <br /> Clears all existing bindings. Unset bindings are treated as NULL. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](SQLiteProgram.md))`()` <br /> Unimplemented. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](SQLiteProgram.md))`()` <br /> | ||

## Public methods

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

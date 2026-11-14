# SQLiteProgram

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteProgram

Kotlin| [Java](SQLiteProgram.md) 
| --- | --- |

```
abstract class SQLiteProgram : SQLiteClosable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.sqlite.SQLiteClosable](SQLiteClosable.md) ||
| | ↳ | [android.database.sqlite.SQLiteProgram](SQLiteProgram.md) |

| Known Direct Subclasses [SQLiteQuery](SQLiteQuery.md), [SQLiteStatement](SQLiteStatement.md) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteQuery](SQLiteQuery.md) | Represents a query that reads the resulting rows into a [SQLiteQuery](SQLiteQuery.md). | | [SQLiteStatement](SQLiteStatement.md) | Represents a statement that can be executed against a database. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base class for compiled SQLite programs.

This class is not thread-safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllArgsAsStrings](SQLiteProgram.md))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Given an array of String bindArgs, this method binds all of them in one single call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindBlob](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Bind a byte array value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindDouble](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Bind a double value to this statement. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindLong](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Bind a long value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindNull](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Bind a NULL value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindString](SQLiteProgram.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Bind a String value to this statement. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBindings](SQLiteProgram.md))`()` Clears all existing bindings. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](SQLiteProgram.md))`()` Unimplemented. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](SQLiteProgram.md))`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](SQLiteClosable.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](SQLiteClosable.md))`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](SQLiteClosable.md))`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](SQLiteClosable.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](SQLiteClosable.md))`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](SQLiteClosable.md))`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||

## Public methods

### bindAllArgsAsStrings

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindAllArgsAsStrings(bindArgs: Array<String!>!): Unit
```

Given an array of String bindArgs, this method binds all of them in one single call.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bindArgs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the String array of bind args, none of which must be null. |

### bindBlob

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindBlob(
    index: Int, 
    value: ByteArray!
): Unit
```

Bind a byte array value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The 1-based index to the parameter to bind |
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:The value to bind, must not be null |

### bindDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindDouble(
    index: Int, 
    value: Double
): Unit
```

Bind a double value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The 1-based index to the parameter to bind |
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The value to bind |

### bindLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindLong(
    index: Int, 
    value: Long
): Unit
```

Bind a long value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called. addToBindArgs

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The 1-based index to the parameter to bind |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The value to bind |

### bindNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindNull(index: Int): Unit
```

Bind a NULL value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The 1-based index to the parameter to bind null to |

### bindString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindString(
    index: Int, 
    value: String!
): Unit
```

Bind a String value to this statement. The value remains bound until [clearBindings](SQLiteProgram.md))is called.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The 1-based index to the parameter to bind |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value to bind, must not be null |

### clearBindings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearBindings(): Unit
```

Clears all existing bindings. Unset bindings are treated as NULL. 

### getUniqueId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUniqueId(): Int
```

**Deprecated:** *This method is deprecated and must not be used.*

Unimplemented.

## Protected methods

### onAllReferencesReleased

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAllReferencesReleased(): Unit
```

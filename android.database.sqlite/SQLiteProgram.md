# SQLiteProgram

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLiteProgram

Kotlin| [Java](https://developer.android.com/reference/android/database/sqlite/SQLiteProgram "View this page in Java") 

```
abstract class SQLiteProgram : SQLiteClosable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.database.sqlite.SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) ||
| | ↳ | [android.database.sqlite.SQLiteProgram](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#) |

| Known Direct Subclasses [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery), [SQLiteStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------| | [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery) | Represents a query that reads the resulting rows into a [SQLiteQuery](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteQuery). | | [SQLiteStatement](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteStatement) | Represents a statement that can be executed against a database. | |

A base class for compiled SQLite programs.

This class is not thread-safe.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindAllArgsAsStrings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindAllArgsAsStrings(kotlin.Array))`(`bindArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Given an array of String bindArgs, this method binds all of them in one single call. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindBlob](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindBlob(kotlin.Int,%20kotlin.ByteArray))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Bind a byte array value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindDouble](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindDouble(kotlin.Int,%20kotlin.Double))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Bind a double value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindLong](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindLong(kotlin.Int,%20kotlin.Long))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Bind a long value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindNull](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindNull(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Bind a NULL value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindString](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#bindString(kotlin.Int,%20kotlin.String))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Bind a String value to this statement. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())`()` Clears all existing bindings. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUniqueId](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#getUniqueId())`()` Unimplemented. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleased](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#onAllReferencesReleased())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [SQLiteClosable](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#acquireReference())`()` <br /> Acquires a reference to the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#close())`()` <br /> Releases a reference to the object, closing the object if the last reference was released. Calling this method is equivalent to calling [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAllReferencesReleasedFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#onAllReferencesReleasedFromContainer())`()` <br /> Called when the last reference to the object was released by a call to [releaseReferenceFromContainer()](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReference](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReference())`()` <br /> Releases a reference to the object, closing the object if the last reference was released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseReferenceFromContainer](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteClosable#releaseReferenceFromContainer())`()` <br /> Releases a reference to the object that was owned by the container of the object, closing the object if the last reference was released. <br /> | ||

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

Bind a byte array value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called.

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

Bind a double value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called.

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

Bind a long value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called. addToBindArgs

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The 1-based index to the parameter to bind |
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The value to bind |

### bindNull

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bindNull(index: Int): Unit
```

Bind a NULL value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called.

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

Bind a String value to this statement. The value remains bound until [clearBindings](https://developer.android.com/reference/kotlin/android/database/sqlite/SQLiteProgram#clearBindings())is called.

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

# CursorJoiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorJoiner

Kotlin| [Java](CursorJoiner.md) 
| --- | --- |

```
class CursorJoiner : MutableIterable<CursorJoiner.Result!>, MutableIterator<CursorJoiner.Result!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.database.CursorJoiner](CursorJoiner.md) |

Does a join on two cursors using the specified columns. The cursors must already be sorted on each of the specified columns in ascending order. This joiner only supports the case where the tuple of key column values is unique.

Typical usage: 

```kotlin
CursorJoiner joiner = new CursorJoiner(cursorA, keyColumnsofA, cursorB, keyColumnsofB);
  for (CursorJoiner.Result joinerResult : joiner) {
      switch (joinerResult) {
          case LEFT:
              // handle case where a row in cursorA is unique
              break;
          case RIGHT:
              // handle case where a row in cursorB is unique
              break;
          case BOTH:
              // handle case where a row with the same key is in both cursors
              break;
      }
  }
  
```

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------|
| | [Result](../android/database/CursorJoiner.Result.md) The result of a call to next(). |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CursorJoiner](CursorJoiner.md))`(`cursorLeft:` ` [Cursor](Cursor.md)!`, `columnNamesLeft:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `cursorRight:` ` [Cursor](Cursor.md)!`, `columnNamesRight:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Initializes the CursorJoiner and resets the cursors to the first row. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNext](CursorJoiner.md))`()` Returns whether or not there are more rows to compare using next(). |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [CursorJoiner.Result](../android/database/CursorJoiner.Result.md)!\> | [iterator](CursorJoiner.md))`()` <br /> |
| [CursorJoiner.Result](../android/database/CursorJoiner.Result.md)! | [next](CursorJoiner.md))`()` Returns the comparison result of the next row from each cursor. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](CursorJoiner.md))`()` <br /> |

## Public constructors

### CursorJoiner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CursorJoiner(
    cursorLeft: Cursor!, 
    columnNamesLeft: Array<String!>!, 
    cursorRight: Cursor!, 
    columnNamesRight: Array<String!>!)
```

Initializes the CursorJoiner and resets the cursors to the first row. The left and right column name arrays must have the same number of columns.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursorLeft` | [Cursor](Cursor.md)!:The left cursor to compare |
| `columnNamesLeft` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The column names to compare from the left cursor |
| `cursorRight` | [Cursor](Cursor.md)!:The right cursor to compare |
| --- | --- |
| `columnNamesRight` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The column names to compare from the right cursor |

## Public methods

### hasNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasNext(): Boolean
```

Returns whether or not there are more rows to compare using next().

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there are more rows to compare |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun iterator(): MutableIterator<CursorJoiner.Result!>
```

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [CursorJoiner.Result](../android/database/CursorJoiner.Result.md)!> | an Iterator. |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun next(): CursorJoiner.Result!
```

Returns the comparison result of the next row from each cursor. If one cursor has no more rows but the other does then subsequent calls to this will indicate that the remaining rows are unique.

The caller must check that hasNext() returns true before calling this.

Once next() has been called the cursors specified in the result of the call to next() are guaranteed to point to the row that was indicated. Reading values from the cursor that was not indicated in the call to next() will result in undefined behavior.

| Return ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CursorJoiner.Result](../android/database/CursorJoiner.Result.md)! | LEFT, if the row pointed to by the left cursor is unique, RIGHT if the row pointed to by the right cursor is unique, BOTH if the rows in both cursors are the same. |

| Exceptions ||
|------------------------------------|---------------------------------------|
| `java.util.NoSuchElementException` | if the iteration has no more elements |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun remove(): Unit
```

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this iterator |
| `java.lang.IllegalStateException` | if the`next`method has not yet been called, or the`remove`method has already been called after the last call to the`next`method |

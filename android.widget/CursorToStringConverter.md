# SimpleCursorAdapter.CursorToStringConverter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorToStringConverter

Kotlin| [Java](https://developer.android.com/reference/android/widget/SimpleCursorAdapter.CursorToStringConverter "View this page in Java") 
| --- | --- |

```
interface CursorToStringConverter
```

| [android.widget.SimpleCursorAdapter.CursorToStringConverter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter#) |

This class can be used by external clients of SimpleCursorAdapter to define how the Cursor should be converted to a String.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter.CursorToStringConverter#convertToString(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Returns a CharSequence representing the specified Cursor. |

## Public methods

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun convertToString(cursor: Cursor!): CharSequence!
```

Returns a CharSequence representing the specified Cursor.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:the cursor for which a CharSequence representation is requested |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a non-null CharSequence representing the cursor |

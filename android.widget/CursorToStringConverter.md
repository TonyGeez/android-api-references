# SimpleCursorAdapter.CursorToStringConverter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorToStringConverter

Kotlin| [Java](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md) 
| --- | --- |

```
interface CursorToStringConverter
```

| [android.widget.SimpleCursorAdapter.CursorToStringConverter](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md) |

This class can be used by external clients of SimpleCursorAdapter to define how the Cursor should be converted to a String.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [convertToString](../android/widget/SimpleCursorAdapter.CursorToStringConverter.md))`(`cursor:` ` [Cursor](../android/database/Cursor.md)!`)` Returns a CharSequence representing the specified Cursor. |

## Public methods

### convertToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun convertToString(cursor: Cursor!): CharSequence!
```

Returns a CharSequence representing the specified Cursor.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](../android/database/Cursor.md)!:the cursor for which a CharSequence representation is requested |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | a non-null CharSequence representing the cursor |

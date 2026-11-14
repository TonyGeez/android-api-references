# NumberPicker.Formatter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Formatter

Kotlin| [Java](../android/widget/NumberPicker.Formatter.md) 
| --- | --- |

```
interface Formatter
```

| [android.widget.NumberPicker.Formatter](../android/widget/NumberPicker.Formatter.md) |

Interface used to format current value into a string for presentation.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/widget/NumberPicker.Formatter.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a string representation of the current value. |

## Public methods

### format

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(value: Int): String!
```

Formats a string representation of the current value.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The currently selected value. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A formatted string representation. |

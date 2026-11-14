# TabStopSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TabStopSpan

Kotlin| [Java](../android/text/style/TabStopSpan.md) 
| --- | --- |

```
interface TabStopSpan : ParagraphStyle
```

| [android.text.style.TabStopSpan](../android/text/style/TabStopSpan.md) |

| Known Direct Subclasses [TabStopSpan.Standard](../android/text/style/TabStopSpan.Standard.md) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------| | [TabStopSpan.Standard](../android/text/style/TabStopSpan.Standard.md) | The default implementation of TabStopSpan that allows setting the offset of the tab stop from the leading margin of the first line of text. | |
| --- | --- | --- | --- | --- | --- | --- |

Paragraph affecting span that changes the position of the tab with respect to the leading margin of the line.`TabStopSpan`will only affect the first tab encountered on the first line of the text.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](../android/text/style/TabStopSpan.Standard.md) The default implementation of TabStopSpan that allows setting the offset of the tab stop from the leading margin of the first line of text. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTabStop](../android/text/style/TabStopSpan.md))`()` Returns the offset of the tab stop from the leading margin of the line, in pixels. |

## Public methods

### getTabStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTabStop(): Int
```

Returns the offset of the tab stop from the leading margin of the line, in pixels.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset, in pixels |

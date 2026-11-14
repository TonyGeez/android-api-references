# TabStopSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TabStopSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/TabStopSpan "View this page in Java") 

```
interface TabStopSpan : ParagraphStyle
```

| [android.text.style.TabStopSpan](https://developer.android.com/reference/kotlin/android/text/style/TabStopSpan#) |

| Known Direct Subclasses [TabStopSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/TabStopSpan.Standard) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------| | [TabStopSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/TabStopSpan.Standard) | The default implementation of TabStopSpan that allows setting the offset of the tab stop from the leading margin of the first line of text. | |

Paragraph affecting span that changes the position of the tab with respect to the leading margin of the line.`TabStopSpan`will only affect the first tab encountered on the first line of the text.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](https://developer.android.com/reference/kotlin/android/text/style/TabStopSpan.Standard) The default implementation of TabStopSpan that allows setting the offset of the tab stop from the leading margin of the first line of text. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTabStop](https://developer.android.com/reference/kotlin/android/text/style/TabStopSpan#getTabStop())`()` Returns the offset of the tab stop from the leading margin of the line, in pixels. |

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

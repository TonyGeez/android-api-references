# Filter.FilterListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/Filter.FilterListener "View this page in Java") 

```
interface FilterListener
```

| [android.widget.Filter.FilterListener](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterListener#) |

| Known Direct Subclasses [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView), [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView) |------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [AbsListView](https://developer.android.com/reference/kotlin/android/widget/AbsListView) | Base class that can be used to implement virtualized lists of items. | | [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView) | An editable text view that shows completion suggestions automatically while the user is typing. | |

| Known Indirect Subclasses [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView), [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView), [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView), [MultiAutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) | A view that shows items in a vertically scrolling two-level list. | | [GridView](https://developer.android.com/reference/kotlin/android/widget/GridView) | A view that shows items in two-dimensional scrolling grid. | | [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MultiAutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/MultiAutoCompleteTextView) | An editable text view, extending [AutoCompleteTextView](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView), that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing. | |

Listener used to receive a notification upon completion of a filtering operation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFilterComplete](https://developer.android.com/reference/kotlin/android/widget/Filter.FilterListener#onFilterComplete(kotlin.Int))`(`count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies the end of a filtering operation. |

## Public methods

### onFilterComplete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFilterComplete(count: Int): Unit
```

Notifies the end of a filtering operation.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of values computed by the filter |

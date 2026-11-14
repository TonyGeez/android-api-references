# Filter.FilterListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilterListener

Kotlin| [Java](../android/widget/Filter.FilterListener.md) 
| --- | --- |

```
interface FilterListener
```

| [android.widget.Filter.FilterListener](../android/widget/Filter.FilterListener.md) |

| Known Direct Subclasses [AbsListView](AbsListView.md), [AutoCompleteTextView](AutoCompleteTextView.md) |------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [AbsListView](AbsListView.md) | Base class that can be used to implement virtualized lists of items. | | [AutoCompleteTextView](AutoCompleteTextView.md) | An editable text view that shows completion suggestions automatically while the user is typing. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ExpandableListView](ExpandableListView.md), [GridView](GridView.md), [ListView](ListView.md), [MultiAutoCompleteTextView](MultiAutoCompleteTextView.md) |----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ExpandableListView](ExpandableListView.md) | A view that shows items in a vertically scrolling two-level list. | | [GridView](GridView.md) | A view that shows items in two-dimensional scrolling grid. | | [ListView](ListView.md) | Displays a vertically-scrollable collection of views, where each view is positioned immediately below the previous view in the list. | | [MultiAutoCompleteTextView](MultiAutoCompleteTextView.md) | An editable text view, extending [AutoCompleteTextView](AutoCompleteTextView.md), that can show completion suggestions for the substring of the text where the user is typing instead of necessarily for the entire thing. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Listener used to receive a notification upon completion of a filtering operation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFilterComplete](../android/widget/Filter.FilterListener.md))`(`count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notifies the end of a filtering operation. |

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

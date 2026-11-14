# Filterable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filterable

Kotlin | [Java](https://developer.android.com/reference/android/widget/Filterable "View this page in Java") 

```
interface Filterable
```

| [android.widget.Filterable](https://developer.android.com/reference/kotlin/android/widget/Filterable#) |

| Known Direct Subclasses [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter), [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter), [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter), [HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter), [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](https://developer.android.com/reference/kotlin/android/widget/ArrayAdapter) | You can use this adapter to provide views for an [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) or [Spinner](https://developer.android.com/reference/kotlin/android/widget/Spinner). | | [CursorAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorAdapter) | Adapter that exposes data from a [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) to a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView) widget. | | [CursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/CursorTreeAdapter) | An adapter that exposes data from a series of [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#) s to an [ExpandableListView](https://developer.android.com/reference/kotlin/android/widget/ExpandableListView) widget. | | [HeaderViewListAdapter](https://developer.android.com/reference/kotlin/android/widget/HeaderViewListAdapter) | ListAdapter used when a ListView has header views. | | [SimpleAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleAdapter) | An easy adapter to map static data to views defined in an XML file. | |

| Known Indirect Subclasses [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter), [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter), [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter), [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorAdapter) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/ResourceCursorTreeAdapter) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorTreeAdapter](https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |

Defines a filterable behavior. A filterable class can have its data constrained by a filter. Filterable classes are usually [android.widget.Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) implementations.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | [getFilter](https://developer.android.com/reference/kotlin/android/widget/Filterable#getFilter())`()` Returns a filter that can be used to constrain data with a filtering pattern. |

## Public methods

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFilter(): Filter!
```

Returns a filter that can be used to constrain data with a filtering pattern.

This method is usually implemented by [android.widget.Adapter](https://developer.android.com/reference/kotlin/android/widget/Adapter) classes.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](https://developer.android.com/reference/kotlin/android/widget/Filter)! | a filter used to constrain data |

# Filterable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filterable

Kotlin | [Java](../android/widget/Filterable.md) 
| --- | --- |

```
interface Filterable
```

| [android.widget.Filterable](../android/widget/Filterable.md) |

| Known Direct Subclasses [ArrayAdapter](../android/widget/ArrayAdapter.md), [CursorAdapter](../android/widget/CursorAdapter.md), [CursorTreeAdapter](../android/widget/CursorTreeAdapter.md), [HeaderViewListAdapter](../android/widget/HeaderViewListAdapter.md), [SimpleAdapter](../android/widget/SimpleAdapter.md) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](../android/widget/ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](../android/widget/AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](../android/widget/ListView.md) or [Spinner](../android/widget/Spinner.md). | | [CursorAdapter](../android/widget/CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android/database/Cursor.md) to a [ListView](../android/widget/ListView.md) widget. | | [CursorTreeAdapter](../android/widget/CursorTreeAdapter.md) | An adapter that exposes data from a series of [Cursor](../android/database/Cursor.md) s to an [ExpandableListView](../android/widget/ExpandableListView.md) widget. | | [HeaderViewListAdapter](../android/widget/HeaderViewListAdapter.md) | ListAdapter used when a ListView has header views. | | [SimpleAdapter](../android/widget/SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md), [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md), [SimpleCursorAdapter](../android/widget/SimpleCursorAdapter.md), [SimpleCursorTreeAdapter](../android/widget/SimpleCursorTreeAdapter.md) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](../android/widget/ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorTreeAdapter](../android/widget/ResourceCursorTreeAdapter.md) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorAdapter](../android/widget/SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorTreeAdapter](../android/widget/SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines a filterable behavior. A filterable class can have its data constrained by a filter. Filterable classes are usually [android.widget.Adapter](../android/widget/Adapter.md) implementations.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Filter](../android/widget/Filter.md)! | [getFilter](../android/widget/Filterable.md))`()` Returns a filter that can be used to constrain data with a filtering pattern. |

## Public methods

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFilter(): Filter!
```

Returns a filter that can be used to constrain data with a filtering pattern.

This method is usually implemented by [android.widget.Adapter](../android/widget/Adapter.md) classes.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](../android/widget/Filter.md)! | a filter used to constrain data |

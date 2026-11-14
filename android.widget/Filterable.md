# Filterable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Filterable

Kotlin | [Java](Filterable.md) 
| --- | --- |

```
interface Filterable
```

| [android.widget.Filterable](Filterable.md) |

| Known Direct Subclasses [ArrayAdapter](ArrayAdapter.md), [CursorAdapter](CursorAdapter.md), [CursorTreeAdapter](CursorTreeAdapter.md), [HeaderViewListAdapter](HeaderViewListAdapter.md), [SimpleAdapter](SimpleAdapter.md) |--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayAdapter](ArrayAdapter.md) | You can use this adapter to provide views for an [AdapterView](AdapterView.md), Returns a view for each object in a collection of data objects you provide, and can be used with list-based user interface widgets such as [ListView](ListView.md) or [Spinner](Spinner.md). | | [CursorAdapter](CursorAdapter.md) | Adapter that exposes data from a [Cursor](../android.database/Cursor.md) to a [ListView](ListView.md) widget. | | [CursorTreeAdapter](CursorTreeAdapter.md) | An adapter that exposes data from a series of [Cursor](../android.database/Cursor.md) s to an [ExpandableListView](ExpandableListView.md) widget. | | [HeaderViewListAdapter](HeaderViewListAdapter.md) | ListAdapter used when a ListView has header views. | | [SimpleAdapter](SimpleAdapter.md) | An easy adapter to map static data to views defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ResourceCursorAdapter](ResourceCursorAdapter.md), [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md), [SimpleCursorAdapter](SimpleCursorAdapter.md), [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) |----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------| | [ResourceCursorAdapter](ResourceCursorAdapter.md) | An easy adapter that creates views defined in an XML file. | | [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md) | A fairly simple ExpandableListAdapter that creates views defined in an XML file. | | [SimpleCursorAdapter](SimpleCursorAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | | [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) | An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines a filterable behavior. A filterable class can have its data constrained by a filter. Filterable classes are usually [android.widget.Adapter](Adapter.md) implementations.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Filter](Filter.md)! | [getFilter](Filterable.md))`()` Returns a filter that can be used to constrain data with a filtering pattern. |

## Public methods

### getFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFilter(): Filter!
```

Returns a filter that can be used to constrain data with a filtering pattern.

This method is usually implemented by [android.widget.Adapter](Adapter.md) classes.

| Return ||
|---------------------------------------------------------------------------------|---------------------------------|
| [Filter](Filter.md)! | a filter used to constrain data |

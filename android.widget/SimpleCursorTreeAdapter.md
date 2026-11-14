# SimpleCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleCursorTreeAdapter

Kotlin| [Java](SimpleCursorTreeAdapter.md) 
| --- | --- |

```
abstract class SimpleCursorTreeAdapter : ResourceCursorTreeAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.widget.BaseExpandableListAdapter](BaseExpandableListAdapter.md) ||||
| | ↳ | [android.widget.CursorTreeAdapter](CursorTreeAdapter.md) |||
| | | ↳ | [android.widget.ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.widget.SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) |

An easy adapter to map columns from a cursor to TextViews or ImageViews defined in an XML file. You can specify which columns you want, which views you want to display the columns, and the XML file that defines the appearance of these views. Separate XML files for child and groups are possible. Binding occurs in two phases. First, if a [android.widget.SimpleCursorTreeAdapter.ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) is available, [ViewBinder.setViewValue(android.view.View, android.database.Cursor, int)](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md))is invoked. If the returned value is true, binding has occurred. If the returned value is false and the view to bind is a TextView, [setViewText(android.widget.TextView,java.lang.String)](SimpleCursorTreeAdapter.md))is invoked. If the returned value is false and the view to bind is an ImageView, [setViewImage(android.widget.ImageView,java.lang.String)](SimpleCursorTreeAdapter.md))is invoked. If no appropriate binding can be found, an [IllegalStateException](../java.lang/IllegalStateException.md) is thrown.

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) This class can be used by external clients of SimpleCursorTreeAdapter to bind values from the Cursor to views. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lastChildLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor. |
| [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `collapsedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expandedGroupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor. |
| [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `groupLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `groupFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `groupTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `childLayout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childFrom:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `childTo:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SimpleCursorTreeAdapter.ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md)! | [getViewBinder](SimpleCursorTreeAdapter.md))`()` Returns the [ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewBinder](SimpleCursorTreeAdapter.md))`(`viewBinder:` ` [SimpleCursorTreeAdapter.ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md)!`)` Sets the binder used to bind data to views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewText](SimpleCursorTreeAdapter.md))`(`v:` ` [TextView](TextView.md)!`, `text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindChildView](SimpleCursorTreeAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindGroupView](SimpleCursorTreeAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setViewImage](SimpleCursorTreeAdapter.md))`(`v:` ` [ImageView](ImageView.md)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Called by bindView() to set the image for an ImageView. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BaseExpandableListAdapter](BaseExpandableListAdapter.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAllItemsEnabled](BaseExpandableListAdapter.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildType](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of child View that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md))for the specified child item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildTypeCount](BaseExpandableListAdapter.md))`()` <br /> Returns the number of types of child Views that will be created by [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getChildView(int, int, boolean, View, ViewGroup)](ExpandableListAdapter.md)), for any group. If the adapter always returns the same type of View for all child items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](AdapterView.md). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedChildId](BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `childId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 1. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a child that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a child's ID and its group's ID. Furthermore, if [hasStableIds()](ExpandableListAdapter.md))is true, the returned ID must be stable as well. | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCombinedGroupId](BaseExpandableListAdapter.md))`(`groupId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Override this method if you foresee a clash in IDs based on this scheme: Base implementation returns a long: - bit 0: Whether this ID points to a child (unset) or group (set), so for this method this bit will be 0. - bit 1-31: Lower 31 bits of the groupId - bit 32-63: Lower 32 bits of the childId.Gets an ID for a group that is unique across any item (either group or child) that is in this list. Expandable lists require each item (group or child) to have a unique ID among all children and groups in the list. This method is responsible for returning that unique ID given a group's ID. Furthermore, if [hasStableIds()](ExpandableListAdapter.md))is true, the returned ID must be stable as well. | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupType](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Get the type of group View that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). for the specified group item. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupTypeCount](BaseExpandableListAdapter.md))`()` <br /> Returns the number of types of group Views that will be created by [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). Each type represents a set of views that can be converted in [android.widget.ExpandableListAdapter#getGroupView(int, boolean, View, ViewGroup)](ExpandableListAdapter.md)). If the adapter always returns the same type of View for all group items, this method should return 1. This method will only be called when the adapter is set on the [AdapterView](AdapterView.md). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](BaseExpandableListAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupExpanded](BaseExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDataSetObserver](BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDataSetObserver](BaseExpandableListAdapter.md))`(`observer:` ` [DataSetObserver](../android.database/DataSetObserver.md)!`)` <br /> | ||
| From class [CursorTreeAdapter](CursorTreeAdapter.md) |-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindChildView](CursorTreeAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Bind an existing view to the child data pointed to by cursor <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindGroupView](CursorTreeAdapter.md))`(`view:` ` [View](../android.view/View.md)!`, `context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Bind an existing view to the group data pointed to by cursor. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [changeCursor](CursorTreeAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [convertToString](CursorTreeAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> | | [Cursor](../android.database/Cursor.md)! | [getChild](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android.view/View.md)! | [getChildView](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Cursor](../android.database/Cursor.md)! | [getChildrenCursor](CursorTreeAdapter.md))`(`groupCursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Gets the Cursor for the children at the given group. Subclasses must implement this method to return the children data for a particular group. If you want to asynchronously query a provider to prevent blocking the UI, it is possible to return null and at a later time call [setChildrenCursor(int,android.database.Cursor)](CursorTreeAdapter.md)). It is your responsibility to manage this Cursor through the Activity lifecycle. It is a good idea to use [Activity.managedQuery](../android.app/Activity.md))which will handle this for you. In some situations, the adapter will deactivate the Cursor on its own, but this will not always be the case, so please ensure the Cursor is properly managed. <br /> | | [Cursor](../android.database/Cursor.md)! | [getCursor](CursorTreeAdapter.md))`()` <br /> | | [Filter](Filter.md)! | [getFilter](CursorTreeAdapter.md))`()` <br /> | | [FilterQueryProvider](FilterQueryProvider.md)! | [getFilterQueryProvider](CursorTreeAdapter.md))`()` <br /> | | [Cursor](../android.database/Cursor.md)! | [getGroup](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](CursorTreeAdapter.md))`()` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android.view/View.md)! | [getGroupView](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](CursorTreeAdapter.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](CursorTreeAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetChanged](CursorTreeAdapter.md))`(`releaseCursors:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies a data set change, but with the option of not releasing any cached cursors. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDataSetInvalidated](CursorTreeAdapter.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onGroupCollapsed](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Cursor](../android.database/Cursor.md)! | [runQueryOnBackgroundThread](CursorTreeAdapter.md))`(`constraint:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChildrenCursor](CursorTreeAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childrenCursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Sets the children Cursor for a particular group. If there is an existing cursor it will be closed. This is useful when asynchronously querying to prevent blocking the UI. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFilterQueryProvider](CursorTreeAdapter.md))`(`filterQueryProvider:` ` [FilterQueryProvider](FilterQueryProvider.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupCursor](CursorTreeAdapter.md))`(`cursor:` ` [Cursor](../android.database/Cursor.md)!`)` <br /> Sets the group Cursor. <br /> | ||
| From class [ExpandableListAdapter](ExpandableListAdapter.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getChild](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given child within the given group. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getChildId](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the given child within the given group. This ID must be unique across all children within the group. The combined ID (see [getCombinedChildId(long,long)](ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android.view/View.md)! | [getChildView](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Gets a View that displays the data for the given child within the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getChildrenCount](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the number of children in a specified group. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getGroup](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the data associated with the given group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupCount](ExpandableListAdapter.md))`()` <br /> Gets the number of groups. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getGroupId](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the ID for the group at the given position. This group ID must be unique across groups. The combined ID (see [getCombinedGroupId(long)](ExpandableListAdapter.md))) must be unique across ALL items (groups and all children). <br /> | | [View](../android.view/View.md)! | [getGroupView](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Gets a View that displays the given group. This View is only for the group--the Views for the group's children will be fetched using [getChildView(int,int,boolean,android.view.View,android.view.ViewGroup)](ExpandableListAdapter.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasStableIds](ExpandableListAdapter.md))`()` <br /> Indicates whether the child and group IDs are stable across changes to the underlying data. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChildSelectable](ExpandableListAdapter.md))`(`groupPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `childPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Whether the child at the specified position is selectable. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class [ResourceCursorTreeAdapter](ResourceCursorTreeAdapter.md) |---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [View](../android.view/View.md)! | [newChildView](ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `isLastChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | | [View](../android.view/View.md)! | [newGroupView](ResourceCursorTreeAdapter.md))`(`context:` ` [Context](../android.content/Context.md)!`, `cursor:` ` [Cursor](../android.database/Cursor.md)!`, `isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> | ||

## Public constructors

### SimpleCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleCursorTreeAdapter(
    context: Context!, 
    cursor: Cursor!, 
    collapsedGroupLayout: Int, 
    expandedGroupLayout: Int, 
    groupFrom: Array<String!>!, 
    groupTo: IntArray!, 
    childLayout: Int, 
    lastChildLayout: Int, 
    childFrom: Array<String!>!, 
    childTo: IntArray!)
```

Constructor.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context where the [ExpandableListView](ExpandableListView.md) associated with this [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) is running |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The database cursor |
| `collapsedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for a collapsed group. The layout file should include at least those named views defined in groupTo. |
| --- | --- |
| `expandedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for an expanded group. The layout file should include at least those named views defined in groupTo. |
| `groupFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names that will be used to display the data for a group. |
| `groupTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The group views (from the group layouts) that should display column in the "from" parameter. These should all be TextViews or ImageViews. The first N views in this list are given the values of the first N columns in the from parameter. |
| --- | --- |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for a child (except the last). The layout file should include at least those named views defined in childTo. |
| `lastChildLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for the last child within a group. The layout file should include at least those named views defined in childTo. |
| `childFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names that will be used to display the data for a child. |
| --- | --- |
| `childTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The child views (from the child layouts) that should display column in the "from" parameter. These should all be TextViews or ImageViews. The first N views in this list are given the values of the first N columns in the from parameter. |

### SimpleCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleCursorTreeAdapter(
    context: Context!, 
    cursor: Cursor!, 
    collapsedGroupLayout: Int, 
    expandedGroupLayout: Int, 
    groupFrom: Array<String!>!, 
    groupTo: IntArray!, 
    childLayout: Int, 
    childFrom: Array<String!>!, 
    childTo: IntArray!)
```

Constructor.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context where the [ExpandableListView](ExpandableListView.md) associated with this [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) is running |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The database cursor |
| `collapsedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for a collapsed group. The layout file should include at least those named views defined in groupTo. |
| --- | --- |
| `expandedGroupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for an expanded group. The layout file should include at least those named views defined in groupTo. |
| `groupFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names that will be used to display the data for a group. |
| `groupTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The group views (from the group layouts) that should display column in the "from" parameter. These should all be TextViews or ImageViews. The first N views in this list are given the values of the first N columns in the from parameter. |
| --- | --- |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for a child. The layout file should include at least those named views defined in childTo. |
| `childFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names that will be used to display the data for a child. |
| `childTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The child views (from the child layouts) that should display column in the "from" parameter. These should all be TextViews or ImageViews. The first N views in this list are given the values of the first N columns in the from parameter. |
| --- | --- |

### SimpleCursorTreeAdapter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SimpleCursorTreeAdapter(
    context: Context!, 
    cursor: Cursor!, 
    groupLayout: Int, 
    groupFrom: Array<String!>!, 
    groupTo: IntArray!, 
    childLayout: Int, 
    childFrom: Array<String!>!, 
    childTo: IntArray!)
```

Constructor.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The context where the [ExpandableListView](ExpandableListView.md) associated with this [SimpleCursorTreeAdapter](SimpleCursorTreeAdapter.md) is running |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The database cursor |
| `groupLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for a group. The layout file should include at least those named views defined in groupTo. |
| --- | --- |
| `groupFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names that will be used to display the data for a group. |
| `groupTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The group views (from the group layouts) that should display column in the "from" parameter. These should all be TextViews or ImageViews. The first N views in this list are given the values of the first N columns in the from parameter. |
| `childLayout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier of a layout file that defines the views for a child. The layout file should include at least those named views defined in childTo. |
| --- | --- |
| `childFrom` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:A list of column names that will be used to display the data for a child. |
| `childTo` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The child views (from the child layouts) that should display column in the "from" parameter. These should all be TextViews or ImageViews. The first N views in this list are given the values of the first N columns in the from parameter. |

## Public methods

### getViewBinder

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getViewBinder(): SimpleCursorTreeAdapter.ViewBinder!
```

Returns the [ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md) used to bind data to views.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SimpleCursorTreeAdapter.ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md)! | a ViewBinder or null if the binder does not exist |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter#setViewBinder(android.widget.SimpleCursorTreeAdapter.ViewBinder)> 

### setViewBinder

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewBinder(viewBinder: SimpleCursorTreeAdapter.ViewBinder!): Unit
```

Sets the binder used to bind data to views.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewBinder` | [SimpleCursorTreeAdapter.ViewBinder](../android/widget/SimpleCursorTreeAdapter.ViewBinder.md)!:the binder used to bind data to views, can be null to remove the existing binder |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/SimpleCursorTreeAdapter#getViewBinder()> 

### setViewText

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setViewText(
    v: TextView!, 
    text: String!
): Unit
```

Called by bindView() to set the text for a TextView but only if there is no existing ViewBinder or if the existing ViewBinder cannot handle binding to a TextView. Intended to be overridden by Adapters that need to filter strings retrieved from the database.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `v` | [TextView](TextView.md)!:TextView to receive text |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text to be set for the TextView |

## Protected methods

### bindChildView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun bindChildView(
    view: View!, 
    context: Context!, 
    cursor: Cursor!, 
    isLastChild: Boolean
): Unit
```

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:Existing view, returned earlier by newChildView |
| `context` | [Context](../android.content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| --- | --- |
| `isLastChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the child is the last child within its group. |

### bindGroupView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun bindGroupView(
    view: View!, 
    context: Context!, 
    cursor: Cursor!, 
    isExpanded: Boolean
): Unit
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:Existing view, returned earlier by newGroupView. |
| `context` | [Context](../android.content/Context.md)!:Interface to application's global information |
| `cursor` | [Cursor](../android.database/Cursor.md)!:The cursor from which to get the data. The cursor is already moved to the correct position. |
| --- | --- |
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the group is expanded. |

### setViewImage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setViewImage(
    v: ImageView!, 
    value: String!
): Unit
```

Called by bindView() to set the image for an ImageView. By default, the value will be treated as a Uri. Intended to be overridden by Adapters that need to filter strings retrieved from the database.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `v` | [ImageView](ImageView.md)!:ImageView to receive an image |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value retrieved from the cursor |

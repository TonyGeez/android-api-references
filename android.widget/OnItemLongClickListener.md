# AdapterView.OnItemLongClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnItemLongClickListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/AdapterView.OnItemLongClickListener "View this page in Java") 
| --- | --- |

```
interface OnItemLongClickListener
```

| [android.widget.AdapterView.OnItemLongClickListener](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemLongClickListener#) |

Interface definition for a callback to be invoked when an item in this view has been clicked and held.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onItemLongClick](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemLongClickListener#onItemLongClick(android.widget.AdapterView,%20android.view.View,%20kotlin.Int,%20kotlin.Long))`(`parent:` ` [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)<*>!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback method to be invoked when an item in this view has been clicked and held. |

## Public methods

### onItemLongClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onItemLongClick(
    parent: AdapterView<*>!, 
    view: View!, 
    position: Int, 
    id: Long
): Boolean
```

Callback method to be invoked when an item in this view has been clicked and held. Implementers can call getItemAtPosition(position) if they need to access the data associated with the selected item.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)\<\*\>!:The AbsListView where the click happened |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view within the AbsListView that was clicked |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the view in the list |
| --- | --- |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The row id of the item that was clicked |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the callback consumed the long click, false otherwise |

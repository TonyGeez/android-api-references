# AdapterView.OnItemSelectedListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnItemSelectedListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/AdapterView.OnItemSelectedListener "View this page in Java") 

```
interface OnItemSelectedListener
```

| [android.widget.AdapterView.OnItemSelectedListener](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemSelectedListener#) |

Interface definition for a callback to be invoked when an item in this view has been selected.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onItemSelected](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemSelectedListener#onItemSelected(android.widget.AdapterView,%20android.view.View,%20kotlin.Int,%20kotlin.Long))`(`parent:` ` [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)<*>!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback method to be invoked when an item in this view has been selected. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNothingSelected](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemSelectedListener#onNothingSelected(android.widget.AdapterView))`(`parent:` ` [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)<*>!`)` Callback method to be invoked when the selection disappears from this view. |

## Public methods

### onItemSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onItemSelected(
    parent: AdapterView<*>!, 
    view: View!, 
    position: Int, 
    id: Long
): Unit
```

Callback method to be invoked when an item in this view has been selected. This callback is invoked only when the newly selected position is different from the previously selected position or if there was no selected item.
Implementers can call getItemAtPosition(position) if they need to access the data associated with the selected item.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)\<\*\>!:The AdapterView where the selection happened |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view within the AdapterView that was clicked |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the view in the adapter |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The row id of the item that is selected |

### onNothingSelected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNothingSelected(parent: AdapterView<*>!): Unit
```

Callback method to be invoked when the selection disappears from this view. The selection can disappear for instance when touch is activated or when the adapter becomes empty.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)\<\*\>!:The AdapterView that now contains no selected item. |

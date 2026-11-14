# AdapterView.OnItemClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnItemClickListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/AdapterView.OnItemClickListener "View this page in Java") 
| --- | --- |

```
interface OnItemClickListener
```

| [android.widget.AdapterView.OnItemClickListener](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemClickListener#) |

| Known Direct Subclasses [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#), [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen.html#) |-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#) | Dialog for choosing accented characters related to a base character. | | [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen.html#) | Represents a top-level [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference.html#) that is the root of a Preference hierarchy. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when an item in this AdapterView has been clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onItemClick](https://developer.android.com/reference/kotlin/android/widget/AdapterView.OnItemClickListener#onItemClick(android.widget.AdapterView,%20android.view.View,%20kotlin.Int,%20kotlin.Long))`(`parent:` ` [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)<*>!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback method to be invoked when an item in this AdapterView has been clicked. |

## Public methods

### onItemClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onItemClick(
    parent: AdapterView<*>!, 
    view: View!, 
    position: Int, 
    id: Long
): Unit
```

Callback method to be invoked when an item in this AdapterView has been clicked.

Implementers can call getItemAtPosition(position) if they need to access the data associated with the selected item.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [AdapterView](https://developer.android.com/reference/kotlin/android/widget/AdapterView)\<\*\>!:The AdapterView where the click happened. |
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The view within the AdapterView that was clicked (this will be a view provided by the adapter) |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the view in the adapter. |
| --- | --- |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The row id of the item that was clicked. |

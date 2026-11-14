# AdapterView.OnItemClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnItemClickListener

Kotlin| [Java](../android/widget/AdapterView.OnItemClickListener.md) 
| --- | --- |

```
interface OnItemClickListener
```

| [android.widget.AdapterView.OnItemClickListener](../android/widget/AdapterView.OnItemClickListener.md) |

| Known Direct Subclasses [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md), [PreferenceScreen](../android/preference/PreferenceScreen.md) |-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. | | [PreferenceScreen](../android/preference/PreferenceScreen.md) | Represents a top-level [Preference](../android/preference/Preference.md) that is the root of a Preference hierarchy. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when an item in this AdapterView has been clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onItemClick](../android/widget/AdapterView.OnItemClickListener.md))`(`parent:` ` [AdapterView](../android/widget/AdapterView.md)<*>!`, `view:` ` [View](../android/view/View.md)!`, `position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Callback method to be invoked when an item in this AdapterView has been clicked. |

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
| `parent` | [AdapterView](../android/widget/AdapterView.md)\<\*\>!:The AdapterView where the click happened. |
| `view` | [View](../android/view/View.md)!:The view within the AdapterView that was clicked (this will be a view provided by the adapter) |
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position of the view in the adapter. |
| --- | --- |
| `id` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The row id of the item that was clicked. |

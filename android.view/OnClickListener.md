# View.OnClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClickListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnClickListener "View this page in Java") 
| --- | --- |

```
interface OnClickListener
```

| [android.view.View.OnClickListener](https://developer.android.com/reference/kotlin/android/view/View.OnClickListener#) |

| Known Direct Subclasses [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#), [KeyboardView](https://developer.android.com/reference/kotlin/android/inputmethodservice/KeyboardView.html#), [QuickContactBadge](https://developer.android.com/reference/kotlin/android/widget/QuickContactBadge.html#) |-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------| | [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog.html#) | Dialog for choosing accented characters related to a base character. | | [KeyboardView](https://developer.android.com/reference/kotlin/android/inputmethodservice/KeyboardView.html#) | A view that renders a virtual [Keyboard](https://developer.android.com/reference/kotlin/android/inputmethodservice/Keyboard.html#). | | [QuickContactBadge](https://developer.android.com/reference/kotlin/android/widget/QuickContactBadge.html#) | Widget used to show an image with the standard QuickContact badge and on-click behavior. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when a view is clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](https://developer.android.com/reference/kotlin/android/view/View.OnClickListener#onClick(android.view.View))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Called when a view has been clicked. |

## Public methods

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClick(v: View!): Unit
```

Called when a view has been clicked.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view that was clicked. |

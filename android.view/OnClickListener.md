# View.OnClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClickListener

Kotlin| [Java](../android/view/View.OnClickListener.md) 
| --- | --- |

```
interface OnClickListener
```

| [android.view.View.OnClickListener](../android/view/View.OnClickListener.md) |

| Known Direct Subclasses [CharacterPickerDialog](../android.text.method/CharacterPickerDialog.md), [KeyboardView](../android.inputmethodservice/KeyboardView.md), [QuickContactBadge](../android.widget/QuickContactBadge.md) |-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------| | [CharacterPickerDialog](../android.text.method/CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. | | [KeyboardView](../android.inputmethodservice/KeyboardView.md) | A view that renders a virtual [Keyboard](../android.inputmethodservice/Keyboard.md). | | [QuickContactBadge](../android.widget/QuickContactBadge.md) | Widget used to show an image with the standard QuickContact badge and on-click behavior. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when a view is clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](../android/view/View.OnClickListener.md))`(`v:` ` [View](View.md)!`)` Called when a view has been clicked. |

## Public methods

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClick(v: View!): Unit
```

Called when a view has been clicked.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md)!:The view that was clicked. |

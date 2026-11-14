# Checkable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Checkable

Kotlin| [Java](https://developer.android.com/reference/android/widget/Checkable "View this page in Java") 

```
interface Checkable
```

| [android.widget.Checkable](https://developer.android.com/reference/kotlin/android/widget/Checkable#) |

| Known Direct Subclasses [CheckedTextView](https://developer.android.com/reference/kotlin/android/widget/CheckedTextView), [CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CheckedTextView](https://developer.android.com/reference/kotlin/android/widget/CheckedTextView) | An extension to [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView) that supports the [Checkable](https://developer.android.com/reference/kotlin/android/widget/Checkable#) interface and displays. | | [CompoundButton](https://developer.android.com/reference/kotlin/android/widget/CompoundButton) | A button with two states, checked and unchecked. | |

| Known Indirect Subclasses [CheckBox](https://developer.android.com/reference/kotlin/android/widget/CheckBox), [RadioButton](https://developer.android.com/reference/kotlin/android/widget/RadioButton), [Switch](https://developer.android.com/reference/kotlin/android/widget/Switch), [ToggleButton](https://developer.android.com/reference/kotlin/android/widget/ToggleButton) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [CheckBox](https://developer.android.com/reference/kotlin/android/widget/CheckBox) | A checkbox is a specific type of two-states button that can be either checked or unchecked. | | [RadioButton](https://developer.android.com/reference/kotlin/android/widget/RadioButton) | A radio button is a two-states button that can be either checked or unchecked. | | [Switch](https://developer.android.com/reference/kotlin/android/widget/Switch) | A Switch is a two-state toggle widget. | | [ToggleButton](https://developer.android.com/reference/kotlin/android/widget/ToggleButton) | Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF". | |

Defines an extension for views that make them checkable.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](https://developer.android.com/reference/kotlin/android/widget/Checkable#isChecked())`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChecked](https://developer.android.com/reference/kotlin/android/widget/Checkable#setChecked(kotlin.Boolean))`(`checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Change the checked state of the view |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [toggle](https://developer.android.com/reference/kotlin/android/widget/Checkable#toggle())`()` Change the checked state of the view to the inverse of its current state |

## Public methods

### isChecked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isChecked(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The current checked state of the view |

### setChecked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setChecked(checked: Boolean): Unit
```

Change the checked state of the view

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------|
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The new checked state |

### toggle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toggle(): Unit
```

Change the checked state of the view to the inverse of its current state

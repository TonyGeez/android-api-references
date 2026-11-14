# Checkable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Checkable

Kotlin| [Java](Checkable.md) 
| --- | --- |

```
interface Checkable
```

| [android.widget.Checkable](Checkable.md) |

| Known Direct Subclasses [CheckedTextView](CheckedTextView.md), [CompoundButton](CompoundButton.md) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CheckedTextView](CheckedTextView.md) | An extension to [TextView](TextView.md) that supports the [Checkable](Checkable.md) interface and displays. | | [CompoundButton](CompoundButton.md) | A button with two states, checked and unchecked. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CheckBox](CheckBox.md), [RadioButton](RadioButton.md), [Switch](Switch.md), [ToggleButton](ToggleButton.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [CheckBox](CheckBox.md) | A checkbox is a specific type of two-states button that can be either checked or unchecked. | | [RadioButton](RadioButton.md) | A radio button is a two-states button that can be either checked or unchecked. | | [Switch](Switch.md) | A Switch is a two-state toggle widget. | | [ToggleButton](ToggleButton.md) | Displays checked/unchecked states as a button with a "light" indicator and by default accompanied with the text "ON" or "OFF". | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines an extension for views that make them checkable.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](Checkable.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChecked](Checkable.md))`(`checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Change the checked state of the view |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [toggle](Checkable.md))`()` Change the checked state of the view to the inverse of its current state |
| --- | --- |

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

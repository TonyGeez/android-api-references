Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCheckedChangeListener

Kotlin | [Java](../android/widget/CompoundButton.OnCheckedChangeListener.md)
| --- | --- |

```
interface OnCheckedChangeListener
```

| [android.widget.CompoundButton.OnCheckedChangeListener](../android/widget/CompoundButton.OnCheckedChangeListener.md) |

Interface definition for a callback to be invoked when the checked state of a compound button changed.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/CompoundButton.OnCheckedChangeListener#onCheckedChanged(android.widget.CompoundButton,%20kotlin.Boolean)(buttonView: https://developer.android.com/reference/kotlin/android/widget/CompoundButton, isChecked: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the checked state of a compound button has changed. |

## Public methods

### onCheckedChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCheckedChanged(
    buttonView: CompoundButton, 
    isChecked: Boolean
): Unit
```

Called when the checked state of a compound button has changed.

| Parameters ||
|---|---|
| `buttonView` | [CompoundButton](CompoundButton.md): The compound button view whose state has changed. This value cannot be `null`. |
| `isChecked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The new checked state of buttonView. |

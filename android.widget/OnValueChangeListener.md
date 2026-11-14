# NumberPicker.OnValueChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnValueChangeListener

Kotlin| [Java](../android/widget/NumberPicker.OnValueChangeListener.md) 
| --- | --- |

```
interface OnValueChangeListener
```

| [android.widget.NumberPicker.OnValueChangeListener](../android/widget/NumberPicker.OnValueChangeListener.md) |

Interface to listen for changes of the current value.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onValueChange](../android/widget/NumberPicker.OnValueChangeListener.md))`(`picker:` ` [NumberPicker](../android/widget/NumberPicker.md)!`, `oldVal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newVal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called upon a change of the current value. |

## Public methods

### onValueChange

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onValueChange(
    picker: NumberPicker!, 
    oldVal: Int, 
    newVal: Int
): Unit
```

Called upon a change of the current value.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `picker` | [NumberPicker](../android/widget/NumberPicker.md)!:The NumberPicker associated with this listener. |
| `oldVal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous value. |
| `newVal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new value. |
| --- | --- |

# NumberPicker.OnValueChangeListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnValueChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/NumberPicker.OnValueChangeListener "View this page in Java") 
| --- | --- |

```
interface OnValueChangeListener
```

| [android.widget.NumberPicker.OnValueChangeListener](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.OnValueChangeListener#) |

Interface to listen for changes of the current value.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onValueChange](https://developer.android.com/reference/kotlin/android/widget/NumberPicker.OnValueChangeListener#onValueChange(android.widget.NumberPicker,%20kotlin.Int,%20kotlin.Int))`(`picker:` ` [NumberPicker](https://developer.android.com/reference/kotlin/android/widget/NumberPicker)!`, `oldVal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newVal:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called upon a change of the current value. |

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
| `picker` | [NumberPicker](https://developer.android.com/reference/kotlin/android/widget/NumberPicker)!:The NumberPicker associated with this listener. |
| `oldVal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous value. |
| `newVal` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new value. |
| --- | --- |

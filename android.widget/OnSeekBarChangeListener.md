# SeekBar.OnSeekBarChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSeekBarChangeListener

Kotlin| [Java](../android/widget/SeekBar.OnSeekBarChangeListener.md) 
| --- | --- |

```
interface OnSeekBarChangeListener
```

| [android.widget.SeekBar.OnSeekBarChangeListener](../android/widget/SeekBar.OnSeekBarChangeListener.md) |

A callback that notifies clients when the progress level has been changed. This includes changes that were initiated by the user through a touch gesture or arrow key/trackball as well as changes that were initiated programmatically.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgressChanged](../android/widget/SeekBar.OnSeekBarChangeListener.md))`(`seekBar:` ` [SeekBar](../android/widget/SeekBar.md)!`, `progress:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fromUser:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notification that the progress level has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartTrackingTouch](../android/widget/SeekBar.OnSeekBarChangeListener.md))`(`seekBar:` ` [SeekBar](../android/widget/SeekBar.md)!`)` Notification that the user has started a touch gesture. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopTrackingTouch](../android/widget/SeekBar.OnSeekBarChangeListener.md))`(`seekBar:` ` [SeekBar](../android/widget/SeekBar.md)!`)` Notification that the user has finished a touch gesture. |
| --- | --- |

## Public methods

### onProgressChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProgressChanged(
    seekBar: SeekBar!, 
    progress: Int, 
    fromUser: Boolean
): Unit
```

Notification that the progress level has changed. Clients can use the fromUser parameter to distinguish user-initiated changes from those that occurred programmatically.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seekBar` | [SeekBar](../android/widget/SeekBar.md)!:The SeekBar whose progress has changed |
| `progress` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current progress level. This will be in the range min..max where min and max were set by [ProgressBar.setMin(int)](../android/widget/ProgressBar.md))and [ProgressBar.setMax(int)](../android/widget/ProgressBar.md)), respectively. (The default values for min is 0 and max is 100.) |
| `fromUser` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the progress change was initiated by the user. |
| --- | --- |

### onStartTrackingTouch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartTrackingTouch(seekBar: SeekBar!): Unit
```

Notification that the user has started a touch gesture. Clients may want to use this to disable advancing the seekbar.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `seekBar` | [SeekBar](../android/widget/SeekBar.md)!:The SeekBar in which the touch gesture began |

### onStopTrackingTouch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopTrackingTouch(seekBar: SeekBar!): Unit
```

Notification that the user has finished a touch gesture. Clients may want to use this to re-enable advancing the seekbar.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `seekBar` | [SeekBar](../android/widget/SeekBar.md)!:The SeekBar in which the touch gesture began |

# SeekBar.OnSeekBarChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSeekBarChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/SeekBar.OnSeekBarChangeListener "View this page in Java") 

```
interface OnSeekBarChangeListener
```

| [android.widget.SeekBar.OnSeekBarChangeListener](https://developer.android.com/reference/kotlin/android/widget/SeekBar.OnSeekBarChangeListener#) |

A callback that notifies clients when the progress level has been changed. This includes changes that were initiated by the user through a touch gesture or arrow key/trackball as well as changes that were initiated programmatically.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProgressChanged](https://developer.android.com/reference/kotlin/android/widget/SeekBar.OnSeekBarChangeListener#onProgressChanged(android.widget.SeekBar,%20kotlin.Int,%20kotlin.Boolean))`(`seekBar:` ` [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar)!`, `progress:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fromUser:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notification that the progress level has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStartTrackingTouch](https://developer.android.com/reference/kotlin/android/widget/SeekBar.OnSeekBarChangeListener#onStartTrackingTouch(android.widget.SeekBar))`(`seekBar:` ` [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar)!`)` Notification that the user has started a touch gesture. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStopTrackingTouch](https://developer.android.com/reference/kotlin/android/widget/SeekBar.OnSeekBarChangeListener#onStopTrackingTouch(android.widget.SeekBar))`(`seekBar:` ` [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar)!`)` Notification that the user has finished a touch gesture. |

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
| `seekBar` | [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar)!:The SeekBar whose progress has changed |
| `progress` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current progress level. This will be in the range min..max where min and max were set by [ProgressBar.setMin(int)](https://developer.android.com/reference/kotlin/android/widget/ProgressBar#setMin(kotlin.Int))and [ProgressBar.setMax(int)](https://developer.android.com/reference/kotlin/android/widget/ProgressBar#setMax(kotlin.Int)), respectively. (The default values for min is 0 and max is 100.) |
| `fromUser` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the progress change was initiated by the user. |

### onStartTrackingTouch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStartTrackingTouch(seekBar: SeekBar!): Unit
```

Notification that the user has started a touch gesture. Clients may want to use this to disable advancing the seekbar.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `seekBar` | [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar)!:The SeekBar in which the touch gesture began |

### onStopTrackingTouch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onStopTrackingTouch(seekBar: SeekBar!): Unit
```

Notification that the user has finished a touch gesture. Clients may want to use this to re-enable advancing the seekbar.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `seekBar` | [SeekBar](https://developer.android.com/reference/kotlin/android/widget/SeekBar)!:The SeekBar in which the touch gesture began |

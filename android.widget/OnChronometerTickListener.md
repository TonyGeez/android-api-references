# Chronometer.OnChronometerTickListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnChronometerTickListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/Chronometer.OnChronometerTickListener "View this page in Java") 
| --- | --- |

```
interface OnChronometerTickListener
```

| [android.widget.Chronometer.OnChronometerTickListener](https://developer.android.com/reference/kotlin/android/widget/Chronometer.OnChronometerTickListener#) |

A callback that notifies when the chronometer has incremented on its own.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChronometerTick](https://developer.android.com/reference/kotlin/android/widget/Chronometer.OnChronometerTickListener#onChronometerTick(android.widget.Chronometer))`(`chronometer:` ` [Chronometer](https://developer.android.com/reference/kotlin/android/widget/Chronometer)!`)` Notification that the chronometer has changed. |

## Public methods

### onChronometerTick

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChronometerTick(chronometer: Chronometer!): Unit
```

Notification that the chronometer has changed.

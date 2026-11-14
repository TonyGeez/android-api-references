# Chronometer.OnChronometerTickListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnChronometerTickListener

Kotlin| [Java](../android/widget/Chronometer.OnChronometerTickListener.md) 
| --- | --- |

```
interface OnChronometerTickListener
```

| [android.widget.Chronometer.OnChronometerTickListener](../android/widget/Chronometer.OnChronometerTickListener.md) |

A callback that notifies when the chronometer has incremented on its own.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChronometerTick](../android/widget/Chronometer.OnChronometerTickListener.md))`(`chronometer:` ` [Chronometer](../android/widget/Chronometer.md)!`)` Notification that the chronometer has changed. |

## Public methods

### onChronometerTick

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onChronometerTick(chronometer: Chronometer!): Unit
```

Notification that the chronometer has changed.

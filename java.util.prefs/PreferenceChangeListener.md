# PreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceChangeListener

```
@FunctionalInterface interface PreferenceChangeListener : EventListener
```

| [java.util.prefs.PreferenceChangeListener](../java/util/prefs/PreferenceChangeListener.md) |

A listener for receiving preference change events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [preferenceChange](../java/util/prefs/PreferenceChangeListener.md))`(`evt:` ` [PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md)!`)` This method gets called when a preference is added, removed or when its value is changed. |

## Public methods

### preferenceChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun preferenceChange(evt: PreferenceChangeEvent!): Unit
```

This method gets called when a preference is added, removed or when its value is changed.

<br />

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evt` | [PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md)!:A PreferenceChangeEvent object describing the event source and the preference that has changed. |

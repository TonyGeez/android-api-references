# PreferencesFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferencesFactory

```
interface PreferencesFactory
```

| [java.util.prefs.PreferencesFactory](../java/util/prefs/PreferencesFactory.md) |

A factory object that generates Preferences objects. Providers of new [Preferences](../java/util/prefs/Preferences.md) implementations should provide corresponding PreferencesFactory implementations so that the new Preferences implementation can be installed in place of the platform-specific default implementation.

**This class is for Preferences implementers only. Normal users of the Preferences facility should have no need to consult this documentation.**

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Preferences](../java/util/prefs/Preferences.md)! | [systemRoot](../java/util/prefs/PreferencesFactory.md))`()` Returns the system root preference node. |
| abstract [Preferences](../java/util/prefs/Preferences.md)! | [userRoot](../java/util/prefs/PreferencesFactory.md))`()` Returns the user root preference node corresponding to the calling user. |

## Public methods

### systemRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun systemRoot(): Preferences!
```

Returns the system root preference node. (Multiple calls on this method will return the same object reference.)

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | the system root preference node |

### userRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun userRoot(): Preferences!
```

Returns the user root preference node corresponding to the calling user. In a server, the returned value will typically depend on some implicit client-context.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Preferences](../java/util/prefs/Preferences.md)! | the user root preference node corresponding to the calling user |

# PreferencesFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferencesFactory

```
interface PreferencesFactory
```

| [java.util.prefs.PreferencesFactory](PreferencesFactory.md) |

A factory object that generates Preferences objects. Providers of new [Preferences](Preferences.md) implementations should provide corresponding PreferencesFactory implementations so that the new Preferences implementation can be installed in place of the platform-specific default implementation.

**This class is for Preferences implementers only. Normal users of the Preferences facility should have no need to consult this documentation.**

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Preferences](Preferences.md)! | [systemRoot](PreferencesFactory.md))`()` Returns the system root preference node. |
| abstract [Preferences](Preferences.md)! | [userRoot](PreferencesFactory.md))`()` Returns the user root preference node corresponding to the calling user. |

## Public methods

### systemRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun systemRoot(): Preferences!
```

Returns the system root preference node. (Multiple calls on this method will return the same object reference.)

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------|
| [Preferences](Preferences.md)! | the system root preference node |

### userRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun userRoot(): Preferences!
```

Returns the user root preference node corresponding to the calling user. In a server, the returned value will typically depend on some implicit client-context.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Preferences](Preferences.md)! | the user root preference node corresponding to the calling user |

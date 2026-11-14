# PreferencesFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferencesFactory

```
interface PreferencesFactory
```

| [java.util.prefs.PreferencesFactory](https://developer.android.com/reference/kotlin/java/util/prefs/PreferencesFactory#) |

A factory object that generates Preferences objects. Providers of new [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences) implementations should provide corresponding PreferencesFactory implementations so that the new Preferences implementation can be installed in place of the platform-specific default implementation.

**This class is for Preferences implementers only. Normal users of the Preferences facility should have no need to consult this documentation.**

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | [systemRoot](https://developer.android.com/reference/kotlin/java/util/prefs/PreferencesFactory#systemRoot())`()` Returns the system root preference node. |
| abstract [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | [userRoot](https://developer.android.com/reference/kotlin/java/util/prefs/PreferencesFactory#userRoot())`()` Returns the user root preference node corresponding to the calling user. |

## Public methods

### systemRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun systemRoot(): Preferences!
```

Returns the system root preference node. (Multiple calls on this method will return the same object reference.)

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------|
| [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | the system root preference node |

### userRoot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun userRoot(): Preferences!
```

Returns the user root preference node corresponding to the calling user. In a server, the returned value will typically depend on some implicit client-context.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences)! | the user root preference node corresponding to the calling user |

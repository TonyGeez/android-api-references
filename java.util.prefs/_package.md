# java.util.prefs

# java.util.prefs

## Interfaces

| [NodeChangeListener](../java/util/prefs/NodeChangeListener.md) | A listener for receiving preference node change events. |
| --- | --- |
| [PreferenceChangeListener](../java/util/prefs/PreferenceChangeListener.md) | A listener for receiving preference change events. |
| [PreferencesFactory](../java/util/prefs/PreferencesFactory.md) | A factory object that generates Preferences objects. |

## Classes

| [AbstractPreferences](../java/util/prefs/AbstractPreferences.md) | This class provides a skeletal implementation of the [Preferences](../java/util/prefs/Preferences.md) class, greatly easing the task of implementing it. |
| --- | --- |
| [NodeChangeEvent](../java/util/prefs/NodeChangeEvent.md) | An event emitted by a Preferences node to indicate that a child of that node has been added or removed. |
| [PreferenceChangeEvent](../java/util/prefs/PreferenceChangeEvent.md) | An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed. |
| [Preferences](../java/util/prefs/Preferences.md) | A node in a hierarchical collection of preference data. |
| --- | --- |

## Exceptions

| [BackingStoreException](../java/util/prefs/BackingStoreException.md) | Thrown to indicate that a preferences operation could not complete because of a failure in the backing store, or a failure to contact the backing store. |
| --- | --- |
| [InvalidPreferencesFormatException](../java/util/prefs/InvalidPreferencesFormatException.md) | Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of preferences, as per the [Preferences](../java/util/prefs/Preferences.md) specification. |

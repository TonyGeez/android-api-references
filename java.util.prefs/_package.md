# java.util.prefs

# java.util.prefs

## Interfaces

| [NodeChangeListener](NodeChangeListener.md) | A listener for receiving preference node change events. |
| --- | --- |
| [PreferenceChangeListener](PreferenceChangeListener.md) | A listener for receiving preference change events. |
| [PreferencesFactory](PreferencesFactory.md) | A factory object that generates Preferences objects. |

## Classes

| [AbstractPreferences](AbstractPreferences.md) | This class provides a skeletal implementation of the [Preferences](Preferences.md) class, greatly easing the task of implementing it. |
| --- | --- |
| [NodeChangeEvent](NodeChangeEvent.md) | An event emitted by a Preferences node to indicate that a child of that node has been added or removed. |
| [PreferenceChangeEvent](PreferenceChangeEvent.md) | An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed. |
| [Preferences](Preferences.md) | A node in a hierarchical collection of preference data. |
| --- | --- |

## Exceptions

| [BackingStoreException](BackingStoreException.md) | Thrown to indicate that a preferences operation could not complete because of a failure in the backing store, or a failure to contact the backing store. |
| --- | --- |
| [InvalidPreferencesFormatException](InvalidPreferencesFormatException.md) | Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of preferences, as per the [Preferences](Preferences.md) specification. |

# java.util.prefs

# java.util.prefs

## Interfaces

| [NodeChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeListener) | A listener for receiving preference node change events. |
| [PreferenceChangeListener](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeListener) | A listener for receiving preference change events. |
| [PreferencesFactory](https://developer.android.com/reference/kotlin/java/util/prefs/PreferencesFactory) | A factory object that generates Preferences objects. |

## Classes

| [AbstractPreferences](https://developer.android.com/reference/kotlin/java/util/prefs/AbstractPreferences) | This class provides a skeletal implementation of the [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences) class, greatly easing the task of implementing it. |
| [NodeChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/NodeChangeEvent) | An event emitted by a Preferences node to indicate that a child of that node has been added or removed. |
| [PreferenceChangeEvent](https://developer.android.com/reference/kotlin/java/util/prefs/PreferenceChangeEvent) | An event emitted by a Preferences node to indicate that a preference has been added, removed or has had its value changed. |
| [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences) | A node in a hierarchical collection of preference data. |

## Exceptions

| [BackingStoreException](https://developer.android.com/reference/kotlin/java/util/prefs/BackingStoreException) | Thrown to indicate that a preferences operation could not complete because of a failure in the backing store, or a failure to contact the backing store. |
| [InvalidPreferencesFormatException](https://developer.android.com/reference/kotlin/java/util/prefs/InvalidPreferencesFormatException) | Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of preferences, as per the [Preferences](https://developer.android.com/reference/kotlin/java/util/prefs/Preferences) specification. |

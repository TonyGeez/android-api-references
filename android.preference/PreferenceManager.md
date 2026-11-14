# PreferenceManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceManager

Kotlin| [Java](https://developer.android.com/reference/android/preference/PreferenceManager "View this page in Java") 
| --- | --- |

```
open class PreferenceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.preference.PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#) |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Used to help create [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) hierarchies from activities or XML.

In most cases, clients should use [PreferenceActivity.addPreferencesFromIntent](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity#addPreferencesFromIntent(android.content.Intent))or [PreferenceActivity.addPreferencesFromResource(int)](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity#addPreferencesFromResource(kotlin.Int)).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnActivityDestroyListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityDestroyListener) Interface definition for a class that will be called when the container's activity is destroyed. |
| abstract | [OnActivityResultListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityResultListener) Interface definition for a class that will be called when the container's activity receives an activity result. |
| abstract | [OnActivityStopListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityStopListener) Interface definition for a class that will be called when the container's activity is stopped. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_HAS_SET_DEFAULT_VALUES](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#KEY_HAS_SET_DEFAULT_VALUES:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METADATA_KEY_PREFERENCES](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#METADATA_KEY_PREFERENCES:kotlin.String) The Activity meta-data key for its XML preference hierarchy. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen)! | [createPreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#createPreferenceScreen(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> |
| open [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference)? | [findPreference](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#findPreference(kotlin.CharSequence))`(`key:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Finds a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) based on its key. |
| openstatic [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#)! | [getDefaultSharedPreferences](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getDefaultSharedPreferences(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Gets a [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) instance that points to the default file that is used by the preference framework in the given context. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultSharedPreferencesName](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getDefaultSharedPreferencesName(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Returns the name used for storing default shared preferences. |
| open [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)? | [getPreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getPreferenceDataStore())`()` Returns the [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) associated with this manager or`null`if the default [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) are used instead. |
| open [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#)! | [getSharedPreferences](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getSharedPreferences())`()` Gets a [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) instance that preferences managed by this will use. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSharedPreferencesMode](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getSharedPreferencesMode())`()` Returns the current mode of the SharedPreferences file that preferences managed by this will use. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSharedPreferencesName](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getSharedPreferencesName())`()` Returns the current name of the SharedPreferences file that preferences managed by this will use. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStorageDefault](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#isStorageDefault())`()` Indicates if the storage location used internally by this class is the default provided by the hosting [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStorageDeviceProtected](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#isStorageDeviceProtected())`()` Indicates if the storage location used internally by this class is backed by device-protected storage. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValues](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setDefaultValues(android.content.Context,%20kotlin.Int,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readAgain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the default values from an XML preference file by reading the values defined by each [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) item's`android:defaultValue`attribute. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValues](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setDefaultValues(android.content.Context,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `sharedPreferencesName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sharedPreferencesMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readAgain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Similar to [setDefaultValues(android.content.Context,int,boolean)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setDefaultValues(android.content.Context,%20kotlin.Int,%20kotlin.Boolean))but allows the client to provide the filename and mode of the shared preferences file. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setPreferenceDataStore(android.preference.PreferenceDataStore))`(`dataStore:` ` [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)!`)` Sets a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) to be used by all Preferences associated with this manager that don't have a custom [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) assigned via [Preference.setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedPreferencesMode](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setSharedPreferencesMode(kotlin.Int))`(`sharedPreferencesMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the mode of the SharedPreferences file that preferences managed by this will use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedPreferencesName](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setSharedPreferencesName(kotlin.String))`(`sharedPreferencesName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of the SharedPreferences file that preferences managed by this will use. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStorageDefault](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setStorageDefault())`()` Sets the storage location used internally by this class to be the default provided by the hosting [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStorageDeviceProtected](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setStorageDeviceProtected())`()` Explicitly set the storage location used internally by this class to be device-protected storage. |

## Constants

### KEY_HAS_SET_DEFAULT_VALUES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY_HAS_SET_DEFAULT_VALUES: String
```

**Deprecated:** *Deprecated in Java.* 

 Value: "_has_set_default_values"

### METADATA_KEY_PREFERENCES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_PREFERENCES: String
```

**Deprecated:** *Deprecated in Java.*

The Activity meta-data key for its XML preference hierarchy. 

 Value: "android.preference"

## Public methods

### createPreferenceScreen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createPreferenceScreen(context: Context!): PreferenceScreen!
```

**Deprecated:** *Deprecated in Java.* 

### findPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findPreference(key: CharSequence!): Preference?
```

**Deprecated:** *Deprecated in Java.*

Finds a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) based on its key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the key of the preference to retrieve |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference)? | the [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) with the key, or`null` |

**See Also**

- [android.preference.PreferenceGroup#findPreference(CharSequence)](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup#findPreference(kotlin.CharSequence)) 

### getDefaultSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultSharedPreferences(context: Context!): SharedPreferences!
```

**Deprecated:** *Deprecated in Java.*

Gets a [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) instance that points to the default file that is used by the preference framework in the given context.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context of the preferences whose values are wanted. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#)! | A [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) instance that can be used to retrieve and listen to values of the preferences. |

### getDefaultSharedPreferencesName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultSharedPreferencesName(context: Context!): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the name used for storing default shared preferences. 
**See Also**

- [#getDefaultSharedPreferences(Context)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getDefaultSharedPreferences(android.content.Context)) 

### getPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceDataStore(): PreferenceDataStore?
```

**Deprecated:** *Deprecated in Java.*

Returns the [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) associated with this manager or`null`if the default [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) are used instead.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)? | The [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) associated with this manager or`null`if none. |

**See Also**

- [#setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setPreferenceDataStore(android.preference.PreferenceDataStore)) 

### getSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferences(): SharedPreferences!
```

**Deprecated:** *Deprecated in Java.*

Gets a [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) instance that preferences managed by this will use.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#)! | a [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) instance pointing to the file that contains the values of preferences that are managed by this PreferenceManager. If a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) has been set, this method returns`null`. |

### getSharedPreferencesMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferencesMode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the current mode of the SharedPreferences file that preferences managed by this will use.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The mode that can be passed to [Context.getSharedPreferences(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSharedPreferences(kotlin.String,%20kotlin.Int)). |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSharedPreferences(kotlin.String,%20kotlin.Int)) 

### getSharedPreferencesName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferencesName(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the current name of the SharedPreferences file that preferences managed by this will use.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The name that can be passed to [Context.getSharedPreferences(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSharedPreferences(kotlin.String,%20kotlin.Int)). |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSharedPreferences(kotlin.String,%20kotlin.Int)) 

### isStorageDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStorageDefault(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Indicates if the storage location used internally by this class is the default provided by the hosting [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#). 
**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setStorageDefault()>
- <https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setStorageDeviceProtected()> 

### isStorageDeviceProtected

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStorageDeviceProtected(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Indicates if the storage location used internally by this class is backed by device-protected storage. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setStorageDefault()>
- <https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setStorageDeviceProtected()> 

### setDefaultValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefaultValues(
    context: Context!, 
    resId: Int, 
    readAgain: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the default values from an XML preference file by reading the values defined by each [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) item's`android:defaultValue`attribute. This should be called by the application's main activity.

<br />

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context of the shared preferences. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID of the preference XML file. |
| `readAgain` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to re-read the default values. If false, this method sets the default values only if this method has never been called in the past (or if the [KEY_HAS_SET_DEFAULT_VALUES](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#KEY_HAS_SET_DEFAULT_VALUES:kotlin.String) in the default value shared preferences file is false). To attempt to set the default values again bypassing this check, set`readAgain`to true. Note: this will NOT reset preferences back to their default values. For that functionality, use [PreferenceManager.getDefaultSharedPreferences(Context)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getDefaultSharedPreferences(android.content.Context))and clear it followed by a call to this method with this parameter set to true. |
| --- | --- |

### setDefaultValues

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefaultValues(
    context: Context!, 
    sharedPreferencesName: String!, 
    sharedPreferencesMode: Int, 
    resId: Int, 
    readAgain: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Similar to [setDefaultValues(android.content.Context,int,boolean)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setDefaultValues(android.content.Context,%20kotlin.Int,%20kotlin.Boolean))but allows the client to provide the filename and mode of the shared preferences file.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The context of the shared preferences. |
| `sharedPreferencesName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A custom name for the shared preferences file. |
| `sharedPreferencesMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The file creation mode for the shared preferences file, such as [android.content.Context#MODE_PRIVATE](https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_PRIVATE:kotlin.Int) or [android.content.Context#MODE_PRIVATE](https://developer.android.com/reference/kotlin/android/content/Context.html#MODE_PRIVATE:kotlin.Int) |
| --- | --- |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID of the preference XML file. |
| `readAgain` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to re-read the default values. If false, this method will set the default values only if this method has never been called in the past (or if the [KEY_HAS_SET_DEFAULT_VALUES](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#KEY_HAS_SET_DEFAULT_VALUES:kotlin.String) in the default value shared preferences file is false). To attempt to set the default values again bypassing this check, set`readAgain`to true. Note: this will NOT reset preferences back to their default values. For that functionality, use [PreferenceManager.getDefaultSharedPreferences(Context)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#getDefaultSharedPreferences(android.content.Context))and clear it followed by a call to this method with this parameter set to true. |

**See Also**

- [#setDefaultValues(Context, int, boolean)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setDefaultValues(android.content.Context,%20kotlin.Int,%20kotlin.Boolean))
- [#setSharedPreferencesName(String)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setSharedPreferencesName(kotlin.String))
- [#setSharedPreferencesMode(int)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setSharedPreferencesMode(kotlin.Int)) 

### setPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferenceDataStore(dataStore: PreferenceDataStore!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) to be used by all Preferences associated with this manager that don't have a custom [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) assigned via [Preference.setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)). Also if the data store is set, the child preferences won't use [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) as long as they are assigned to this manager.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataStore` | [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)!:The [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) to be used by this manager. |

**See Also**

- [android.preference.Preference#setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)) 

### setSharedPreferencesMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedPreferencesMode(sharedPreferencesMode: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the mode of the SharedPreferences file that preferences managed by this will use.

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------|
| `sharedPreferencesMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The mode of the SharedPreferences file. |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSharedPreferences(kotlin.String,%20kotlin.Int)) 

### setSharedPreferencesName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedPreferencesName(sharedPreferencesName: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the name of the SharedPreferences file that preferences managed by this will use.

If custom [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) is set, this won't override its usage.

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `sharedPreferencesName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the SharedPreferences file. |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSharedPreferences(kotlin.String,%20kotlin.Int))
- [#setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setPreferenceDataStore(android.preference.PreferenceDataStore)) 

### setStorageDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStorageDefault(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the storage location used internally by this class to be the default provided by the hosting [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#). 

### setStorageDeviceProtected

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStorageDeviceProtected(): Unit
```

**Deprecated:** *Deprecated in Java.*

Explicitly set the storage location used internally by this class to be device-protected storage.

On devices with direct boot, data stored in this location is encrypted with a key tied to the physical device, and it can be accessed immediately after the device has booted successfully, both*before and after*the user has authenticated with their credentials (such as a lock pattern or PIN).

Because device-protected data is available without user authentication, you should carefully limit the data you store using this Context. For example, storing sensitive authentication tokens or passwords in the device-protected area is strongly discouraged. 
**See Also**

- [android.content.Context#createDeviceProtectedStorageContext()](https://developer.android.com/reference/kotlin/android/content/Context.html#createDeviceProtectedStorageContext())

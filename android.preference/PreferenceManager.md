# PreferenceManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceManager

Kotlin| [Java](../android/preference/PreferenceManager.md) 
| --- | --- |

```
open class PreferenceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.preference.PreferenceManager](../android/preference/PreferenceManager.md) |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Used to help create [Preference](../android/preference/Preference.md) hierarchies from activities or XML.

In most cases, clients should use [PreferenceActivity.addPreferencesFromIntent](../android/preference/PreferenceActivity.md))or [PreferenceActivity.addPreferencesFromResource(int)](../android/preference/PreferenceActivity.md)).

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnActivityDestroyListener](../android/preference/PreferenceManager.OnActivityDestroyListener.md) Interface definition for a class that will be called when the container's activity is destroyed. |
| abstract | [OnActivityResultListener](../android/preference/PreferenceManager.OnActivityResultListener.md) Interface definition for a class that will be called when the container's activity receives an activity result. |
| abstract | [OnActivityStopListener](../android/preference/PreferenceManager.OnActivityStopListener.md) Interface definition for a class that will be called when the container's activity is stopped. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY_HAS_SET_DEFAULT_VALUES](../android/preference/PreferenceManager.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [METADATA_KEY_PREFERENCES](../android/preference/PreferenceManager.md) The Activity meta-data key for its XML preference hierarchy. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PreferenceScreen](../android/preference/PreferenceScreen.md)! | [createPreferenceScreen](../android/preference/PreferenceManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` <br /> |
| open [Preference](../android/preference/Preference.md)? | [findPreference](../android/preference/PreferenceManager.md))`(`key:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Finds a [Preference](../android/preference/Preference.md) based on its key. |
| openstatic [SharedPreferences](../android/content/SharedPreferences.md)! | [getDefaultSharedPreferences](../android/preference/PreferenceManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Gets a [SharedPreferences](../android/content/SharedPreferences.md) instance that points to the default file that is used by the preference framework in the given context. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultSharedPreferencesName](../android/preference/PreferenceManager.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Returns the name used for storing default shared preferences. |
| open [PreferenceDataStore](../android/preference/PreferenceDataStore.md)? | [getPreferenceDataStore](../android/preference/PreferenceManager.md))`()` Returns the [PreferenceDataStore](../android/preference/PreferenceDataStore.md) associated with this manager or`null`if the default [android.content.SharedPreferences](../android/content/SharedPreferences.md) are used instead. |
| open [SharedPreferences](../android/content/SharedPreferences.md)! | [getSharedPreferences](../android/preference/PreferenceManager.md))`()` Gets a [SharedPreferences](../android/content/SharedPreferences.md) instance that preferences managed by this will use. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSharedPreferencesMode](../android/preference/PreferenceManager.md))`()` Returns the current mode of the SharedPreferences file that preferences managed by this will use. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSharedPreferencesName](../android/preference/PreferenceManager.md))`()` Returns the current name of the SharedPreferences file that preferences managed by this will use. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStorageDefault](../android/preference/PreferenceManager.md))`()` Indicates if the storage location used internally by this class is the default provided by the hosting [Context](../android/content/Context.md). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStorageDeviceProtected](../android/preference/PreferenceManager.md))`()` Indicates if the storage location used internally by this class is backed by device-protected storage. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValues](../android/preference/PreferenceManager.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readAgain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the default values from an XML preference file by reading the values defined by each [Preference](../android/preference/Preference.md) item's`android:defaultValue`attribute. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValues](../android/preference/PreferenceManager.md))`(`context:` ` [Context](../android/content/Context.md)!`, `sharedPreferencesName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `sharedPreferencesMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `readAgain:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Similar to [setDefaultValues(android.content.Context,int,boolean)](../android/preference/PreferenceManager.md))but allows the client to provide the filename and mode of the shared preferences file. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](../android/preference/PreferenceManager.md))`(`dataStore:` ` [PreferenceDataStore](../android/preference/PreferenceDataStore.md)!`)` Sets a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by all Preferences associated with this manager that don't have a custom [PreferenceDataStore](../android/preference/PreferenceDataStore.md) assigned via [Preference.setPreferenceDataStore(PreferenceDataStore)](../android/preference/Preference.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedPreferencesMode](../android/preference/PreferenceManager.md))`(`sharedPreferencesMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the mode of the SharedPreferences file that preferences managed by this will use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSharedPreferencesName](../android/preference/PreferenceManager.md))`(`sharedPreferencesName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of the SharedPreferences file that preferences managed by this will use. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStorageDefault](../android/preference/PreferenceManager.md))`()` Sets the storage location used internally by this class to be the default provided by the hosting [Context](../android/content/Context.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStorageDeviceProtected](../android/preference/PreferenceManager.md))`()` Explicitly set the storage location used internally by this class to be device-protected storage. |

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

Finds a [Preference](../android/preference/Preference.md) based on its key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the key of the preference to retrieve |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Preference](../android/preference/Preference.md)? | the [Preference](../android/preference/Preference.md) with the key, or`null` |

**See Also**

- [android.preference.PreferenceGroup#findPreference(CharSequence)](../android/preference/PreferenceGroup.md)) 

### getDefaultSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultSharedPreferences(context: Context!): SharedPreferences!
```

**Deprecated:** *Deprecated in Java.*

Gets a [SharedPreferences](../android/content/SharedPreferences.md) instance that points to the default file that is used by the preference framework in the given context.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context of the preferences whose values are wanted. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences](../android/content/SharedPreferences.md)! | A [SharedPreferences](../android/content/SharedPreferences.md) instance that can be used to retrieve and listen to values of the preferences. |

### getDefaultSharedPreferencesName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultSharedPreferencesName(context: Context!): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the name used for storing default shared preferences. 
**See Also**

- [#getDefaultSharedPreferences(Context)](../android/preference/PreferenceManager.md)) 

### getPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceDataStore(): PreferenceDataStore?
```

**Deprecated:** *Deprecated in Java.*

Returns the [PreferenceDataStore](../android/preference/PreferenceDataStore.md) associated with this manager or`null`if the default [android.content.SharedPreferences](../android/content/SharedPreferences.md) are used instead.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreferenceDataStore](../android/preference/PreferenceDataStore.md)? | The [PreferenceDataStore](../android/preference/PreferenceDataStore.md) associated with this manager or`null`if none. |

**See Also**

- [#setPreferenceDataStore(PreferenceDataStore)](../android/preference/PreferenceManager.md)) 

### getSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferences(): SharedPreferences!
```

**Deprecated:** *Deprecated in Java.*

Gets a [SharedPreferences](../android/content/SharedPreferences.md) instance that preferences managed by this will use.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences](../android/content/SharedPreferences.md)! | a [SharedPreferences](../android/content/SharedPreferences.md) instance pointing to the file that contains the values of preferences that are managed by this PreferenceManager. If a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) has been set, this method returns`null`. |

### getSharedPreferencesMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferencesMode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the current mode of the SharedPreferences file that preferences managed by this will use.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The mode that can be passed to [Context.getSharedPreferences(String, int)](../android/content/Context.md)). |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](../android/content/Context.md)) 

### getSharedPreferencesName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferencesName(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the current name of the SharedPreferences file that preferences managed by this will use.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The name that can be passed to [Context.getSharedPreferences(String, int)](../android/content/Context.md)). |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](../android/content/Context.md)) 

### isStorageDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isStorageDefault(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Indicates if the storage location used internally by this class is the default provided by the hosting [Context](../android/content/Context.md). 
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

Sets the default values from an XML preference file by reading the values defined by each [Preference](../android/preference/Preference.md) item's`android:defaultValue`attribute. This should be called by the application's main activity.

<br />

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context of the shared preferences. |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID of the preference XML file. |
| `readAgain` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to re-read the default values. If false, this method sets the default values only if this method has never been called in the past (or if the [KEY_HAS_SET_DEFAULT_VALUES](../android/preference/PreferenceManager.md) in the default value shared preferences file is false). To attempt to set the default values again bypassing this check, set`readAgain`to true. Note: this will NOT reset preferences back to their default values. For that functionality, use [PreferenceManager.getDefaultSharedPreferences(Context)](../android/preference/PreferenceManager.md))and clear it followed by a call to this method with this parameter set to true. |
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

Similar to [setDefaultValues(android.content.Context,int,boolean)](../android/preference/PreferenceManager.md))but allows the client to provide the filename and mode of the shared preferences file.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The context of the shared preferences. |
| `sharedPreferencesName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A custom name for the shared preferences file. |
| `sharedPreferencesMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The file creation mode for the shared preferences file, such as [android.content.Context#MODE_PRIVATE](../android/content/Context.md) or [android.content.Context#MODE_PRIVATE](../android/content/Context.md) |
| --- | --- |
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource ID of the preference XML file. |
| `readAgain` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to re-read the default values. If false, this method will set the default values only if this method has never been called in the past (or if the [KEY_HAS_SET_DEFAULT_VALUES](../android/preference/PreferenceManager.md) in the default value shared preferences file is false). To attempt to set the default values again bypassing this check, set`readAgain`to true. Note: this will NOT reset preferences back to their default values. For that functionality, use [PreferenceManager.getDefaultSharedPreferences(Context)](../android/preference/PreferenceManager.md))and clear it followed by a call to this method with this parameter set to true. |

**See Also**

- [#setDefaultValues(Context, int, boolean)](../android/preference/PreferenceManager.md))
- [#setSharedPreferencesName(String)](../android/preference/PreferenceManager.md))
- [#setSharedPreferencesMode(int)](../android/preference/PreferenceManager.md)) 

### setPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferenceDataStore(dataStore: PreferenceDataStore!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by all Preferences associated with this manager that don't have a custom [PreferenceDataStore](../android/preference/PreferenceDataStore.md) assigned via [Preference.setPreferenceDataStore(PreferenceDataStore)](../android/preference/Preference.md)). Also if the data store is set, the child preferences won't use [android.content.SharedPreferences](../android/content/SharedPreferences.md) as long as they are assigned to this manager.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataStore` | [PreferenceDataStore](../android/preference/PreferenceDataStore.md)!:The [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by this manager. |

**See Also**

- [android.preference.Preference#setPreferenceDataStore(PreferenceDataStore)](../android/preference/Preference.md)) 

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

- [android.content.Context#getSharedPreferences(String, int)](../android/content/Context.md)) 

### setSharedPreferencesName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSharedPreferencesName(sharedPreferencesName: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the name of the SharedPreferences file that preferences managed by this will use.

If custom [PreferenceDataStore](../android/preference/PreferenceDataStore.md) is set, this won't override its usage.

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------|
| `sharedPreferencesName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the SharedPreferences file. |

**See Also**

- [android.content.Context#getSharedPreferences(String, int)](../android/content/Context.md))
- [#setPreferenceDataStore(PreferenceDataStore)](../android/preference/PreferenceManager.md)) 

### setStorageDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStorageDefault(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the storage location used internally by this class to be the default provided by the hosting [Context](../android/content/Context.md). 

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

- [android.content.Context#createDeviceProtectedStorageContext()](../android/content/Context.md))

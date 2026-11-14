# LocaleConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocaleConfig

Kotlin| [Java](https://developer.android.com/reference/android/app/LocaleConfig "View this page in Java") 
| --- | --- |

```
open class LocaleConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#) |

The LocaleConfig of an application. There are two sources. One is from an XML resource file with an`<locale-config>`element and referenced in the manifest via`android:localeConfig`on`<application>`. The other is that the application dynamically provides an override version which is persisted in [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig)).

For more information about the LocaleConfig from an XML resource file, see [the section on per-app language preferences](https://developer.android.com/about/versions/13/features/app-languages#use-localeconfig).

## Summary

| XML attributes ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [`android:localeConfig`](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#attr_LocaleConfig) | An XML resource with the application's android. |
| [`android:name`](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#attr_LocaleConfig) | The IETF BCP47 language tag of the supported locale. |

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_NOT_SPECIFIED](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_NOT_SPECIFIED:kotlin.Int) No android:localeConfig tag on . |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_PARSING_FAILED:kotlin.Int) Malformed input in the XML file where the LocaleConfig was stored. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_SUCCESS:kotlin.Int) succeeded reading the LocaleConfig structure stored in an XML file. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_LOCALE](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#TAG_LOCALE:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TAG_LOCALE_CONFIG](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#TAG_LOCALE_CONFIG:kotlin.String) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#LocaleConfig(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Returns an override LocaleConfig if it has been set via [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig)). |
| [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#LocaleConfig(android.os.LocaleList))`(`locales:` ` [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)`)` Return the LocaleConfig with any sequence of locales combined into a [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#). |

| Public methods ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#describeContents())`()` <br /> |
| openstatic [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#) | [fromContextIgnoringOverride](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#fromContextIgnoringOverride(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`)` Returns a LocaleConfig from the application resources regardless of whether any LocaleConfig is overridden via [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig)). |
| open [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | [getDefaultLocale](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#getDefaultLocale())`()` Returns the locale the strings in values/strings. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatus](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#getStatus())`()` Get the status of reading the resource file where the LocaleConfig was stored. |
| open [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)? | [getSupportedLocales](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#getSupportedLocales())`()` Returns the locales supported by the specified application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## XML attributes

### android:localeConfig

```
android:localeConfig
```
An XML resource with the application's [android.app.LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#)

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:name

```
android:name
```
The [IETF BCP47 language tag](https://www.rfc-editor.org/rfc/bcp/bcp47.txt) of the supported locale. [android.app.LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#)

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

## Constants

### STATUS_NOT_SPECIFIED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_NOT_SPECIFIED: Int
```

No android:localeConfig tag on . 

 Value: 1

### STATUS_PARSING_FAILED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_PARSING_FAILED: Int
```

Malformed input in the XML file where the LocaleConfig was stored. 

 Value: 2

### STATUS_SUCCESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_SUCCESS: Int
```

succeeded reading the LocaleConfig structure stored in an XML file. 

 Value: 0

### TAG_LOCALE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_LOCALE: String
```  

 Value: "locale"

### TAG_LOCALE_CONFIG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAG_LOCALE_CONFIG: String
```  

 Value: "locale-config"

## Public constructors

### LocaleConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocaleConfig(context: Context)
```

Returns an override LocaleConfig if it has been set via [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig)). Otherwise, returns the LocaleConfig from the application resources.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the context of the application. This value cannot be`null`. |

**See Also**

- [android.content.Context#createPackageContext(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)) 

### LocaleConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LocaleConfig(locales: LocaleList)
```

Return the LocaleConfig with any sequence of locales combined into a [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#).

**Note:** Applications seeking to create an override LocaleConfig via [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig))should use this constructor to first create the LocaleConfig they intend the system to see as the override.

**Note:** The creation of this LocaleConfig does not automatically mean it will become the override config for an application. Any LocaleConfig desired to be the override must be passed into the [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig)), otherwise it will not persist or affect the system's understanding of app-supported resources.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locales` | [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#):the desired locales for a specified application This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### fromContextIgnoringOverride

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromContextIgnoringOverride(context: Context): LocaleConfig
```

Returns a LocaleConfig from the application resources regardless of whether any LocaleConfig is overridden via [LocaleManager.setOverrideLocaleConfig(LocaleConfig)](https://developer.android.com/reference/kotlin/android/app/LocaleManager#setOverrideLocaleConfig(android.app.LocaleConfig)).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the context of the application. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [LocaleConfig](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#) | This value cannot be`null`. |

**See Also**

- [android.content.Context#createPackageContext(String, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#createPackageContext(kotlin.String,%20kotlin.Int)) 

### getDefaultLocale

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultLocale(): Locale?
```

Returns the locale the strings in values/strings.xml (the default strings in the directory with no locale qualifier) are in if specified, otherwise null

| Return ||
|----------------------------------------------------------------------------------|----------------------------|
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | The default Locale or null |

### getStatus

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatus(): Int
```

Get the status of reading the resource file where the LocaleConfig was stored.

Distinguish "the application didn't provide the resource file" from "the application provided malformed input" if [getSupportedLocales()](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#getSupportedLocales())returns`null`.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `STATUS_SUCCESS`if the LocaleConfig structure existed in an XML file was successfully read, or`STATUS_NOT_SPECIFIED`if no android:localeConfig tag on pointing to an XML file that stores the LocaleConfig, or`STATUS_PARSING_FAILED`if the application provided malformed input for the LocaleConfig structure. Value is [android.app.LocaleConfig#STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_SUCCESS:kotlin.Int), [android.app.LocaleConfig#STATUS_NOT_SPECIFIED](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_NOT_SPECIFIED:kotlin.Int), or [android.app.LocaleConfig#STATUS_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_PARSING_FAILED:kotlin.Int) |

**See Also**

- [#STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_SUCCESS:kotlin.Int)
- [#STATUS_NOT_SPECIFIED](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_NOT_SPECIFIED:kotlin.Int)
- [#STATUS_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/app/LocaleConfig#STATUS_PARSING_FAILED:kotlin.Int) 

### getSupportedLocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSupportedLocales(): LocaleList?
```

Returns the locales supported by the specified application.

**Note:** The locale format should follow the [IETF BCP47 regular expression](https://www.rfc-editor.org/rfc/bcp/bcp47.txt)

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)? | the [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#) This value may be`null`. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LocaleConfig!>
```

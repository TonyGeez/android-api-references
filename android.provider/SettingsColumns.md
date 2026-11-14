# Contacts.SettingsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.SettingsColumns "View this page in Java") 
| --- | --- |

```
interface SettingsColumns
```

| [android.provider.Contacts.SettingsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns#) |

| Known Direct Subclasses [Contacts.Settings](https://developer.android.com/reference/kotlin/android/provider/Contacts.Settings) |--------------------------------------------------------------------------------------------------------|-------------------------------------| | [Contacts.Settings](https://developer.android.com/reference/kotlin/android/provider/Contacts.Settings) | The settings over all of the people | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the Settings table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns#KEY:kotlin.String) The key of this setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALUE](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns#VALUE:kotlin.String) The value of this setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_SYNC_ACCOUNT](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns#_SYNC_ACCOUNT:kotlin.String) The _SYNC_ACCOUNT to which this setting corresponds. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_SYNC_ACCOUNT_TYPE](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns#_SYNC_ACCOUNT_TYPE:kotlin.String) The _SYNC_ACCOUNT_TYPE to which this setting corresponds. |

## Constants

### KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The key of this setting.

Type: TEXT 

 Value: "key"

### VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALUE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The value of this setting.

Type: TEXT 

 Value: "value"

### _SYNC_ACCOUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val _SYNC_ACCOUNT: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The _SYNC_ACCOUNT to which this setting corresponds. This may be null.

Type: TEXT 

 Value: "_sync_account"

### _SYNC_ACCOUNT_TYPE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val _SYNC_ACCOUNT_TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The _SYNC_ACCOUNT_TYPE to which this setting corresponds. This may be null.

Type: TEXT 

 Value: "_sync_account_type"

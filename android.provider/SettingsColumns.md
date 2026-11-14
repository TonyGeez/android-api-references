# Contacts.SettingsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsColumns

Kotlin| [Java](../android/provider/Contacts.SettingsColumns.md) 
| --- | --- |

```
interface SettingsColumns
```

| [android.provider.Contacts.SettingsColumns](../android/provider/Contacts.SettingsColumns.md) |

| Known Direct Subclasses [Contacts.Settings](../android/provider/Contacts.Settings.md) |--------------------------------------------------------------------------------------------------------|-------------------------------------| | [Contacts.Settings](../android/provider/Contacts.Settings.md) | The settings over all of the people | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](ContactsContract.md)

Columns from the Settings table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEY](../android/provider/Contacts.SettingsColumns.md) The key of this setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALUE](../android/provider/Contacts.SettingsColumns.md) The value of this setting. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_SYNC_ACCOUNT](../android/provider/Contacts.SettingsColumns.md) The _SYNC_ACCOUNT to which this setting corresponds. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_SYNC_ACCOUNT_TYPE](../android/provider/Contacts.SettingsColumns.md) The _SYNC_ACCOUNT_TYPE to which this setting corresponds. |

## Constants

### KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEY: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The key of this setting.

Type: TEXT 

 Value: "key"

### VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALUE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The value of this setting.

Type: TEXT 

 Value: "value"

### _SYNC_ACCOUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val _SYNC_ACCOUNT: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The _SYNC_ACCOUNT to which this setting corresponds. This may be null.

Type: TEXT 

 Value: "_sync_account"

### _SYNC_ACCOUNT_TYPE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val _SYNC_ACCOUNT_TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The _SYNC_ACCOUNT_TYPE to which this setting corresponds. This may be null.

Type: TEXT 

 Value: "_sync_account_type"

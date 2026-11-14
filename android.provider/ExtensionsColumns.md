# Contacts.ExtensionsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtensionsColumns

Kotlin| [Java](../android/provider/Contacts.ExtensionsColumns.md) 
| --- | --- |

```
interface ExtensionsColumns
```

| [android.provider.Contacts.ExtensionsColumns](../android/provider/Contacts.ExtensionsColumns.md) |

| Known Direct Subclasses [Contacts.Extensions](../android/provider/Contacts.Extensions.md), [Contacts.People.Extensions](../android/provider/Contacts.People.Extensions.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------| | [Contacts.Extensions](../android/provider/Contacts.Extensions.md) | The extensions for a person | | [Contacts.People.Extensions](../android/provider/Contacts.People.Extensions.md) | The extensions for a person | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](ContactsContract.md)

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](../android/provider/Contacts.ExtensionsColumns.md) The name of this extension. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALUE](../android/provider/Contacts.ExtensionsColumns.md) The value of this extension. |

## Constants

### NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The name of this extension. May not be null. There may be at most one row for each name.

Type: TEXT 

 Value: "name"

### VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALUE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The value of this extension. May not be null.

Type: TEXT 

 Value: "value"

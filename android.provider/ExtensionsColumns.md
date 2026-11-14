# Contacts.ExtensionsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExtensionsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.ExtensionsColumns "View this page in Java") 

```
interface ExtensionsColumns
```

| [android.provider.Contacts.ExtensionsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.ExtensionsColumns#) |

| Known Direct Subclasses [Contacts.Extensions](https://developer.android.com/reference/kotlin/android/provider/Contacts.Extensions), [Contacts.People.Extensions](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.Extensions) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------| | [Contacts.Extensions](https://developer.android.com/reference/kotlin/android/provider/Contacts.Extensions) | The extensions for a person | | [Contacts.People.Extensions](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.Extensions) | The extensions for a person | |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](https://developer.android.com/reference/kotlin/android/provider/Contacts.ExtensionsColumns#NAME:kotlin.String) The name of this extension. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [VALUE](https://developer.android.com/reference/kotlin/android/provider/Contacts.ExtensionsColumns#VALUE:kotlin.String) The value of this extension. |

## Constants

### NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The name of this extension. May not be null. There may be at most one row for each name.

Type: TEXT 

 Value: "name"

### VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VALUE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The value of this extension. May not be null.

Type: TEXT 

 Value: "value"

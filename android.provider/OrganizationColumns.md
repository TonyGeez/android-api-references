# Contacts.OrganizationColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OrganizationColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.OrganizationColumns "View this page in Java") 

```
interface OrganizationColumns
```

| [android.provider.Contacts.OrganizationColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#) |

| Known Direct Subclasses [Contacts.Organizations](https://developer.android.com/reference/kotlin/android/provider/Contacts.Organizations) |------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------| | [Contacts.Organizations](https://developer.android.com/reference/kotlin/android/provider/Contacts.Organizations) | A sub directory of a single person that contains all of their Phones. | |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the Organizations table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COMPANY](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#COMPANY:kotlin.String) The name of the company for this organization. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ISPRIMARY](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#ISPRIMARY:kotlin.String) Whether this is the primary organization |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#LABEL:kotlin.String) The user provided label, only used if TYPE is TYPE_CUSTOM. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PERSON_ID](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#PERSON_ID:kotlin.String) The person this organization is tied to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TITLE](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#TITLE:kotlin.String) The title within this organization. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#TYPE:kotlin.String) The type of the organizations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUSTOM](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#TYPE_CUSTOM:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#TYPE_OTHER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WORK](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns#TYPE_WORK:kotlin.Int) <br /> |

## Constants

### COMPANY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPANY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The name of the company for this organization.

Type: TEXT 

 Value: "company"

### ISPRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISPRIMARY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Whether this is the primary organization

Type: INTEGER (if set, non-0 means true) 

 Value: "isprimary"

### LABEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The user provided label, only used if TYPE is TYPE_CUSTOM.

Type: TEXT 

 Value: "label"

### PERSON_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERSON_ID: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The person this organization is tied to.

Type: TEXT 

 Value: "person"

### TITLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TITLE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The title within this organization.

Type: TEXT 

 Value: "title"

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The type of the organizations.

Type: INTEGER (one of the constants below) 

 Value: "type"

### TYPE_CUSTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUSTOM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 0

### TYPE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 2

### TYPE_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 1

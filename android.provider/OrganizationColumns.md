# Contacts.OrganizationColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OrganizationColumns

Kotlin| [Java](../android/provider/Contacts.OrganizationColumns.md) 
| --- | --- |

```
interface OrganizationColumns
```

| [android.provider.Contacts.OrganizationColumns](../android/provider/Contacts.OrganizationColumns.md) |

| Known Direct Subclasses [Contacts.Organizations](../android/provider/Contacts.Organizations.md) |------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------| | [Contacts.Organizations](../android/provider/Contacts.Organizations.md) | A sub directory of a single person that contains all of their Phones. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](ContactsContract.md)

Columns from the Organizations table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [COMPANY](../android/provider/Contacts.OrganizationColumns.md) The name of the company for this organization. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ISPRIMARY](../android/provider/Contacts.OrganizationColumns.md) Whether this is the primary organization |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](../android/provider/Contacts.OrganizationColumns.md) The user provided label, only used if TYPE is TYPE_CUSTOM. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PERSON_ID](../android/provider/Contacts.OrganizationColumns.md) The person this organization is tied to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TITLE](../android/provider/Contacts.OrganizationColumns.md) The title within this organization. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](../android/provider/Contacts.OrganizationColumns.md) The type of the organizations. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUSTOM](../android/provider/Contacts.OrganizationColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](../android/provider/Contacts.OrganizationColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WORK](../android/provider/Contacts.OrganizationColumns.md) <br /> |
| --- | --- |

## Constants

### COMPANY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPANY: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The name of the company for this organization.

Type: TEXT 

 Value: "company"

### ISPRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISPRIMARY: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

Whether this is the primary organization

Type: INTEGER (if set, non-0 means true) 

 Value: "isprimary"

### LABEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The user provided label, only used if TYPE is TYPE_CUSTOM.

Type: TEXT 

 Value: "label"

### PERSON_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERSON_ID: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The person this organization is tied to.

Type: TEXT 

 Value: "person"

### TITLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TITLE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The title within this organization.

Type: TEXT 

 Value: "title"

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The type of the organizations.

Type: INTEGER (one of the constants below) 

 Value: "type"

### TYPE_CUSTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUSTOM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 0

### TYPE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 2

### TYPE_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 1

# Contacts.PhonesColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhonesColumns

Kotlin| [Java](../android/provider/Contacts.PhonesColumns.md) 
| --- | --- |

```
interface PhonesColumns
```

| [android.provider.Contacts.PhonesColumns](../android/provider/Contacts.PhonesColumns.md) |

| Known Direct Subclasses [Contacts.People](../android/provider/Contacts.People.md), [Contacts.People.Phones](../android/provider/Contacts.People.Phones.md), [Contacts.Phones](../android/provider/Contacts.Phones.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [Contacts.People](../android/provider/Contacts.People.md) | This table contains people. | | [Contacts.People.Phones](../android/provider/Contacts.People.Phones.md) | A sub directory of a single person that contains all of their Phones. | | [Contacts.Phones](../android/provider/Contacts.Phones.md) | This table stores phone numbers and a reference to the person that the contact method belongs to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](ContactsContract.md)

Columns from the Phones table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ISPRIMARY](../android/provider/Contacts.PhonesColumns.md) Whether this is the primary phone number |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](../android/provider/Contacts.PhonesColumns.md) The user provided label for the phone number, only used if TYPE is TYPE_CUSTOM. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMBER](../android/provider/Contacts.PhonesColumns.md) The phone number as the user entered it. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMBER_KEY](../android/provider/Contacts.PhonesColumns.md) The normalized phone number |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](../android/provider/Contacts.PhonesColumns.md) The type of the the phone number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUSTOM](../android/provider/Contacts.PhonesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FAX_HOME](../android/provider/Contacts.PhonesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FAX_WORK](../android/provider/Contacts.PhonesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HOME](../android/provider/Contacts.PhonesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MOBILE](../android/provider/Contacts.PhonesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](../android/provider/Contacts.PhonesColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PAGER](../android/provider/Contacts.PhonesColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WORK](../android/provider/Contacts.PhonesColumns.md) <br /> |

## Constants

### ISPRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISPRIMARY: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

Whether this is the primary phone number

Type: INTEGER (if set, non-0 means true) 

 Value: "isprimary"

### LABEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The user provided label for the phone number, only used if TYPE is TYPE_CUSTOM.

Type: TEXT 

 Value: "label"

### NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBER: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The phone number as the user entered it.

Type: TEXT 

 Value: "number"

### NUMBER_KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBER_KEY: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The normalized phone number

Type: TEXT 

 Value: "number_key"

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The type of the the phone number.

Type: INTEGER (one of the constants below) 

 Value: "type"

### TYPE_CUSTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUSTOM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 0

### TYPE_FAX_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FAX_HOME: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 5

### TYPE_FAX_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FAX_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 4

### TYPE_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HOME: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 1

### TYPE_MOBILE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MOBILE: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 2

### TYPE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 7

### TYPE_PAGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_PAGER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 6

### TYPE_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)* 

 Value: 3

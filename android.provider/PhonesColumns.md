# Contacts.PhonesColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhonesColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.PhonesColumns "View this page in Java") 

```
interface PhonesColumns
```

| [android.provider.Contacts.PhonesColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#) |

| Known Direct Subclasses [Contacts.People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People), [Contacts.People.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.Phones), [Contacts.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.Phones) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [Contacts.People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People) | This table contains people. | | [Contacts.People.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.Phones) | A sub directory of a single person that contains all of their Phones. | | [Contacts.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.Phones) | This table stores phone numbers and a reference to the person that the contact method belongs to. | |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the Phones table that other columns join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ISPRIMARY](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#ISPRIMARY:kotlin.String) Whether this is the primary phone number |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#LABEL:kotlin.String) The user provided label for the phone number, only used if TYPE is TYPE_CUSTOM. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMBER](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#NUMBER:kotlin.String) The phone number as the user entered it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMBER_KEY](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#NUMBER_KEY:kotlin.String) The normalized phone number |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE:kotlin.String) The type of the the phone number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUSTOM](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_CUSTOM:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FAX_HOME](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_FAX_HOME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FAX_WORK](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_FAX_WORK:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HOME](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_HOME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MOBILE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_MOBILE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_OTHER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_PAGER](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_PAGER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WORK](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns#TYPE_WORK:kotlin.Int) <br /> |

## Constants

### ISPRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISPRIMARY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Whether this is the primary phone number

Type: INTEGER (if set, non-0 means true) 

 Value: "isprimary"

### LABEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The user provided label for the phone number, only used if TYPE is TYPE_CUSTOM.

Type: TEXT 

 Value: "label"

### NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBER: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The phone number as the user entered it.

Type: TEXT 

 Value: "number"

### NUMBER_KEY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBER_KEY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The normalized phone number

Type: TEXT 

 Value: "number_key"

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The type of the the phone number.

Type: INTEGER (one of the constants below) 

 Value: "type"

### TYPE_CUSTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUSTOM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 0

### TYPE_FAX_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FAX_HOME: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 5

### TYPE_FAX_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FAX_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 4

### TYPE_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HOME: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 1

### TYPE_MOBILE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MOBILE: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 2

### TYPE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 7

### TYPE_PAGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_PAGER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 6

### TYPE_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 3

# Contacts.ContactMethodsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactMethodsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.ContactMethodsColumns "View this page in Java") 

```
interface ContactMethodsColumns
```

| [android.provider.Contacts.ContactMethodsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#) |

| Known Direct Subclasses [Contacts.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods), [Contacts.People.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.ContactMethods) |----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [Contacts.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods) | This table stores all non-phone contact methods and a reference to the person that the contact method belongs to. | | [Contacts.People.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.ContactMethods) | A subdirectory of a single person that contains all of their ContactMethods. | |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the ContactMethods table that other tables join into themseleves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUX_DATA](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#AUX_DATA:kotlin.String) Auxiliary data for the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#DATA:kotlin.String) The data for the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ISPRIMARY](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#ISPRIMARY:kotlin.String) Whether this is the primary organization |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KIND](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#KIND:kotlin.String) The kind of the the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#LABEL:kotlin.String) The user defined label for the the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#TYPE:kotlin.String) The type of the contact method, must be one of the types below. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUSTOM](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#TYPE_CUSTOM:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HOME](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#TYPE_HOME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#TYPE_OTHER:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WORK](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns#TYPE_WORK:kotlin.Int) <br /> |

## Constants

### AUX_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUX_DATA: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Auxiliary data for the contact method.

Type: TEXT 

 Value: "aux_data"

### DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The data for the contact method.

Type: TEXT 

 Value: "data"

### ISPRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISPRIMARY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Whether this is the primary organization

Type: INTEGER (if set, non-0 means true) 

 Value: "isprimary"

### KIND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The kind of the the contact method. For example, email address, postal address, etc.

Type: INTEGER (one of the values below) 

 Value: "kind"

### LABEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The user defined label for the the contact method.

Type: TEXT 

 Value: "label"

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The type of the contact method, must be one of the types below.

Type: INTEGER (one of the values below) 

 Value: "type"

### TYPE_CUSTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUSTOM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 0

### TYPE_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HOME: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 1

### TYPE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 3

### TYPE_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: 2

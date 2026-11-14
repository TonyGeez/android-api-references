# Contacts.ContactMethodsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactMethodsColumns

Kotlin| [Java](../android/provider/Contacts.ContactMethodsColumns.md) 
| --- | --- |

```
interface ContactMethodsColumns
```

| [android.provider.Contacts.ContactMethodsColumns](../android/provider/Contacts.ContactMethodsColumns.md) |

| Known Direct Subclasses [Contacts.ContactMethods](../android/provider/Contacts.ContactMethods.md), [Contacts.People.ContactMethods](../android/provider/Contacts.People.ContactMethods.md) |----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [Contacts.ContactMethods](../android/provider/Contacts.ContactMethods.md) | This table stores all non-phone contact methods and a reference to the person that the contact method belongs to. | | [Contacts.People.ContactMethods](../android/provider/Contacts.People.ContactMethods.md) | A subdirectory of a single person that contains all of their ContactMethods. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](../android/provider/ContactsContract.md)

Columns from the ContactMethods table that other tables join into themseleves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUX_DATA](../android/provider/Contacts.ContactMethodsColumns.md) Auxiliary data for the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA](../android/provider/Contacts.ContactMethodsColumns.md) The data for the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ISPRIMARY](../android/provider/Contacts.ContactMethodsColumns.md) Whether this is the primary organization |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KIND](../android/provider/Contacts.ContactMethodsColumns.md) The kind of the the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](../android/provider/Contacts.ContactMethodsColumns.md) The user defined label for the the contact method. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](../android/provider/Contacts.ContactMethodsColumns.md) The type of the contact method, must be one of the types below. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CUSTOM](../android/provider/Contacts.ContactMethodsColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_HOME](../android/provider/Contacts.ContactMethodsColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_OTHER](../android/provider/Contacts.ContactMethodsColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_WORK](../android/provider/Contacts.ContactMethodsColumns.md) <br /> |

## Constants

### AUX_DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUX_DATA: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Auxiliary data for the contact method.

Type: TEXT 

 Value: "aux_data"

### DATA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The data for the contact method.

Type: TEXT 

 Value: "data"

### ISPRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISPRIMARY: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Whether this is the primary organization

Type: INTEGER (if set, non-0 means true) 

 Value: "isprimary"

### KIND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The kind of the the contact method. For example, email address, postal address, etc.

Type: INTEGER (one of the values below) 

 Value: "kind"

### LABEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The user defined label for the the contact method.

Type: TEXT 

 Value: "label"

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The type of the contact method, must be one of the types below.

Type: INTEGER (one of the values below) 

 Value: "type"

### TYPE_CUSTOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CUSTOM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)* 

 Value: 0

### TYPE_HOME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_HOME: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)* 

 Value: 1

### TYPE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_OTHER: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)* 

 Value: 3

### TYPE_WORK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_WORK: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)* 

 Value: 2

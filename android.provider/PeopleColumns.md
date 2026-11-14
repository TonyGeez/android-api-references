# Contacts.PeopleColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeopleColumns

Kotlin| [Java](../android/provider/Contacts.PeopleColumns.md) 
| --- | --- |

```
interface PeopleColumns
```

| [android.provider.Contacts.PeopleColumns](../android/provider/Contacts.PeopleColumns.md) |

| Known Direct Subclasses [Contacts.ContactMethods](../android/provider/Contacts.ContactMethods.md), [Contacts.People](../android/provider/Contacts.People.md), [Contacts.People.ContactMethods](../android/provider/Contacts.People.ContactMethods.md), [Contacts.People.Phones](../android/provider/Contacts.People.Phones.md), [Contacts.Phones](../android/provider/Contacts.Phones.md) |----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [Contacts.ContactMethods](../android/provider/Contacts.ContactMethods.md) | This table stores all non-phone contact methods and a reference to the person that the contact method belongs to. | | [Contacts.People](../android/provider/Contacts.People.md) | This table contains people. | | [Contacts.People.ContactMethods](../android/provider/Contacts.People.ContactMethods.md) | A subdirectory of a single person that contains all of their ContactMethods. | | [Contacts.People.Phones](../android/provider/Contacts.People.Phones.md) | A sub directory of a single person that contains all of their Phones. | | [Contacts.Phones](../android/provider/Contacts.Phones.md) | This table stores phone numbers and a reference to the person that the contact method belongs to. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](ContactsContract.md)

Columns from the People table that other tables join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CUSTOM_RINGTONE](../android/provider/Contacts.PeopleColumns.md) A custom ringtone associated with a person. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME](../android/provider/Contacts.PeopleColumns.md) The display name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_TIME_CONTACTED](../android/provider/Contacts.PeopleColumns.md) The last time a person was contacted. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](../android/provider/Contacts.PeopleColumns.md) The person's name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NOTES](../android/provider/Contacts.PeopleColumns.md) Notes about the person. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHONETIC_NAME](../android/provider/Contacts.PeopleColumns.md) Phonetic equivalent of the person's name, in a locale-dependent character set (e.g. hiragana for Japanese). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_VERSION](../android/provider/Contacts.PeopleColumns.md) The server version of the photo |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEND_TO_VOICEMAIL](../android/provider/Contacts.PeopleColumns.md) Whether the person should always be sent to voicemail. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STARRED](../android/provider/Contacts.PeopleColumns.md) Is the contact starred? |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TIMES_CONTACTED](../android/provider/Contacts.PeopleColumns.md) The number of times a person has been contacted |

## Constants

### CUSTOM_RINGTONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUSTOM_RINGTONE: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

A custom ringtone associated with a person. Not always present.

Type: TEXT (URI to the ringtone) 

 Value: "custom_ringtone"

### DISPLAY_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The display name. If name is not null name, else if number is not null number, else if email is not null email.

Type: TEXT 

 Value: "display_name"

### LAST_TIME_CONTACTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAST_TIME_CONTACTED: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The last time a person was contacted.

Type: INTEGER 

 Value: "last_time_contacted"

### NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The person's name.

Type: TEXT 

 Value: "name"

### NOTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTES: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

Notes about the person.

Type: TEXT 

 Value: "notes"

### PHONETIC_NAME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONETIC_NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

Phonetic equivalent of the person's name, in a locale-dependent character set (e.g. hiragana for Japanese). Used for pronunciation and/or collation in some languages.

Type: TEXT 

 Value: "phonetic_name"

### PHOTO_VERSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_VERSION: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The server version of the photo

Type: TEXT (the version number portion of the photo URI) 

 Value: "photo_version"

### SEND_TO_VOICEMAIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEND_TO_VOICEMAIL: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

Whether the person should always be sent to voicemail. Not always present.

Type: INTEGER (0 for false, 1 for true) 

 Value: "send_to_voicemail"

### STARRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STARRED: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

Is the contact starred?

Type: INTEGER (boolean) 

 Value: "starred"

### TIMES_CONTACTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMES_CONTACTED: String
```

**Deprecated:** *see [android.provider.ContactsContract](ContactsContract.md)*

The number of times a person has been contacted

Type: INTEGER 

 Value: "times_contacted"

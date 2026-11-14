# Contacts.PeopleColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeopleColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.PeopleColumns "View this page in Java") 

```
interface PeopleColumns
```

| [android.provider.Contacts.PeopleColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#) |

| Known Direct Subclasses [Contacts.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods), [Contacts.People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People), [Contacts.People.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.ContactMethods), [Contacts.People.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.Phones), [Contacts.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.Phones) |----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [Contacts.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods) | This table stores all non-phone contact methods and a reference to the person that the contact method belongs to. | | [Contacts.People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People) | This table contains people. | | [Contacts.People.ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.ContactMethods) | A subdirectory of a single person that contains all of their ContactMethods. | | [Contacts.People.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.People.Phones) | A sub directory of a single person that contains all of their Phones. | | [Contacts.Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.Phones) | This table stores phone numbers and a reference to the person that the contact method belongs to. | |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the People table that other tables join into themselves.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CUSTOM_RINGTONE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#CUSTOM_RINGTONE:kotlin.String) A custom ringtone associated with a person. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#DISPLAY_NAME:kotlin.String) The display name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LAST_TIME_CONTACTED](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#LAST_TIME_CONTACTED:kotlin.String) The last time a person was contacted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#NAME:kotlin.String) The person's name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NOTES](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#NOTES:kotlin.String) Notes about the person. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHONETIC_NAME](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#PHONETIC_NAME:kotlin.String) Phonetic equivalent of the person's name, in a locale-dependent character set (e.g. hiragana for Japanese). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_VERSION](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#PHOTO_VERSION:kotlin.String) The server version of the photo |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SEND_TO_VOICEMAIL](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#SEND_TO_VOICEMAIL:kotlin.String) Whether the person should always be sent to voicemail. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STARRED](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#STARRED:kotlin.String) Is the contact starred? |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TIMES_CONTACTED](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns#TIMES_CONTACTED:kotlin.String) The number of times a person has been contacted |

## Constants

### CUSTOM_RINGTONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CUSTOM_RINGTONE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

A custom ringtone associated with a person. Not always present.

Type: TEXT (URI to the ringtone) 

 Value: "custom_ringtone"

### DISPLAY_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DISPLAY_NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The display name. If name is not null name, else if number is not null number, else if email is not null email.

Type: TEXT 

 Value: "display_name"

### LAST_TIME_CONTACTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LAST_TIME_CONTACTED: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The last time a person was contacted.

Type: INTEGER 

 Value: "last_time_contacted"

### NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The person's name.

Type: TEXT 

 Value: "name"

### NOTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTES: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Notes about the person.

Type: TEXT 

 Value: "notes"

### PHONETIC_NAME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONETIC_NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Phonetic equivalent of the person's name, in a locale-dependent character set (e.g. hiragana for Japanese). Used for pronunciation and/or collation in some languages.

Type: TEXT 

 Value: "phonetic_name"

### PHOTO_VERSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_VERSION: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The server version of the photo

Type: TEXT (the version number portion of the photo URI) 

 Value: "photo_version"

### SEND_TO_VOICEMAIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEND_TO_VOICEMAIL: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Whether the person should always be sent to voicemail. Not always present.

Type: INTEGER (0 for false, 1 for true) 

 Value: "send_to_voicemail"

### STARRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STARRED: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Is the contact starred?

Type: INTEGER (boolean) 

 Value: "starred"

### TIMES_CONTACTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TIMES_CONTACTED: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The number of times a person has been contacted

Type: INTEGER 

 Value: "times_contacted"

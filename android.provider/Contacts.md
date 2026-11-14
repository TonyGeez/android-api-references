# Contacts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Contacts

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts "View this page in Java") 

```
open class Contacts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.Contacts](https://developer.android.com/reference/kotlin/android/provider/Contacts#) |

| **This class was deprecated in API level 5.**
|
| The APIs have been superseded by [ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract). The newer APIs allow access multiple accounts and support aggregation of similar contacts. These APIs continue to work but will only return data for the first Google account created, which matches the original behavior.

The Contacts provider stores all information about contacts.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ContactMethods](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods) This table stores all non-phone contact methods and a reference to the person that the contact method belongs to. |
| abstract | [ContactMethodsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethodsColumns) Columns from the ContactMethods table that other tables join into themseleves. |
| | [Extensions](https://developer.android.com/reference/kotlin/android/provider/Contacts.Extensions) The extensions for a person |
| abstract | [ExtensionsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.ExtensionsColumns) <br /> |
| | [GroupMembership](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupMembership) <br /> |
| | [Groups](https://developer.android.com/reference/kotlin/android/provider/Contacts.Groups) This table contains the groups for an account. |
| abstract | [GroupsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns) Columns from the groups table. |
| | [Intents](https://developer.android.com/reference/kotlin/android/provider/Contacts.Intents) Contains helper classes used to create or manage [Intents](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that involve contacts. |
| abstract | [OrganizationColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.OrganizationColumns) Columns from the Organizations table that other columns join into themselves. |
| | [Organizations](https://developer.android.com/reference/kotlin/android/provider/Contacts.Organizations) A sub directory of a single person that contains all of their Phones. |
| | [People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People) This table contains people. |
| abstract | [PeopleColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PeopleColumns) Columns from the People table that other tables join into themselves. |
| | [Phones](https://developer.android.com/reference/kotlin/android/provider/Contacts.Phones) This table stores phone numbers and a reference to the person that the contact method belongs to. |
| abstract | [PhonesColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhonesColumns) Columns from the Phones table that other columns join into themselves. |
| | [Photos](https://developer.android.com/reference/kotlin/android/provider/Contacts.Photos) The photos over all of the people |
| abstract | [PhotosColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PhotosColumns) Columns from the Photos table that other columns join into themselves. |
| abstract | [PresenceColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns) The IM presence columns with some contacts specific columns mixed in. |
| | [Settings](https://developer.android.com/reference/kotlin/android/provider/Contacts.Settings) The settings over all of the people |
| abstract | [SettingsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.SettingsColumns) Columns from the Settings table that other columns join into themselves. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/Contacts#AUTHORITY:kotlin.String) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_EMAIL](https://developer.android.com/reference/kotlin/android/provider/Contacts#KIND_EMAIL:kotlin.Int) Signifies an email address row that is stored in the ContactMethods table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_IM](https://developer.android.com/reference/kotlin/android/provider/Contacts#KIND_IM:kotlin.Int) Signifies an IM address row that is stored in the ContactMethods table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_ORGANIZATION](https://developer.android.com/reference/kotlin/android/provider/Contacts#KIND_ORGANIZATION:kotlin.Int) Signifies an Organization row that is stored in the Organizations table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_PHONE](https://developer.android.com/reference/kotlin/android/provider/Contacts#KIND_PHONE:kotlin.Int) Signifies a Phone row that is stored in the Phones table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_POSTAL](https://developer.android.com/reference/kotlin/android/provider/Contacts#KIND_POSTAL:kotlin.Int) Signifies a postal address row that is stored in the ContactMethods table |

| Properties ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [CONTENT_URI](https://developer.android.com/reference/kotlin/android/provider/Contacts#CONTENT_URI:android.net.Uri) The content:// style URL for this provider |

## Constants

### AUTHORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)* 

 Value: "contacts"

### KIND_EMAIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_EMAIL: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Signifies an email address row that is stored in the ContactMethods table 

 Value: 1

### KIND_IM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_IM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Signifies an IM address row that is stored in the ContactMethods table 

 Value: 3

### KIND_ORGANIZATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_ORGANIZATION: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Signifies an Organization row that is stored in the Organizations table 

 Value: 4

### KIND_PHONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_PHONE: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Signifies a Phone row that is stored in the Phones table 

 Value: 5

### KIND_POSTAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_POSTAL: Int
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Signifies a postal address row that is stored in the ContactMethods table 

 Value: 2

## Properties

### CONTENT_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_URI: Uri!
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The content:// style URL for this provider

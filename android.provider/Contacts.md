# Contacts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Contacts

Kotlin| [Java](../android/provider/Contacts.md) 
| --- | --- |

```
open class Contacts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.Contacts](../android/provider/Contacts.md) |

| **This class was deprecated in API level 5.**
|
| The APIs have been superseded by [ContactsContract](../android/provider/ContactsContract.md). The newer APIs allow access multiple accounts and support aggregation of similar contacts. These APIs continue to work but will only return data for the first Google account created, which matches the original behavior.

The Contacts provider stores all information about contacts.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [ContactMethods](../android/provider/Contacts.ContactMethods.md) This table stores all non-phone contact methods and a reference to the person that the contact method belongs to. |
| abstract | [ContactMethodsColumns](../android/provider/Contacts.ContactMethodsColumns.md) Columns from the ContactMethods table that other tables join into themseleves. |
| | [Extensions](../android/provider/Contacts.Extensions.md) The extensions for a person |
| --- | --- |
| abstract | [ExtensionsColumns](../android/provider/Contacts.ExtensionsColumns.md) <br /> |
| | [GroupMembership](../android/provider/Contacts.GroupMembership.md) <br /> |
| | [Groups](../android/provider/Contacts.Groups.md) This table contains the groups for an account. |
| --- | --- |
| abstract | [GroupsColumns](../android/provider/Contacts.GroupsColumns.md) Columns from the groups table. |
| | [Intents](../android/provider/Contacts.Intents.md) Contains helper classes used to create or manage [Intents](../android/content/Intent.md) that involve contacts. |
| abstract | [OrganizationColumns](../android/provider/Contacts.OrganizationColumns.md) Columns from the Organizations table that other columns join into themselves. |
| --- | --- |
| | [Organizations](../android/provider/Contacts.Organizations.md) A sub directory of a single person that contains all of their Phones. |
| | [People](../android/provider/Contacts.People.md) This table contains people. |
| abstract | [PeopleColumns](../android/provider/Contacts.PeopleColumns.md) Columns from the People table that other tables join into themselves. |
| --- | --- |
| | [Phones](../android/provider/Contacts.Phones.md) This table stores phone numbers and a reference to the person that the contact method belongs to. |
| abstract | [PhonesColumns](../android/provider/Contacts.PhonesColumns.md) Columns from the Phones table that other columns join into themselves. |
| | [Photos](../android/provider/Contacts.Photos.md) The photos over all of the people |
| --- | --- |
| abstract | [PhotosColumns](../android/provider/Contacts.PhotosColumns.md) Columns from the Photos table that other columns join into themselves. |
| abstract | [PresenceColumns](../android/provider/Contacts.PresenceColumns.md) The IM presence columns with some contacts specific columns mixed in. |
| | [Settings](../android/provider/Contacts.Settings.md) The settings over all of the people |
| --- | --- |
| abstract | [SettingsColumns](../android/provider/Contacts.SettingsColumns.md) Columns from the Settings table that other columns join into themselves. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](../android/provider/Contacts.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_EMAIL](../android/provider/Contacts.md) Signifies an email address row that is stored in the ContactMethods table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_IM](../android/provider/Contacts.md) Signifies an IM address row that is stored in the ContactMethods table |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_ORGANIZATION](../android/provider/Contacts.md) Signifies an Organization row that is stored in the Organizations table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_PHONE](../android/provider/Contacts.md) Signifies a Phone row that is stored in the Phones table |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_POSTAL](../android/provider/Contacts.md) Signifies a postal address row that is stored in the ContactMethods table |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](../android/net/Uri.md)! | [CONTENT_URI](../android/provider/Contacts.md) The content:// style URL for this provider |

## Constants

### AUTHORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)* 

 Value: "contacts"

### KIND_EMAIL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_EMAIL: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Signifies an email address row that is stored in the ContactMethods table 

 Value: 1

### KIND_IM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_IM: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Signifies an IM address row that is stored in the ContactMethods table 

 Value: 3

### KIND_ORGANIZATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_ORGANIZATION: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Signifies an Organization row that is stored in the Organizations table 

 Value: 4

### KIND_PHONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_PHONE: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Signifies a Phone row that is stored in the Phones table 

 Value: 5

### KIND_POSTAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_POSTAL: Int
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Signifies a postal address row that is stored in the ContactMethods table 

 Value: 2

## Properties

### CONTENT_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_URI: Uri!
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The content:// style URL for this provider

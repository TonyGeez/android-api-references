# ContactsContract.DeletedContactsColumns

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeletedContactsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.DeletedContactsColumns "View this page in Java") 

```
protected interface DeletedContactsColumns
```

| [android.provider.ContactsContract.DeletedContactsColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContactsColumns#) |

| Known Direct Subclasses [ContactsContract.DeletedContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContacts) |--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------| | [ContactsContract.DeletedContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContacts) | Constants for the deleted contact table. | |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_DELETED_TIMESTAMP](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContactsColumns#CONTACT_DELETED_TIMESTAMP:kotlin.String) Time (milliseconds since epoch) that the contact was deleted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DeletedContactsColumns#CONTACT_ID:kotlin.String) A reference to the [ContactsContract.Contacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that was deleted. |

## Constants

### CONTACT_DELETED_TIMESTAMP

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_DELETED_TIMESTAMP: String
```

Time (milliseconds since epoch) that the contact was deleted. 

 Value: "contact_deleted_timestamp"

### CONTACT_ID

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_ID: String
```

A reference to the [ContactsContract.Contacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that was deleted.

Type: INTEGER 

 Value: "contact_id"

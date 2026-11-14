# ContactsContract.DeletedContactsColumns

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeletedContactsColumns

Kotlin| [Java](../android/provider/ContactsContract.DeletedContactsColumns.md) 
| --- | --- |

```
protected interface DeletedContactsColumns
```

| [android.provider.ContactsContract.DeletedContactsColumns](../android/provider/ContactsContract.DeletedContactsColumns.md) |

| Known Direct Subclasses [ContactsContract.DeletedContacts](../android/provider/ContactsContract.DeletedContacts.md) |--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------| | [ContactsContract.DeletedContacts](../android/provider/ContactsContract.DeletedContacts.md) | Constants for the deleted contact table. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_DELETED_TIMESTAMP](../android/provider/ContactsContract.DeletedContactsColumns.md) Time (milliseconds since epoch) that the contact was deleted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_ID](../android/provider/ContactsContract.DeletedContactsColumns.md) A reference to the [ContactsContract.Contacts._ID](../android/provider/BaseColumns.md) that was deleted. |

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

A reference to the [ContactsContract.Contacts._ID](../android/provider/BaseColumns.md) that was deleted.

Type: INTEGER 

 Value: "contact_id"

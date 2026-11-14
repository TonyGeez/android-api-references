# ContactsContract.PhoneLookupColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneLookupColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.PhoneLookupColumns "View this page in Java") 

```
protected interface PhoneLookupColumns
```

| [android.provider.ContactsContract.PhoneLookupColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#) |

| Known Direct Subclasses [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup) |------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [ContactsContract.PhoneLookup](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookup) | A table that represents the result of looking up a phone number, for example for caller ID. | |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#CONTACT_ID:kotlin.String) A reference to the [ContactsContract.Contacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that this data belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#DATA_ID:kotlin.String) The ID of the data row. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#LABEL:kotlin.String) The user defined label for the phone number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NORMALIZED_NUMBER](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#NORMALIZED_NUMBER:kotlin.String) The phone number's E164 representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMBER](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#NUMBER:kotlin.String) The phone number as the user entered it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneLookupColumns#TYPE:kotlin.String) The type of phone number, for example Home or Work. |

## Constants

### CONTACT_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_ID: String
```

A reference to the [ContactsContract.Contacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that this data belongs to.

Type: INTEGER 

 Value: "contact_id"

### DATA_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_ID: String
```

The ID of the data row.

Type: INTEGER 

 Value: "data_id"

### LABEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LABEL: String
```

The user defined label for the phone number.

Type: TEXT 

 Value: "label"

### NORMALIZED_NUMBER

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NORMALIZED_NUMBER: String
```

The phone number's E164 representation.

Type: TEXT 

 Value: "normalized_number"

### NUMBER

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBER: String
```

The phone number as the user entered it.

Type: TEXT 

 Value: "number"

### TYPE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE: String
```

The type of phone number, for example Home or Work.

Type: INTEGER 

 Value: "type"

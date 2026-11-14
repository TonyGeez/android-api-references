# ContactsContract.PhoneLookupColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneLookupColumns

Kotlin| [Java](../android/provider/ContactsContract.PhoneLookupColumns.md) 
| --- | --- |

```
protected interface PhoneLookupColumns
```

| [android.provider.ContactsContract.PhoneLookupColumns](../android/provider/ContactsContract.PhoneLookupColumns.md) |

| Known Direct Subclasses [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md) |------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------| | [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md) | A table that represents the result of looking up a phone number, for example for caller ID. | |
| --- | --- | --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_ID](../android/provider/ContactsContract.PhoneLookupColumns.md) A reference to the [ContactsContract.Contacts._ID](../android/provider/BaseColumns.md) that this data belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA_ID](../android/provider/ContactsContract.PhoneLookupColumns.md) The ID of the data row. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LABEL](../android/provider/ContactsContract.PhoneLookupColumns.md) The user defined label for the phone number. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NORMALIZED_NUMBER](../android/provider/ContactsContract.PhoneLookupColumns.md) The phone number's E164 representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NUMBER](../android/provider/ContactsContract.PhoneLookupColumns.md) The phone number as the user entered it. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE](../android/provider/ContactsContract.PhoneLookupColumns.md) The type of phone number, for example Home or Work. |
| --- | --- |

## Constants

### CONTACT_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTACT_ID: String
```

A reference to the [ContactsContract.Contacts._ID](../android/provider/BaseColumns.md) that this data belongs to.

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

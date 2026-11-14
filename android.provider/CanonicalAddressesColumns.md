# Telephony.CanonicalAddressesColumns

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CanonicalAddressesColumns

Kotlin| [Java](../android/provider/Telephony.CanonicalAddressesColumns.md) 
| --- | --- |

```
interface CanonicalAddressesColumns : BaseColumns
```

| [android.provider.Telephony.CanonicalAddressesColumns](../android/provider/Telephony.CanonicalAddressesColumns.md) |

Columns for the "canonical_addresses" table used by MMS and SMS.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ADDRESS](../android/provider/Telephony.CanonicalAddressesColumns.md) An address used in MMS or SMS. |

| Inherited constants ||
|---|---|
| From class [BaseColumns](../android/provider/BaseColumns.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](../android/provider/BaseColumns.md) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](../android/provider/BaseColumns.md) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### ADDRESS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADDRESS: String
```

An address used in MMS or SMS. Email addresses are converted to lower case and are compared by string equality. Other addresses are compared using PHONE_NUMBERS_EQUAL.

Type: TEXT 

 Value: "address"

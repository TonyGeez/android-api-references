# Telephony.CanonicalAddressesColumns

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CanonicalAddressesColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Telephony.CanonicalAddressesColumns "View this page in Java") 
| --- | --- |

```
interface CanonicalAddressesColumns : BaseColumns
```

| [android.provider.Telephony.CanonicalAddressesColumns](https://developer.android.com/reference/kotlin/android/provider/Telephony.CanonicalAddressesColumns#) |

Columns for the "canonical_addresses" table used by MMS and SMS.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ADDRESS](https://developer.android.com/reference/kotlin/android/provider/Telephony.CanonicalAddressesColumns#ADDRESS:kotlin.String) An address used in MMS or SMS. |

| Inherited constants ||
|---|---|
| From class [BaseColumns](https://developer.android.com/reference/kotlin/android/provider/BaseColumns) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_COUNT](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_COUNT:kotlin.String) <br /> The count of rows in a directory. Type: INTEGER <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [_ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) <br /> The unique ID for a row. Type: INTEGER (long) <br /> | ||

## Constants

### ADDRESS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADDRESS: String
```

An address used in MMS or SMS. Email addresses are converted to lower case and are compared by string equality. Other addresses are compared using PHONE_NUMBERS_EQUAL.

Type: TEXT 

 Value: "address"

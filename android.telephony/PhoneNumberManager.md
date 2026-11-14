Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneNumberManager

Kotlin | [Java](PhoneNumberManager.md)
| --- | --- |

```
open class PhoneNumberManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.PhoneNumberManager](PhoneNumberManager.md) |

PhoneNumberManager provides APIs for parsing phone numbers from various sources, such as URIs.

## Summary

| Public methods ||
|---|---|
| open [ParsedPhoneNumber](ParsedPhoneNumber.md) | `https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberManager#parsePhoneNumber(kotlin.collections.MutableList,%20kotlin.String)(associatedUris: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>?, countryIso: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Parses the associated URIs into a `https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber` object. |

## Public methods

### parsePhoneNumber

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parsePhoneNumber(
    associatedUris: MutableList<Uri!>?, 
    countryIso: String
): ParsedPhoneNumber
```

Parses the associated URIs into a `https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber` object.

This method attempts to parse the provided list of URIs into a valid phone number. The order of the URIs in the list is significant; it is recommended to prioritize URIs that are more likely to contain a valid phone number by placing them at the beginning of the list. The method will iterate through the list and return the first URI that can be successfully parsed into a valid phone number.

| Parameters ||
|---|---|
| `associatedUris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>?: The list of URIs to be parsed. The order of the URIs in the list matters. The method iterates through the list and stops at the first URI that can be parsed into a valid phone number. It is recommended to place the URIs that are most likely to contain a valid phone number at the beginning of the list. This value may be `null`. |
| `countryIso` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The country ISO code to be used for parsing. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber` | A `https://developer.android.com/reference/kotlin/android/telephony/ParsedPhoneNumber` object representing the first successfully parsed phone number from the provided list or an error if no numbers could be parsed. This value cannot be `null`. |

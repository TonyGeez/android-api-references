# PhoneNumberUtils

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneNumberUtils

Kotlin| [Java](https://developer.android.com/reference/android/telephony/PhoneNumberUtils "View this page in Java") 

```
open class PhoneNumberUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.PhoneNumberUtils](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#) |

Various utilities for dealing with phone number strings.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BCD_EXTENDED_TYPE_CALLED_PARTY](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_JAPAN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#FORMAT_JAPAN:kotlin.Int) Japanese formatting |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_NANP](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#FORMAT_NANP:kotlin.Int) NANP formatting |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAT_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#FORMAT_UNKNOWN:kotlin.Int) The current locale is unknown, look for a country code or don't format |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [PAUSE](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#PAUSE:kotlin.Char) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOA_International](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#TOA_International:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TOA_Unknown](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#TOA_Unknown:kotlin.Int) <br /> |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [WAIT](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#WAIT:kotlin.Char) <br /> |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [WILD](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#WILD:kotlin.Char) <br /> |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------|---|
| [PhoneNumberUtils](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#PhoneNumberUtils())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTtsSpan](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#addTtsSpan(android.text.Spannable,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endExclusive:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attach a [TtsSpan](https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.html#) to the supplied`Spannable`at the indicated location, annotating that location as containing a phone number. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areSamePhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#areSamePhoneNumber(kotlin.String,%20kotlin.String,%20kotlin.String))`(`number1:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `number2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `defaultCountryIso:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Determines if two phone numbers are the same. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [calledPartyBCDFragmentToString](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDFragmentToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Like calledPartyBCDToString, but field does not start with a TOA byte. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [calledPartyBCDFragmentToString](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDFragmentToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bcdExtType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Like calledPartyBCDToString, but field does not start with a TOA byte. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [calledPartyBCDToString](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` 3GPP TS 24. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [calledPartyBCDToString](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bcdExtType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` 3GPP TS 24. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compare](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#compare(android.content.Context,%20kotlin.String,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `a:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compare phone numbers a and b, and return true if they're identical enough for caller ID purposes. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compare](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#compare(kotlin.String,%20kotlin.String))`(`a:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compare phone numbers a and b, return true if they're identical enough for caller ID purposes. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [convertKeypadLettersToDigits](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#convertKeypadLettersToDigits(kotlin.String))`(`input:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Translates any alphabetic letters (i.e. \[A-Za-z\]) in the specified phone number into the equivalent numeric digits, according to the phone keypad letter mapping described in ITU E. |
| openstatic [TtsSpan](https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.html#)! | [createTtsSpan](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#createTtsSpan(kotlin.String))`(`phoneNumberString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a`TtsSpan`for the supplied`String`. |
| openstatic [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [createTtsSpannable](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#createTtsSpannable(kotlin.CharSequence))`(`phoneNumber:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Wrap the supplied`CharSequence`with a`TtsSpan`, annotating it as containing a phone number in its entirety. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [extractNetworkPortion](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#extractNetworkPortion(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Extracts the network address portion and canonicalizes (filters out separators.) Network address portion is everything up to DTMF control digit separators (pause or wait), but without non-dialable characters. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [extractPostDialPortion](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#extractPostDialPortion(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Extracts the post-dial sequence of DTMF control digits, pauses, and waits. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [formatJapaneseNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatJapaneseNumber(android.text.Editable))`(`text:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`)` Formats a phone number in-place using the Japanese formatting rules. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [formatNanpNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNanpNumber(android.text.Editable))`(`text:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`)` Formats a phone number in-place using the NANP formatting rules. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [formatNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumber(android.text.Editable,%20kotlin.Int))`(`text:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `defaultFormattingType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Formats a phone number in-place. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumber(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Breaks the given number down and formats it according to the rules for the country the number is from. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumber(kotlin.String,%20kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultCountryIso:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Format a phone number. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumber(kotlin.String,%20kotlin.String,%20kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `phoneNumberE164:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultCountryIso:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Format the phone number only if the given number hasn't been formatted. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumberToE164](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumberToE164(kotlin.String,%20kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultCountryIso:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Formats the specified`phoneNumber`to the E. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatNumberToRFC3966](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#formatNumberToRFC3966(kotlin.String,%20kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `defaultCountryIso:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Formats the specified`phoneNumber`to the RFC3966 representation. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFormatTypeForLocale](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#getFormatTypeForLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns the phone number formatting type for the given locale. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNumberFromIntent](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#getNumberFromIntent(android.content.Intent,%20android.content.Context))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Extracts the phone number from an Intent. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStrippedReversed](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#getStrippedReversed(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the network portion reversed. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [is12Key](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#is12Key(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` True if c is ISO-LATIN characters 0-9, \*, # |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDialable](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isDialable(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` True if c is ISO-LATIN characters 0-9, \*, # , +, WILD |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmergencyNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isEmergencyNumber(kotlin.String))`(`number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks a given number against the list of emergency numbers provided by the RIL and SIM card. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGlobalPhoneNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isGlobalPhoneNumber(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isISODigit](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isISODigit(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` True if c is ISO-LATIN characters 0-9 |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLocalEmergencyNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isLocalEmergencyNumber(android.content.Context,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Checks if a given number is an emergency number for the country that the user is in. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNonSeparator](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isNonSeparator(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` True if c is ISO-LATIN characters 0-9, \*, # , +, WILD, WAIT, PAUSE |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReallyDialable](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isReallyDialable(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` True if c is ISO-LATIN characters 0-9, \*, # , + (no WILD) |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStartsPostDial](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isStartsPostDial(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` This any anything to the right of this char is part of the post-dial string (eg this is PAUSE or WAIT) |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVoiceMailNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isVoiceMailNumber(kotlin.String))`(`number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` isVoiceMailNumber: checks a given number against the voicemail number provided by the RIL and SIM card. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWellFormedSmsAddress](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isWellFormedSmsAddress(kotlin.String))`(`address:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return true iff the network portion of`address`is, as far as we can tell on the device, suitable for use as an SMS destination address. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWpsCallNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#isWpsCallNumber(kotlin.String))`(`number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Check if the number is for Wireless Priority Service call. |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [networkPortionToCalledPartyBCD](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#networkPortionToCalledPartyBCD(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Note: calls extractNetworkPortion(), so do not use for SIM EF\[ADN\] style records Returns null if network portion is empty. |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [networkPortionToCalledPartyBCDWithLength](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#networkPortionToCalledPartyBCDWithLength(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Same as [networkPortionToCalledPartyBCD](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#networkPortionToCalledPartyBCD(kotlin.String)), but includes a one-byte length prefix. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [normalizeNumber](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#normalizeNumber(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Normalize a phone number by removing the characters other than digits. |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [numberToCalledPartyBCD](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#numberToCalledPartyBCD(kotlin.String))`(`number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Convert a dialing number to BCD byte array |
| openstatic [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [numberToCalledPartyBCD](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#numberToCalledPartyBCD(kotlin.String,%20kotlin.Int))`(`number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `bcdExtType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convert a dialing number to BCD byte array |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [replaceUnicodeDigits](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#replaceUnicodeDigits(kotlin.String))`(`number:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Replaces all unicode(e.g. Arabic, Persian) digits with their decimal digit equivalents. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [stringFromStringAndTOA](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#stringFromStringAndTOA(kotlin.String,%20kotlin.Int))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `TOA:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Basically: makes sure there's a + in front of a TOA_International number Returns null if s == null |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [stripSeparators](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#stripSeparators(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Strips separators from a phone number string. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toCallerIDMinMatch](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#toCallerIDMinMatch(kotlin.String))`(`phoneNumber:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the rightmost minimum matched characters in the network portion in \*reversed\* order This can be used to do a database lookup against the column that stores getStrippedReversed() Returns null if phoneNumber == null |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toaFromString](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#toaFromString(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the TOA for the given dial string Basically, returns TOA_International if there's a + prefix |

## Constants

### BCD_EXTENDED_TYPE_CALLED_PARTY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BCD_EXTENDED_TYPE_CALLED_PARTY: Int
```  

 Value: 2

### BCD_EXTENDED_TYPE_EF_ADN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BCD_EXTENDED_TYPE_EF_ADN: Int
```  

 Value: 1

### FORMAT_JAPAN

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_JAPAN: Int
```

Japanese formatting 

 Value: 2

### FORMAT_NANP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_NANP: Int
```

NANP formatting 

 Value: 1

### FORMAT_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAT_UNKNOWN: Int
```

The current locale is unknown, look for a country code or don't format 

 Value: 0

### PAUSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PAUSE: Char
```  

 Value: ','

### TOA_International

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOA_International: Int
```  

 Value: 145

### TOA_Unknown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TOA_Unknown: Int
```  

 Value: 129

### WAIT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WAIT: Char
```  

 Value: ';'

### WILD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WILD: Char
```  

 Value: 'N'

## Public constructors

### PhoneNumberUtils

```
PhoneNumberUtils()
```

## Public methods

### addTtsSpan

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun addTtsSpan(
    s: Spannable!, 
    start: Int, 
    endExclusive: Int
): Unit
```

Attach a [TtsSpan](https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.html#) to the supplied`Spannable`at the indicated location, annotating that location as containing a phone number.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:A`Spannable`to annotate. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The starting character position of the phone number in`s`. |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The position after the ending character in the phone number`s`. |

### areSamePhoneNumber

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun areSamePhoneNumber(
    number1: String, 
    number2: String, 
    defaultCountryIso: String
): Boolean
```

Determines if two phone numbers are the same.

Matching is based on [compare(java.lang.String,java.lang.String)](https://github.com/google/libphonenumber>libphonenumber</a>. Unlike <code><a docref=), matching takes into account national dialing plans rather than simply matching the last 7 digits of the two phone numbers. As a result, it is expected that some numbers which would match using the previous method will no longer match using this new approach.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `number2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `defaultCountryIso` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The lowercase two letter ISO 3166-1 country code. Used when parsing the phone numbers where it is not possible to determine the country associated with a phone number based on the number alone. It is recommended to pass in [TelephonyManager.getNetworkCountryIso()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#getNetworkCountryIso()). This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the two given phone number are same. |

### calledPartyBCDFragmentToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calledPartyBCDFragmentToString(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int
): String!
```

**Deprecated:** *use[calledPartyBCDFragmentToString(byte[],int,int,int)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDFragmentToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))instead. Calling this method is equivalent to calling[calledPartyBCDFragmentToString(byte[],int,int,int)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDFragmentToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))with [BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int) as the extended type.*

Like calledPartyBCDToString, but field does not start with a TOA byte. For example: SIM ADN extension fields 

### calledPartyBCDFragmentToString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calledPartyBCDFragmentToString(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int, 
    bcdExtType: Int
): String!
```

Like calledPartyBCDToString, but field does not start with a TOA byte. For example: SIM ADN extension fields

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bcdExtType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int), or [android.telephony.PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY:kotlin.Int) |

### calledPartyBCDToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calledPartyBCDToString(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int
): String!
```

**Deprecated:** *use[calledPartyBCDToString(byte[],int,int,int)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))instead. Calling this method is equivalent to calling[calledPartyBCDToString(byte[],int,int)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#calledPartyBCDToString(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))with [BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int) as the extended type.*

3GPP TS 24.008 10.5.4.7 Called Party BCD Number See Also TS 51.011 10.5.1 "dialing number/ssc string" and TS 11.11 "10.3.1 EF adn (Abbreviated dialing numbers)"

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data buffer |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):should point to the TOA (aka. TON/NPI) octet after the length byte |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the number of bytes including TOA byte and must be at least 2 |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | partial string on invalid decode |

### calledPartyBCDToString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun calledPartyBCDToString(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int, 
    bcdExtType: Int
): String!
```

3GPP TS 24.008 10.5.4.7 Called Party BCD Number See Also TS 51.011 10.5.1 "dialing number/ssc string" and TS 11.11 "10.3.1 EF adn (Abbreviated dialing numbers)"

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the data buffer |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):should point to the TOA (aka. TON/NPI) octet after the length byte |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the number of bytes including TOA byte and must be at least 2 |
| `bcdExtType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):used to determine the extended bcd coding Value is [android.telephony.PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int), or [android.telephony.PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY:kotlin.Int) |

**See Also**

- [#BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int)
- [#BCD_EXTENDED_TYPE_CALLED_PARTY](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY:kotlin.Int) 

### compare

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun compare(
    context: Context!, 
    a: String!, 
    b: String!
): Boolean
```

**Deprecated:** *use [areSamePhoneNumber(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#areSamePhoneNumber(kotlin.String,%20kotlin.String,%20kotlin.String))instead*

Compare phone numbers a and b, and return true if they're identical enough for caller ID purposes. Checks a resource to determine whether to use a strict or loose comparison algorithm. 

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun compare(
    a: String!, 
    b: String!
): Boolean
```

**Deprecated:** *use [areSamePhoneNumber(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#areSamePhoneNumber(kotlin.String,%20kotlin.String,%20kotlin.String))instead*

Compare phone numbers a and b, return true if they're identical enough for caller ID purposes. 

### convertKeypadLettersToDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convertKeypadLettersToDigits(input: String!): String!
```

Translates any alphabetic letters (i.e. \[A-Za-z\]) in the specified phone number into the equivalent numeric digits, according to the phone keypad letter mapping described in ITU E.161 and ISO/IEC 9995-8.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the input string, with alpha letters converted to numeric digits using the phone keypad letter mapping. For example, an input of "1-800-GOOG-411" will return "1-800-4664-411". |

### createTtsSpan

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createTtsSpan(phoneNumberString: String!): TtsSpan!
```

Create a`TtsSpan`for the supplied`String`.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumberString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`the entirety of which represents a phone number. |

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------|
| [TtsSpan](https://developer.android.com/reference/kotlin/android/text/style/TtsSpan.html#)! | A`TtsSpan`for {@param phoneNumberString}. |

### createTtsSpannable

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createTtsSpannable(phoneNumber: CharSequence!): CharSequence!
```

Wrap the supplied`CharSequence`with a`TtsSpan`, annotating it as containing a phone number in its entirety.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:A`CharSequence`the entirety of which represents a phone number. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | A`CharSequence`with appropriate annotations. |

### extractNetworkPortion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun extractNetworkPortion(phoneNumber: String!): String!
```

Extracts the network address portion and canonicalizes (filters out separators.) Network address portion is everything up to DTMF control digit separators (pause or wait), but without non-dialable characters. Please note that the GSM wild character is allowed in the result. This must be resolved before dialing. Returns null if phoneNumber == null 

### extractPostDialPortion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun extractPostDialPortion(phoneNumber: String!): String!
```

Extracts the post-dial sequence of DTMF control digits, pauses, and waits. Strips separators. This string may be empty, but will not be null unless phoneNumber == null. Returns null if phoneNumber == null 

### formatJapaneseNumber

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatJapaneseNumber(text: Editable!): Unit
```

**Deprecated:** *Use link #formatNumber(String phoneNumber, String defaultCountryIso) instead*

Formats a phone number in-place using the Japanese formatting rules. Numbers will be formatted as:

` 03-xxxx-xxxx 090-xxxx-xxxx 0120-xxx-xxx +81-3-xxxx-xxxx +81-90-xxxx-xxxx `

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!:the number to be formatted, will be modified with the formatting |

### formatNanpNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNanpNumber(text: Editable!): Unit
```

**Deprecated:** *Use link #formatNumber(String phoneNumber, String defaultCountryIso) instead*

Formats a phone number in-place using the NANP formatting rules. Numbers will be formatted as:

` xxxxx xxx-xxxx xxx-xxx-xxxx 1-xxx-xxx-xxxx +1-xxx-xxx-xxxx `

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!:the number to be formatted, will be modified with the formatting |

### formatNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNumber(
    text: Editable!, 
    defaultFormattingType: Int
): Unit
```

**Deprecated:** *Use link #formatNumber(String phoneNumber, String defaultCountryIso) instead*

Formats a phone number in-place. Currently [FORMAT_JAPAN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#FORMAT_JAPAN:kotlin.Int) and [FORMAT_NANP](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#FORMAT_NANP:kotlin.Int) is supported as a second argument.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!:The number to be formatted, will be modified with the formatting |
| `defaultFormattingType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The default formatting rules to apply if the number does not begin with +\[country_code\] |

### formatNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNumber(source: String!): String!
```

**Deprecated:** *Use link #formatNumber(String phoneNumber, String defaultCountryIso) instead*

Breaks the given number down and formats it according to the rules for the country the number is from.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The phone number to format |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A locally acceptable formatting of the input, or the raw input if formatting rules aren't known for the number |

### formatNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNumber(
    phoneNumber: String!, 
    defaultCountryIso: String!
): String!
```

Format a phone number.

If the given number doesn't have the country code, the phone will be formatted to the default country's convention.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to be formatted. |
| `defaultCountryIso` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ISO 3166-1 two letters country code whose convention will be used if the given number doesn't have the country code. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted number, or null if the given number is not valid. |

### formatNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNumber(
    phoneNumber: String!, 
    phoneNumberE164: String!, 
    defaultCountryIso: String!
): String!
```

Format the phone number only if the given number hasn't been formatted.

The number which has only dailable character is treated as not being formatted.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to be formatted. |
| `phoneNumberE164` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the E164 format number whose country code is used if the given phoneNumber doesn't have the country code. |
| `defaultCountryIso` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ISO 3166-1 two letters country code whose convention will be used if the phoneNumberE164 is null or invalid, or if phoneNumber contains IDD. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted number if the given number has been formatted, otherwise, return the given number. |

### formatNumberToE164

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNumberToE164(
    phoneNumber: String!, 
    defaultCountryIso: String!
): String!
```

Formats the specified`phoneNumber`to the E.164 representation.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the phone number to format. |
| `defaultCountryIso` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ISO 3166-1 two letters country code in UPPER CASE. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the E.164 representation, or null if the given phone number is not valid. |

### formatNumberToRFC3966

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatNumberToRFC3966(
    phoneNumber: String!, 
    defaultCountryIso: String!
): String!
```

Formats the specified`phoneNumber`to the RFC3966 representation.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the phone number to format. |
| `defaultCountryIso` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ISO 3166-1 two letters country code in UPPER CASE. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the RFC3966 representation, or null if the given phone number is not valid. |

### getFormatTypeForLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getFormatTypeForLocale(locale: Locale!): Int
```

**Deprecated:** *Use link #formatNumber(String phoneNumber, String defaultCountryIso) instead*

Returns the phone number formatting type for the given locale.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The locale of interest, usually [Locale.getDefault()](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()) |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The formatting type for the given locale, or FORMAT_UNKNOWN if the formatting rules are not known for the given locale |

### getNumberFromIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberFromIntent(
    intent: Intent!, 
    context: Context!
): String!
```

Extracts the phone number from an Intent.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:the intent to get the number of |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:a context to use for database access |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the phone number that would be called by the intent, or`null`if the number cannot be found. |

### getStrippedReversed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getStrippedReversed(phoneNumber: String!): String!
```

Returns the network portion reversed. This string is intended to go into an index column for a database lookup. Returns null if phoneNumber == null 

### is12Key

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun is12Key(c: Char): Boolean
```

True if c is ISO-LATIN characters 0-9, \*, # 

### isDialable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isDialable(c: Char): Boolean
```

True if c is ISO-LATIN characters 0-9, \*, # , +, WILD 

### isEmergencyNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isEmergencyNumber(number: String!): Boolean
```

**Deprecated:** *Please use [TelephonyManager.isEmergencyNumber(String)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isEmergencyNumber(kotlin.String))instead.*

Checks a given number against the list of emergency numbers provided by the RIL and SIM card.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to look up. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the number is in the list of emergency numbers listed in the RIL / SIM, otherwise return false. |

### isGlobalPhoneNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isGlobalPhoneNumber(phoneNumber: String!): Boolean
```  

### isISODigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isISODigit(c: Char): Boolean
```

True if c is ISO-LATIN characters 0-9 

### isLocalEmergencyNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isLocalEmergencyNumber(
    context: Context!, 
    number: String!
): Boolean
```

**Deprecated:** *Please use [TelephonyManager.isEmergencyNumber(String)](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#isEmergencyNumber(kotlin.String))instead.*

Checks if a given number is an emergency number for the country that the user is in.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to look up. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the specific context which the number should be checked against |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the specified number is an emergency number for the country the user is currently in. |

### isNonSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isNonSeparator(c: Char): Boolean
```

True if c is ISO-LATIN characters 0-9, \*, # , +, WILD, WAIT, PAUSE 

### isReallyDialable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isReallyDialable(c: Char): Boolean
```

True if c is ISO-LATIN characters 0-9, \*, # , + (no WILD) 

### isStartsPostDial

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isStartsPostDial(c: Char): Boolean
```

This any anything to the right of this char is part of the post-dial string (eg this is PAUSE or WAIT) 

### isVoiceMailNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isVoiceMailNumber(number: String!): Boolean
```

isVoiceMailNumber: checks a given number against the voicemail number provided by the RIL and SIM card. The caller must have the READ_PHONE_STATE credential.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to look up. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the number is in the list of voicemail. False otherwise, including if the caller does not have the permission to read the VM number. |

### isWellFormedSmsAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isWellFormedSmsAddress(address: String!): Boolean
```

Return true iff the network portion of`address`is, as far as we can tell on the device, suitable for use as an SMS destination address. 

### isWpsCallNumber

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isWpsCallNumber(number: String): Boolean
```

Check if the number is for Wireless Priority Service call.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The phone number used for WPS call. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if number matches WPS pattern and`false`otherwise. |

### networkPortionToCalledPartyBCD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun networkPortionToCalledPartyBCD(s: String!): ByteArray!
```

Note: calls extractNetworkPortion(), so do not use for SIM EF\[ADN\] style records Returns null if network portion is empty. 

### networkPortionToCalledPartyBCDWithLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun networkPortionToCalledPartyBCDWithLength(s: String!): ByteArray!
```

Same as [networkPortionToCalledPartyBCD](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#networkPortionToCalledPartyBCD(kotlin.String)), but includes a one-byte length prefix. 

### normalizeNumber

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun normalizeNumber(phoneNumber: String!): String!
```

Normalize a phone number by removing the characters other than digits. If the given number has keypad letters, the letters will be converted to digits first.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to be normalized. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the normalized number. |

### numberToCalledPartyBCD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun numberToCalledPartyBCD(number: String!): ByteArray!
```

**Deprecated:** *use [numberToCalledPartyBCD(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#numberToCalledPartyBCD(kotlin.String,%20kotlin.Int))instead. Calling this method is equivalent to calling [numberToCalledPartyBCD(java.lang.String,int)](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#numberToCalledPartyBCD(kotlin.String,%20kotlin.Int))with [BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int) as the extended type.*

Convert a dialing number to BCD byte array

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:dialing number string. If the dialing number starts with '+', set to international TOA |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | BCD byte array |

### numberToCalledPartyBCD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun numberToCalledPartyBCD(
    number: String!, 
    bcdExtType: Int
): ByteArray!
```

Convert a dialing number to BCD byte array

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:dialing number string. If the dialing number starts with '+', set to international TOA |
| `bcdExtType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):used to determine the extended bcd coding Value is [android.telephony.PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int), or [android.telephony.PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------------|----------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | BCD byte array |

**See Also**

- [#BCD_EXTENDED_TYPE_EF_ADN](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_EF_ADN:kotlin.Int)
- [#BCD_EXTENDED_TYPE_CALLED_PARTY](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberUtils#BCD_EXTENDED_TYPE_CALLED_PARTY:kotlin.Int) 

### replaceUnicodeDigits

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun replaceUnicodeDigits(number: String!): String!
```

Replaces all unicode(e.g. Arabic, Persian) digits with their decimal digit equivalents.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `number` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the number to perform the replacement on. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the replaced number. |

### stringFromStringAndTOA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stringFromStringAndTOA(
    s: String!, 
    TOA: Int
): String!
```

Basically: makes sure there's a + in front of a TOA_International number Returns null if s == null 

### stripSeparators

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun stripSeparators(phoneNumber: String!): String!
```

Strips separators from a phone number string.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------|
| `phoneNumber` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:phone number to strip. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | phone string stripped of separators. |

### toCallerIDMinMatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toCallerIDMinMatch(phoneNumber: String!): String!
```

Returns the rightmost minimum matched characters in the network portion in \*reversed\* order This can be used to do a database lookup against the column that stores getStrippedReversed() Returns null if phoneNumber == null 

### toaFromString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toaFromString(s: String!): Int
```

Returns the TOA for the given dial string Basically, returns TOA_International if there's a + prefix

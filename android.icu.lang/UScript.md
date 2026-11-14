Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UScript

```
class UScript
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.lang.UScript](https://developer.android.com/reference/kotlin/android/icu/lang/UScript#) |

Constants for ISO 15924 script codes, and related functions.

The current set of script code constants supports at least all scripts that are encoded in the version of Unicode which ICU currently supports. The names of the constants are usually derived from the Unicode script property value aliases. See UAX #24 Unicode Script Property (http://www.unicode.org/reports/tr24/) and http://www.unicode.org/Public/UCD/latest/ucd/PropertyValueAliases.txt .

In addition, constants for many ISO 15924 script codes are included, for use with language tags, CLDR data, and similar. Some of those codes are not used in the Unicode Character Database (UCD). For example, there are no characters that have a UCD script property value of Hans or Hant. All Han ideographs have the Hani script property value in Unicode.

Private-use codes Qaaa..Qabx are not included, except as used in the UCD or in CLDR.

Starting with ICU 55, script codes are only added when their scripts have been or will certainly be encoded in Unicode, and have been assigned Unicode script property value aliases, to ensure that their script names are stable and match the names of the constants. Script codes like Latf and Aran that are not subject to separate encoding may be added at any time.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.ScriptUsage` Script usage constants. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ADLAM:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#AFAKA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#AHOM:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ANATOLIAN_HIEROGLYPHS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ARABIC:kotlin.Int` Arabic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ARABIC_NASTALIQ:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ARMENIAN:kotlin.Int` Armenian |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#AVESTAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BALINESE:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BAMUM:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BASSA_VAH:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BATAK:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BENGALI:kotlin.Int` Bengali |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BERIA_ERFE:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BHAIKSUKI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BLISSYMBOLS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BOOK_PAHLAVI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BOPOMOFO:kotlin.Int` Bopomofo |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BRAHMI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BRAILLE:kotlin.Int` Braille Script in Unicode 4 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BUGINESE:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#BUHID:kotlin.Int` Buhid |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CANADIAN_ABORIGINAL:kotlin.Int` Unified Canadian Aboriginal Symbols |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CARIAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CAUCASIAN_ALBANIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CHAKMA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CHAM:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CHEROKEE:kotlin.Int` Cherokee |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CHORASMIAN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CIRTH:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#COMMON:kotlin.Int` Common |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#COPTIC:kotlin.Int` Coptic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CUNEIFORM:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CYPRIOT:kotlin.Int` Cypriot Script in Unicode 4 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CYPRO_MINOAN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#CYRILLIC:kotlin.Int` Cyrillic |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#DEMOTIC_EGYPTIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#DESERET:kotlin.Int` Deseret |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#DEVANAGARI:kotlin.Int` Devanagari |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#DIVES_AKURU:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#DOGRA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#DUPLOYAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#EASTERN_SYRIAC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#EGYPTIAN_HIEROGLYPHS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ELBASAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ELYMAIC:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ESTRANGELO_SYRIAC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ETHIOPIC:kotlin.Int` Ethiopic |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GARAY:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GEORGIAN:kotlin.Int` Georgian |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GLAGOLITIC:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GOTHIC:kotlin.Int` Gothic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GRANTHA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GREEK:kotlin.Int` Greek |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GUJARATI:kotlin.Int` Gujarati |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GUNJALA_GONDI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GURMUKHI:kotlin.Int` Gurmukhi |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#GURUNG_KHEMA:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HAN:kotlin.Int` Han |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HANGUL:kotlin.Int` Hangul |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HANIFI_ROHINGYA:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HANUNOO:kotlin.Int` Hanunooo |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HAN_WITH_BOPOMOFO:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HARAPPAN_INDUS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HATRAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HEBREW:kotlin.Int` Hebrew |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HIERATIC_EGYPTIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#HIRAGANA:kotlin.Int` Hiragana |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#IMPERIAL_ARAMAIC:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#INHERITED:kotlin.Int` Inherited |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#INSCRIPTIONAL_PAHLAVI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#INSCRIPTIONAL_PARTHIAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#INVALID_CODE:kotlin.Int` Invalid code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#JAMO:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#JAPANESE:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#JAVANESE:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#JURCHEN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KAITHI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KANNADA:kotlin.Int` Kannada |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KATAKANA:kotlin.Int` Katakana |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KATAKANA_OR_HIRAGANA:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KAWI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KAYAH_LI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KHAROSHTHI:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KHITAN_SMALL_SCRIPT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KHMER:kotlin.Int` Khmer |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KHOJKI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KHUDAWADI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KHUTSURI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KIRAT_RAI:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KOREAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#KPELLE:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LANNA:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LAO:kotlin.Int` Lao |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LATIN:kotlin.Int` Latin |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LATIN_FRAKTUR:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LATIN_GAELIC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LEPCHA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LIMBU:kotlin.Int` Limbu Script in Unicode 4 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LINEAR_A:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LINEAR_B:kotlin.Int` Linear B Script in Unicode 4 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LISU:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LOMA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LYCIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#LYDIAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MAHAJANI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MAKASAR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MALAYALAM:kotlin.Int` Malayalam |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MANDAEAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MANDAIC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MANICHAEAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MARCHEN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MASARAM_GONDI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MATHEMATICAL_NOTATION:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MAYAN_HIEROGLYPHS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MEDEFAIDRIN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MEITEI_MAYEK:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MENDE:kotlin.Int` Mende Kikakui ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MEROITIC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MEROITIC_CURSIVE:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MEROITIC_HIEROGLYPHS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MIAO:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MODI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MONGOLIAN:kotlin.Int` Mangolian |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MOON:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MRO:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MULTANI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#MYANMAR:kotlin.Int` Myammar |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NABATAEAN:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NAG_MUNDARI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NAKHI_GEBA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NANDINAGARI:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NEWA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NEW_TAI_LUE:kotlin.Int` Script in Unicode 4. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NKO:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NUSHU:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#NYIAKENG_PUACHUE_HMONG:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OGHAM:kotlin.Int` Ogham |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_CHURCH_SLAVONIC_CYRILLIC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_HUNGARIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_ITALIC:kotlin.Int` Old Itallic |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_NORTH_ARABIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_PERMIC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_PERSIAN:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_SOGDIAN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_SOUTH_ARABIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OLD_UYGHUR:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OL_CHIKI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OL_ONAL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ORIYA:kotlin.Int` Oriya |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ORKHON:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OSAGE:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#OSMANYA:kotlin.Int` Osmanya Script in Unicode 4 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PAHAWH_HMONG:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PALMYRENE:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PAU_CIN_HAU:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PHAGS_PA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PHOENICIAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PHONETIC_POLLARD:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#PSALTER_PAHLAVI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#REJANG:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#RONGORONGO:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#RUNIC:kotlin.Int` Runic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SAMARITAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SARATI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SAURASHTRA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SHARADA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SHAVIAN:kotlin.Int` Shavian Script in Unicode 4 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SIDDHAM:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SIDETIC:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SIGN_WRITING:kotlin.Int` ISO 15924 script code for Sutton SignWriting |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SIMPLIFIED_HAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SINDHI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SINHALA:kotlin.Int` Sinhala |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SOGDIAN:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SORA_SOMPENG:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SOYOMBO:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SUNDANESE:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SUNUWAR:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SYLOTI_NAGRI:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SYMBOLS:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SYMBOLS_EMOJI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#SYRIAC:kotlin.Int` Syriac |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAGALOG:kotlin.Int` Tagalog |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAGBANWA:kotlin.Int` Tagbanwa |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAI_LE:kotlin.Int` Tai Le Script in Unicode 4 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAI_VIET:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAI_YO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAKRI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TAMIL:kotlin.Int` Tamil |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TANGSA:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TANGUT:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TELUGU:kotlin.Int` Telugu |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TENGWAR:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#THAANA:kotlin.Int` Thana |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#THAI:kotlin.Int` Thai |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TIBETAN:kotlin.Int` Tibetan |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TIFINAGH:kotlin.Int` Script in Unicode 4. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TIRHUTA:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TODHRI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TOLONG_SIKI:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TOTO:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TRADITIONAL_HAN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TRADITIONAL_HAN_WITH_LATIN:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#TULU_TIGALARI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#UCAS:kotlin.Int` Unified Canadian Aboriginal Symbols (alias) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#UGARITIC:kotlin.Int` Ugaritic Script in Unicode 4 |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#UNKNOWN:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#UNWRITTEN_LANGUAGES:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#VAI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#VISIBLE_SPEECH:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#VITHKUQI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#WANCHO:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#WARANG_CITI:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#WESTERN_SYRIAC:kotlin.Int` ISO 15924 script code |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#WOLEAI:kotlin.Int` ISO 15924 script code |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#YEZIDI:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#YI:kotlin.Int` Yi syllables |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#ZANABAZAR_SQUARE:kotlin.Int` ISO 15924 script code |
| --- | --- |

| Public methods ||
|---|---|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#breaksBetweenLetters(kotlin.Int)(script: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the script allows line breaks between letters (excluding hyphenation). |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getCode(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Gets a script codes associated with the given locale or ISO 15924 abbreviation or name. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getCode(kotlin.String)(nameOrAbbrOrLocale: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets the script codes associated with the given locale or ISO 15924 abbreviation or name. |
| --- | --- |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getCode(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Gets a script codes associated with the given locale or ISO 15924 abbreviation or name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getCodeFromName(kotlin.String)(nameOrAbbr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the script code associated with the given Unicode script property alias (name or abbreviation). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getName(kotlin.Int)(scriptCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the long Unicode script name, if there is one. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getSampleString(kotlin.Int)(script: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the script sample character string. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getScript(kotlin.Int)(codepoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the script code associated with the given codepoint. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getScriptExtensions(kotlin.Int,%20java.util.BitSet)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, set: https://developer.android.com/reference/kotlin/java/util/BitSet.html#!)` Sets code point c's Script_Extensions as script code integers into the output BitSet. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getShortName(kotlin.Int)(scriptCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the 4-letter ISO 15924 script code, which is the same as the short Unicode script name if Unicode has names for the script. |
| static [UScript.ScriptUsage](https://developer.android.com/reference/kotlin/android/icu/lang/UScript.ScriptUsage)! | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getUsage(kotlin.Int)(script: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the script usage according to UAX #31 Unicode Identifier and Pattern Syntax. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#hasScript(kotlin.Int,%20kotlin.Int)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sc: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Do the Script_Extensions of code point c contain script sc? If c does not have explicit Script_Extensions, then this tests whether c has the Script property value sc. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#isCased(kotlin.Int)(script: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if in modern (or most recent) usage of the script case distinctions are customary. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#isRightToLeft(kotlin.Int)(script: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns true if the script is written right-to-left. |

## Constants

### ADLAM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADLAM: Int
```

ISO 15924 script code

 Value: 167

### AFAKA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AFAKA: Int
```

ISO 15924 script code

 Value: 147

### AHOM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AHOM: Int
```

ISO 15924 script code

 Value: 161

### ANATOLIAN_HIEROGLYPHS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANATOLIAN_HIEROGLYPHS: Int
```

ISO 15924 script code

 Value: 156

### ARABIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARABIC: Int
```

Arabic

 Value: 2

### ARABIC_NASTALIQ

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARABIC_NASTALIQ: Int
```

 Value: 200

### ARMENIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ARMENIAN: Int
```

Armenian

 Value: 3

### AVESTAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val AVESTAN: Int
```

ISO 15924 script code

 Value: 117

### BALINESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BALINESE: Int
```

ISO 15924 script code

 Value: 62

### BAMUM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BAMUM: Int
```

ISO 15924 script code

 Value: 130

### BASSA_VAH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BASSA_VAH: Int
```

ISO 15924 script code

 Value: 134

### BATAK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BATAK: Int
```

ISO 15924 script code

 Value: 63

### BENGALI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BENGALI: Int
```

Bengali

 Value: 4

### BERIA_ERFE

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BERIA_ERFE: Int
```

 Value: 208

### BHAIKSUKI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BHAIKSUKI: Int
```

ISO 15924 script code

 Value: 168

### BLISSYMBOLS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BLISSYMBOLS: Int
```

ISO 15924 script code

 Value: 64

### BOOK_PAHLAVI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOOK_PAHLAVI: Int
```

ISO 15924 script code

 Value: 124

### BOPOMOFO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOPOMOFO: Int
```

Bopomofo

 Value: 5

### BRAHMI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BRAHMI: Int
```

ISO 15924 script code

 Value: 65

### BRAILLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BRAILLE: Int
```

Braille Script in Unicode 4

 Value: 46

### BUGINESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUGINESE: Int
```

Script in Unicode 4.1

 Value: 55

### BUHID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUHID: Int
```

Buhid

 Value: 44

### CANADIAN_ABORIGINAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CANADIAN_ABORIGINAL: Int
```

Unified Canadian Aboriginal Symbols

 Value: 40

### CARIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CARIAN: Int
```

ISO 15924 script code

 Value: 104

### CAUCASIAN_ALBANIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CAUCASIAN_ALBANIAN: Int
```

ISO 15924 script code

 Value: 159

### CHAKMA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHAKMA: Int
```

ISO 15924 script code

 Value: 118

### CHAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHAM: Int
```

ISO 15924 script code

 Value: 66

### CHEROKEE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHEROKEE: Int
```

Cherokee

 Value: 6

### CHORASMIAN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHORASMIAN: Int
```

 Value: 189

### CIRTH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CIRTH: Int
```

ISO 15924 script code

 Value: 67

### COMMON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMMON: Int
```

Common

 Value: 0

### COPTIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COPTIC: Int
```

Coptic

 Value: 7

### CUNEIFORM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CUNEIFORM: Int
```

ISO 15924 script code

 Value: 101

### CYPRIOT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CYPRIOT: Int
```

Cypriot Script in Unicode 4

 Value: 47

### CYPRO_MINOAN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CYPRO_MINOAN: Int
```

 Value: 193

### CYRILLIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CYRILLIC: Int
```

Cyrillic

 Value: 8

### DEMOTIC_EGYPTIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEMOTIC_EGYPTIAN: Int
```

ISO 15924 script code

 Value: 69

### DESERET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DESERET: Int
```

Deseret

 Value: 9

### DEVANAGARI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVANAGARI: Int
```

Devanagari

 Value: 10

### DIVES_AKURU

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIVES_AKURU: Int
```

 Value: 190

### DOGRA

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOGRA: Int
```

ISO 15924 script code

 Value: 178

### DUPLOYAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLOYAN: Int
```

ISO 15924 script code

 Value: 135

### EASTERN_SYRIAC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EASTERN_SYRIAC: Int
```

ISO 15924 script code

 Value: 97

### EGYPTIAN_HIEROGLYPHS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EGYPTIAN_HIEROGLYPHS: Int
```

ISO 15924 script code

 Value: 71

### ELBASAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ELBASAN: Int
```

ISO 15924 script code

 Value: 136

### ELYMAIC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ELYMAIC: Int
```

 Value: 185

### ESTRANGELO_SYRIAC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ESTRANGELO_SYRIAC: Int
```

ISO 15924 script code

 Value: 95

### ETHIOPIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ETHIOPIC: Int
```

Ethiopic

 Value: 11

### GARAY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GARAY: Int
```

 Value: 201

### GEORGIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GEORGIAN: Int
```

Georgian

 Value: 12

### GLAGOLITIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GLAGOLITIC: Int
```

Script in Unicode 4.1

 Value: 56

### GOTHIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GOTHIC: Int
```

Gothic

 Value: 13

### GRANTHA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GRANTHA: Int
```

ISO 15924 script code

 Value: 137

### GREEK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GREEK: Int
```

Greek

 Value: 14

### GUJARATI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GUJARATI: Int
```

Gujarati

 Value: 15

### GUNJALA_GONDI

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GUNJALA_GONDI: Int
```

 Value: 179

### GURMUKHI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GURMUKHI: Int
```

Gurmukhi

 Value: 16

### GURUNG_KHEMA

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GURUNG_KHEMA: Int
```

 Value: 202

### HAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HAN: Int
```

Han

 Value: 17

### HANGUL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANGUL: Int
```

Hangul

 Value: 18

### HANIFI_ROHINGYA

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANIFI_ROHINGYA: Int
```

 Value: 182

### HANUNOO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HANUNOO: Int
```

Hanunooo

 Value: 43

### HAN_WITH_BOPOMOFO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HAN_WITH_BOPOMOFO: Int
```

ISO 15924 script code

 Value: 172

### HARAPPAN_INDUS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HARAPPAN_INDUS: Int
```

ISO 15924 script code

 Value: 77

### HATRAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HATRAN: Int
```

ISO 15924 script code

 Value: 162

### HEBREW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HEBREW: Int
```

Hebrew

 Value: 19

### HIERATIC_EGYPTIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HIERATIC_EGYPTIAN: Int
```

ISO 15924 script code

 Value: 70

### HIRAGANA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HIRAGANA: Int
```

Hiragana

 Value: 20

### IMPERIAL_ARAMAIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IMPERIAL_ARAMAIC: Int
```

ISO 15924 script code

 Value: 116

### INHERITED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INHERITED: Int
```

Inherited

 Value: 1

### INSCRIPTIONAL_PAHLAVI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSCRIPTIONAL_PAHLAVI: Int
```

ISO 15924 script code

 Value: 122

### INSCRIPTIONAL_PARTHIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INSCRIPTIONAL_PARTHIAN: Int
```

ISO 15924 script code

 Value: 125

### INVALID_CODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_CODE: Int
```

Invalid code

 Value: -1

### JAMO

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JAMO: Int
```

ISO 15924 script code

 Value: 173

### JAPANESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JAPANESE: Int
```

ISO 15924 script code

 Value: 105

### JAVANESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JAVANESE: Int
```

ISO 15924 script code

 Value: 78

### JURCHEN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JURCHEN: Int
```

ISO 15924 script code

 Value: 148

### KAITHI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KAITHI: Int
```

ISO 15924 script code

 Value: 120

### KANNADA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KANNADA: Int
```

Kannada

 Value: 21

### KATAKANA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KATAKANA: Int
```

Katakana

 Value: 22

### KATAKANA_OR_HIRAGANA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KATAKANA_OR_HIRAGANA: Int
```

Script in Unicode 4.0.1

 Value: 54

### KAWI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KAWI: Int
```

 Value: 198

### KAYAH_LI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KAYAH_LI: Int
```

ISO 15924 script code

 Value: 79

### KHAROSHTHI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KHAROSHTHI: Int
```

Script in Unicode 4.1

 Value: 57

### KHITAN_SMALL_SCRIPT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KHITAN_SMALL_SCRIPT: Int
```

 Value: 191

### KHMER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KHMER: Int
```

Khmer

 Value: 23

### KHOJKI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KHOJKI: Int
```

ISO 15924 script code

 Value: 157

### KHUDAWADI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KHUDAWADI: Int
```

ISO 15924 script code

 Value: 145

### KHUTSURI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KHUTSURI: Int
```

ISO 15924 script code

 Value: 72

### KIRAT_RAI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KIRAT_RAI: Int
```

 Value: 203

### KOREAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KOREAN: Int
```

ISO 15924 script code

 Value: 119

### KPELLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KPELLE: Int
```

ISO 15924 script code

 Value: 138

### LANNA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LANNA: Int
```

ISO 15924 script code

 Value: 106

### LAO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAO: Int
```

Lao

 Value: 24

### LATIN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATIN: Int
```

Latin

 Value: 25

### LATIN_FRAKTUR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATIN_FRAKTUR: Int
```

ISO 15924 script code

 Value: 80

### LATIN_GAELIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LATIN_GAELIC: Int
```

ISO 15924 script code

 Value: 81

### LEPCHA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LEPCHA: Int
```

ISO 15924 script code

 Value: 82

### LIMBU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIMBU: Int
```

Limbu Script in Unicode 4

 Value: 48

### LINEAR_A

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LINEAR_A: Int
```

ISO 15924 script code

 Value: 83

### LINEAR_B

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LINEAR_B: Int
```

Linear B Script in Unicode 4

 Value: 49

### LISU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LISU: Int
```

ISO 15924 script code

 Value: 131

### LOMA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOMA: Int
```

ISO 15924 script code

 Value: 139

### LYCIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LYCIAN: Int
```

ISO 15924 script code

 Value: 107

### LYDIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LYDIAN: Int
```

ISO 15924 script code

 Value: 108

### MAHAJANI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAHAJANI: Int
```

ISO 15924 script code

 Value: 160

### MAKASAR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAKASAR: Int
```

 Value: 180

### MALAYALAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MALAYALAM: Int
```

Malayalam

 Value: 26

### MANDAEAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANDAEAN: Int
```

ISO 15924 script code

 Value: 84

### MANDAIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANDAIC: Int
```

ISO 15924 script code

 Value: 84

### MANICHAEAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MANICHAEAN: Int
```

ISO 15924 script code

 Value: 121

### MARCHEN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MARCHEN: Int
```

ISO 15924 script code

 Value: 169

### MASARAM_GONDI

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MASARAM_GONDI: Int
```

ISO 15924 script code

 Value: 175

### MATHEMATICAL_NOTATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATHEMATICAL_NOTATION: Int
```

ISO 15924 script code

 Value: 128

### MAYAN_HIEROGLYPHS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAYAN_HIEROGLYPHS: Int
```

ISO 15924 script code

 Value: 85

### MEDEFAIDRIN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEDEFAIDRIN: Int
```

 Value: 181

### MEITEI_MAYEK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEITEI_MAYEK: Int
```

ISO 15924 script code

 Value: 115

### MENDE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MENDE: Int
```

Mende Kikakui ISO 15924 script code

 Value: 140

### MEROITIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEROITIC: Int
```

ISO 15924 script code

 Value: 86

### MEROITIC_CURSIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEROITIC_CURSIVE: Int
```

ISO 15924 script code

 Value: 141

### MEROITIC_HIEROGLYPHS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MEROITIC_HIEROGLYPHS: Int
```

ISO 15924 script code

 Value: 86

### MIAO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIAO: Int
```

ISO 15924 script code

 Value: 92

### MODI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODI: Int
```

ISO 15924 script code

 Value: 163

### MONGOLIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MONGOLIAN: Int
```

Mangolian

 Value: 27

### MOON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MOON: Int
```

ISO 15924 script code

 Value: 114

### MRO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MRO: Int
```

ISO 15924 script code

 Value: 149

### MULTANI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MULTANI: Int
```

ISO 15924 script code

 Value: 164

### MYANMAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MYANMAR: Int
```

Myammar

 Value: 28

### NABATAEAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NABATAEAN: Int
```

ISO 15924 script code

 Value: 143

### NAG_MUNDARI

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NAG_MUNDARI: Int
```

 Value: 199

### NAKHI_GEBA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NAKHI_GEBA: Int
```

ISO 15924 script code

 Value: 132

### NANDINAGARI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NANDINAGARI: Int
```

 Value: 187

### NEWA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NEWA: Int
```

ISO 15924 script code

 Value: 170

### NEW_TAI_LUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NEW_TAI_LUE: Int
```

Script in Unicode 4.1

 Value: 59

### NKO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NKO: Int
```

ISO 15924 script code

 Value: 87

### NUSHU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NUSHU: Int
```

ISO 15924 script code

 Value: 150

### NYIAKENG_PUACHUE_HMONG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NYIAKENG_PUACHUE_HMONG: Int
```

 Value: 186

### OGHAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OGHAM: Int
```

Ogham

 Value: 29

### OLD_CHURCH_SLAVONIC_CYRILLIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_CHURCH_SLAVONIC_CYRILLIC: Int
```

ISO 15924 script code

 Value: 68

### OLD_HUNGARIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_HUNGARIAN: Int
```

ISO 15924 script code

 Value: 76

### OLD_ITALIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_ITALIC: Int
```

Old Itallic

 Value: 30

### OLD_NORTH_ARABIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_NORTH_ARABIAN: Int
```

ISO 15924 script code

 Value: 142

### OLD_PERMIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_PERMIC: Int
```

ISO 15924 script code

 Value: 89

### OLD_PERSIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_PERSIAN: Int
```

Script in Unicode 4.1

 Value: 61

### OLD_SOGDIAN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_SOGDIAN: Int
```

 Value: 184

### OLD_SOUTH_ARABIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_SOUTH_ARABIAN: Int
```

ISO 15924 script code

 Value: 133

### OLD_UYGHUR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OLD_UYGHUR: Int
```

 Value: 194

### OL_CHIKI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OL_CHIKI: Int
```

ISO 15924 script code

 Value: 109

### OL_ONAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OL_ONAL: Int
```

 Value: 204

### ORIYA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORIYA: Int
```

Oriya

 Value: 31

### ORKHON

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ORKHON: Int
```

ISO 15924 script code

 Value: 88

### OSAGE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OSAGE: Int
```

ISO 15924 script code

 Value: 171

### OSMANYA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OSMANYA: Int
```

Osmanya Script in Unicode 4

 Value: 50

### PAHAWH_HMONG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAHAWH_HMONG: Int
```

ISO 15924 script code

 Value: 75

### PALMYRENE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PALMYRENE: Int
```

ISO 15924 script code

 Value: 144

### PAU_CIN_HAU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAU_CIN_HAU: Int
```

ISO 15924 script code

 Value: 165

### PHAGS_PA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHAGS_PA: Int
```

ISO 15924 script code

 Value: 90

### PHOENICIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHOENICIAN: Int
```

ISO 15924 script code

 Value: 91

### PHONETIC_POLLARD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHONETIC_POLLARD: Int
```

ISO 15924 script code

 Value: 92

### PSALTER_PAHLAVI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PSALTER_PAHLAVI: Int
```

ISO 15924 script code

 Value: 123

### REJANG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REJANG: Int
```

ISO 15924 script code

 Value: 110

### RONGORONGO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RONGORONGO: Int
```

ISO 15924 script code

 Value: 93

### RUNIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RUNIC: Int
```

Runic

 Value: 32

### SAMARITAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMARITAN: Int
```

ISO 15924 script code

 Value: 126

### SARATI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SARATI: Int
```

ISO 15924 script code

 Value: 94

### SAURASHTRA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAURASHTRA: Int
```

ISO 15924 script code

 Value: 111

### SHARADA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHARADA: Int
```

ISO 15924 script code

 Value: 151

### SHAVIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SHAVIAN: Int
```

Shavian Script in Unicode 4

 Value: 51

### SIDDHAM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIDDHAM: Int
```

ISO 15924 script code

 Value: 166

### SIDETIC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIDETIC: Int
```

 Value: 209

### SIGN_WRITING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGN_WRITING: Int
```

ISO 15924 script code for Sutton SignWriting

 Value: 112

### SIMPLIFIED_HAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIMPLIFIED_HAN: Int
```

ISO 15924 script code

 Value: 73

### SINDHI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SINDHI: Int
```

ISO 15924 script code

 Value: 145

### SINHALA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SINHALA: Int
```

Sinhala

 Value: 33

### SOGDIAN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOGDIAN: Int
```

 Value: 183

### SORA_SOMPENG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SORA_SOMPENG: Int
```

ISO 15924 script code

 Value: 152

### SOYOMBO

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SOYOMBO: Int
```

ISO 15924 script code

 Value: 176

### SUNDANESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUNDANESE: Int
```

ISO 15924 script code

 Value: 113

### SUNUWAR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SUNUWAR: Int
```

 Value: 205

### SYLOTI_NAGRI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYLOTI_NAGRI: Int
```

Script in Unicode 4.1

 Value: 58

### SYMBOLS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYMBOLS: Int
```

ISO 15924 script code

 Value: 129

### SYMBOLS_EMOJI

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYMBOLS_EMOJI: Int
```

ISO 15924 script code

 Value: 174

### SYRIAC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SYRIAC: Int
```

Syriac

 Value: 34

### TAGALOG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAGALOG: Int
```

Tagalog

 Value: 42

### TAGBANWA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAGBANWA: Int
```

Tagbanwa

 Value: 45

### TAI_LE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAI_LE: Int
```

Tai Le Script in Unicode 4

 Value: 52

### TAI_VIET

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAI_VIET: Int
```

ISO 15924 script code

 Value: 127

### TAI_YO

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAI_YO: Int
```

 Value: 210

### TAKRI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAKRI: Int
```

ISO 15924 script code

 Value: 153

### TAMIL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAMIL: Int
```

Tamil

 Value: 35

### TANGSA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TANGSA: Int
```

 Value: 195

### TANGUT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TANGUT: Int
```

ISO 15924 script code

 Value: 154

### TELUGU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TELUGU: Int
```

Telugu

 Value: 36

### TENGWAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TENGWAR: Int
```

ISO 15924 script code

 Value: 98

### THAANA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THAANA: Int
```

Thana

 Value: 37

### THAI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val THAI: Int
```

Thai

 Value: 38

### TIBETAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIBETAN: Int
```

Tibetan

 Value: 39

### TIFINAGH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIFINAGH: Int
```

Script in Unicode 4.1

 Value: 60

### TIRHUTA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TIRHUTA: Int
```

ISO 15924 script code

 Value: 158

### TODHRI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TODHRI: Int
```

 Value: 206

### TOLONG_SIKI

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOLONG_SIKI: Int
```

 Value: 211

### TOTO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TOTO: Int
```

 Value: 196

### TRADITIONAL_HAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRADITIONAL_HAN: Int
```

ISO 15924 script code

 Value: 74

### TRADITIONAL_HAN_WITH_LATIN

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRADITIONAL_HAN_WITH_LATIN: Int
```

 Value: 212

### TULU_TIGALARI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TULU_TIGALARI: Int
```

 Value: 207

### UCAS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UCAS: Int
```

Unified Canadian Aboriginal Symbols (alias)

 Value: 40

### UGARITIC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UGARITIC: Int
```

Ugaritic Script in Unicode 4

 Value: 53

### UNKNOWN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN: Int
```

ISO 15924 script code

 Value: 103

### UNWRITTEN_LANGUAGES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNWRITTEN_LANGUAGES: Int
```

ISO 15924 script code

 Value: 102

### VAI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VAI: Int
```

ISO 15924 script code

 Value: 99

### VISIBLE_SPEECH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VISIBLE_SPEECH: Int
```

ISO 15924 script code

 Value: 100

### VITHKUQI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VITHKUQI: Int
```

 Value: 197

### WANCHO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WANCHO: Int
```

 Value: 188

### WARANG_CITI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WARANG_CITI: Int
```

ISO 15924 script code

 Value: 146

### WESTERN_SYRIAC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WESTERN_SYRIAC: Int
```

ISO 15924 script code

 Value: 96

### WOLEAI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WOLEAI: Int
```

ISO 15924 script code

 Value: 155

### YEZIDI

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YEZIDI: Int
```

 Value: 192

### YI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val YI: Int
```

Yi syllables

 Value: 41

### ZANABAZAR_SQUARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ZANABAZAR_SQUARE: Int
```

ISO 15924 script code

 Value: 177

## Public methods

### breaksBetweenLetters

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun breaksBetweenLetters(script: Int): Boolean
```

Returns true if the script allows line breaks between letters (excluding hyphenation). Such a script typically requires dictionary-based line breaking. For example, Hani and Thai.

| Parameters ||
|---|---|
| `script` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the script allows line breaks between letters |

### getCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getCode(locale: ULocale!): IntArray!
```

Gets a script codes associated with the given locale or ISO 15924 abbreviation or name. Returns MALAYAM given "Malayam" OR "Mlym". Returns LATIN given "en" OR "en_US"

| Parameters ||
|---|---|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!: ULocale |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | The script codes array. null if the code cannot be found. |

### getCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getCode(nameOrAbbrOrLocale: String!): IntArray!
```

Gets the script codes associated with the given locale or ISO 15924 abbreviation or name. Returns MALAYAM given "Malayam" OR "Mlym". Returns LATIN given "en" OR "en_US"

Note: To search by short or long script alias only, use `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#getCodeFromName(kotlin.String)` instead. That does a fast lookup with no access of the locale data.

| Parameters ||
|---|---|
| `nameOrAbbrOrLocale` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: name of the script or ISO 15924 code or locale |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | The script codes array. null if the code cannot be found. |

### getCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getCode(locale: Locale!): IntArray!
```

Gets a script codes associated with the given locale or ISO 15924 abbreviation or name. Returns MALAYAM given "Malayam" OR "Mlym". Returns LATIN given "en" OR "en_US"

| Parameters ||
|---|---|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!: Locale |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | The script codes array. null if the code cannot be found. |

### getCodeFromName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getCodeFromName(nameOrAbbr: String!): Int
```

Returns the script code associated with the given Unicode script property alias (name or abbreviation). Short aliases are ISO 15924 script codes. Returns MALAYAM given "Malayam" OR "Mlym".

| Parameters ||
|---|---|
| `nameOrAbbr` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: name of the script or ISO 15924 code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The script code value, or INVALID_CODE if the code cannot be found. |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getName(scriptCode: Int): String!
```

Returns the long Unicode script name, if there is one. Otherwise returns the 4-letter ISO 15924 script code. Returns "Malayam" given MALAYALAM.

| Parameters ||
|---|---|
| `scriptCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): int script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | long script name as given in PropertyValueAliases.txt, or the 4-letter code |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the script code is not valid |

### getSampleString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSampleString(script: Int): String!
```

Returns the script sample character string. This string normally consists of one code point but might be longer. The string is empty if the script is not encoded.

| Parameters ||
|---|---|
| `script` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the sample character string |

### getScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getScript(codepoint: Int): Int
```

Gets the script code associated with the given codepoint. Returns UScript.MALAYAM given 0x0D02

| Parameters ||
|---|---|
| `codepoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): UChar32 codepoint |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The script code |

### getScriptExtensions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getScriptExtensions(
    c: Int, 
    set: BitSet!
): Int
```

Sets code point c's Script_Extensions as script code integers into the output BitSet.

- If c does have Script_Extensions, then the return value is the negative number of Script_Extensions codes (= -set.cardinality()); in this case, the Script property value (normally Common or Inherited) is not included in the set.
- If c does not have Script_Extensions, then the one Script code is put into the set and also returned.
- If c is not a valid code point, then the one `https://developer.android.com/reference/kotlin/android/icu/lang/UScript#UNKNOWN:kotlin.Int` code is put into the set and also returned.

In other words, if the return value is non-negative, it is c's single Script code and the set contains exactly this Script code. If the return value is -n, then the set contains c's n\>=2 Script_Extensions script codes.

<br />

Some characters are commonly used in multiple scripts. For more information, see UAX #24: http://www.unicode.org/reports/tr24/.

| Parameters ||
|---|---|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): code point |
| `set` | [BitSet](https://developer.android.com/reference/kotlin/java/util/BitSet.html#)!: set of script code integers; will be cleared, then bits are set corresponding to c's Script_Extensions |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | negative number of script codes in c's Script_Extensions, or the non-negative single Script value |

### getShortName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getShortName(scriptCode: Int): String!
```

Returns the 4-letter ISO 15924 script code, which is the same as the short Unicode script name if Unicode has names for the script. Returns "Mlym" given MALAYALAM.

| Parameters ||
|---|---|
| `scriptCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): int script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | short script name (4-letter code) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the script code is not valid |

### getUsage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getUsage(script: Int): UScript.ScriptUsage!
```

Returns the script usage according to UAX #31 Unicode Identifier and Pattern Syntax. Returns `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.ScriptUsage` if the script is not encoded in Unicode.

| Parameters ||
|---|---|
| `script` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): script code |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.ScriptUsage!` | script usage |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.ScriptUsage`

### hasScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hasScript(
    c: Int, 
    sc: Int
): Boolean
```

Do the Script_Extensions of code point c contain script sc? If c does not have explicit Script_Extensions, then this tests whether c has the Script property value sc.

Some characters are commonly used in multiple scripts. For more information, see UAX #24: http://www.unicode.org/reports/tr24/.

| Parameters ||
|---|---|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): code point |
| `sc` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if sc is in Script_Extensions(c) |

### isCased

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isCased(script: Int): Boolean
```

Returns true if in modern (or most recent) usage of the script case distinctions are customary. For example, Latn and Cyrl.

| Parameters ||
|---|---|
| `script` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the script is cased |

### isRightToLeft

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isRightToLeft(script: Int): Boolean
```

Returns true if the script is written right-to-left. For example, Arab and Hebr.

| Parameters ||
|---|---|
| `script` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): script code |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the script is right-to-left |

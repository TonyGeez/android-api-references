# android.icu.util

# android.icu.util

Kotlin | [Java](https://developer.android.com/reference/android/icu/util/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [Freezable](https://developer.android.com/reference/kotlin/android/icu/util/Freezable) | Provides a flexible mechanism for controlling access, without requiring that a class be immutable. |
| --- | --- |
| [RangeValueIterator](https://developer.android.com/reference/kotlin/android/icu/util/RangeValueIterator) | Interface for enabling iteration over sets of \<int index, int value\>, where index is the sorted integer index in ascending order and value, its associated integer value. |
| [ValueIterator](https://developer.android.com/reference/kotlin/android/icu/util/ValueIterator) | Interface for enabling iteration over sets of \<int, Object\>, where int is the sorted integer index in ascending order, and Object its associated value. |

## Classes

| [BuddhistCalendar](https://developer.android.com/reference/kotlin/android/icu/util/BuddhistCalendar) | `BuddhistCalendar` is a subclass of `GregorianCalendar` that numbers years since the birth of the Buddha. |
| --- | --- |
| [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar) | **\[icu enhancement\]** ICU's replacement for [java.util.Calendar](https://developer.android.com/reference/kotlin/java/util/Calendar.html#). |
| [ChineseCalendar](https://developer.android.com/reference/kotlin/android/icu/util/ChineseCalendar) | `ChineseCalendar` is a concrete subclass of [Calendar](https://developer.android.com/reference/kotlin/android/icu/util/Calendar) that implements a traditional Chinese calendar. |
| [CopticCalendar](https://developer.android.com/reference/kotlin/android/icu/util/CopticCalendar) | Implement the Coptic calendar system. |
| --- | --- |
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency) | A class encapsulating a currency, as defined by ISO 4217. |
| [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount) | An amount of currency, consisting of a Number and a Currency. |
| [DateInterval](https://developer.android.com/reference/kotlin/android/icu/util/DateInterval) | This class represents date interval. |
| --- | --- |
| [EthiopicCalendar](https://developer.android.com/reference/kotlin/android/icu/util/EthiopicCalendar) | Implement the Ethiopic calendar system. |
| [GregorianCalendar](https://developer.android.com/reference/kotlin/android/icu/util/GregorianCalendar) | **\[icu enhancement\]** ICU's replacement for [java.util.GregorianCalendar](https://developer.android.com/reference/kotlin/java/util/GregorianCalendar.html#). |
| [HebrewCalendar](https://developer.android.com/reference/kotlin/android/icu/util/HebrewCalendar) | `HebrewCalendar` is a subclass of `Calendar` that that implements the traditional Hebrew calendar. |
| --- | --- |
| [IndianCalendar](https://developer.android.com/reference/kotlin/android/icu/util/IndianCalendar) | `IndianCalendar` is a subclass of `GregorianCalendar` that numbers years since the birth of the Buddha. |
| [IslamicCalendar](https://developer.android.com/reference/kotlin/android/icu/util/IslamicCalendar) | `IslamicCalendar` is a subclass of `Calendar` that that implements the Islamic civil and religious calendars. |
| [JapaneseCalendar](https://developer.android.com/reference/kotlin/android/icu/util/JapaneseCalendar) | `JapaneseCalendar` is a subclass of `GregorianCalendar` that numbers years and eras based on the reigns of the Japanese emperors. |
| --- | --- |
| [LocaleData](https://developer.android.com/reference/kotlin/android/icu/util/LocaleData) | A class for accessing miscellaneous data in the locale bundles |
| [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure) | An amount of a specified unit, consisting of a Number and a Unit. |
| [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit) | A unit such as length, mass, volume, currency, etc. |
| --- | --- |
| [Output](https://developer.android.com/reference/kotlin/android/icu/util/Output) | Simple struct-like class for output parameters. |
| [TaiwanCalendar](https://developer.android.com/reference/kotlin/android/icu/util/TaiwanCalendar) | `TaiwanCalendar` is a subclass of `GregorianCalendar` that numbers years since 1912. |
| [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit) | Measurement unit for time units. |
| --- | --- |
| [TimeZone](https://developer.android.com/reference/kotlin/android/icu/util/TimeZone) | **\[icu enhancement\]** ICU's replacement for [java.util.TimeZone](https://developer.android.com/reference/kotlin/java/util/TimeZone.html#). |
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale) | **\[icu enhancement\]** ICU's replacement for [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |
| [UniversalTimeScale](https://developer.android.com/reference/kotlin/android/icu/util/UniversalTimeScale) | There are quite a few different conventions for binary datetime, depending on different platforms and protocols. |
| --- | --- |
| [VersionInfo](https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo) | Class to store version numbers of the form major. |

## Exceptions

| [ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException) | Unchecked version of [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#). |
| --- | --- |
| [IllformedLocaleException](https://developer.android.com/reference/kotlin/android/icu/util/IllformedLocaleException) | Thrown by methods in [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale) and [ULocale.Builder](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder) to indicate that an argument is not a well-formed BCP 47 tag. |

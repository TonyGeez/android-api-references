# IDNA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IDNA

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/IDNA "View this page in Java") 

```
abstract class IDNA
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.IDNA](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#) |

Abstract base class for IDNA processing. See http://www.unicode.org/reports/tr46/ and http://www.ietf.org/rfc/rfc3490.txt

The IDNA class is not intended for public subclassing.

The non-static methods implement UTS #46 and IDNA2008. IDNA2008 is implemented according to UTS #46, see [getUTS46Instance(int)](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#getUTS46Instance(kotlin.Int)).

IDNA2003 is obsolete. The static methods implement IDNA2003. They are all deprecated.

IDNA2003 API Overview:

The static IDNA API methods implement the IDNA protocol as defined in the [IDNA RFC](http://www.ietf.org/rfc/rfc3490.txt). The draft defines 2 operations: ToASCII and ToUnicode. Domain labels containing non-ASCII code points are required to be processed by ToASCII operation before passing it to resolver libraries. Domain names that are obtained from resolver libraries are required to be processed by ToUnicode operation before displaying the domain name to the user. IDNA requires that implementations process input strings with [Nameprep](http://www.ietf.org/rfc/rfc3491.txt), which is a profile of [Stringprep](http://www.ietf.org/rfc/rfc3454.txt), and then with [Punycode](http://www.ietf.org/rfc/rfc3492.txt). Implementations of IDNA MUST fully implement Nameprep and Punycode; neither Nameprep nor Punycode are optional. The input and output of ToASCII and ToUnicode operations are Unicode and are designed to be chainable, i.e., applying ToASCII or ToUnicode operations multiple times to an input string will yield the same result as applying the operation once. ToUnicode(ToUnicode(ToUnicode...(ToUnicode(string)))) == ToUnicode(string) ToASCII(ToASCII(ToASCII...(ToASCII(string))) == ToASCII(string).

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------|
| | [Error](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Error) IDNA error bit set values. |
| | [Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info) Output container for IDNA processing errors. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHECK_BIDI](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#CHECK_BIDI:kotlin.Int) IDNA option to check for whether the input conforms to the BiDi rules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHECK_CONTEXTJ](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#CHECK_CONTEXTJ:kotlin.Int) IDNA option to check for whether the input conforms to the CONTEXTJ rules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHECK_CONTEXTO](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#CHECK_CONTEXTO:kotlin.Int) IDNA option to check for whether the input conforms to the CONTEXTO rules. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#DEFAULT:kotlin.Int) Default options value: None of the other options are set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONTRANSITIONAL_TO_ASCII](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#NONTRANSITIONAL_TO_ASCII:kotlin.Int) IDNA option for nontransitional processing in ToASCII(). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONTRANSITIONAL_TO_UNICODE](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#NONTRANSITIONAL_TO_UNICODE:kotlin.Int) IDNA option for nontransitional processing in ToUnicode(). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USE_STD3_RULES](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#USE_STD3_RULES:kotlin.Int) Option to check whether the input conforms to the STD3 ASCII rules, for example the restriction of labels to LDH characters (ASCII Letters, Digits and Hyphen-Minus). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [IDNA](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#)! | [getUTS46Instance](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#getUTS46Instance(kotlin.Int))`(`options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns an IDNA instance which implements UTS #46. |
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [labelToASCII](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#labelToASCII(kotlin.CharSequence,%20java.lang.StringBuilder,%20android.icu.text.IDNA.Info))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `dest:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `info:` ` [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!`)` Converts a single domain name label into its ASCII form for DNS lookup. |
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [labelToUnicode](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#labelToUnicode(kotlin.CharSequence,%20java.lang.StringBuilder,%20android.icu.text.IDNA.Info))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `dest:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `info:` ` [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!`)` Converts a single domain name label into its Unicode form for human-readable display. |
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [nameToASCII](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#nameToASCII(kotlin.CharSequence,%20java.lang.StringBuilder,%20android.icu.text.IDNA.Info))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `dest:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `info:` ` [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!`)` Converts a whole domain name into its ASCII form for DNS lookup. |
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [nameToUnicode](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#nameToUnicode(kotlin.CharSequence,%20java.lang.StringBuilder,%20android.icu.text.IDNA.Info))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `dest:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `info:` ` [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!`)` Converts a whole domain name into its Unicode form for human-readable display. |

## Constants

### CHECK_BIDI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHECK_BIDI: Int
```

IDNA option to check for whether the input conforms to the BiDi rules. For use in static worker and factory methods.

This option is ignored by the IDNA2003 implementation. (IDNA2003 always performs a BiDi check.) 

 Value: 4

### CHECK_CONTEXTJ

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHECK_CONTEXTJ: Int
```

IDNA option to check for whether the input conforms to the CONTEXTJ rules. For use in static worker and factory methods.

This option is ignored by the IDNA2003 implementation. (The CONTEXTJ check is new in IDNA2008.) 

 Value: 8

### CHECK_CONTEXTO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHECK_CONTEXTO: Int
```

IDNA option to check for whether the input conforms to the CONTEXTO rules. For use in static worker and factory methods.

This option is ignored by the IDNA2003 implementation. (The CONTEXTO check is new in IDNA2008.)

This is for use by registries for IDNA2008 conformance. UTS #46 does not require the CONTEXTO check. 

 Value: 64

### DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: Int
```

Default options value: None of the other options are set. 

 Value: 0

### NONTRANSITIONAL_TO_ASCII

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONTRANSITIONAL_TO_ASCII: Int
```

IDNA option for nontransitional processing in ToASCII(). For use in static worker and factory methods.

By default, ToASCII() uses transitional processing. Unicode 15.1 UTS #46 deprecated transitional processing.

This option is ignored by the IDNA2003 implementation. (This is only relevant for compatibility of newer IDNA implementations with IDNA2003.) 

 Value: 16

### NONTRANSITIONAL_TO_UNICODE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONTRANSITIONAL_TO_UNICODE: Int
```

IDNA option for nontransitional processing in ToUnicode(). For use in static worker and factory methods.

By default, ToUnicode() uses transitional processing. Unicode 15.1 UTS #46 deprecated transitional processing.

This option is ignored by the IDNA2003 implementation. (This is only relevant for compatibility of newer IDNA implementations with IDNA2003.) 

 Value: 32

### USE_STD3_RULES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USE_STD3_RULES: Int
```

Option to check whether the input conforms to the STD3 ASCII rules, for example the restriction of labels to LDH characters (ASCII Letters, Digits and Hyphen-Minus). For use in static worker and factory methods. 

 Value: 2

## Public methods

### getUTS46Instance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getUTS46Instance(options: Int): IDNA!
```

Returns an IDNA instance which implements UTS #46. Returns an unmodifiable instance, owned by the caller. Cache it for multiple operations, and delete it when done. The instance is thread-safe, that is, it can be used concurrently.

UTS #46 defines Unicode IDNA Compatibility Processing, updated to the latest version of Unicode and compatible with both IDNA2003 and IDNA2008.

The worker functions use transitional processing, including deviation mappings, unless [NONTRANSITIONAL_TO_ASCII](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#NONTRANSITIONAL_TO_ASCII:kotlin.Int) or [NONTRANSITIONAL_TO_UNICODE](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#NONTRANSITIONAL_TO_UNICODE:kotlin.Int) is used in which case the deviation characters are passed through without change.**Unicode 15.1 UTS #46 deprecated transitional processing.**

Disallowed characters are mapped to U+FFFD.

Operations with the UTS #46 instance do not support the ALLOW_UNASSIGNED option.

By default, the UTS #46 implementation allows all ASCII characters (as valid or mapped). When the USE_STD3_RULES option is used, ASCII characters other than letters, digits, hyphen (LDH) and dot/full stop are disallowed and mapped to U+FFFD.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Bit set to modify the processing and error checking. These should include [IDNA.DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#DEFAULT:kotlin.Int), or [IDNA.NONTRANSITIONAL_TO_ASCII](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#NONTRANSITIONAL_TO_ASCII:kotlin.Int)| [IDNA.NONTRANSITIONAL_TO_UNICODE](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#NONTRANSITIONAL_TO_UNICODE:kotlin.Int). |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------|
| [IDNA](https://developer.android.com/reference/kotlin/android/icu/text/IDNA#)! | the UTS #46 IDNA instance, if successful |

### labelToASCII

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun labelToASCII(
    label: CharSequence!, 
    dest: StringBuilder!, 
    info: IDNA.Info!
): StringBuilder!
```

Converts a single domain name label into its ASCII form for DNS lookup. If any processing step fails, then info.hasErrors() will be true and the result might not be an ASCII string. The label might be modified according to the types of errors. Labels with severe errors will be left in (or turned into) their Unicode form.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Input domain name label |
| `dest` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:Destination string object |
| `info` | [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!:Output container of IDNA processing details. |

| Return ||
|------------------------------------------------------------------------------------------------|------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | dest |

### labelToUnicode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun labelToUnicode(
    label: CharSequence!, 
    dest: StringBuilder!, 
    info: IDNA.Info!
): StringBuilder!
```

Converts a single domain name label into its Unicode form for human-readable display. If any processing step fails, then info.hasErrors() will be true. The label might be modified according to the types of errors.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Input domain name label |
| `dest` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:Destination string object |
| `info` | [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!:Output container of IDNA processing details. |

| Return ||
|------------------------------------------------------------------------------------------------|------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | dest |

### nameToASCII

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nameToASCII(
    name: CharSequence!, 
    dest: StringBuilder!, 
    info: IDNA.Info!
): StringBuilder!
```

Converts a whole domain name into its ASCII form for DNS lookup. If any processing step fails, then info.hasErrors() will be true and the result might not be an ASCII string. The domain name might be modified according to the types of errors. Labels with severe errors will be left in (or turned into) their Unicode form.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Input domain name |
| `dest` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:Destination string object |
| `info` | [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!:Output container of IDNA processing details. |

| Return ||
|------------------------------------------------------------------------------------------------|------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | dest |

### nameToUnicode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nameToUnicode(
    name: CharSequence!, 
    dest: StringBuilder!, 
    info: IDNA.Info!
): StringBuilder!
```

Converts a whole domain name into its Unicode form for human-readable display. If any processing step fails, then info.hasErrors() will be true. The domain name might be modified according to the types of errors.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Input domain name |
| `dest` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:Destination string object |
| `info` | [IDNA.Info](https://developer.android.com/reference/kotlin/android/icu/text/IDNA.Info)!:Output container of IDNA processing details. |

| Return ||
|------------------------------------------------------------------------------------------------|------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | dest |

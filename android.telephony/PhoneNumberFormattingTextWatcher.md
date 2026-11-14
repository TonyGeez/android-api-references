# PhoneNumberFormattingTextWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneNumberFormattingTextWatcher

Kotlin| [Java](https://developer.android.com/reference/android/telephony/PhoneNumberFormattingTextWatcher "View this page in Java") 
| --- | --- |

```
open class PhoneNumberFormattingTextWatcher : TextWatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher#) |

| **This class was deprecated in API level 35.**
|
| This is a thin wrapper on a \`libphonenumber\` \`AsYouTypeFormatter\`; it is recommended to use that instead.

Watches a [android.widget.TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) and if a phone number is entered will format it.

Stop formatting when the user

- Inputs non-dialable characters
- Removes the separator in the middle of string.

The formatting will be restarted once the text is cleared.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher#PhoneNumberFormattingTextWatcher())`()` The formatting is based on the current system locale and future locale changes may not take effect on this instance. |
| [PhoneNumberFormattingTextWatcher](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher#PhoneNumberFormattingTextWatcher(kotlin.String))`(`countryCode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The formatting is based on the given`countryCode`. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterTextChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher#afterTextChanged(android.text.Editable))`(`s:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeTextChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher#beforeTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTextChanged](https://developer.android.com/reference/kotlin/android/telephony/PhoneNumberFormattingTextWatcher#onTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `before:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

## Public constructors

### PhoneNumberFormattingTextWatcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PhoneNumberFormattingTextWatcher()
```

The formatting is based on the current system locale and future locale changes may not take effect on this instance. 

### PhoneNumberFormattingTextWatcher

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PhoneNumberFormattingTextWatcher(countryCode: String!)
```

The formatting is based on the given`countryCode`. 
This method may take several seconds to complete, so it should only be called from a worker thread.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `countryCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ISO 3166-1 two-letter country code that indicates the country/region where the phone number is being entered. |

## Public methods

### afterTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun afterTextChanged(s: Editable!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### beforeTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun beforeTextChanged(
    s: CharSequence!, 
    start: Int, 
    count: Int, 
    after: Int
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### onTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTextChanged(
    s: CharSequence!, 
    start: Int, 
    before: Int, 
    count: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

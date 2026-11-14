# Sanitizer

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Sanitizer

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/Sanitizer "View this page in Java") 
| --- | --- |

```
interface Sanitizer
```

| [android.service.autofill.Sanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/Sanitizer#) |

| Known Direct Subclasses [DateValueSanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/DateValueSanitizer), [TextValueSanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/TextValueSanitizer) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DateValueSanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/DateValueSanitizer) | Sanitizes a date [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#) using a [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat.html#). | | [TextValueSanitizer](https://developer.android.com/reference/kotlin/android/service/autofill/TextValueSanitizer) | Sanitizes a text [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#) using a regular expression (regex) substitution. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Helper class used to sanitize user input before using it in a save request.

Typically used to avoid displaying the save UI for values that are autofilled but reformatted by the app---for example, if the autofill service sends a credit card number value as "004815162342108" and the app automatically changes it to "0048 1516 2342 108".

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary

# Sanitizer

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Sanitizer

Kotlin| [Java](../android/service/autofill/Sanitizer.md) 
| --- | --- |

```
interface Sanitizer
```

| [android.service.autofill.Sanitizer](../android/service/autofill/Sanitizer.md) |

| Known Direct Subclasses [DateValueSanitizer](../android/service/autofill/DateValueSanitizer.md), [TextValueSanitizer](../android/service/autofill/TextValueSanitizer.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DateValueSanitizer](../android/service/autofill/DateValueSanitizer.md) | Sanitizes a date [AutofillValue](../android/view/autofill/AutofillValue.md) using a [DateFormat](../android/icu/text/DateFormat.md). | | [TextValueSanitizer](../android/service/autofill/TextValueSanitizer.md) | Sanitizes a text [AutofillValue](../android/view/autofill/AutofillValue.md) using a regular expression (regex) substitution. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Helper class used to sanitize user input before using it in a save request.

Typically used to avoid displaying the save UI for values that are autofilled but reformatted by the app---for example, if the autofill service sends a credit card number value as "004815162342108" and the app automatically changes it to "0048 1516 2342 108".

**Note:**This interface is not meant to be implemented by app developers; only implementations provided by the Android System can be used in other Autofill APIs.

## Summary

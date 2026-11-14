# Validator

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validator

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/Validator "View this page in Java") 
| --- | --- |

```
interface Validator
```

| [android.service.autofill.Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator#) |

| Known Direct Subclasses [LuhnChecksumValidator](https://developer.android.com/reference/kotlin/android/service/autofill/LuhnChecksumValidator), [RegexValidator](https://developer.android.com/reference/kotlin/android/service/autofill/RegexValidator) |------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------| | [LuhnChecksumValidator](https://developer.android.com/reference/kotlin/android/service/autofill/LuhnChecksumValidator) | Validator that returns`true`if the number created by concatenating all given fields pass a Luhn algorithm checksum. | | [RegexValidator](https://developer.android.com/reference/kotlin/android/service/autofill/RegexValidator) | Defines if a field is valid based on a regular expression (regex). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Class used to define whether a condition is satisfied.

Typically used to avoid displaying the save UI when the user input is invalid.

## Summary

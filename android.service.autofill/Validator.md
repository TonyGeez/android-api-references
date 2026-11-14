# Validator

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validator

Kotlin| [Java](../android/service/autofill/Validator.md) 
| --- | --- |

```
interface Validator
```

| [android.service.autofill.Validator](../android/service/autofill/Validator.md) |

| Known Direct Subclasses [LuhnChecksumValidator](../android/service/autofill/LuhnChecksumValidator.md), [RegexValidator](../android/service/autofill/RegexValidator.md) |------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------| | [LuhnChecksumValidator](../android/service/autofill/LuhnChecksumValidator.md) | Validator that returns`true`if the number created by concatenating all given fields pass a Luhn algorithm checksum. | | [RegexValidator](../android/service/autofill/RegexValidator.md) | Defines if a field is valid based on a regular expression (regex). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Class used to define whether a condition is satisfied.

Typically used to avoid displaying the save UI when the user input is invalid.

## Summary

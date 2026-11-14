# Validators

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validators

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/Validators "View this page in Java") 
| --- | --- |

```
class Validators
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.Validators](https://developer.android.com/reference/kotlin/android/service/autofill/Validators#) |

Factory for [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) operations.

See [SaveInfo.Builder.setValidator(Validator)](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo.Builder#setValidator(android.service.autofill.Validator))for examples.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | [and](https://developer.android.com/reference/kotlin/android/service/autofill/Validators#and(android.service.autofill.Validator))`(`vararg` `validators:` ` [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator)!`)` Creates a validator that is only valid if all`validators`are valid. |
| static [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | [not](https://developer.android.com/reference/kotlin/android/service/autofill/Validators#not(android.service.autofill.Validator))`(`validator:` ` [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator)`)` Creates a validator that is valid when`validator`is not, and vice versa. |
| static [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | [or](https://developer.android.com/reference/kotlin/android/service/autofill/Validators#or(android.service.autofill.Validator))`(`vararg` `validators:` ` [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator)!`)` Creates a validator that is valid if any of the`validators`is valid. |
| --- | --- |

## Public methods

### and

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun and(vararg validators: Validator!): Validator
```

Creates a validator that is only valid if all`validators`are valid.

Used to represent an`AND`boolean operation in a chain of validators.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `validators` | [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator)!:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any element of`validators`is an instance of a class that is not provided by the Android System. |

### not

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun not(validator: Validator): Validator
```

Creates a validator that is valid when`validator`is not, and vice versa.

Used to represent a`NOT`boolean operation in a chain of validators.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `validator` | [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`validator`is an instance of a class that is not provided by the Android System. |

### or

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun or(vararg validators: Validator!): Validator
```

Creates a validator that is valid if any of the`validators`is valid.

Used to represent an`OR`boolean operation in a chain of validators.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| `validators` | [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator)!:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [Validator](https://developer.android.com/reference/kotlin/android/service/autofill/Validator) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any element of`validators`is an instance of a class that is not provided by the Android System. |

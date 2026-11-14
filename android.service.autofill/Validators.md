# Validators

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validators

Kotlin| [Java](Validators.md) 
| --- | --- |

```
class Validators
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.Validators](Validators.md) |

Factory for [Validator](Validator.md) operations.

See [SaveInfo.Builder.setValidator(Validator)](../android/service/autofill/SaveInfo.Builder.md))for examples.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Validator](Validator.md) | [and](Validators.md))`(`vararg` `validators:` ` [Validator](Validator.md)!`)` Creates a validator that is only valid if all`validators`are valid. |
| static [Validator](Validator.md) | [not](Validators.md))`(`validator:` ` [Validator](Validator.md)`)` Creates a validator that is valid when`validator`is not, and vice versa. |
| static [Validator](Validator.md) | [or](Validators.md))`(`vararg` `validators:` ` [Validator](Validator.md)!`)` Creates a validator that is valid if any of the`validators`is valid. |
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
| `validators` | [Validator](Validator.md)!:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [Validator](Validator.md) | This value cannot be`null`. |

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
| `validator` | [Validator](Validator.md):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [Validator](Validator.md) | This value cannot be`null`. |

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
| `validators` | [Validator](Validator.md)!:This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [Validator](Validator.md) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any element of`validators`is an instance of a class that is not provided by the Android System. |

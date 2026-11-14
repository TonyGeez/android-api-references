# FieldClassification

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FieldClassification

Kotlin| [Java](../android/service/autofill/FieldClassification.md) 
| --- | --- |

```
class FieldClassification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.FieldClassification](../android/service/autofill/FieldClassification.md) |

Represents the [field classification](../android/service/autofill/AutofillService.md) results for a given field.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Match](../android/service/autofill/FieldClassification.Match.md) Represents the score of a [UserData](../android/service/autofill/UserData.md) entry for the field. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FieldClassification.Match](../android/service/autofill/FieldClassification.Match.md)!\> | [getMatches](../android/service/autofill/FieldClassification.md))`()` Gets the [matches](../android/service/autofill/FieldClassification.Match.md) with the highest [scores](../android/service/autofill/FieldClassification.Match.md))(sorted in descending order). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/service/autofill/FieldClassification.md))`()` <br /> |

## Public methods

### getMatches

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatches(): MutableList<FieldClassification.Match!>
```

Gets the [matches](../android/service/autofill/FieldClassification.Match.md) with the highest [scores](../android/service/autofill/FieldClassification.Match.md))(sorted in descending order).

**Note:**There's no guarantee of how many matches will be returned. In fact, the Android System might return just the top match to minimize the impact of field classification in the device's health.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FieldClassification.Match](../android/service/autofill/FieldClassification.Match.md)!> | This value cannot be`null`. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

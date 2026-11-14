# FieldClassification

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FieldClassification

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/FieldClassification "View this page in Java") 

```
class FieldClassification
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.autofill.FieldClassification](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification#) |

Represents the [field classification](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService#FieldClassification) results for a given field.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Match](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match) Represents the score of a [UserData](https://developer.android.com/reference/kotlin/android/service/autofill/UserData) entry for the field. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FieldClassification.Match](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match)!\> | [getMatches](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification#getMatches())`()` Gets the [matches](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match) with the highest [scores](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match#getScore())(sorted in descending order). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification#toString())`()` <br /> |

## Public methods

### getMatches

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatches(): MutableList<FieldClassification.Match!>
```

Gets the [matches](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match) with the highest [scores](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match#getScore())(sorted in descending order).

**Note:**There's no guarantee of how many matches will be returned. In fact, the Android System might return just the top match to minimize the impact of field classification in the device's health.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FieldClassification.Match](https://developer.android.com/reference/kotlin/android/service/autofill/FieldClassification.Match)!> | This value cannot be`null`. |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

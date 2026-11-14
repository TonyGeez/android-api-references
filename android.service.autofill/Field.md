# Field

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Field

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/Field "View this page in Java") 
| --- | --- |

```
class Field
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.Field](https://developer.android.com/reference/kotlin/android/service/autofill/Field#) |

This class is used to set all information of a field. Such as the [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#) to be autofilled, a [explicit filter](https://developer.android.com/reference/kotlin/android/service/autofill/Field#Filtering), and presentations to be visualized, etc.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/autofill/Field.Builder) A builder for [Field](https://developer.android.com/reference/kotlin/android/service/autofill/Field#) |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pattern](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#)? | [getFilter](https://developer.android.com/reference/kotlin/android/service/autofill/Field#getFilter())`()` Regex used to determine if the dataset should be shown in the autofill UI; when`null`, it disables filtering on that dataset (this is the recommended approach when`value`is not`null`and field contains sensitive data such as passwords). |
| [Presentations](https://developer.android.com/reference/kotlin/android/service/autofill/Presentations)? | [getPresentations](https://developer.android.com/reference/kotlin/android/service/autofill/Field#getPresentations())`()` The presentations used to visualize this field in Autofill UI. |
| [AutofillValue](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillValue.html#)? | [getValue](https://developer.android.com/reference/kotlin/android/service/autofill/Field#getValue())`()` The value to be autofilled. |
| --- | --- |

## Public methods

### getFilter

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFilter(): Pattern?
```

Regex used to determine if the dataset should be shown in the autofill UI; when`null`, it disables filtering on that dataset (this is the recommended approach when`value`is not`null`and field contains sensitive data such as passwords). 

### getPresentations

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPresentations(): Presentations?
```

The presentations used to visualize this field in Autofill UI.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------------|
| [Presentations](https://developer.android.com/reference/kotlin/android/service/autofill/Presentations)? | This value may be`null`. |

### getValue

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): AutofillValue?
```

The value to be autofilled. Pass`null`if you do not have the value but the target view is a logical part of the dataset. For example, if the dataset needs authentication and you have no access to the value.

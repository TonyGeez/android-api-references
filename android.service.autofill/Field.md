# Field

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Field

Kotlin| [Java](Field.md) 
| --- | --- |

```
class Field
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.Field](Field.md) |

This class is used to set all information of a field. Such as the [AutofillValue](../android.view.autofill/AutofillValue.md) to be autofilled, a [explicit filter](Field.md), and presentations to be visualized, etc.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/autofill/Field.Builder.md) A builder for [Field](Field.md) |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pattern](../java.util.regex/Pattern.md)? | [getFilter](Field.md))`()` Regex used to determine if the dataset should be shown in the autofill UI; when`null`, it disables filtering on that dataset (this is the recommended approach when`value`is not`null`and field contains sensitive data such as passwords). |
| [Presentations](Presentations.md)? | [getPresentations](Field.md))`()` The presentations used to visualize this field in Autofill UI. |
| [AutofillValue](../android.view.autofill/AutofillValue.md)? | [getValue](Field.md))`()` The value to be autofilled. |
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
| [Presentations](Presentations.md)? | This value may be`null`. |

### getValue

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): AutofillValue?
```

The value to be autofilled. Pass`null`if you do not have the value but the target view is a logical part of the dataset. For example, if the dataset needs authentication and you have no access to the value.

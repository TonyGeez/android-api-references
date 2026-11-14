# AutoCompleteTextView.Validator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validator

Kotlin| [Java](../android/widget/AutoCompleteTextView.Validator.md) 
| --- | --- |

```
interface Validator
```

| [android.widget.AutoCompleteTextView.Validator](../android/widget/AutoCompleteTextView.Validator.md) |

This interface is used to make sure that the text entered in this TextView complies to a certain format. Since there is no foolproof way to prevent the user from leaving this View with an incorrect value in it, all we can do is try to fix it ourselves when this happens.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [fixText](../android/widget/AutoCompleteTextView.Validator.md))`(`invalidText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Corrects the specified text to make it valid. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](../android/widget/AutoCompleteTextView.Validator.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Validates the specified text. |

## Public methods

### fixText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun fixText(invalidText: CharSequence!): CharSequence!
```

Corrects the specified text to make it valid.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `invalidText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:A string that doesn't pass validation: isValid(invalidText) returns false |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | A string based on invalidText such as invoking isValid() on it returns true. |

**See Also**

- [#isValid(CharSequence)](../android/widget/AutoCompleteTextView.Validator.md)) 

### isValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(text: CharSequence!): Boolean
```

Validates the specified text.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true If the text currently in the text editor is valid. |

**See Also**

- [#fixText(CharSequence)](../android/widget/AutoCompleteTextView.Validator.md))

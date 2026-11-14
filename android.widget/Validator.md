# AutoCompleteTextView.Validator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Validator

Kotlin| [Java](https://developer.android.com/reference/android/widget/AutoCompleteTextView.Validator "View this page in Java") 

```
interface Validator
```

| [android.widget.AutoCompleteTextView.Validator](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.Validator#) |

This interface is used to make sure that the text entered in this TextView complies to a certain format. Since there is no foolproof way to prevent the user from leaving this View with an incorrect value in it, all we can do is try to fix it ourselves when this happens.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [fixText](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.Validator#fixText(kotlin.CharSequence))`(`invalidText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Corrects the specified text to make it valid. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.Validator#isValid(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Validates the specified text. |

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

- [#isValid(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.Validator#isValid(kotlin.CharSequence)) 

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

- [#fixText(CharSequence)](https://developer.android.com/reference/kotlin/android/widget/AutoCompleteTextView.Validator#fixText(kotlin.CharSequence))

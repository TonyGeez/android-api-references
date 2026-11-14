# UCharacterCategory

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UCharacterCategory

Kotlin| [Java](../android/icu/lang/UCharacterCategory.md) 
| --- | --- |

```
class UCharacterCategory : UCharacterEnums.ECharacterCategory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.lang.UCharacterCategory](../android/icu/lang/UCharacterCategory.md) |

Enumerated Unicode category types from the UnicodeData.txt file. Used as return results from [UCharacter](../android/icu/lang/UCharacter.md) Equivalent to icu's UCharCategory. Refer to [Unicode Consortium](http://www.unicode.org/Public/UNIDATA/UCD.html) for more information about UnicodeData.txt.

*NOTE:* the UCharacterCategory values are*not*compatible with those returned by java.lang.Character.getType. UCharacterCategory values match the ones used in ICU4C, while java.lang.Character type values, though similar, skip the value 17.

This class is not subclassable

## Summary

| Inherited constants ||
|---|---|
| From class [ECharacterCategory](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) |------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [COMBINING_SPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Mc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [CONNECTOR_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [CONTROL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [CURRENCY_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Sc <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DASH_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pd <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [DECIMAL_DIGIT_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Nd <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [ENCLOSING_MARK](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Me <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [END_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pe <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FINAL_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pf <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FINAL_QUOTE_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pf This name is compatible with java.lang.Character's name for this type. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [FORMAT](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cf <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [GENERAL_OTHER_TYPES](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cn Not Assigned (no characters in \[UnicodeData.txt\] have this property) <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [INITIAL_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pi <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [INITIAL_QUOTE_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Pi This name is compatible with java.lang.Character's name for this type. <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LETTER_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Nl <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LINE_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Zl <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LOWERCASE_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Ll <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MATH_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Sm <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MODIFIER_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lm <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MODIFIER_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Sk <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [NON_SPACING_MARK](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Mn <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lo <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_NUMBER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type No <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Po <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [OTHER_SYMBOL](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type So <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PARAGRAPH_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Zp <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [PRIVATE_USE](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Co <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SPACE_SEPARATOR](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Zs <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [START_PUNCTUATION](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Ps <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [SURROGATE](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Cs <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [TITLECASE_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lt <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [UNASSIGNED](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Unassigned character type <br /> | | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [UPPERCASE_LETTER](../android/icu/lang/UCharacterEnums.ECharacterCategory.md) <br /> Character type Lu <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](../android/icu/lang/UCharacterCategory.md))`(`category:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the name of the argument category |

## Public methods

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(category: Int): String!
```

Gets the name of the argument category

| Parameters ||
|------------|---------------------------------------------------------------------------------------------|
| `category` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):to retrieve name |

| Return ||
|-----------------------------------------------------------------------------------|---------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | category name |

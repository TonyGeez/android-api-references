# VirtualViewFillInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualViewFillInfo

Kotlin| [Java](https://developer.android.com/reference/android/view/autofill/VirtualViewFillInfo "View this page in Java") 

```
class VirtualViewFillInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.autofill.VirtualViewFillInfo](https://developer.android.com/reference/kotlin/android/view/autofill/VirtualViewFillInfo#) |

Information for the virtual view to the autofill framework.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/autofill/VirtualViewFillInfo.Builder) A builder for [VirtualViewFillInfo](https://developer.android.com/reference/kotlin/android/view/autofill/VirtualViewFillInfo#) |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getAutofillHints](https://developer.android.com/reference/kotlin/android/view/autofill/VirtualViewFillInfo#getAutofillHints())`()` Autofill hints of the virtual view. |

## Public methods

### getAutofillHints

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAutofillHints(): Array<String!>?
```

Autofill hints of the virtual view.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

**See Also**

- [android.view.View#setAutofillHints(String...)](https://developer.android.com/reference/kotlin/android/view/View.html#setAutofillHints(kotlin.String))

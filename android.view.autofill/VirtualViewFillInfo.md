# VirtualViewFillInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualViewFillInfo

Kotlin| [Java](../android/view/autofill/VirtualViewFillInfo.md) 
| --- | --- |

```
class VirtualViewFillInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.autofill.VirtualViewFillInfo](../android/view/autofill/VirtualViewFillInfo.md) |

Information for the virtual view to the autofill framework.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/autofill/VirtualViewFillInfo.Builder.md) A builder for [VirtualViewFillInfo](../android/view/autofill/VirtualViewFillInfo.md) |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getAutofillHints](../android/view/autofill/VirtualViewFillInfo.md))`()` Autofill hints of the virtual view. |

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

- [android.view.View#setAutofillHints(String...)](../android/view/View.md))

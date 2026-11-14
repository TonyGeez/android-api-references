# TransformationMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransformationMethod

Kotlin| [Java](https://developer.android.com/reference/android/text/method/TransformationMethod "View this page in Java") 
| --- | --- |

```
interface TransformationMethod
```

| [android.text.method.TransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/TransformationMethod#) |

| Known Direct Subclasses [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod), [ReplacementTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod) |---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod) | <br /> | | [ReplacementTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod) | This transformation method causes the characters in the [getOriginal](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal())array to be replaced by the corresponding characters in the [getReplacement](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement())array. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod), [SingleLineTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/SingleLineTransformationMethod) |---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod) | This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF). | | [SingleLineTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/SingleLineTransformationMethod) | This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

TextView uses TransformationMethods to do things like replacing the characters of passwords with dots, or keeping the newline characters from causing line breaks in single-line text fields.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTransformation](https://developer.android.com/reference/kotlin/android/text/method/TransformationMethod#getTransformation(kotlin.CharSequence,%20android.view.View))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Returns a CharSequence that is a transformation of the source text -- for example, replacing each character with a dot in a password field. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChanged](https://developer.android.com/reference/kotlin/android/text/method/TransformationMethod#onFocusChanged(android.view.View,%20kotlin.CharSequence,%20kotlin.Boolean,%20kotlin.Int,%20android.graphics.Rect))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `sourceText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `focused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `previouslyFocusedRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` This method is called when the TextView that uses this TransformationMethod gains or loses focus. |

## Public methods

### getTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTransformation(
    source: CharSequence!, 
    view: View!
): CharSequence!
```

Returns a CharSequence that is a transformation of the source text -- for example, replacing each character with a dot in a password field. Beware that the returned text must be exactly the same length as the source text, and that if the source text is Editable, the returned text must mirror it dynamically instead of doing a one-time copy. The method should not return`null`unless`source`is`null`. 

### onFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFocusChanged(
    view: View!, 
    sourceText: CharSequence!, 
    focused: Boolean, 
    direction: Int, 
    previouslyFocusedRect: Rect!
): Unit
```

This method is called when the TextView that uses this TransformationMethod gains or loses focus.

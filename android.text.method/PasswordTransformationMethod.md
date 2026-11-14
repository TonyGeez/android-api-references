# PasswordTransformationMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PasswordTransformationMethod

Kotlin| [Java](https://developer.android.com/reference/android/text/method/PasswordTransformationMethod "View this page in Java") 
| --- | --- |

```
open class PasswordTransformationMethod : TextWatcher, TransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#) |

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#PasswordTransformationMethod())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterTextChanged](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#afterTextChanged(android.text.Editable))`(`s:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeTextChanged](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#beforeTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#getInstance())`()` <br /> |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTransformation](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#getTransformation(kotlin.CharSequence,%20android.view.View))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChanged](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#onFocusChanged(android.view.View,%20kotlin.CharSequence,%20kotlin.Boolean,%20kotlin.Int,%20android.graphics.Rect))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `sourceText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `focused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `previouslyFocusedRect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTextChanged](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod#onTextChanged(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `before:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

## Public constructors

### PasswordTransformationMethod

```
PasswordTransformationMethod()
```

## Public methods

### afterTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun afterTextChanged(s: Editable!): Unit
```  

### beforeTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun beforeTextChanged(
    s: CharSequence!, 
    start: Int, 
    count: Int, 
    after: Int
): Unit
```  

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): PasswordTransformationMethod!
```  

### getTransformation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransformation(
    source: CharSequence!, 
    view: View!
): CharSequence!
```  

### onFocusChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFocusChanged(
    view: View!, 
    sourceText: CharSequence!, 
    focused: Boolean, 
    direction: Int, 
    previouslyFocusedRect: Rect!
): Unit
```  

### onTextChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTextChanged(
    s: CharSequence!, 
    start: Int, 
    before: Int, 
    count: Int
): Unit
```

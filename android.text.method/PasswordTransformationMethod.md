# PasswordTransformationMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PasswordTransformationMethod

Kotlin| [Java](PasswordTransformationMethod.md) 
| --- | --- |

```
open class PasswordTransformationMethod : TextWatcher, TransformationMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.PasswordTransformationMethod](PasswordTransformationMethod.md) |

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PasswordTransformationMethod](PasswordTransformationMethod.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [afterTextChanged](PasswordTransformationMethod.md))`(`s:` ` [Editable](../android.text/Editable.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [beforeTextChanged](PasswordTransformationMethod.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `after:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [PasswordTransformationMethod](PasswordTransformationMethod.md)! | [getInstance](PasswordTransformationMethod.md))`()` <br /> |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTransformation](PasswordTransformationMethod.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `view:` ` [View](../android.view/View.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFocusChanged](PasswordTransformationMethod.md))`(`view:` ` [View](../android.view/View.md)!`, `sourceText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `focused:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `previouslyFocusedRect:` ` [Rect](../android.graphics/Rect.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTextChanged](PasswordTransformationMethod.md))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `before:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
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

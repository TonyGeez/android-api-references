# SpannableString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SpannableString

Kotlin | [Java](SpannableString.md) 
| --- | --- |

```
open class SpannableString : CharSequence, GetChars, Spannable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.SpannableString](SpannableString.md) |

This is the class for text whose content is immutable but to which markup objects can be attached and detached. For mutable text, see [SpannableStringBuilder](SpannableStringBuilder.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SpannableString](SpannableString.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` For the backward compatibility reasons, this constructor copies all spans including . |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](SpannableString.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](SpannableString.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getChars](SpannableString.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanEnd](SpannableString.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanFlags](SpannableString.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanStart](SpannableString.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getSpans](SpannableString.md))`(`queryStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `queryEnd:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `kind:` ` [Class](../java.lang/Class.md)<T>!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](SpannableString.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextSpanTransition](SpannableString.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `kind:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpan](SpannableString.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpan](SpannableString.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [subSequence](SpannableString.md))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SpannableString.md))`()` <br /> |
| open static [SpannableString](SpannableString.md)! | [valueOf](SpannableString.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](SpannableString.md) <br /> |

## Public constructors

### SpannableString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SpannableString(source: CharSequence!)
```

For the backward compatibility reasons, this constructor copies all spans including .

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `source` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: source text |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(i: Int): Char
```

| Parameters ||
|---------|----------------------------------------------|
| `index` | the index of the `char` value to be returned |

| Return ||
|------------------------------------------------------------------------------|----------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the specified `char` value |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than `length()` |

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChars(
    start: Int, 
    end: Int, 
    dest: CharArray!, 
    off: Int
): Unit
```  

### getSpanEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanEnd(what: Any!): Int
```  

### getSpanFlags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanFlags(what: Any!): Int
```  

### getSpanStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanStart(what: Any!): Int
```  

### getSpans

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> getSpans(
    queryStart: Int, 
    queryEnd: Int, 
    kind: Class<T>!
): Array<T>!
```  

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### nextSpanTransition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextSpanTransition(
    start: Int, 
    limit: Int, 
    kind: Class<Any!>!
): Int
```  

### removeSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeSpan(what: Any!): Unit
```  

### setSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpan(
    what: Any!, 
    start: Int, 
    end: Int, 
    flags: Int
): Unit
```  

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

| Parameters ||
|---------|----------------------------|
| `start` | the start index, inclusive |
| `end` | the end index, exclusive |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the specified subsequence |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if `start` or `end` are negative, if `end` is greater than `length()`, or if `start` is greater than `end` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string consisting of exactly this sequence of characters |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(source: CharSequence!): SpannableString!
```

## Properties

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val length: Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of `char`s in this sequence |

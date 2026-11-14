# StringJoiner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringJoiner

```
class StringJoiner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#) |

`StringJoiner`is used to construct a sequence of characters separated by a delimiter and optionally starting with a supplied prefix and ending with a supplied suffix.

Prior to adding something to the`StringJoiner`, its`sj.toString()`method will, by default, return`prefix + suffix`. However, if the`setEmptyValue`method is called, the`emptyValue`supplied will be returned instead. This can be used, for example, when creating a string using set notation to indicate an empty set, i.e.`"{}"`, where the`prefix`is`"{"`, the`suffix`is`"}"`and nothing has been added to the`StringJoiner`.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#StringJoiner(kotlin.CharSequence))`(`delimiter:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Constructs a`StringJoiner`with no characters in it, with no`prefix`or`suffix`, and a copy of the supplied`delimiter`. |
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#StringJoiner(kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.CharSequence))`(`delimiter:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `prefix:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `suffix:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Constructs a`StringJoiner`with no characters in it using copies of the supplied`prefix`,`delimiter`and`suffix`. |

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)! | [add](https://developer.android.com/reference/kotlin/java/util/StringJoiner#add(kotlin.CharSequence))`(`newElement:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Adds a copy of the given`CharSequence`value as the next element of the`StringJoiner`value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/java/util/StringJoiner#length())`()` Returns the length of the`String`representation of this`StringJoiner`. |
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)! | [merge](https://developer.android.com/reference/kotlin/java/util/StringJoiner#merge(java.util.StringJoiner))`(`other:` ` [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)!`)` Adds the contents of the given`StringJoiner`without prefix and suffix as the next element if it is non-empty. |
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)! | [setEmptyValue](https://developer.android.com/reference/kotlin/java/util/StringJoiner#setEmptyValue(kotlin.CharSequence))`(`emptyValue:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the sequence of characters to be used when determining the string representation of this`StringJoiner`and no elements have been added yet, that is, when it is empty. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/StringJoiner#toString())`()` Returns the current value, consisting of the`prefix`, the values added so far separated by the`delimiter`, and the`suffix`, unless no elements have been added in which case, the`prefix + suffix`or the`emptyValue`characters are returned. |

## Public constructors

### StringJoiner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringJoiner(delimiter: CharSequence!)
```

Constructs a`StringJoiner`with no characters in it, with no`prefix`or`suffix`, and a copy of the supplied`delimiter`. If no characters are added to the`StringJoiner`and methods accessing the value of it are invoked, it will not return a`prefix`or`suffix`(or properties thereof) in the result, unless`setEmptyValue`has first been called.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence of characters to be used between each element added to the`StringJoiner`value |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`delimiter`is`null` |

### StringJoiner

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringJoiner(
    delimiter: CharSequence!, 
    prefix: CharSequence!, 
    suffix: CharSequence!)
```

Constructs a`StringJoiner`with no characters in it using copies of the supplied`prefix`,`delimiter`and`suffix`. If no characters are added to the`StringJoiner`and methods accessing the string value of it are invoked, it will return the`prefix + suffix`(or properties thereof) in the result, unless`setEmptyValue`has first been called.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence of characters to be used between each element added to the`StringJoiner` |
| `prefix` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence of characters to be used at the beginning |
| `suffix` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence of characters to be used at the end |

| Exceptions ||
|----------------------------------|--------------------------------------------|
| `java.lang.NullPointerException` | if`prefix`,`delimiter`, or`suffix`is`null` |

## Public methods

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(newElement: CharSequence!): StringJoiner!
```

Adds a copy of the given`CharSequence`value as the next element of the`StringJoiner`value. If`newElement`is`null`, then`"null"`is added.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------|
| `newElement` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The element to add |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------|
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)! | a reference to this`StringJoiner` |

### length

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun length(): Int
```

Returns the length of the`String`representation of this`StringJoiner`. Note that if no add methods have been called, then the length of the`String`representation (either`prefix + suffix`or`emptyValue`) will be returned. The value should be equivalent to`toString().length()`.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the current value of`StringJoiner` |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun merge(other: StringJoiner!): StringJoiner!
```

Adds the contents of the given`StringJoiner`without prefix and suffix as the next element if it is non-empty. If the given`StringJoiner`is empty, the call has no effect.

A`StringJoiner`is empty if [add()](https://developer.android.com/reference/kotlin/java/util/StringJoiner#add(kotlin.CharSequence))has never been called, and if`merge()`has never been called with a non-empty`StringJoiner`argument.

If the other`StringJoiner`is using a different delimiter, then elements from the other`StringJoiner`are concatenated with that delimiter and the result is appended to this`StringJoiner`as a single element.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)!:The`StringJoiner`whose contents should be merged into this one |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)! | This`StringJoiner` |

| Exceptions ||
|----------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if the other`StringJoiner`is null |

### setEmptyValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setEmptyValue(emptyValue: CharSequence!): StringJoiner!
```

Sets the sequence of characters to be used when determining the string representation of this`StringJoiner`and no elements have been added yet, that is, when it is empty. A copy of the`emptyValue`parameter is made for this purpose. Note that once an add method has been called, the`StringJoiner`is no longer considered empty, even if the element(s) added correspond to the empty`String`.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `emptyValue` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the characters to return as the value of an empty`StringJoiner` |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| [StringJoiner](https://developer.android.com/reference/kotlin/java/util/StringJoiner#)! | this`StringJoiner`itself so the calls may be chained |

| Exceptions ||
|----------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | when the`emptyValue`parameter is`null` |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the current value, consisting of the`prefix`, the values added so far separated by the`delimiter`, and the`suffix`, unless no elements have been added in which case, the`prefix + suffix`or the`emptyValue`characters are returned.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the string representation of this`StringJoiner` |

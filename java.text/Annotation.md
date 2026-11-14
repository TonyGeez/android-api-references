# Annotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Annotation

```
open class Annotation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.Annotation](../java/text/Annotation.md) |

An Annotation object is used as a wrapper for a text attribute value if the attribute has annotation characteristics. These characteristics are:

- The text range that the attribute is applied to is critical to the semantics of the range. That means, the attribute cannot be applied to subranges of the text range that it applies to, and, if two adjacent text ranges have the same value for this attribute, the attribute still cannot be applied to the combined range as a whole with this value.
- The attribute or its value usually do no longer apply if the underlying text is changed.

An example is grammatical information attached to a sentence: For the previous sentence, you can say that "an example" is the subject, but you cannot say the same about "an", "example", or "exam". When the text is changed, the grammatical information typically becomes invalid. Another example is Japanese reading information (yomi).

<br />

Wrapping the attribute value into an Annotation object guarantees that adjacent text runs don't get merged even if the attribute values are equal, and indicates to text containers that the attribute should be discarded if the underlying text is modified.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Annotation](../java/text/Annotation.md))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs an annotation record with the given value, which may be null. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getValue](../java/text/Annotation.md))`()` Returns the value of the attribute, which may be null. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/text/Annotation.md))`()` Returns the String representation of this Annotation. |

## Public constructors

### Annotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Annotation(value: Any!)
```

Constructs an annotation record with the given value, which may be null.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the value of the attribute |

## Public methods

### getValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValue(): Any!
```

Returns the value of the attribute, which may be null.

| Return ||
|-----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the value of the attribute |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of this Annotation.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the`String`representation of this`Annotation` |

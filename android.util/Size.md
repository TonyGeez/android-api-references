# Size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Size

Kotlin| [Java](Size.md) 
| --- | --- |

```
class Size
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.Size](Size.md) |

Immutable class for describing width and height dimensions in pixels.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Size](Size.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new immutable Size instance. |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Size.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Check if this size is equal to another size. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](Size.md))`()` Get the height of the size (in pixels). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](Size.md))`()` Get the width of the size (in pixels). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Size.md))`()` Returns a hash code value for the object. |
| static [Size](Size.md)! | [parseSize](Size.md))`(`string:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses the specified string as a size value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Size.md))`()` Return the size represented as a string with the format`"WxH"` |
| --- | --- |

## Public constructors

### Size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Size(
    width: Int, 
    height: Int)
```

Create a new immutable Size instance.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The width of the size, in pixels |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The height of the size, in pixels |

## Public methods

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Check if this size is equal to another size.

Two sizes are equal if and only if both their widths and heights are equal.

A size object is never equal to any other type of object.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects were equal,`false`otherwise |

### getHeight

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

Get the height of the size (in pixels).

| Return ||
|----------------------------------------------------------------------------|--------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | height |

### getWidth

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Get the width of the size (in pixels).

| Return ||
|----------------------------------------------------------------------------|-------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | width |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java.util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java.lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### parseSize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parseSize(string: String!): Size!
```

Parses the specified string as a size value.

The ASCII characters`\``u002a`('\*') and`\``u0078`('x') are recognized as separators between the width and height.

For any`Size s`:`Size.parseSize(s.toString()).equals(s)`. However, the method also handles sizes expressed in the following forms:

"*width* `x`*height* " or "*width* `*`*height* "`=> new Size(width, height)`, where*width* and*height*are string integers potentially containing a sign, such as "-10", "+7" or "5". 

```kotlin
<code>Size.parseSize("3*+6").equals(new Size(3, 6)) == true
  Size.parseSize("-3x-6").equals(new Size(-3, -6)) == true
  Size.parseSize("4 by 3") =&gt; throws NumberFormatException
  </code>
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `string` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string representation of a size value. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Size](Size.md)! | the size value represented by`string`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------|
| `java.lang.NumberFormatException` | if`string`cannot be parsed as a size value. |
| `java.lang.NullPointerException` | if`string`was`null` |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return the size represented as a string with the format`"WxH"`

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation of the size |

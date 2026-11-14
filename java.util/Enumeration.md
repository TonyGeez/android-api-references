# Enumeration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Enumeration

```
interface Enumeration<E : Any!>
```

| [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration#) |

| Known Direct Subclasses [StringTokenizer](https://developer.android.com/reference/kotlin/java/util/StringTokenizer) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------| | [StringTokenizer](https://developer.android.com/reference/kotlin/java/util/StringTokenizer) | The string tokenizer class allows an application to break a string into tokens. | |

An object that implements the Enumeration interface generates a series of elements, one at a time. Successive calls to the`nextElement`method return successive elements of the series.

For example, to print all elements of a`Vector<E>`*v*: 

```kotlin
for (Enumeration<E> e = v.elements(); e.hasMoreElements();)
        System.out.println(e.nextElement());
```

Methods are provided to enumerate through the elements of a vector, the keys of a hashtable, and the values in a hashtable. Enumerations are also used to specify the input streams to a`SequenceInputStream`.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\>! | [asIterator](https://developer.android.com/reference/kotlin/java/util/Enumeration#asIterator())`()` Returns an [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator) that traverses the remaining elements covered by this enumeration. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasMoreElements](https://developer.android.com/reference/kotlin/java/util/Enumeration#hasMoreElements())`()` Tests if this enumeration contains more elements. |
| abstractE | [nextElement](https://developer.android.com/reference/kotlin/java/util/Enumeration#nextElement())`()` Returns the next element of this enumeration if this enumeration object has at least one more element to provide. |

## Public methods

### asIterator

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun asIterator(): MutableIterator<E>!
```

Returns an [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator) that traverses the remaining elements covered by this enumeration. Traversal is undefined if any methods are called on this enumeration after the call to`asIterator`.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E>! | an Iterator representing the remaining elements of this Enumeration |

### hasMoreElements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasMoreElements(): Boolean
```

Tests if this enumeration contains more elements.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if this enumeration object contains at least one more element to provide;`false`otherwise. |

### nextElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextElement(): E
```

Returns the next element of this enumeration if this enumeration object has at least one more element to provide.

| Return ||
|---|---------------------------------------|
| E | the next element of this enumeration. |

| Exceptions ||
|------------------------------------|----------------------------|
| `java.util.NoSuchElementException` | if no more elements exist. |

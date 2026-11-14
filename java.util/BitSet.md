# BitSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BitSet

```
open class BitSet : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.BitSet](BitSet.md) |

This class implements a vector of bits that grows as needed. Each component of the bit set has a`boolean`value. The bits of a`BitSet`are indexed by nonnegative integers. Individual indexed bits can be examined, set, or cleared. One`BitSet`may be used to modify the contents of another`BitSet`through logical AND, logical inclusive OR, and logical exclusive OR operations.

By default, all bits in the set initially have the value`false`.

Every bit set has a current size, which is the number of bits of space currently in use by the bit set. Note that the size is related to the implementation of a bit set, so it may change with implementation. The length of a bit set relates to logical length of a bit set and is defined independently of implementation.

Unless otherwise noted, passing a null parameter to any of the methods in a`BitSet`will result in a`NullPointerException`.

A`BitSet`is not safe for multithreaded use without external synchronization.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BitSet](BitSet.md))`()` Creates a new bit set. |
| [BitSet](BitSet.md))`(`nbits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a bit set whose initial size is large enough to explicitly represent bits with indices in the range`0`through`nbits-1`. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [and](BitSet.md))`(`set:` ` [BitSet](BitSet.md)!`)` Performs a logical**AND**of this target bit set with the argument bit set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [andNot](BitSet.md))`(`set:` ` [BitSet](BitSet.md)!`)` Clears all of the bits in this`BitSet`whose corresponding bit is set in the specified`BitSet`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [cardinality](BitSet.md))`()` Returns the number of bits set to`true`in this`BitSet`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](BitSet.md))`()` Sets all of the bits in this BitSet to`false`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](BitSet.md))`(`bitIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit specified by the index to`false`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bits from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to`false`. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](BitSet.md))`()` Cloning this`BitSet`produces a new`BitSet`that is equal to it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](BitSet.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flip](BitSet.md))`(`bitIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit at the specified index to the complement of its current value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flip](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets each bit from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to the complement of its current value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [get](BitSet.md))`(`bitIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the bit with the specified index. |
| open [BitSet](BitSet.md)! | [get](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a new`BitSet`composed of bits from this`BitSet`from`fromIndex`(inclusive) to`toIndex`(exclusive). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](BitSet.md))`()` Returns the hash code value for this bit set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [intersects](BitSet.md))`(`set:` ` [BitSet](BitSet.md)!`)` Returns true if the specified`BitSet`has any bits set to`true`that are also set to`true`in this`BitSet`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](BitSet.md))`()` Returns true if this`BitSet`contains no bits that are set to`true`. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](BitSet.md))`()` Returns the "logical size" of this`BitSet`: the index of the highest set bit in the`BitSet`plus one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextClearBit](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the first bit that is set to`false`that occurs on or after the specified starting index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextSetBit](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the first bit that is set to`true`that occurs on or after the specified starting index. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [or](BitSet.md))`(`set:` ` [BitSet](BitSet.md)!`)` Performs a logical**OR**of this bit set with the bit set argument. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousClearBit](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the nearest bit that is set to`false`that occurs on or before the specified starting index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousSetBit](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the index of the nearest bit that is set to`true`that occurs on or before the specified starting index. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](BitSet.md))`(`bitIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bit at the specified index to`true`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](BitSet.md))`(`bitIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the bit at the specified index to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the bits from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to`true`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](BitSet.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the bits from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to the specified value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](BitSet.md))`()` Returns the number of bits of space actually in use by this`BitSet`to represent bit values. |
| open [IntStream](../java.util.stream/IntStream.md)! | [stream](BitSet.md))`()` Returns a stream of indices for which this`BitSet`contains a bit in the set state. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](BitSet.md))`()` Returns a new byte array containing all the bits in this bit set. |
| open [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [toLongArray](BitSet.md))`()` Returns a new long array containing all the bits in this bit set. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](BitSet.md))`()` Returns a string representation of this bit set. |
| --- | --- |
| openstatic [BitSet](BitSet.md)! | [valueOf](BitSet.md))`(`bytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Returns a new bit set containing all the bits in the given byte array. |
| openstatic [BitSet](BitSet.md)! | [valueOf](BitSet.md))`(`bb:` ` [ByteBuffer](../java.nio/ByteBuffer.md)!`)` Returns a new bit set containing all the bits in the given byte buffer between its position and limit. |
| openstatic [BitSet](BitSet.md)! | [valueOf](BitSet.md))`(`lb:` ` [LongBuffer](../java.nio/LongBuffer.md)!`)` Returns a new bit set containing all the bits in the given long buffer between its position and limit. |
| --- | --- |
| openstatic [BitSet](BitSet.md)! | [valueOf](BitSet.md))`(`longs:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Returns a new bit set containing all the bits in the given long array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [xor](BitSet.md))`(`set:` ` [BitSet](BitSet.md)!`)` Performs a logical**XOR**of this bit set with the bit set argument. |

## Public constructors

### BitSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitSet()
```

Creates a new bit set. All bits are initially`false`. 

### BitSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BitSet(nbits: Int)
```

Creates a bit set whose initial size is large enough to explicitly represent bits with indices in the range`0`through`nbits-1`. All bits are initially`false`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------|
| `nbits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial size of the bit set |

| Exceptions ||
|----------------------------------------|-------------------------------------------|
| `java.lang.NegativeArraySizeException` | if the specified initial size is negative |

## Public methods

### and

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun and(set: BitSet!): Unit
```

Performs a logical**AND** of this target bit set with the argument bit set. This bit set is modified so that each bit in it has the value`true`if and only if it both initially had the value`true`and the corresponding bit in the bit set argument also had the value`true`.

| Parameters ||
|-------|---------------------------------------------------------------------------------------|
| `set` | [BitSet](BitSet.md)!:a bit set |

### andNot

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andNot(set: BitSet!): Unit
```

Clears all of the bits in this`BitSet`whose corresponding bit is set in the specified`BitSet`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `set` | [BitSet](BitSet.md)!:the`BitSet`with which to mask this`BitSet` |

### cardinality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cardinality(): Int
```

Returns the number of bits set to`true`in this`BitSet`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bits set to`true`in this`BitSet` |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Sets all of the bits in this BitSet to`false`. 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(bitIndex: Int): Unit
```

Sets the bit specified by the index to`false`.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------|
| `bitIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the bit to be cleared |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sets the bits from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to`false`.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first bit to be cleared |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after the last bit to be cleared |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`fromIndex`is negative, or`toIndex`is negative, or`fromIndex`is larger than`toIndex` |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Cloning this`BitSet`produces a new`BitSet`that is equal to it. The clone of the bit set is another bit set that has exactly the same bits set to`true`as this bit set.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this bit set |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/BitSet#size()> 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and is a`BitSet`object that has exactly the same set of bits set to`true`as this bit set. That is, for every nonnegative`int`index`k`, 

```kotlin
((BitSet)obj).get(k) == this.get(k)
```
must be true. The current sizes of the two bit sets are not compared.

<br />

| Parameters ||
|-------|----------------------------|
| `obj` | the object to compare with |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/java/util/BitSet#size()> 

### flip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flip(bitIndex: Int): Unit
```

Sets the bit at the specified index to the complement of its current value.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------|
| `bitIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the bit to flip |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### flip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun flip(
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sets each bit from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to the complement of its current value.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first bit to flip |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after the last bit to flip |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`fromIndex`is negative, or`toIndex`is negative, or`fromIndex`is larger than`toIndex` |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(bitIndex: Int): Boolean
```

Returns the value of the bit with the specified index. The value is`true`if the bit with the index`bitIndex`is currently set in this`BitSet`; otherwise, the result is`false`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `bitIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bit index |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the bit with the specified index |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    fromIndex: Int, 
    toIndex: Int
): BitSet!
```

Returns a new`BitSet`composed of bits from this`BitSet`from`fromIndex`(inclusive) to`toIndex`(exclusive).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first bit to include |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after the last bit to include |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------|
| [BitSet](BitSet.md)! | a new`BitSet`from a range of this`BitSet` |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`fromIndex`is negative, or`toIndex`is negative, or`fromIndex`is larger than`toIndex` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this bit set. The hash code depends only on which bits are set within this`BitSet`.

The hash code is defined to be the result of the following calculation: 

```kotlin
<code>public int hashCode() {
      long h = 1234;
      long[] words = toLongArray();
      for (int i = words.length; --i &gt;= 0; )
          h ^= words[i] * (i + 1);
      return (int)((h &gt;&gt; 32) ^ h);
  }</code>
```
Note that the hash code changes if the set of bits is altered.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this bit set |

### intersects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun intersects(set: BitSet!): Boolean
```

Returns true if the specified`BitSet`has any bits set to`true`that are also set to`true`in this`BitSet`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `set` | [BitSet](BitSet.md)!:`BitSet`to intersect with |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean indicating whether this`BitSet`intersects the specified`BitSet` |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns true if this`BitSet`contains no bits that are set to`true`.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean indicating whether this`BitSet`is empty |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun length(): Int
```

Returns the "logical size" of this`BitSet`: the index of the highest set bit in the`BitSet`plus one. Returns zero if the`BitSet`contains no set bits.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the logical size of this`BitSet` |

### nextClearBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextClearBit(fromIndex: Int): Int
```

Returns the index of the first bit that is set to`false`that occurs on or after the specified starting index.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to start checking from (inclusive) |

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the next clear bit |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### nextSetBit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextSetBit(fromIndex: Int): Int
```

Returns the index of the first bit that is set to`true`that occurs on or after the specified starting index. If no such bit exists then`-1`is returned.

To iterate over the`true`bits in a`BitSet`, use the following loop: 

```kotlin
<code>for (int i = bs.nextSetBit(0); i &gt;= 0; i = bs.nextSetBit(i+1)) {
      // operate on index i here
      if (i == Integer.MAX_VALUE) {
          break; // or (i+1) would overflow
      }
  }</code>
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to start checking from (inclusive) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the next set bit, or`-1`if there is no such bit |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### or

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun or(set: BitSet!): Unit
```

Performs a logical**OR** of this bit set with the bit set argument. This bit set is modified so that a bit in it has the value`true`if and only if it either already had the value`true`or the corresponding bit in the bit set argument has the value`true`.

| Parameters ||
|-------|---------------------------------------------------------------------------------------|
| `set` | [BitSet](BitSet.md)!:a bit set |

### previousClearBit

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousClearBit(fromIndex: Int): Int
```

Returns the index of the nearest bit that is set to`false`that occurs on or before the specified starting index. If no such bit exists, or if`-1`is given as the starting index, then`-1`is returned.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to start checking from (inclusive) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the previous clear bit, or`-1`if there is no such bit |

| Exceptions ||
|---------------------------------------|-----------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is less than`-1` |

### previousSetBit

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousSetBit(fromIndex: Int): Int
```

Returns the index of the nearest bit that is set to`true`that occurs on or before the specified starting index. If no such bit exists, or if`-1`is given as the starting index, then`-1`is returned.

To iterate over the`true`bits in a`BitSet`, use the following loop: 

```kotlin
<code>for (int i = bs.length(); (i = bs.previousSetBit(i-1)) &gt;= 0; ) {
      // operate on index i here
  }</code>
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index to start checking from (inclusive) |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the previous set bit, or`-1`if there is no such bit |

| Exceptions ||
|---------------------------------------|-----------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is less than`-1` |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(bitIndex: Int): Unit
```

Sets the bit at the specified index to`true`.

| Parameters ||
|------------|----------------------------------------------------------------------------------------|
| `bitIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit index |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    bitIndex: Int, 
    value: Boolean
): Unit
```

Sets the bit at the specified index to the specified value.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `bitIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bit index |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a boolean value to set |

| Exceptions ||
|---------------------------------------|------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sets the bits from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to`true`.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first bit to be set |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after the last bit to be set |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`fromIndex`is negative, or`toIndex`is negative, or`fromIndex`is larger than`toIndex` |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    fromIndex: Int, 
    toIndex: Int, 
    value: Boolean
): Unit
```

Sets the bits from the specified`fromIndex`(inclusive) to the specified`toIndex`(exclusive) to the specified value.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first bit to be set |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after the last bit to be set |
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):value to set the selected bits to |
| --- | --- |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`fromIndex`is negative, or`toIndex`is negative, or`fromIndex`is larger than`toIndex` |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun size(): Int
```

Returns the number of bits of space actually in use by this`BitSet`to represent bit values. The maximum element in the set is the size - 1st element.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bits currently in this bit set |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stream(): IntStream!
```

Returns a stream of indices for which this`BitSet`contains a bit in the set state. The indices are returned in order, from lowest to highest. The size of the stream is the number of bits in the set state, equal to the value returned by the [cardinality()](BitSet.md))method.

The stream binds to this bit set when the terminal stream operation commences (specifically, the spliterator for the stream is [*late-binding*](Spliterator.md)). If the bit set is modified during that operation then the result is undefined.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------|
| [IntStream](../java.util.stream/IntStream.md)! | a stream of integers representing set indices |

### toByteArray

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toByteArray(): ByteArray!
```

Returns a new byte array containing all the bits in this bit set.

More precisely, if 
`byte[] bytes = s.toByteArray();` 
then`bytes.length == (s.length()+7)/8`and 
`s.get(n) == ((bytes[n/8] & (1<<(n%8))) != 0)` 
for all`n < 8 * bytes.length`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing a little-endian representation of all the bits in this bit set |

### toLongArray

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLongArray(): LongArray!
```

Returns a new long array containing all the bits in this bit set.

More precisely, if 
`long[] longs = s.toLongArray();` 
then`longs.length == (s.length()+63)/64`and 
`s.get(n) == ((longs[n/64] & (1L<<(n%64))) != 0)` 
for all`n < 64 * longs.length`.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | a long array containing a little-endian representation of all the bits in this bit set |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this bit set. For every index for which this`BitSet`contains a bit in the set state, the decimal representation of that index is included in the result. Such indices are listed in order from lowest to highest, separated by ", " (a comma and a space) and surrounded by braces, resulting in the usual mathematical notation for a set of integers.

Example: 

```kotlin
BitSet drPepper = new BitSet();
```
Now`drPepper.toString()`returns "`{}`". 

```kotlin
drPepper.set(2);
```
Now`drPepper.toString()`returns "`{2}`". 

```kotlin
drPepper.set(4);
  drPepper.set(10);
```
Now`drPepper.toString()`returns "`{2, 4, 10}`".

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this bit set |

### valueOf

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(bytes: ByteArray!): BitSet!
```

Returns a new bit set containing all the bits in the given byte array.

More precisely, 
`BitSet.valueOf(bytes).get(n) == ((bytes[n/8] & (1<<(n%8))) != 0)` 
for all`n < 8 * bytes.length`.

This method is equivalent to`BitSet.valueOf(ByteBuffer.wrap(bytes))`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing a little-endian representation of a sequence of bits to be used as the initial bits of the new bit set |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [BitSet](BitSet.md)! | a`BitSet`containing all the bits in the byte array |

### valueOf

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(bb: ByteBuffer!): BitSet!
```

Returns a new bit set containing all the bits in the given byte buffer between its position and limit.

More precisely, 
`BitSet.valueOf(bb).get(n) == ((bb.get(bb.position()+n/8) & (1<<(n%8))) != 0)` 
for all`n < 8 * bb.remaining()`.

The byte buffer is not modified by this method, and no reference to the buffer is retained by the bit set.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bb` | [ByteBuffer](../java.nio/ByteBuffer.md)!:a byte buffer containing a little-endian representation of a sequence of bits between its position and limit, to be used as the initial bits of the new bit set |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [BitSet](BitSet.md)! | a`BitSet`containing all the bits in the buffer in the specified range |

### valueOf

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(lb: LongBuffer!): BitSet!
```

Returns a new bit set containing all the bits in the given long buffer between its position and limit.

More precisely, 
`BitSet.valueOf(lb).get(n) == ((lb.get(lb.position()+n/64) & (1L<<(n%64))) != 0)` 
for all`n < 64 * lb.remaining()`.

The long buffer is not modified by this method, and no reference to the buffer is retained by the bit set.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lb` | [LongBuffer](../java.nio/LongBuffer.md)!:a long buffer containing a little-endian representation of a sequence of bits between its position and limit, to be used as the initial bits of the new bit set |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [BitSet](BitSet.md)! | a`BitSet`containing all the bits in the buffer in the specified range |

### valueOf

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(longs: LongArray!): BitSet!
```

Returns a new bit set containing all the bits in the given long array.

More precisely, 
`BitSet.valueOf(longs).get(n) == ((longs[n/64] & (1L<<(n%64))) != 0)` 
for all`n < 64 * longs.length`.

This method is equivalent to`BitSet.valueOf(LongBuffer.wrap(longs))`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `longs` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:a long array containing a little-endian representation of a sequence of bits to be used as the initial bits of the new bit set |

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [BitSet](BitSet.md)! | a`BitSet`containing all the bits in the long array |

### xor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun xor(set: BitSet!): Unit
```

Performs a logical**XOR** of this bit set with the bit set argument. This bit set is modified so that a bit in it has the value`true`if and only if one of the following statements holds:

- The bit initially has the value`true`, and the corresponding bit in the argument has the value`false`.
- The bit initially has the value`false`, and the corresponding bit in the argument has the value`true`.

<br />

| Parameters ||
|-------|---------------------------------------------------------------------------------------|
| `set` | [BitSet](BitSet.md)!:a bit set |

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Arrays

```
class Arrays
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Arrays](Arrays.md) |

This class contains various methods for manipulating arrays (such as sorting and searching). This class also contains a static factory that allows arrays to be viewed as lists.

The methods in this class all throw a `NullPointerException`, if the specified array reference is null, except where noted.

The documentation for the methods contained in this class includes brief descriptions of the *implementations* . Such descriptions should be regarded as *implementation notes* , rather than parts of the *specification* . Implementors should feel free to substitute other algorithms, so long as the specification itself is adhered to. (For example, the algorithm used by `sort(Object[])` does not have to be a MergeSort, but it does have to be *stable*.)

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|---|---|
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | asList Returns a fixed-size list backed by the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of bytes for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of bytes for the specified value using the binary search algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of chars for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of chars for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of doubles for the specified value using the binary search algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of doubles for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of floats for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of floats for the specified value using the binary search algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of ints for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of ints for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array for the specified object using the binary search algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array for the specified object using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of longs for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of longs for the specified value using the binary search algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array of shorts for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array of shorts for the specified value using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches a range of the specified array for the specified object using the binary search algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | binarySearch Searches the specified array for the specified object using the binary search algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `boolean` arrays lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `boolean` arrays lexicographically over the specified ranges. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `byte` arrays lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `byte` arrays lexicographically over the specified ranges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `char` arrays lexicographically. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `char` arrays lexicographically over the specified ranges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `double` arrays lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `double` arrays lexicographically over the specified ranges. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `float` arrays lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `float` arrays lexicographically over the specified ranges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `int` arrays lexicographically over the specified ranges. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `int` arrays lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `long` arrays lexicographically over the specified ranges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `long` arrays lexicographically. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `short` arrays lexicographically over the specified ranges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `short` arrays lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `Object` arrays lexicographically over the specified ranges. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `Object` arrays lexicographically over the specified ranges. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `Object` arrays, within comparable elements, lexicographically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares two `Object` arrays lexicographically using a specified comparator. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `byte` arrays lexicographically, numerically treating elements as unsigned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `byte` arrays lexicographically over the specified ranges, numerically treating elements as unsigned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `int` arrays lexicographically over the specified ranges, numerically treating elements as unsigned. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `int` arrays lexicographically, numerically treating elements as unsigned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `long` arrays lexicographically over the specified ranges, numerically treating elements as unsigned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `long` arrays lexicographically, numerically treating elements as unsigned. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `short` arrays lexicographically over the specified ranges, numerically treating elements as unsigned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareUnsigned Compares two `short` arrays lexicographically, numerically treating elements as unsigned. |
| static [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html) | copyOf Copies the specified array, truncating or padding with `false` (if necessary) so the copy has the specified length. |
| --- | --- |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | copyOf Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. |
| static [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html) | copyOf Copies the specified array, truncating or padding with null characters (if necessary) so the copy has the specified length. |
| static [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html) | copyOf Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. |
| --- | --- |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | copyOf Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | copyOf Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. |
| static [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | copyOf Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. |
| --- | --- |
| static [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html) | copyOf Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | copyOf Copies the specified array, truncating or padding with nulls (if necessary) so the copy has the specified length. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | copyOf Copies the specified array, truncating or padding with nulls (if necessary) so the copy has the specified length. |
| --- | --- |
| static [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| static [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| --- | --- |
| static [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| --- | --- |
| static [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| static [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html) | copyOfRange Copies the specified range of the specified array into a new array. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | copyOfRange Copies the specified range of the specified array into a new array. |
| --- | --- |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | copyOfRange Copies the specified range of the specified array into a new array. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | deepEquals Returns `true` if the two specified arrays are *deeply equal* to one another. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | deepHashCode Returns a hash code based on the "deep contents" of the specified array. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | deepToString Returns a string representation of the "deep contents" of the specified array. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of booleans are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of booleans, over the specified ranges, are *equal* to one another. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of bytes are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of bytes, over the specified ranges, are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of chars are *equal* to one another. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of chars, over the specified ranges, are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of doubles are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of doubles, over the specified ranges, are *equal* to one another. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of floats are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of floats, over the specified ranges, are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of ints, over the specified ranges, are *equal* to one another. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of ints are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of Objects, over the specified ranges, are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of Objects are *equal* to one another. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of longs, over the specified ranges, are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of longs are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of shorts, over the specified ranges, are *equal* to one another. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of shorts are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns true if the two specified arrays of Objects, over the specified ranges, are *equal* to one another. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Returns `true` if the two specified arrays of Objects are *equal* to one another. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified boolean value to each element of the specified array of booleans. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified boolean value to each element of the specified range of the specified array of booleans. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified byte value to each element of the specified array of bytes. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified byte value to each element of the specified range of the specified array of bytes. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified char value to each element of the specified array of chars. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified char value to each element of the specified range of the specified array of chars. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified double value to each element of the specified array of doubles. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified double value to each element of the specified range of the specified array of doubles. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified float value to each element of the specified array of floats. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified float value to each element of the specified range of the specified array of floats. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified int value to each element of the specified array of ints. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified int value to each element of the specified range of the specified array of ints. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified Object reference to each element of the specified range of the specified array of Objects. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified Object reference to each element of the specified array of Objects. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified long value to each element of the specified range of the specified array of longs. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified long value to each element of the specified array of longs. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified short value to each element of the specified range of the specified array of shorts. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | fill Assigns the specified short value to each element of the specified array of shorts. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code based on the contents of the specified array. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `boolean` arrays, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `boolean` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `byte` arrays, otherwise return -1 if no mismatch is found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `byte` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `char` arrays, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `char` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `double` arrays, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `double` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `float` arrays, otherwise return -1 if no mismatch is found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `float` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `int` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `int` arrays, otherwise return -1 if no mismatch is found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `Object` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `Object` arrays, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `long` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `long` arrays, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `short` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `short` arrays, otherwise return -1 if no mismatch is found. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the relative index of the first mismatch between two `Object` arrays over the specified ranges, otherwise return -1 if no mismatch is found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | mismatch Finds and returns the index of the first mismatch between two `Object` arrays, otherwise return -1 if no mismatch is found. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Performs parallelPrefix for the given subrange of the array. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Cumulates, in parallel, each element of the given array in place, using the supplied function. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Performs parallelPrefix for the given subrange of the array. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Cumulates, in parallel, each element of the given array in place, using the supplied function. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Performs parallelPrefix for the given subrange of the array. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Cumulates, in parallel, each element of the given array in place, using the supplied function. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Performs parallelPrefix for the given subrange of the array. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelPrefix Cumulates, in parallel, each element of the given array in place, using the supplied function. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSetAll Set all elements of the specified array, in parallel, using the provided generator function to compute each element. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSetAll Set all elements of the specified array, in parallel, using the provided generator function to compute each element. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSetAll Set all elements of the specified array, in parallel, using the provided generator function to compute each element. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSetAll Set all elements of the specified array, in parallel, using the provided generator function to compute each element. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified range of the specified array of objects according to the order induced by the specified comparator. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | parallelSort Sorts the specified array of objects according to the order induced by the specified comparator. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAll Set all elements of the specified array, using the provided generator function to compute each element. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAll Set all elements of the specified array, using the provided generator function to compute each element. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAll Set all elements of the specified array, using the provided generator function to compute each element. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setAll Set all elements of the specified array, using the provided generator function to compute each element. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array into ascending numerical order. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the array into ascending order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified range of the specified array of objects according to the order induced by the specified comparator. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sort Sorts the specified array of objects according to the order induced by the specified comparator. |
| --- | --- |
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md) | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble` covering all of the specified array. |
| static [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md) | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble` covering the specified range of the specified array. |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md) | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt` covering all of the specified array. |
| --- | --- |
| static [Spliterator.OfInt](../java/util/Spliterator.OfInt.md) | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt` covering the specified range of the specified array. |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md) | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong` covering all of the specified array. |
| static [Spliterator.OfLong](../java/util/Spliterator.OfLong.md) | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong` covering the specified range of the specified array. |
| --- | --- |
| static [Spliterator](Spliterator.md)\<T\> | spliterator Returns a Spliterator covering all of the specified array. |
| static [Spliterator](Spliterator.md)\<T\> | spliterator Returns a Spliterator covering the specified range of the specified array. |
| static [DoubleStream](../java.util.stream/DoubleStream.md) | stream Returns a sequential DoubleStream with the specified array as its source. |
| --- | --- |
| static [DoubleStream](../java.util.stream/DoubleStream.md) | stream Returns a sequential DoubleStream with the specified range of the specified array as its source. |
| static [IntStream](../java.util.stream/IntStream.md) | stream Returns a sequential IntStream with the specified array as its source. |
| static [IntStream](../java.util.stream/IntStream.md) | stream Returns a sequential IntStream with the specified range of the specified array as its source. |
| --- | --- |
| static [LongStream](../java.util.stream/LongStream.md) | stream Returns a sequential LongStream with the specified array as its source. |
| static [LongStream](../java.util.stream/LongStream.md) | stream Returns a sequential LongStream with the specified range of the specified array as its source. |
| static [Stream](../java.util.stream/Stream.md)\<T\> | stream Returns a sequential Stream with the specified array as its source. |
| --- | --- |
| static [Stream](../java.util.stream/Stream.md)\<T\> | stream Returns a sequential Stream with the specified range of the specified array as its source. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the contents of the specified array. |

## Public methods

### asList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
@SafeVarargs static fun <T : Any!> asList(vararg a: T): MutableList<T>
```

Returns a fixed-size list backed by the specified array. Changes made to the array will be visible in the returned list, and changes made to the list will be visible in the array. The returned list is `https://developer.android.com/reference/kotlin/java/io/Serializable.html#` and implements RandomAccess.

The returned list implements the optional `Collection` methods, except those that would change the size of the returned list. Those methods leave the list unchanged and throw `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

If the specified array's actual component type differs from the type parameter T, this can result in operations on the returned list throwing an `ArrayStoreException`.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `a` | T: the array by which the list will be backed |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<T>` | a list view of the specified array |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified array is `null` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: ByteArray, 
    key: Byte
): Int
```

Searches the specified array of bytes for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be searched |
| `key` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: ByteArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Byte
): Int
```

Searches a range of the specified array of bytes for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: CharArray, 
    key: Char
): Int
```

Searches the specified array of chars for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be searched |
| `key` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: CharArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Char
): Int
```

Searches a range of the specified array of chars for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: DoubleArray, 
    key: Double
): Int
```

Searches the specified array of doubles for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found. This method considers all NaN values to be equivalent and equal.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be searched |
| `key` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: DoubleArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Double
): Int
```

Searches a range of the specified array of doubles for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found. This method considers all NaN values to be equivalent and equal.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: FloatArray, 
    key: Float
): Int
```

Searches the specified array of floats for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found. This method considers all NaN values to be equivalent and equal.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be searched |
| `key` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: FloatArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Float
): Int
```

Searches a range of the specified array of floats for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found. This method considers all NaN values to be equivalent and equal.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: IntArray, 
    key: Int
): Int
```

Searches the specified array of ints for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be searched |
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: IntArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Int
): Int
```

Searches a range of the specified array of ints for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: Array<Any!>, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Any
): Int
```

Searches a range of the specified array for the specified object using the binary search algorithm. The range must be sorted into ascending order according to the [natural ordering](../java.lang/Comparable.md) of its elements (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. (If the range contains elements that are not mutually comparable (for example, strings and integers), it *cannot* be sorted according to the natural ordering of its elements, hence results are undefined.) If the range contains multiple elements equal to the specified object, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.ClassCastException` | if the search key is not comparable to the elements of the array within the specified range. |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| --- | --- |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: Array<Any!>, 
    key: Any
): Int
```

Searches the specified array for the specified object using the binary search algorithm. The array must be sorted into ascending order according to the [natural ordering](../java.lang/Comparable.md) of its elements (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. (If the array contains elements that are not mutually comparable (for example, strings and integers), it *cannot* be sorted according to the natural ordering of its elements, hence results are undefined.) If the array contains multiple elements equal to the specified object, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the array to be searched |
| `key` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the search key is not comparable to the elements of the array. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: LongArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Long
): Int
```

Searches a range of the specified array of longs for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: LongArray, 
    key: Long
): Int
```

Searches the specified array of longs for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be searched |
| `key` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: ShortArray, 
    fromIndex: Int, 
    toIndex: Int, 
    key: Short
): Int
```

Searches a range of the specified array of shorts for the specified value using the binary search algorithm. The range must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| --- | --- |
| `key` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun binarySearch(
    a: ShortArray, 
    key: Short
): Int
```

Searches the specified array of shorts for the specified value using the binary search algorithm. The array must be sorted (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements with the specified value, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be searched |
| `key` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the value to be searched for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

### binarySearch

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> binarySearch(
    a: Array<T>, 
    fromIndex: Int, 
    toIndex: Int, 
    key: T, 
    c: Comparator<in T>?
): Int
```

Searches a range of the specified array for the specified object using the binary search algorithm. The range must be sorted into ascending order according to the specified comparator (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the range contains multiple elements equal to the specified object, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be searched |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be searched |
| --- | --- |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be searched |
| `key` | T: the value to be searched for |
| `c` | [Comparator](Comparator.md)\<in T\>?: the comparator by which the array is ordered. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array within the specified range; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element in the range greater than the key, or `toIndex` if all elements in the range are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0 or toIndex > a.length` |
| `java.lang.ClassCastException` | if the range contains elements that are not *mutually comparable* using the specified comparator, or the search key is not comparable to the elements in the range using this comparator. |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| --- | --- |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> binarySearch(
    a: Array<T>, 
    key: T, 
    c: Comparator<in T>?
): Int
```

Searches the specified array for the specified object using the binary search algorithm. The array must be sorted into ascending order according to the specified comparator (as by the sort method) prior to making this call. If it is not sorted, the results are undefined. If the array contains multiple elements equal to the specified object, there is no guarantee which one will be found.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be searched |
| `key` | T: the value to be searched for |
| --- | --- |
| `c` | [Comparator](Comparator.md)\<in T\>?: the comparator by which the array is ordered. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | index of the search key, if it is contained in the array; otherwise, `(-(insertion point) - 1)`. The *insertion point* is defined as the point at which the key would be inserted into the array: the index of the first element greater than the key, or `a.length` if all elements in the array are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* using the specified comparator, or the search key is not comparable to the elements of the array using this comparator. |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: BooleanArray?, 
    b: BooleanArray?
): Int
```

Compares two `boolean` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: the first array to compare |
| `b` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: BooleanArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: BooleanArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `boolean` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: ByteArray?, 
    b: ByteArray?
): Int
```

Compares two `byte` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the first array to compare |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: ByteArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ByteArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `byte` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: CharArray?, 
    b: CharArray?
): Int
```

Compares two `char` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: the first array to compare |
| `b` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: CharArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: CharArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `char` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: DoubleArray?, 
    b: DoubleArray?
): Int
```

Compares two `double` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: the first array to compare |
| `b` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: DoubleArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: DoubleArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `double` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: FloatArray?, 
    b: FloatArray?
): Int
```

Compares two `float` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the first array to compare |
| `b` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: FloatArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: FloatArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `float` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: IntArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: IntArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `int` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: IntArray?, 
    b: IntArray?
): Int
```

Compares two `int` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the first array to compare |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: LongArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: LongArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `long` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: LongArray?, 
    b: LongArray?
): Int
```

Compares two `long` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the first array to compare |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: ShortArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ShortArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `short` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    a: ShortArray?, 
    b: ShortArray?
): Int
```

Compares two `short` arrays lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compare, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the first array to compare |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Comparable<T>!> compare(
    a: Array<T>, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: Array<T>, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `Object` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements of type `T` at a relative index `i` within the respective arrays that is the prefix length, as if by:

```kotlin
<code>Comparator.nullsFirst(Comparator.&lt;T&gt;naturalOrder()).
          compare(a[aFromIndex + i, b[bFromIndex + i])
  </code>
```
Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively:

```kotlin
<code>Arrays.equals(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) ==
          (Arrays.compare(a, aFromIndex, aToIndex, b, bFromIndex, bToIndex) == 0)
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of comparable array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| --- | --- |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| --- | --- |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> compare(
    a: Array<T>, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: Array<T>, 
    bFromIndex: Int, 
    bToIndex: Int, 
    cmp: Comparator<in T>
): Int
```

Compares two `Object` arrays lexicographically over the specified ranges.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing with the specified comparator two elements at a relative index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

| Parameters ||
|---|---|
| `<T>` | the type of array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| --- | --- |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| --- | --- |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| `cmp` | [Comparator](Comparator.md)\<in T\>: the comparator to compare array elements |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array or the comparator is `null` |
| --- | --- |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Comparable<T>!> compare(
    a: Array<T>?, 
    b: Array<T>?
): Int
```

Compares two `Object` arrays, within comparable elements, lexicographically.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements of type `T` at an index `i` within the respective arrays that is the prefix length, as if by:

```kotlin
<code>Comparator.nullsFirst(Comparator.&lt;T&gt;naturalOrder()).
          compare(a[i], b[i])
  </code>
```
Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal. A `null` array element is considered lexicographically less than a non-`null` array element. Two `null` array elements are considered equal.

The comparison is consistent with equals, more specifically the following holds for arrays `a` and `b`:

```kotlin
<code>Arrays.equals(a, b) == (Arrays.compare(a, b) == 0)
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of comparable array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: the first array to compare |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: the second array to compare |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compare

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> compare(
    a: Array<T>?, 
    b: Array<T>?, 
    cmp: Comparator<in T>
): Int
```

Compares two `Object` arrays lexicographically using a specified comparator.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing with the specified comparator two elements at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

| Parameters ||
|---|---|
| `<T>` | the type of array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: the first array to compare |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: the second array to compare |
| --- | --- |
| `cmp` | [Comparator](Comparator.md)\<in T\>: the comparator to compare array elements |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the comparator is `null` |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: ByteArray?, 
    b: ByteArray?
): Int
```

Compares two `byte` arrays lexicographically, numerically treating elements as unsigned.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the first array to compare |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: ByteArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ByteArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `byte` arrays lexicographically over the specified ranges, numerically treating elements as unsigned.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is null |
| --- | --- |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: IntArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: IntArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `int` arrays lexicographically over the specified ranges, numerically treating elements as unsigned.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is null |
| --- | --- |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: IntArray?, 
    b: IntArray?
): Int
```

Compares two `int` arrays lexicographically, numerically treating elements as unsigned.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the first array to compare |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: LongArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: LongArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `long` arrays lexicographically over the specified ranges, numerically treating elements as unsigned.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is null |
| --- | --- |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: LongArray?, 
    b: LongArray?
): Int
```

Compares two `long` arrays lexicographically, numerically treating elements as unsigned.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the first array to compare |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: ShortArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ShortArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Compares two `short` arrays lexicographically over the specified ranges, numerically treating elements as unsigned.

If the two arrays, over the specified ranges, share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at a relative index within the respective arrays that is the length of the prefix. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two range lengths. (See mismatch for the definition of a common and proper prefix.)

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the first array to compare |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be compared |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be compared |
| --- | --- |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the second array to compare |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be compared |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be compared |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if, over the specified ranges, the first and second array are equal and contain the same elements in the same order; a value less than `0` if, over the specified ranges, the first array is lexicographically less than the second array; and a value greater than `0` if, over the specified ranges, the first array is lexicographically greater than the second array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is null |
| --- | --- |

### compareUnsigned

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compareUnsigned(
    a: ShortArray?, 
    b: ShortArray?
): Int
```

Compares two `short` arrays lexicographically, numerically treating elements as unsigned.

If the two arrays share a common prefix then the lexicographic comparison is the result of comparing two elements, as if by compareUnsigned, at an index within the respective arrays that is the prefix length. Otherwise, one array is a proper prefix of the other and, lexicographic comparison is the result of comparing the two array lengths. (See mismatch for the definition of a common and proper prefix.)

A `null` array reference is considered lexicographically less than a non-`null` array reference. Two `null` array references are considered equal.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the first array to compare |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the second array to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the first and second array are equal and contain the same elements in the same order; a value less than `0` if the first array is lexicographically less than the second array; and a value greater than `0` if the first array is lexicographically greater than the second array |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: BooleanArray, 
    newLength: Int
): BooleanArray
```

Copies the specified array, truncating or padding with `false` (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `false`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html` | a copy of the original array, truncated or padded with false elements to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: ByteArray, 
    newLength: Int
): ByteArray
```

Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `(byte)0`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | a copy of the original array, truncated or padded with zeros to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: CharArray, 
    newLength: Int
): CharArray
```

Copies the specified array, truncating or padding with null characters (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `'\u005cu0000'`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html` | a copy of the original array, truncated or padded with null characters to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: DoubleArray, 
    newLength: Int
): DoubleArray
```

Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `0d`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html` | a copy of the original array, truncated or padded with zeros to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: FloatArray, 
    newLength: Int
): FloatArray
```

Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `0f`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | a copy of the original array, truncated or padded with zeros to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: IntArray, 
    newLength: Int
): IntArray
```

Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `0`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | a copy of the original array, truncated or padded with zeros to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: LongArray, 
    newLength: Int
): LongArray
```

Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `0L`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html` | a copy of the original array, truncated or padded with zeros to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOf(
    original: ShortArray, 
    newLength: Int
): ShortArray
```

Copies the specified array, truncating or padding with zeros (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `(short)0`. Such indices will exist if and only if the specified length is greater than that of the original array.

| Parameters ||
|---|---|
| `original` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html` | a copy of the original array, truncated or padded with zeros to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> copyOf(
    original: Array<T>, 
    newLength: Int
): Array<T>
```

Copies the specified array, truncating or padding with nulls (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `null`. Such indices will exist if and only if the specified length is greater than that of the original array. The resulting array is of exactly the same class as the original array.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `original` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be copied |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | a copy of the original array, truncated or padded with nulls to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |

### copyOf

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, U : Any!> copyOf(
    original: Array<U>, 
    newLength: Int, 
    newType: Class<out Array<T>!>
): Array<T>
```

Copies the specified array, truncating or padding with nulls (if necessary) so the copy has the specified length. For all indices that are valid in both the original array and the copy, the two arrays will contain identical values. For any indices that are valid in the copy but not the original, the copy will contain `null`. Such indices will exist if and only if the specified length is greater than that of the original array. The resulting array is of the class `newType`.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the returned array |
| `<U>` | the class of the objects in the original array |
| `original` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<U\>: the array to be copied |
| --- | --- |
| `newLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the copy to be returned |
| `newType` | [Class](../java.lang/Class.md)\<out [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>!\>: the class of the copy to be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | a copy of the original array, truncated or padded with nulls to obtain the specified length |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if an element copied from `original` is not of a runtime type that can be stored in an array of class `newType` |
| `java.lang.NegativeArraySizeException` | if `newLength` is negative |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: BooleanArray, 
    from: Int, 
    to: Int
): BooleanArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `false` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html` | a new array containing the specified range from the original array, truncated or padded with false elements to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: ByteArray, 
    from: Int, 
    to: Int
): ByteArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `(byte)0` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | a new array containing the specified range from the original array, truncated or padded with zeros to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: CharArray, 
    from: Int, 
    to: Int
): CharArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `'\u005cu0000'` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html` | a new array containing the specified range from the original array, truncated or padded with null characters to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: DoubleArray, 
    from: Int, 
    to: Int
): DoubleArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `0d` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html` | a new array containing the specified range from the original array, truncated or padded with zeros to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: FloatArray, 
    from: Int, 
    to: Int
): FloatArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `0f` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | a new array containing the specified range from the original array, truncated or padded with zeros to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: IntArray, 
    from: Int, 
    to: Int
): IntArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `0` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html` | a new array containing the specified range from the original array, truncated or padded with zeros to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: LongArray, 
    from: Int, 
    to: Int
): LongArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `0L` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html` | a new array containing the specified range from the original array, truncated or padded with zeros to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyOfRange(
    original: ShortArray, 
    from: Int, 
    to: Int
): ShortArray
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `(short)0` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

| Parameters ||
|---|---|
| `original` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html` | a new array containing the specified range from the original array, truncated or padded with zeros to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> copyOfRange(
    original: Array<T>, 
    from: Int, 
    to: Int
): Array<T>
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `null` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`.

The resulting array is of exactly the same class as the original array.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `original` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array from which a range is to be copied |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| --- | --- |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | a new array containing the specified range from the original array, truncated or padded with nulls to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.IllegalArgumentException` | if `from > to` |
| `java.lang.NullPointerException` | if `original` is null |
| --- | --- |

### copyOfRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!, U : Any!> copyOfRange(
    original: Array<U>, 
    from: Int, 
    to: Int, 
    newType: Class<out Array<T>!>
): Array<T>
```

Copies the specified range of the specified array into a new array. The initial index of the range (`from`) must lie between zero and `original.length`, inclusive. The value at `original[from]` is placed into the initial element of the copy (unless `from == original.length` or `from == to`). Values from subsequent elements in the original array are placed into subsequent elements in the copy. The final index of the range (`to`), which must be greater than or equal to `from`, may be greater than `original.length`, in which case `null` is placed in all elements of the copy whose index is greater than or equal to `original.length - from`. The length of the returned array will be `to - from`. The resulting array is of the class `newType`.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the returned array |
| `<U>` | the class of the objects in the original array |
| `original` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<U\>: the array from which a range is to be copied |
| --- | --- |
| `from` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the initial index of the range to be copied, inclusive |
| `to` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the final index of the range to be copied, exclusive. (This index may lie outside the array.) |
| `newType` | [Class](../java.lang/Class.md)\<out [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>!\>: the class of the copy to be returned |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | a new array containing the specified range from the original array, truncated or padded with nulls to obtain the required length |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `from < 0` or `from > original.length` |
| `java.lang.ArrayStoreException` | if an element copied from `original` is not of a runtime type that can be stored in an array of class `newType`. |
| `java.lang.IllegalArgumentException` | if `from > to` |
| --- | --- |
| `java.lang.NullPointerException` | if `original` is null |

### deepEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun deepEquals(
    a1: Array<Any!>?, 
    a2: Array<Any!>?
): Boolean
```

Returns `true` if the two specified arrays are *deeply equal* to one another. Unlike the equals method, this method is appropriate for use with nested arrays of arbitrary depth.

Two array references are considered deeply equal if both are `null`, or if they refer to arrays that contain the same number of elements and all corresponding pairs of elements in the two arrays are deeply equal.

Two possibly `null` elements `e1` and `e2` are deeply equal if any of the following conditions hold:

- `e1` and `e2` are both arrays of object reference types, and `Arrays.deepEquals(e1, e2) would return true`
- `e1` and `e2` are arrays of the same primitive type, and the appropriate overloading of `Arrays.equals(e1, e2)` would return true.
- `e1 == e2`
- `e1.equals(e2)` would return true.

Note that this definition permits `null` elements at any depth.

If either of the specified arrays contain themselves as elements either directly or indirectly through one or more levels of arrays, the behavior of this method is undefined.

| Parameters ||
|---|---|
| `a1` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: one array to be tested for equality |
| `a2` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

**See Also**

- equals
- deepEquals

### deepHashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun deepHashCode(a: Array<Any!>?): Int
```

Returns a hash code based on the "deep contents" of the specified array. If the array contains other arrays as elements, the hash code is based on their contents and so on, ad infinitum. It is therefore unacceptable to invoke this method on an array that contains itself as an element, either directly or indirectly through one or more levels of arrays. The behavior of such an invocation is undefined.

For any two arrays `a` and `b` such that `Arrays.deepEquals(a, b)`, it is also the case that `Arrays.deepHashCode(a) == Arrays.deepHashCode(b)`.

The computation of the value returned by this method is similar to that of the value returned by java.util.List#hashCode() on a list containing the same elements as `a` in the same order, with one difference: If an element `e` of `a` is itself an array, its hash code is computed not by calling `e.hashCode()`, but as by calling the appropriate overloading of `Arrays.hashCode(e)` if `e` is an array of a primitive type, or as by calling `Arrays.deepHashCode(e)` recursively if `e` is an array of a reference type. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: the array whose deep-content-based hash code to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a deep-content-based hash code for `a` |

**See Also**

- hashCode

### deepToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun deepToString(a: Array<Any!>?): String
```

Returns a string representation of the "deep contents" of the specified array. If the array contains other arrays as elements, the string representation contains their contents and so on. This method is designed for converting multidimensional arrays to strings.

The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(Object)`, unless they are themselves arrays.

If an element `e` is an array of a primitive type, it is converted to a string as by invoking the appropriate overloading of `Arrays.toString(e)`. If an element `e` is an array of a reference type, it is converted to a string as by invoking this method recursively.

To avoid infinite recursion, if the specified array contains itself as an element, or contains an indirect reference to itself through one or more levels of arrays, the self-reference is converted to the string `"[...]"`. For example, an array containing only a reference to itself would be rendered as `"[[...]]"`.

This method returns `"null"` if the specified array is `null`.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

**See Also**

- toString

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: BooleanArray?, 
    a2: BooleanArray?
): Boolean
```

Returns `true` if the two specified arrays of booleans are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: one array to be tested for equality |
| `a2` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: BooleanArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: BooleanArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of booleans, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: ByteArray?, 
    a2: ByteArray?
): Boolean
```

Returns `true` if the two specified arrays of bytes are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: one array to be tested for equality |
| `a2` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: ByteArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ByteArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of bytes, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: CharArray?, 
    a2: CharArray?
): Boolean
```

Returns `true` if the two specified arrays of chars are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: one array to be tested for equality |
| `a2` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: CharArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: CharArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of chars, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: DoubleArray?, 
    a2: DoubleArray?
): Boolean
```

Returns `true` if the two specified arrays of doubles are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`. Two doubles `d1` and `d2` are considered equal if:

```kotlin
<code>Double.valueOf(d1).equals(Double.valueOf(d2))</code>
```
(Unlike the `==` operator, this method considers `NaN` equal to itself, and 0.0d unequal to -0.0d.)

<br />

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: one array to be tested for equality |
| `a2` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

**See Also**

- equals

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: DoubleArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: DoubleArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of doubles, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

Two doubles `d1` and `d2` are considered equal if:

```kotlin
<code>Double.valueOf(d1).equals(Double.valueOf(d2))</code>
```
(Unlike the `==` operator, this method considers `NaN` equal to itself, and 0.0d unequal to -0.0d.)

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

**See Also**

- equals

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: FloatArray?, 
    a2: FloatArray?
): Boolean
```

Returns `true` if the two specified arrays of floats are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`. Two floats `f1` and `f2` are considered equal if:

```kotlin
<code>Float.valueOf(f1).equals(Float.valueOf(f2))</code>
```
(Unlike the `==` operator, this method considers `NaN` equal to itself, and 0.0f unequal to -0.0f.)

<br />

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: one array to be tested for equality |
| `a2` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

**See Also**

- equals

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: FloatArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: FloatArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of floats, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

Two floats `f1` and `f2` are considered equal if:

```kotlin
<code>Float.valueOf(f1).equals(Float.valueOf(f2))</code>
```
(Unlike the `==` operator, this method considers `NaN` equal to itself, and 0.0f unequal to -0.0f.)

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

**See Also**

- equals

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: IntArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: IntArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of ints, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: IntArray?, 
    a2: IntArray?
): Boolean
```

Returns `true` if the two specified arrays of ints are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: one array to be tested for equality |
| `a2` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: Array<Any!>, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: Array<Any!>, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of Objects, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

Two objects `e1` and `e2` are considered *equal* if `Objects.equals(e1, e2)`.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: Array<Any!>?, 
    a2: Array<Any!>?
): Boolean
```

Returns `true` if the two specified arrays of Objects are *equal* to one another. The two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. Two objects `e1` and `e2` are considered *equal* if `Objects.equals(e1, e2)`. In other words, the two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: one array to be tested for equality |
| `a2` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: LongArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: LongArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of longs, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: LongArray?, 
    a2: LongArray?
): Boolean
```

Returns `true` if the two specified arrays of longs are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: one array to be tested for equality |
| `a2` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: ShortArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ShortArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Boolean
```

Returns true if the two specified arrays of shorts, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun equals(
    a: ShortArray?, 
    a2: ShortArray?
): Boolean
```

Returns `true` if the two specified arrays of shorts are *equal* to one another. Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: one array to be tested for equality |
| `a2` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the other array to be tested for equality |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> equals(
    a: Array<T>, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: Array<T>, 
    bFromIndex: Int, 
    bToIndex: Int, 
    cmp: Comparator<in T>
): Boolean
```

Returns true if the two specified arrays of Objects, over the specified ranges, are *equal* to one another.

Two arrays are considered equal if the number of elements covered by each range is the same, and all corresponding pairs of elements over the specified ranges in the two arrays are equal. In other words, two arrays are equal if they contain, over the specified ranges, the same elements in the same order.

Two objects `e1` and `e2` are considered *equal* if, given the specified comparator, `cmp.compare(e1, e2) == 0`.

| Parameters ||
|---|---|
| `<T>` | the type of array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the first array to be tested for equality |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| --- | --- |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the second array to be tested for equality |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| --- | --- |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| `cmp` | [Comparator](Comparator.md)\<in T\>: the comparator to compare array elements |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays, over the specified ranges, are equal |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array or the comparator is `null` |
| --- | --- |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> equals(
    a: Array<T>?, 
    a2: Array<T>?, 
    cmp: Comparator<in T>
): Boolean
```

Returns `true` if the two specified arrays of Objects are *equal* to one another.

Two arrays are considered equal if both arrays contain the same number of elements, and all corresponding pairs of elements in the two arrays are equal. In other words, the two arrays are equal if they contain the same elements in the same order. Also, two array references are considered equal if both are `null`.

Two objects `e1` and `e2` are considered *equal* if, given the specified comparator, `cmp.compare(e1, e2) == 0`.

| Parameters ||
|---|---|
| `<T>` | the type of array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: one array to be tested for equality |
| `a2` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>?: the other array to be tested for equality |
| --- | --- |
| `cmp` | [Comparator](Comparator.md)\<in T\>: the comparator to compare array elements |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the two arrays are equal |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the comparator is `null` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: BooleanArray, 
    val: Boolean
): Unit
```

Assigns the specified boolean value to each element of the specified array of booleans.

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the array to be filled |
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: BooleanArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Boolean
): Unit
```

Assigns the specified boolean value to each element of the specified range of the specified array of booleans. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: ByteArray, 
    val: Byte
): Unit
```

Assigns the specified byte value to each element of the specified array of bytes.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be filled |
| `val` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: ByteArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Byte
): Unit
```

Assigns the specified byte value to each element of the specified range of the specified array of bytes. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: CharArray, 
    val: Char
): Unit
```

Assigns the specified char value to each element of the specified array of chars.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be filled |
| `val` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: CharArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Char
): Unit
```

Assigns the specified char value to each element of the specified range of the specified array of chars. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: DoubleArray, 
    val: Double
): Unit
```

Assigns the specified double value to each element of the specified array of doubles.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be filled |
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: DoubleArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Double
): Unit
```

Assigns the specified double value to each element of the specified range of the specified array of doubles. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: FloatArray, 
    val: Float
): Unit
```

Assigns the specified float value to each element of the specified array of floats.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be filled |
| `val` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: FloatArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Float
): Unit
```

Assigns the specified float value to each element of the specified range of the specified array of floats. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: IntArray, 
    val: Int
): Unit
```

Assigns the specified int value to each element of the specified array of ints.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be filled |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: IntArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Int
): Unit
```

Assigns the specified int value to each element of the specified range of the specified array of ints. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: Array<Any!>, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Any?
): Unit
```

Assigns the specified Object reference to each element of the specified range of the specified array of Objects. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.ArrayStoreException` | if the specified value is not of a runtime type that can be stored in the specified array |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| --- | --- |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: Array<Any!>, 
    val: Any?
): Unit
```

Assigns the specified Object reference to each element of the specified array of Objects.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the array to be filled |
| `val` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if the specified value is not of a runtime type that can be stored in the specified array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: LongArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Long
): Unit
```

Assigns the specified long value to each element of the specified range of the specified array of longs. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: LongArray, 
    val: Long
): Unit
```

Assigns the specified long value to each element of the specified array of longs.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be filled |
| `val` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to be stored in all elements of the array |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: ShortArray, 
    fromIndex: Int, 
    toIndex: Int, 
    val: Short
): Unit
```

Assigns the specified short value to each element of the specified range of the specified array of shorts. The range to be filled extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be filled is empty.)

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be filled |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be filled with the specified value |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be filled with the specified value |
| --- | --- |
| `val` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the value to be stored in all elements of the array |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun fill(
    a: ShortArray, 
    val: Short
): Unit
```

Assigns the specified short value to each element of the specified array of shorts.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be filled |
| `val` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): the value to be stored in all elements of the array |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: BooleanArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `boolean` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Boolean.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: ByteArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `byte` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Byte.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: CharArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `char` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Character.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: DoubleArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `double` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Double.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: FloatArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `float` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Float.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: IntArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two non-null `int` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Integer.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: Array<Any!>?): Int
```

Returns a hash code based on the contents of the specified array. If the array contains other arrays as elements, the hash code is based on their identities rather than their contents. It is therefore acceptable to invoke this method on an array that contains itself as an element, either directly or indirectly through one or more levels of arrays.

For any two arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is equal to the value that would be returned by `Arrays.asList(a).hashCode()`, unless `a` is `null`, in which case `0` is returned.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: the array whose content-based hash code to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

**See Also**

- deepHashCode

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: LongArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `long` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Long.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(a: ShortArray?): Int
```

Returns a hash code based on the contents of the specified array. For any two `short` arrays `a` and `b` such that `Arrays.equals(a, b)`, it is also the case that `Arrays.hashCode(a) == Arrays.hashCode(b)`.

The value returned by this method is the same value that would be obtained by invoking the java.util.List#hashCode() method on a List containing a sequence of `https://developer.android.com/reference/kotlin/java/lang/Short.html#` instances representing the elements of `a` in the same order. If `a` is `null`, this method returns 0.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the array whose hash value to compute |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a content-based hash code for `a` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: BooleanArray, 
    b: BooleanArray
): Int
```

Finds and returns the index of the first mismatch between two `boolean` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      a[pl] != b[pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the first array to be tested for a mismatch |
| `b` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: BooleanArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: BooleanArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `boolean` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      a[aFromIndex + pl] != b[bFromIndex + pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: ByteArray, 
    b: ByteArray
): Int
```

Finds and returns the index of the first mismatch between two `byte` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      a[pl] != b[pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the first array to be tested for a mismatch |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: ByteArray!, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ByteArray!, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `byte` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      a[aFromIndex + pl] != b[bFromIndex + pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: CharArray, 
    b: CharArray
): Int
```

Finds and returns the index of the first mismatch between two `char` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      a[pl] != b[pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the first array to be tested for a mismatch |
| `b` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: CharArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: CharArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `char` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      a[aFromIndex + pl] != b[bFromIndex + pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: DoubleArray, 
    b: DoubleArray
): Int
```

Finds and returns the index of the first mismatch between two `double` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      Double.compare(a[pl], b[pl]) != 0
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the first array to be tested for a mismatch |
| `b` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: DoubleArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: DoubleArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `double` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      Double.compare(a[aFromIndex + pl], b[bFromIndex + pl]) != 0
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: FloatArray, 
    b: FloatArray
): Int
```

Finds and returns the index of the first mismatch between two `float` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      Float.compare(a[pl], b[pl]) != 0
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the first array to be tested for a mismatch |
| `b` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: FloatArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: FloatArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `float` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      Float.compare(a[aFromIndex + pl], b[bFromIndex + pl]) != 0
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: IntArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: IntArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `int` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      a[aFromIndex + pl] != b[bFromIndex + pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: IntArray, 
    b: IntArray
): Int
```

Finds and returns the index of the first mismatch between two `int` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      a[pl] != b[pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the first array to be tested for a mismatch |
| `b` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: Array<Any!>, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: Array<Any!>, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `Object` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      !Objects.equals(a[aFromIndex + pl], b[bFromIndex + pl])
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: Array<Any!>, 
    b: Array<Any!>
): Int
```

Finds and returns the index of the first mismatch between two `Object` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      !Objects.equals(a[pl], b[pl])
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the first array to be tested for a mismatch |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: LongArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: LongArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `long` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      a[aFromIndex + pl] != b[bFromIndex + pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: LongArray, 
    b: LongArray
): Int
```

Finds and returns the index of the first mismatch between two `long` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      a[pl] != b[pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the first array to be tested for a mismatch |
| `b` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: ShortArray, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: ShortArray, 
    bFromIndex: Int, 
    bToIndex: Int
): Int
```

Finds and returns the relative index of the first mismatch between two `short` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl) &amp;&amp;
      a[aFromIndex + pl] != b[bFromIndex + pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex))
  </code>
```

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| --- | --- |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun mismatch(
    a: ShortArray, 
    b: ShortArray
): Int
```

Finds and returns the index of the first mismatch between two `short` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl) &amp;&amp;
      a[pl] != b[pl]
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length))
  </code>
```

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the first array to be tested for a mismatch |
| `b` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the second array to be tested for a mismatch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array is `null` |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> mismatch(
    a: Array<T>, 
    aFromIndex: Int, 
    aToIndex: Int, 
    b: Array<T>, 
    bFromIndex: Int, 
    bToIndex: Int, 
    cmp: Comparator<in T>
): Int
```

Finds and returns the relative index of the first mismatch between two `Object` arrays over the specified ranges, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller range.

If the two arrays, over the specified ranges, share a common prefix then the returned relative index is the length of the common prefix and it follows that there is a mismatch between the two elements at that relative index within the respective arrays. If one array is a proper prefix of the other, over the specified ranges, then the returned relative index is the length of the smaller range and it follows that the relative index is only valid for the array with the larger range. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, aFromIndex, aFromIndex + pl, b, bFromIndex, bFromIndex + pl, cmp) &amp;&amp;
      cmp.compare(a[aFromIndex + pl], b[bFromIndex + pl]) != 0
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b` with specified ranges \[`aFromIndex`, `aToIndex`) and \[`bFromIndex`, `bToIndex`) respectively, share a proper prefix if the following expression is true:

```kotlin
<code>(aToIndex - aFromIndex) != (bToIndex - bFromIndex) &amp;&amp;
      Arrays.equals(a, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    b, 0, Math.min(aToIndex - aFromIndex, bToIndex - bFromIndex),
                    cmp)
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the first array to be tested for a mismatch |
| `aFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the first array to be tested |
| --- | --- |
| `aToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the first array to be tested |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the second array to be tested for a mismatch |
| `bFromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (inclusive) of the first element in the second array to be tested |
| --- | --- |
| `bToIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index (exclusive) of the last element in the second array to be tested |
| `cmp` | [Comparator](Comparator.md)\<in T\>: the comparator to compare array elements |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the relative index of the first mismatch between the two arrays over the specified ranges, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `aFromIndex < 0 or aToIndex > a.length` or if `bFromIndex < 0 or bToIndex > b.length` |
| `java.lang.IllegalArgumentException` | if `aFromIndex > aToIndex` or if `bFromIndex > bToIndex` |
| `java.lang.NullPointerException` | if either array or the comparator is `null` |
| --- | --- |

### mismatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> mismatch(
    a: Array<T>, 
    b: Array<T>, 
    cmp: Comparator<in T>
): Int
```

Finds and returns the index of the first mismatch between two `Object` arrays, otherwise return -1 if no mismatch is found. The index will be in the range of 0 (inclusive) up to the length (inclusive) of the smaller array.

The specified comparator is used to determine if two array elements from the each array are not equal.

If the two arrays share a common prefix then the returned index is the length of the common prefix and it follows that there is a mismatch between the two elements at that index within the respective arrays. If one array is a proper prefix of the other then the returned index is the length of the smaller array and it follows that the index is only valid for the larger array. Otherwise, there is no mismatch.

Two non-`null` arrays, `a` and `b`, share a common prefix of length `pl` if the following expression is true:

```kotlin
<code>pl &gt;= 0 &amp;&amp;
      pl &lt; Math.min(a.length, b.length) &amp;&amp;
      Arrays.equals(a, 0, pl, b, 0, pl, cmp)
      cmp.compare(a[pl], b[pl]) != 0
  </code>
```
Note that a common prefix length of `0` indicates that the first elements from each array mismatch.

Two non-`null` arrays, `a` and `b`, share a proper prefix if the following expression is true:

```kotlin
<code>a.length != b.length &amp;&amp;
      Arrays.equals(a, 0, Math.min(a.length, b.length),
                    b, 0, Math.min(a.length, b.length),
                    cmp)
  </code>
```

| Parameters ||
|---|---|
| `<T>` | the type of array elements |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the first array to be tested for a mismatch |
| `b` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the second array to be tested for a mismatch |
| --- | --- |
| `cmp` | [Comparator](Comparator.md)\<in T\>: the comparator to compare array elements |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first mismatch between the two arrays, otherwise `-1`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if either array or the comparator is `null` |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelPrefix(
    array: DoubleArray, 
    fromIndex: Int, 
    toIndex: Int, 
    op: DoubleBinaryOperator
): Unit
```

Performs parallelPrefix for the given subrange of the array.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive |
| --- | --- |
| `op` | [DoubleBinaryOperator](../java.util.function/DoubleBinaryOperator.md): a side-effect-free, associative function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > array.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| `java.lang.NullPointerException` | if the specified array or function is null |
| --- | --- |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelPrefix(
    array: DoubleArray, 
    op: DoubleBinaryOperator
): Unit
```

Cumulates, in parallel, each element of the given array in place, using the supplied function. For example if the array initially holds `[2.0, 1.0, 0.0, 3.0]` and the operation performs addition, then upon return the array holds `[2.0, 3.0, 3.0, 6.0]`. Parallel prefix computation is usually more efficient than sequential loops for large arrays.

Because floating-point operations may not be strictly associative, the returned result may not be identical to the value that would be obtained if the operation was performed sequentially.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array, which is modified in-place by this method |
| `op` | [DoubleBinaryOperator](../java.util.function/DoubleBinaryOperator.md): a side-effect-free function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified array or function is null |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelPrefix(
    array: IntArray, 
    fromIndex: Int, 
    toIndex: Int, 
    op: IntBinaryOperator
): Unit
```

Performs parallelPrefix for the given subrange of the array.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive |
| --- | --- |
| `op` | [IntBinaryOperator](../java.util.function/IntBinaryOperator.md): a side-effect-free, associative function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > array.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| `java.lang.NullPointerException` | if the specified array or function is null |
| --- | --- |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelPrefix(
    array: IntArray, 
    op: IntBinaryOperator
): Unit
```

Cumulates, in parallel, each element of the given array in place, using the supplied function. For example if the array initially holds `[2, 1, 0, 3]` and the operation performs addition, then upon return the array holds `[2, 3, 3, 6]`. Parallel prefix computation is usually more efficient than sequential loops for large arrays.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array, which is modified in-place by this method |
| `op` | [IntBinaryOperator](../java.util.function/IntBinaryOperator.md): a side-effect-free, associative function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified array or function is null |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelPrefix(
    array: LongArray, 
    fromIndex: Int, 
    toIndex: Int, 
    op: LongBinaryOperator
): Unit
```

Performs parallelPrefix for the given subrange of the array.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive |
| --- | --- |
| `op` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md): a side-effect-free, associative function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > array.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| `java.lang.NullPointerException` | if the specified array or function is null |
| --- | --- |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelPrefix(
    array: LongArray, 
    op: LongBinaryOperator
): Unit
```

Cumulates, in parallel, each element of the given array in place, using the supplied function. For example if the array initially holds `[2, 1, 0, 3]` and the operation performs addition, then upon return the array holds `[2, 3, 3, 6]`. Parallel prefix computation is usually more efficient than sequential loops for large arrays.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array, which is modified in-place by this method |
| `op` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md): a side-effect-free, associative function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified array or function is null |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> parallelPrefix(
    array: Array<T>, 
    fromIndex: Int, 
    toIndex: Int, 
    op: BinaryOperator<T>
): Unit
```

Performs parallelPrefix for the given subrange of the array.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive |
| --- | --- |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive |
| `op` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<T\>: a side-effect-free, associative function to perform the cumulation |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > array.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |
| `java.lang.NullPointerException` | if the specified array or function is null |
| --- | --- |

### parallelPrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> parallelPrefix(
    array: Array<T>, 
    op: BinaryOperator<T>
): Unit
```

Cumulates, in parallel, each element of the given array in place, using the supplied function. For example if the array initially holds `[2, 1, 0, 3]` and the operation performs addition, then upon return the array holds `[2, 3, 3, 6]`. Parallel prefix computation is usually more efficient than sequential loops for large arrays.

| Parameters ||
|---|---|
| `<T>` | the class of the objects in the array |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array, which is modified in-place by this method |
| `op` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<T\>: a side-effect-free, associative function to perform the cumulation |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified array or function is null |

### parallelSetAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSetAll(
    array: DoubleArray, 
    generator: IntToDoubleFunction
): Unit
```

Set all elements of the specified array, in parallel, using the provided generator function to compute each element.

If the generator function throws an exception, an unchecked exception is thrown from `parallelSetAll` and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): array to be initialized |
| `generator` | [IntToDoubleFunction](../java.util.function/IntToDoubleFunction.md): a function accepting an index and producing the desired value for that position |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### parallelSetAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSetAll(
    array: IntArray, 
    generator: IntUnaryOperator
): Unit
```

Set all elements of the specified array, in parallel, using the provided generator function to compute each element.

If the generator function throws an exception, an unchecked exception is thrown from `parallelSetAll` and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): array to be initialized |
| `generator` | [IntUnaryOperator](../java.util.function/IntUnaryOperator.md): a function accepting an index and producing the desired value for that position |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### parallelSetAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSetAll(
    array: LongArray, 
    generator: IntToLongFunction
): Unit
```

Set all elements of the specified array, in parallel, using the provided generator function to compute each element.

If the generator function throws an exception, an unchecked exception is thrown from `parallelSetAll` and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): array to be initialized |
| `generator` | [IntToLongFunction](../java.util.function/IntToLongFunction.md): a function accepting an index and producing the desired value for that position |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### parallelSetAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> parallelSetAll(
    array: Array<T>, 
    generator: IntFunction<out T>
): Unit
```

Set all elements of the specified array, in parallel, using the provided generator function to compute each element.

If the generator function throws an exception, an unchecked exception is thrown from `parallelSetAll` and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `<T>` | type of elements of the array |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: array to be initialized |
| `generator` | [IntFunction](../java.util.function/IntFunction.md)\<out T\>: a function accepting an index and producing the desired value for that position |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: ByteArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: ByteArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: CharArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: CharArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: DoubleArray): Unit
```

Sorts the specified array into ascending numerical order.

The `<` relation does not provide a total order on all double values: `-0.0d == 0.0d` is `true` and a `Double.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0d` is treated as less than value `0.0d` and `Double.NaN` is considered greater than any other value and all `Double.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: DoubleArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

The `<` relation does not provide a total order on all double values: `-0.0d == 0.0d` is `true` and a `Double.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0d` is treated as less than value `0.0d` and `Double.NaN` is considered greater than any other value and all `Double.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: FloatArray): Unit
```

Sorts the specified array into ascending numerical order.

The `<` relation does not provide a total order on all float values: `-0.0f == 0.0f` is `true` and a `Float.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0f` is treated as less than value `0.0f` and `Float.NaN` is considered greater than any other value and all `Float.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: FloatArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

The `<` relation does not provide a total order on all float values: `-0.0f == 0.0f` is `true` and a `Float.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0f` is treated as less than value `0.0f` and `Float.NaN` is considered greater than any other value and all `Float.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: IntArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: IntArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: LongArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: LongArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(a: ShortArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be sorted |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun parallelSort(
    a: ShortArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending numerical order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Comparable<T>!> parallelSort(a: Array<T>): Unit
```

Sorts the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. All elements in the array must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface. Furthermore, all elements in the array must be *mutually comparable* (that is, `e1.compareTo(e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the array).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

| Parameters ||
|---|---|
| `<T>` | the class of the objects to be sorted |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be sorted |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* (for example, strings and integers) |
| `java.lang.IllegalArgumentException` | (optional) if the natural ordering of the array elements is found to violate the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` contract |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Comparable<T>!> parallelSort(
    a: Array<T>, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. The range to be sorted extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be sorted is empty.) All elements in this range must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface. Furthermore, all elements in this range must be *mutually comparable* (that is, `e1.compareTo(e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the array).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

| Parameters ||
|---|---|
| `<T>` | the class of the objects to be sorted |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be sorted |
| --- | --- |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be sorted |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* (for example, strings and integers). |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` or (optional) if the natural ordering of the array elements is found to violate the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` contract |
| --- | --- |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> parallelSort(
    a: Array<T>, 
    fromIndex: Int, 
    toIndex: Int, 
    cmp: Comparator<in T>?
): Unit
```

Sorts the specified range of the specified array of objects according to the order induced by the specified comparator. The range to be sorted extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be sorted is empty.) All elements in the range must be *mutually comparable* by the specified comparator (that is, `c.compare(e1, e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the range).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

| Parameters ||
|---|---|
| `<T>` | the class of the objects to be sorted |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be sorted |
| --- | --- |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be sorted |
| `cmp` | [Comparator](Comparator.md)\<in T\>?: the comparator to determine the order of the array. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* (for example, strings and integers). |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` or (optional) if the natural ordering of the array elements is found to violate the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` contract |
| --- | --- |

### parallelSort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> parallelSort(
    a: Array<T>, 
    cmp: Comparator<in T>?
): Unit
```

Sorts the specified array of objects according to the order induced by the specified comparator. All elements in the array must be *mutually comparable* by the specified comparator (that is, `c.compare(e1, e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the array).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

| Parameters ||
|---|---|
| `<T>` | the class of the objects to be sorted |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be sorted |
| `cmp` | [Comparator](Comparator.md)\<in T\>?: the comparator to determine the order of the array. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* using the specified comparator |
| `java.lang.IllegalArgumentException` | (optional) if the comparator is found to violate the Comparator contract |

### setAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setAll(
    array: DoubleArray, 
    generator: IntToDoubleFunction
): Unit
```

Set all elements of the specified array, using the provided generator function to compute each element.

If the generator function throws an exception, it is relayed to the caller and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): array to be initialized |
| `generator` | [IntToDoubleFunction](../java.util.function/IntToDoubleFunction.md): a function accepting an index and producing the desired value for that position |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### setAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setAll(
    array: IntArray, 
    generator: IntUnaryOperator
): Unit
```

Set all elements of the specified array, using the provided generator function to compute each element.

If the generator function throws an exception, it is relayed to the caller and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): array to be initialized |
| `generator` | [IntUnaryOperator](../java.util.function/IntUnaryOperator.md): a function accepting an index and producing the desired value for that position |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### setAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setAll(
    array: LongArray, 
    generator: IntToLongFunction
): Unit
```

Set all elements of the specified array, using the provided generator function to compute each element.

If the generator function throws an exception, it is relayed to the caller and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): array to be initialized |
| `generator` | [IntToLongFunction](../java.util.function/IntToLongFunction.md): a function accepting an index and producing the desired value for that position |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### setAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> setAll(
    array: Array<T>, 
    generator: IntFunction<out T>
): Unit
```

Set all elements of the specified array, using the provided generator function to compute each element.

If the generator function throws an exception, it is relayed to the caller and the array is left in an indeterminate state.

| Parameters ||
|---|---|
| `<T>` | type of elements of the array |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: array to be initialized |
| `generator` | [IntFunction](../java.util.function/IntFunction.md)\<out T\>: a function accepting an index and producing the desired value for that position |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the generator is null |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: ByteArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: ByteArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: CharArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: CharArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: DoubleArray): Unit
```

Sorts the specified array into ascending numerical order.

The `<` relation does not provide a total order on all double values: `-0.0d == 0.0d` is `true` and a `Double.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0d` is treated as less than value `0.0d` and `Double.NaN` is considered greater than any other value and all `Double.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: DoubleArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

The `<` relation does not provide a total order on all double values: `-0.0d == 0.0d` is `true` and a `Double.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0d` is treated as less than value `0.0d` and `Double.NaN` is considered greater than any other value and all `Double.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: FloatArray): Unit
```

Sorts the specified array into ascending numerical order.

The `<` relation does not provide a total order on all float values: `-0.0f == 0.0f` is `true` and a `Float.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0f` is treated as less than value `0.0f` and `Float.NaN` is considered greater than any other value and all `Float.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: FloatArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

The `<` relation does not provide a total order on all float values: `-0.0f == 0.0f` is `true` and a `Float.NaN` value compares neither less than, greater than, nor equal to any value, even itself. This method uses the total order imposed by the method compareTo: `-0.0f` is treated as less than value `0.0f` and `Float.NaN` is considered greater than any other value and all `Float.NaN` values are considered equal.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: IntArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: IntArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: Array<Any!>): Unit
```

Sorts the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. All elements in the array must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface. Furthermore, all elements in the array must be *mutually comparable* (that is, `e1.compareTo(e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the array).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

Implementation note: This implementation is a stable, adaptive, iterative mergesort that requires far fewer than n lg(n) comparisons when the input array is partially sorted, while offering the performance of a traditional mergesort when the input array is randomly ordered. If the input array is nearly sorted, the implementation requires approximately n comparisons. Temporary storage requirements vary from a small constant for nearly sorted input arrays to n/2 object references for randomly ordered input arrays.

The implementation takes equal advantage of ascending and descending order in its input array, and can take advantage of ascending and descending order in different parts of the same input array. It is well-suited to merging two or more sorted arrays: simply concatenate the arrays and sort the resulting array.

The implementation was adapted from Tim Peters's list sort for Python ([TimSort](http://svn.python.org/projects/python/trunk/Objects/listsort.txt)). It uses techniques from Peter McIlroy's "Optimistic Sorting and Information Theoretic Complexity", in Proceedings of the Fourth Annual ACM-SIAM Symposium on Discrete Algorithms, pp 467-474, January 1993.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the array to be sorted |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* (for example, strings and integers) |
| `java.lang.IllegalArgumentException` | (optional) if the natural ordering of the array elements is found to violate the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` contract |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: Array<Any!>, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the specified array of objects into ascending order, according to the [natural ordering](../java.lang/Comparable.md) of its elements. The range to be sorted extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be sorted is empty.) All elements in this range must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface. Furthermore, all elements in this range must be *mutually comparable* (that is, `e1.compareTo(e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the array).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

Implementation note: This implementation is a stable, adaptive, iterative mergesort that requires far fewer than n lg(n) comparisons when the input array is partially sorted, while offering the performance of a traditional mergesort when the input array is randomly ordered. If the input array is nearly sorted, the implementation requires approximately n comparisons. Temporary storage requirements vary from a small constant for nearly sorted input arrays to n/2 object references for randomly ordered input arrays.

The implementation takes equal advantage of ascending and descending order in its input array, and can take advantage of ascending and descending order in different parts of the same input array. It is well-suited to merging two or more sorted arrays: simply concatenate the arrays and sort the resulting array.

The implementation was adapted from Tim Peters's list sort for Python ([TimSort](http://svn.python.org/projects/python/trunk/Objects/listsort.txt)). It uses techniques from Peter McIlroy's "Optimistic Sorting and Information Theoretic Complexity", in Proceedings of the Fourth Annual ACM-SIAM Symposium on Discrete Algorithms, pp 467-474, January 1993.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>: the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* (for example, strings and integers). |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` or (optional) if the natural ordering of the array elements is found to violate the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` contract |
| --- | --- |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: LongArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: LongArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(a: ShortArray): Unit
```

Sorts the specified array into ascending numerical order.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be sorted |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun sort(
    a: ShortArray, 
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Sorts the specified range of the array into ascending order. The range to be sorted extends from the index `fromIndex`, inclusive, to the index `toIndex`, exclusive. If `fromIndex == toIndex`, the range to be sorted is empty.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html): the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element, inclusive, to be sorted |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element, exclusive, to be sorted |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> sort(
    a: Array<T>, 
    fromIndex: Int, 
    toIndex: Int, 
    c: Comparator<in T>?
): Unit
```

Sorts the specified range of the specified array of objects according to the order induced by the specified comparator. The range to be sorted extends from index `fromIndex`, inclusive, to index `toIndex`, exclusive. (If `fromIndex==toIndex`, the range to be sorted is empty.) All elements in the range must be *mutually comparable* by the specified comparator (that is, `c.compare(e1, e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the range).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

Implementation note: This implementation is a stable, adaptive, iterative mergesort that requires far fewer than n lg(n) comparisons when the input array is partially sorted, while offering the performance of a traditional mergesort when the input array is randomly ordered. If the input array is nearly sorted, the implementation requires approximately n comparisons. Temporary storage requirements vary from a small constant for nearly sorted input arrays to n/2 object references for randomly ordered input arrays.

The implementation takes equal advantage of ascending and descending order in its input array, and can take advantage of ascending and descending order in different parts of the same input array. It is well-suited to merging two or more sorted arrays: simply concatenate the arrays and sort the resulting array.

The implementation was adapted from Tim Peters's list sort for Python ([TimSort](http://svn.python.org/projects/python/trunk/Objects/listsort.txt)). It uses techniques from Peter McIlroy's "Optimistic Sorting and Information Theoretic Complexity", in Proceedings of the Fourth Annual ACM-SIAM Symposium on Discrete Algorithms, pp 467-474, January 1993.

| Parameters ||
|---|---|
| `<T>` | the class of the objects to be sorted |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be sorted |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first element (inclusive) to be sorted |
| --- | --- |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the last element (exclusive) to be sorted |
| `c` | [Comparator](Comparator.md)\<in T\>?: the comparator to determine the order of the array. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used. |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `fromIndex < 0` or `toIndex > a.length` |
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* using the specified comparator. |
| `java.lang.IllegalArgumentException` | if `fromIndex > toIndex` or (optional) if the comparator is found to violate the Comparator contract |
| --- | --- |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> sort(
    a: Array<T>, 
    c: Comparator<in T>?
): Unit
```

Sorts the specified array of objects according to the order induced by the specified comparator. All elements in the array must be *mutually comparable* by the specified comparator (that is, `c.compare(e1, e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the array).

This sort is guaranteed to be *stable*: equal elements will not be reordered as a result of the sort.

Implementation note: This implementation is a stable, adaptive, iterative mergesort that requires far fewer than n lg(n) comparisons when the input array is partially sorted, while offering the performance of a traditional mergesort when the input array is randomly ordered. If the input array is nearly sorted, the implementation requires approximately n comparisons. Temporary storage requirements vary from a small constant for nearly sorted input arrays to n/2 object references for randomly ordered input arrays.

The implementation takes equal advantage of ascending and descending order in its input array, and can take advantage of ascending and descending order in different parts of the same input array. It is well-suited to merging two or more sorted arrays: simply concatenate the arrays and sort the resulting array.

The implementation was adapted from Tim Peters's list sort for Python ([TimSort](http://svn.python.org/projects/python/trunk/Objects/listsort.txt)). It uses techniques from Peter McIlroy's "Optimistic Sorting and Information Theoretic Complexity", in Proceedings of the Fourth Annual ACM-SIAM Symposium on Discrete Algorithms, pp 467-474, January 1993.

| Parameters ||
|---|---|
| `<T>` | the class of the objects to be sorted |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array to be sorted |
| `c` | [Comparator](Comparator.md)\<in T\>?: the comparator to determine the order of the array. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the array contains elements that are not *mutually comparable* using the specified comparator |
| `java.lang.IllegalArgumentException` | (optional) if the comparator is found to violate the Comparator contract |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun spliterator(array: DoubleArray): Spliterator.OfDouble
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble` covering all of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array, assumed to be unmodified during use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble` | a spliterator for the array elements |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun spliterator(
    array: DoubleArray, 
    startInclusive: Int, 
    endExclusive: Int
): Spliterator.OfDouble
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble` covering the specified range of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfDouble` | a spliterator for the array elements |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun spliterator(array: IntArray): Spliterator.OfInt
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt` covering all of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array, assumed to be unmodified during use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt` | a spliterator for the array elements |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun spliterator(
    array: IntArray, 
    startInclusive: Int, 
    endExclusive: Int
): Spliterator.OfInt
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt` covering the specified range of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfInt` | a spliterator for the array elements |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun spliterator(array: LongArray): Spliterator.OfLong
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong` covering all of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array, assumed to be unmodified during use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong` | the spliterator for the array elements |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun spliterator(
    array: LongArray, 
    startInclusive: Int, 
    endExclusive: Int
): Spliterator.OfLong
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong` covering the specified range of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.OfLong` | a spliterator for the array elements |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> spliterator(array: Array<T>): Spliterator<T>
```

Returns a Spliterator covering all of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `<T>` | type of elements |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array, assumed to be unmodified during use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator<T>` | a spliterator for the array elements |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> spliterator(
    array: Array<T>, 
    startInclusive: Int, 
    endExclusive: Int
): Spliterator<T>
```

Returns a Spliterator covering the specified range of the specified array.

The spliterator reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#SUBSIZED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator#IMMUTABLE:kotlin.Int`.

| Parameters ||
|---|---|
| `<T>` | type of elements |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| --- | --- |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator<T>` | a spliterator for the array elements |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stream(array: DoubleArray): DoubleStream
```

Returns a sequential DoubleStream with the specified array as its source.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array, assumed to be unmodified during use |

| Return ||
|---|---|
| DoubleStream | a `DoubleStream` for the array |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stream(
    array: DoubleArray, 
    startInclusive: Int, 
    endExclusive: Int
): DoubleStream
```

Returns a sequential DoubleStream with the specified range of the specified array as its source.

| Parameters ||
|---|---|
| `array` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html): the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |
| --- | --- |

| Return ||
|---|---|
| DoubleStream | a `DoubleStream` for the array range |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stream(array: IntArray): IntStream
```

Returns a sequential IntStream with the specified array as its source.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array, assumed to be unmodified during use |

| Return ||
|---|---|
| IntStream | an `IntStream` for the array |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stream(
    array: IntArray, 
    startInclusive: Int, 
    endExclusive: Int
): IntStream
```

Returns a sequential IntStream with the specified range of the specified array as its source.

| Parameters ||
|---|---|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html): the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |
| --- | --- |

| Return ||
|---|---|
| IntStream | an `IntStream` for the array range |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stream(array: LongArray): LongStream
```

Returns a sequential LongStream with the specified array as its source.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array, assumed to be unmodified during use |

| Return ||
|---|---|
| LongStream | a `LongStream` for the array |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun stream(
    array: LongArray, 
    startInclusive: Int, 
    endExclusive: Int
): LongStream
```

Returns a sequential LongStream with the specified range of the specified array as its source.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html): the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |
| --- | --- |

| Return ||
|---|---|
| LongStream | a `LongStream` for the array range |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> stream(array: Array<T>): Stream<T>
```

Returns a sequential Stream with the specified array as its source.

| Parameters ||
|---|---|
| `<T>` | The type of the array elements |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: The array, assumed to be unmodified during use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream<T>` | a `Stream` for the array |

### stream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun <T : Any!> stream(
    array: Array<T>, 
    startInclusive: Int, 
    endExclusive: Int
): Stream<T>
```

Returns a sequential Stream with the specified range of the specified array as its source.

| Parameters ||
|---|---|
| `<T>` | the type of the array elements |
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array, assumed to be unmodified during use |
| `startInclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the first index to cover, inclusive |
| --- | --- |
| `endExclusive` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index immediately past the last index to cover |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream<T>` | a `Stream` for the array range |

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if `startInclusive` is negative, `endExclusive` is less than `startInclusive`, or `endExclusive` is greater than the array size |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: BooleanArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(boolean)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: ByteArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(byte)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: CharArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(char)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: DoubleArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(double)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: FloatArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(float)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: IntArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(int)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: Array<Any!>?): String
```

Returns a string representation of the contents of the specified array. If the array contains other arrays as elements, they are converted to strings by the toString method inherited from `Object`, which describes their *identities* rather than their contents.

The value returned by this method is equal to the value that would be returned by `Arrays.asList(a).toString()`, unless `a` is `null`, in which case `"null"` is returned.

| Parameters ||
|---|---|
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

**See Also**

- deepToString

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: LongArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(long)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(a: ShortArray?): String
```

Returns a string representation of the contents of the specified array. The string representation consists of a list of the array's elements, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (a comma followed by a space). Elements are converted to strings as by `String.valueOf(short)`. Returns `"null"` if `a` is `null`.

| Parameters ||
|---|---|
| `a` | [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)?: the array whose string representation to return |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of `a` |

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollationKey

```
class CollationKey : Comparable<CollationKey!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#) |

A `CollationKey` represents a `String` under the rules of a specific `Collator` object. Comparing two `CollationKey`s returns the relative order of the `String`s they represent.

Since the rule set of `Collator`s can differ, the sort orders of the same string under two different `Collator`s might differ. Hence comparing `CollationKey`s generated from different `Collator`s can give incorrect results.

Both the method `CollationKey.compareTo(CollationKey)` and the method `Collator.compare(String, String)` compare two strings and returns their relative order. The performance characteristics of these two approaches can differ. Note that collation keys are often less efficient than simply doing comparison. For more details, see the ICU User Guide.

During the construction of a `CollationKey`, the entire source string is examined and processed into a series of bits terminated by a null, that are stored in the `CollationKey`. When `CollationKey.compareTo(CollationKey)` executes, it performs bitwise comparison on the bit sequences. This can incurs startup cost when creating the `CollationKey`, but once the key is created, binary comparisons are fast. This approach is recommended when the same strings are to be compared over and over again.

On the other hand, implementations of `Collator.compare(String, String)` can examine and process the strings only until the first characters differing in order. This approach is recommended if the strings are to be compared only once.

More information about the composition of the bit sequence can be found in the [user guide](https://unicode-org.github.io/icu/userguide/collation/architecture).

The following example shows how `CollationKey`s can be used to sort a list of `String`s.

```kotlin
// Create an array of CollationKeys for the Strings to be sorted.
  Collator myCollator = Collator.getInstance();
  CollationKey[] keys = new CollationKey[3];
  keys[0] = myCollator.getCollationKey("Tom");
  keys[1] = myCollator.getCollationKey("Dick");
  keys[2] = myCollator.getCollationKey("Harry");
  sort( keys );
  <br>//...
  <br>// Inside body of sort routine, compare keys this way
  if( keys[i].compareTo( keys[j] ) > 0 )
     // swap keys[i] and keys[j]
  <br>//...
  <br>// Finally, when we've returned from sort.
  System.out.println( keys[0].getSourceString() );
  System.out.println( keys[1].getSourceString() );
  System.out.println( keys[2].getSourceString() );
  
```

This class is not subclassable

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey.BoundMode` Options that used in the API CollationKey. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#CollationKey(kotlin.String,%20kotlin.ByteArray)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` CollationKey constructor. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#compareTo(android.icu.text.CollationKey)(other: https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#!)` Compare this CollationKey to another CollationKey. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#equals(android.icu.text.CollationKey)(target: https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#!)` Compare this CollationKey and the argument target CollationKey for equality. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compare this CollationKey and the specified Object for equality. |
| [CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#)! | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#getBound(kotlin.Int,%20kotlin.Int)(boundType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, noOfLevels: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Produces a bound for the sort order of a given collation key and a strength level. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#getSourceString()()` Return the source string that this CollationKey represents. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#hashCode()()` Returns a hash code for this CollationKey. |
| [CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#)! | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#merge(android.icu.text.CollationKey)(source: https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#!)` Merges this CollationKey with another. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#toByteArray()()` Duplicates and returns the value of this CollationKey as a sequence of big-endian bytes terminated by a null. |

## Public constructors

### CollationKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CollationKey(
    source: String!, 
    key: ByteArray!)
```

CollationKey constructor. This constructor is given public access, unlike the JDK version, to allow access to users extending the Collator class. See `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getCollationKey(kotlin.String)`.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: string this CollationKey is to represent |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: array of bytes that represent the collation order of argument source terminated by a null |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Collator`

## Public methods

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: CollationKey!): Int
```

Compare this CollationKey to another CollationKey. The collation rules of the Collator that created this key are applied.

**Note:** Comparison between CollationKeys created by different Collators might return incorrect results. See class documentation.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `target` | target CollationKey |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an integer value. If the value is less than zero this CollationKey is less than than target, if the value is zero they are equal, and if the value is greater than zero this CollationKey is greater than target. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | is thrown if argument is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#compare(kotlin.String,%20kotlin.String)`

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(target: CollationKey!): Boolean
```

Compare this CollationKey and the argument target CollationKey for equality. The collation rules of the Collator object which created these objects are applied.

See note in compareTo(CollationKey) for warnings of incorrect results

| Parameters ||
|---|---|
| `target` | [CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#)!: the CollationKey to compare to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if two objects are equal, false otherwise. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | is thrown when the argument is null. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compare this CollationKey and the specified Object for equality. The collation rules of the Collator that created this key are applied.

See note in compareTo(CollationKey) for warnings about possible incorrect results.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `target` | the object to compare to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the two keys compare as equal, false otherwise. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | is thrown when the argument is not a CollationKey. NullPointerException is thrown when the argument is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#compareTo(android.icu.text.CollationKey)`

### getBound

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBound(
    boundType: Int, 
    noOfLevels: Int
): CollationKey!
```

Produces a bound for the sort order of a given collation key and a strength level. This API does not attempt to find a bound for the CollationKey String representation, hence null will be returned in its place.

Resulting bounds can be used to produce a range of strings that are between upper and lower bounds. For example, if bounds are produced for a sortkey of string "smith", strings between upper and lower bounds with primary strength would include "Smith", "SMITH", "sMiTh".

There are two upper bounds that can be produced. If BoundMode.UPPER is produced, strings matched would be as above. However, if a bound is produced using BoundMode.UPPER_LONG is used, the above example will also match "Smithsonian" and similar.

For more on usage, see example in test procedure [src/com/ibm/icu/dev/test/collator/CollationAPITest/TestBounds.](https://github.com/unicode-org/icu/blob/main/icu4j/main/collate/src/test/java/com/ibm/icu/dev/test/collator/CollationAPITest.java)

Collation keys produced may be compared using the `compare` API.

| Parameters ||
|---|---|
| `boundType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Mode of bound required. It can be BoundMode.LOWER, which produces a lower inclusive bound, BoundMode.UPPER, that produces upper bound that matches strings of the same length or BoundMode.UPPER_LONG that matches strings that have the same starting substring as the source string. |
| `noOfLevels` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Strength levels required in the resulting bound (for most uses, the recommended value is PRIMARY). This strength should be less than the maximum strength of this CollationKey. See users guide for explanation on the strength levels a collation key can have. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#!` | the result bounded CollationKey with a valid sort order but a null String representation. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | thrown when the strength level requested is higher than or equal to the strength in this CollationKey. In the case of an Exception, information about the maximum strength to use will be returned in the Exception. The user can then call getBound() again with the appropriate strength. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#`
- `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey.BoundMode`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int`

### getSourceString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSourceString(): String!
```

Return the source string that this CollationKey represents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | source string that this CollationKey represents |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this CollationKey. The hash value is calculated on the key itself, not the String from which the key was created. Thus if x and y are CollationKeys, then x.hashCode(x) == y.hashCode() if x.equals(y) is true. This allows language-sensitive comparison in a hash table.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash value. |

### merge

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun merge(source: CollationKey!): CollationKey!
```

Merges this CollationKey with another. The levels are merged with their corresponding counterparts (primaries with primaries, secondaries with secondaries etc.). Between the values from the same level a separator is inserted.

This is useful, for example, for combining sort keys from first and last names to sort such pairs. See http://www.unicode.org/reports/tr10/#Merging_Sort_Keys

The recommended way to achieve "merged" sorting is by concatenating strings with U+FFFE between them. The concatenation has the same sort order as the merged sort keys, but merge(getSortKey(str1), getSortKey(str2)) may differ from getSortKey(str1 + '\\uFFFE' + str2). Using strings with U+FFFE may yield shorter sort keys.

For details about Sort Key Features see https://unicode-org.github.io/icu/userguide/collation/api#sort-key-features

It is possible to merge multiple sort keys by consecutively merging another one with the intermediate result.

Only the sort key bytes of the CollationKeys are merged. This API does not attempt to merge the String representations of the CollationKeys, hence null will be returned as the result's String representation.

Example (uncompressed):

```kotlin
191B1D 01 050505 01 910505 00
  1F2123 01 050505 01 910505 00
```
will be merged as

```kotlin
191B1D 02 1F2123 01 050505 02 050505 01 910505 02 910505 00
```

| Parameters ||
|---|---|
| `source` | [CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#)!: CollationKey to merge with |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey#!` | a CollationKey that contains the valid merged sort keys with a null String representation, i.e. `new CollationKey(null, merged_sort_keys)` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | thrown if source CollationKey argument is null or of 0 length. |

### toByteArray

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toByteArray(): ByteArray!
```

Duplicates and returns the value of this CollationKey as a sequence of big-endian bytes terminated by a null.

If two CollationKeys can be legitimately compared, then one can compare the byte arrays of each to obtain the same result, e.g.

```kotlin
byte key1[] = collationkey1.toByteArray();
  byte key2[] = collationkey2.toByteArray();
  int key, targetkey;
  int i = 0;
  do {
        key = key1[i] & 0xFF;
      targetkey = key2[i] & 0xFF;
      if (key < targetkey) {
          System.out.println("String 1 is less than string 2");
          return;
      }
      if (targetkey < key) {
          System.out.println("String 1 is more than string 2");
      }
      i ++;
  } while (key != 0 && targetKey != 0);
 
  System.out.println("Strings are equal.");
  
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | CollationKey value in a sequence of big-endian byte bytes terminated by a null. |

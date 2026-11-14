# Edits

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Edits

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/Edits "View this page in Java") 

```
class Edits
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#) |

Records lengths of string edits but not replacement text. Supports replacements, insertions, deletions in linear progression. Does not support moving/reordering of text.

There are two types of edits:*change edits* and*no-change edits* . Add edits to instances of this class using [addReplace(int,int)](https://developer.android.com/reference/kotlin/android/icu/text/Edits#addReplace(kotlin.Int,%20kotlin.Int))(for change edits) and [addUnchanged(int)](https://developer.android.com/reference/kotlin/android/icu/text/Edits#addUnchanged(kotlin.Int))(for no-change edits). Change edits are retained with full granularity, whereas adjacent no-change edits are always merged together. In no-change edits, there is a one-to-one mapping between code points in the source and destination strings.

After all edits have been added, instances of this class should be considered immutable, and an [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator) can be used for queries.

There are four flavors of Edits.Iterator:

- [getFineIterator()](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getFineIterator())retains full granularity of change edits.
- [getFineChangesIterator()](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getFineChangesIterator())retains full granularity of change edits, and when calling next() on the iterator, skips over no-change edits (unchanged regions).
- [getCoarseIterator()](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getCoarseIterator())treats adjacent change edits as a single edit. (Adjacent no-change edits are automatically merged during the construction phase.)
- [getCoarseChangesIterator()](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getCoarseChangesIterator())treats adjacent change edits as a single edit, and when calling next() on the iterator, skips over no-change edits (unchanged regions).

For example, consider the string "abcßDeF", which case-folds to "abcssdef". This string has the following fine edits:

- abc ⇨ abc (no-change)
- ß ⇨ ss (change)
- D ⇨ d (change)
- e ⇨ e (no-change)
- F ⇨ f (change)

and the following coarse edits (note how adjacent change edits get merged together):

<!-- -->

- abc ⇨ abc (no-change)
- ßD ⇨ ssd (change)
- e ⇨ e (no-change)
- F ⇨ f (change)

The "fine changes" and "coarse changes" iterators will step through only the change edits when their [Edits.Iterator.next()](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator#next())methods are called. They are identical to the non-change iterators when their [Edits.Iterator.findSourceIndex(int)](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator#findSourceIndex(kotlin.Int))or [Edits.Iterator.findDestinationIndex(int)](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator#findDestinationIndex(kotlin.Int))methods are used to walk through the string.

For examples of how to use this class, see the test`TestCaseMapEditsIteratorDocs`in UCharacterCaseTest.java.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator) Access to the list of edits. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------|---|
| [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#Edits())`()` Constructs an empty object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addReplace](https://developer.android.com/reference/kotlin/android/icu/text/Edits#addReplace(kotlin.Int,%20kotlin.Int))`(`oldLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a change edit: a record for a text replacement/insertion/deletion. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addUnchanged](https://developer.android.com/reference/kotlin/android/icu/text/Edits#addUnchanged(kotlin.Int))`(`unchangedLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adds a no-change edit: a record for an unchanged segment of text. |
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | [getCoarseChangesIterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getCoarseChangesIterator())`()` Returns an Iterator for coarse-grained change edits (adjacent change edits are treated as one). |
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | [getCoarseIterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getCoarseIterator())`()` Returns an Iterator for coarse-grained change and no-change edits (adjacent change edits are treated as one). |
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | [getFineChangesIterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getFineChangesIterator())`()` Returns an Iterator for fine-grained change edits (full granularity of change edits is retained). |
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | [getFineIterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits#getFineIterator())`()` Returns an Iterator for fine-grained change and no-change edits (full granularity of change edits is retained). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasChanges](https://developer.android.com/reference/kotlin/android/icu/text/Edits#hasChanges())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lengthDelta](https://developer.android.com/reference/kotlin/android/icu/text/Edits#lengthDelta())`()` How much longer is the new text compared with the old text? |
| [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#)! | [mergeAndAppend](https://developer.android.com/reference/kotlin/android/icu/text/Edits#mergeAndAppend(android.icu.text.Edits,%20android.icu.text.Edits))`(`ab:` ` [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#)!`, `bc:` ` [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#)!`)` Merges the two input Edits and appends the result to this object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [numberOfChanges](https://developer.android.com/reference/kotlin/android/icu/text/Edits#numberOfChanges())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/android/icu/text/Edits#reset())`()` Resets the data but may not release memory. |

## Public constructors

### Edits

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Edits()
```

Constructs an empty object.

## Public methods

### addReplace

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addReplace(
    oldLength: Int, 
    newLength: Int
): Unit
```

Adds a change edit: a record for a text replacement/insertion/deletion. Normally called from inside ICU string transformation functions, not user code. 

### addUnchanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addUnchanged(unchangedLength: Int): Unit
```

Adds a no-change edit: a record for an unchanged segment of text. Normally called from inside ICU string transformation functions, not user code. 

### getCoarseChangesIterator

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCoarseChangesIterator(): Edits.Iterator!
```

Returns an Iterator for coarse-grained change edits (adjacent change edits are treated as one). Can be used to perform simple string updates. Skips no-change edits.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | an Iterator that merges adjacent changes. |

### getCoarseIterator

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCoarseIterator(): Edits.Iterator!
```

Returns an Iterator for coarse-grained change and no-change edits (adjacent change edits are treated as one). Can be used to perform simple string updates. Adjacent change edits are treated as one edit.

| Return ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | an Iterator that merges adjacent changes. |

### getFineChangesIterator

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFineChangesIterator(): Edits.Iterator!
```

Returns an Iterator for fine-grained change edits (full granularity of change edits is retained). Can be used for modifying styled text. Skips no-change edits.

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | an Iterator that separates adjacent changes. |

### getFineIterator

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFineIterator(): Edits.Iterator!
```

Returns an Iterator for fine-grained change and no-change edits (full granularity of change edits is retained). Can be used for modifying styled text.

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Edits.Iterator](https://developer.android.com/reference/kotlin/android/icu/text/Edits.Iterator)! | an Iterator that separates adjacent changes. |

### hasChanges

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasChanges(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if there are any change edits |

### lengthDelta

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lengthDelta(): Int
```

How much longer is the new text compared with the old text?

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | new length minus old length |

### mergeAndAppend

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun mergeAndAppend(
    ab: Edits!, 
    bc: Edits!
): Edits!
```

Merges the two input Edits and appends the result to this object.

Consider two string transformations (for example, normalization and case mapping) where each records Edits in addition to writing an output string. 
Edits ab reflect how substrings of input string a map to substrings of intermediate string b. 
Edits bc reflect how substrings of intermediate string b map to substrings of output string c. 
This function merges ab and bc such that the additional edits recorded in this object reflect how substrings of input string a map to substrings of output string c.

If unrelated Edits are passed in where the output string of the first has a different length than the input string of the second, then an IllegalArgumentException is thrown.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ab` | [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#)!:reflects how substrings of input string a map to substrings of intermediate string b. |
| `bc` | [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#)!:reflects how substrings of intermediate string b map to substrings of output string c. |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------|
| [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits#)! | this, with the merged edits appended |

### numberOfChanges

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun numberOfChanges(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of change edits |

### reset

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Unit
```

Resets the data but may not release memory.

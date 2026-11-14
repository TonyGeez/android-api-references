# AlphabetIndexer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlphabetIndexer

Kotlin| [Java](https://developer.android.com/reference/android/widget/AlphabetIndexer "View this page in Java") 
| --- | --- |

```
open class AlphabetIndexer : DataSetObserver, SectionIndexer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.database.DataSetObserver](https://developer.android.com/reference/kotlin/android/database/DataSetObserver.html#) ||
| | ↳ | [android.widget.AlphabetIndexer](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#) |

A helper class for adapters that implement the SectionIndexer interface. If the items in the adapter are sorted by simple alphabet-based sorting, then this class provides a way to do fast indexing of large lists using binary search. It caches the indices that have been determined through the binary search and also invalidates the cache if changes occur in the cursor.

<br />

Your adapter is responsible for updating the cursor by calling [setCursor](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#setCursor(android.database.Cursor))if the cursor changes. [getPositionForSection](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#getPositionForSection(kotlin.Int))method does the binary search for the starting index of a given section (alphabet).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlphabetIndexer](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#AlphabetIndexer(android.database.Cursor,%20kotlin.Int,%20kotlin.CharSequence))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`, `sortedColumnIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alphabet:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Constructs the indexer. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPositionForSection](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#getPositionForSection(kotlin.Int))`(`sectionIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs a binary search or cache lookup to find the first row that matches a given section's starting letter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSectionForPosition](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#getSectionForPosition(kotlin.Int))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the section index for a given position in the list by querying the item and comparing it with all items in the section array. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getSections](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#getSections())`()` Returns the section array constructed from the alphabet provided in the constructor. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onChanged](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#onChanged())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvalidated](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#onInvalidated())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCursor](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#setCursor(android.database.Cursor))`(`cursor:` ` [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!`)` Sets a new cursor as the data set and resets the cache of indices. |
| --- | --- |

| Protected methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#compare(kotlin.String,%20kotlin.String))`(`word:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `letter:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Default implementation compares the first character of word with letter. |

| Properties ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [mAlphabet](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#mAlphabet:kotlin.CharSequence) The string of characters that make up the indexing sections. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [mColumnIndex](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#mColumnIndex:kotlin.Int) The index of the cursor column that this list is sorted on. |
| [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)! | [mDataCursor](https://developer.android.com/reference/kotlin/android/widget/AlphabetIndexer#mDataCursor:android.database.Cursor) Cursor that is used by the adapter of the list view. |
| --- | --- |

## Public constructors

### AlphabetIndexer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AlphabetIndexer(
    cursor: Cursor!, 
    sortedColumnIndex: Int, 
    alphabet: CharSequence!)
```

Constructs the indexer.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:the cursor containing the data set |
| `sortedColumnIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the column number in the cursor that is sorted alphabetically |
| `alphabet` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:string containing the alphabet, with space as the first character. For example, use the string " ABCDEFGHIJKLMNOPQRSTUVWXYZ" for English indexing. The characters must be uppercase and be sorted in ascii/unicode order. Basically characters in the alphabet will show up as preview letters. |
| --- | --- |

## Public methods

### getPositionForSection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositionForSection(sectionIndex: Int): Int
```

Performs a binary search or cache lookup to find the first row that matches a given section's starting letter.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------|
| `sectionIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the section to search for |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the row index of the first occurrence, or the nearest next letter. For instance, if searching for "T" and no "T" is found, then the first row starting with "U" or any higher letter is returned. If there is no data following "T" at all, then the list size is returned. |

### getSectionForPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSectionForPosition(position: Int): Int
```

Returns the section index for a given position in the list by querying the item and comparing it with all items in the section array.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the adapter for which to return the corresponding section index |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the corresponding section within the array of section objects, constrained to fall within the array bounds |

### getSections

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSections(): Array<Any!>!
```

Returns the section array constructed from the alphabet provided in the constructor.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | the section array |

### onChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onChanged(): Unit
```  

### onInvalidated

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInvalidated(): Unit
```  

### setCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCursor(cursor: Cursor!): Unit
```

Sets a new cursor as the data set and resets the cache of indices.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `cursor` | [Cursor](https://developer.android.com/reference/kotlin/android/database/Cursor.html#)!:the new cursor to use as the data set |

## Protected methods

### compare

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun compare(
    word: String!, 
    letter: String!
): Int
```

Default implementation compares the first character of word with letter.

## Properties

### mAlphabet

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mAlphabet: CharSequence!
```

The string of characters that make up the indexing sections. 

### mColumnIndex

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mColumnIndex: Int
```

The index of the cursor column that this list is sorted on. 

### mDataCursor

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mDataCursor: Cursor!
```

Cursor that is used by the adapter of the list view.

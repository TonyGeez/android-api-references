# SectionIndexer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SectionIndexer

Kotlin| [Java](SectionIndexer.md) 
| --- | --- |

```
interface SectionIndexer
```

| [android.widget.SectionIndexer](SectionIndexer.md) |

| Known Direct Subclasses [AlphabetIndexer](AlphabetIndexer.md) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [AlphabetIndexer](AlphabetIndexer.md) | A helper class for adapters that implement the SectionIndexer interface. | |
| --- | --- | --- | --- | --- | --- | --- |

Interface that may implemented on [Adapter](Adapter.md) s to enable fast scrolling between sections of an [AbsListView](AbsListView.md).

A section is a group of list items that have something in common. For example, they may begin with the same letter or they may be songs from the same artist.

[ExpandableListAdapter](ExpandableListAdapter.md) s that consider groups and sections as synonymous should account for collapsed groups and return an appropriate section/position.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPositionForSection](SectionIndexer.md))`(`sectionIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Given the index of a section within the array of section objects, returns the starting position of that section within the adapter. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSectionForPosition](SectionIndexer.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Given a position within the adapter, returns the index of the corresponding section within the array of section objects. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getSections](SectionIndexer.md))`()` Returns an array of objects representing sections of the list. |
| --- | --- |

## Public methods

### getPositionForSection

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPositionForSection(sectionIndex: Int): Int
```

Given the index of a section within the array of section objects, returns the starting position of that section within the adapter.

If the section's starting position is outside of the adapter bounds, the position must be clipped to fall within the size of the adapter.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `sectionIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the section within the array of section objects |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the starting position of that section within the adapter, constrained to fall within the adapter bounds |

### getSectionForPosition

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSectionForPosition(position: Int): Int
```

Given a position within the adapter, returns the index of the corresponding section within the array of section objects.

If the section index is outside of the section array bounds, the index must be clipped to fall within the size of the section array.

For example, consider an indexer where the section at array index 0 starts at adapter position 100. Calling this method with position 10, which is before the first section, must return index 0.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position within the adapter for which to return the corresponding section index |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the corresponding section within the array of section objects, constrained to fall within the array bounds |

### getSections

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSections(): Array<Any!>!
```

Returns an array of objects representing sections of the list. The returned array and its contents should be non-null.

The list view will call toString() on the objects to get the preview text to display while scrolling. For example, an adapter may return an array of Strings representing letters of the alphabet. Or, it may return an array of objects whose toString() methods return their section titles.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | the array of section objects |

# Bidi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Bidi

```
class Bidi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.text.Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi#) |

This class implements the Unicode Bidirectional Algorithm.

A Bidi object provides information on the bidirectional reordering of the text used to create it. This is required, for example, to properly display Arabic or Hebrew text. These languages are inherently mixed directional, as they order numbers from left-to-right while ordering most other text from right-to-left.

Once created, a Bidi object can be queried to see if the text it represents is all left-to-right or all right-to-left. Such objects are very lightweight and this text is relatively easy to process.

If there are multiple runs of text, information about the runs can be accessed by indexing to get the start, limit, and level of a run. The level represents both the direction and the 'nesting level' of a directional run. Odd levels are right-to-left, while even levels are left-to-right. So for example level 0 represents left-to-right text, while level 1 represents right-to-left text, and level 2 represents left-to-right text embedded in a right-to-left run.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_DEFAULT_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/java/text/Bidi#DIRECTION_DEFAULT_LEFT_TO_RIGHT:kotlin.Int) Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_DEFAULT_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/java/text/Bidi#DIRECTION_DEFAULT_RIGHT_TO_LEFT:kotlin.Int) Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/java/text/Bidi#DIRECTION_LEFT_TO_RIGHT:kotlin.Int) Constant indicating base direction is left-to-right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/java/text/Bidi#DIRECTION_RIGHT_TO_LEFT:kotlin.Int) Constant indicating base direction is right-to-left. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi#Bidi(kotlin.CharArray,%20kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `textStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `embeddings:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `embStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paragraphLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create Bidi from the given text, embedding, and direction information. |
| [Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi#Bidi(kotlin.String,%20kotlin.Int))`(`paragraph:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create Bidi from the given paragraph of text and base direction. |
| [Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi#Bidi(java.text.AttributedCharacterIterator))`(`paragraph:` ` [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!`)` Create Bidi from the given paragraph of text. |

| Public methods ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [baseIsLeftToRight](https://developer.android.com/reference/kotlin/java/text/Bidi#baseIsLeftToRight())`()` Return true if the base direction is left-to-right. |
| [Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi#)! | [createLineBidi](https://developer.android.com/reference/kotlin/java/text/Bidi#createLineBidi(kotlin.Int,%20kotlin.Int))`(`lineStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lineLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a Bidi object representing the bidi information on a line of text within the paragraph represented by the current Bidi. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBaseLevel](https://developer.android.com/reference/kotlin/java/text/Bidi#getBaseLevel())`()` Return the base level (0 if left-to-right, 1 if right-to-left). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/java/text/Bidi#getLength())`()` Return the length of text in the line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevelAt](https://developer.android.com/reference/kotlin/java/text/Bidi#getLevelAt(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the resolved level of the character at offset. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunCount](https://developer.android.com/reference/kotlin/java/text/Bidi#getRunCount())`()` Return the number of level runs. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLevel](https://developer.android.com/reference/kotlin/java/text/Bidi#getRunLevel(kotlin.Int))`(`run:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the level of the nth logical run in this line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLimit](https://developer.android.com/reference/kotlin/java/text/Bidi#getRunLimit(kotlin.Int))`(`run:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the index of the character past the end of the nth logical run in this line, as an offset from the start of the line. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunStart](https://developer.android.com/reference/kotlin/java/text/Bidi#getRunStart(kotlin.Int))`(`run:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the index of the character at the start of the nth logical run in this line, as an offset from the start of the line. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeftToRight](https://developer.android.com/reference/kotlin/java/text/Bidi#isLeftToRight())`()` Return true if the line is all left-to-right text and the base direction is left-to-right. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMixed](https://developer.android.com/reference/kotlin/java/text/Bidi#isMixed())`()` Return true if the line is not left-to-right or right-to-left. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRightToLeft](https://developer.android.com/reference/kotlin/java/text/Bidi#isRightToLeft())`()` Return true if the line is all right-to-left text, and the base direction is right-to-left. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reorderVisually](https://developer.android.com/reference/kotlin/java/text/Bidi#reorderVisually(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`levels:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `levelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `objectStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reorder the objects in the array into visual order based on their levels. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresBidi](https://developer.android.com/reference/kotlin/java/text/Bidi#requiresBidi(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the specified text requires bidi analysis. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/text/Bidi#toString())`()` Display the bidi internal state, used in debugging. |

## Constants

### DIRECTION_DEFAULT_LEFT_TO_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_DEFAULT_LEFT_TO_RIGHT: Int
```

Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. If no strong directional character is present, the base direction is left-to-right. 

 Value: -2

### DIRECTION_DEFAULT_RIGHT_TO_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_DEFAULT_RIGHT_TO_LEFT: Int
```

Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. If no strong directional character is present, the base direction is right-to-left. 

 Value: -1

### DIRECTION_LEFT_TO_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_LEFT_TO_RIGHT: Int
```

Constant indicating base direction is left-to-right. 

 Value: 0

### DIRECTION_RIGHT_TO_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_RIGHT_TO_LEFT: Int
```

Constant indicating base direction is right-to-left. 

 Value: 1

## Public constructors

### Bidi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi(
    text: CharArray!, 
    textStart: Int, 
    embeddings: ByteArray!, 
    embStart: Int, 
    paragraphLength: Int, 
    flags: Int)
```

Create Bidi from the given text, embedding, and direction information. The embeddings array may be null. If present, the values represent embedding level information. Negative values from -1 to -61 indicate overrides at the absolute value of the level. Positive values from 1 to 61 indicate embeddings. Where values are zero, the base embedding level as determined by the base direction is assumed.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array containing the paragraph of text to process. |
| `textStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the text array of the start of the paragraph. |
| `embeddings` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:an array containing embedding values for each character in the paragraph. This can be null, in which case it is assumed that there is no external embedding information. |
| `embStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the embedding array of the start of the paragraph. |
| `paragraphLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the paragraph in the text and embeddings arrays. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a collection of flags that control the algorithm. The algorithm understands the flags DIRECTION_LEFT_TO_RIGHT, DIRECTION_RIGHT_TO_LEFT, DIRECTION_DEFAULT_LEFT_TO_RIGHT, and DIRECTION_DEFAULT_RIGHT_TO_LEFT. Other values are reserved. |

### Bidi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi(
    paragraph: String!, 
    flags: Int)
```

Create Bidi from the given paragraph of text and base direction.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paragraph` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a paragraph of text |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a collection of flags that control the algorithm. The algorithm understands the flags DIRECTION_LEFT_TO_RIGHT, DIRECTION_RIGHT_TO_LEFT, DIRECTION_DEFAULT_LEFT_TO_RIGHT, and DIRECTION_DEFAULT_RIGHT_TO_LEFT. Other values are reserved. |

### Bidi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi(paragraph: AttributedCharacterIterator!)
```

Create Bidi from the given paragraph of text.

The RUN_DIRECTION attribute in the text, if present, determines the base direction (left-to-right or right-to-left). If not present, the base direction is computes using the Unicode Bidirectional Algorithm, defaulting to left-to-right if there are no strong directional characters in the text. This attribute, if present, must be applied to all the text in the paragraph.

The BIDI_EMBEDDING attribute in the text, if present, represents embedding level information. Negative values from -1 to -62 indicate overrides at the absolute value of the level. Positive values from 1 to 62 indicate embeddings. Where values are zero or not defined, the base embedding level as determined by the base direction is assumed.

The NUMERIC_SHAPING attribute in the text, if present, converts European digits to other decimal digits before running the bidi algorithm. This attribute, if present, must be applied to all the text in the paragraph.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paragraph` | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)!:a paragraph of text with optional character and paragraph attribute information |

**See Also**

- [java.awt.font.TextAttribute#BIDI_EMBEDDING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute.html#BIDI_EMBEDDING:java.awt.font.TextAttribute)
- [java.awt.font.TextAttribute#NUMERIC_SHAPING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute.html#NUMERIC_SHAPING:java.awt.font.TextAttribute)
- [java.awt.font.TextAttribute#RUN_DIRECTION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute.html#RUN_DIRECTION:java.awt.font.TextAttribute)

## Public methods

### baseIsLeftToRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun baseIsLeftToRight(): Boolean
```

Return true if the base direction is left-to-right.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the base direction is left-to-right |

### createLineBidi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createLineBidi(
    lineStart: Int, 
    lineLimit: Int
): Bidi!
```

Create a Bidi object representing the bidi information on a line of text within the paragraph represented by the current Bidi. This call is not required if the entire paragraph fits on one line.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `lineStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset from the start of the paragraph to the start of the line. |
| `lineLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset from the start of the paragraph to the limit of the line. |

| Return ||
|-------------------------------------------------------------------------|---------------|
| [Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi#)! | a`Bidi`object |

### getBaseLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBaseLevel(): Int
```

Return the base level (0 if left-to-right, 1 if right-to-left).

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the base level |

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLength(): Int
```

Return the length of text in the line.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of text in the line |

### getLevelAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLevelAt(offset: Int): Int
```

Return the resolved level of the character at offset. If offset is \< 0 or ≥ the length of the line, return the base direction level.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the character for which to return the level |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resolved level of the character at offset |

### getRunCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRunCount(): Int
```

Return the number of level runs.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of level runs |

### getRunLevel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRunLevel(run: Int): Int
```

Return the level of the nth logical run in this line.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `run` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the run, between 0 and`getRunCount()` |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the level of the run |

### getRunLimit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRunLimit(run: Int): Int
```

Return the index of the character past the end of the nth logical run in this line, as an offset from the start of the line. For example, this will return the length of the line for the last run on the line.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `run` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the run, between 0 and`getRunCount()` |

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | limit the limit of the run |

### getRunStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRunStart(run: Int): Int
```

Return the index of the character at the start of the nth logical run in this line, as an offset from the start of the line.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `run` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the run, between 0 and`getRunCount()` |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the start of the run |

### isLeftToRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLeftToRight(): Boolean
```

Return true if the line is all left-to-right text and the base direction is left-to-right.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the line is all left-to-right text and the base direction is left-to-right |

### isMixed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMixed(): Boolean
```

Return true if the line is not left-to-right or right-to-left. This means it either has mixed runs of left-to-right and right-to-left text, or the base direction differs from the direction of the only run of text.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the line is not left-to-right or right-to-left. |

### isRightToLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRightToLeft(): Boolean
```

Return true if the line is all right-to-left text, and the base direction is right-to-left.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the line is all right-to-left text, and the base direction is right-to-left |

### reorderVisually

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun reorderVisually(
    levels: ByteArray!, 
    levelStart: Int, 
    objects: Array<Any!>!, 
    objectStart: Int, 
    count: Int
): Unit
```

Reorder the objects in the array into visual order based on their levels. This is a utility function to use when you have a collection of objects representing runs of text in logical order, each run containing text at a single level. The elements at`index`from`objectStart`up to`objectStart + count`in the objects array will be reordered into visual order assuming each run of text has the level indicated by the corresponding element in the levels array (at`index - objectStart + levelStart`).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `levels` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:an array representing the bidi level of each object |
| `levelStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start position in the levels array |
| `objects` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:the array of objects to be reordered into visual order |
| `objectStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start position in the objects array |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of objects to reorder |

### requiresBidi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun requiresBidi(
    text: CharArray!, 
    start: Int, 
    limit: Int
): Boolean
```

Return true if the specified text requires bidi analysis. If this returns false, the text will display left-to-right. Clients can then avoid constructing a Bidi object. Text in the Arabic Presentation Forms area of Unicode is presumed to already be shaped and ordered for display, and so will not cause this function to return true.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the text containing the characters to test |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the range of characters to test |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit of the range of characters to test |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the range of characters requires bidi analysis |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Display the bidi internal state, used in debugging.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

# BreakIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BreakIterator

Kotlin| [Java](../android/icu/text/BreakIterator.md) 
| --- | --- |

```
abstract class BreakIterator : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.BreakIterator](../android/icu/text/BreakIterator.md) |

**\[icu enhancement\]** ICU's replacement for [java.text.BreakIterator](../java/text/BreakIterator.md). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

A class that locates boundaries in text. This class defines a protocol for objects that break up a piece of natural-language text according to a set of criteria. Instances or subclasses of BreakIterator can be provided, for example, to break a piece of text into words, sentences, or logical characters according to the conventions of some language or group of languages. We provide five built-in types of BreakIterator:

- getTitleInstance() returns a BreakIterator that locates boundaries between title breaks.
- getSentenceInstance() returns a BreakIterator that locates boundaries between sentences. This is useful for triple-click selection, for example.
- getWordInstance() returns a BreakIterator that locates boundaries between words. This is useful for double-click selection or "find whole words" searches. This type of BreakIterator makes sure there is a boundary position at the beginning and end of each legal word. (Numbers count as words, too.) Whitespace and punctuation are kept separate from real words.
- getLineInstance() returns a BreakIterator that locates positions where it is legal for a text editor to wrap lines. This is similar to word breaking, but not the same: punctuation and whitespace are generally kept with words (you don't want a line to start with whitespace, for example), and some special characters can force a position to be considered a line-break position or prevent a position from being a line-break position.
- getCharacterInstance() returns a BreakIterator that locates boundaries between logical characters. Because of the structure of the Unicode encoding, a logical character may be stored internally as more than one Unicode code point. (A with an umlaut may be stored as an a followed by a separate combining umlaut character, for example, but the user still thinks of it as one character.) This iterator allows various processes (especially text editors) to treat as characters the units of text that a user would think of as characters, rather than the units of text that the computer sees as "characters".

The text boundary positions are found according to the rules described in Unicode Standard Annex #29, Text Boundaries, and Unicode Standard Annex #14, Line Breaking Properties. These are available at http://www.unicode.org/reports/tr14/ and http://www.unicode.org/reports/tr29/.

BreakIterator's interface follows an "iterator" model (hence the name), meaning it has a concept of a "current position" and methods like first(), last(), next(), and previous() that update the current position. All BreakIterators uphold the following invariants:

- The beginning and end of the text are always treated as boundary positions.
- The current position of the iterator is always a boundary position (random- access methods move the iterator to the nearest boundary position before or after the specified position, not*to*the specified position).
- DONE is used as a flag to indicate when iteration has stopped. DONE is only returned when the current position is the end of the text and the user calls next(), or when the current position is the beginning of the text and the user calls previous().
- Break positions are numbered by the positions of the characters that follow them. Thus, under normal circumstances, the position before the first character is 0, the position after the first character is 1, and the position after the last character is 1 plus the length of the string.
- The client can change the position of an iterator, or the text it analyzes, at will, but cannot change the behavior. If the user wants different behavior, he must instantiate a new iterator.

BreakIterator accesses the text it analyzes through a CharacterIterator, which makes it possible to use BreakIterator to analyze text in any text-storage vehicle that provides a CharacterIterator interface.**Note:** Some types of BreakIterator can take a long time to create, and instances of BreakIterator are not currently cached by the system. For optimal performance, keep instances of BreakIterator around as long as makes sense. For example, when word-wrapping a document, don't create and destroy a new BreakIterator for each line. Create one break iterator for the whole document (or whatever stretch of text you're wrapping) and use it to do the whole job of wrapping the text.

**Examples**:

Creating and using text boundaries 

```kotlin
public static void main(String args[]) {
       if (args.length == 1) {
           String stringToExamine = args[0];
           //print each word in order
           BreakIterator boundary = BreakIterator.getWordInstance();
           boundary.setText(stringToExamine);
           printEachForward(boundary, stringToExamine);
           //print each sentence in reverse order
           boundary = BreakIterator.getSentenceInstance(Locale.US);
           boundary.setText(stringToExamine);
           printEachBackward(boundary, stringToExamine);
           printFirst(boundary, stringToExamine);
           printLast(boundary, stringToExamine);
       }
  }
  
```
Print each element in order 

```kotlin
public static void printEachForward(BreakIterator boundary, String source) {
      int start = boundary.first();
      for (int end = boundary.next();
           end != BreakIterator.DONE;
           start = end, end = boundary.next()) {
           System.out.println(source.substring(start,end));
      }
  }
  
```
Print each element in reverse order 

```kotlin
public static void printEachBackward(BreakIterator boundary, String source) {
      int end = boundary.last();
      for (int start = boundary.previous();
           start != BreakIterator.DONE;
           end = start, start = boundary.previous()) {
          System.out.println(source.substring(start,end));
      }
  }
  
```
Print first element 

```kotlin
public static void printFirst(BreakIterator boundary, String source) {
      int start = boundary.first();
      int end = boundary.next();
      System.out.println(source.substring(start,end));
  }
  
```
Print last element 

```kotlin
public static void printLast(BreakIterator boundary, String source) {
      int end = boundary.last();
      int start = boundary.previous();
      System.out.println(source.substring(start,end));
  }
  
```
Print the element at a specified position 

```kotlin
public static void printAt(BreakIterator boundary, int pos, String source) {
      int end = boundary.following(pos);
      int start = boundary.previous();
      System.out.println(source.substring(start,end));
  }
  
```
Find the next word 

```kotlin
public static int nextWordStartAfter(int pos, String text) {
      BreakIterator wb = BreakIterator.getWordInstance();
      wb.setText(text);
      int wordStart = wb.following(pos);
      for (;;) {
          int wordLimit = wb.next();
          if (wordLimit == BreakIterator.DONE) {
              return BreakIterator.DONE;
          }
          int wordStatus = wb.getRuleStatus();
          if (wordStatus != BreakIterator.WORD_NONE) {
              return wordStart;
          }
          wordStart = wordLimit;
       }
  }
  
```
The iterator returned by #getWordInstance is unique in that the break positions it returns don't represent both the start and end of the thing being iterated over. That is, a sentence-break iterator returns breaks that each represent the end of one sentence and the beginning of the next. With the word-break iterator, the characters between two boundaries might be a word, or they might be the punctuation or whitespace between two words. The above code uses [getRuleStatus](../android/icu/text/BreakIterator.md))to identify and ignore boundaries associated with punctuation or other non-word characters.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](../android/icu/text/BreakIterator.md) DONE is returned by previous() and next() after all valid boundaries have been returned. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_CHARACTER](../android/icu/text/BreakIterator.md) **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_LINE](../android/icu/text/BreakIterator.md) **\[icu\]** |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_SENTENCE](../android/icu/text/BreakIterator.md) **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_TITLE](../android/icu/text/BreakIterator.md) **\[icu\]** |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KIND_WORD](../android/icu/text/BreakIterator.md) **\[icu\]** |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_IDEO](../android/icu/text/BreakIterator.md) Tag value for words containing ideographic characters, lower limit |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_IDEO_LIMIT](../android/icu/text/BreakIterator.md) Tag value for words containing ideographic characters, upper limit |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_KANA](../android/icu/text/BreakIterator.md) Tag value for words containing kana characters, lower limit |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_KANA_LIMIT](../android/icu/text/BreakIterator.md) Tag value for words containing kana characters, upper limit |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_LETTER](../android/icu/text/BreakIterator.md) Tag value for words that contain letters, excluding hiragana, katakana or ideographic characters, lower limit. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_LETTER_LIMIT](../android/icu/text/BreakIterator.md) Tag value for words containing letters, upper limit |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_NONE](../android/icu/text/BreakIterator.md) Tag value for "words" that do not fit into any of other categories. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_NONE_LIMIT](../android/icu/text/BreakIterator.md) Upper bound for tags for uncategorized words. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_NUMBER](../android/icu/text/BreakIterator.md) Tag value for words that appear to be numbers, lower limit. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WORD_NUMBER_LIMIT](../android/icu/text/BreakIterator.md) Tag value for words that appear to be numbers, upper limit. |

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [BreakIterator](../android/icu/text/BreakIterator.md))`()` Default constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/text/BreakIterator.md))`()` Clone method. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [current](../android/icu/text/BreakIterator.md))`()` Return the iterator's current position. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [first](../android/icu/text/BreakIterator.md))`()` Set the iterator to the first boundary position. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [following](../android/icu/text/BreakIterator.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the iterator's current iteration position to be the first boundary position following the specified position. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getAvailableLocales](../android/icu/text/BreakIterator.md))`()` Returns a list of locales for which BreakIterators can be used. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getCharacterInstance](../android/icu/text/BreakIterator.md))`()` Returns a new instance of BreakIterator that locates logical-character boundaries. |
| --- | --- |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getCharacterInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Returns a new instance of BreakIterator that locates logical-character boundaries. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getCharacterInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [Locale](../java/util/Locale.md)!`)` Returns a new instance of BreakIterator that locates logical-character boundaries. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getLineInstance](../android/icu/text/BreakIterator.md))`()` Returns a new instance of BreakIterator that locates legal line- wrapping positions. |
| --- | --- |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getLineInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Returns a new instance of BreakIterator that locates legal line- wrapping positions. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getLineInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [Locale](../java/util/Locale.md)!`)` Returns a new instance of BreakIterator that locates legal line- wrapping positions. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRuleStatus](../android/icu/text/BreakIterator.md))`()` For RuleBasedBreakIterators, return the status tag from the break rule that determined the boundary at the current iteration position. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRuleStatusVec](../android/icu/text/BreakIterator.md))`(`fillInArray:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` For RuleBasedBreakIterators, get the status (tag) values from the break rule(s) that determined the the boundary at the current iteration position. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getSentenceInstance](../android/icu/text/BreakIterator.md))`()` Returns a new instance of BreakIterator that locates sentence boundaries. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getSentenceInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Returns a new instance of BreakIterator that locates sentence boundaries. |
| --- | --- |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getSentenceInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [Locale](../java/util/Locale.md)!`)` Returns a new instance of BreakIterator that locates sentence boundaries. |
| abstract [CharacterIterator](../java/text/CharacterIterator.md)! | [getText](../android/icu/text/BreakIterator.md))`()` Returns a CharacterIterator over the text being analyzed. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getTitleInstance](../android/icu/text/BreakIterator.md))`()` **\[icu\]**Returns a new instance of BreakIterator that locates title boundaries. |
| --- | --- |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getTitleInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Returns a new instance of BreakIterator that locates title boundaries. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getTitleInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [Locale](../java/util/Locale.md)!`)` **\[icu\]**Returns a new instance of BreakIterator that locates title boundaries. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getWordInstance](../android/icu/text/BreakIterator.md))`()` Returns a new instance of BreakIterator that locates word boundaries. |
| --- | --- |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getWordInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Returns a new instance of BreakIterator that locates word boundaries. |
| openstatic [BreakIterator](../android/icu/text/BreakIterator.md)! | [getWordInstance](../android/icu/text/BreakIterator.md))`(`where:` ` [Locale](../java/util/Locale.md)!`)` Returns a new instance of BreakIterator that locates word boundaries. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBoundary](../android/icu/text/BreakIterator.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the specified position is a boundary position. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [last](../android/icu/text/BreakIterator.md))`()` Set the iterator to the last boundary position. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](../android/icu/text/BreakIterator.md))`()` Advances the iterator forward one boundary. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](../android/icu/text/BreakIterator.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Move the iterator by the specified number of steps in the text. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [preceding](../android/icu/text/BreakIterator.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the iterator's current iteration position to be the last boundary position preceding the specified position. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previous](../android/icu/text/BreakIterator.md))`()` Move the iterator backward one boundary. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../android/icu/text/BreakIterator.md))`(`newText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the iterator to analyze a new piece of text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../android/icu/text/BreakIterator.md))`(`newText:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the iterator to analyze a new piece of text. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../android/icu/text/BreakIterator.md))`(`newText:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`)` Sets the iterator to analyze a new piece of text. |

## Constants

### DONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DONE: Int
```

DONE is returned by previous() and next() after all valid boundaries have been returned. 

 Value: -1

### KIND_CHARACTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_CHARACTER: Int
```

**\[icu\]** 

 Value: 0

### KIND_LINE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_LINE: Int
```

**\[icu\]** 

 Value: 2

### KIND_SENTENCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_SENTENCE: Int
```

**\[icu\]** 

 Value: 3

### KIND_TITLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_TITLE: Int
```

**Deprecated:** *ICU 64 Use #getWordInstance instead.*

**\[icu\]** 

 Value: 4

**See Also**

### KIND_WORD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KIND_WORD: Int
```

**\[icu\]** 

 Value: 1

### WORD_IDEO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_IDEO: Int
```

Tag value for words containing ideographic characters, lower limit 

 Value: 400

### WORD_IDEO_LIMIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_IDEO_LIMIT: Int
```

Tag value for words containing ideographic characters, upper limit 

 Value: 500

### WORD_KANA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_KANA: Int
```

Tag value for words containing kana characters, lower limit 

 Value: 300

### WORD_KANA_LIMIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_KANA_LIMIT: Int
```

Tag value for words containing kana characters, upper limit 

 Value: 400

### WORD_LETTER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_LETTER: Int
```

Tag value for words that contain letters, excluding hiragana, katakana or ideographic characters, lower limit. 

 Value: 200

### WORD_LETTER_LIMIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_LETTER_LIMIT: Int
```

Tag value for words containing letters, upper limit 

 Value: 300

### WORD_NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_NONE: Int
```

Tag value for "words" that do not fit into any of other categories. Includes spaces and most punctuation. 

 Value: 0

### WORD_NONE_LIMIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_NONE_LIMIT: Int
```

Upper bound for tags for uncategorized words. 

 Value: 100

### WORD_NUMBER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_NUMBER: Int
```

Tag value for words that appear to be numbers, lower limit. 

 Value: 100

### WORD_NUMBER_LIMIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WORD_NUMBER_LIMIT: Int
```

Tag value for words that appear to be numbers, upper limit. 

 Value: 200

## Protected constructors

### BreakIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected BreakIterator()
```

Default constructor. There is no state that is carried by this abstract base class.

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Clone method. Creates another BreakIterator with the same behavior and current state as this one.

| Return ||
|----------------------------------------------------------------------------|------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | The clone. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### current

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun current(): Int
```

Return the iterator's current position.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The iterator's current position. |

### first

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun first(): Int
```

Set the iterator to the first boundary position. This is always the beginning index of the text this iterator iterates over. For example, if the iterator iterates over a whole string, this function will always return 0.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character offset of the beginning of the stretch of text being broken. |

### following

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun following(offset: Int): Int
```

Sets the iterator's current iteration position to be the first boundary position following the specified position. (Whether the specified position is itself a boundary position or not doesn't matter-- this function always moves the iteration position to the first boundary after the specified position.) If the specified position is the past-the-end position, returns DONE.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The character position to start searching from. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the first boundary position following "offset" (whether or not "offset" itself is a boundary position), or DONE if "offset" is the past-the-end offset. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns a list of locales for which BreakIterators can be used.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | An array of Locales. All of the locales in the array can be used when creating a BreakIterator. |

### getCharacterInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCharacterInstance(): BreakIterator!
```

Returns a new instance of BreakIterator that locates logical-character boundaries. This function assumes that the text being analyzed is in the default locale's language.

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates logical-character boundaries. |

### getCharacterInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCharacterInstance(where: ULocale!): BreakIterator!
```

**\[icu\]**Returns a new instance of BreakIterator that locates logical-character boundaries.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [ULocale](../android/icu/util/ULocale.md)!:A Locale specifying the language of the text being analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates logical-character boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getCharacterInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCharacterInstance(where: Locale!): BreakIterator!
```

Returns a new instance of BreakIterator that locates logical-character boundaries.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [Locale](../java/util/Locale.md)!:A Locale specifying the language of the text being analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates logical-character boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getLineInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLineInstance(): BreakIterator!
```

Returns a new instance of BreakIterator that locates legal line- wrapping positions. This function assumes the text being broken is in the default locale's language.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates legal line-wrapping positions. |

### getLineInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLineInstance(where: ULocale!): BreakIterator!
```

**\[icu\]**Returns a new instance of BreakIterator that locates legal line- wrapping positions.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [ULocale](../android/icu/util/ULocale.md)!:A Locale specifying the language of the text being broken. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates legal line-wrapping positions. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getLineInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLineInstance(where: Locale!): BreakIterator!
```

Returns a new instance of BreakIterator that locates legal line- wrapping positions.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [Locale](../java/util/Locale.md)!:A Locale specifying the language of the text being broken. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates legal line-wrapping positions. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getRuleStatus

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRuleStatus(): Int
```

For RuleBasedBreakIterators, return the status tag from the break rule that determined the boundary at the current iteration position.

For break iterator types that do not support a rule status, a default value of 0 is returned.

<br />

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The status from the break rule that determined the boundary at the current iteration position. |

### getRuleStatusVec

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRuleStatusVec(fillInArray: IntArray!): Int
```

For RuleBasedBreakIterators, get the status (tag) values from the break rule(s) that determined the the boundary at the current iteration position.

For break iterator types that do not support rule status, no values are returned.

If the size of the output array is insufficient to hold the data, the output will be truncated to the available length. No exception will be thrown.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `fillInArray` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:an array to be filled in with the status values. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of rule status values from rules that determined the the boundary at the current iteration position. In the event that the array is too small, the return value is the total number of status values that were available, not the reduced number that were actually returned. |

### getSentenceInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSentenceInstance(): BreakIterator!
```

Returns a new instance of BreakIterator that locates sentence boundaries. This function assumes the text being analyzed is in the default locale's language.

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates sentence boundaries. |

### getSentenceInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSentenceInstance(where: ULocale!): BreakIterator!
```

**\[icu\]**Returns a new instance of BreakIterator that locates sentence boundaries.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [ULocale](../android/icu/util/ULocale.md)!:A Locale specifying the language of the text being analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates sentence boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getSentenceInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSentenceInstance(where: Locale!): BreakIterator!
```

Returns a new instance of BreakIterator that locates sentence boundaries.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [Locale](../java/util/Locale.md)!:A Locale specifying the language of the text being analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates sentence boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getText(): CharacterIterator!
```

Returns a CharacterIterator over the text being analyzed.

***Caution:***The state of the returned CharacterIterator must not be modified in any way while the BreakIterator is still in use. Doing so will lead to undefined behavior of the BreakIterator. Clone the returned CharacterIterator first and work with that.

The returned CharacterIterator is a reference to the**actual iterator being used**by the BreakIterator. No guarantees are made about the current position of this iterator when it is returned; it may differ from the BreakIterators current position. If you need to move that position to examine the text, clone this function's return value first.

| Return ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [CharacterIterator](../java/text/CharacterIterator.md)! | A CharacterIterator over the text being analyzed. |

### getTitleInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTitleInstance(): BreakIterator!
```

**Deprecated:** *ICU 64 Use #getWordInstance instead.*

**\[icu\]**Returns a new instance of BreakIterator that locates title boundaries. This function assumes the text being analyzed is in the default locale's language. The iterator returned locates title boundaries as described for Unicode 3.2 only. For Unicode 4.0 and above title boundary iteration, please use a word boundary iterator. #getWordInstance

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates title boundaries. |

### getTitleInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTitleInstance(where: ULocale!): BreakIterator!
```

**Deprecated:** *ICU 64 Use #getWordInstance instead.*

**\[icu\]**Returns a new instance of BreakIterator that locates title boundaries. The iterator returned locates title boundaries as described for Unicode 3.2 only. For Unicode 4.0 and above title boundary iteration, please use Word Boundary iterator.#getWordInstance

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [ULocale](../android/icu/util/ULocale.md)!:A Locale specifying the language of the text being analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates title boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getTitleInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getTitleInstance(where: Locale!): BreakIterator!
```

**Deprecated:** *ICU 64 Use #getWordInstance instead.*

**\[icu\]**Returns a new instance of BreakIterator that locates title boundaries. The iterator returned locates title boundaries as described for Unicode 3.2 only. For Unicode 4.0 and above title boundary iteration, please use Word Boundary iterator.#getWordInstance

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [Locale](../java/util/Locale.md)!:A Locale specifying the language of the text being analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | A new instance of BreakIterator that locates title boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getWordInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getWordInstance(): BreakIterator!
```

Returns a new instance of BreakIterator that locates word boundaries. This function assumes that the text being analyzed is in the default locale's language.

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | An instance of BreakIterator that locates word boundaries. |

### getWordInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getWordInstance(where: ULocale!): BreakIterator!
```

**\[icu\]**Returns a new instance of BreakIterator that locates word boundaries.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [ULocale](../android/icu/util/ULocale.md)!:A locale specifying the language of the text to be analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | An instance of BreakIterator that locates word boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### getWordInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getWordInstance(where: Locale!): BreakIterator!
```

Returns a new instance of BreakIterator that locates word boundaries.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `where` | [Locale](../java/util/Locale.md)!:A locale specifying the language of the text to be analyzed. |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [BreakIterator](../android/icu/text/BreakIterator.md)! | An instance of BreakIterator that locates word boundaries. |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`where`is null. |

### isBoundary

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBoundary(offset: Int): Boolean
```

Return true if the specified position is a boundary position. If the function returns true, the current iteration position is set to the specified position; if the function returns false, the current iteration position is set as though following() had been called.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to check. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if "offset" is a boundary position. |

### last

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun last(): Int
```

Set the iterator to the last boundary position. This is always the "past-the-end" index of the text this iterator iterates over. For example, if the iterator iterates over a whole string (call it "text"), this function will always return text.length().

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character offset of the end of the stretch of text being broken. |

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): Int
```

Advances the iterator forward one boundary. The current iteration position is updated to point to the next boundary position after the current position, and this is also the value that is returned. If the current position is equal to the value returned by last(), or to DONE, this function returns DONE and sets the current position to DONE.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the first boundary position following the iteration position. |

### next

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(n: Int): Int
```

Move the iterator by the specified number of steps in the text. A positive number moves the iterator forward; a negative number moves the iterator backwards. If this causes the iterator to move off either end of the text, this function returns DONE; otherwise, this function returns the position of the appropriate boundary. Calling this function is equivalent to calling next() or previous() n times.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of boundaries to advance over (if positive, moves forward; if negative, moves backwards). |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the boundary n boundaries from the current iteration position, or DONE if moving n boundaries causes the iterator to advance off either end of the text. |

### preceding

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preceding(offset: Int): Int
```

Sets the iterator's current iteration position to be the last boundary position preceding the specified position. (Whether the specified position is itself a boundary position or not doesn't matter-- this function always moves the iteration position to the last boundary before the specified position.) If the specified position is the starting position, returns DONE.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The character position to start searching from. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the last boundary position preceding "offset" (whether of not "offset" itself is a boundary position), or DONE if "offset" is the starting offset of the iterator. |

### previous

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previous(): Int
```

Move the iterator backward one boundary. The current iteration position is updated to point to the last boundary position before the current position, and this is also the value that is returned. If the current position is equal to the value returned by first(), or to DONE, this function returns DONE and sets the current position to DONE.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the last boundary position preceding the iteration position. |

### setText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setText(newText: CharSequence!): Unit
```

Sets the iterator to analyze a new piece of text. The new piece of text is passed in as a CharSequence, and the current iteration position is reset to the beginning of the text. (The old text is dropped.)

The text underlying the CharSequence must not be be modified while the BreakIterator holds a references to it. (As could possibly occur with a StringBuilder, for example).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:A CharSequence containing the text to analyze with this BreakIterator. |

### setText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setText(newText: String!): Unit
```

Sets the iterator to analyze a new piece of text. The new piece of text is passed in as a String, and the current iteration position is reset to the beginning of the string. (The old text is dropped.)

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `newText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A String containing the text to analyze with this BreakIterator. |

### setText

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setText(newText: CharacterIterator!): Unit
```

Sets the iterator to analyze a new piece of text. This function resets the current iteration position to the beginning of the text. (The old iterator is dropped.)

***Caution:***The supplied CharacterIterator is used directly by the BreakIterator, and must not be altered in any way by code outside of the BreakIterator. Doing so will lead to undefined behavior of the BreakIterator.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newText` | [CharacterIterator](../java/text/CharacterIterator.md)!:A CharacterIterator referring to the text to analyze with this BreakIterator (the iterator's current position is ignored, but its other state is significant). |

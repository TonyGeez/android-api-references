# BreakIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BreakIterator

```
abstract class BreakIterator : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.text.BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#) |

The`BreakIterator`class implements methods for finding the location of boundaries in text. Instances of`BreakIterator`maintain a current position and scan over text returning the index of characters where boundaries occur. Internally,`BreakIterator`scans text using a`CharacterIterator`, and is thus able to scan text held by any object implementing that protocol. A`StringCharacterIterator`is used to scan`String`objects passed to`setText`. The`CharacterIterator`object must not be modified after having been passed to`setText`. If the text in the`CharacterIterator`object is changed, the caller must reset`BreakIterator`by calling`setText`.

You use the factory methods provided by this class to create instances of various types of break iterators. In particular, use`getWordInstance`,`getLineInstance`,`getSentenceInstance`, and`getCharacterInstance`to create`BreakIterator`s that perform word, line, sentence, and character boundary analysis respectively. A single`BreakIterator`can work only on one unit (word, line, sentence, and so on). You must use a different iterator for each unit boundary analysis you wish to perform.

Line boundary analysis determines where a text string can be broken when line-wrapping. The mechanism correctly handles punctuation and hyphenated words. Actual line breaking needs to also consider the available line width and is handled by higher-level software.

Sentence boundary analysis allows selection with correct interpretation of periods within numbers and abbreviations, and trailing punctuation marks such as quotation marks and parentheses.

Word boundary analysis is used by search and replace functions, as well as within text editing applications that allow the user to select words with a double click. Word selection provides correct interpretation of punctuation marks within and following words. Characters that are not part of a word, such as symbols or punctuation marks, have word-breaks on both sides.

Character boundary analysis allows users to interact with characters as they expect to, for example, when moving the cursor through a text string. Character boundary analysis provides correct navigation through character strings, regardless of how the character is stored. The boundaries returned may be those of supplementary characters, combining character sequences, or ligature clusters. For example, an accented character might be stored as a base character and a diacritical mark. What users consider to be a character can differ between languages.

The`BreakIterator`instances returned by the factory methods of this class are intended for use with natural languages only, not for programming language text. It is however possible to define subclasses that tokenize a programming language.

**Examples**:

Creating and using text boundaries: 

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
Print each element in order: 

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
Print each element in reverse order: 

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
Print first element: 

```kotlin
public static void printFirst(BreakIterator boundary, String source) {
      int start = boundary.first();
      int end = boundary.next();
      System.out.println(source.substring(start,end));
  }
  
```
Print last element: 

```kotlin
public static void printLast(BreakIterator boundary, String source) {
      int end = boundary.last();
      int start = boundary.previous();
      System.out.println(source.substring(start,end));
  }
  
```
Print the element at a specified position: 

```kotlin
public static void printAt(BreakIterator boundary, int pos, String source) {
      int end = boundary.following(pos);
      int start = boundary.previous();
      System.out.println(source.substring(start,end));
  }
  
```
Find the next word: 

```kotlin
<code>public static int nextWordStartAfter(int pos, String text) {
      BreakIterator wb = BreakIterator.getWordInstance();
      wb.setText(text);
      int last = wb.following(pos);
      int current = wb.next();
      while (current != BreakIterator.DONE) {
          for (int p = last; p &lt; current; p++) {
              if (Character.isLetter(text.codePointAt(p)))
                  return last;
          }
          last = current;
          current = wb.next();
      }
      return BreakIterator.DONE;
  }
  </code>
```
(The iterator returned by BreakIterator.getWordInstance() is unique in that the break positions it returns don't represent both the start and end of the thing being iterated over. That is, a sentence-break iterator returns breaks that each represent the end of one sentence and the beginning of the next. With the word-break iterator, the characters between two boundaries might be a word, or they might be the punctuation or whitespace between two words. The above code uses a simple heuristic to determine which boundary is the beginning of a word: If the characters between this boundary and the next boundary include at least one letter (this can be an alphabetical letter, a CJK ideograph, a Hangul syllable, a Kana character, etc.), then the text between this boundary and the next is a word; otherwise, it's the material between words.)

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](https://developer.android.com/reference/kotlin/java/text/BreakIterator#DONE:kotlin.Int) DONE is returned by previous(), next(), next(int), preceding(int) and following(int) when either the first or last text boundary has been reached. |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------|---|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#BreakIterator())`()` Constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/BreakIterator#clone())`()` Create a copy of this iterator |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [current](https://developer.android.com/reference/kotlin/java/text/BreakIterator#current())`()` Returns character index of the text boundary that was most recently returned by next(), next(int), previous(), first(), last(), following(int) or preceding(int). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [first](https://developer.android.com/reference/kotlin/java/text/BreakIterator#first())`()` Returns the first boundary. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [following](https://developer.android.com/reference/kotlin/java/text/BreakIterator#following(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the first boundary following the specified character offset. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getAvailableLocales())`()` Returns an array of all locales for which the`get*Instance`methods of this class can return localized instances. |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getCharacterInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getCharacterInstance())`()` Returns a new`BreakIterator`instance for [character breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#character) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()). |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getCharacterInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getCharacterInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a new`BreakIterator`instance for [character breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#character) for the given locale. |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getLineInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getLineInstance())`()` Returns a new`BreakIterator`instance for [line breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#line) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()). |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getLineInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getLineInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a new`BreakIterator`instance for [line breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#line) for the given locale. |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getSentenceInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getSentenceInstance())`()` Returns a new`BreakIterator`instance for [sentence breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#sentence) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()). |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getSentenceInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getSentenceInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a new`BreakIterator`instance for [sentence breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#sentence) for the given locale. |
| abstract [CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator)! | [getText](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getText())`()` Get the text being scanned |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getWordInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getWordInstance())`()` Returns a new`BreakIterator`instance for [word breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#word) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()). |
| openstatic [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | [getWordInstance](https://developer.android.com/reference/kotlin/java/text/BreakIterator#getWordInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a new`BreakIterator`instance for [word breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#word) for the given locale. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBoundary](https://developer.android.com/reference/kotlin/java/text/BreakIterator#isBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the specified character offset is a text boundary. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [last](https://developer.android.com/reference/kotlin/java/text/BreakIterator#last())`()` Returns the last boundary. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](https://developer.android.com/reference/kotlin/java/text/BreakIterator#next())`()` Returns the boundary following the current boundary. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](https://developer.android.com/reference/kotlin/java/text/BreakIterator#next(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the nth boundary from the current boundary. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [preceding](https://developer.android.com/reference/kotlin/java/text/BreakIterator#preceding(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the last boundary preceding the specified character offset. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previous](https://developer.android.com/reference/kotlin/java/text/BreakIterator#previous())`()` Returns the boundary preceding the current boundary. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/java/text/BreakIterator#setText(kotlin.String))`(`newText:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set a new text string to be scanned. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/java/text/BreakIterator#setText(java.text.CharacterIterator))`(`newText:` ` [CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator)!`)` Set a new text for scanning. |

## Constants

### DONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DONE: Int
```

DONE is returned by previous(), next(), next(int), preceding(int) and following(int) when either the first or last text boundary has been reached. 

 Value: -1

## Protected constructors

### BreakIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected BreakIterator()
```

Constructor. BreakIterator is stateless and has no default behavior.

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Create a copy of this iterator

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | A copy of this |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### current

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun current(): Int
```

Returns character index of the text boundary that was most recently returned by next(), next(int), previous(), first(), last(), following(int) or preceding(int). If any of these methods returns`BreakIterator.DONE`because either first or last text boundary has been reached, it returns the first or last text boundary depending on which one is reached.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The text boundary returned from the above methods, first or last text boundary. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/BreakIterator#next()>
- [#next(int)](https://developer.android.com/reference/kotlin/java/text/BreakIterator#next(kotlin.Int))
- <https://developer.android.com/reference/kotlin/java/text/BreakIterator#previous()>
- <https://developer.android.com/reference/kotlin/java/text/BreakIterator#first()>
- <https://developer.android.com/reference/kotlin/java/text/BreakIterator#last()>
- [#following(int)](https://developer.android.com/reference/kotlin/java/text/BreakIterator#following(kotlin.Int))
- [#preceding(int)](https://developer.android.com/reference/kotlin/java/text/BreakIterator#preceding(kotlin.Int)) 

### first

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun first(): Int
```

Returns the first boundary. The iterator's current position is set to the first text boundary.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character index of the first text boundary. |

### following

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun following(offset: Int): Int
```

Returns the first boundary following the specified character offset. If the specified offset is equal to the last text boundary, it returns`BreakIterator.DONE`and the iterator's current position is unchanged. Otherwise, the iterator's current position is set to the returned boundary. The value returned is always greater than the offset or the value`BreakIterator.DONE`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character offset to begin scanning. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The first boundary after the specified offset or`BreakIterator.DONE`if the last text boundary is passed in as the offset. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified offset is less than the first text boundary or greater than the last text boundary. |

### getAvailableLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the`get*Instance`methods of this class can return localized instances. It must contain at least a`Locale`instance equal to [Locale.US](https://developer.android.com/reference/kotlin/java/util/Locale.html#US:java.util.Locale).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | An array of locales for which localized`BreakIterator`instances are available. |

### getCharacterInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCharacterInstance(): BreakIterator!
```

Returns a new`BreakIterator`instance for [character breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#character) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()).

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for character breaks |

### getCharacterInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCharacterInstance(locale: Locale!): BreakIterator!
```

Returns a new`BreakIterator`instance for [character breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#character) for the given locale.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the desired locale |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for character breaks |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### getLineInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLineInstance(): BreakIterator!
```

Returns a new`BreakIterator`instance for [line breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#line) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()).

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for line breaks |

### getLineInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLineInstance(locale: Locale!): BreakIterator!
```

Returns a new`BreakIterator`instance for [line breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#line) for the given locale.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the desired locale |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for line breaks |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### getSentenceInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSentenceInstance(): BreakIterator!
```

Returns a new`BreakIterator`instance for [sentence breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#sentence) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()).

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for sentence breaks |

### getSentenceInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSentenceInstance(locale: Locale!): BreakIterator!
```

Returns a new`BreakIterator`instance for [sentence breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#sentence) for the given locale.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the desired locale |

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for sentence breaks |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getText(): CharacterIterator!
```

Get the text being scanned

| Return ||
|--------------------------------------------------------------------------------------------------|------------------------|
| [CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator)! | the text being scanned |

### getWordInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getWordInstance(): BreakIterator!
```

Returns a new`BreakIterator`instance for [word breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#word) for the [default locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault()).

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for word breaks |

### getWordInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getWordInstance(locale: Locale!): BreakIterator!
```

Returns a new`BreakIterator`instance for [word breaks](https://developer.android.com/reference/kotlin/java/text/BreakIterator#word) for the given locale.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the desired locale |

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------|
| [BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator#)! | A break iterator for word breaks |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### isBoundary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBoundary(offset: Int): Boolean
```

Returns true if the specified character offset is a text boundary.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character offset to check. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if "offset" is a boundary position,`false`otherwise. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified offset is less than the first text boundary or greater than the last text boundary. |

### last

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun last(): Int
```

Returns the last boundary. The iterator's current position is set to the last text boundary.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character index of the last text boundary. |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): Int
```

Returns the boundary following the current boundary. If the current boundary is the last text boundary, it returns`BreakIterator.DONE`and the iterator's current position is unchanged. Otherwise, the iterator's current position is set to the boundary following the current boundary.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character index of the next text boundary or`BreakIterator.DONE`if the current boundary is the last text boundary. Equivalent to next(1). |

**See Also**

- [#next(int)](https://developer.android.com/reference/kotlin/java/text/BreakIterator#next(kotlin.Int)) 

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(n: Int): Int
```

Returns the nth boundary from the current boundary. If either the first or last text boundary has been reached, it returns`BreakIterator.DONE`and the current position is set to either the first or last text boundary depending on which one is reached. Otherwise, the iterator's current position is set to the new boundary. For example, if the iterator's current position is the mth text boundary and three more boundaries exist from the current boundary to the last text boundary, the next(2) call will return m + 2. The new text position is set to the (m + 2)th text boundary. A next(4) call would return`BreakIterator.DONE`and the last text boundary would become the new text position.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):which boundary to return. A value of 0 does nothing. Negative values move to previous boundaries and positive values move to later boundaries. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character index of the nth boundary from the current position or`BreakIterator.DONE`if either first or last text boundary has been reached. |

### preceding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preceding(offset: Int): Int
```

Returns the last boundary preceding the specified character offset. If the specified offset is equal to the first text boundary, it returns`BreakIterator.DONE`and the iterator's current position is unchanged. Otherwise, the iterator's current position is set to the returned boundary. The value returned is always less than the offset or the value`BreakIterator.DONE`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character offset to begin scanning. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The last boundary before the specified offset or`BreakIterator.DONE`if the first text boundary is passed in as the offset. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified offset is less than the first text boundary or greater than the last text boundary. |

### previous

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previous(): Int
```

Returns the boundary preceding the current boundary. If the current boundary is the first text boundary, it returns`BreakIterator.DONE`and the iterator's current position is unchanged. Otherwise, the iterator's current position is set to the boundary preceding the current boundary.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The character index of the previous text boundary or`BreakIterator.DONE`if the current boundary is the first text boundary. |

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setText(newText: String!): Unit
```

Set a new text string to be scanned. The current scan position is reset to first().

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `newText` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:new text to scan. |

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setText(newText: CharacterIterator!): Unit
```

Set a new text for scanning. The current scan position is reset to first().

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `newText` | [CharacterIterator](https://developer.android.com/reference/kotlin/java/text/CharacterIterator)!:new text to scan. |

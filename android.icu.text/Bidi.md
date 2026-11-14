# Bidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Bidi

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/Bidi "View this page in Java") 

```
open class Bidi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#) |

<br />

## Bidi algorithm for ICU

This is an implementation of the Unicode Bidirectional Algorithm. The algorithm is defined in the [Unicode Standard Annex #9](https://www.unicode.org/reports/tr9/).

<br />

Note: Libraries that perform a bidirectional algorithm and reorder strings accordingly are sometimes called "Storage Layout Engines". ICU's Bidi and shaping (ArabicShaping) classes can be used at the core of such "Storage Layout Engines".

### General remarks about the API:

The "limit" of a sequence of characters is the position just after their last character, i.e., one more than that position.

Some of the API methods provide access to "runs". Such a "run" is defined as a sequence of characters that are at the same embedding level after performing the Bidi algorithm.

### Basic concept: paragraph

A piece of text can be divided into several paragraphs by characters with the Bidi class`Block Separator`. For handling of paragraphs, see:

- [countParagraphs](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#countParagraphs())
- [getParaLevel](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParaLevel())
- [getParagraph](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraph(kotlin.Int))
- [getParagraphByIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraphByIndex(kotlin.Int))

### Basic concept: text direction

The direction of a piece of text may be:

- [LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LTR:kotlin.Byte)
- [RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#RTL:kotlin.Byte)
- [MIXED](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MIXED:kotlin.Byte)
- [NEUTRAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#NEUTRAL:kotlin.Byte)

### Basic concept: levels

Levels in this API represent embedding levels according to the Unicode Bidirectional Algorithm. Their low-order bit (even/odd value) indicates the visual direction.

Levels can be abstract values when used for the`paraLevel`and`embeddingLevels`arguments of`setPara()`; there:

- the high-order bit of an`embeddingLevels[]`value indicates whether the using application is specifying the level of a character to*override*whatever the Bidi implementation would resolve it to.
- `paraLevel`can be set to the pseudo-level values`LEVEL_DEFAULT_LTR`and`LEVEL_DEFAULT_RTL`.

The related constants are not real, valid level values.`DEFAULT_XXX`can be used to specify a default for the paragraph level for when the`setPara()`method shall determine it but there is no strongly typed character in the input.

Note that the value for`LEVEL_DEFAULT_LTR`is even and the one for`LEVEL_DEFAULT_RTL`is odd, just like with normal LTR and RTL level values - these special values are designed that way. Also, the implementation assumes that MAX_EXPLICIT_LEVEL is odd.

Note: The numeric values of the related constants will not change: They are tied to the use of 7-bit byte values (plus the override bit) and of the byte data type in this API.

**See Also:**

- [LEVEL_DEFAULT_LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_LTR:kotlin.Byte)
- [LEVEL_DEFAULT_RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_RTL:kotlin.Byte)
- [LEVEL_OVERRIDE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_OVERRIDE:kotlin.Byte)
- [MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte)
- setPara

### Basic concept: Reordering Mode

Reordering mode values indicate which variant of the Bidi algorithm to use.**See Also:**

- [setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))
- [REORDER_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_DEFAULT:kotlin.Short)
- [REORDER_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_NUMBERS_SPECIAL:kotlin.Short)
- [REORDER_GROUP_NUMBERS_WITH_R](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_GROUP_NUMBERS_WITH_R:kotlin.Short)
- [REORDER_RUNS_ONLY](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_RUNS_ONLY:kotlin.Short)
- [REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short)
- [REORDER_INVERSE_LIKE_DIRECT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_LIKE_DIRECT:kotlin.Short)
- [REORDER_INVERSE_FOR_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_FOR_NUMBERS_SPECIAL:kotlin.Short)

### Basic concept: Reordering Options

Reordering options can be applied during Bidi text transformations.**See Also:**

- [setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int))
- [OPTION_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_DEFAULT:kotlin.Int)
- [OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int)
- [OPTION_STREAMING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_STREAMING:kotlin.Int)

#### Sample code for the ICU Bidi API

##### Rendering a paragraph with the ICU Bidi API

This is (hypothetical) sample code that illustrates how the ICU Bidi API could be used to render a paragraph of text. Rendering code depends highly on the graphics system, therefore this sample code must make a lot of assumptions, which may or may not match any existing graphics system's properties.

The basic assumptions are:

- Rendering is done from left to right on a horizontal line.
- A run of single-style, unidirectional text can be rendered at once.
- Such a run of text is passed to the graphics system with characters (code units) in logical order.
- The line-breaking algorithm is very complicated and Locale-dependent - and therefore its implementation omitted from this sample code.

```kotlin
package android.icu.dev.test.bidi;
 
   import android.icu.text.Bidi;
   import android.icu.text.BidiRun;
 
   public class Sample {
 
       static final int styleNormal = 0;
       static final int styleSelected = 1;
       static final int styleBold = 2;
       static final int styleItalics = 4;
       static final int styleSuper=8;
       static final int styleSub = 16;
 
       static class StyleRun {
           int limit;
           int style;
 
           public StyleRun(int limit, int style) {
               this.limit = limit;
               this.style = style;
           }
       }
 
       static class Bounds {
           int start;
           int limit;
 
           public Bounds(int start, int limit) {
               this.start = start;
               this.limit = limit;
           }
       }
 
       static int getTextWidth(String text, int start, int limit,
                               StyleRun[] styleRuns, int styleRunCount) {
           // simplistic way to compute the width
           return limit - start;
       }
 
       // set limit and StyleRun limit for a line
       // from text[start] and from styleRuns[styleRunStart]
       // using Bidi.getLogicalRun(...)
       // returns line width
       static int getLineBreak(String text, Bounds line, Bidi para,
                               StyleRun styleRuns[], Bounds styleRun) {
           // dummy return
           return 0;
       }
 
       // render runs on a line sequentially, always from left to right
 
       // prepare rendering a new line
       static void startLine(byte textDirection, int lineWidth) {
           System.out.println();
       }
 
       // render a run of text and advance to the right by the run width
       // the text[start..limit-1] is always in logical order
       static void renderRun(String text, int start, int limit,
                             byte textDirection, int style) {
       }
 
       // We could compute a cross-product
       // from the style runs with the directional runs
       // and then reorder it.
       // Instead, here we iterate over each run type
       // and render the intersections -
       // with shortcuts in simple (and common) cases.
       // renderParagraph() is the main function.
 
       // render a directional run with
       // (possibly) multiple style runs intersecting with it
       static void renderDirectionalRun(String text, int start, int limit,
                                        byte direction, StyleRun styleRuns[],
                                        int styleRunCount) {
           int i;
 
           // iterate over style runs
           if (direction == Bidi.LTR) {
               int styleLimit;
               for (i = 0; i < styleRunCount; ++i) {
                   styleLimit = styleRuns[i].limit;
                   if (start < styleLimit) {
                       if (styleLimit > limit) {
                           styleLimit = limit;
                       }
                       renderRun(text, start, styleLimit,
                                 direction, styleRuns[i].style);
                       if (styleLimit == limit) {
                           break;
                       }
                       start = styleLimit;
                   }
               }
           } else {
               int styleStart;
 
               for (i = styleRunCount-1; i >= 0; --i) {
                   if (i > 0) {
                       styleStart = styleRuns[i-1].limit;
                   } else {
                       styleStart = 0;
                   }
                   if (limit >= styleStart) {
                       if (styleStart < start) {
                           styleStart = start;
                       }
                       renderRun(text, styleStart, limit, direction,
                                 styleRuns[i].style);
                       if (styleStart == start) {
                           break;
                       }
                       limit = styleStart;
                   }
               }
           }
       }
 
       // the line object represents text[start..limit-1]
       static void renderLine(Bidi line, String text, int start, int limit,
                              StyleRun styleRuns[], int styleRunCount) {
           byte direction = line.getDirection();
           if (direction != Bidi.MIXED) {
               // unidirectional
               if (styleRunCount <= 1) {
                   renderRun(text, start, limit, direction, styleRuns[0].style);
               } else {
                   renderDirectionalRun(text, start, limit, direction,
                                        styleRuns, styleRunCount);
               }
           } else {
               // mixed-directional
               int count, i;
               BidiRun run;
 
               try {
                   count = line.countRuns();
               } catch (IllegalStateException e) {
                   e.printStackTrace();
                   return;
               }
               if (styleRunCount <= 1) {
                   int style = styleRuns[0].style;
 
                   // iterate over directional runs
                   for (i = 0; i < count; ++i) {
                       run = line.getVisualRun(i);
                       renderRun(text, run.getStart(), run.getLimit(),
                                 run.getDirection(), style);
                   }
               } else {
                   // iterate over both directional and style runs
                   for (i = 0; i < count; ++i) {
                       run = line.getVisualRun(i);
                       renderDirectionalRun(text, run.getStart(),
                                            run.getLimit(), run.getDirection(),
                                            styleRuns, styleRunCount);
                   }
               }
           }
       }
 
       static void renderParagraph(String text, byte textDirection,
                                   StyleRun styleRuns[], int styleRunCount,
                                   int lineWidth) {
           int length = text.length();
           Bidi para = new Bidi();
           try {
               para.setPara(text,
                            textDirection != 0 ? Bidi.LEVEL_DEFAULT_RTL
                                               : Bidi.LEVEL_DEFAULT_LTR,
                            null);
           } catch (Exception e) {
               e.printStackTrace();
               return;
           }
           byte paraLevel = (byte)(1 & para.getParaLevel());
           StyleRun styleRun = new StyleRun(length, styleNormal);
 
           if (styleRuns == null || styleRunCount <= 0) {
               styleRuns = new StyleRun[1];
               styleRunCount = 1;
               styleRuns[0] = styleRun;
           }
           // assume styleRuns[styleRunCount-1].limit>=length
 
           int width = getTextWidth(text, 0, length, styleRuns, styleRunCount);
           if (width <= lineWidth) {
               // everything fits onto one line
 
               // prepare rendering a new line from either left or right
               startLine(paraLevel, width);
 
               renderLine(para, text, 0, length, styleRuns, styleRunCount);
           } else {
               // we need to render several lines
               Bidi line = new Bidi(length, 0);
               int start = 0, limit;
               int styleRunStart = 0, styleRunLimit;
 
               for (;;) {
                   limit = length;
                   styleRunLimit = styleRunCount;
                   width = getLineBreak(text, new Bounds(start, limit),
                                        para, styleRuns,
                                        new Bounds(styleRunStart, styleRunLimit));
                   try {
                       line = para.setLine(start, limit);
                   } catch (Exception e) {
                       e.printStackTrace();
                       return;
                   }
                   // prepare rendering a new line
                   // from either left or right
                   startLine(paraLevel, width);
 
                   if (styleRunStart > 0) {
                       int newRunCount = styleRuns.length - styleRunStart;
                       StyleRun[] newRuns = new StyleRun[newRunCount];
                       System.arraycopy(styleRuns, styleRunStart, newRuns, 0,
                                        newRunCount);
                       renderLine(line, text, start, limit, newRuns,
                                  styleRunLimit - styleRunStart);
                   } else {
                       renderLine(line, text, start, limit, styleRuns,
                                  styleRunLimit - styleRunStart);
                   }
                   if (limit == length) {
                       break;
                   }
                   start = limit;
                   styleRunStart = styleRunLimit - 1;
                   if (start >= styleRuns[styleRunStart].limit) {
                       ++styleRunStart;
                   }
               }
           }
       }
 
       public static void main(String[] args)
       {
           renderParagraph("Some Latin text...", Bidi.LTR, null, 0, 80);
           renderParagraph("Some Hebrew text...", Bidi.RTL, null, 0, 60);
       }
   }
 
  
```

## Summary

| Constants ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_DEFAULT_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_DEFAULT_LEFT_TO_RIGHT:kotlin.Int) Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_DEFAULT_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_DEFAULT_RIGHT_TO_LEFT:kotlin.Int) Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_LEFT_TO_RIGHT:kotlin.Int) Constant indicating base direction is left-to-right. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_RIGHT_TO_LEFT:kotlin.Int) Constant indicating base direction is right-to-left. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [DO_MIRRORING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DO_MIRRORING:kotlin.Short) option bit for writeReordered(): replace characters with the "mirrored" property in RTL runs by their mirror-image mappings |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [INSERT_LRM_FOR_NUMERIC](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#INSERT_LRM_FOR_NUMERIC:kotlin.Short) option bit for writeReordered(): surround the run with LRMs if necessary; this is part of the approximate "inverse Bidi" algorithm |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [KEEP_BASE_COMBINING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#KEEP_BASE_COMBINING:kotlin.Short) option bit for writeReordered(): keep combining characters after their base characters in RTL runs |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LEVEL_DEFAULT_LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_LTR:kotlin.Byte) Paragraph level setting |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LEVEL_DEFAULT_RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_RTL:kotlin.Byte) Paragraph level setting |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LEVEL_OVERRIDE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_OVERRIDE:kotlin.Byte) Bit flag for level input. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LTR:kotlin.Byte) Left-to-right text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAP_NOWHERE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAP_NOWHERE:kotlin.Int) Special value which can be returned by the mapping methods when a logical index has no corresponding visual index or vice-versa. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte) Maximum explicit embedding level. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [MIXED](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MIXED:kotlin.Byte) Mixed-directional text. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [NEUTRAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#NEUTRAL:kotlin.Byte) No strongly directional text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_DEFAULT:kotlin.Int) Option value for`setReorderingOptions`: disable all the options which can be set with this method |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int) Option bit for`setReorderingOptions`: insert Bidi marks (LRM or RLM) when needed to ensure correct result of a reordering to a Logical order |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int) Option bit for`setReorderingOptions`: remove Bidi control characters |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_STREAMING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_STREAMING:kotlin.Int) Option bit for`setReorderingOptions`: process the output as part of a stream to be continued |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [OUTPUT_REVERSE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OUTPUT_REVERSE:kotlin.Short) option bit for writeReordered(): write the output in reverse order |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REMOVE_BIDI_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REMOVE_BIDI_CONTROLS:kotlin.Short) option bit for writeReordered(): remove Bidi control characters (this does not affect INSERT_LRM_FOR_NUMERIC) |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_DEFAULT:kotlin.Short) Reordering mode: Regular Logical to Visual Bidi algorithm according to Unicode. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_GROUP_NUMBERS_WITH_R](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_GROUP_NUMBERS_WITH_R:kotlin.Short) Reordering mode: Logical to Visual algorithm grouping numbers with adjacent R characters (reversible algorithm). |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_INVERSE_FOR_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_FOR_NUMBERS_SPECIAL:kotlin.Short) Reordering mode: Inverse Bidi (Visual to Logical) algorithm for the`REORDER_NUMBERS_SPECIAL`Bidi algorithm. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_INVERSE_LIKE_DIRECT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_LIKE_DIRECT:kotlin.Short) Reordering mode: Visual to Logical algorithm equivalent to the regular Logical to Visual algorithm. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short) Reordering mode: Visual to Logical algorithm which handles numbers like L (same algorithm as selected by`setInverse(true)`. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_NUMBERS_SPECIAL:kotlin.Short) Reordering mode: Logical to Visual algorithm which handles numbers in a way which mimicks the behavior of Windows XP. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [REORDER_RUNS_ONLY](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_RUNS_ONLY:kotlin.Short) Reordering mode: Reorder runs only to transform a Logical LTR string to the logical RTL string with the same display, or vice-versa. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#RTL:kotlin.Byte) Right-to-left text. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#Bidi())`()` Allocate a`Bidi`object. |
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#Bidi(kotlin.CharArray,%20kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `textStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `embeddings:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `embStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `paragraphLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create Bidi from the given text, embedding, and direction information. |
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#Bidi(kotlin.Int,%20kotlin.Int))`(`maxLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxRunCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Allocate a`Bidi`object with preallocated memory for internal structures. |
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#Bidi(kotlin.String,%20kotlin.Int))`(`paragraph:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create Bidi from the given paragraph of text and base direction. |
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#Bidi(java.text.AttributedCharacterIterator))`(`paragraph:` ` [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)!`)` Create Bidi from the given paragraph of text. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [baseIsLeftToRight](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#baseIsLeftToRight())`()` Return true if the base direction is left-to-right |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countParagraphs](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#countParagraphs())`()` Get the number of paragraphs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [countRuns](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#countRuns())`()` Get the number of runs. |
| open [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#)! | [createLineBidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#createLineBidi(kotlin.Int,%20kotlin.Int))`(`lineStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `lineLimit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a Bidi object representing the bidi information on a line of text within the paragraph represented by the current Bidi. |
| openstatic [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getBaseDirection](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getBaseDirection(kotlin.CharSequence))`(`paragraph:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Get the base direction of the text provided according to the Unicode Bidirectional Algorithm. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBaseLevel](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getBaseLevel())`()` Return the base level (0 if left-to-right, 1 if right-to-left). |
| open [BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier)! | [getCustomClassifier](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getCustomClassifier())`()` Gets the current custom class classifier used for Bidi class determination. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCustomizedClass](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getCustomizedClass(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the Bidi class for a given code point. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getDirection](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getDirection())`()` Get the directionality of the text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLength())`()` Get the length of the text. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getLevelAt](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLevelAt(kotlin.Int))`(`charIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the level for one character. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getLevels](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLevels())`()` Get an array of levels for each character. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLogicalIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalIndex(kotlin.Int))`(`visualIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the logical text position from a visual position. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getLogicalMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalMap())`()` Get a logical-to-visual index map (array) for the characters in the`Bidi`(paragraph or line) object. |
| open [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | [getLogicalRun](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalRun(kotlin.Int))`(`logicalPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a logical run. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getParaLevel](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParaLevel())`()` Get the paragraph level of the text. |
| open [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | [getParagraph](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraph(kotlin.Int))`(`charIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a paragraph, given a position within the text. |
| open [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | [getParagraphByIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraphByIndex(kotlin.Int))`(`paraIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a paragraph, given the index of this paragraph. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraphIndex(kotlin.Int))`(`charIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the index of a paragraph, given a position within the text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength())`()` Get the length of the source text processed by the last call to`setPara()`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getReorderingMode())`()` What is the requested reordering mode for a given Bidi object? |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getReorderingOptions())`()` What are the reordering options applied to a given Bidi object? |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getResultLength())`()` Get the length of the reordered text resulting from the last call to`setPara()`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunCount](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getRunCount())`()` Return the number of level runs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLevel](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getRunLevel(kotlin.Int))`(`run:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the level of the nth logical run in this line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunLimit](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getRunLimit(kotlin.Int))`(`run:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the index of the character past the end of the nth logical run in this line, as an offset from the start of the line. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRunStart](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getRunStart(kotlin.Int))`(`run:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the index of the character at the start of the nth logical run in this line, as an offset from the start of the line. |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getText())`()` Get the text. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTextAsString](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getTextAsString())`()` Get the text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualIndex(kotlin.Int))`(`logicalIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the visual position from a logical text position. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getVisualMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualMap())`()` Get a visual-to-logical index map (array) for the characters in the`Bidi`(paragraph or line) object. |
| open [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | [getVisualRun](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualRun(kotlin.Int))`(`runIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get a`BidiRun`object according to its index. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [invertMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#invertMap(kotlin.IntArray))`(`srcMap:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Invert an index map. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#isInverse())`()` Is this`Bidi`object set to perform the inverse Bidi algorithm? |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLeftToRight](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#isLeftToRight())`()` Return true if the line is all left-to-right text and the base direction is left-to-right. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMixed](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#isMixed())`()` Return true if the line is not left-to-right or right-to-left. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOrderParagraphsLTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#isOrderParagraphsLTR())`()` Is this`Bidi`object set to allocate level 0 to block separators so that successive paragraphs progress from left to right? |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRightToLeft](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#isRightToLeft())`()` Return true if the line is all right-to-left text, and the base direction is right-to-left |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [orderParagraphsLTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#orderParagraphsLTR(kotlin.Boolean))`(`ordarParaLTR:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specify whether block separators must be allocated level zero, so that successive paragraphs will progress from left to right. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [reorderLogical](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#reorderLogical(kotlin.ByteArray))`(`levels:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` This is a convenience method that does not use a`Bidi`object. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [reorderVisual](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#reorderVisual(kotlin.ByteArray))`(`levels:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` This is a convenience method that does not use a`Bidi`object. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reorderVisually](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#reorderVisually(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`levels:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `levelStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objects:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `objectStart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `count:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reorder the objects in the array into visual order based on their levels. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [requiresBidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#requiresBidi(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int))`(`text:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return true if the specified text requires bidi analysis. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setContext(kotlin.String,%20kotlin.String))`(`prologue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `epilogue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the context before a call to setPara(). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCustomClassifier](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setCustomClassifier(android.icu.text.BidiClassifier))`(`classifier:` ` [BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier)!`)` Set a custom Bidi classifier used by the UBA implementation for Bidi class determination. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setInverse(kotlin.Boolean))`(`isInverse:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Modify the operation of the Bidi algorithm such that it approximates an "inverse Bidi" algorithm. |
| open [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#)! | [setLine](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setLine(kotlin.Int,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` `setLine()`returns a`Bidi`object to contain the reordering information, especially the resolved levels, for all the characters in a line of text. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPara](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setPara(kotlin.CharArray,%20kotlin.Byte,%20kotlin.ByteArray))`(`chars:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `paraLevel:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `embeddingLevels:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Perform the Unicode Bidi algorithm. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPara](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setPara(kotlin.String,%20kotlin.Byte,%20kotlin.ByteArray))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `paraLevel:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`, `embeddingLevels:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Perform the Unicode Bidi algorithm. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPara](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setPara(java.text.AttributedCharacterIterator))`(`paragraph:` ` [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)!`)` Perform the Unicode Bidi algorithm on a given paragraph, as defined in the [Unicode Standard Annex #9](https://www.unicode.org/reports/tr9/), version 13, also described in The Unicode Standard, Version 4. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))`(`reorderingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Modify the operation of the Bidi algorithm such that it implements some variant to the basic Bidi algorithm or approximates an "inverse Bidi" algorithm, depending on different values of the "reordering mode". |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int))`(`options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Specify which of the reordering options should be applied during Bidi transformations. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int))`(`options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Take a`Bidi`object containing the reordering information for a piece of text (one or more paragraphs) set by`setPara()`or for a line of text set by`setLine()`and return a string containing the reordered text. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [writeReverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReverse(kotlin.String,%20kotlin.Int))`(`src:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reverse a Right-To-Left run of Unicode text. |

## Constants

### DIRECTION_DEFAULT_LEFT_TO_RIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_DEFAULT_LEFT_TO_RIGHT: Int
```

Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. If no strong directional character is present, the base direction is left-to-right. 

 Value: 126

### DIRECTION_DEFAULT_RIGHT_TO_LEFT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_DEFAULT_RIGHT_TO_LEFT: Int
```

Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. If no strong directional character is present, the base direction is right-to-left. 

 Value: 127

### DIRECTION_LEFT_TO_RIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_LEFT_TO_RIGHT: Int
```

Constant indicating base direction is left-to-right. 

 Value: 0

### DIRECTION_RIGHT_TO_LEFT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIRECTION_RIGHT_TO_LEFT: Int
```

Constant indicating base direction is right-to-left. 

 Value: 1

### DO_MIRRORING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DO_MIRRORING: Short
```

option bit for writeReordered(): replace characters with the "mirrored" property in RTL runs by their mirror-image mappings 

 Value: 2

**See Also**

- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### INSERT_LRM_FOR_NUMERIC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INSERT_LRM_FOR_NUMERIC: Short
```

option bit for writeReordered(): surround the run with LRMs if necessary; this is part of the approximate "inverse Bidi" algorithm

This option does not imply corresponding adjustment of the index mappings. 

 Value: 4

**See Also**

- [#setInverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setInverse(kotlin.Boolean))
- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### KEEP_BASE_COMBINING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEEP_BASE_COMBINING: Short
```

option bit for writeReordered(): keep combining characters after their base characters in RTL runs 

 Value: 1

**See Also**

- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### LEVEL_DEFAULT_LTR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_DEFAULT_LTR: Byte
```

Paragraph level setting

Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. If no strong directional character is present, then set the paragraph level to 0 (left-to-right).

If this value is used in conjunction with reordering modes`REORDER_INVERSE_LIKE_DIRECT`or`REORDER_INVERSE_FOR_NUMBERS_SPECIAL`, the text to reorder is assumed to be visual LTR, and the text after reordering is required to be the corresponding logical string with appropriate contextual direction. The direction of the result string will be RTL if either the rightmost or leftmost strong character of the source text is RTL or Arabic Letter, the direction will be LTR otherwise.

If reordering option`OPTION_INSERT_MARKS`is set, an RLM may be added at the beginning of the result string to ensure round trip (that the result string, when reordered back to visual, will produce the original source text). 

 Value: 126

**See Also**

- [#REORDER_INVERSE_LIKE_DIRECT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_LIKE_DIRECT:kotlin.Short)
- [#REORDER_INVERSE_FOR_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_FOR_NUMBERS_SPECIAL:kotlin.Short) 

### LEVEL_DEFAULT_RTL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_DEFAULT_RTL: Byte
```

Paragraph level setting

Constant indicating that the base direction depends on the first strong directional character in the text according to the Unicode Bidirectional Algorithm. If no strong directional character is present, then set the paragraph level to 1 (right-to-left).

If this value is used in conjunction with reordering modes`REORDER_INVERSE_LIKE_DIRECT`or`REORDER_INVERSE_FOR_NUMBERS_SPECIAL`, the text to reorder is assumed to be visual LTR, and the text after reordering is required to be the corresponding logical string with appropriate contextual direction. The direction of the result string will be RTL if either the rightmost or leftmost strong character of the source text is RTL or Arabic Letter, or if the text contains no strong character; the direction will be LTR otherwise.

If reordering option`OPTION_INSERT_MARKS`is set, an RLM may be added at the beginning of the result string to ensure round trip (that the result string, when reordered back to visual, will produce the original source text). 

 Value: 127

**See Also**

- [#REORDER_INVERSE_LIKE_DIRECT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_LIKE_DIRECT:kotlin.Short)
- [#REORDER_INVERSE_FOR_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_FOR_NUMBERS_SPECIAL:kotlin.Short) 

### LEVEL_OVERRIDE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_OVERRIDE: Byte
```

Bit flag for level input. Overrides directional properties. 

 Value: -128

### LTR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LTR: Byte
```

Left-to-right text.

- As return value for`getDirection()`, it means that the source string contains no right-to-left characters, or that the source string is empty and the paragraph level is even.
- As return value for`getBaseDirection()`, it means that the first strong character of the source string has a left-to-right direction.

<br />

 Value: 0

### MAP_NOWHERE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAP_NOWHERE: Int
```

Special value which can be returned by the mapping methods when a logical index has no corresponding visual index or vice-versa. This may happen for the logical-to-visual mapping of a Bidi control when option`OPTION_REMOVE_CONTROLS`is specified. This can also happen for the visual-to-logical mapping of a Bidi mark (LRM or RLM) inserted by option`OPTION_INSERT_MARKS`. 

 Value: -1

**See Also**

- [#getVisualIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualIndex(kotlin.Int))
- [#getVisualMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualMap())
- [#getLogicalIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalIndex(kotlin.Int))
- [#getLogicalMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalMap())
- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int) 

### MAX_EXPLICIT_LEVEL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_EXPLICIT_LEVEL: Byte
```

Maximum explicit embedding level. Same as the max_depth value in the [Unicode Bidirectional Algorithm](http://www.unicode.org/reports/tr9/#BD2). (The maximum resolved level can be up to`MAX_EXPLICIT_LEVEL+1`). 

 Value: 125

### MIXED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIXED: Byte
```

Mixed-directional text.

As return value for`getDirection()`, it means that the source string contains both left-to-right and right-to-left characters. 

 Value: 2

### NEUTRAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NEUTRAL: Byte
```

No strongly directional text.

As return value for`getBaseDirection()`, it means that the source string is missing or empty, or contains neither left-to-right nor right-to-left characters. 

 Value: 3

### OPTION_DEFAULT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_DEFAULT: Int
```

Option value for`setReorderingOptions`: disable all the options which can be set with this method 

 Value: 0

**See Also**

- [#setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int)) 

### OPTION_INSERT_MARKS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_INSERT_MARKS: Int
```

Option bit for`setReorderingOptions`: insert Bidi marks (LRM or RLM) when needed to ensure correct result of a reordering to a Logical order

This option must be set or reset before calling`setPara`.

This option is significant only with reordering modes which generate a result with Logical order, specifically.

- `REORDER_RUNS_ONLY`
- `REORDER_INVERSE_NUMBERS_AS_L`
- `REORDER_INVERSE_LIKE_DIRECT`
- `REORDER_INVERSE_FOR_NUMBERS_SPECIAL`

If this option is set in conjunction with reordering mode`REORDER_INVERSE_NUMBERS_AS_L`or with calling`setInverse(true)`, it implies option`INSERT_LRM_FOR_NUMERIC`in calls to method`writeReordered()`.

For other reordering modes, a minimum number of LRM or RLM characters will be added to the source text after reordering it so as to ensure round trip, i.e. when applying the inverse reordering mode on the resulting logical text with removal of Bidi marks (option`OPTION_REMOVE_CONTROLS`set before calling`setPara()`or option`REMOVE_BIDI_CONTROLS`in`writeReordered`), the result will be identical to the source text in the first transformation.

This option will be ignored if specified together with option`OPTION_REMOVE_CONTROLS`. It inhibits option`REMOVE_BIDI_CONTROLS`in calls to method`writeReordered()`and it implies option`INSERT_LRM_FOR_NUMERIC`in calls to method`writeReordered()`if the reordering mode is`REORDER_INVERSE_NUMBERS_AS_L`. 

 Value: 1

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))
- [#setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int))
- [#INSERT_LRM_FOR_NUMERIC](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#INSERT_LRM_FOR_NUMERIC:kotlin.Short)
- [#REMOVE_BIDI_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REMOVE_BIDI_CONTROLS:kotlin.Short)
- [#OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int)
- [#REORDER_RUNS_ONLY](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_RUNS_ONLY:kotlin.Short)
- [#REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short)
- [#REORDER_INVERSE_LIKE_DIRECT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_LIKE_DIRECT:kotlin.Short)
- [#REORDER_INVERSE_FOR_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_FOR_NUMBERS_SPECIAL:kotlin.Short) 

### OPTION_REMOVE_CONTROLS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_REMOVE_CONTROLS: Int
```

Option bit for`setReorderingOptions`: remove Bidi control characters

This option must be set or reset before calling`setPara`.

This option nullifies option`OPTION_INSERT_MARKS`. It inhibits option`INSERT_LRM_FOR_NUMERIC`in calls to method`writeReordered()`and it implies option`REMOVE_BIDI_CONTROLS`in calls to that method. 

 Value: 2

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))
- [#setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int))
- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#INSERT_LRM_FOR_NUMERIC](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#INSERT_LRM_FOR_NUMERIC:kotlin.Short)
- [#REMOVE_BIDI_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REMOVE_BIDI_CONTROLS:kotlin.Short) 

### OPTION_STREAMING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_STREAMING: Int
```

Option bit for`setReorderingOptions`: process the output as part of a stream to be continued

This option must be set or reset before calling`setPara`.

This option specifies that the caller is interested in processing large text object in parts. The results of the successive calls are expected to be concatenated by the caller. Only the call for the last part will have this option bit off.

When this option bit is on,`setPara()`may process less than the full source text in order to truncate the text at a meaningful boundary. The caller should call`getProcessedLength()`immediately after calling`setPara()`in order to determine how much of the source text has been processed. Source text beyond that length should be resubmitted in following calls to`setPara`. The processed length may be less than the length of the source text if a character preceding the last character of the source text constitutes a reasonable boundary (like a block separator) for text to be continued. 
If the last character of the source text constitutes a reasonable boundary, the whole text will be processed at once. 
If nowhere in the source text there exists such a reasonable boundary, the processed length will be zero. 
The caller should check for such an occurrence and do one of the following:

- submit a larger amount of text with a better chance to include a reasonable boundary.
- resubmit the same text after turning off option`OPTION_STREAMING`.

In all cases, this option should be turned off before processing the last part of the text.

When the`OPTION_STREAMING`option is used, it is recommended to call`orderParagraphsLTR(true)`before calling`setPara()`so that later paragraphs may be concatenated to previous paragraphs on the right. 

 Value: 4

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))
- [#setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int))
- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength()) 

### OUTPUT_REVERSE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OUTPUT_REVERSE: Short
```

option bit for writeReordered(): write the output in reverse order

This has the same effect as calling`writeReordered()`first without this option, and then calling`writeReverse()`without mirroring. Doing this in the same step is faster and avoids a temporary buffer. An example for using this option is output to a character terminal that is designed for RTL scripts and stores text in reverse order. 

 Value: 16

**See Also**

- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### REMOVE_BIDI_CONTROLS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REMOVE_BIDI_CONTROLS: Short
```

option bit for writeReordered(): remove Bidi control characters (this does not affect INSERT_LRM_FOR_NUMERIC)

This option does not imply corresponding adjustment of the index mappings. 

 Value: 8

**See Also**

- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int))
- [#INSERT_LRM_FOR_NUMERIC](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#INSERT_LRM_FOR_NUMERIC:kotlin.Short) 

### REORDER_DEFAULT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_DEFAULT: Short
```

Reordering mode: Regular Logical to Visual Bidi algorithm according to Unicode. 

 Value: 0

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### REORDER_GROUP_NUMBERS_WITH_R

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_GROUP_NUMBERS_WITH_R: Short
```

Reordering mode: Logical to Visual algorithm grouping numbers with adjacent R characters (reversible algorithm). 

 Value: 2

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### REORDER_INVERSE_FOR_NUMBERS_SPECIAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_INVERSE_FOR_NUMBERS_SPECIAL: Short
```

Reordering mode: Inverse Bidi (Visual to Logical) algorithm for the`REORDER_NUMBERS_SPECIAL`Bidi algorithm. 

 Value: 6

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### REORDER_INVERSE_LIKE_DIRECT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_INVERSE_LIKE_DIRECT: Short
```

Reordering mode: Visual to Logical algorithm equivalent to the regular Logical to Visual algorithm. 

 Value: 5

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### REORDER_INVERSE_NUMBERS_AS_L

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_INVERSE_NUMBERS_AS_L: Short
```

Reordering mode: Visual to Logical algorithm which handles numbers like L (same algorithm as selected by`setInverse(true)`. 

 Value: 4

**See Also**

- [#setInverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setInverse(kotlin.Boolean))
- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### REORDER_NUMBERS_SPECIAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_NUMBERS_SPECIAL: Short
```

Reordering mode: Logical to Visual algorithm which handles numbers in a way which mimicks the behavior of Windows XP. 

 Value: 1

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### REORDER_RUNS_ONLY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REORDER_RUNS_ONLY: Short
```

Reordering mode: Reorder runs only to transform a Logical LTR string to the logical RTL string with the same display, or vice-versa. 
If this mode is set together with option`OPTION_INSERT_MARKS`, some Bidi controls in the source text may be removed and other controls may be added to produce the minimum combination which has the required display. 

 Value: 3

**See Also**

- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### RTL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RTL: Byte
```

Right-to-left text.

- As return value for`getDirection()`, it means that the source string contains no left-to-right characters, or that the source string is empty and the paragraph level is odd.
- As return value for`getBaseDirection()`, it means that the first strong character of the source string has a right-to-left direction.

<br />

 Value: 1

## Public constructors

### Bidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi()
```

Allocate a`Bidi`object. Such an object is initially empty. It is assigned the Bidi properties of a piece of text containing one or more paragraphs by`setPara()`or the Bidi properties of a line within a paragraph by`setLine()`.

This object can be reused.

`setPara()`and`setLine()`will allocate additional memory for internal structures as necessary. 

### Bidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi(
    text: CharArray!, 
    textStart: Int, 
    embeddings: ByteArray!, 
    embStart: Int, 
    paragraphLength: Int, 
    flags: Int)
```

Create Bidi from the given text, embedding, and direction information.

The embeddings array may be null. If present, the values represent embedding level information. Negative values indicate overrides at the absolute value of the level. Positive values indicate embeddings. (See [MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte).) Where values are zero, the base embedding level as determined by the base direction is assumed, except for paragraph separators which remain at 0 to prevent reordering of paragraphs.

Note: This constructor calls setPara() internally, after converting the java.text.Bidi-style embeddings with negative overrides into ICU-style embeddings with bit fields for [LEVEL_OVERRIDE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_OVERRIDE:kotlin.Byte) and the level.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:an array containing the paragraph of text to process. |
| `textStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the text array of the start of the paragraph. |
| `embeddings` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:an array containing embedding values for each character in the paragraph. This can be null, in which case it is assumed that there is no external embedding information. |
| `embStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the embedding array of the start of the paragraph. |
| `paragraphLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the paragraph in the text and embeddings arrays. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a collection of flags that control the algorithm. The algorithm understands the flags DIRECTION_LEFT_TO_RIGHT, DIRECTION_RIGHT_TO_LEFT, DIRECTION_DEFAULT_LEFT_TO_RIGHT, and DIRECTION_DEFAULT_RIGHT_TO_LEFT. Other values are reserved. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the values in embeddings are not within the allowed range |

**See Also**

- [#DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_LEFT_TO_RIGHT:kotlin.Int)
- [#DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_RIGHT_TO_LEFT:kotlin.Int)
- [#DIRECTION_DEFAULT_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_DEFAULT_LEFT_TO_RIGHT:kotlin.Int)
- [#DIRECTION_DEFAULT_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_DEFAULT_RIGHT_TO_LEFT:kotlin.Int) 

### Bidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi(
    maxLength: Int, 
    maxRunCount: Int)
```

Allocate a`Bidi`object with preallocated memory for internal structures. This method provides a`Bidi`object like the default constructor but it also preallocates memory for internal structures according to the sizings supplied by the caller.

The preallocation can be limited to some of the internal memory by setting some values to 0 here. That means that if, e.g.,`maxRunCount`cannot be reasonably predetermined and should not be set to`maxLength`(the only failproof value) to avoid wasting memory, then`maxRunCount`could be set to 0 here and the internal structures that are associated with it will be allocated on demand, just like with the default constructor.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the maximum text or line length that internal memory will be preallocated for. An attempt to associate this object with a longer text will fail, unless this value is 0, which leaves the allocation up to the implementation. |
| `maxRunCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the maximum anticipated number of same-level runs that internal memory will be preallocated for. An attempt to access visual runs on an object that was not preallocated for as many runs as the text was actually resolved to will fail, unless this value is 0, which leaves the allocation up to the implementation. The number of runs depends on the actual text and maybe anywhere between 1 and`maxLength`. It is typically small. |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if maxLength or maxRunCount is less than 0 |

### Bidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

**See Also**

- [#DIRECTION_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_LEFT_TO_RIGHT:kotlin.Int)
- [#DIRECTION_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_RIGHT_TO_LEFT:kotlin.Int)
- [#DIRECTION_DEFAULT_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_DEFAULT_LEFT_TO_RIGHT:kotlin.Int)
- [#DIRECTION_DEFAULT_RIGHT_TO_LEFT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DIRECTION_DEFAULT_RIGHT_TO_LEFT:kotlin.Int) 

### Bidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Bidi(paragraph: AttributedCharacterIterator!)
```

Create Bidi from the given paragraph of text.

The RUN_DIRECTION attribute in the text, if present, determines the base direction (left-to-right or right-to-left). If not present, the base direction is computed using the Unicode Bidirectional Algorithm, defaulting to left-to-right if there are no strong directional characters in the text. This attribute, if present, must be applied to all the text in the paragraph.

The BIDI_EMBEDDING attribute in the text, if present, represents embedding level information. Negative values indicate overrides at the absolute value of the level. Positive values indicate embeddings. (See [MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte).) Where values are zero or not defined, the base embedding level as determined by the base direction is assumed.

The NUMERIC_SHAPING attribute in the text, if present, converts European digits to other decimal digits before running the bidi algorithm. This attribute, if present, must be applied to all the text in the paragraph.

Note: this constructor calls setPara() internally.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paragraph` | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)!:a paragraph of text with optional character and paragraph attribute information |

## Public methods

### baseIsLeftToRight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun baseIsLeftToRight(): Boolean
```

Return true if the base direction is left-to-right

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the base direction is left-to-right |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### countParagraphs

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countParagraphs(): Int
```

Get the number of paragraphs.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of paragraphs. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### countRuns

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun countRuns(): Int
```

Get the number of runs. This method may invoke the actual reordering on the`Bidi`object, after`setPara()`may have resolved only the levels of the text. Therefore,`countRuns()`may have to allocate memory, and may throw an exception if it fails to do so.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of runs. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### createLineBidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createLineBidi(
    lineStart: Int, 
    lineLimit: Int
): Bidi!
```

Create a Bidi object representing the bidi information on a line of text within the paragraph represented by the current Bidi. This call is not required if the entire paragraph fits on one line.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `lineStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset from the start of the paragraph to the start of the line. |
| `lineLimit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset from the start of the paragraph to the limit of the line. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara` |
| `java.lang.IllegalArgumentException` | if lineStart and lineLimit are not in the range`0<=lineStart<lineLimit<=getProcessedLength()`, or if the specified line crosses a paragraph boundary |

### getBaseDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getBaseDirection(paragraph: CharSequence!): Byte
```

Get the base direction of the text provided according to the Unicode Bidirectional Algorithm. The base direction is derived from the first character in the string with bidirectional character type L, R, or AL. If the first such character has type L, LTR is returned. If the first such character has type R or AL, RTL is returned. If the string does not contain any character of these types, then NEUTRAL is returned. This is a lightweight function for use when only the base direction is needed and no further bidi processing of the text is needed.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `paragraph` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text whose paragraph level direction is needed. |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | LTR, RTL, NEUTRAL |

**See Also**

- [#LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LTR:kotlin.Byte)
- [#RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#RTL:kotlin.Byte)
- [#NEUTRAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#NEUTRAL:kotlin.Byte) 

### getBaseLevel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBaseLevel(): Int
```

Return the base level (0 if left-to-right, 1 if right-to-left).

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the base level |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### getCustomClassifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCustomClassifier(): BidiClassifier!
```

Gets the current custom class classifier used for Bidi class determination.

| Return ||
|---------------------------------------------------------------------------------------------------|--------------------------------------|
| [BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier)! | An instance of class`BidiClassifier` |

**See Also**

- [#setCustomClassifier](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setCustomClassifier(android.icu.text.BidiClassifier)) 

### getCustomizedClass

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCustomizedClass(c: Int): Int
```

Retrieves the Bidi class for a given code point.

If a`BidiClassifier`is defined and returns a value other than`UCharacter.getIntPropertyMaxValue(UProperty.BIDI_CLASS)+1`, that value is used; otherwise the default class determination mechanism is invoked.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The code point to get a Bidi class for. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The Bidi class for the character`c`that is in effect for this`Bidi`instance. |

**See Also**

- [android.icu.text.BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier) 

### getDirection

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDirection(): Byte
```

Get the directionality of the text.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | a value of`LTR`,`RTL`or`MIXED`that indicates if the entire text represented by this object is unidirectional, and which direction, or if it is mixed-directional. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LTR:kotlin.Byte)
- [#RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#RTL:kotlin.Byte)
- [#MIXED](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MIXED:kotlin.Byte) 

### getLength

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLength(): Int
```

Get the length of the text.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The length of the text that the`Bidi`object was created for. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### getLevelAt

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLevelAt(charIndex: Int): Byte
```

Get the level for one character.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------|
| `charIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of a character. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | The level for the character at`charIndex`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if charIndex is not in the range`0<=charIndex<getProcessedLength()` |

**See Also**

- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength()) 

### getLevels

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLevels(): ByteArray!
```

Get an array of levels for each character.

Note that this method may allocate memory under some circumstances, unlike`getLevelAt()`.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | The levels array for the text, or`null`if an error occurs. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### getLogicalIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogicalIndex(visualIndex: Int): Int
```

Get the logical text position from a visual position. If such a mapping is used many times on the same`Bidi`object, then calling`getVisualMap()`is more efficient.

The value returned may be`MAP_NOWHERE`if there is no logical position because the corresponding text character is a Bidi mark inserted in the output by option`OPTION_INSERT_MARKS`.

This is the inverse method to`getVisualIndex()`.

When the visual output is altered by using options of`writeReordered()`such as`INSERT_LRM_FOR_NUMERIC`,`KEEP_BASE_COMBINING`,`OUTPUT_REVERSE`,`REMOVE_BIDI_CONTROLS`, the logical position returned may not be correct. It is advised to use, when possible, reordering options such as [OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int) and [OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------|
| `visualIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the visual position of a character. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of this character in the text. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if`visualIndex`is not in the range`0<=visualIndex<getResultLength()` |

**See Also**

- [#getVisualMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualMap())
- [#getVisualIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualIndex(kotlin.Int))
- [#getResultLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getResultLength())
- [#MAP_NOWHERE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAP_NOWHERE:kotlin.Int)
- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### getLogicalMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogicalMap(): IntArray!
```

Get a logical-to-visual index map (array) for the characters in the`Bidi`(paragraph or line) object.

Some values in the map may be`MAP_NOWHERE`if the corresponding text characters are Bidi controls removed from the visual output by the option`OPTION_REMOVE_CONTROLS`.

When the visual output is altered by using options of`writeReordered()`such as`INSERT_LRM_FOR_NUMERIC`,`KEEP_BASE_COMBINING`,`OUTPUT_REVERSE`,`REMOVE_BIDI_CONTROLS`, the visual positions returned may not be correct. It is advised to use, when possible, reordering options such as [OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int) and [OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int).

Note that in right-to-left runs, this mapping places second surrogates before first ones (which is generally a bad idea) and combining characters before base characters. Use of [writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)), optionally with the [KEEP_BASE_COMBINING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#KEEP_BASE_COMBINING:kotlin.Short) option can be considered instead of using the mapping, in order to avoid these issues.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array of`getProcessedLength()`indexes which will reflect the reordering of the characters. The index map will result in`indexMap[logicalIndex]==visualIndex`, where`indexMap`represents the returned array. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#getVisualMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualMap())
- [#getVisualIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getVisualIndex(kotlin.Int))
- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength())
- [#MAP_NOWHERE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAP_NOWHERE:kotlin.Int)
- [#OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int)
- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### getLogicalRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLogicalRun(logicalPosition: Int): BidiRun!
```

Get a logical run. This method returns information about a run and is used to retrieve runs in logical order.

This is especially useful for line-breaking on a paragraph.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| `logicalPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is a logical position within the source text. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | a BidiRun object filled with`start`containing the first character of the run,`limit`containing the limit of the run, and`embeddingLevel`containing the level of the run. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if logicalPosition is not in the range`0<=logicalPosition<getProcessedLength()` |

**See Also**

- [android.icu.text.BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)
- [android.icu.text.BidiRun#getStart()](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getStart())
- [android.icu.text.BidiRun#getLimit()](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getLimit())
- [android.icu.text.BidiRun#getEmbeddingLevel()](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getEmbeddingLevel()) 

### getParaLevel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParaLevel(): Byte
```

Get the paragraph level of the text.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | The paragraph level. If there are multiple paragraphs, their level may vary if the required paraLevel is LEVEL_DEFAULT_LTR or LEVEL_DEFAULT_RTL. In that case, the level of the first paragraph is returned. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#LEVEL_DEFAULT_LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_LTR:kotlin.Byte)
- [#LEVEL_DEFAULT_RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_RTL:kotlin.Byte)
- [#getParagraph](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraph(kotlin.Int))
- [#getParagraphByIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraphByIndex(kotlin.Int)) 

### getParagraph

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraph(charIndex: Int): BidiRun!
```

Get a paragraph, given a position within the text. This method returns information about a paragraph. 
Note: if the paragraph index is known, it is more efficient to retrieve the paragraph information using getParagraphByIndex().

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `charIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the index of a character within the text, in the range`[0..getProcessedLength()-1]`. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | a BidiRun object with the details of the paragraph: `start`will receive the index of the first character of the paragraph in the text. `limit`will receive the limit of the paragraph. `embeddingLevel`will receive the level of the paragraph. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if charIndex is not within the legal range |

**See Also**

- [android.icu.text.BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)
- [#getParagraphByIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getParagraphByIndex(kotlin.Int))
- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength()) 

### getParagraphByIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraphByIndex(paraIndex: Int): BidiRun!
```

Get a paragraph, given the index of this paragraph. This method returns information about a paragraph.

<br />

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `paraIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the number of the paragraph, in the range`[0..countParagraphs()-1]`. |

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | a BidiRun object with the details of the paragraph: `start`will receive the index of the first character of the paragraph in the text. `limit`will receive the limit of the paragraph. `embeddingLevel`will receive the level of the paragraph. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if paraIndex is not in the range`[0..countParagraphs()-1]` |

**See Also**

- [android.icu.text.BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun) 

### getParagraphIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraphIndex(charIndex: Int): Int
```

Get the index of a paragraph, given a position within the text.

<br />

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `charIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the index of a character within the text, in the range`[0..getProcessedLength()-1]`. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the paragraph containing the specified position, starting from 0. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if charIndex is not within the legal range |

**See Also**

- [android.icu.text.BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)
- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength()) 

### getProcessedLength

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProcessedLength(): Int
```

Get the length of the source text processed by the last call to`setPara()`. This length may be different from the length of the source text if option`OPTION_STREAMING`has been set. 
Note that whenever the length of the text affects the execution or the result of a method, it is the processed length which must be considered, except for`setPara`(which receives unprocessed source text) and`getLength`(which returns the original length of the source text). 
In particular, the processed length is the one to consider in the following cases:

- maximum value of the`limit`argument of`setLine`
- maximum value of the`charIndex`argument of`getParagraph`
- maximum value of the`charIndex`argument of`getLevelAt`
- number of elements in the array returned by`getLevels`
- maximum value of the`logicalStart`argument of`getLogicalRun`
- maximum value of the`logicalIndex`argument of`getVisualIndex`
- number of elements returned by`getLogicalMap`
- length of text processed by`writeReordered`

<br />

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The length of the part of the source text processed by the last call to`setPara`. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#OPTION_STREAMING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_STREAMING:kotlin.Int) 

### getReorderingMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReorderingMode(): Int
```

What is the requested reordering mode for a given Bidi object?

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current reordering mode of the Bidi object |

**See Also**

- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int)) 

### getReorderingOptions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReorderingOptions(): Int
```

What are the reordering options applied to a given Bidi object?

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current reordering options of the Bidi object |

**See Also**

- [#setReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingOptions(kotlin.Int)) 

### getResultLength

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResultLength(): Int
```

Get the length of the reordered text resulting from the last call to`setPara()`. This length may be different from the length of the source text if option`OPTION_INSERT_MARKS`or option`OPTION_REMOVE_CONTROLS`has been set. 
This resulting length is the one to consider in the following cases:

- maximum value of the`visualIndex`argument of`getLogicalIndex`
- number of elements returned by`getVisualMap`

Note that this length stays identical to the source text length if Bidi marks are inserted or removed using option bits of`writeReordered`, or if option`REORDER_INVERSE_NUMBERS_AS_L`has been set.

<br />

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The length of the reordered text resulting from the last call to`setPara`. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int)
- [#REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short) 

### getRunCount

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRunCount(): Int
```

Return the number of level runs.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of level runs |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

### getRunLevel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRunLevel(run: Int): Int
```

Return the level of the nth logical run in this line.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------|
| `run` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the run, between 0 and`countRuns()-1` |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the level of the run |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if`run`is not in the range`0<=run<countRuns()` |

### getRunLimit

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRunLimit(run: Int): Int
```

Return the index of the character past the end of the nth logical run in this line, as an offset from the start of the line. For example, this will return the length of the line for the last run on the line.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `run` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the run, between 0 and`countRuns()` |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the limit of the run |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if`run`is not in the range`0<=run<countRuns()` |

### getRunStart

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRunStart(run: Int): Int
```

Return the index of the character at the start of the nth logical run in this line, as an offset from the start of the line.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `run` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the run, between 0 and`countRuns()` |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the start of the run |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if`run`is not in the range`0<=run<countRuns()` |

### getText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getText(): CharArray!
```

Get the text.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | A`char`array containing the text that the`Bidi`object was created for. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#setLine](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setLine(kotlin.Int,%20kotlin.Int)) 

### getTextAsString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTextAsString(): String!
```

Get the text.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | A`String`containing the text that the`Bidi`object was created for. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#setLine](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setLine(kotlin.Int,%20kotlin.Int)) 

### getVisualIndex

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVisualIndex(logicalIndex: Int): Int
```

Get the visual position from a logical text position. If such a mapping is used many times on the same`Bidi`object, then calling`getLogicalMap()`is more efficient.

The value returned may be`MAP_NOWHERE`if there is no visual position because the corresponding text character is a Bidi control removed from output by the option`OPTION_REMOVE_CONTROLS`.

When the visual output is altered by using options of`writeReordered()`such as`INSERT_LRM_FOR_NUMERIC`,`KEEP_BASE_COMBINING`,`OUTPUT_REVERSE`,`REMOVE_BIDI_CONTROLS`, the visual position returned may not be correct. It is advised to use, when possible, reordering options such as [OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int) and [OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int).

Note that in right-to-left runs, this mapping places second surrogates before first ones (which is generally a bad idea) and combining characters before base characters. Use of [writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)), optionally with the [KEEP_BASE_COMBINING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#KEEP_BASE_COMBINING:kotlin.Short) option can be considered instead of using the mapping, in order to avoid these issues.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------|
| `logicalIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the index of a character in the text. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The visual position of this character. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if`logicalIndex`is not in the range`0<=logicalIndex<getProcessedLength()` |

**See Also**

- [#getLogicalMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalMap())
- [#getLogicalIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalIndex(kotlin.Int))
- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength())
- [#MAP_NOWHERE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAP_NOWHERE:kotlin.Int)
- [#OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int)
- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### getVisualMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVisualMap(): IntArray!
```

Get a visual-to-logical index map (array) for the characters in the`Bidi`(paragraph or line) object.

Some values in the map may be`MAP_NOWHERE`if the corresponding text characters are Bidi marks inserted in the visual output by the option`OPTION_INSERT_MARKS`.

When the visual output is altered by using options of`writeReordered()`such as`INSERT_LRM_FOR_NUMERIC`,`KEEP_BASE_COMBINING`,`OUTPUT_REVERSE`,`REMOVE_BIDI_CONTROLS`, the logical positions returned may not be correct. It is advised to use, when possible, reordering options such as [OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int) and [OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array of`getResultLength()`indexes which will reflect the reordering of the characters. The index map will result in`indexMap[visualIndex]==logicalIndex`, where`indexMap`represents the returned array. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#getLogicalMap](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalMap())
- [#getLogicalIndex](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getLogicalIndex(kotlin.Int))
- [#getResultLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getResultLength())
- [#MAP_NOWHERE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAP_NOWHERE:kotlin.Int)
- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)) 

### getVisualRun

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVisualRun(runIndex: Int): BidiRun!
```

Get a`BidiRun`object according to its index. BidiRun methods may be used to retrieve the run's logical start, length and level, which can be even for an LTR run or odd for an RTL run. In an RTL run, the character at the logical start is visually on the right of the displayed run. The length is the number of characters in the run.

`countRuns()`is normally called before the runs are retrieved.

Example: 

```kotlin
Bidi bidi = new Bidi();
   String text = "abc 123 DEFG xyz";
   bidi.setPara(text, Bidi.RTL, null);
   int i, count=bidi.countRuns(), logicalStart, visualIndex=0, length;
   BidiRun run;
   for (i = 0; i < count; ++i) {
       run = bidi.getVisualRun(i);
       logicalStart = run.getStart();
       length = run.getLength();
       if (Bidi.LTR == run.getEmbeddingLevel()) {
           do { // LTR
               show_char(text.charAt(logicalStart++), visualIndex++);
           } while (--length > 0);
       } else {
           logicalStart += length;  // logicalLimit
           do { // RTL
               show_char(text.charAt(--logicalStart), visualIndex++);
           } while (--length > 0);
       }
   }
  
```

Note that in right-to-left runs, code like this places second surrogates before first ones (which is generally a bad idea) and combining characters before base characters.

Use of [writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int)), optionally with the [KEEP_BASE_COMBINING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#KEEP_BASE_COMBINING:kotlin.Short) option, can be considered in order to avoid these issues.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `runIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the number of the run in visual order, in the range`[0..countRuns()-1]`. |

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)! | a BidiRun object containing the details of the run. The directionality of the run is`LTR==0`or`RTL==1`, never`MIXED`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |
| `java.lang.IllegalArgumentException` | if`runIndex`is not in the range`0<=runIndex<countRuns()` |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/Bidi#countRuns()>
- [android.icu.text.BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun)
- [android.icu.text.BidiRun#getStart()](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getStart())
- [android.icu.text.BidiRun#getLength()](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getLength())
- [android.icu.text.BidiRun#getEmbeddingLevel()](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun#getEmbeddingLevel()) 

### invertMap

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun invertMap(srcMap: IntArray!): IntArray!
```

Invert an index map. The index mapping of the argument map is inverted and returned as an array of indexes that we will call the inverse map.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcMap` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:is an array whose elements define the original mapping from a source array to a destination array. Some elements of the source array may have no mapping in the destination array. In that case, their value will be the special value`MAP_NOWHERE`. All elements must be \>=0 or equal to`MAP_NOWHERE`. Some elements in the source map may have a value greater than the srcMap.length if the destination array has more elements than the source array. There must be no duplicate indexes (two or more elements with the same value except`MAP_NOWHERE`). |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array representing the inverse map. This array has a number of elements equal to 1 + the highest value in`srcMap`. For elements of the result array which have no matching elements in the source array, the corresponding elements in the inverse map will receive a value equal to`MAP_NOWHERE`. If element with index i in`srcMap`has a value k different from`MAP_NOWHERE`, this means that element i of the source array maps to element k in the destination array. The inverse map will have value i in its k-th element. For all elements of the destination array which do not map to an element in the source array, the corresponding element in the inverse map will have a value equal to`MAP_NOWHERE`. |

**See Also**

- [#MAP_NOWHERE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAP_NOWHERE:kotlin.Int) 

### isInverse

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInverse(): Boolean
```

Is this`Bidi`object set to perform the inverse Bidi algorithm?

Note: calling this method after setting the reordering mode with`setReorderingMode`will return`true`if the reordering mode was set to`REORDER_INVERSE_NUMBERS_AS_L`,`false`for all other values.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the`Bidi`object is set to perform the inverse Bidi algorithm by handling numbers as L. |

**See Also**

- [#setInverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setInverse(kotlin.Boolean))
- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))
- [#REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short) 

### isLeftToRight

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLeftToRight(): Boolean
```

Return true if the line is all left-to-right text and the base direction is left-to-right.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the line is all left-to-right text and the base direction is left-to-right. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara` |

### isMixed

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMixed(): Boolean
```

Return true if the line is not left-to-right or right-to-left. This means it either has mixed runs of left-to-right and right-to-left text, or the base direction differs from the direction of the only run of text.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the line is not left-to-right or right-to-left. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara` |

### isOrderParagraphsLTR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOrderParagraphsLTR(): Boolean
```

Is this`Bidi`object set to allocate level 0 to block separators so that successive paragraphs progress from left to right?

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the`Bidi`object is set to allocate level 0 to block separators. |

### isRightToLeft

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRightToLeft(): Boolean
```

Return true if the line is all right-to-left text, and the base direction is right-to-left

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the line is all right-to-left text, and the base direction is right-to-left |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara` |

### orderParagraphsLTR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun orderParagraphsLTR(ordarParaLTR: Boolean): Unit
```

Specify whether block separators must be allocated level zero, so that successive paragraphs will progress from left to right. This method must be called before`setPara()`. Paragraph separators (B) may appear in the text. Setting them to level zero means that all paragraph separators (including one possibly appearing in the last text position) are kept in the reordered text after the text that they follow in the source text. When this feature is not enabled, a paragraph separator at the last position of the text before reordering will go to the first position of the reordered text when the paragraph level is odd.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ordarParaLTR` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):specifies whether paragraph separators (B) must receive level 0, so that successive paragraphs progress from left to right. |

**See Also**

### reorderLogical

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun reorderLogical(levels: ByteArray!): IntArray!
```

This is a convenience method that does not use a`Bidi`object. It is intended to be used for when an application has determined the levels of objects (character sequences) and just needs to have them reordered (L2). This is equivalent to using`getLogicalMap()`on a`Bidi`object.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `levels` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:is an array of levels that have been determined by the application. |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array of`levels.length`indexes which will reflect the reordering of the characters. The index map will result in`indexMap[logicalIndex]==visualIndex`, where`indexMap`represents the returned array. |

### reorderVisual

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun reorderVisual(levels: ByteArray!): IntArray!
```

This is a convenience method that does not use a`Bidi`object. It is intended to be used for when an application has determined the levels of objects (character sequences) and just needs to have them reordered (L2). This is equivalent to using`getVisualMap()`on a`Bidi`object.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `levels` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:is an array of levels that have been determined by the application. |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | an array of`levels.length`indexes which will reflect the reordering of the characters. The index map will result in`indexMap[visualIndex]==logicalIndex`, where`indexMap`represents the returned array. |

### reorderVisually

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun reorderVisually(
    levels: ByteArray!, 
    levelStart: Int, 
    objects: Array<Any!>!, 
    objectStart: Int, 
    count: Int
): Unit
```

Reorder the objects in the array into visual order based on their levels. This is a utility method to use when you have a collection of objects representing runs of text in logical order, each run containing text at a single level. The elements at`index`from`objectStart`up to`objectStart + count`in the objects array will be reordered into visual order assuming each run of text has the level indicated by the corresponding element in the levels array (at`index - objectStart + levelStart`).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `levels` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:an array representing the bidi level of each object |
| `levelStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start position in the levels array |
| `objects` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:the array of objects to be reordered into visual order |
| `objectStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start position in the objects array |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of objects to reorder |

### requiresBidi

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun requiresBidi(
    text: CharArray!, 
    start: Int, 
    limit: Int
): Boolean
```

Return true if the specified text requires bidi analysis. If this returns false, the text will display left-to-right. Clients can then avoid constructing a Bidi object. Text in the Arabic Presentation Forms area of Unicode is presumed to already be shaped and ordered for display, and so will not cause this method to return true.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:the text containing the characters to test |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the range of characters to test |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the limit of the range of characters to test |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the range of characters requires bidi analysis |

### setContext

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(
    prologue: String!, 
    epilogue: String!
): Unit
```

Set the context before a call to setPara().

setPara() computes the left-right directionality for a given piece of text which is supplied as one of its arguments. Sometimes this piece of text (the "main text") should be considered in context, because text appearing before ("prologue") and/or after ("epilogue") the main text may affect the result of this computation.

This function specifies the prologue and/or the epilogue for the next call to setPara(). If successive calls to setPara() all need specification of a context, setContext() must be called before each call to setPara(). In other words, a context is not "remembered" after the following successful call to setPara().

If a call to setPara() specifies DEFAULT_LTR or DEFAULT_RTL as paraLevel and is preceded by a call to setContext() which specifies a prologue, the paragraph level will be computed taking in consideration the text in the prologue.

When setPara() is called without a previous call to setContext, the main text is handled as if preceded and followed by strong directional characters at the current paragraph level. Calling setContext() with specification of a prologue will change this behavior by handling the main text as if preceded by the last strong character appearing in the prologue, if any. Calling setContext() with specification of an epilogue will change the behavior of setPara() by handling the main text as if followed by the first strong character or digit appearing in the epilogue, if any.

Note 1: if`setContext`is called repeatedly without calling`setPara`, the earlier calls have no effect, only the last call will be remembered for the next call to`setPara`.

Note 2: calling`setContext(null, null)`cancels any previous setting of non-empty prologue or epilogue. The next call to`setPara()`will process no prologue or epilogue.

Note 3: users must be aware that even after setting the context before a call to setPara() to perform e.g. a logical to visual transformation, the resulting string may not be identical to what it would have been if all the text, including prologue and epilogue, had been processed together. 
Example (upper case letters represent RTL characters): 
prologue = "`abc DE`" 
epilogue = none 
main text = "`FGH xyz`" 
paraLevel = LTR 
display without prologue = "`HGF xyz`" ("HGF" is adjacent to "xyz") 
display with prologue = "`abc HGFED xyz`" ("HGF" is not adjacent to "xyz") 

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `prologue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:is the text which precedes the text that will be specified in a coming call to setPara(). If there is no prologue to consider, this parameter can be`null`. |
| `epilogue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:is the text which follows the text that will be specified in a coming call to setPara(). If there is no epilogue to consider, this parameter can be`null`. |

**See Also**

### setCustomClassifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCustomClassifier(classifier: BidiClassifier!): Unit
```

Set a custom Bidi classifier used by the UBA implementation for Bidi class determination.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `classifier` | [BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier)!:A new custom classifier. This can be null. |

**See Also**

- [#getCustomClassifier](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getCustomClassifier()) 

### setInverse

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInverse(isInverse: Boolean): Unit
```

Modify the operation of the Bidi algorithm such that it approximates an "inverse Bidi" algorithm. This method must be called before`setPara()`.

The normal operation of the Bidi algorithm as described in the Unicode Technical Report is to take text stored in logical (keyboard, typing) order and to determine the reordering of it for visual rendering. Some legacy systems store text in visual order, and for operations with standard, Unicode-based algorithms, the text needs to be transformed to logical order. This is effectively the inverse algorithm of the described Bidi algorithm. Note that there is no standard algorithm for this "inverse Bidi" and that the current implementation provides only an approximation of "inverse Bidi".

With`isInversed`set to`true`, this method changes the behavior of some of the subsequent methods in a way that they can be used for the inverse Bidi algorithm. Specifically, runs of text with numeric characters will be treated in a special way and may need to be surrounded with LRM characters when they are written in reordered sequence.

Output runs should be retrieved using`getVisualRun()`. Since the actual input for "inverse Bidi" is visually ordered text and`getVisualRun()`gets the reordered runs, these are actually the runs of the logically ordered output.

Calling this method with argument`isInverse`set to`true`is equivalent to calling`setReorderingMode`with argument`reorderingMode`set to`REORDER_INVERSE_NUMBERS_AS_L`. 
Calling this method with argument`isInverse`set to`false`is equivalent to calling`setReorderingMode`with argument`reorderingMode`set to`REORDER_DEFAULT`.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `isInverse` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):specifies "forward" or "inverse" Bidi operation. |

**See Also**

- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int))
- [#setReorderingMode](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setReorderingMode(kotlin.Int))
- [#REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short)
- [#REORDER_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_DEFAULT:kotlin.Short) 

### setLine

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLine(
    start: Int, 
    limit: Int
): Bidi!
```

`setLine()`returns a`Bidi`object to contain the reordering information, especially the resolved levels, for all the characters in a line of text. This line of text is specified by referring to a`Bidi`object representing this information for a piece of text containing one or more paragraphs, and by specifying a range of indexes in this text.

In the new line object, the indexes will range from 0 to`limit-start-1`.

This is used after calling`setPara()`for a piece of text, and after line-breaking on that text. It is not necessary if each paragraph is treated as a single line.

After line-breaking, rules (L1) and (L2) for the treatment of trailing WS and for reordering are performed on a`Bidi`object that represents a line.

**Important:** the line`Bidi`object may reference data within the global text`Bidi`object. You should not alter the content of the global text object until you are finished using the line object.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the line's first index into the text. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is just behind the line's last index into the text (its last index +1). |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#)! | a`Bidi`object that will now represent a line of the text. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara` |
| `java.lang.IllegalArgumentException` | if start and limit are not in the range`0<=start<limit<=getProcessedLength()`, or if the specified line crosses a paragraph boundary |

**See Also**

- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength()) 

### setPara

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPara(
    chars: CharArray!, 
    paraLevel: Byte, 
    embeddingLevels: ByteArray!
): Unit
```

Perform the Unicode Bidi algorithm. It is defined in the [Unicode Standard Annex #9](http://www.unicode.org/reports/tr9/).

This method takes a piece of plain text containing one or more paragraphs, with or without externally specified embedding levels from*styled*text and computes the left-right-directionality of each character.

If the entire text is all of the same directionality, then the method may not perform all the steps described by the algorithm, i.e., some levels may not be the same as if all steps were performed. This is not relevant for unidirectional text. 
For example, in pure LTR text with numbers the numbers would get a resolved level of 2 higher than the surrounding text according to the algorithm. This implementation may set all resolved levels to the same value in such a case.

The text can be composed of multiple paragraphs. Occurrence of a block separator in the text terminates a paragraph, and whatever comes next starts a new paragraph. The exception to this rule is when a Carriage Return (CR) is followed by a Line Feed (LF). Both CR and LF are block separators, but in that case, the pair of characters is considered as terminating the preceding paragraph, and a new paragraph will be started by a character coming after the LF.

The text is stored internally as an array of characters. Therefore the documentation will refer to indexes of the characters in the text.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:contains the text that the Bidi algorithm will be performed on. This text can be retrieved with`getText()`or`getTextAsString`. |
| `paraLevel` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):specifies the default level for the text; it is typically 0 (LTR) or 1 (RTL). If the method shall determine the paragraph level from the text, then`paraLevel`can be set to either`LEVEL_DEFAULT_LTR`or`LEVEL_DEFAULT_RTL`; if the text contains multiple paragraphs, the paragraph level shall be determined separately for each paragraph; if a paragraph does not include any strongly typed character, then the desired default is used (0 for LTR or 1 for RTL). Any other value between 0 and`MAX_EXPLICIT_LEVEL`is also valid, with odd levels indicating RTL. |
| `embeddingLevels` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:(in) may be used to preset the embedding and override levels, ignoring characters like LRE and PDF in the text. A level overrides the directional property of its corresponding (same index) character if the level has the`LEVEL_OVERRIDE`bit set. Aside from that bit, it must be`paraLevel<=embeddingLevels[]<=MAX_EXPLICIT_LEVEL`, except that level 0 is always allowed. Level 0 for a paragraph separator prevents reordering of paragraphs; this only works reliably if`LEVEL_OVERRIDE`is also set for paragraph separators. Level 0 for other characters is treated as a wildcard and is lifted up to the resolved level of the surrounding paragraph. **Caution:** A reference to this array, not a copy of the levels, will be stored in the`Bidi`object; the`embeddingLevels`should not be modified to avoid unexpected results on subsequent Bidi operations. However, the`setPara()`and`setLine()`methods may modify some or all of the levels. **Note:** the`embeddingLevels`array must have one entry for each character in`text`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the values in embeddingLevels are not within the allowed range |

**See Also**

- [#LEVEL_DEFAULT_LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_LTR:kotlin.Byte)
- [#LEVEL_DEFAULT_RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_RTL:kotlin.Byte)
- [#LEVEL_OVERRIDE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_OVERRIDE:kotlin.Byte)
- [#MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte) 

### setPara

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPara(
    text: String!, 
    paraLevel: Byte, 
    embeddingLevels: ByteArray!
): Unit
```

Perform the Unicode Bidi algorithm. It is defined in the [Unicode Standard Annex #9](http://www.unicode.org/reports/tr9/).

This method takes a piece of plain text containing one or more paragraphs, with or without externally specified embedding levels from*styled*text and computes the left-right-directionality of each character.

If the entire text is all of the same directionality, then the method may not perform all the steps described by the algorithm, i.e., some levels may not be the same as if all steps were performed. This is not relevant for unidirectional text. 
For example, in pure LTR text with numbers the numbers would get a resolved level of 2 higher than the surrounding text according to the algorithm. This implementation may set all resolved levels to the same value in such a case.

The text can be composed of multiple paragraphs. Occurrence of a block separator in the text terminates a paragraph, and whatever comes next starts a new paragraph. The exception to this rule is when a Carriage Return (CR) is followed by a Line Feed (LF). Both CR and LF are block separators, but in that case, the pair of characters is considered as terminating the preceding paragraph, and a new paragraph will be started by a character coming after the LF.

Although the text is passed here as a`String`, it is stored internally as an array of characters. Therefore the documentation will refer to indexes of the characters in the text.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:contains the text that the Bidi algorithm will be performed on. This text can be retrieved with`getText()`or`getTextAsString`. |
| `paraLevel` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):specifies the default level for the text; it is typically 0 (LTR) or 1 (RTL). If the method shall determine the paragraph level from the text, then`paraLevel`can be set to either`LEVEL_DEFAULT_LTR`or`LEVEL_DEFAULT_RTL`; if the text contains multiple paragraphs, the paragraph level shall be determined separately for each paragraph; if a paragraph does not include any strongly typed character, then the desired default is used (0 for LTR or 1 for RTL). Any other value between 0 and`MAX_EXPLICIT_LEVEL`is also valid, with odd levels indicating RTL. |
| `embeddingLevels` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:(in) may be used to preset the embedding and override levels, ignoring characters like LRE and PDF in the text. A level overrides the directional property of its corresponding (same index) character if the level has the`LEVEL_OVERRIDE`bit set. Aside from that bit, it must be`paraLevel<=embeddingLevels[]<=MAX_EXPLICIT_LEVEL`, except that level 0 is always allowed. Level 0 for a paragraph separator prevents reordering of paragraphs; this only works reliably if`LEVEL_OVERRIDE`is also set for paragraph separators. Level 0 for other characters is treated as a wildcard and is lifted up to the resolved level of the surrounding paragraph. **Caution:** A reference to this array, not a copy of the levels, will be stored in the`Bidi`object; the`embeddingLevels`should not be modified to avoid unexpected results on subsequent Bidi operations. However, the`setPara()`and`setLine()`methods may modify some or all of the levels. **Note:** the`embeddingLevels`array must have one entry for each character in`text`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the values in embeddingLevels are not within the allowed range |

**See Also**

- [#LEVEL_DEFAULT_LTR](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_LTR:kotlin.Byte)
- [#LEVEL_DEFAULT_RTL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_DEFAULT_RTL:kotlin.Byte)
- [#LEVEL_OVERRIDE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#LEVEL_OVERRIDE:kotlin.Byte)
- [#MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte) 

### setPara

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPara(paragraph: AttributedCharacterIterator!): Unit
```

Perform the Unicode Bidi algorithm on a given paragraph, as defined in the [Unicode Standard Annex #9](https://www.unicode.org/reports/tr9/), version 13, also described in The Unicode Standard, Version 4.0 .

This method takes a paragraph of text and computes the left-right-directionality of each character. The text should not contain any Unicode block separators.

The RUN_DIRECTION attribute in the text, if present, determines the base direction (left-to-right or right-to-left). If not present, the base direction is computed using the Unicode Bidirectional Algorithm, defaulting to left-to-right if there are no strong directional characters in the text. This attribute, if present, must be applied to all the text in the paragraph.

The BIDI_EMBEDDING attribute in the text, if present, represents embedding level information. Negative values indicate overrides at the absolute value of the level. Positive values indicate embeddings. (See [MAX_EXPLICIT_LEVEL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#MAX_EXPLICIT_LEVEL:kotlin.Byte).) Where values are zero or not defined, the base embedding level as determined by the base direction is assumed.

The NUMERIC_SHAPING attribute in the text, if present, converts European digits to other decimal digits before running the bidi algorithm. This attribute, if present, must be applied to all the text in the paragraph. If the entire text is all of the same directionality, then the method may not perform all the steps described by the algorithm, i.e., some levels may not be the same as if all steps were performed. This is not relevant for unidirectional text. 
For example, in pure LTR text with numbers the numbers would get a resolved level of 2 higher than the surrounding text according to the algorithm. This implementation may set all resolved levels to the same value in such a case.

<br />

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `paragraph` | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#)!:a paragraph of text with optional character and paragraph attribute information |

### setReorderingMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReorderingMode(reorderingMode: Int): Unit
```

Modify the operation of the Bidi algorithm such that it implements some variant to the basic Bidi algorithm or approximates an "inverse Bidi" algorithm, depending on different values of the "reordering mode". This method must be called before`setPara()`, and stays in effect until called again with a different argument.

The normal operation of the Bidi algorithm as described in the Unicode Standard Annex #9 is to take text stored in logical (keyboard, typing) order and to determine how to reorder it for visual rendering.

With the reordering mode set to a value other than`REORDER_DEFAULT`, this method changes the behavior of some of the subsequent methods in a way such that they implement an inverse Bidi algorithm or some other algorithm variants.

Some legacy systems store text in visual order, and for operations with standard, Unicode-based algorithms, the text needs to be transformed into logical order. This is effectively the inverse algorithm of the described Bidi algorithm. Note that there is no standard algorithm for this "inverse Bidi", so a number of variants are implemented here.

In other cases, it may be desirable to emulate some variant of the Logical to Visual algorithm (e.g. one used in MS Windows), or perform a Logical to Logical transformation.

- When the Reordering Mode is set to`REORDER_DEFAULT`, the standard Bidi Logical to Visual algorithm is applied.
- When the reordering mode is set to`REORDER_NUMBERS_SPECIAL`, the algorithm used to perform Bidi transformations when calling`setPara`should approximate the algorithm used in Microsoft Windows XP rather than strictly conform to the Unicode Bidi algorithm. 
 The differences between the basic algorithm and the algorithm addressed by this option are as follows:
 - Within text at an even embedding level, the sequence "123AB" (where AB represent R or AL letters) is transformed to "123BA" by the Unicode algorithm and to "BA123" by the Windows algorithm.
 - Arabic-Indic numbers (AN) are handled by the Windows algorithm just like regular numbers (EN).
- When the reordering mode is set to`REORDER_GROUP_NUMBERS_WITH_R`, numbers located between LTR text and RTL text are associated with the RTL text. For instance, an LTR paragraph with content "abc 123 DEF" (where upper case letters represent RTL characters) will be transformed to "abc FED 123" (and not "abc 123 FED"), "DEF 123 abc" will be transformed to "123 FED abc" and "123 FED abc" will be transformed to "DEF 123 abc". This makes the algorithm reversible and makes it useful when round trip (from visual to logical and back to visual) must be achieved without adding LRM characters. However, this is a variation from the standard Unicode Bidi algorithm. 
 The source text should not contain Bidi control characters other than LRM or RLM.
- When the reordering mode is set to`REORDER_RUNS_ONLY`, a "Logical to Logical" transformation must be performed:
 - If the default text level of the source text (argument`paraLevel`in`setPara`) is even, the source text will be handled as LTR logical text and will be transformed to the RTL logical text which has the same LTR visual display.
 - If the default level of the source text is odd, the source text will be handled as RTL logical text and will be transformed to the LTR logical text which has the same LTR visual display.

 This mode may be needed when logical text which is basically Arabic or Hebrew, with possible included numbers or phrases in English, has to be displayed as if it had an even embedding level (this can happen if the displaying application treats all text as if it was basically LTR). 
 This mode may also be needed in the reverse case, when logical text which is basically English, with possible included phrases in Arabic or Hebrew, has to be displayed as if it had an odd embedding level. 
 Both cases could be handled by adding LRE or RLE at the head of the text, if the display subsystem supports these formatting controls. If it does not, the problem may be handled by transforming the source text in this mode before displaying it, so that it will be displayed properly. 
 The source text should not contain Bidi control characters other than LRM or RLM.
- When the reordering mode is set to`REORDER_INVERSE_NUMBERS_AS_L`, an "inverse Bidi" algorithm is applied. Runs of text with numeric characters will be treated like LTR letters and may need to be surrounded with LRM characters when they are written in reordered sequence (the option`INSERT_LRM_FOR_NUMERIC`can be used with method`writeReordered`to this end. This mode is equivalent to calling`setInverse()`with argument`isInverse`set to`true`.
- When the reordering mode is set to`REORDER_INVERSE_LIKE_DIRECT`, the "direct" Logical to Visual Bidi algorithm is used as an approximation of an "inverse Bidi" algorithm. This mode is similar to mode`REORDER_INVERSE_NUMBERS_AS_L`but is closer to the regular Bidi algorithm. 
 For example, an LTR paragraph with the content "FED 123 456 CBA" (where upper case represents RTL characters) will be transformed to "ABC 456 123 DEF", as opposed to "DEF 123 456 ABC" with mode`REORDER_INVERSE_NUMBERS_AS_L`. 
 When used in conjunction with option`OPTION_INSERT_MARKS`, this mode generally adds Bidi marks to the output significantly more sparingly than mode`REORDER_INVERSE_NUMBERS_AS_L`. 
 with option`INSERT_LRM_FOR_NUMERIC`in calls to`writeReordered`.
- When the reordering mode is set to`REORDER_INVERSE_FOR_NUMBERS_SPECIAL`, the Logical to Visual Bidi algorithm used in Windows XP is used as an approximation of an "inverse Bidi" algorithm. 
 For example, an LTR paragraph with the content "abc FED123" (where upper case represents RTL characters) will be transformed to "abc 123DEF.

In all the reordering modes specifying an "inverse Bidi" algorithm (i.e. those with a name starting with`REORDER_INVERSE`), output runs should be retrieved using`getVisualRun()`, and the output text with`writeReordered()`. The caller should keep in mind that in "inverse Bidi" modes the input is actually visually ordered text and reordered output returned by`getVisualRun()`or`writeReordered()`are actually runs or character string of logically ordered output. 
For all the "inverse Bidi" modes, the source text should not contain Bidi control characters other than LRM or RLM.

Note that option`OUTPUT_REVERSE`of`writeReordered`has no useful meaning and should not be used in conjunction with any value of the reordering mode specifying "inverse Bidi" or with value`REORDER_RUNS_ONLY`.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `reorderingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):specifies the required variant of the Bidi algorithm. |

**See Also**

- [#setInverse](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#setInverse(kotlin.Boolean))
- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int))
- [#INSERT_LRM_FOR_NUMERIC](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#INSERT_LRM_FOR_NUMERIC:kotlin.Short)
- [#OUTPUT_REVERSE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OUTPUT_REVERSE:kotlin.Short)
- [#REORDER_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_DEFAULT:kotlin.Short)
- [#REORDER_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_NUMBERS_SPECIAL:kotlin.Short)
- [#REORDER_GROUP_NUMBERS_WITH_R](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_GROUP_NUMBERS_WITH_R:kotlin.Short)
- [#REORDER_RUNS_ONLY](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_RUNS_ONLY:kotlin.Short)
- [#REORDER_INVERSE_NUMBERS_AS_L](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_NUMBERS_AS_L:kotlin.Short)
- [#REORDER_INVERSE_LIKE_DIRECT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_LIKE_DIRECT:kotlin.Short)
- [#REORDER_INVERSE_FOR_NUMBERS_SPECIAL](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REORDER_INVERSE_FOR_NUMBERS_SPECIAL:kotlin.Short) 

### setReorderingOptions

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReorderingOptions(options: Int): Unit
```

Specify which of the reordering options should be applied during Bidi transformations.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of zero or more of the following reordering options:`OPTION_DEFAULT`,`OPTION_INSERT_MARKS`,`OPTION_REMOVE_CONTROLS`,`OPTION_STREAMING`. |

**See Also**

- [#getReorderingOptions](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getReorderingOptions())
- [#OPTION_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_DEFAULT:kotlin.Int)
- [#OPTION_INSERT_MARKS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_INSERT_MARKS:kotlin.Int)
- [#OPTION_REMOVE_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_REMOVE_CONTROLS:kotlin.Int)
- [#OPTION_STREAMING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_STREAMING:kotlin.Int) 

### writeReordered

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeReordered(options: Int): String!
```

Take a`Bidi`object containing the reordering information for a piece of text (one or more paragraphs) set by`setPara()`or for a line of text set by`setLine()`and return a string containing the reordered text.

The text may have been aliased (only a reference was stored without copying the contents), thus it must not have been modified since the`setPara()`call. This method preserves the integrity of characters with multiple code units and (optionally) combining characters. Characters in RTL runs can be replaced by mirror-image characters in the returned string. Note that "real" mirroring has to be done in a rendering engine by glyph selection and that for many "mirrored" characters there are no Unicode characters as mirror-image equivalents. There are also options to insert or remove Bidi control characters; see the descriptions of the return value and the`options`parameter, and of the option bit flags.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options for the reordering that control how the reordered text is written. The options include mirroring the characters on a code point basis and inserting LRM characters, which is used especially for transforming visually stored text to logically stored text (although this is still an imperfect implementation of an "inverse Bidi" algorithm because it uses the "forward Bidi" algorithm at its core). The available options are:`DO_MIRRORING`,`INSERT_LRM_FOR_NUMERIC`,`KEEP_BASE_COMBINING`,`OUTPUT_REVERSE`,`REMOVE_BIDI_CONTROLS`,`STREAMING` |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The reordered text. If the`INSERT_LRM_FOR_NUMERIC`option is set, then the length of the returned string could be as large as`getLength()+2*countRuns()`. If the`REMOVE_BIDI_CONTROLS`option is set, then the length of the returned string may be less than`getLength()`. If none of these options is set, then the length of the returned string will be exactly`getProcessedLength()`. |

| Exceptions ||
|-----------------------------------|--------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this call is not preceded by a successful call to`setPara`or`setLine` |

**See Also**

- [#DO_MIRRORING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#DO_MIRRORING:kotlin.Short)
- [#INSERT_LRM_FOR_NUMERIC](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#INSERT_LRM_FOR_NUMERIC:kotlin.Short)
- [#KEEP_BASE_COMBINING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#KEEP_BASE_COMBINING:kotlin.Short)
- [#OUTPUT_REVERSE](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OUTPUT_REVERSE:kotlin.Short)
- [#REMOVE_BIDI_CONTROLS](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#REMOVE_BIDI_CONTROLS:kotlin.Short)
- [#OPTION_STREAMING](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#OPTION_STREAMING:kotlin.Int)
- [#getProcessedLength](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#getProcessedLength()) 

### writeReverse

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun writeReverse(
    src: String!, 
    options: Int
): String!
```

Reverse a Right-To-Left run of Unicode text. This method preserves the integrity of characters with multiple code units and (optionally) combining characters. Characters can be replaced by mirror-image characters in the destination buffer. Note that "real" mirroring has to be done in a rendering engine by glyph selection and that for many "mirrored" characters there are no Unicode characters as mirror-image equivalents. There are also options to insert or remove Bidi control characters. This method is the implementation for reversing RTL runs as part of`writeReordered()`. For detailed descriptions of the parameters, see there. Since no Bidi controls are inserted here, the output string length will never exceed`src.length()`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The RTL run text. |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options for the reordering that control how the reordered text is written. See the`options`parameter in`writeReordered()`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The reordered text. If the`REMOVE_BIDI_CONTROLS`option is set, then the length of the returned string may be less than`src.length()`. If this option is not set, then the length of the returned string will be exactly`src.length()`. |

| Exceptions ||
|--------------------------------------|-----------------|
| `java.lang.IllegalArgumentException` | if`src`is null. |

**See Also**

- [#writeReordered](https://developer.android.com/reference/kotlin/android/icu/text/Bidi#writeReordered(kotlin.Int))

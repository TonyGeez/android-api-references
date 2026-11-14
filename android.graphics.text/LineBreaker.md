Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineBreaker

```
open class LineBreaker
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.text.LineBreaker](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#) |

Provides automatic line breaking for a *single* paragraph.

```kotlin
<code>
  Paint paint = new Paint();
  Paint bigPaint = new Paint();
  bigPaint.setTextSize(paint.getTextSize() * 2.0);
  String text = "Hello, Android.";
 
  // Prepare the measured text
  MeasuredText mt = new MeasuredText.Builder(text.toCharArray())
      .appendStyleRun(paint, 7, false)  // Use paint for "Hello, "
      .appednStyleRun(bigPaint, 8, false)  // Use bigPaint for "Hello, "
      .build();
 
  LineBreaker lb = new LineBreaker.Builder()
      // Use simple line breaker
      .setBreakStrategy(LineBreaker.BREAK_STRATEGY_SIMPLE)
      // Do not add hyphenation.
      .setHyphenationFrequency(LineBreaker.HYPHENATION_FREQUENCY_NONE)
      // Build the LineBreaker
      .build();
 
  ParagraphConstraints c = new ParagraphConstraints();
  c.setWidth(240);  // Set the line wieth as 1024px
 
  // Do the line breaking
  Result r = lb.computeLineBreaks(mt, c, 0);
 
  // Compute the total height of the text.
  float totalHeight = 0;
  for (int i = 0; i &lt; r.getLineCount(); ++i) {  // iterate over the lines
     totalHeight += r.getLineDescent(i) - r.getLineAscent(i);
  }
 
  // Draw text to the canvas
  Bitmap bmp = Bitmap.createBitmap(240, totalHeight, Bitmap.Config.ARGB_8888);
  Canvas c = new Canvas(bmp);
  float yOffset = 0f;
  int prevOffset = 0;
  for (int i = 0; i &lt; r.getLineCount(); ++i) {  // iterate over the lines
      int nextOffset = r.getLineBreakOffset(i);
      c.drawText(text, prevOffset, nextOffset, 0f, yOffset, paint);
 
      prevOffset = nextOffset;
      yOffset += r.getLineDescent(i) - r.getLineAscent(i);
  }
  </code>
```

<br />

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.Builder` Helper class for creating a `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#`. |
| open | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.ParagraphConstraints` Line breaking constraints for single paragraph. |
| open | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.Result` Holds the result of the `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#computeLineBreaks(android.graphics.text.MeasuredText,%20android.graphics.text.LineBreaker.ParagraphConstraints,%20kotlin.Int)`. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#BREAK_STRATEGY_BALANCED:kotlin.Int` Value for break strategy indicating balanced line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#BREAK_STRATEGY_HIGH_QUALITY:kotlin.Int` Value for break strategy indicating high quality line breaking. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#BREAK_STRATEGY_SIMPLE:kotlin.Int` Value for break strategy indicating simple line breaking. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#HYPHENATION_FREQUENCY_FULL:kotlin.Int` Value for hyphenation frequency indicating the full amount of automatic hyphenation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#HYPHENATION_FREQUENCY_NONE:kotlin.Int` Value for hyphenation frequency indicating no automatic hyphenation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#HYPHENATION_FREQUENCY_NORMAL:kotlin.Int` Value for hyphenation frequency indicating a light amount of automatic hyphenation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#JUSTIFICATION_MODE_INTER_CHARACTER:kotlin.Int` Value for justification mode indicating the text is justified by stretching letter spacing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#JUSTIFICATION_MODE_INTER_WORD:kotlin.Int` Value for justification mode indicating the text is justified by stretching word spacing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#JUSTIFICATION_MODE_NONE:kotlin.Int` Value for justification mode indicating no justification. |
| --- | --- |

| Public methods ||
|---|---|
| open [LineBreaker.Result](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.Result) | `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker#computeLineBreaks(android.graphics.text.MeasuredText,%20android.graphics.text.LineBreaker.ParagraphConstraints,%20kotlin.Int)(measuredPara: https://developer.android.com/reference/kotlin/android/graphics/text/MeasuredText, constraints: https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.ParagraphConstraints, lineNumber: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Break paragraph into lines. |

## Constants

### BREAK_STRATEGY_BALANCED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BREAK_STRATEGY_BALANCED: Int
```

Value for break strategy indicating balanced line breaking. The line breaker does whole-paragraph optimization for making all lines similar length, and also applies automatic hyphenation when required. This break strategy is good for small screen devices such as watch screens.

 Value: 2

### BREAK_STRATEGY_HIGH_QUALITY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BREAK_STRATEGY_HIGH_QUALITY: Int
```

Value for break strategy indicating high quality line breaking. With this option line breaker does whole-paragraph optimization for more readable text, and also applies automatic hyphenation when required.

 Value: 1

### BREAK_STRATEGY_SIMPLE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BREAK_STRATEGY_SIMPLE: Int
```

Value for break strategy indicating simple line breaking. The line breaker puts words to the line as much as possible and breaks line if no more words can fit into the same line. Automatic hyphens are only added when a line has a single word and that word is longer than line width. This is the fastest break strategy and ideal for editor.

 Value: 0

### HYPHENATION_FREQUENCY_FULL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HYPHENATION_FREQUENCY_FULL: Int
```

Value for hyphenation frequency indicating the full amount of automatic hyphenation. This hyphenation frequency is useful for running text and where it's important to put the maximum amount of text in a screen with limited space.

 Value: 2

### HYPHENATION_FREQUENCY_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HYPHENATION_FREQUENCY_NONE: Int
```

Value for hyphenation frequency indicating no automatic hyphenation. Using this option disables auto hyphenation which results in better text layout performance. A word may be broken without hyphens when a line has a single word and that word is longer than line width. Soft hyphens are ignored and will not be used as suggestions for potential line breaks.

 Value: 0

### HYPHENATION_FREQUENCY_NORMAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HYPHENATION_FREQUENCY_NORMAL: Int
```

Value for hyphenation frequency indicating a light amount of automatic hyphenation. This hyphenation frequency is useful for informal cases, such as short sentences or chat messages.

 Value: 1

### JUSTIFICATION_MODE_INTER_CHARACTER

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JUSTIFICATION_MODE_INTER_CHARACTER: Int
```

Value for justification mode indicating the text is justified by stretching letter spacing.

 Value: 2

### JUSTIFICATION_MODE_INTER_WORD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JUSTIFICATION_MODE_INTER_WORD: Int
```

Value for justification mode indicating the text is justified by stretching word spacing.

 Value: 1

### JUSTIFICATION_MODE_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JUSTIFICATION_MODE_NONE: Int
```

Value for justification mode indicating no justification.

 Value: 0

## Public methods

### computeLineBreaks

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun computeLineBreaks(
    measuredPara: MeasuredText, 
    constraints: LineBreaker.ParagraphConstraints, 
    lineNumber: Int
): LineBreaker.Result
```

Break paragraph into lines. The result is filled to out param.

| Parameters ||
|---|---|
| `measuredPara` | [MeasuredText](https://developer.android.com/reference/kotlin/android/graphics/text/MeasuredText): a result of the text measurement. This value cannot be `null`. |
| `constraints` | [LineBreaker.ParagraphConstraints](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.ParagraphConstraints): for a single paragraph. This value cannot be `null`. |
| `lineNumber` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a line number of this paragraph. Value is 0 or greater |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/text/LineBreaker.Result` | This value cannot be `null`. |

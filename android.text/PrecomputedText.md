# PrecomputedText

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrecomputedText

Kotlin| [Java](PrecomputedText.md) 
| --- | --- |

```
open class PrecomputedText : Spannable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.PrecomputedText](PrecomputedText.md) |

A text which has the character metrics data. A text object that contains the character metrics data and can be used to improve the performance of text layout operations. When a PrecomputedText is created with a given [CharSequence](../java.lang/CharSequence.md), it will measure the text metrics during the creation. This PrecomputedText instance can be set on [android.widget.TextView](../android.widget/TextView.md) or [StaticLayout](StaticLayout.md). Since the text layout information will be included in this instance, [android.widget.TextView](../android.widget/TextView.md) or [StaticLayout](StaticLayout.md) will not have to recalculate this information. Note that the [PrecomputedText](PrecomputedText.md) created from different parameters of the target will be rejected internally and compute the text layout again with the current [android.widget.TextView](../android.widget/TextView.md) parameters. 

```kotlin
An example usage is:
  <code>
   static void asyncSetText(TextView textView, final String longString, Executor bgExecutor) {
       // construct precompute related parameters using the TextView that we will set the text on.
       final PrecomputedText.Params params = textView.getTextMetricsParams();
       final Reference textViewRef = new WeakReference&lt;&gt;(textView);
       bgExecutor.submit(() -&gt; {
           TextView textView = textViewRef.get();
           if (textView == null) return;
           final PrecomputedText precomputedText = PrecomputedText.create(longString, params);
           textView.post(() -&gt; {
               TextView textView = textViewRef.get();
               if (textView == null) return;
               textView.setText(precomputedText);
           });
       });
   }
  </code>
```
Note that the [PrecomputedText](PrecomputedText.md) created from different parameters of the target [android.widget.TextView](../android.widget/TextView.md) will be rejected. Note that any [android.text.NoCopySpan](NoCopySpan.md) attached to the original text won't be passed to PrecomputedText.

<br />

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Params](../android/text/PrecomputedText.Params.md) The information required for building [PrecomputedText](PrecomputedText.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [PrecomputedText](PrecomputedText.md)! | [create](PrecomputedText.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `params:` ` [PrecomputedText.Params](../android/text/PrecomputedText.Params.md)`)` Create a new [PrecomputedText](PrecomputedText.md) which will pre-compute text measurement and glyph positioning information. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [get](PrecomputedText.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getBounds](PrecomputedText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [Rect](../android.graphics/Rect.md)`)` Retrieves the text bounding box for the given range. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getFontMetricsInt](PrecomputedText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outMetrics:` ` [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)`)` Retrieves the text font metrics for the given range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphCount](PrecomputedText.md))`()` Returns the count of paragraphs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphEnd](PrecomputedText.md))`(`paraIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the paragraph end offset of the text. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParagraphStart](PrecomputedText.md))`(`paraIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the paragraph start offset of the text. |
| open [PrecomputedText.Params](../android/text/PrecomputedText.Params.md) | [getParams](PrecomputedText.md))`()` Returns the layout parameters used to measure this text. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanEnd](PrecomputedText.md))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanFlags](PrecomputedText.md))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanStart](PrecomputedText.md))`(`tag:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getSpans](PrecomputedText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Class](../java.lang/Class.md)<T>!`)` <br /> |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](PrecomputedText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns text width for the given range. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextSpanTransition](PrecomputedText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeSpan](PrecomputedText.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSpan](PrecomputedText.md))`(`what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | [subSequence](PrecomputedText.md))`(`startIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `endIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PrecomputedText.md))`()` <br /> |
| --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](PrecomputedText.md) <br /> |

## Public methods

### create

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun create(
    text: CharSequence, 
    params: PrecomputedText.Params
): PrecomputedText!
```

Create a new [PrecomputedText](PrecomputedText.md) which will pre-compute text measurement and glyph positioning information.

This can be expensive, so computing this on a background thread before your text will be presented can save work on the UI thread.
Note that any [android.text.NoCopySpan](NoCopySpan.md) attached to the text won't be passed to the created PrecomputedText.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):the text to be measured This value cannot be`null`. |
| `params` | [PrecomputedText.Params](../android/text/PrecomputedText.Params.md):parameters that define how text will be precomputed This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [PrecomputedText](PrecomputedText.md)! | A [PrecomputedText](PrecomputedText.md) |

### get

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(index: Int): Char
```

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the`char`value to be returned |

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the specified`char`value |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the`index`argument is negative or not less than`length()` |

### getBounds

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBounds(
    start: Int, 
    end: Int, 
    bounds: Rect
): Unit
```

Retrieves the text bounding box for the given range. Both`start`and`end`offset need to be in the same paragraph, otherwise IllegalArgumentException will be thrown.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the inclusive start offset in the text Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the exclusive end offset in the text Value is 0 or greater |
| `bounds` | [Rect](../android.graphics/Rect.md):the output rectangle This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if start and end offset are in the different paragraph. |

### getFontMetricsInt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFontMetricsInt(
    start: Int, 
    end: Int, 
    outMetrics: Paint.FontMetricsInt
): Unit
```

Retrieves the text font metrics for the given range. Both`start`and`end`offset need to be in the same paragraph, otherwise IllegalArgumentException will be thrown.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the inclusive start offset in the text Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the exclusive end offset in the text Value is 0 or greater |
| `outMetrics` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md):the output font metrics This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if start and end offset are in the different paragraph. |

### getParagraphCount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraphCount(): Int
```

Returns the count of paragraphs.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getParagraphEnd

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraphEnd(paraIndex: Int): Int
```

Returns the paragraph end offset of the text.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------|
| `paraIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getParagraphStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParagraphStart(paraIndex: Int): Int
```

Returns the paragraph start offset of the text.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------|
| `paraIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getParams

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParams(): PrecomputedText.Params
```

Returns the layout parameters used to measure this text.

| Return ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------|
| [PrecomputedText.Params](../android/text/PrecomputedText.Params.md) | This value cannot be`null`. |

### getSpanEnd

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanEnd(tag: Any!): Int
```  

### getSpanFlags

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanFlags(tag: Any!): Int
```  

### getSpanStart

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanStart(tag: Any!): Int
```  

### getSpans

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> getSpans(
    start: Int, 
    end: Int, 
    type: Class<T>!
): Array<T>!
```  

### getWidth

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(
    start: Int, 
    end: Int
): Float
```

Returns text width for the given range. Both`start`and`end`offset need to be in the same paragraph, otherwise IllegalArgumentException will be thrown.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the inclusive start offset in the text Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the exclusive end offset in the text Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the text width Value is 0.0f or greater |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if start and end offset are in the different paragraph. |

### nextSpanTransition

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextSpanTransition(
    start: Int, 
    limit: Int, 
    type: Class<Any!>!
): Int
```  

### removeSpan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeSpan(what: Any!): Unit
```

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if [MetricAffectingSpan](../android.text.style/MetricAffectingSpan.md) is specified. |

### setSpan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSpan(
    what: Any!, 
    start: Int, 
    end: Int, 
    flags: Int
): Unit
```

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if [MetricAffectingSpan](../android.text.style/MetricAffectingSpan.md) is specified. |

### subSequence

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

| Parameters ||
|---------|----------------------------|
| `start` | the start index, inclusive |
| `end` | the end index, exclusive |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | the specified subsequence |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`start`or`end`are negative, if`end`is greater than`length()`, or if`start`is greater than`end` |

### toString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string consisting of exactly this sequence of characters |

## Properties

### length

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val length: Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of`char`s in this sequence |

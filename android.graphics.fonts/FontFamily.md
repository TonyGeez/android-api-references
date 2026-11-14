# FontFamily

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FontFamily

Kotlin | [Java](../android/graphics/fonts/FontFamily.md) 
| --- | --- |

```
class FontFamily
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.fonts.FontFamily](../android/graphics/fonts/FontFamily.md) |

A font family class can be used for creating Typeface.

A font family is a bundle of fonts for drawing text in various styles. For example, you can bundle regular style font and bold style font into a single font family, then system will select the correct style font from family for drawing. 

```kotlin
FontFamily family = new FontFamily.Builder(new Font.Builder("regular.ttf").build())
       .addFont(new Font.Builder("bold.ttf").build()).build();
   Typeface typeface = new Typeface.Builder2(family).build();
 
   SpannableStringBuilder ssb = new SpannableStringBuilder("Hello, World.");
   ssb.setSpan(new StyleSpan(Typeface.Bold), 6, 12, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);
 
   textView.setTypeface(typeface);
   textView.setText(ssb);
  
```
In this example, "Hello, " is drawn with "regular.ttf", and "World." is drawn with "bold.ttf". If there is no font exactly matches with the text style, the system will select the closest font.

<br />

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/graphics/fonts/FontFamily.Builder.md) A builder class for creating new FontFamily. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Font](../android/graphics/fonts/Font.md) | [getFont](../android/graphics/fonts/FontFamily.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a font |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](../android/graphics/fonts/FontFamily.md))`()` Returns the number of fonts in this FontFamily. |

## Public methods

### getFont

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFont(index: Int): Font
```

Returns a font

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an index of the font Value is 0 or greater |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Font](../android/graphics/fonts/Font.md) | a registered font This value cannot be `null`. |

### getSize

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Int
```

Returns the number of fonts in this FontFamily.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of fonts registered in this family. Value is 1 or greater |

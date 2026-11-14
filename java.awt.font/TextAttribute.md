# TextAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextAttribute

```
class TextAttribute : AttributedCharacterIterator.Attribute
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.text.AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#) ||
| | ↳ | [java.awt.font.TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#) |

The`TextAttribute`class defines attribute keys and attribute values used for text rendering.

`TextAttribute`instances are used as attribute keys to identify attributes in classes handling text attributes. Other constants defined in this class can be used as attribute values.

For each text attribute, the documentation provides:

- the type of its value,
- the relevant predefined constants, if any
- the default effect if the attribute is absent
- the valid values if there are limitations
- a description of the effect.

<br />

### Values

- The values of attributes must always be immutable.
- Where value limitations are given, any value outside of that set is reserved for future use; the value will be treated as the default.
- The value`null`is treated the same as the default value and results in the default behavior.
- If the value is not of the proper type, the attribute will be ignored.
- The identity of the value does not matter, only the actual value. For example,`TextAttribute.WEIGHT_BOLD`and`new Float(2.0)`indicate the same`WEIGHT`.
- Attribute values of type`Number`(used for`WEIGHT`,`WIDTH`,`POSTURE`,`SIZE`,`JUSTIFICATION`, and`TRACKING`) can vary along their natural range and are not restricted to the predefined constants.`Number.floatValue()`is used to get the actual value from the`Number`.
- The values for`WEIGHT`,`WIDTH`, and`POSTURE`are interpolated by the system, which can select the 'nearest available' font or use other techniques to approximate the user's request.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TextAttribute(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`TextAttribute`with the specified name. |

| Protected methods ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [readResolve](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#readResolve())`()` Resolves instances being deserialized to the predefined constants. |

| Inherited functions ||
|---|---|
| From class [Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares two objects for equality. This version only returns true for`x.equals(y)`if`x`and`y`refer to the same object, and guarantees this for all subclasses. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#getName())`()` <br /> Returns the name of the attribute. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#hashCode())`()` <br /> Returns a hash code value for the object. This version is identical to the one in`Object`, but is also final. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#toString())`()` <br /> Returns a string representation of the object. This version returns the concatenation of class name,`"("`, a name identifying the attribute and`")"`. <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [BACKGROUND](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#BACKGROUND:java.awt.font.TextAttribute) Attribute key for the paint used to render the background of the text. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [BIDI_EMBEDDING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#BIDI_EMBEDDING:java.awt.font.TextAttribute) Attribute key for the embedding level of the text. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [CHAR_REPLACEMENT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#CHAR_REPLACEMENT:java.awt.font.TextAttribute) Attribute key for a user-defined glyph to display in lieu of the font's standard glyph for a character. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [FAMILY](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#FAMILY:java.awt.font.TextAttribute) Attribute key for the font name. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [FONT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#FONT:java.awt.font.TextAttribute) Attribute key used to provide the font to use to render text. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [FOREGROUND](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#FOREGROUND:java.awt.font.TextAttribute) Attribute key for the paint used to render the text. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [INPUT_METHOD_HIGHLIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_HIGHLIGHT:java.awt.font.TextAttribute) Attribute key for input method highlight styles. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [INPUT_METHOD_UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_UNDERLINE:java.awt.font.TextAttribute) Attribute key for input method underlines. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [JUSTIFICATION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION:java.awt.font.TextAttribute) Attribute key for the justification of a paragraph. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [JUSTIFICATION_FULL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION_FULL:kotlin.Float) Justify the line to the full requested width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [JUSTIFICATION_NONE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION_NONE:kotlin.Float) Do not allow the line to be justified. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [KERNING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#KERNING:java.awt.font.TextAttribute) Attribute key to request kerning. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [KERNING_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#KERNING_ON:kotlin.Int) Request standard kerning. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [LIGATURES](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#LIGATURES:java.awt.font.TextAttribute) Attribute key for enabling optional ligatures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [LIGATURES_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#LIGATURES_ON:kotlin.Int) Request standard optional ligatures. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [NUMERIC_SHAPING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#NUMERIC_SHAPING:java.awt.font.TextAttribute) Attribute key for converting ASCII decimal digits to other decimal ranges. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [POSTURE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE:java.awt.font.TextAttribute) Attribute key for the posture of a font. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [POSTURE_OBLIQUE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE_OBLIQUE:kotlin.Float) The standard italic posture. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [POSTURE_REGULAR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE_REGULAR:kotlin.Float) The standard posture, upright. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [RUN_DIRECTION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION:java.awt.font.TextAttribute) Attribute key for the run direction of the line. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [RUN_DIRECTION_LTR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION_LTR:kotlin.Boolean) Left-to-right run direction. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [RUN_DIRECTION_RTL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION_RTL:kotlin.Boolean) Right-to-left run direction. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [SIZE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SIZE:java.awt.font.TextAttribute) Attribute key for the font size. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [STRIKETHROUGH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#STRIKETHROUGH:java.awt.font.TextAttribute) Attribute key for strikethrough. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [STRIKETHROUGH_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#STRIKETHROUGH_ON:kotlin.Boolean) A single strikethrough. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [SUPERSCRIPT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT:java.awt.font.TextAttribute) Attribute key for superscripting and subscripting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [SUPERSCRIPT_SUB](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT_SUB:kotlin.Int) Standard subscript. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [SUPERSCRIPT_SUPER](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT_SUPER:kotlin.Int) Standard superscript. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [SWAP_COLORS](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS:java.awt.font.TextAttribute) Attribute key for swapping foreground and background`Paints`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [SWAP_COLORS_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS_ON:kotlin.Boolean) Swap foreground and background. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [TRACKING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING:java.awt.font.TextAttribute) Attribute key to control tracking. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [TRACKING_LOOSE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING_LOOSE:kotlin.Float) Perform loose tracking. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [TRACKING_TIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING_TIGHT:kotlin.Float) Perform tight tracking. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [TRANSFORM](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRANSFORM:java.awt.font.TextAttribute) Attribute key for the transform of a font. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE:java.awt.font.TextAttribute) Attribute key for underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_DASHED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_DASHED:kotlin.Int) Single pixel dashed low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_DOTTED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_DOTTED:kotlin.Int) Single pixel dotted low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_GRAY](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_GRAY:kotlin.Int) Double pixel gray low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_ONE_PIXEL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_ONE_PIXEL:kotlin.Int) Single pixel solid low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_TWO_PIXEL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_TWO_PIXEL:kotlin.Int) Double pixel solid low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_ON:kotlin.Int) Standard underline. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) Attribute key for the weight of a font. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_BOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_BOLD:kotlin.Float) The standard bold weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_DEMIBOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_DEMIBOLD:kotlin.Float) A moderately lighter weight than`WEIGHT_BOLD`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_DEMILIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_DEMILIGHT:kotlin.Float) An intermediate weight between`WEIGHT_LIGHT`and`WEIGHT_STANDARD`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_EXTRABOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_EXTRABOLD:kotlin.Float) An extra heavy weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_EXTRA_LIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_EXTRA_LIGHT:kotlin.Float) The lightest predefined weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_HEAVY](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_HEAVY:kotlin.Float) A moderately heavier weight than`WEIGHT_BOLD`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_LIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_LIGHT:kotlin.Float) The standard light weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_MEDIUM](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_MEDIUM:kotlin.Float) An intermediate weight between`WEIGHT_REGULAR`and`WEIGHT_BOLD`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_REGULAR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_REGULAR:kotlin.Float) The standard weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_SEMIBOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_SEMIBOLD:kotlin.Float) A moderately heavier weight than`WEIGHT_REGULAR`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_ULTRABOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_ULTRABOLD:kotlin.Float) The heaviest predefined weight. |
| static [TextAttribute](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#)! | [WIDTH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH:java.awt.font.TextAttribute) Attribute key for the width of a font. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_CONDENSED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_CONDENSED:kotlin.Float) The most condensed predefined width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_EXTENDED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_EXTENDED:kotlin.Float) The most extended predefined width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_REGULAR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_REGULAR:kotlin.Float) The standard width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_SEMI_CONDENSED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_SEMI_CONDENSED:kotlin.Float) A moderately condensed width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_SEMI_EXTENDED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_SEMI_EXTENDED:kotlin.Float) A moderately extended width. |

| Inherited properties ||
|---|---|
| From class [Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#) |------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#)! | [INPUT_METHOD_SEGMENT](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#INPUT_METHOD_SEGMENT:java.text.AttributedCharacterIterator.Attribute) <br /> Attribute key for input method segments. Input methods often break up text into segments, which usually correspond to words. Values are instances of [Annotation](https://developer.android.com/reference/kotlin/java/text/Annotation.html#) holding a`null`reference. <br /> | | [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#)! | [LANGUAGE](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#LANGUAGE:java.text.AttributedCharacterIterator.Attribute) <br /> Attribute key for the language of some text. Values are instances of [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). <br /> | | [AttributedCharacterIterator.Attribute](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#)! | [READING](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.Attribute.html#READING:java.text.AttributedCharacterIterator.Attribute) <br /> Attribute key for the reading of some text. In languages where the written form and the pronunciation of a word are only loosely related (such as Japanese), it is often necessary to store the reading (pronunciation) along with the written form. Values are instances of [Annotation](https://developer.android.com/reference/kotlin/java/text/Annotation.html#) holding instances of [String](https://developer.android.com/reference/kotlin/java/lang/String.html#). <br /> | ||

## Protected constructors

### TextAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected TextAttribute(name: String!)
```

Constructs a`TextAttribute`with the specified name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute name to assign to this`TextAttribute` |

## Protected methods

### readResolve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun readResolve(): Any!
```

Resolves instances being deserialized to the predefined constants.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the resolved`Attribute`object |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------|
| `java.io.InvalidObjectException` | if the object to resolve is not an instance of`Attribute` |

## Properties

### BACKGROUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BACKGROUND: TextAttribute!
```

Attribute key for the paint used to render the background of the text. Values are instances of**`Paint`**. The default value is null, indicating that the background should not be rendered.

The logical bounds of the text will be filled using this`Paint`, and then the text will be rendered on top of it (but see [SWAP_COLORS](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS:java.awt.font.TextAttribute)).

The visual bounds of the text is extended to include the logical bounds, if necessary. The outline is not affected. 
**See Also**

- [#SWAP_COLORS](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS:java.awt.font.TextAttribute) 

### BIDI_EMBEDDING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_EMBEDDING: TextAttribute!
```

Attribute key for the embedding level of the text. Values are instances of**`Integer`** . The default value is`null`, indicating that the the Bidirectional algorithm should run without explicit embeddings.

Positive values 1 through 61 are*embedding* levels, negative values -1 through -61 are*override*levels. The value 0 means that the base line direction is used. These levels are passed in the embedding levels array to the constructor.

*Note:*When this attribute is present anywhere in a paragraph, then any Unicode bidi control characters (RLO, LRO, RLE, LRE, and PDF) in the paragraph are disregarded, and runs of text where this attribute is not present are treated as though it were present and had the value 0. 
**See Also**

- [java.text.Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi.html#) 

### CHAR_REPLACEMENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHAR_REPLACEMENT: TextAttribute!
```

Attribute key for a user-defined glyph to display in lieu of the font's standard glyph for a character. Values are intances of GraphicAttribute. The default value is null, indicating that the standard glyphs provided by the font should be used.

This attribute is used to reserve space for a graphic or other component embedded in a line of text. It is required for correct positioning of 'inline' components within a line when bidirectional reordering (see [java.text.Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi.html#)) is performed. Each character (Unicode code point) will be rendered using the provided GraphicAttribute. Typically, the characters to which this attribute is applied should be`\uFFFC`.

The GraphicAttribute determines the logical and visual bounds of the text; the actual Font values are ignored. 

### FAMILY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FAMILY: TextAttribute!
```

Attribute key for the font name. Values are instances of**`String`** . The default value is`"Default"`, which causes the platform default font family to be used.

The`Font`class defines constants for the logical font names.

This defines the value passed as`name`to the`Font`constructor. Both logical and physical font names are allowed. If a font with the requested name is not found, the default font is used.

*Note:* This attribute is unfortunately misnamed, as it specifies the face name and not just the family. Thus values such as "Lucida Sans Bold" will select that face if it exists. Note, though, that if the requested face does not exist, the default will be used with*regular*weight. The "Bold" in the name is part of the face name, not a separate request that the font's weight be bold. 

### FONT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FONT: TextAttribute!
```

Attribute key used to provide the font to use to render text. The default value is null, indicating that normal resolution of a`Font`from attributes should be performed.

`TextLayout`and`AttributedCharacterIterator`work in terms of`Maps`of`TextAttributes`. Normally, all the attributes are examined and used to select and configure a`Font`instance. If a`FONT`attribute is present, though, its associated`Font`will be used. This provides a way for users to override the resolution of font attributes into a`Font`, or force use of a particular`Font`instance. This also allows users to specify subclasses of`Font`in cases where a`Font`can be subclassed.

`FONT`is used for special situations where clients already have a`Font`instance but still need to use`Map`-based APIs. Typically, there will be no other attributes in the`Map`except the`FONT`attribute. With`Map`-based APIs the common case is to specify all attributes individually, so`FONT`is not needed or desireable.

However, if both`FONT`and other attributes are present in the`Map`, the rendering system will merge the attributes defined in the`Font`with the additional attributes. This merging process classifies`TextAttributes`into two groups. One group, the 'primary' group, is considered fundamental to the selection and metric behavior of a font. These attributes are`FAMILY`,`WEIGHT`,`WIDTH`,`POSTURE`,`SIZE`,`TRANSFORM`,`SUPERSCRIPT`, and`TRACKING`. The other group, the 'secondary' group, consists of all other defined attributes, with the exception of`FONT`itself.

To generate the new`Map`, first the`Font`is obtained from the`FONT`attribute, and*all* of its attributes extracted into a new`Map`. Then only the*secondary* attributes from the original`Map`are added to those in the new`Map`. Thus the values of primary attributes come solely from the`Font`, and the values of secondary attributes originate with the`Font`but can be overridden by other values in the`Map`. 

### FOREGROUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOREGROUND: TextAttribute!
```

Attribute key for the paint used to render the text. Values are instances of**`Paint`** . The default value is null, indicating that the`Paint`set on the`Graphics2D`at the time of rendering is used.

Glyphs will be rendered using this`Paint`regardless of the`Paint`value set on the`Graphics`(but see [SWAP_COLORS](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS:java.awt.font.TextAttribute)). 
**See Also**

- [#SWAP_COLORS](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS:java.awt.font.TextAttribute) 

### INPUT_METHOD_HIGHLIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_HIGHLIGHT: TextAttribute!
```

Attribute key for input method highlight styles. The default value is`null`, which means that input method styles should not be applied before rendering. 
**See Also**

- [java.text.Annotation](https://developer.android.com/reference/kotlin/java/text/Annotation.html#) 

### INPUT_METHOD_UNDERLINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_UNDERLINE: TextAttribute!
```

Attribute key for input method underlines. Values are instances of**`Integer`** . The default value is`-1`, which means no underline.

Several constant values are provided, see [UNDERLINE_LOW_ONE_PIXEL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_ONE_PIXEL:kotlin.Int), [UNDERLINE_LOW_TWO_PIXEL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_TWO_PIXEL:kotlin.Int), [UNDERLINE_LOW_DOTTED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_DOTTED:kotlin.Int), [UNDERLINE_LOW_GRAY](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_GRAY:kotlin.Int), and [UNDERLINE_LOW_DASHED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_LOW_DASHED:kotlin.Int).

This may be used in conjunction with [UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE:java.awt.font.TextAttribute) if desired. The primary purpose is for use by input methods. Other use of these underlines for simple ornamentation might confuse users.

The input method underline affects both the visual bounds and the outline of the text. 

### JUSTIFICATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION: TextAttribute!
```

Attribute key for the justification of a paragraph. Values are instances of**`Number`**. The default value is 1, indicating that justification should use the full width provided. Values are pinned to the range \[0..1\].

The constants [JUSTIFICATION_FULL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION_FULL:kotlin.Float) and [JUSTIFICATION_NONE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION_NONE:kotlin.Float) are provided.

Specifies the fraction of the extra space to use when justification is requested on a`TextLayout`. For example, if the line is 50 points wide and it is requested to justify to 70 points, a value of 0.75 will pad to use three-quarters of the remaining space, or 15 points, so that the resulting line will be 65 points in length.

*Note:*This should have the same value for all the text in a paragraph, otherwise the behavior is undetermined. 

### JUSTIFICATION_FULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_FULL: Float!
```

Justify the line to the full requested width. This is the default value for`JUSTIFICATION`. 
**See Also**

- [#JUSTIFICATION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION:java.awt.font.TextAttribute) 

### JUSTIFICATION_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_NONE: Float!
```

Do not allow the line to be justified. 
**See Also**

- [#JUSTIFICATION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#JUSTIFICATION:java.awt.font.TextAttribute) 

### KERNING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KERNING: TextAttribute!
```

Attribute key to request kerning. Values are instances of**`Integer`** . The default value is`0`, which does not request kerning.

The constant value [KERNING_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#KERNING_ON:kotlin.Int) is provided.

The default advances of single characters are not appropriate for some character sequences, for example "To" or "AWAY". Without kerning the adjacent characters appear to be separated by too much space. Kerning causes selected sequences of characters to be spaced differently for a more pleasing visual appearance. 

### KERNING_ON

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KERNING_ON: Int!
```

Request standard kerning. 
**See Also**

- [#KERNING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#KERNING:java.awt.font.TextAttribute) 

### LIGATURES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGATURES: TextAttribute!
```

Attribute key for enabling optional ligatures. Values are instances of**`Integer`** . The default value is`0`, which means do not use optional ligatures.

The constant value [LIGATURES_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#LIGATURES_ON:kotlin.Int) is defined.

Ligatures required by the writing system are always enabled. 

### LIGATURES_ON

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGATURES_ON: Int!
```

Request standard optional ligatures. 
**See Also**

- [#LIGATURES](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#LIGATURES:java.awt.font.TextAttribute) 

### NUMERIC_SHAPING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMERIC_SHAPING: TextAttribute!
```

Attribute key for converting ASCII decimal digits to other decimal ranges. Values are instances of [NumericShaper](https://developer.android.com/reference/kotlin/java/awt/font/NumericShaper). The default is`null`, which means do not perform numeric shaping.

When a numeric shaper is defined, the text is first processed by the shaper before any other analysis of the text is performed.

*Note:*This should have the same value for all the text in the paragraph, otherwise the behavior is undetermined. 
**See Also**

- [java.awt.font.NumericShaper](https://developer.android.com/reference/kotlin/java/awt/font/NumericShaper) 

### POSTURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSTURE: TextAttribute!
```

Attribute key for the posture of a font. Values are instances of**`Number`** . The default value is`POSTURE_REGULAR`.

Two constant values are provided, [POSTURE_REGULAR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE_REGULAR:kotlin.Float) and [POSTURE_OBLIQUE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE_OBLIQUE:kotlin.Float). The value`POSTURE_OBLIQUE`corresponds to the style value`Font.ITALIC`as passed to the`Font`constructor.

The value is roughly the slope of the stems of the font, expressed as the run over the rise. Positive values lean right.

The system can interpolate the provided value.

This will affect the font's italic angle as returned by`Font.getItalicAngle`. 

### POSTURE_OBLIQUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSTURE_OBLIQUE: Float!
```

The standard italic posture. 
**See Also**

- [#POSTURE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE:java.awt.font.TextAttribute) 

### POSTURE_REGULAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSTURE_REGULAR: Float!
```

The standard posture, upright. This is the default value for`POSTURE`. 
**See Also**

- [#POSTURE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#POSTURE:java.awt.font.TextAttribute) 

### RUN_DIRECTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUN_DIRECTION: TextAttribute!
```

Attribute key for the run direction of the line. Values are instances of**`Boolean`** . The default value is null, which indicates that the standard Bidi algorithm for determining run direction should be used with the value [java.text.Bidi#DIRECTION_DEFAULT_LEFT_TO_RIGHT](https://developer.android.com/reference/kotlin/java/text/Bidi.html#DIRECTION_DEFAULT_LEFT_TO_RIGHT:kotlin.Int).

The constants [RUN_DIRECTION_RTL](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION_RTL:kotlin.Boolean) and [RUN_DIRECTION_LTR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION_LTR:kotlin.Boolean) are provided.

This determines the value passed to the constructor to select the primary direction of the text in the paragraph.

*Note:*This attribute should have the same value for all the text in a paragraph, otherwise the behavior is undetermined. 
**See Also**

- [java.text.Bidi](https://developer.android.com/reference/kotlin/java/text/Bidi.html#) 

### RUN_DIRECTION_LTR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUN_DIRECTION_LTR: Boolean!
```

Left-to-right run direction. 
**See Also**

- [#RUN_DIRECTION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION:java.awt.font.TextAttribute) 

### RUN_DIRECTION_RTL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUN_DIRECTION_RTL: Boolean!
```

Right-to-left run direction. 
**See Also**

- [#RUN_DIRECTION](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#RUN_DIRECTION:java.awt.font.TextAttribute) 

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIZE: TextAttribute!
```

Attribute key for the font size. Values are instances of**`Number`**. The default value is 12pt.

This corresponds to the`size`parameter to the`Font`constructor.

Very large or small sizes will impact rendering performance, and the rendering system might not render text at these sizes. Negative sizes are illegal and result in the default size.

Note that the appearance and metrics of a 12pt font with a 2x transform might be different than that of a 24 point font with no transform. 

### STRIKETHROUGH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRIKETHROUGH: TextAttribute!
```

Attribute key for strikethrough. Values are instances of**`Boolean`** . The default value is`false`, which means no strikethrough.

The constant value [STRIKETHROUGH_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#STRIKETHROUGH_ON:kotlin.Boolean) is provided.

The strikethrough affects both the visual bounds and the outline of the text. 

### STRIKETHROUGH_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRIKETHROUGH_ON: Boolean!
```

A single strikethrough. 
**See Also**

- [#STRIKETHROUGH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#STRIKETHROUGH:java.awt.font.TextAttribute) 

### SUPERSCRIPT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPERSCRIPT: TextAttribute!
```

Attribute key for superscripting and subscripting. Values are instances of**`Integer`**. The default value is 0, which means that no superscript or subscript is used.

Two constant values are provided, see [SUPERSCRIPT_SUPER](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT_SUPER:kotlin.Int) and [SUPERSCRIPT_SUB](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT_SUB:kotlin.Int). These have the values 1 and -1 respectively. Values of greater magnitude define greater levels of superscript or subscripting, for example, 2 corresponds to super-superscript, 3 to super-super-superscript, and similarly for negative values and subscript, up to a level of 7 (or -7). Values beyond this range are reserved; behavior is platform-dependent.

`SUPERSCRIPT`can impact the ascent and descent of a font. The ascent and descent can never become negative, however. 

### SUPERSCRIPT_SUB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPERSCRIPT_SUB: Int!
```

Standard subscript. 
**See Also**

- [#SUPERSCRIPT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT:java.awt.font.TextAttribute) 

### SUPERSCRIPT_SUPER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPERSCRIPT_SUPER: Int!
```

Standard superscript. 
**See Also**

- [#SUPERSCRIPT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SUPERSCRIPT:java.awt.font.TextAttribute) 

### SWAP_COLORS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SWAP_COLORS: TextAttribute!
```

Attribute key for swapping foreground and background`Paints`. Values are instances of**`Boolean`** . The default value is`false`, which means do not swap colors.

The constant value [SWAP_COLORS_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS_ON:kotlin.Boolean) is defined.

If the [FOREGROUND](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#FOREGROUND:java.awt.font.TextAttribute) attribute is set, its`Paint`will be used as the background, otherwise the`Paint`currently on the`Graphics`will be used. If the [BACKGROUND](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#BACKGROUND:java.awt.font.TextAttribute) attribute is set, its`Paint`will be used as the foreground, otherwise the system will find a contrasting color to the (resolved) background so that the text will be visible. 
**See Also**

- [#FOREGROUND](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#FOREGROUND:java.awt.font.TextAttribute)
- [#BACKGROUND](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#BACKGROUND:java.awt.font.TextAttribute) 

### SWAP_COLORS_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SWAP_COLORS_ON: Boolean!
```

Swap foreground and background. 
**See Also**

- [#SWAP_COLORS](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#SWAP_COLORS:java.awt.font.TextAttribute) 

### TRACKING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACKING: TextAttribute!
```

Attribute key to control tracking. Values are instances of**`Number`** . The default value is`0`, which means no additional tracking.

The constant values [TRACKING_TIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING_TIGHT:kotlin.Float) and [TRACKING_LOOSE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING_LOOSE:kotlin.Float) are provided.

The tracking value is multiplied by the font point size and passed through the font transform to determine an additional amount to add to the advance of each glyph cluster. Positive tracking values will inhibit formation of optional ligatures. Tracking values are typically between`-0.1`and`0.3`; values outside this range are generally not desireable. 

### TRACKING_LOOSE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACKING_LOOSE: Float!
```

Perform loose tracking. 
**See Also**

- [#TRACKING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING:java.awt.font.TextAttribute) 

### TRACKING_TIGHT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACKING_TIGHT: Float!
```

Perform tight tracking. 
**See Also**

- [#TRACKING](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#TRACKING:java.awt.font.TextAttribute) 

### TRANSFORM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSFORM: TextAttribute!
```

Attribute key for the transform of a font. Values are instances of**`TransformAttribute`** . The default value is`TransformAttribute.IDENTITY`.

The primary intent is to support scaling and skewing, though other effects are possible.

Some transforms will cause the baseline to be rotated and/or shifted. The text and the baseline are transformed together so that the text follows the new baseline. For example, with text on a horizontal baseline, the new baseline follows the direction of the unit x vector passed through the transform. Text metrics are measured against this new baseline. So, for example, with other things being equal, text rendered with a rotated TRANSFORM and an unrotated TRANSFORM will measure as having the same ascent, descent, and advance. 

### UNDERLINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE: TextAttribute!
```

Attribute key for underline. Values are instances of**`Integer`**. The default value is -1, which means no underline.

The constant value [UNDERLINE_ON](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE_ON:kotlin.Int) is provided.

The underline affects both the visual bounds and the outline of the text. 

### UNDERLINE_LOW_DASHED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_DASHED: Int!
```

Single pixel dashed low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_UNDERLINE:java.awt.font.TextAttribute) 

### UNDERLINE_LOW_DOTTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_DOTTED: Int!
```

Single pixel dotted low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_UNDERLINE:java.awt.font.TextAttribute) 

### UNDERLINE_LOW_GRAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_GRAY: Int!
```

Double pixel gray low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_UNDERLINE:java.awt.font.TextAttribute) 

### UNDERLINE_LOW_ONE_PIXEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_ONE_PIXEL: Int!
```

Single pixel solid low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_UNDERLINE:java.awt.font.TextAttribute) 

### UNDERLINE_LOW_TWO_PIXEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_TWO_PIXEL: Int!
```

Double pixel solid low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#INPUT_METHOD_UNDERLINE:java.awt.font.TextAttribute) 

### UNDERLINE_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_ON: Int!
```

Standard underline. 
**See Also**

- [#UNDERLINE](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#UNDERLINE:java.awt.font.TextAttribute) 

### WEIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT: TextAttribute!
```

Attribute key for the weight of a font. Values are instances of**`Number`** . The default value is`WEIGHT_REGULAR`.

Several constant values are provided, see [WEIGHT_EXTRA_LIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_EXTRA_LIGHT:kotlin.Float), [WEIGHT_LIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_LIGHT:kotlin.Float), [WEIGHT_DEMILIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_DEMILIGHT:kotlin.Float), [WEIGHT_REGULAR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_REGULAR:kotlin.Float), [WEIGHT_SEMIBOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_SEMIBOLD:kotlin.Float), [WEIGHT_MEDIUM](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_MEDIUM:kotlin.Float), [WEIGHT_DEMIBOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_DEMIBOLD:kotlin.Float), [WEIGHT_BOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_BOLD:kotlin.Float), [WEIGHT_HEAVY](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_HEAVY:kotlin.Float), [WEIGHT_EXTRABOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_EXTRABOLD:kotlin.Float), and [WEIGHT_ULTRABOLD](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT_ULTRABOLD:kotlin.Float). The value`WEIGHT_BOLD`corresponds to the style value`Font.BOLD`as passed to the`Font`constructor.

The value is roughly the ratio of the stem width to that of the regular weight.

The system can interpolate the provided value. 

### WEIGHT_BOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_BOLD: Float!
```

The standard bold weight. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_DEMIBOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_DEMIBOLD: Float!
```

A moderately lighter weight than`WEIGHT_BOLD`. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_DEMILIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_DEMILIGHT: Float!
```

An intermediate weight between`WEIGHT_LIGHT`and`WEIGHT_STANDARD`. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_EXTRABOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_EXTRABOLD: Float!
```

An extra heavy weight. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_EXTRA_LIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_EXTRA_LIGHT: Float!
```

The lightest predefined weight. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_HEAVY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_HEAVY: Float!
```

A moderately heavier weight than`WEIGHT_BOLD`. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_LIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_LIGHT: Float!
```

The standard light weight. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_MEDIUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_MEDIUM: Float!
```

An intermediate weight between`WEIGHT_REGULAR`and`WEIGHT_BOLD`. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_REGULAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_REGULAR: Float!
```

The standard weight. This is the default value for`WEIGHT`. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_SEMIBOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_SEMIBOLD: Float!
```

A moderately heavier weight than`WEIGHT_REGULAR`. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WEIGHT_ULTRABOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_ULTRABOLD: Float!
```

The heaviest predefined weight. 
**See Also**

- [#WEIGHT](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WEIGHT:java.awt.font.TextAttribute) 

### WIDTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH: TextAttribute!
```

Attribute key for the width of a font. Values are instances of**`Number`** . The default value is`WIDTH_REGULAR`.

Several constant values are provided, see [WIDTH_CONDENSED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_CONDENSED:kotlin.Float), [WIDTH_SEMI_CONDENSED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_SEMI_CONDENSED:kotlin.Float), [WIDTH_REGULAR](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_REGULAR:kotlin.Float), [WIDTH_SEMI_EXTENDED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_SEMI_EXTENDED:kotlin.Float), [WIDTH_EXTENDED](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH_EXTENDED:kotlin.Float).

The value is roughly the ratio of the advance width to that of the regular width.

The system can interpolate the provided value. 

### WIDTH_CONDENSED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_CONDENSED: Float!
```

The most condensed predefined width. 
**See Also**

- [#WIDTH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH:java.awt.font.TextAttribute) 

### WIDTH_EXTENDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_EXTENDED: Float!
```

The most extended predefined width. 
**See Also**

- [#WIDTH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH:java.awt.font.TextAttribute) 

### WIDTH_REGULAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_REGULAR: Float!
```

The standard width. This is the default value for`WIDTH`. 
**See Also**

- [#WIDTH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH:java.awt.font.TextAttribute) 

### WIDTH_SEMI_CONDENSED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_SEMI_CONDENSED: Float!
```

A moderately condensed width. 
**See Also**

- [#WIDTH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH:java.awt.font.TextAttribute) 

### WIDTH_SEMI_EXTENDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_SEMI_EXTENDED: Float!
```

A moderately extended width. 
**See Also**

- [#WIDTH](https://developer.android.com/reference/kotlin/java/awt/font/TextAttribute#WIDTH:java.awt.font.TextAttribute)

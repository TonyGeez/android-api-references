# TextAttribute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextAttribute

```
class TextAttribute : AttributedCharacterIterator.Attribute
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.text.AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md) ||
| | ↳ | [java.awt.font.TextAttribute](../java/awt/font/TextAttribute.md) |

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
| [TextAttribute](../java/awt/font/TextAttribute.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`TextAttribute`with the specified name. |

| Protected methods ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [readResolve](../java/awt/font/TextAttribute.md))`()` Resolves instances being deserialized to the predefined constants. |

| Inherited functions ||
|---|---|
| From class [Attribute](../java/text/AttributedCharacterIterator.Attribute.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/AttributedCharacterIterator.Attribute.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares two objects for equality. This version only returns true for`x.equals(y)`if`x`and`y`refer to the same object, and guarantees this for all subclasses. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/text/AttributedCharacterIterator.Attribute.md))`()` <br /> Returns the name of the attribute. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/text/AttributedCharacterIterator.Attribute.md))`()` <br /> Returns a hash code value for the object. This version is identical to the one in`Object`, but is also final. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/text/AttributedCharacterIterator.Attribute.md))`()` <br /> Returns a string representation of the object. This version returns the concatenation of class name,`"("`, a name identifying the attribute and`")"`. <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [BACKGROUND](../java/awt/font/TextAttribute.md) Attribute key for the paint used to render the background of the text. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [BIDI_EMBEDDING](../java/awt/font/TextAttribute.md) Attribute key for the embedding level of the text. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [CHAR_REPLACEMENT](../java/awt/font/TextAttribute.md) Attribute key for a user-defined glyph to display in lieu of the font's standard glyph for a character. |
| --- | --- |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [FAMILY](../java/awt/font/TextAttribute.md) Attribute key for the font name. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [FONT](../java/awt/font/TextAttribute.md) Attribute key used to provide the font to use to render text. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [FOREGROUND](../java/awt/font/TextAttribute.md) Attribute key for the paint used to render the text. |
| --- | --- |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [INPUT_METHOD_HIGHLIGHT](../java/awt/font/TextAttribute.md) Attribute key for input method highlight styles. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [INPUT_METHOD_UNDERLINE](../java/awt/font/TextAttribute.md) Attribute key for input method underlines. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [JUSTIFICATION](../java/awt/font/TextAttribute.md) Attribute key for the justification of a paragraph. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [JUSTIFICATION_FULL](../java/awt/font/TextAttribute.md) Justify the line to the full requested width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [JUSTIFICATION_NONE](../java/awt/font/TextAttribute.md) Do not allow the line to be justified. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [KERNING](../java/awt/font/TextAttribute.md) Attribute key to request kerning. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [KERNING_ON](../java/awt/font/TextAttribute.md) Request standard kerning. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [LIGATURES](../java/awt/font/TextAttribute.md) Attribute key for enabling optional ligatures. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [LIGATURES_ON](../java/awt/font/TextAttribute.md) Request standard optional ligatures. |
| --- | --- |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [NUMERIC_SHAPING](../java/awt/font/TextAttribute.md) Attribute key for converting ASCII decimal digits to other decimal ranges. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [POSTURE](../java/awt/font/TextAttribute.md) Attribute key for the posture of a font. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [POSTURE_OBLIQUE](../java/awt/font/TextAttribute.md) The standard italic posture. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [POSTURE_REGULAR](../java/awt/font/TextAttribute.md) The standard posture, upright. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [RUN_DIRECTION](../java/awt/font/TextAttribute.md) Attribute key for the run direction of the line. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [RUN_DIRECTION_LTR](../java/awt/font/TextAttribute.md) Left-to-right run direction. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [RUN_DIRECTION_RTL](../java/awt/font/TextAttribute.md) Right-to-left run direction. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [SIZE](../java/awt/font/TextAttribute.md) Attribute key for the font size. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [STRIKETHROUGH](../java/awt/font/TextAttribute.md) Attribute key for strikethrough. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [STRIKETHROUGH_ON](../java/awt/font/TextAttribute.md) A single strikethrough. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [SUPERSCRIPT](../java/awt/font/TextAttribute.md) Attribute key for superscripting and subscripting. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [SUPERSCRIPT_SUB](../java/awt/font/TextAttribute.md) Standard subscript. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [SUPERSCRIPT_SUPER](../java/awt/font/TextAttribute.md) Standard superscript. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [SWAP_COLORS](../java/awt/font/TextAttribute.md) Attribute key for swapping foreground and background`Paints`. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)! | [SWAP_COLORS_ON](../java/awt/font/TextAttribute.md) Swap foreground and background. |
| --- | --- |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [TRACKING](../java/awt/font/TextAttribute.md) Attribute key to control tracking. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [TRACKING_LOOSE](../java/awt/font/TextAttribute.md) Perform loose tracking. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [TRACKING_TIGHT](../java/awt/font/TextAttribute.md) Perform tight tracking. |
| --- | --- |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [TRANSFORM](../java/awt/font/TextAttribute.md) Attribute key for the transform of a font. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [UNDERLINE](../java/awt/font/TextAttribute.md) Attribute key for underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_DASHED](../java/awt/font/TextAttribute.md) Single pixel dashed low underline. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_DOTTED](../java/awt/font/TextAttribute.md) Single pixel dotted low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_GRAY](../java/awt/font/TextAttribute.md) Double pixel gray low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_ONE_PIXEL](../java/awt/font/TextAttribute.md) Single pixel solid low underline. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_LOW_TWO_PIXEL](../java/awt/font/TextAttribute.md) Double pixel solid low underline. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)! | [UNDERLINE_ON](../java/awt/font/TextAttribute.md) Standard underline. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [WEIGHT](../java/awt/font/TextAttribute.md) Attribute key for the weight of a font. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_BOLD](../java/awt/font/TextAttribute.md) The standard bold weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_DEMIBOLD](../java/awt/font/TextAttribute.md) A moderately lighter weight than`WEIGHT_BOLD`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_DEMILIGHT](../java/awt/font/TextAttribute.md) An intermediate weight between`WEIGHT_LIGHT`and`WEIGHT_STANDARD`. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_EXTRABOLD](../java/awt/font/TextAttribute.md) An extra heavy weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_EXTRA_LIGHT](../java/awt/font/TextAttribute.md) The lightest predefined weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_HEAVY](../java/awt/font/TextAttribute.md) A moderately heavier weight than`WEIGHT_BOLD`. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_LIGHT](../java/awt/font/TextAttribute.md) The standard light weight. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_MEDIUM](../java/awt/font/TextAttribute.md) An intermediate weight between`WEIGHT_REGULAR`and`WEIGHT_BOLD`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_REGULAR](../java/awt/font/TextAttribute.md) The standard weight. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_SEMIBOLD](../java/awt/font/TextAttribute.md) A moderately heavier weight than`WEIGHT_REGULAR`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WEIGHT_ULTRABOLD](../java/awt/font/TextAttribute.md) The heaviest predefined weight. |
| static [TextAttribute](../java/awt/font/TextAttribute.md)! | [WIDTH](../java/awt/font/TextAttribute.md) Attribute key for the width of a font. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_CONDENSED](../java/awt/font/TextAttribute.md) The most condensed predefined width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_EXTENDED](../java/awt/font/TextAttribute.md) The most extended predefined width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_REGULAR](../java/awt/font/TextAttribute.md) The standard width. |
| --- | --- |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_SEMI_CONDENSED](../java/awt/font/TextAttribute.md) A moderately condensed width. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)! | [WIDTH_SEMI_EXTENDED](../java/awt/font/TextAttribute.md) A moderately extended width. |

| Inherited properties ||
|---|---|
| From class [Attribute](../java/text/AttributedCharacterIterator.Attribute.md) |------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)! | [INPUT_METHOD_SEGMENT](../java/text/AttributedCharacterIterator.Attribute.md) <br /> Attribute key for input method segments. Input methods often break up text into segments, which usually correspond to words. Values are instances of [Annotation](../java/text/Annotation.md) holding a`null`reference. <br /> | | [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)! | [LANGUAGE](../java/text/AttributedCharacterIterator.Attribute.md) <br /> Attribute key for the language of some text. Values are instances of [Locale](../java/util/Locale.md). <br /> | | [AttributedCharacterIterator.Attribute](../java/text/AttributedCharacterIterator.Attribute.md)! | [READING](../java/text/AttributedCharacterIterator.Attribute.md) <br /> Attribute key for the reading of some text. In languages where the written form and the pronunciation of a word are only loosely related (such as Japanese), it is often necessary to store the reading (pronunciation) along with the written form. Values are instances of [Annotation](../java/text/Annotation.md) holding instances of [String](../java/lang/String.md). <br /> | ||

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

The logical bounds of the text will be filled using this`Paint`, and then the text will be rendered on top of it (but see [SWAP_COLORS](../java/awt/font/TextAttribute.md)).

The visual bounds of the text is extended to include the logical bounds, if necessary. The outline is not affected. 
**See Also**

- [#SWAP_COLORS](../java/awt/font/TextAttribute.md) 

### BIDI_EMBEDDING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIDI_EMBEDDING: TextAttribute!
```

Attribute key for the embedding level of the text. Values are instances of**`Integer`** . The default value is`null`, indicating that the the Bidirectional algorithm should run without explicit embeddings.

Positive values 1 through 61 are*embedding* levels, negative values -1 through -61 are*override*levels. The value 0 means that the base line direction is used. These levels are passed in the embedding levels array to the constructor.

*Note:*When this attribute is present anywhere in a paragraph, then any Unicode bidi control characters (RLO, LRO, RLE, LRE, and PDF) in the paragraph are disregarded, and runs of text where this attribute is not present are treated as though it were present and had the value 0. 
**See Also**

- [java.text.Bidi](../java/text/Bidi.md) 

### CHAR_REPLACEMENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHAR_REPLACEMENT: TextAttribute!
```

Attribute key for a user-defined glyph to display in lieu of the font's standard glyph for a character. Values are intances of GraphicAttribute. The default value is null, indicating that the standard glyphs provided by the font should be used.

This attribute is used to reserve space for a graphic or other component embedded in a line of text. It is required for correct positioning of 'inline' components within a line when bidirectional reordering (see [java.text.Bidi](../java/text/Bidi.md)) is performed. Each character (Unicode code point) will be rendered using the provided GraphicAttribute. Typically, the characters to which this attribute is applied should be`\uFFFC`.

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

Glyphs will be rendered using this`Paint`regardless of the`Paint`value set on the`Graphics`(but see [SWAP_COLORS](../java/awt/font/TextAttribute.md)). 
**See Also**

- [#SWAP_COLORS](../java/awt/font/TextAttribute.md) 

### INPUT_METHOD_HIGHLIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_HIGHLIGHT: TextAttribute!
```

Attribute key for input method highlight styles. The default value is`null`, which means that input method styles should not be applied before rendering. 
**See Also**

- [java.text.Annotation](../java/text/Annotation.md) 

### INPUT_METHOD_UNDERLINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_UNDERLINE: TextAttribute!
```

Attribute key for input method underlines. Values are instances of**`Integer`** . The default value is`-1`, which means no underline.

Several constant values are provided, see [UNDERLINE_LOW_ONE_PIXEL](../java/awt/font/TextAttribute.md), [UNDERLINE_LOW_TWO_PIXEL](../java/awt/font/TextAttribute.md), [UNDERLINE_LOW_DOTTED](../java/awt/font/TextAttribute.md), [UNDERLINE_LOW_GRAY](../java/awt/font/TextAttribute.md), and [UNDERLINE_LOW_DASHED](../java/awt/font/TextAttribute.md).

This may be used in conjunction with [UNDERLINE](../java/awt/font/TextAttribute.md) if desired. The primary purpose is for use by input methods. Other use of these underlines for simple ornamentation might confuse users.

The input method underline affects both the visual bounds and the outline of the text. 

### JUSTIFICATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION: TextAttribute!
```

Attribute key for the justification of a paragraph. Values are instances of**`Number`**. The default value is 1, indicating that justification should use the full width provided. Values are pinned to the range \[0..1\].

The constants [JUSTIFICATION_FULL](../java/awt/font/TextAttribute.md) and [JUSTIFICATION_NONE](../java/awt/font/TextAttribute.md) are provided.

Specifies the fraction of the extra space to use when justification is requested on a`TextLayout`. For example, if the line is 50 points wide and it is requested to justify to 70 points, a value of 0.75 will pad to use three-quarters of the remaining space, or 15 points, so that the resulting line will be 65 points in length.

*Note:*This should have the same value for all the text in a paragraph, otherwise the behavior is undetermined. 

### JUSTIFICATION_FULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_FULL: Float!
```

Justify the line to the full requested width. This is the default value for`JUSTIFICATION`. 
**See Also**

- [#JUSTIFICATION](../java/awt/font/TextAttribute.md) 

### JUSTIFICATION_NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JUSTIFICATION_NONE: Float!
```

Do not allow the line to be justified. 
**See Also**

- [#JUSTIFICATION](../java/awt/font/TextAttribute.md) 

### KERNING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KERNING: TextAttribute!
```

Attribute key to request kerning. Values are instances of**`Integer`** . The default value is`0`, which does not request kerning.

The constant value [KERNING_ON](../java/awt/font/TextAttribute.md) is provided.

The default advances of single characters are not appropriate for some character sequences, for example "To" or "AWAY". Without kerning the adjacent characters appear to be separated by too much space. Kerning causes selected sequences of characters to be spaced differently for a more pleasing visual appearance. 

### KERNING_ON

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KERNING_ON: Int!
```

Request standard kerning. 
**See Also**

- [#KERNING](../java/awt/font/TextAttribute.md) 

### LIGATURES

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGATURES: TextAttribute!
```

Attribute key for enabling optional ligatures. Values are instances of**`Integer`** . The default value is`0`, which means do not use optional ligatures.

The constant value [LIGATURES_ON](../java/awt/font/TextAttribute.md) is defined.

Ligatures required by the writing system are always enabled. 

### LIGATURES_ON

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIGATURES_ON: Int!
```

Request standard optional ligatures. 
**See Also**

- [#LIGATURES](../java/awt/font/TextAttribute.md) 

### NUMERIC_SHAPING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMERIC_SHAPING: TextAttribute!
```

Attribute key for converting ASCII decimal digits to other decimal ranges. Values are instances of [NumericShaper](../java/awt/font/NumericShaper.md). The default is`null`, which means do not perform numeric shaping.

When a numeric shaper is defined, the text is first processed by the shaper before any other analysis of the text is performed.

*Note:*This should have the same value for all the text in the paragraph, otherwise the behavior is undetermined. 
**See Also**

- [java.awt.font.NumericShaper](../java/awt/font/NumericShaper.md) 

### POSTURE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSTURE: TextAttribute!
```

Attribute key for the posture of a font. Values are instances of**`Number`** . The default value is`POSTURE_REGULAR`.

Two constant values are provided, [POSTURE_REGULAR](../java/awt/font/TextAttribute.md) and [POSTURE_OBLIQUE](../java/awt/font/TextAttribute.md). The value`POSTURE_OBLIQUE`corresponds to the style value`Font.ITALIC`as passed to the`Font`constructor.

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

- [#POSTURE](../java/awt/font/TextAttribute.md) 

### POSTURE_REGULAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSTURE_REGULAR: Float!
```

The standard posture, upright. This is the default value for`POSTURE`. 
**See Also**

- [#POSTURE](../java/awt/font/TextAttribute.md) 

### RUN_DIRECTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUN_DIRECTION: TextAttribute!
```

Attribute key for the run direction of the line. Values are instances of**`Boolean`** . The default value is null, which indicates that the standard Bidi algorithm for determining run direction should be used with the value [java.text.Bidi#DIRECTION_DEFAULT_LEFT_TO_RIGHT](../java/text/Bidi.md).

The constants [RUN_DIRECTION_RTL](../java/awt/font/TextAttribute.md) and [RUN_DIRECTION_LTR](../java/awt/font/TextAttribute.md) are provided.

This determines the value passed to the constructor to select the primary direction of the text in the paragraph.

*Note:*This attribute should have the same value for all the text in a paragraph, otherwise the behavior is undetermined. 
**See Also**

- [java.text.Bidi](../java/text/Bidi.md) 

### RUN_DIRECTION_LTR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUN_DIRECTION_LTR: Boolean!
```

Left-to-right run direction. 
**See Also**

- [#RUN_DIRECTION](../java/awt/font/TextAttribute.md) 

### RUN_DIRECTION_RTL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RUN_DIRECTION_RTL: Boolean!
```

Right-to-left run direction. 
**See Also**

- [#RUN_DIRECTION](../java/awt/font/TextAttribute.md) 

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

The constant value [STRIKETHROUGH_ON](../java/awt/font/TextAttribute.md) is provided.

The strikethrough affects both the visual bounds and the outline of the text. 

### STRIKETHROUGH_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRIKETHROUGH_ON: Boolean!
```

A single strikethrough. 
**See Also**

- [#STRIKETHROUGH](../java/awt/font/TextAttribute.md) 

### SUPERSCRIPT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPERSCRIPT: TextAttribute!
```

Attribute key for superscripting and subscripting. Values are instances of**`Integer`**. The default value is 0, which means that no superscript or subscript is used.

Two constant values are provided, see [SUPERSCRIPT_SUPER](../java/awt/font/TextAttribute.md) and [SUPERSCRIPT_SUB](../java/awt/font/TextAttribute.md). These have the values 1 and -1 respectively. Values of greater magnitude define greater levels of superscript or subscripting, for example, 2 corresponds to super-superscript, 3 to super-super-superscript, and similarly for negative values and subscript, up to a level of 7 (or -7). Values beyond this range are reserved; behavior is platform-dependent.

`SUPERSCRIPT`can impact the ascent and descent of a font. The ascent and descent can never become negative, however. 

### SUPERSCRIPT_SUB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPERSCRIPT_SUB: Int!
```

Standard subscript. 
**See Also**

- [#SUPERSCRIPT](../java/awt/font/TextAttribute.md) 

### SUPERSCRIPT_SUPER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPERSCRIPT_SUPER: Int!
```

Standard superscript. 
**See Also**

- [#SUPERSCRIPT](../java/awt/font/TextAttribute.md) 

### SWAP_COLORS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SWAP_COLORS: TextAttribute!
```

Attribute key for swapping foreground and background`Paints`. Values are instances of**`Boolean`** . The default value is`false`, which means do not swap colors.

The constant value [SWAP_COLORS_ON](../java/awt/font/TextAttribute.md) is defined.

If the [FOREGROUND](../java/awt/font/TextAttribute.md) attribute is set, its`Paint`will be used as the background, otherwise the`Paint`currently on the`Graphics`will be used. If the [BACKGROUND](../java/awt/font/TextAttribute.md) attribute is set, its`Paint`will be used as the foreground, otherwise the system will find a contrasting color to the (resolved) background so that the text will be visible. 
**See Also**

- [#FOREGROUND](../java/awt/font/TextAttribute.md)
- [#BACKGROUND](../java/awt/font/TextAttribute.md) 

### SWAP_COLORS_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SWAP_COLORS_ON: Boolean!
```

Swap foreground and background. 
**See Also**

- [#SWAP_COLORS](../java/awt/font/TextAttribute.md) 

### TRACKING

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACKING: TextAttribute!
```

Attribute key to control tracking. Values are instances of**`Number`** . The default value is`0`, which means no additional tracking.

The constant values [TRACKING_TIGHT](../java/awt/font/TextAttribute.md) and [TRACKING_LOOSE](../java/awt/font/TextAttribute.md) are provided.

The tracking value is multiplied by the font point size and passed through the font transform to determine an additional amount to add to the advance of each glyph cluster. Positive tracking values will inhibit formation of optional ligatures. Tracking values are typically between`-0.1`and`0.3`; values outside this range are generally not desireable. 

### TRACKING_LOOSE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACKING_LOOSE: Float!
```

Perform loose tracking. 
**See Also**

- [#TRACKING](../java/awt/font/TextAttribute.md) 

### TRACKING_TIGHT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRACKING_TIGHT: Float!
```

Perform tight tracking. 
**See Also**

- [#TRACKING](../java/awt/font/TextAttribute.md) 

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

The constant value [UNDERLINE_ON](../java/awt/font/TextAttribute.md) is provided.

The underline affects both the visual bounds and the outline of the text. 

### UNDERLINE_LOW_DASHED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_DASHED: Int!
```

Single pixel dashed low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](../java/awt/font/TextAttribute.md) 

### UNDERLINE_LOW_DOTTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_DOTTED: Int!
```

Single pixel dotted low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](../java/awt/font/TextAttribute.md) 

### UNDERLINE_LOW_GRAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_GRAY: Int!
```

Double pixel gray low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](../java/awt/font/TextAttribute.md) 

### UNDERLINE_LOW_ONE_PIXEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_ONE_PIXEL: Int!
```

Single pixel solid low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](../java/awt/font/TextAttribute.md) 

### UNDERLINE_LOW_TWO_PIXEL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_LOW_TWO_PIXEL: Int!
```

Double pixel solid low underline. 
**See Also**

- [#INPUT_METHOD_UNDERLINE](../java/awt/font/TextAttribute.md) 

### UNDERLINE_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDERLINE_ON: Int!
```

Standard underline. 
**See Also**

- [#UNDERLINE](../java/awt/font/TextAttribute.md) 

### WEIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT: TextAttribute!
```

Attribute key for the weight of a font. Values are instances of**`Number`** . The default value is`WEIGHT_REGULAR`.

Several constant values are provided, see [WEIGHT_EXTRA_LIGHT](../java/awt/font/TextAttribute.md), [WEIGHT_LIGHT](../java/awt/font/TextAttribute.md), [WEIGHT_DEMILIGHT](../java/awt/font/TextAttribute.md), [WEIGHT_REGULAR](../java/awt/font/TextAttribute.md), [WEIGHT_SEMIBOLD](../java/awt/font/TextAttribute.md), [WEIGHT_MEDIUM](../java/awt/font/TextAttribute.md), [WEIGHT_DEMIBOLD](../java/awt/font/TextAttribute.md), [WEIGHT_BOLD](../java/awt/font/TextAttribute.md), [WEIGHT_HEAVY](../java/awt/font/TextAttribute.md), [WEIGHT_EXTRABOLD](../java/awt/font/TextAttribute.md), and [WEIGHT_ULTRABOLD](../java/awt/font/TextAttribute.md). The value`WEIGHT_BOLD`corresponds to the style value`Font.BOLD`as passed to the`Font`constructor.

The value is roughly the ratio of the stem width to that of the regular weight.

The system can interpolate the provided value. 

### WEIGHT_BOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_BOLD: Float!
```

The standard bold weight. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_DEMIBOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_DEMIBOLD: Float!
```

A moderately lighter weight than`WEIGHT_BOLD`. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_DEMILIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_DEMILIGHT: Float!
```

An intermediate weight between`WEIGHT_LIGHT`and`WEIGHT_STANDARD`. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_EXTRABOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_EXTRABOLD: Float!
```

An extra heavy weight. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_EXTRA_LIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_EXTRA_LIGHT: Float!
```

The lightest predefined weight. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_HEAVY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_HEAVY: Float!
```

A moderately heavier weight than`WEIGHT_BOLD`. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_LIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_LIGHT: Float!
```

The standard light weight. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_MEDIUM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_MEDIUM: Float!
```

An intermediate weight between`WEIGHT_REGULAR`and`WEIGHT_BOLD`. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_REGULAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_REGULAR: Float!
```

The standard weight. This is the default value for`WEIGHT`. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_SEMIBOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_SEMIBOLD: Float!
```

A moderately heavier weight than`WEIGHT_REGULAR`. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WEIGHT_ULTRABOLD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WEIGHT_ULTRABOLD: Float!
```

The heaviest predefined weight. 
**See Also**

- [#WEIGHT](../java/awt/font/TextAttribute.md) 

### WIDTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH: TextAttribute!
```

Attribute key for the width of a font. Values are instances of**`Number`** . The default value is`WIDTH_REGULAR`.

Several constant values are provided, see [WIDTH_CONDENSED](../java/awt/font/TextAttribute.md), [WIDTH_SEMI_CONDENSED](../java/awt/font/TextAttribute.md), [WIDTH_REGULAR](../java/awt/font/TextAttribute.md), [WIDTH_SEMI_EXTENDED](../java/awt/font/TextAttribute.md), [WIDTH_EXTENDED](../java/awt/font/TextAttribute.md).

The value is roughly the ratio of the advance width to that of the regular width.

The system can interpolate the provided value. 

### WIDTH_CONDENSED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_CONDENSED: Float!
```

The most condensed predefined width. 
**See Also**

- [#WIDTH](../java/awt/font/TextAttribute.md) 

### WIDTH_EXTENDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_EXTENDED: Float!
```

The most extended predefined width. 
**See Also**

- [#WIDTH](../java/awt/font/TextAttribute.md) 

### WIDTH_REGULAR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_REGULAR: Float!
```

The standard width. This is the default value for`WIDTH`. 
**See Also**

- [#WIDTH](../java/awt/font/TextAttribute.md) 

### WIDTH_SEMI_CONDENSED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_SEMI_CONDENSED: Float!
```

A moderately condensed width. 
**See Also**

- [#WIDTH](../java/awt/font/TextAttribute.md) 

### WIDTH_SEMI_EXTENDED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WIDTH_SEMI_EXTENDED: Float!
```

A moderately extended width. 
**See Also**

- [#WIDTH](../java/awt/font/TextAttribute.md)

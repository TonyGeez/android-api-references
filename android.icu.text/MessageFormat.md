# MessageFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageFormat

Kotlin| [Java](../android/icu/text/MessageFormat.md) 
| --- | --- |

```
open class MessageFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](../java/text/Format.md) |||
| | ↳ | [android.icu.text.UFormat](../android/icu/text/UFormat.md) ||
| | | ↳ | [android.icu.text.MessageFormat](../android/icu/text/MessageFormat.md) |
| --- | --- | --- | --- |

**\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](../java/text/MessageFormat.md). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

MessageFormat prepares strings for display to users, with optional arguments (variables/placeholders). The arguments can occur in any order, which is necessary for translation into languages with different grammars.

A MessageFormat is constructed from a*pattern*string with arguments in {curly braces} which will be replaced by formatted values.

`MessageFormat`differs from the other`Format`classes in that you create a`MessageFormat`object with one of its constructors (not with a`getInstance`style factory method). Factory methods aren't necessary because`MessageFormat`itself doesn't implement locale-specific behavior. Any locale-specific behavior is defined by the pattern that you provide and the subformats used for inserted arguments.

Arguments can be named (using identifiers) or numbered (using small ASCII-digit integers). Some of the API methods work only with argument numbers and throw an exception if the pattern has named arguments (see [usesNamedArguments()](../android/icu/text/MessageFormat.md))).

An argument might not specify any format type. In this case, a Number value is formatted with a default (for the locale) NumberFormat, a Date value is formatted with a default (for the locale) DateFormat, and for any other value its toString() value is used.

An argument might specify a "simple" type for which the specified Format object is created, cached and used.

An argument might have a "complex" type with nested MessageFormat sub-patterns. During formatting, one of these sub-messages is selected according to the argument value and recursively formatted.

After construction, a custom Format object can be set for a top-level argument, overriding the default formatting and parsing behavior for that argument. However, custom formatting can be achieved more simply by writing a typeless argument in the pattern string and supplying it with a preformatted string value.

When formatting, MessageFormat takes a collection of argument values and writes an output string. The argument values may be passed as an array (when the pattern contains only numbered arguments) or as a Map (which works for both named and numbered arguments).

Each argument is matched with one of the input values by array index or map key and formatted according to its pattern specification (or using a custom Format object if one was set). A numbered pattern argument is matched with a map key that contains that number as an ASCII-decimal-digit string (without leading zero).

### Patterns and Their Interpretation

`MessageFormat`uses patterns of the following form: 

```kotlin
message = messageText (argument messageText)*
  argument = noneArg | simpleArg | complexArg
  complexArg = choiceArg | pluralArg | selectArg | selectordinalArg
 
  noneArg = '{' argNameOrNumber '}'
  simpleArg = '{' argNameOrNumber ',' argType [',' argStyle] '}'
  choiceArg = '{' argNameOrNumber ',' "choice" ',' choiceStyle '}'
  pluralArg = '{' argNameOrNumber ',' "plural" ',' pluralStyle '}'
  selectArg = '{' argNameOrNumber ',' "select" ',' selectStyle '}'
  selectordinalArg = '{' argNameOrNumber ',' "selectordinal" ',' pluralStyle '}'
 
  choiceStyle: see <code><a docref="java.text.ChoiceFormat">ChoiceFormat</a></code>pluralStyle: see <code><a docref="android.icu.text.PluralFormat">PluralFormat</a></code>selectStyle: see <code><a docref="android.icu.text.SelectFormat">SelectFormat</a></code>argNameOrNumber = argName | argNumber
  argName = [^[[:Pattern_Syntax:][:Pattern_White_Space:]]]+
  argNumber = '0' | ('1'..'9' ('0'..'9')*)
 
  argType = "number" | "date" | "time" | "spellout" | "ordinal" | "duration"
  argStyle = "short" | "medium" | "long" | "full" | "integer" | "currency" | "percent" | argStyleText
  
```

- messageText can contain quoted literal strings including syntax characters. A quoted literal string begins with an ASCII apostrophe and a syntax character (usually a {curly brace}) and continues until the next single apostrophe. A double ASCII apostrophe inside or outside of a quoted string represents one literal apostrophe.
- Quotable syntax characters are the {curly braces} in all messageText parts, plus the '#' sign in a messageText immediately inside a pluralStyle, and the '|' symbol in a messageText immediately inside a choiceStyle.
| --- | --- |
- See also [MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md)
- In argStyleText, every single ASCII apostrophe begins and ends quoted literal text, and unquoted {curly braces} must occur in matched pairs.

Recommendation: Use the real apostrophe (single quote) character \\\\u2019 for human-readable text, and use the ASCII apostrophe (\\\\u0027 ' ) only in program syntax, like quoting in MessageFormat. See the annotations for U+0027 Apostrophe in The Unicode Standard.

The`choice`argument type is deprecated. Use`plural`arguments for proper plural selection, and`select`arguments for simple selection among a fixed set of choices.

The`argType`and`argStyle`values are used to create a`Format`instance for the format element. The following table shows how the values map to Format instances. Combinations not shown in the table are illegal. Any`argStyleText`must be a valid pattern string for the Format subclass used.

| argType | argStyle | resulting Format object |
|------------|---------------------------|----------------------------------------------------------------------------------------------------------------|
| *(none)* || `null` |
| `number` | *(none)* | `NumberFormat.getInstance(getLocale())` |
| `number` | `integer` | `NumberFormat.getIntegerInstance(getLocale())` |
| --- | --- | --- |
| `number` | `currency` | `NumberFormat.getCurrencyInstance(getLocale())` |
| `number` | `percent` | `NumberFormat.getPercentInstance(getLocale())` |
| `number` | *argStyleText* | `new DecimalFormat(argStyleText, new DecimalFormatSymbols(getLocale()))` |
| --- | --- | --- |
| `date` | *(none)* | `DateFormat.getDateInstance(DateFormat.DEFAULT, getLocale())` |
| `date` | `short` | `DateFormat.getDateInstance(DateFormat.SHORT, getLocale())` |
| `date` | `medium` | `DateFormat.getDateInstance(DateFormat.DEFAULT, getLocale())` |
| --- | --- | --- |
| `date` | `long` | `DateFormat.getDateInstance(DateFormat.LONG, getLocale())` |
| `date` | `full` | `DateFormat.getDateInstance(DateFormat.FULL, getLocale())` |
| `date` | *argStyleText* | `new SimpleDateFormat(argStyleText, getLocale())` |
| --- | --- | --- |
| `time` | *(none)* | `DateFormat.getTimeInstance(DateFormat.DEFAULT, getLocale())` |
| `time` | `short` | `DateFormat.getTimeInstance(DateFormat.SHORT, getLocale())` |
| `time` | `medium` | `DateFormat.getTimeInstance(DateFormat.DEFAULT, getLocale())` |
| --- | --- | --- |
| `time` | `long` | `DateFormat.getTimeInstance(DateFormat.LONG, getLocale())` |
| `time` | `full` | `DateFormat.getTimeInstance(DateFormat.FULL, getLocale())` |
| `time` | *argStyleText* | `new SimpleDateFormat(argStyleText, getLocale())` |
| --- | --- | --- |
| `spellout` | *argStyleText (optional)* | `new RuleBasedNumberFormat(getLocale(), RuleBasedNumberFormat.SPELLOUT) ` ` .setDefaultRuleset(argStyleText);` |
| `ordinal` | *argStyleText (optional)* | `new RuleBasedNumberFormat(getLocale(), RuleBasedNumberFormat.ORDINAL) ` ` .setDefaultRuleset(argStyleText);` |
| `duration` | *argStyleText (optional)* | `new RuleBasedNumberFormat(getLocale(), RuleBasedNumberFormat.DURATION) ` ` .setDefaultRuleset(argStyleText);` |
| --- | --- | --- |

#### Differences from java.text.MessageFormat

The ICU MessageFormat supports both named and numbered arguments, while the JDK MessageFormat only supports numbered arguments. Named arguments make patterns more readable.

ICU implements a more user-friendly apostrophe quoting syntax. In message text, an apostrophe only begins quoting literal text if it immediately precedes a syntax character (mostly {curly braces}). 
In the JDK MessageFormat, an apostrophe always begins quoting, which requires common text like "don't" and "aujourd'hui" to be written with doubled apostrophes like "don''t" and "aujourd''hui". For more details see [MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md).

ICU does not create a ChoiceFormat object for a choiceArg, pluralArg or selectArg but rather handles such arguments itself. The JDK MessageFormat does create and use a ChoiceFormat object (`new ChoiceFormat(argStyleText)`). The JDK does not support plural and select arguments at all.

#### Usage Information

Here are some examples of usage: 

```kotlin
Object[] arguments = {
      7,
      new Date(System.currentTimeMillis()),
      "a disturbance in the Force"
  };
 
  String result = MessageFormat.format(
      "At {1,time} on {1,date}, there was {2} on planet {0,number,integer}.",
      arguments);
 
  <em>output</em>: At 12:30 PM on Jul 3, 2053, there was a disturbance
            in the Force on planet 7.
 
  
```
Typically, the message format will come from resources, and the arguments will be dynamically set at runtime.

Example 2: 

```kotlin
Object[] testArgs = { 3, "MyDisk" };
 
  MessageFormat form = new MessageFormat(
      "The disk \"{1}\" contains {0} file(s).");
 
  System.out.println(form.format(testArgs));
 
  // output, with different testArgs
  <em>output</em>: The disk "MyDisk" contains 0 file(s).
  <em>output</em>: The disk "MyDisk" contains 1 file(s).
  <em>output</em>: The disk "MyDisk" contains 1,273 file(s).
  
```

For messages that include plural forms, you can use a plural argument: 

```kotlin
MessageFormat msgFmt = new MessageFormat(
      "{num_files, plural, " +
      "=0{There are no files on disk \"{disk_name}\".}" +
      "=1{There is one file on disk \"{disk_name}\".}" +
      "other{There are # files on disk \"{disk_name}\".}}",
      ULocale.ENGLISH);
  Map args = new HashMap();
  args.put("num_files", 0);
  args.put("disk_name", "MyDisk");
  System.out.println(msgFmt.format(args));
  args.put("num_files", 3);
  System.out.println(msgFmt.format(args));
 
  <em>output</em>:
  There are no files on disk "MyDisk".
  There are 3 files on "MyDisk".
  
```
See [PluralFormat](../android/icu/text/PluralFormat.md) and [PluralRules](../android/icu/text/PluralRules.md) for details.

#### Synchronization

MessageFormats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](../android/icu/text/MessageFormat.Field.md) Defines constants that are used as attribute keys in the`AttributedCharacterIterator`returned from`MessageFormat.formatToCharacterIterator`. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MessageFormat](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a MessageFormat for the default`FORMAT`locale and the specified pattern. |
| [MessageFormat](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Constructs a MessageFormat for the specified locale and pattern. |
| [MessageFormat](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Constructs a MessageFormat for the specified locale and pattern. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](../android/icu/text/MessageFormat.md))`(`pttrn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the pattern used by this message format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `aposMode:` ` [MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md)!`)` **\[icu\]**Sets the ApostropheMode and the pattern used by this message format. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [autoQuoteApostrophe](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Converts an 'apostrophe-friendly' pattern into a standard pattern. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/text/MessageFormat.md))`()` Creates and returns a copy of this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/text/MessageFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/MessageFormat.md))`(`arguments:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `result:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Formats a map or array of objects and appends the`MessageFormat`'s pattern, with format elements replaced by the formatted objects, to the provided`StringBuffer`. |
| --- | --- |
| [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/MessageFormat.md))`(`arguments:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `result:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Formats an array of objects and appends the`MessageFormat`'s pattern, with arguments replaced by the formatted objects, to the provided`StringBuffer`. |
| [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/MessageFormat.md))`(`arguments:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `result:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Formats a map of objects and appends the`MessageFormat`'s pattern, with arguments replaced by the formatted objects, to the provided`StringBuffer`. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `arguments:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Creates a MessageFormat with the given pattern and uses it to format the given arguments. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/MessageFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `arguments:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a MessageFormat with the given pattern and uses it to format the given arguments. |
| open [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | [formatToCharacterIterator](../android/icu/text/MessageFormat.md))`(`arguments:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an array of objects and inserts them into the`MessageFormat`'s pattern, producing an`AttributedCharacterIterator`. |
| open [MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md)! | [getApostropheMode](../android/icu/text/MessageFormat.md))`()` **\[icu\]** |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getArgumentNames](../android/icu/text/MessageFormat.md))`()` **\[icu\]**Returns the top-level argument names. |
| open [Format](../java/text/Format.md)! | [getFormatByArgumentName](../android/icu/text/MessageFormat.md))`(`argumentName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the first top-level format associated with the given argument name. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](../java/text/Format.md)!\>! | [getFormats](../android/icu/text/MessageFormat.md))`()` Returns the Format objects used for the format elements in the previously set pattern string. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](../java/text/Format.md)!\>! | [getFormatsByArgumentIndex](../android/icu/text/MessageFormat.md))`()` Returns the Format objects used for the values passed into`format`methods or returned from`parse`methods. |
| open [Locale](../java/util/Locale.md)! | [getLocale](../android/icu/text/MessageFormat.md))`()` Returns the locale that's used when creating or comparing subformats. |
| open [ULocale](../android/icu/util/ULocale.md)! | [getULocale](../android/icu/text/MessageFormat.md))`()` **\[icu\]**Returns the locale that's used when creating argument Format objects. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/text/MessageFormat.md))`()` Returns a hash code value for the object. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parse](../android/icu/text/MessageFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce an object array. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parse](../android/icu/text/MessageFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` Parses the string. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../android/icu/text/MessageFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` Parses text from a string to produce an object array or Map. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parseToMap](../android/icu/text/MessageFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Parses text from the beginning of the given string to produce a map from argument to values. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parseToMap](../android/icu/text/MessageFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` **\[icu\]**Parses the string, returning the results in a Map. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormat](../android/icu/text/MessageFormat.md))`(`formatElementIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newFormat:` ` [Format](../java/text/Format.md)!`)` Sets the Format object to use for the format element with the given format element index within the previously set pattern string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatByArgumentIndex](../android/icu/text/MessageFormat.md))`(`argumentIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newFormat:` ` [Format](../java/text/Format.md)!`)` Sets the Format object to use for the format elements within the previously set pattern string that use the given argument index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatByArgumentName](../android/icu/text/MessageFormat.md))`(`argumentName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `newFormat:` ` [Format](../java/text/Format.md)!`)` **\[icu\]**Sets the Format object to use for the format elements within the previously set pattern string that use the given argument name. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormats](../android/icu/text/MessageFormat.md))`(`newFormats:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](../java/text/Format.md)!>!`)` Sets the Format objects to use for the format elements in the previously set pattern string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatsByArgumentIndex](../android/icu/text/MessageFormat.md))`(`newFormats:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](../java/text/Format.md)!>!`)` Sets the Format objects to use for the values passed into`format`methods or returned from`parse`methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatsByArgumentName](../android/icu/text/MessageFormat.md))`(`newFormats:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Format](../java/text/Format.md)!>!`)` **\[icu\]** Sets the Format objects to use for the values passed into`format`methods or returned from`parse`methods. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](../android/icu/text/MessageFormat.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Sets the locale to be used for creating argument Format objects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](../android/icu/text/MessageFormat.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Sets the locale to be used for creating argument Format objects. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](../android/icu/text/MessageFormat.md))`()` Returns the applied pattern string. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [usesNamedArguments](../android/icu/text/MessageFormat.md))`()` **\[icu\]**Returns true if this MessageFormat uses named arguments, and false otherwise. |

## Public constructors

### MessageFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessageFormat(pattern: String!)
```

Constructs a MessageFormat for the default`FORMAT`locale and the specified pattern. Sets the locale and calls applyPattern(pattern).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### MessageFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessageFormat(
    pattern: String!, 
    locale: ULocale!)
```

Constructs a MessageFormat for the specified locale and pattern. Sets the locale and calls applyPattern(pattern).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

### MessageFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessageFormat(
    pattern: String!, 
    locale: Locale!)
```

Constructs a MessageFormat for the specified locale and pattern. Sets the locale and calls applyPattern(pattern).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |
| `locale` | [Locale](../java/util/Locale.md)!:the locale for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

## Public methods

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pttrn: String!): Unit
```

Sets the pattern used by this message format. Parses the pattern and caches Format objects for simple argument types. Patterns and their interpretation are specified in the [class description](../android/icu/text/MessageFormat.md).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `pttrn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(
    pattern: String!, 
    aposMode: MessagePattern.ApostropheMode!
): Unit
```

**\[icu\]** Sets the ApostropheMode and the pattern used by this message format. Parses the pattern and caches Format objects for simple argument types. Patterns and their interpretation are specified in the [class description](../android/icu/text/MessageFormat.md).

This method is best used only once on a given object to avoid confusion about the mode, and after constructing the object with an empty pattern string to minimize overhead.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |
| `aposMode` | [MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md)!:the new ApostropheMode |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |

**See Also**

- [android.icu.text.MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md) 

### autoQuoteApostrophe

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun autoQuoteApostrophe(pattern: String!): String!
```

**\[icu\]** Converts an 'apostrophe-friendly' pattern into a standard pattern.*This is obsolete for ICU 4.8 and higher MessageFormat pattern strings.* It can still be useful together with [java.text.MessageFormat](../java/text/MessageFormat.md).

See the class description for more about apostrophes and quoting, and differences between ICU and [java.text.MessageFormat](../java/text/MessageFormat.md).

[java.text.MessageFormat](../java/text/MessageFormat.md) and ICU 4.6 and earlier MessageFormat treat all ASCII apostrophes as quotes, which is problematic in some languages, e.g. French, where apostrophe is commonly used. This utility assumes that only an unpaired apostrophe immediately before a brace is a true quote. Other unpaired apostrophes are paired, and the resulting standard pattern string is returned.

**Note**: It is not guaranteed that the returned pattern is indeed a valid pattern. The only effect is to convert between patterns having different quoting semantics.

**Note**: This method only works on top-level messageText, not messageText nested inside a complexArg.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the 'apostrophe-friendly' pattern to convert |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the standard equivalent of the original pattern |

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates and returns a copy of this object.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    arguments: Any!, 
    result: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats a map or array of objects and appends the`MessageFormat`'s pattern, with format elements replaced by the formatted objects, to the provided`StringBuffer`. This is equivalent to either of [format](../android/icu/text/MessageFormat.md))`((Object[]) arguments, result, pos)` [format](../android/icu/text/MessageFormat.md))`((Map) arguments, result, pos)`A map must be provided if this format uses named arguments, otherwise an IllegalArgumentException will be thrown.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | where the text is to be appended |
| `pos` | [FieldPosition](../java/text/FieldPosition.md)!:On input: an alignment field, if desired On output: the offsets of the alignment field |
| --- | --- |
| `arguments` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a map or array of objects to be formatted |
| `result` | [StringBuffer](../java/lang/StringBuffer.md)!:where text is appended |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](../java/lang/StringBuffer.md)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if`arguments`is an array of Object and this format uses named arguments |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    arguments: Array<Any!>!, 
    result: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats an array of objects and appends the`MessageFormat`'s pattern, with arguments replaced by the formatted objects, to the provided`StringBuffer`.

The text substituted for the individual format elements is derived from the current subformat of the format element and the`arguments`element at the format element's argument index as indicated by the first matching line of the following table. An argument is*unavailable* if`arguments`is`null`or has fewer than argumentIndex+1 elements. When an argument is unavailable no substitution is performed.

| argType or Format | value object | Formatted Text |
|------------------------------------|---------------------|----------------------------------------------------------------------------------------------------|
| *any* | *unavailable* | `"{" + argNameOrNumber + "}"` |
| *any* | `null` | `"null"` |
| custom Format`!= null` | *any* | `customFormat.format(argument)` |
| --- | --- | --- |
| noneArg, or custom Format`== null` | `instanceof Number` | `NumberFormat.getInstance(getLocale()).format(argument)` |
| noneArg, or custom Format`== null` | `instanceof Date` | `DateFormat.getDateTimeInstance(DateFormat.SHORT, DateFormat.SHORT, getLocale()).format(argument)` |
| noneArg, or custom Format`== null` | `instanceof String` | `argument` |
| --- | --- | --- |
| noneArg, or custom Format`== null` | *any* | `argument.toString()` |
| complexArg | *any* | result of recursive formatting of a selected sub-message |

If`pos`is non-null, and refers to`Field.ARGUMENT`, the location of the first formatted string will be returned. This method is only supported when the format does not use named arguments, otherwise an IllegalArgumentException is thrown.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `arguments` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:an array of objects to be formatted and substituted. |
| `result` | [StringBuffer](../java/lang/StringBuffer.md)!:where text is appended. |
| `pos` | [FieldPosition](../java/text/FieldPosition.md)!:On input: an alignment field, if desired. On output: the offsets of the alignment field. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    arguments: MutableMap<String!, Any!>!, 
    result: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats a map of objects and appends the`MessageFormat`'s pattern, with arguments replaced by the formatted objects, to the provided`StringBuffer`.

The text substituted for the individual format elements is derived from the current subformat of the format element and the`arguments`value corresponding to the format element's argument name.

A numbered pattern argument is matched with a map key that contains that number as an ASCII-decimal-digit string (without leading zero).

An argument is*unavailable* if`arguments`is`null`or does not have a value corresponding to an argument name in the pattern. When an argument is unavailable no substitution is performed.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `arguments` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:a map of objects to be formatted and substituted. |
| `result` | [StringBuffer](../java/lang/StringBuffer.md)!:where text is appended. |
| `pos` | [FieldPosition](../java/text/FieldPosition.md)!:On input: an alignment field, if desired. On output: the offsets of the alignment field. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------|
| [StringBuffer](../java/lang/StringBuffer.md)! | the passed-in StringBuffer |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if a value in the`arguments`array is not of the type expected by the corresponding argument or custom Format object. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun format(
    pattern: String!, 
    vararg arguments: Any!
): String!
```

Creates a MessageFormat with the given pattern and uses it to format the given arguments. This is equivalent to`(new ` [MessageFormat](../android/icu/text/MessageFormat.md))`(pattern)).` [format](../android/icu/text/MessageFormat.md))`(arguments, new StringBuffer(), null).toString()`

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun format(
    pattern: String!, 
    arguments: MutableMap<String!, Any!>!
): String!
```

Creates a MessageFormat with the given pattern and uses it to format the given arguments. The pattern must identifyarguments by name instead of by number.

<br />

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if a value in the`arguments`array is not of the type expected by the corresponding argument or custom Format object. |

**See Also**

- [#format(Map, StringBuffer, FieldPosition)](../android/icu/text/MessageFormat.md))
- [#format(String, Object[])](https://developer.android.com/reference/kotlin/android/icu/text/MessageFormat#format(kotlin.String,%20kotlin.Any)) 

### formatToCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatToCharacterIterator(arguments: Any!): AttributedCharacterIterator!
```

Formats an array of objects and inserts them into the`MessageFormat`'s pattern, producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String.

The text of the returned`AttributedCharacterIterator`is the same that would be returned by
[format](../android/icu/text/MessageFormat.md))`(arguments, new StringBuffer(), null).toString()`

In addition, the`AttributedCharacterIterator`contains at least attributes indicating where text was generated from an argument in the`arguments`array. The keys of these attributes are of type`MessageFormat.Field`, their values are`Integer`objects indicating the index in the`arguments`array of the argument from which the text was generated.

The attributes/value from the underlying`Format`instances that`MessageFormat`uses will also be placed in the resulting`AttributedCharacterIterator`. This allows you to not only find where an argument is placed in the resulting String, but also which fields it contains in turn.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `arguments` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:an array of objects to be formatted and substituted. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if obj is null. |
| `java.lang.IllegalArgumentException` | if a value in the`arguments`array is not of the type expected by the corresponding argument or custom Format object. |
| `java.lang.NullPointerException` | if`arguments`is null. |
| --- | --- |

### getApostropheMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getApostropheMode(): MessagePattern.ApostropheMode!
```

**\[icu\]**

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MessagePattern.ApostropheMode](../android/icu/text/MessagePattern.ApostropheMode.md)! | this instance's ApostropheMode. |

### getArgumentNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getArgumentNames(): MutableSet<String!>!
```

**\[icu\]** Returns the top-level argument names. For more details, see [setFormatByArgumentName(java.lang.String,java.text.Format)](../android/icu/text/MessageFormat.md)).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a Set of argument names |

### getFormatByArgumentName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormatByArgumentName(argumentName: String!): Format!
```

**\[icu\]** Returns the first top-level format associated with the given argument name. For more details, see [setFormatByArgumentName(java.lang.String,java.text.Format)](../android/icu/text/MessageFormat.md)).

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------|
| `argumentName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the desired argument. |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Format](../java/text/Format.md)! | the Format associated with the name, or null if there isn't one. |

### getFormats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormats(): Array<Format!>!
```

Returns the Format objects used for the format elements in the previously set pattern string. The order of formats in the returned array corresponds to the order of format elements in the pattern string.

Since the order of format elements in a pattern string often changes during localization, it's generally better to use the [getFormatsByArgumentIndex()](../android/icu/text/MessageFormat.md))method, which assumes an order of formats corresponding to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods. This method is only supported when exclusively numbers are used for argument names. Otherwise an IllegalArgumentException is thrown.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](../java/text/Format.md)!>! | the formats used for the format elements in the pattern |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### getFormatsByArgumentIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormatsByArgumentIndex(): Array<Format!>!
```

Returns the Format objects used for the values passed into`format`methods or returned from`parse`methods. The indices of elements in the returned array correspond to the argument indices used in the previously set pattern string. The order of formats in the returned array thus corresponds to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

If an argument index is used for more than one format element in the pattern string, then the format used for the last such format element is returned in the array. If an argument index is not used for any format element in the pattern string, then null is returned in the array. This method is only supported when exclusively numbers are used for argument names. Otherwise an IllegalArgumentException is thrown.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](../java/text/Format.md)!>! | the formats used for the arguments within the pattern |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### getLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): Locale!
```

Returns the locale that's used when creating or comparing subformats.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Locale](../java/util/Locale.md)! | the locale used when creating or comparing subformats |

### getULocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getULocale(): ULocale!
```

**\[icu\]**Returns the locale that's used when creating argument Format objects.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ULocale](../android/icu/util/ULocale.md)! | the locale used when creating or comparing subformats |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(source: String!): Array<Any!>!
```

Parses text from the beginning of the given string to produce an object array. The method may not use the entire text of the given string.

See the [parse(java.lang.String,java.text.ParsePosition)](../android/icu/text/MessageFormat.md))method for more information on message parsing.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`whose beginning should be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | An`Object`array parsed from the string. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    source: String!, 
    pos: ParsePosition!
): Array<Any!>!
```

Parses the string.

Caveats: The parse may fail in a number of circumstances. For example:

- If one of the arguments does not occur in the pattern.
- If the format of an argument loses information, such as with a choice format where a large number formats to "many".
- Does not yet handle recursion (where the substituted strings contain {n} references.)
- Will not always find a match (or the correct match) if some part of the parse is ambiguous. For example, if the pattern "{1},{2}" is used with the string arguments {"a,b", "c"}, it will format as "a,b,c". When the result is parsed, it will return {"a", "b,c"}.
- If a single argument is parsed more than once in the string, then the later parse wins.

When the parse fails, use ParsePosition.getErrorIndex() to find out where in the string did the parsing failed. The returned error index is the starting offset of the sub-patterns that the string is comparing with. For example, if the parsing string "AAA {0} BBB" is comparing against the pattern "AAD {0} BBB", the error index is 0. When an error occurs, the call to this method will return null. If the source is null, return an empty array.

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

Parses text from a string to produce an object array or Map.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed object array is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

See the [parse(java.lang.String,java.text.ParsePosition)](../android/icu/text/MessageFormat.md))method for more information on message parsing.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`, part of which should be parsed. |
| `pos` | [ParsePosition](../java/text/ParsePosition.md)!:A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | An`Object`parsed from the string, either an array of Object, or a Map, depending on whether named arguments are used. This can be queried using`usesNamedArguments`. In case of error, returns null. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`pos`is null. |

### parseToMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseToMap(source: String!): MutableMap<String!, Any!>!
```

**\[icu\]**Parses text from the beginning of the given string to produce a map from argument to values. The method may not use the entire text of the given string.

See the [parse(java.lang.String,java.text.ParsePosition)](../android/icu/text/MessageFormat.md))method for more information on message parsing.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`whose beginning should be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | A`Map`parsed from the string. |

| Exceptions ||
|----------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |

**See Also**

- [#parseToMap(String, ParsePosition)](../android/icu/text/MessageFormat.md)) 

### parseToMap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseToMap(
    source: String!, 
    pos: ParsePosition!
): MutableMap<String!, Any!>!
```

**\[icu\]**Parses the string, returning the results in a Map. This is similar to the version that returns an array of Object. This supports both named and numbered arguments-- if numbered, the keys in the map are the corresponding ASCII-decimal-digit strings (e.g. "0", "1", "2"...).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text to parse |
| `pos` | [ParsePosition](../java/text/ParsePosition.md)!:the position at which to start parsing. on return, contains the result of the parse. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a Map containing key/value pairs for each parsed argument. |

### setFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormat(
    formatElementIndex: Int, 
    newFormat: Format!
): Unit
```

Sets the Format object to use for the format element with the given format element index within the previously set pattern string. The format element index is the zero-based number of the format element counting from the start of the pattern string.

Since the order of format elements in a pattern string often changes during localization, it is generally better to use the [setFormatByArgumentIndex](../android/icu/text/MessageFormat.md))method, which accesses format elements based on the argument index they specify.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `formatElementIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of a format element within the pattern |
| `newFormat` | [Format](../java/text/Format.md)!:the format to use for the specified format element |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if formatElementIndex is equal to or larger than the number of format elements in the pattern string |

### setFormatByArgumentIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatByArgumentIndex(
    argumentIndex: Int, 
    newFormat: Format!
): Unit
```

Sets the Format object to use for the format elements within the previously set pattern string that use the given argument index. The argument index is part of the format element definition and represents an index into the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

If the argument index is used for more than one format element in the pattern string, then the new format is used for all such format elements. If the argument index is not used for any format element in the pattern string, then the new format is ignored. This method is only supported when exclusively numbers are used for argument names. Otherwise an IllegalArgumentException is thrown.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `argumentIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the argument index for which to use the new format |
| `newFormat` | [Format](../java/text/Format.md)!:the new format to use |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if this format uses named arguments |

### setFormatByArgumentName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatByArgumentName(
    argumentName: String!, 
    newFormat: Format!
): Unit
```

**\[icu\]**Sets the Format object to use for the format elements within the previously set pattern string that use the given argument name.

If the argument name is used for more than one format element in the pattern string, then the new format is used for all such format elements. If the argument name is not used for any format element in the pattern string, then the new format is ignored.

This API may be used on formats that do not use named arguments. In this case`argumentName`should be a String that names an argument index, e.g. "0", "1", "2"... etc. If it does not name a valid index, the format will be ignored. No error is thrown.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `argumentName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the argument to change |
| `newFormat` | [Format](../java/text/Format.md)!:the new format to use |

### setFormats

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormats(newFormats: Array<Format!>!): Unit
```

Sets the Format objects to use for the format elements in the previously set pattern string. The order of formats in`newFormats`corresponds to the order of format elements in the pattern string.

If more formats are provided than needed by the pattern string, the remaining ones are ignored. If fewer formats are provided than needed, then only the first`newFormats.length`formats are replaced.

Since the order of format elements in a pattern string often changes during localization, it is generally better to use the [setFormatsByArgumentIndex](../android/icu/text/MessageFormat.md))method, which assumes an order of formats corresponding to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newFormats` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](../java/text/Format.md)!\>!:the new formats to use |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`newFormats`is null |

### setFormatsByArgumentIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatsByArgumentIndex(newFormats: Array<Format!>!): Unit
```

Sets the Format objects to use for the values passed into`format`methods or returned from`parse`methods. The indices of elements in`newFormats`correspond to the argument indices used in the previously set pattern string. The order of formats in`newFormats`thus corresponds to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

If an argument index is used for more than one format element in the pattern string, then the corresponding new format is used for all such format elements. If an argument index is not used for any format element in the pattern string, then the corresponding new format is ignored. If fewer formats are provided than needed, then only the formats for argument indices less than`newFormats.length`are replaced. This method is only supported if the format does not use named arguments, otherwise an IllegalArgumentException is thrown.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newFormats` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](../java/text/Format.md)!\>!:the new formats to use |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | if`newFormats`is null |
| `java.lang.IllegalArgumentException` | if this formatter uses named arguments |

### setFormatsByArgumentName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatsByArgumentName(newFormats: MutableMap<String!, Format!>!): Unit
```

**\[icu\]** Sets the Format objects to use for the values passed into`format`methods or returned from`parse`methods. The keys in`newFormats`are the argument names in the previously set pattern string, and the values are the formats.

Only argument names from the pattern string are considered. Extra keys in`newFormats`that do not correspond to an argument name are ignored. Similarly, if there is no format in newFormats for an argument name, the formatter for that argument remains unchanged.

This may be called on formats that do not use named arguments. In this case the map will be queried for key Strings that represent argument indices, e.g. "0", "1", "2" etc.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newFormats` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Format](../java/text/Format.md)!\>!:a map from String to Format providing new formats for named arguments. |

### setLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocale(locale: ULocale!): Unit
```

Sets the locale to be used for creating argument Format objects. This affects subsequent calls to the #applyPattern method as well as to the`format`and [formatToCharacterIterator](../android/icu/text/MessageFormat.md))methods.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale to be used when creating or comparing subformats |

### setLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocale(locale: Locale!): Unit
```

Sets the locale to be used for creating argument Format objects. This affects subsequent calls to the #applyPattern method as well as to the`format`and [formatToCharacterIterator](../android/icu/text/MessageFormat.md))methods.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale to be used when creating or comparing subformats |

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Returns the applied pattern string.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern string |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | after custom Format objects have been set via setFormat() or similar APIs |

### usesNamedArguments

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun usesNamedArguments(): Boolean
```

**\[icu\]**Returns true if this MessageFormat uses named arguments, and false otherwise. See class description.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if named arguments are used. |

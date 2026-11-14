# MessageFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MessageFormat

```
open class MessageFormat : Format
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format) ||
| | ↳ | [java.text.MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat#) |

provides a means to produce concatenated messages in a language-neutral way. Use this to construct messages displayed for end users.

`MessageFormat`takes a set of objects, formats them, then inserts the formatted strings into the pattern at the appropriate places.

**Note:** `MessageFormat`differs from the other`Format`classes in that you create a`MessageFormat`object with one of its constructors (not with a`getInstance`style factory method). The factory methods aren't necessary because`MessageFormat`itself doesn't implement locale specific behavior. Any locale specific behavior is defined by the pattern that you provide as well as the subformats used for inserted arguments.

## Patterns and Their Interpretation

`MessageFormat`uses patterns of the following form: 

```kotlin
<i>MessageFormatPattern:</i><i>String</i><i>MessageFormatPattern</i><i>FormatElement</i><i>String</i><i>FormatElement:</i>{ <i>ArgumentIndex</i>}
          { <i>ArgumentIndex</i>, <i>FormatType</i>}
          { <i>ArgumentIndex</i>, <i>FormatType</i>, <i>FormatStyle</i>}
 
  <i>FormatType: one of </i>number date time choice
 
  <i>FormatStyle:</i>short
          medium
          long
          full
          integer
          currency
          percent
          <i>SubformatPattern</i>
```

Within a*String* , a pair of single quotes can be used to quote any arbitrary characters except single quotes. For example, pattern string`"'{0}'"`represents string`"{0}"`, not a*FormatElement* . A single quote itself must be represented by doubled single quotes`''`throughout a*String* . For example, pattern string`"'{''}'"`is interpreted as a sequence of`'{`(start of quoting and a left curly brace),`''`(a single quote), and`}'`(a right curly brace and end of quoting),*not* `'{'`and`'}'`(quoted left and right curly braces): representing string`"{'}"`,*not* `"{}"`.

A*SubformatPattern* is interpreted by its corresponding subformat, and subformat-dependent pattern rules apply. For example, pattern string`"{1,number,$'#',##}"`(*SubformatPattern* with underline) will produce a number format with the pound-sign quoted, with a result such as:`"$#31,45"`. Refer to each`Format`subclass documentation for details.

Any unmatched quote is treated as closed at the end of the given pattern. For example, pattern string`"'{0}"`is treated as pattern`"'{0}'"`.

Any curly braces within an unquoted pattern must be balanced. For example,`"ab {0} de"`and`"ab '}' de"`are valid patterns, but`"ab {0'}' de"`,`"ab } de"`and`"''{''"`are not.

**Warning:**
: The rules for using quotes within message format patterns unfortunately have shown to be somewhat confusing. In particular, it isn't always obvious to localizers whether single quotes need to be doubled or not. Make sure to inform localizers about the rules, and tell them (for example, by using comments in resource bundle source files) which strings will be processed by`MessageFormat`. Note that localizers may need to use single quotes in translated strings where the original version doesn't have them.

The*ArgumentIndex* value is a non-negative integer written using the digits`'0'`through`'9'`, and represents an index into the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

The*FormatType* and*FormatStyle* values are used to create a`Format`instance for the format element. The following table shows how the values map to`Format`instances. Combinations not shown in the table are illegal. A*SubformatPattern* must be a valid pattern string for the`Format`subclass used.

| FormatType | FormatStyle | Subformat Created |
| --- | --- | --- |
| *(none)* | *(none)* | `null` |
| `number` | *(none)* | [NumberFormat.getInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getInstance(java.util.Locale))`(getLocale())` |
| `number` | `integer` | [NumberFormat.getIntegerInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance(java.util.Locale))`(getLocale())` |
| --- | --- | --- |
| `number` | `currency` | [NumberFormat.getCurrencyInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance(java.util.Locale))`(getLocale())` |
| `number` | `percent` | [NumberFormat.getPercentInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance(java.util.Locale))`(getLocale())` |
| `number` | *SubformatPattern* | `new` [DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat#DecimalFormat(kotlin.String,%20java.text.DecimalFormatSymbols))`(subformatPattern,` [DecimalFormatSymbols.getInstance](https://developer.android.com/reference/kotlin/java/text/DecimalFormatSymbols#getInstance(java.util.Locale))`(getLocale()))` |
| --- | --- | --- |
| `date` | *(none)* | [DateFormat.getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.DEFAULT](https://developer.android.com/reference/kotlin/java/text/DateFormat#DEFAULT:kotlin.Int)`, getLocale())` |
| `date` | `short` | [DateFormat.getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.SHORT](https://developer.android.com/reference/kotlin/java/text/DateFormat#SHORT:kotlin.Int)`, getLocale())` |
| `date` | `medium` | [DateFormat.getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.DEFAULT](https://developer.android.com/reference/kotlin/java/text/DateFormat#DEFAULT:kotlin.Int)`, getLocale())` |
| --- | --- | --- |
| `date` | `long` | [DateFormat.getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.LONG](https://developer.android.com/reference/kotlin/java/text/DateFormat#LONG:kotlin.Int)`, getLocale())` |
| `date` | `full` | [DateFormat.getDateInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getDateInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.FULL](https://developer.android.com/reference/kotlin/java/text/DateFormat#FULL:kotlin.Int)`, getLocale())` |
| `date` | *SubformatPattern* | `new` [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.util.Locale))`(subformatPattern, getLocale())` |
| --- | --- | --- |
| `time` | *(none)* | [DateFormat.getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.DEFAULT](https://developer.android.com/reference/kotlin/java/text/DateFormat#DEFAULT:kotlin.Int)`, getLocale())` |
| `time` | `short` | [DateFormat.getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.SHORT](https://developer.android.com/reference/kotlin/java/text/DateFormat#SHORT:kotlin.Int)`, getLocale())` |
| `time` | `medium` | [DateFormat.getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.DEFAULT](https://developer.android.com/reference/kotlin/java/text/DateFormat#DEFAULT:kotlin.Int)`, getLocale())` |
| --- | --- | --- |
| `time` | `long` | [DateFormat.getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.LONG](https://developer.android.com/reference/kotlin/java/text/DateFormat#LONG:kotlin.Int)`, getLocale())` |
| `time` | `full` | [DateFormat.getTimeInstance](https://developer.android.com/reference/kotlin/java/text/DateFormat#getTimeInstance(kotlin.Int,%20java.util.Locale))`(` [DateFormat.FULL](https://developer.android.com/reference/kotlin/java/text/DateFormat#FULL:kotlin.Int)`, getLocale())` |
| `time` | *SubformatPattern* | `new` [SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat#SimpleDateFormat(kotlin.String,%20java.util.Locale))`(subformatPattern, getLocale())` |
| --- | --- | --- |
| `choice` | *SubformatPattern* | `new` [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#ChoiceFormat(kotlin.String))`(subformatPattern)` |
|------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

### Usage Information

Here are some examples of usage. In real internationalized programs, the message format pattern and other static strings will, of course, be obtained from resource bundles. Other parameters will be dynamically determined at runtime.

The first example uses the static method`MessageFormat.format`, which internally creates a`MessageFormat`for one-time use: 

```kotlin
int planet = 7;
  String event = "a disturbance in the Force";
 
  String result = MessageFormat.format(
      "At {1,time} on {1,date}, there was {2} on planet {0,number,integer}.",
      planet, new Date(), event);
  
```
The output is: 

```kotlin
At 12:30 PM on Jul 3, 2053, there was a disturbance in the Force on planet 7.
  
```

The following example creates a`MessageFormat`instance that can be used repeatedly: 

```kotlin
int fileCount = 1273;
  String diskName = "MyDisk";
  Object[] testArgs = {new Long(fileCount), diskName};
 
  MessageFormat form = new MessageFormat(
      "The disk \"{1}\" contains {0} file(s).");
 
  System.out.println(form.format(testArgs));
  
```
The output with different values for`fileCount`: 

```kotlin
The disk "MyDisk" contains 0 file(s).
  The disk "MyDisk" contains 1 file(s).
  The disk "MyDisk" contains 1,273 file(s).
  
```

For more sophisticated patterns, you can use a`ChoiceFormat`to produce correct forms for singular and plural: 

```kotlin
MessageFormat form = new MessageFormat("The disk \"{1}\" contains {0}.");
  double[] filelimits = {0,1,2};
  String[] filepart = {"no files","one file","{0,number} files"};
  ChoiceFormat fileform = new ChoiceFormat(filelimits, filepart);
  form.setFormatByArgumentIndex(0, fileform);
 
  int fileCount = 1273;
  String diskName = "MyDisk";
  Object[] testArgs = {new Long(fileCount), diskName};
 
  System.out.println(form.format(testArgs));
  
```
The output with different values for`fileCount`: 

```kotlin
The disk "MyDisk" contains no files.
  The disk "MyDisk" contains one file.
  The disk "MyDisk" contains 1,273 files.
  
```

You can create the`ChoiceFormat`programmatically, as in the above example, or by using a pattern. See [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat) for more information. 

```kotlin
<code>form.applyPattern(
     "There {0,choice,0#are no files|1#is one file|1&lt;are {0,number,integer} files}.");
  </code>
```

**Note:** As we see above, the string produced by a`ChoiceFormat`in`MessageFormat`is treated as special; occurrences of '{' are used to indicate subformats, and cause recursion. If you create both a`MessageFormat`and`ChoiceFormat`programmatically (instead of using the string patterns), then be careful not to produce a format that recurses on itself, which will cause an infinite loop.

When a single argument is parsed more than once in the string, the last match will be the final result of the parsing. For example, 

```kotlin
MessageFormat mf = new MessageFormat("{0,number,#.##}, {0,number,#.#}");
  Object[] objs = {new Double(3.1415)};
  String result = mf.format( objs );
  // result now equals "3.14, 3.1"
  objs = null;
  objs = mf.parse(result, new ParsePosition(0));
  // objs now equals {new Double(3.1)}
  
```

Likewise, parsing with a`MessageFormat`object using patterns containing multiple occurrences of the same argument would return the last match. For example, 

```kotlin
MessageFormat mf = new MessageFormat("{0}, {0}, {0}");
  String forParsing = "x, y, z";
  Object[] objs = mf.parse(forParsing, new ParsePosition(0));
  // result now equals {new String("z")}
  
```

### Synchronization

Message formats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](https://developer.android.com/reference/kotlin/java/text/MessageFormat.Field) Defines constants that are used as attribute keys in the`AttributedCharacterIterator`returned from`MessageFormat.formatToCharacterIterator`. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat#MessageFormat(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a MessageFormat for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale and the specified pattern. |
| [MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat#MessageFormat(kotlin.String,%20java.util.Locale))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Constructs a MessageFormat for the specified locale and pattern. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](https://developer.android.com/reference/kotlin/java/text/MessageFormat#applyPattern(kotlin.String))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the pattern used by this message format. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/MessageFormat#clone())`()` Creates and returns a copy of this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/text/MessageFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Equality comparison between two message format objects |
| --- | --- |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/java/text/MessageFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`arguments:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `result:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)!`)` Formats an array of objects and appends the`MessageFormat`'s pattern, with format elements replaced by the formatted objects, to the provided`StringBuffer`. |
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/java/text/MessageFormat#format(kotlin.Array,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`arguments:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `result:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)!`)` Formats an array of objects and appends the`MessageFormat`'s pattern, with format elements replaced by the formatted objects, to the provided`StringBuffer`. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/MessageFormat#format(kotlin.String,%20kotlin.Any))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `arguments:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Creates a MessageFormat with the given pattern and uses it to format the given arguments. |
| --- | --- |
| open [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/MessageFormat#formatToCharacterIterator(kotlin.Any))`(`arguments:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an array of objects and inserts them into the`MessageFormat`'s pattern, producing an`AttributedCharacterIterator`. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!\>! | [getFormats](https://developer.android.com/reference/kotlin/java/text/MessageFormat#getFormats())`()` Gets the formats used for the format elements in the previously set pattern string. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!\>! | [getFormatsByArgumentIndex](https://developer.android.com/reference/kotlin/java/text/MessageFormat#getFormatsByArgumentIndex())`()` Gets the formats used for the values passed into`format`methods or returned from`parse`methods. |
| --- | --- |
| open [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | [getLocale](https://developer.android.com/reference/kotlin/java/text/MessageFormat#getLocale())`()` Gets the locale that's used when creating or comparing subformats. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/text/MessageFormat#hashCode())`()` Generates a hash code for the message format object. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parse](https://developer.android.com/reference/kotlin/java/text/MessageFormat#parse(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce an object array. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parse](https://developer.android.com/reference/kotlin/java/text/MessageFormat#parse(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)!`)` Parses the string. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/MessageFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)!`)` Parses text from a string to produce an object array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setFormat(kotlin.Int,%20java.text.Format))`(`formatElementIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newFormat:` ` [Format](https://developer.android.com/reference/kotlin/java/text/Format)!`)` Sets the format to use for the format element with the given format element index within the previously set pattern string. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatByArgumentIndex](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setFormatByArgumentIndex(kotlin.Int,%20java.text.Format))`(`argumentIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newFormat:` ` [Format](https://developer.android.com/reference/kotlin/java/text/Format)!`)` Sets the format to use for the format elements within the previously set pattern string that use the given argument index. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormats](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setFormats(kotlin.Array))`(`newFormats:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!>!`)` Sets the formats to use for the format elements in the previously set pattern string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFormatsByArgumentIndex](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setFormatsByArgumentIndex(kotlin.Array))`(`newFormats:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!>!`)` Sets the formats to use for the values passed into`format`methods or returned from`parse`methods. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLocale](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Sets the locale to be used when creating or comparing subformats. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](https://developer.android.com/reference/kotlin/java/text/MessageFormat#toPattern())`()` Returns a pattern representing the current state of the message format. |

| Inherited functions ||
|---|---|
| From class [Format](https://developer.android.com/reference/kotlin/java/text/Format) |-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an object to produce a string. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format#parseObject(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

## Public constructors

### MessageFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessageFormat(pattern: String!)
```

Constructs a MessageFormat for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale and the specified pattern. The constructor first sets the locale, then parses the pattern and creates a list of subformats for the format elements contained in it. Patterns and their interpretation are specified in the [class description](https://developer.android.com/reference/kotlin/java/text/MessageFormat#patterns).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |
| `java.lang.NullPointerException` | if`pattern`is`null` |

### MessageFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MessageFormat(
    pattern: String!, 
    locale: Locale!)
```

Constructs a MessageFormat for the specified locale and pattern. The constructor first sets the locale, then parses the pattern and creates a list of subformats for the format elements contained in it. Patterns and their interpretation are specified in the [class description](https://developer.android.com/reference/kotlin/java/text/MessageFormat#patterns).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |
| `java.lang.NullPointerException` | if`pattern`is`null` |

## Public methods

### applyPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pattern: String!): Unit
```

Sets the pattern used by this message format. The method parses the pattern and creates a list of subformats for the format elements contained in it. Patterns and their interpretation are specified in the [class description](https://developer.android.com/reference/kotlin/java/text/MessageFormat#patterns).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this message format |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid |
| `java.lang.NullPointerException` | if`pattern`is`null` |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Equality comparison between two message format objects

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    arguments: Any!, 
    result: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats an array of objects and appends the`MessageFormat`'s pattern, with format elements replaced by the formatted objects, to the provided`StringBuffer`. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/MessageFormat#format(kotlin.Array,%20java.lang.StringBuffer,%20java.text.FieldPosition))`((Object[]) arguments, result, pos)`

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | where the text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)!:keeps track on the position of the first replaced argument in the output string. |
| --- | --- |
| `arguments` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:an array of objects to be formatted and substituted. |
| `result` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!:where text is appended. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`result`is`null` |
| `java.lang.IllegalArgumentException` | if an argument in the`arguments`array is not of the type expected by the format element(s) that use it. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    arguments: Array<Any!>!, 
    result: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats an array of objects and appends the`MessageFormat`'s pattern, with format elements replaced by the formatted objects, to the provided`StringBuffer`.

The text substituted for the individual format elements is derived from the current subformat of the format element and the`arguments`element at the format element's argument index as indicated by the first matching line of the following table. An argument is*unavailable* if`arguments`is`null`or has fewer than argumentIndex+1 elements.

| Subformat | Argument | Formatted Text |
| --- | --- | --- |
| *any* | *unavailable* | `"{" + argumentIndex + "}"` |
| *any* | `null` | `"null"` |
| `instanceof ChoiceFormat` | *any* | `subformat.format(argument).indexOf('{') >= 0 ?` ` (new MessageFormat(subformat.format(argument), getLocale())).format(argument) : subformat.format(argument)` |
| --- | --- | --- |
| `!= null` | *any* | `subformat.format(argument)` |
| `null` | `instanceof Number` | `NumberFormat.getInstance(getLocale()).format(argument)` |
| `null` | `instanceof Date` | `DateFormat.getDateTimeInstance(DateFormat.SHORT, DateFormat.SHORT, getLocale()).format(argument)` |
| --- | --- | --- |
| `null` | `instanceof String` | `argument` |
| `null` | *any* | `argument.toString()` |
|---------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|

If`pos`is non-null, and refers to`Field.ARGUMENT`, the location of the first formatted string will be returned.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `arguments` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:an array of objects to be formatted and substituted. |
| `result` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!:where text is appended. |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)!:keeps track on the position of the first replaced argument in the output string. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | the string buffer passed in as`result`, with formatted text appended |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if an argument in the`arguments`array is not of the type expected by the format element(s) that use it. |
| `java.lang.NullPointerException` | if`result`is`null` |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun format(
    pattern: String!, 
    vararg arguments: Any!
): String!
```

Creates a MessageFormat with the given pattern and uses it to format the given arguments. This is equivalent to`(new ` [MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat#MessageFormat(kotlin.String))`(pattern)).` [format](https://developer.android.com/reference/kotlin/java/text/MessageFormat#format(kotlin.Array,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(arguments, new StringBuffer(), null).toString()`

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern string |
| `arguments` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:object(s) to format |

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the formatted string |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid, or if an argument in the`arguments`array is not of the type expected by the format element(s) that use it. |
| `java.lang.NullPointerException` | if`pattern`is`null` |

### formatToCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatToCharacterIterator(arguments: Any!): AttributedCharacterIterator!
```

Formats an array of objects and inserts them into the`MessageFormat`'s pattern, producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String.

The text of the returned`AttributedCharacterIterator`is the same that would be returned by
[format](https://developer.android.com/reference/kotlin/java/text/MessageFormat#format(kotlin.Array,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(arguments, new StringBuffer(), null).toString()`

In addition, the`AttributedCharacterIterator`contains at least attributes indicating where text was generated from an argument in the`arguments`array. The keys of these attributes are of type`MessageFormat.Field`, their values are`Integer`objects indicating the index in the`arguments`array of the argument from which the text was generated.

The attributes/value from the underlying`Format`instances that`MessageFormat`uses will also be placed in the resulting`AttributedCharacterIterator`. This allows you to not only find where an argument is placed in the resulting String, but also which fields it contains in turn.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `arguments` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:an array of objects to be formatted and substituted. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`arguments`is null. |
| `java.lang.IllegalArgumentException` | if an argument in the`arguments`array is not of the type expected by the format element(s) that use it. |

### getFormats

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormats(): Array<Format!>!
```

Gets the formats used for the format elements in the previously set pattern string. The order of formats in the returned array corresponds to the order of format elements in the pattern string.

Since the order of format elements in a pattern string often changes during localization, it's generally better to use the [getFormatsByArgumentIndex](https://developer.android.com/reference/kotlin/java/text/MessageFormat#getFormatsByArgumentIndex())method, which assumes an order of formats corresponding to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!>! | the formats used for the format elements in the pattern |

### getFormatsByArgumentIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormatsByArgumentIndex(): Array<Format!>!
```

Gets the formats used for the values passed into`format`methods or returned from`parse`methods. The indices of elements in the returned array correspond to the argument indices used in the previously set pattern string. The order of formats in the returned array thus corresponds to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

If an argument index is used for more than one format element in the pattern string, then the format used for the last such format element is returned in the array. If an argument index is not used for any format element in the pattern string, then null is returned in the array.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!>! | the formats used for the arguments within the pattern |

### getLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): Locale!
```

Gets the locale that's used when creating or comparing subformats.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | the locale used when creating or comparing subformats |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Generates a hash code for the message format object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(source: String!): Array<Any!>!
```

Parses text from the beginning of the given string to produce an object array. The method may not use the entire text of the given string.

See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/MessageFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on message parsing.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`whose beginning should be parsed. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | An`Object`array parsed from the string. |

| Exceptions ||
|----------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

When the parse fails, use ParsePosition.getErrorIndex() to find out where in the string the parsing failed. The returned error index is the starting offset of the sub-patterns that the string is comparing with. For example, if the parsing string "AAA {0} BBB" is comparing against the pattern "AAD {0} BBB", the error index is 0. When an error occurs, the call to this method will return null. If the source is null, return an empty array.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to parse |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)!:the parse position |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | an array of parsed objects |

| Exceptions ||
|----------------------------------|----------------------------------------------|
| `java.lang.NullPointerException` | if`pos`is`null`for a non-null`source`string. |

### parseObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

Parses text from a string to produce an object array.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed object array is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/MessageFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on message parsing.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A`String`, part of which should be parsed. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)!:A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | An`Object`array parsed from the string. In case of error, returns null. |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`pos`is null. |

### setFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormat(
    formatElementIndex: Int, 
    newFormat: Format!
): Unit
```

Sets the format to use for the format element with the given format element index within the previously set pattern string. The format element index is the zero-based number of the format element counting from the start of the pattern string.

Since the order of format elements in a pattern string often changes during localization, it is generally better to use the [setFormatByArgumentIndex](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setFormatByArgumentIndex(kotlin.Int,%20java.text.Format))method, which accesses format elements based on the argument index they specify.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `formatElementIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of a format element within the pattern |
| `newFormat` | [Format](https://developer.android.com/reference/kotlin/java/text/Format)!:the format to use for the specified format element |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if`formatElementIndex`is equal to or larger than the number of format elements in the pattern string |

### setFormatByArgumentIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatByArgumentIndex(
    argumentIndex: Int, 
    newFormat: Format!
): Unit
```

Sets the format to use for the format elements within the previously set pattern string that use the given argument index. The argument index is part of the format element definition and represents an index into the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

If the argument index is used for more than one format element in the pattern string, then the new format is used for all such format elements. If the argument index is not used for any format element in the pattern string, then the new format is ignored.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `argumentIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the argument index for which to use the new format |
| `newFormat` | [Format](https://developer.android.com/reference/kotlin/java/text/Format)!:the new format to use |

### setFormats

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormats(newFormats: Array<Format!>!): Unit
```

Sets the formats to use for the format elements in the previously set pattern string. The order of formats in`newFormats`corresponds to the order of format elements in the pattern string.

If more formats are provided than needed by the pattern string, the remaining ones are ignored. If fewer formats are provided than needed, then only the first`newFormats.length`formats are replaced.

Since the order of format elements in a pattern string often changes during localization, it is generally better to use the [setFormatsByArgumentIndex](https://developer.android.com/reference/kotlin/java/text/MessageFormat#setFormatsByArgumentIndex(kotlin.Array))method, which assumes an order of formats corresponding to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newFormats` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!\>!:the new formats to use |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`newFormats`is null |

### setFormatsByArgumentIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFormatsByArgumentIndex(newFormats: Array<Format!>!): Unit
```

Sets the formats to use for the values passed into`format`methods or returned from`parse`methods. The indices of elements in`newFormats`correspond to the argument indices used in the previously set pattern string. The order of formats in`newFormats`thus corresponds to the order of elements in the`arguments`array passed to the`format`methods or the result array returned by the`parse`methods.

If an argument index is used for more than one format element in the pattern string, then the corresponding new format is used for all such format elements. If an argument index is not used for any format element in the pattern string, then the corresponding new format is ignored. If fewer formats are provided than needed, then only the formats for argument indices less than`newFormats.length`are replaced.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newFormats` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Format](https://developer.android.com/reference/kotlin/java/text/Format)!\>!:the new formats to use |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`newFormats`is null |

### setLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLocale(locale: Locale!): Unit
```

Sets the locale to be used when creating or comparing subformats. This affects subsequent calls

- to the [applyPattern](https://developer.android.com/reference/kotlin/java/text/MessageFormat#applyPattern(kotlin.String))and [toPattern](https://developer.android.com/reference/kotlin/java/text/MessageFormat#toPattern())methods if format elements specify a format type and therefore have the subformats created in the`applyPattern`method, as well as
- to the`format`and [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/MessageFormat#formatToCharacterIterator(kotlin.Any))methods if format elements do not specify a format type and therefore have the subformats created in the formatting methods.

Subformats that have already been created are not affected.

<br />

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale to be used when creating or comparing subformats |

### toPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Returns a pattern representing the current state of the message format. The string is constructed from internal information and therefore does not necessarily equal the previously applied pattern.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a pattern representing the current state of the message format |

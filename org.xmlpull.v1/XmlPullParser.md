# XmlPullParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XmlPullParser

```
interface XmlPullParser
```

| [org.xmlpull.v1.XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#) |

| Known Direct Subclasses [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) |-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------| | [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser.html#) | The XML parsing interface returned for an XML resource. | |
| --- | --- | --- | --- | --- | --- | --- |

XML Pull Parser is an interface that defines parsing functionality provided in [XMLPULL V1 API](http://www.xmlpull.org/)(visit this website to learn more about API and its implementations).

There are following different kinds of parser depending on which features are set:

- **non-validating**parser as defined in XML 1.0 spec when FEATURE_PROCESS_DOCDECL is set to true
- **validating parser**as defined in XML 1.0 spec when FEATURE_VALIDATION is true (and that implies that FEATURE_PROCESS_DOCDECL is true)
- when FEATURE_PROCESS_DOCDECL is false (this is default and if different value is required necessary must be changed before parsing is started) then parser behaves like XML 1.0 compliant non-validating parser under condition that*no DOCDECL is present* in XML documents (internal entites can still be defined with defineEntityReplacementText()). This mode of operation is intended**for operation in constrained environments**such as J2ME.

There are two key methods: next() and nextToken(). While next() provides access to high level parsing events, nextToken() allows access to lower level tokens.

The current event state of the parser can be determined by calling the [getEventType()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getEventType())method. Initially, the parser is in the [START_DOCUMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#START_DOCUMENT) state.

The method [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())advances the parser to the next event. The int value returned from next determines the current parser state and is identical to the value returned from following calls to getEventType ().

Th following event types are seen by next()

[START_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#START_TAG)
: An XML start tag was read.

[TEXT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#TEXT)
: Text content was read; the text content can be retrieved using the getText() method. (when in validating mode next() will not report ignorable whitespace, use nextToken() instead)

[END_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_TAG)
: An end tag was read

[END_DOCUMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_DOCUMENT)
: No more events are available

after first next() or nextToken() (or any other next\*() method) is called user application can obtain XML version, standalone and encoding from XML declaration in following ways:

- **version** : getProperty("<http://xmlpull.org/v1/doc/properties.html#xmldecl-version>") returns String ("1.0") or null if XMLDecl was not read or if property is not supported
- **standalone** : getProperty("<http://xmlpull.org/v1/doc/properties.html#xmldecl-standalone>") returns Boolean: null if there was no standalone declaration or if property is not supported otherwise returns Boolean(true) if standalone="yes" and Boolean(false) when standalone="no"
- **encoding**: obtained from getInputEncoding() null if stream had unknown encoding (not set in setInputStream) and it was not declared in XMLDecl

A minimal example for using this API may look as follows: 

```kotlin
import java.io.IOException;
  import java.io.StringReader;
 
  import org.xmlpull.v1.XmlPullParser;
  import org.xmlpull.v1.<a href="XmlPullParserException.html">XmlPullParserException</a>;
  import org.xmlpull.v1.<a href="XmlPullParserFactory.html">XmlPullParserFactory</a>;
 
  public class SimpleXmlPullApp
  {
 
      public static void main (String args[])
          throws XmlPullParserException, IOException
      {
          XmlPullParserFactory factory = XmlPullParserFactory.newInstance();
          factory.setNamespaceAware(true);
          XmlPullParser xpp = factory.newPullParser();
 
          xpp.<a href="#setInput">setInput</a>( new StringReader ( "<foo>Hello World!</foo>" ) );
          int eventType = xpp.getEventType();
          while (eventType != XmlPullParser.END_DOCUMENT) {
           if(eventType == XmlPullParser.START_DOCUMENT) {
               System.out.println("Start document");
           } else if(eventType == XmlPullParser.START_TAG) {
               System.out.println("Start tag "+xpp.<a href="#getName()">getName()</a>);
           } else if(eventType == XmlPullParser.END_TAG) {
               System.out.println("End tag "+xpp.getName());
           } else if(eventType == XmlPullParser.TEXT) {
               System.out.println("Text "+xpp.<a href="#getText()">getText()</a>);
           }
           eventType = xpp.next();
          }
          System.out.println("End document");
      }
  }
  
```

The above example will generate the following output: 

```kotlin
Start document
  Start tag foo
  Text Hello World!
  End tag foo
  End document
  
```

For more details on API usage, please refer to the quick Introduction available at<http://www.xmlpull.org>

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CDSECT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#CDSECT:kotlin.Int) A CDATA sections was just read; this token is available only from calls to [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#COMMENT:kotlin.Int) An XML comment was just read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOCDECL](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#DOCDECL:kotlin.Int) An XML document type declaration was just read. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [END_DOCUMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_DOCUMENT:kotlin.Int) Logical end of the xml document. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [END_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_TAG:kotlin.Int) Returned from getEventType(), [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next()), or [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())when an end tag was read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ENTITY_REF](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#ENTITY_REF:kotlin.Int) An entity reference was just read; this token is available from [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())only. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_PROCESS_DOCDECL](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_PROCESS_DOCDECL:kotlin.String) This feature determines whether the document declaration is processed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_PROCESS_NAMESPACES](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_PROCESS_NAMESPACES:kotlin.String) This feature determines whether the parser processes namespaces. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_REPORT_NAMESPACE_ATTRIBUTES](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_REPORT_NAMESPACE_ATTRIBUTES:kotlin.String) This feature determines whether namespace attributes are exposed via the attribute access methods. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [FEATURE_VALIDATION](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_VALIDATION:kotlin.String) If this feature is activated, all validation errors as defined in the XML 1. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IGNORABLE_WHITESPACE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#IGNORABLE_WHITESPACE:kotlin.Int) Ignorable whitespace was just read. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NO_NAMESPACE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#NO_NAMESPACE:kotlin.String) This constant represents the default namespace (empty string "") |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROCESSING_INSTRUCTION](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#PROCESSING_INSTRUCTION:kotlin.Int) An XML processing instruction declaration was just read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [START_DOCUMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#START_DOCUMENT:kotlin.Int) Signalize that parser is at the very beginning of the document and nothing was read yet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [START_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#START_TAG:kotlin.Int) Returned from getEventType(), [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next()), [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())when a start tag was read. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TEXT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#TEXT:kotlin.Int) Character data was read and will is available by calling getText(). |

| Public methods ||
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [defineEntityReplacementText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#defineEntityReplacementText(kotlin.String,%20kotlin.String))`(`entityName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `replacementText:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set new value for entity replacement text as defined in [XML 1.0 Section 4.5 Construction of Internal Entity Replacement Text](http://www.w3.org/TR/REC-xml#intern-replacement). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAttributeCount](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeCount())`()` Returns the number of attributes of the current start tag, or -1 if the current event type is not START_TAG |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAttributeName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeName(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the local name of the specified attribute if namespaces are enabled or just attribute name if namespaces are disabled. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAttributeNamespace](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeNamespace(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the namespace URI of the attribute with the given index (starts from 0). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAttributePrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributePrefix(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the prefix of the specified attribute Returns null if the element has no prefix. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAttributeType](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeType(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the type of the specified attribute If parser is non-validating it MUST return CDATA. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAttributeValue](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeValue(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the given attributes value. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAttributeValue](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeValue(kotlin.String,%20kotlin.String))`(`namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the attributes value identified by namespace URI and namespace localName. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getColumnNumber())`()` Returns the current column number, starting from 1. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDepth](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getDepth())`()` Returns the current depth of the element. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEventType](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getEventType())`()` Returns the type of the current event (START_TAG, END_TAG, TEXT, etc.) |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the current value of the given feature. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInputEncoding](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getInputEncoding())`()` Returns the input encoding if known, null otherwise. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getLineNumber())`()` Returns the current line number, starting from 1. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getName())`()` For START_TAG or END_TAG events, the (local) name of the current element is returned when namespaces are enabled. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespace](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespace())`()` Returns the namespace URI of the current element. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespace](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespace(kotlin.String))`(`prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the URI corresponding to the given prefix, depending on current state of the parser. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNamespaceCount](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespaceCount(kotlin.Int))`(`depth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the numbers of elements in the namespace stack for the given depth. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespacePrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespacePrefix(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the namespace prefix for the given position in the namespace stack. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNamespaceUri](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespaceUri(kotlin.Int))`(`pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the namespace URI for the given position in the namespace stack If the position is out of range, an exception is thrown. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPositionDescription](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getPositionDescription())`()` Returns a short text describing the current parser state, including the position, a description of the current event and the data source if known. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getPrefix())`()` Returns the prefix of the current element. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getProperty](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getProperty(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Look up the value of a property. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText())`()` Returns the text content of the current event as String. |
| --- | --- |
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getTextCharacters](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getTextCharacters(kotlin.IntArray))`(`holderForStartAndLength:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Returns the buffer that contains the text of the current event, as well as the start offset and length relevant for the current event. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAttributeDefault](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#isAttributeDefault(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns if the specified attribute was not in input was declared in XML. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmptyElementTag](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#isEmptyElementTag())`()` Returns true if the current event is START_TAG and the tag is degenerated (e.g. \<foobar/\>). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWhitespace](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#isWhitespace())`()` Checks whether the current TEXT event contains only whitespace characters. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())`()` Get next parsing event - element content will be coalesced and only one TEXT event must be returned for whole element content (comments and processing instructions will be ignored and entity references must be expanded or exception must be thrown if entity reference can not be expanded). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextTag](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextTag())`()` Call next() and return event if it is START_TAG or END_TAG otherwise throw an exception. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nextText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextText())`()` If current event is START_TAG then if next element is TEXT then element content is returned or if next event is END_TAG then empty string is returned, otherwise exception is thrown. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())`()` This method works similarly to next() but will expose additional event types (COMMENT, CDSECT, DOCDECL, ENTITY_REF, PROCESSING_INSTRUCTION, or IGNORABLE_WHITESPACE) if they are available in input. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [require](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#require(kotlin.Int,%20kotlin.String,%20kotlin.String))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `namespace:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Test if the current event is of the given type and if the namespace and name do match. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `state:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Use this call to change the general behaviour of the parser, such as namespace processing or doctype declaration handling. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setInput(java.io.InputStream,%20kotlin.String))`(`inputStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `inputEncoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the input stream the parser is going to process. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInput](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setInput(java.io.Reader))`(`in:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` Set the input source for parser to the given reader and resets the parser. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setProperty(kotlin.String,%20kotlin.Any))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the value of a property. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [TYPES](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#TYPES:kotlin.Array) This array can be used to convert the event type integer constants such as START_TAG or TEXT to to a string. |

## Constants

### CDSECT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CDSECT: Int
```

A CDATA sections was just read; this token is available only from calls to [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()). A call to next() will accumulate various text events into a single event of type TEXT. The text contained in the CDATA section is available by calling getText(). 

 Value: 5

**See Also**

- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText()) 

### COMMENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMMENT: Int
```

An XML comment was just read. This event type is this token is available via [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())only; calls to next() will skip comments automatically. The content of the comment can be accessed using the getText() method. 

 Value: 9

**See Also**

- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText()) 

### DOCDECL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOCDECL: Int
```

An XML document type declaration was just read. This token is available from [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())only. The unparsed text inside the doctype is available via the getText() method. 

 Value: 10

**See Also**

- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText()) 

### END_DOCUMENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val END_DOCUMENT: Int
```

Logical end of the xml document. Returned from getEventType, next() and nextToken() when the end of the input document has been reached.

**NOTE:** subsequent calls to [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())or [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())may result in exception being thrown. 

 Value: 1

**See Also**

- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()) 

### END_TAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val END_TAG: Int
```

Returned from getEventType(), [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next()), or [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())when an end tag was read. The name of start tag is available from getName(), its namespace and prefix are available from getNamespace() and getPrefix(). 

 Value: 3

**See Also**

- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getName())
- [#getPrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getPrefix())
- [#FEATURE_PROCESS_NAMESPACES](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_PROCESS_NAMESPACES:kotlin.String) 

### ENTITY_REF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTITY_REF: Int
```

An entity reference was just read; this token is available from [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())only. The entity name is available by calling getName(). If available, the replacement text can be obtained by calling getText(); otherwise, the user is responsible for resolving the entity reference. This event type is never returned from next(); next() will accumulate the replacement text and other text events to a single TEXT event. 

 Value: 6

**See Also**

- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText()) 

### FEATURE_PROCESS_DOCDECL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_PROCESS_DOCDECL: String
```

This feature determines whether the document declaration is processed. If set to false, the DOCDECL event type is reported by nextToken() and ignored by next(). If this feature is activated, then the document declaration must be processed by the parser.

**Please note:**If the document type declaration was ignored, entity references may cause exceptions later in the parsing process. The default value of this feature is false. It cannot be changed during parsing. 

 Value: "http://xmlpull.org/v1/doc/features.html#process-docdecl"

**See Also**

- [#getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getFeature(kotlin.String))
- [#setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setFeature(kotlin.String,%20kotlin.Boolean)) 

### FEATURE_PROCESS_NAMESPACES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_PROCESS_NAMESPACES: String
```

This feature determines whether the parser processes namespaces. As for all features, the default value is false.

**NOTE:**The value can not be changed during parsing an must be set before parsing. 

 Value: "http://xmlpull.org/v1/doc/features.html#process-namespaces"

**See Also**

- [#getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getFeature(kotlin.String))
- [#setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setFeature(kotlin.String,%20kotlin.Boolean)) 

### FEATURE_REPORT_NAMESPACE_ATTRIBUTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_REPORT_NAMESPACE_ATTRIBUTES: String
```

This feature determines whether namespace attributes are exposed via the attribute access methods. Like all features, the default value is false. This feature cannot be changed during parsing. 

 Value: "http://xmlpull.org/v1/doc/features.html#report-namespace-prefixes"

**See Also**

- [#getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getFeature(kotlin.String))
- [#setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setFeature(kotlin.String,%20kotlin.Boolean)) 

### FEATURE_VALIDATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FEATURE_VALIDATION: String
```

If this feature is activated, all validation errors as defined in the XML 1.0 specification are reported. This implies that FEATURE_PROCESS_DOCDECL is true and both, the internal and external document type declaration will be processed.

**Please Note:**This feature can not be changed during parsing. The default value is false. 

 Value: "http://xmlpull.org/v1/doc/features.html#validation"

**See Also**

- [#getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getFeature(kotlin.String))
- [#setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#setFeature(kotlin.String,%20kotlin.Boolean)) 

### IGNORABLE_WHITESPACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IGNORABLE_WHITESPACE: Int
```

Ignorable whitespace was just read. This token is available only from [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())). For non-validating parsers, this event is only reported by nextToken() when outside the root element. Validating parsers may be able to detect ignorable whitespace at other locations. The ignorable whitespace string is available by calling getText()

**NOTE:**this is different from calling the isWhitespace() method, since text content may be whitespace but not ignorable. Ignorable whitespace is skipped by next() automatically; this event type is never returned from next(). 

 Value: 7

**See Also**

- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText()) 

### NO_NAMESPACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_NAMESPACE: String
```

This constant represents the default namespace (empty string "") 

 Value: ""

### PROCESSING_INSTRUCTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROCESSING_INSTRUCTION: Int
```

An XML processing instruction declaration was just read. This event type is available only via [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()). getText() will return text that is inside the processing instruction. Calls to next() will skip processing instructions automatically. 

 Value: 8

**See Also**

- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText()) 

### START_DOCUMENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val START_DOCUMENT: Int
```

Signalize that parser is at the very beginning of the document and nothing was read yet. This event type can only be observed by calling getEvent() before the first call to next(), nextToken, or nextTag()). 

 Value: 0

**See Also**

- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()) 

### START_TAG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val START_TAG: Int
```

Returned from getEventType(), [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next()), [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())when a start tag was read. The name of start tag is available from getName(), its namespace and prefix are available from getNamespace() and getPrefix() if [namespaces are enabled](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_PROCESS_NAMESPACES). See getAttribute\* methods to retrieve element attributes. See getNamespace\* methods to retrieve newly declared namespaces. 

 Value: 2

**See Also**

- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getName())
- [#getPrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getPrefix())
- [#getAttributeCount](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeCount())
- [#getDepth](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getDepth())
- [#getNamespaceCount](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespaceCount(kotlin.Int))
- [#FEATURE_PROCESS_NAMESPACES](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_PROCESS_NAMESPACES:kotlin.String) 

### TEXT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TEXT: Int
```

Character data was read and will is available by calling getText().

**Please note:** [next()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())will accumulate multiple events into one TEXT event, skipping IGNORABLE_WHITESPACE, PROCESSING_INSTRUCTION and COMMENT events, In contrast, [nextToken()](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())will stop reading text when any other event is observed. Also, when the state was reached by calling next(), the text value will be normalized, whereas getText() will return unnormalized content in the case of nextToken(). This allows an exact roundtrip without changing line ends when examining low level events, whereas for high level applications the text is normalized appropriately. 

 Value: 4

**See Also**

- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken())
- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText())

## Public methods

### defineEntityReplacementText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun defineEntityReplacementText(
    entityName: String!, 
    replacementText: String!
): Unit
```

Set new value for entity replacement text as defined in [XML 1.0 Section 4.5 Construction of Internal Entity Replacement Text](http://www.w3.org/TR/REC-xml#intern-replacement). If FEATURE_PROCESS_DOCDECL or FEATURE_VALIDATION are set, calling this function will result in an exception -- when processing of DOCDECL is enabled, there is no need to the entity replacement text manually.

The motivation for this function is to allow very small implementations of XMLPULL that will work in J2ME environments. Though these implementations may not be able to process the document type declaration, they still can work with known DTDs by using this function.

**Please notes:**The given value is used literally as replacement text and it corresponds to declaring entity in DTD that has all special characters escaped: left angle bracket is replaced with \&lt;, ampersand with \&amp; and so on.

**Note:**The given value is the literal replacement text and must not contain any other entity reference (if it contains any entity reference there will be no further replacement).

**Note:**The list of pre-defined entity names will always contain standard XML entities such as amp (\&amp;), lt (\&lt;), gt (\&gt;), quot (\&quot;), and apos ('). Those cannot be redefined by this method! 
**See Also**

- [#FEATURE_PROCESS_DOCDECL](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_PROCESS_DOCDECL:kotlin.String)
- [#FEATURE_VALIDATION](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#FEATURE_VALIDATION:kotlin.String) 

### getAttributeCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeCount(): Int
```

Returns the number of attributes of the current start tag, or -1 if the current event type is not START_TAG 
**See Also**

- [#getAttributeNamespace](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeNamespace(kotlin.Int))
- [#getAttributeName](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributeName(kotlin.Int))
- [#getAttributePrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getAttributePrefix(kotlin.Int)) 

### getAttributeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeName(index: Int): String!
```

Returns the local name of the specified attribute if namespaces are enabled or just attribute name if namespaces are disabled. Throws an IndexOutOfBoundsException if the index is out of range or current event type is not START_TAG.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zero-based index of attribute |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | attribute name (null is never returned) |

### getAttributeNamespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeNamespace(index: Int): String!
```

Returns the namespace URI of the attribute with the given index (starts from 0). Returns an empty string ("") if namespaces are not enabled or the attribute has no namespace. Throws an IndexOutOfBoundsException if the index is out of range or the current event type is not START_TAG.

**NOTE:** if FEATURE_REPORT_NAMESPACE_ATTRIBUTES is set then namespace attributes (xmlns:ns='...') must be reported with namespace<http://www.w3.org/2000/xmlns/>(visit this URL for description!). The default namespace attribute (xmlns="...") will be reported with empty namespace.

**NOTE:** The xml prefix is bound as defined in [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/#ns-using) specification to "http://www.w3.org/XML/1998/namespace".

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zero-based index of attribute |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | attribute namespace, empty string ("") is returned if namespaces processing is not enabled or namespaces processing is enabled but attribute has no namespace (it has no prefix). |

### getAttributePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributePrefix(index: Int): String!
```

Returns the prefix of the specified attribute Returns null if the element has no prefix. If namespaces are disabled it will always return null. Throws an IndexOutOfBoundsException if the index is out of range or current event type is not START_TAG.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zero-based index of attribute |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | attribute prefix or null if namespaces processing is not enabled. |

### getAttributeType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeType(index: Int): String!
```

Returns the type of the specified attribute If parser is non-validating it MUST return CDATA.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zero-based index of attribute |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | attribute type (null is never returned) |

### getAttributeValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeValue(index: Int): String!
```

Returns the given attributes value. Throws an IndexOutOfBoundsException if the index is out of range or current event type is not START_TAG.

**NOTE:** attribute value must be normalized (including entity replacement text if PROCESS_DOCDECL is false) as described in [XML 1.0 section 3.3.3 Attribute-Value Normalization](http://www.w3.org/TR/REC-xml#AVNormalize)

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zero-based index of attribute |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | value of attribute (null is never returned) |

**See Also**

- [#defineEntityReplacementText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#defineEntityReplacementText(kotlin.String,%20kotlin.String)) 

### getAttributeValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAttributeValue(
    namespace: String!, 
    name: String!
): String!
```

Returns the attributes value identified by namespace URI and namespace localName. If namespaces are disabled namespace must be null. If current event type is not START_TAG then IndexOutOfBoundsException will be thrown.

**NOTE:** attribute value must be normalized (including entity replacement text if PROCESS_DOCDECL is false) as described in [XML 1.0 section 3.3.3 Attribute-Value Normalization](http://www.w3.org/TR/REC-xml#AVNormalize)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `namespace` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Namespace of the attribute if namespaces are enabled otherwise must be null |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:If namespaces enabled local name of attribute otherwise just attribute name |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | value of attribute or null if attribute with given name does not exist |

**See Also**

- [#defineEntityReplacementText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#defineEntityReplacementText(kotlin.String,%20kotlin.String)) 

### getColumnNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getColumnNumber(): Int
```

Returns the current column number, starting from 1. When the parser does not know the current column number or can not determine it, -1 is returned (e.g. for WBXML).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current column number or -1 if unknown. |

### getDepth

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDepth(): Int
```

Returns the current depth of the element. Outside the root element, the depth is 0. The depth is incremented by 1 when a start tag is reached. The depth is decremented AFTER the end tag event was observed. 

```kotlin
<!-- outside -->     0
  <root>                  1
    sometext                 1
      <foobar>         2
      </foobar>        2
  </root>              1
  <!-- outside -->     0
  
```

<br />

### getEventType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEventType(): Int
```

Returns the type of the current event (START_TAG, END_TAG, TEXT, etc.) 
**See Also**

- <https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next()>
- <https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()> 

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFeature(name: String!): Boolean
```

Returns the current value of the given feature.

**Please note:** unknown features are**always**returned as false.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of feature to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The value of the feature. |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if string the feature name is null |

### getInputEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInputEncoding(): String!
```

Returns the input encoding if known, null otherwise. If setInput(InputStream, inputEncoding) was called with an inputEncoding value other than null, this value must be returned from this method. Otherwise, if inputEncoding is null and the parser supports the encoding detection feature (http://xmlpull.org/v1/doc/features.html#detect-encoding), it must return the detected encoding. If setInput(Reader) was called, null is returned. After first call to next if XML declaration was present this method will return encoding declared. 

### getLineNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLineNumber(): Int
```

Returns the current line number, starting from 1. When the parser does not know the current line number or can not determine it, -1 is returned (e.g. for WBXML).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current line number or -1 if unknown. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String!
```

For START_TAG or END_TAG events, the (local) name of the current element is returned when namespaces are enabled. When namespace processing is disabled, the raw name is returned. For ENTITY_REF events, the entity name is returned. If the current event is not START_TAG, END_TAG, or ENTITY_REF, null is returned.

**Please note:**To reconstruct the raw element name when namespaces are enabled and the prefix is not null, you will need to add the prefix and a colon to localName.. 

### getNamespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespace(): String!
```

Returns the namespace URI of the current element. The default namespace is represented as empty string. If namespaces are not enabled, an empty String ("") is always returned. The current event must be START_TAG or END_TAG; otherwise, null is returned. 

### getNamespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespace(prefix: String!): String!
```

Returns the URI corresponding to the given prefix, depending on current state of the parser.

If the prefix was not declared in the current scope, null is returned. The default namespace is included in the namespace table and is available via getNamespace (null).

This method is a convenience method for 

```kotlin
for (int i = getNamespaceCount(getDepth ())-1; i >= 0; i--) {
    if (getNamespacePrefix(i).equals( prefix )) {
      return getNamespaceUri(i);
    }
   }
   return null;
  
```

**Please note:** parser implementations may provide more efficient lookup, e.g. using a Hashtable. The 'xml' prefix is bound to "http://www.w3.org/XML/1998/namespace", as defined in the [Namespaces in XML](http://www.w3.org/TR/REC-xml-names/#ns-using) specification. Analogous, the 'xmlns' prefix is resolved to<http://www.w3.org/2000/xmlns/> 
**See Also**

- [#getNamespaceCount](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespaceCount(kotlin.Int))
- [#getNamespacePrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespacePrefix(kotlin.Int))
- [#getNamespaceUri](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespaceUri(kotlin.Int)) 

### getNamespaceCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespaceCount(depth: Int): Int
```

Returns the numbers of elements in the namespace stack for the given depth. If namespaces are not enabled, 0 is returned.

**NOTE:**when parser is on END_TAG then it is allowed to call this function with getDepth()+1 argument to retrieve position of namespace prefixes and URIs that were declared on corresponding START_TAG.

**NOTE:**to retrieve list of namespaces declared in current element: 

```kotlin
XmlPullParser pp = ...
        int nsStart = pp.getNamespaceCount(pp.getDepth()-1);
        int nsEnd = pp.getNamespaceCount(pp.getDepth());
        for (int i = nsStart; i < nsEnd; i++) {
           String prefix = pp.getNamespacePrefix(i);
           String ns = pp.getNamespaceUri(i);
            // ...
       }
  
```  
**See Also**

- [#getNamespacePrefix](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespacePrefix(kotlin.Int))
- [#getNamespaceUri](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespaceUri(kotlin.Int))
- <https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespace()>
- [#getNamespace(String)](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getNamespace(kotlin.String)) 

### getNamespacePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespacePrefix(pos: Int): String!
```

Returns the namespace prefix for the given position in the namespace stack. Default namespace declaration (xmlns='...') will have null as prefix. If the given index is out of range, an exception is thrown.

**Please note:**when the parser is on an END_TAG, namespace prefixes that were declared in the corresponding START_TAG are still accessible although they are no longer in scope. 

### getNamespaceUri

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNamespaceUri(pos: Int): String!
```

Returns the namespace URI for the given position in the namespace stack If the position is out of range, an exception is thrown.

**NOTE:**when parser is on END_TAG then namespace prefixes that were declared in corresponding START_TAG are still accessible even though they are not in scope 

### getPositionDescription

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPositionDescription(): String!
```

Returns a short text describing the current parser state, including the position, a description of the current event and the data source if known. This method is especially useful to provide meaningful error messages and for debugging purposes. 

### getPrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrefix(): String!
```

Returns the prefix of the current element. If the element is in the default namespace (has no prefix), null is returned. If namespaces are not enabled, or the current event is not START_TAG or END_TAG, null is returned. 

### getProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getProperty(name: String!): Any!
```

Look up the value of a property. The property name is any fully-qualified URI.

**NOTE:** unknown properties are**always**returned as null.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of property to be retrieved. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The value of named property. |

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getText(): String!
```

Returns the text content of the current event as String. The value returned depends on current event type, for example for TEXT event it is element content (this is typical case when next() is used). See description of nextToken() for detailed description of possible returned values for different types of events.

**NOTE:**in case of ENTITY_REF, this method returns the entity replacement text (or null if not available). This is the only case where getText() and getTextCharacters() return different values. 
**See Also**

- [#getEventType](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getEventType())
- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()) 

### getTextCharacters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTextCharacters(holderForStartAndLength: IntArray!): CharArray!
```

Returns the buffer that contains the text of the current event, as well as the start offset and length relevant for the current event. See getText(), next() and nextToken() for description of possible returned values.

**Please note:**this buffer must not be modified and its content MAY change after a call to next() or nextToken(). This method will always return the same value as getText(), except for ENTITY_REF. In the case of ENTITY ref, getText() returns the replacement text and this method returns the actual input buffer containing the entity name. If getText() returns null, this method returns null as well and the values returned in the holder array MUST be -1 (both start and length).

| Parameters ||
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `holderForStartAndLength` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Must hold an 2-element int array into which the start offset and length values will be written. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | char buffer that contains the text of the current event (null if the current event has no text associated). |

**See Also**

- [#getText](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#getText())
- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#nextToken](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#nextToken()) 

### isAttributeDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isAttributeDefault(index: Int): Boolean
```

Returns if the specified attribute was not in input was declared in XML. If parser is non-validating it MUST always return false. This information is part of XML infoset:

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):zero-based index of attribute |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | false if attribute was in input |

### isEmptyElementTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmptyElementTag(): Boolean
```

Returns true if the current event is START_TAG and the tag is degenerated (e.g. \<foobar/\>).

**NOTE:**if the parser is not on START_TAG, an exception will be thrown. 

### isWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isWhitespace(): Boolean
```

Checks whether the current TEXT event contains only whitespace characters. For IGNORABLE_WHITESPACE, this is always true. For TEXT and CDSECT, false is returned when the current event text contains at least one non-white space character. For any other event type an exception is thrown.

**Please note:**non-validating parsers are not able to distinguish whitespace and ignorable whitespace, except from whitespace outside the root element. Ignorable whitespace is reported as separate event, which is exposed via nextToken only. 

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): Int
```

Get next parsing event - element content will be coalesced and only one TEXT event must be returned for whole element content (comments and processing instructions will be ignored and entity references must be expanded or exception must be thrown if entity reference can not be expanded). If element content is empty (content is "") then no TEXT event will be reported.

**NOTE:**empty element (such as \<tag/\>) will be reported with two separate events: START_TAG, END_TAG - it must be so to preserve parsing equivalency of empty element to \<tag\>\</tag\>. (see isEmptyElementTag ()) 
**See Also**

- [#isEmptyElementTag](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#isEmptyElementTag())
- [#START_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#START_TAG:kotlin.Int)
- [#TEXT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#TEXT:kotlin.Int)
- [#END_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_TAG:kotlin.Int)
- [#END_DOCUMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_DOCUMENT:kotlin.Int) 

### nextTag

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextTag(): Int
```

Call next() and return event if it is START_TAG or END_TAG otherwise throw an exception. It will skip whitespace TEXT before actual tag if any.

essentially it does this 

```kotlin
int eventType = next();
    if(eventType == TEXT &&  isWhitespace()) {   // skip whitespace
       eventType = next();
    }
    if (eventType != START_TAG &&  eventType != END_TAG) {
       throw new XmlPullParserException("expected start or end tag", this, null);
    }
    return eventType;
  
```  

### nextText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextText(): String!
```

If current event is START_TAG then if next element is TEXT then element content is returned or if next event is END_TAG then empty string is returned, otherwise exception is thrown. After calling this function successfully parser will be positioned on END_TAG.

The motivation for this function is to allow to parse consistently both empty elements and elements that has non empty content, for example for input:

1. \<tag\>foo\</tag\>
2. \<tag\>\</tag\> (which is equivalent to \<tag/\> both input can be parsed with the same code: 

   ```kotlin
   p.nextTag()
       p.requireEvent(p.START_TAG, "", "tag");
       String content = p.nextText();
       p.requireEvent(p.END_TAG, "", "tag");
     
   ```
 This function together with nextTag make it very easy to parse XML that has no mixed content.

 Essentially it does this 

   ```kotlin
   if(getEventType() != START_TAG) {
         throw new XmlPullParserException(
           "parser must be on START_TAG to read next text", this, null);
      }
      int eventType = next();
      if(eventType == TEXT) {
         String result = getText();
         eventType = next();
         if(eventType != END_TAG) {
           throw new XmlPullParserException(
              "event TEXT it must be immediately followed by END_TAG", this, null);
          }
          return result;
      } else if(eventType == END_TAG) {
         return "";
      } else {
         throw new XmlPullParserException(
           "parser must be on START_TAG or TEXT to read text", this, null);
      }
     
   ```

 **Warning:** Prior to API level 14, the pull parser returned by`android.util.Xml`did not always advance to the END_TAG event when this method was called. Work around by using manually advancing after calls to nextText(): 

   ```kotlin
   String text = xpp.nextText();
      if (xpp.getEventType() != XmlPullParser.END_TAG) {
          xpp.next();
      }
     
```  

### nextToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextToken(): Int
```

This method works similarly to next() but will expose additional event types (COMMENT, CDSECT, DOCDECL, ENTITY_REF, PROCESSING_INSTRUCTION, or IGNORABLE_WHITESPACE) if they are available in input.

If special feature [FEATURE_XML_ROUNDTRIP](http://xmlpull.org/v1/doc/features.html#xml-roundtrip)(identified by URI: http://xmlpull.org/v1/doc/features.html#xml-roundtrip) is enabled it is possible to do XML document round trip ie. reproduce exectly on output the XML input using getText(): returned content is always unnormalized (exactly as in input). Otherwise returned content is end-of-line normalized as described [XML 1.0 End-of-Line Handling](http://www.w3.org/TR/REC-xml#sec-line-ends) and. Also when this feature is enabled exact content of START_TAG, END_TAG, DOCDECL and PROCESSING_INSTRUCTION is available.

Here is the list of tokens that can be returned from nextToken() and what getText() and getTextCharacters() returns:

START_DOCUMENT
: null

END_DOCUMENT
: null

START_TAG
: null unless FEATURE_XML_ROUNDTRIP enabled and then returns XML tag, ex: \<tag attr='val'\>

END_TAG
: null unless FEATURE_XML_ROUNDTRIP id enabled and then returns XML tag, ex: \</tag\>

TEXT
: return element content. 
 Note: that element content may be delivered in multiple consecutive TEXT events.

IGNORABLE_WHITESPACE
: return characters that are determined to be ignorable white space. If the FEATURE_XML_ROUNDTRIP is enabled all whitespace content outside root element will always reported as IGNORABLE_WHITESPACE otherwise reporting is optional. 
 Note: that element content may be delivered in multiple consecutive IGNORABLE_WHITESPACE events.

CDSECT
: return text*inside*CDATA (ex. 'fo\<o' from \<!CDATA\[fo\<o\]\]\>)

PROCESSING_INSTRUCTION
: if FEATURE_XML_ROUNDTRIP is true return exact PI content ex: 'pi foo' from \<?pi foo?\> otherwise it may be exact PI content or concatenation of PI target, space and data so for example for \<?target data?\> string "target data" may be returned if FEATURE_XML_ROUNDTRIP is false.

COMMENT
: return comment content ex. 'foo bar' from \<!--foo bar--\>

ENTITY_REF
: getText() MUST return entity replacement text if PROCESS_DOCDECL is false otherwise getText() MAY return null, additionally getTextCharacters() MUST return entity name (for example 'entity_name' for \&entity_name;). 
 **NOTE:** this is the only place where value returned from getText() and getTextCharacters()**are different** 
 **NOTE:** it is user responsibility to resolve entity reference if PROCESS_DOCDECL is false and there is no entity replacement text set in defineEntityReplacementText() method (getText() will be null) 
 **NOTE:** character entities (ex. \&#32;) and standard entities such as \&amp; \&lt; \&gt; \&quot; ' are reported as well and are**not**reported as TEXT tokens but as ENTITY_REF tokens! This requirement is added to allow to do roundtrip of XML documents!

DOCDECL
: if FEATURE_XML_ROUNDTRIP is true or PROCESS_DOCDECL is false then return what is inside of DOCDECL for example it returns: 

    ```kotlin
    " titlepage SYSTEM "http://www.foo.bar/dtds/typo.dtd"
      [<!ENTITY % active.links "INCLUDE">]"
    ```

 for input document that contained: 

    ```kotlin
    <!DOCTYPE titlepage SYSTEM "http://www.foo.bar/dtds/typo.dtd"
      [<!ENTITY % active.links "INCLUDE">]>
    ```
 otherwise if FEATURE_XML_ROUNDTRIP is false and PROCESS_DOCDECL is true then what is returned is undefined (it may be even null)

**NOTE:**there is no guarantee that there will only one TEXT or IGNORABLE_WHITESPACE event from nextToken() as parser may chose to deliver element content in multiple tokens (dividing element content into chunks)

**NOTE:**whether returned text of token is end-of-line normalized is depending on FEATURE_XML_ROUNDTRIP.

**NOTE:**XMLDecl (\<?xml ...?\>) is not reported but its content is available through optional properties (see class description above). 
**See Also**

- [#next](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#next())
- [#START_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#START_TAG:kotlin.Int)
- [#TEXT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#TEXT:kotlin.Int)
- [#END_TAG](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_TAG:kotlin.Int)
- [#END_DOCUMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#END_DOCUMENT:kotlin.Int)
- [#COMMENT](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#COMMENT:kotlin.Int)
- [#DOCDECL](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#DOCDECL:kotlin.Int)
- [#PROCESSING_INSTRUCTION](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#PROCESSING_INSTRUCTION:kotlin.Int)
- [#ENTITY_REF](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#ENTITY_REF:kotlin.Int)
- [#IGNORABLE_WHITESPACE](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser#IGNORABLE_WHITESPACE:kotlin.Int) 

### require

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun require(
    type: Int, 
    namespace: String!, 
    name: String!
): Unit
```

Test if the current event is of the given type and if the namespace and name do match. null will match any namespace and any name. If the test is not passed, an exception is thrown. The exception text indicates the parser position, the expected event and the current event that is not meeting the requirement.

Essentially it does this 

```kotlin
if (type != getEventType()
   || (namespace != null &&  !namespace.equals( getNamespace () ) )
   || (name != null &&  !name.equals( getName() ) ) )
      throw new XmlPullParserException( "expected "+ TYPES[ type ]+getPositionDescription());
  
```  

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setFeature(
    name: String!, 
    state: Boolean
): Unit
```

Use this call to change the general behaviour of the parser, such as namespace processing or doctype declaration handling. This method must be called before the first call to next or nextToken. Otherwise, an exception is thrown.

Example: call setFeature(FEATURE_PROCESS_NAMESPACES, true) in order to switch on namespace processing. The initial settings correspond to the properties requested from the XML Pull Parser factory. If none were requested, all features are deactivated by default.

| Exceptions ||
|-----------------------------------------|---------------------------------------------------|
| `org.xmlpull.v1.XmlPullParserException` | If the feature is not supported or can not be set |
| `java.lang.IllegalArgumentException` | If string with the feature name is null |

### setInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInput(
    inputStream: InputStream!, 
    inputEncoding: String!
): Unit
```

Sets the input stream the parser is going to process. This call resets the parser state and sets the event type to the initial value START_DOCUMENT.

**NOTE:** If an input encoding string is passed, it MUST be used. Otherwise, if inputEncoding is null, the parser SHOULD try to determine input encoding following XML 1.0 specification (see below). If encoding detection is supported then following feature<http://xmlpull.org/v1/doc/features.html#detect-encoding>MUST be true and otherwise it must be false.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:contains a raw byte input stream of possibly unknown encoding (when inputEncoding is null). |
| `inputEncoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:if not null it MUST be used as encoding for inputStream |

### setInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setInput(in: Reader!): Unit
```

Set the input source for parser to the given reader and resets the parser. The event type is set to the initial value START_DOCUMENT. Setting the reader to null will just stop parsing and reset parser state, allowing the parser to free internal resources such as parsing buffers. 

### setProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setProperty(
    name: String!, 
    value: Any!
): Unit
```

Set the value of a property. The property name is any fully-qualified URI.

| Exceptions ||
|-----------------------------------------|----------------------------------------------------|
| `org.xmlpull.v1.XmlPullParserException` | If the property is not supported or can not be set |
| `java.lang.IllegalArgumentException` | If string with the property name is null |

## Properties

### TYPES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPES: Array<String!>!
```

This array can be used to convert the event type integer constants such as START_TAG or TEXT to to a string. For example, the value of TYPES\[START_TAG\] is the string "START_TAG". This array is intended for diagnostic output only. Relying on the contents of the array may be dangerous since malicious applications may alter the array, although it is final, due to limitations of the Java language.

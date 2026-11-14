# SQLXML

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SQLXML

```
interface SQLXML
```

| [java.sql.SQLXML](https://developer.android.com/reference/kotlin/java/sql/SQLXML#) |

The mapping in the JavaTM programming language for the SQL XML type. XML is a built-in type that stores an XML value as a column value in a row of a database table. By default drivers implement an SQLXML object as a logical pointer to the XML data rather than the data itself. An SQLXML object is valid for the duration of the transaction in which it was created.

The SQLXML interface provides methods for accessing the XML value as a String, a Reader or Writer, or as a Stream. The XML value may also be accessed through a Source or set as a Result, which are used with XML Parser APIs such as DOM, SAX, and StAX, as well as with XSLT transforms and XPath evaluations.

Methods in the interfaces ResultSet, CallableStatement, and PreparedStatement, such as getSQLXML allow a programmer to access an XML value. In addition, this interface has methods for updating an XML value.

The XML value of the SQLXML instance may be obtained as a BinaryStream using 

```kotlin
SQLXML sqlxml = resultSet.getSQLXML(column);
    InputStream binaryStream = sqlxml.getBinaryStream();
  
```
For example, to parse an XML value with a DOM parser: 

```kotlin
DocumentBuilder parser = DocumentBuilderFactory.newInstance().newDocumentBuilder();
    Document result = parser.parse(binaryStream);
  
```
or to parse an XML value with a SAX parser to your handler: 

```kotlin
SAXParser parser = SAXParserFactory.newInstance().newSAXParser();
    parser.parse(binaryStream, myHandler);
  
```
or to parse an XML value with a StAX parser: 

```kotlin
XMLInputFactory factory = XMLInputFactory.newInstance();
    XMLStreamReader streamReader = factory.createXMLStreamReader(binaryStream);
  
```

Because databases may use an optimized representation for the XML, accessing the value through getSource() and setResult() can lead to improved processing performance without serializing to a stream representation and parsing the XML.

For example, to obtain a DOM Document Node: 

```kotlin
DOMSource domSource = sqlxml.getSource(DOMSource.class);
    Document document = (Document) domSource.getNode();
  
```
or to set the value to a DOM Document Node to myNode: 

```kotlin
DOMResult domResult = sqlxml.setResult(DOMResult.class);
    domResult.setNode(myNode);
  
```
or, to send SAX events to your handler: 

```kotlin
SAXSource saxSource = sqlxml.getSource(SAXSource.class);
    XMLReader xmlReader = saxSource.getXMLReader();
    xmlReader.setContentHandler(myHandler);
    xmlReader.parse(saxSource.getInputSource());
  
```
or, to set the result value from SAX events: 

```kotlin
SAXResult saxResult = sqlxml.setResult(SAXResult.class);
    ContentHandler contentHandler = saxResult.getXMLReader().getContentHandler();
    contentHandler.startDocument();
    // set the XML elements and attributes into the result
    contentHandler.endDocument();
  
```
or, to obtain StAX events: 

```kotlin
StAXSource staxSource = sqlxml.getSource(StAXSource.class);
    XMLStreamReader streamReader = staxSource.getXMLStreamReader();
  
```
or, to set the result value from StAX events: 

```kotlin
StAXResult staxResult = sqlxml.setResult(StAXResult.class);
    XMLStreamWriter streamWriter = staxResult.getXMLStreamWriter();
  
```
or, to perform XSLT transformations on the XML value using the XSLT in xsltFile output to file resultFile: 

```kotlin
File xsltFile = new File("a.xslt");
    File myFile = new File("result.xml");
    Transformer xslt = TransformerFactory.newInstance().newTransformer(new StreamSource(xsltFile));
    Source source = sqlxml.getSource(null);
    Result result = new StreamResult(myFile);
    xslt.transform(source, result);
  
```
or, to evaluate an XPath expression on the XML value: 

```kotlin
XPath xpath = XPathFactory.newInstance().newXPath();
    DOMSource domSource = sqlxml.getSource(DOMSource.class);
    Document document = (Document) domSource.getNode();
    String expression = "/foo/@bar";
    String barValue = xpath.evaluate(expression, document);
  
```
To set the XML value to be the result of an XSLT transform: 

```kotlin
File sourceFile = new File("source.xml");
    Transformer xslt = TransformerFactory.newInstance().newTransformer(new StreamSource(xsltFile));
    Source streamSource = new StreamSource(sourceFile);
    Result result = sqlxml.setResult(null);
    xslt.transform(streamSource, result);
  
```
Any Source can be transformed to a Result using the identity transform specified by calling newTransformer(): 

```kotlin
Transformer identity = TransformerFactory.newInstance().newTransformer();
    Source source = sqlxml.getSource(null);
    File myFile = new File("result.xml");
    Result result = new StreamResult(myFile);
    identity.transform(source, result);
  
```
To write the contents of a Source to standard output: 

```kotlin
Transformer identity = TransformerFactory.newInstance().newTransformer();
    Source source = sqlxml.getSource(null);
    Result result = new StreamResult(System.out);
    identity.transform(source, result);
  
```
To create a DOMSource from a DOMResult: 

```kotlin
DOMSource domSource = new DOMSource(domResult.getNode());
  
```

Incomplete or invalid XML values may cause an SQLException when set or the exception may occur when execute() occurs. All streams must be closed before execute() occurs or an SQLException will be thrown.

Reading and writing XML values to or from an SQLXML object can happen at most once. The conceptual states of readable and not readable determine if one of the reading APIs will return a value or throw an exception. The conceptual states of writable and not writable determine if one of the writing APIs will set a value or throw an exception.

The state moves from readable to not readable once free() or any of the reading APIs are called: getBinaryStream(), getCharacterStream(), getSource(), and getString(). Implementations may also change the state to not writable when this occurs.

The state moves from writable to not writeable once free() or any of the writing APIs are called: setBinaryStream(), setCharacterStream(), setResult(), and setString(). Implementations may also change the state to not readable when this occurs.

<br />

All methods on the`SQLXML`interface must be fully implemented if the JDBC driver supports the data type.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [free](https://developer.android.com/reference/kotlin/java/sql/SQLXML#free())`()` This method closes this object and releases the resources that it held. |
| abstract [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getBinaryStream](https://developer.android.com/reference/kotlin/java/sql/SQLXML#getBinaryStream())`()` Retrieves the XML value designated by this SQLXML instance as a stream. |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/java/sql/SQLXML#getCharacterStream())`()` Retrieves the XML value designated by this SQLXML instance as a java. |
| --- | --- |
| abstractT | [getSource](https://developer.android.com/reference/kotlin/java/sql/SQLXML#getSource(java.lang.Class))`(`sourceClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Returns a Source for reading the XML value designated by this SQLXML instance. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getString](https://developer.android.com/reference/kotlin/java/sql/SQLXML#getString())`()` Returns a string representation of the XML value designated by this SQLXML instance. |
| abstract [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [setBinaryStream](https://developer.android.com/reference/kotlin/java/sql/SQLXML#setBinaryStream())`()` Retrieves a stream that can be used to write the XML value that this SQLXML instance represents. |
| --- | --- |
| abstract [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [setCharacterStream](https://developer.android.com/reference/kotlin/java/sql/SQLXML#setCharacterStream())`()` Retrieves a stream to be used to write the XML value that this SQLXML instance represents. |
| abstractT | [setResult](https://developer.android.com/reference/kotlin/java/sql/SQLXML#setResult(java.lang.Class))`(`resultClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` Returns a Result for setting the XML value designated by this SQLXML instance. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](https://developer.android.com/reference/kotlin/java/sql/SQLXML#setString(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the XML value designated by this SQLXML instance to the given String representation. |
| --- | --- |

## Public methods

### free

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun free(): Unit
```

This method closes this object and releases the resources that it held. The SQL XML object becomes invalid and neither readable or writeable when this method is called. After`free`has been called, any attempt to invoke a method other than`free`will result in a`SQLException`being thrown. If`free`is called multiple times, the subsequent calls to`free`are treated as a no-op.

| Exceptions ||
|--------------------------------------------|-------------------------------------------------|
| `java.sql.SQLException` | if there is an error freeing the XML value. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBinaryStream(): InputStream!
```

Retrieves the XML value designated by this SQLXML instance as a stream. The bytes of the input stream are interpreted according to appendix F of the XML 1.0 specification. The behavior of this method is the same as ResultSet.getBinaryStream() when the designated column of the ResultSet has a type java.sql.Types of SQLXML.

The SQL XML object becomes not readable when this method is called and may also become not writable depending on implementation.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | a stream containing the XML data. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value. An exception is thrown if the state is not readable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(): Reader!
```

Retrieves the XML value designated by this SQLXML instance as a java.io.Reader object. The format of this stream is defined by org.xml.sax.InputSource, where the characters in the stream represent the unicode code points for XML according to section 2 and appendix B of the XML 1.0 specification. Although an encoding declaration other than unicode may be present, the encoding of the stream is unicode. The behavior of this method is the same as ResultSet.getCharacterStream() when the designated column of the ResultSet has a type java.sql.Types of SQLXML.

The SQL XML object becomes not readable when this method is called and may also become not writable depending on implementation.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------|
| [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | a stream containing the XML data. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value. The getCause() method of the exception may provide a more detailed exception, for example, if the stream does not contain valid characters. An exception is thrown if the state is not readable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getSource

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Source!> getSource(sourceClass: Class<T>!): T
```

Returns a Source for reading the XML value designated by this SQLXML instance. Sources are used as inputs to XML parsers and XSLT transformers.

Sources for XML parsers will have namespace processing on by default. The systemID of the Source is implementation dependent.

The SQL XML object becomes not readable when this method is called and may also become not writable depending on implementation.

Note that SAX is a callback architecture, so a returned SAXSource should then be set with a content handler that will receive the SAX events from parsing. The content handler will receive callbacks based on the contents of the XML. 

```kotlin
SAXSource saxSource = sqlxml.getSource(SAXSource.class);
    XMLReader xmlReader = saxSource.getXMLReader();
    xmlReader.setContentHandler(myHandler);
    xmlReader.parse(saxSource.getInputSource());
  
```

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sourceClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The class of the source, or null. If the class is null, a vendor specifc Source implementation will be returned. The following classes are supported at a minimum: ```kotlin javax.xml.transform.dom.DOMSource - returns a DOMSource javax.xml.transform.sax.SAXSource - returns a SAXSource javax.xml.transform.stax.StAXSource - returns a StAXSource javax.xml.transform.stream.StreamSource - returns a StreamSource ``` |

| Return ||
|---|-------------------------------------|
| T | a Source for reading the XML value. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value or if this feature is not supported. The getCause() method of the exception may provide a more detailed exception, for example, if an XML parser exception occurs. An exception is thrown if the state is not readable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### getString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getString(): String!
```

Returns a string representation of the XML value designated by this SQLXML instance. The format of this String is defined by org.xml.sax.InputSource, where the characters in the stream represent the unicode code points for XML according to section 2 and appendix B of the XML 1.0 specification. Although an encoding declaration other than unicode may be present, the encoding of the String is unicode. The behavior of this method is the same as ResultSet.getString() when the designated column of the ResultSet has a type java.sql.Types of SQLXML.

The SQL XML object becomes not readable when this method is called and may also become not writable depending on implementation.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representation of the XML value designated by this SQLXML instance. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value. The getCause() method of the exception may provide a more detailed exception, for example, if the stream does not contain valid characters. An exception is thrown if the state is not readable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setBinaryStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBinaryStream(): OutputStream!
```

Retrieves a stream that can be used to write the XML value that this SQLXML instance represents. The stream begins at position 0. The bytes of the stream are interpreted according to appendix F of the XML 1.0 specification The behavior of this method is the same as ResultSet.updateBinaryStream() when the designated column of the ResultSet has a type java.sql.Types of SQLXML.

The SQL XML object becomes not writeable when this method is called and may also become not readable depending on implementation.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | a stream to which data can be written. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value. An exception is thrown if the state is not writable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setCharacterStream

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(): Writer!
```

Retrieves a stream to be used to write the XML value that this SQLXML instance represents. The format of this stream is defined by org.xml.sax.InputSource, where the characters in the stream represent the unicode code points for XML according to section 2 and appendix B of the XML 1.0 specification. Although an encoding declaration other than unicode may be present, the encoding of the stream is unicode. The behavior of this method is the same as ResultSet.updateCharacterStream() when the designated column of the ResultSet has a type java.sql.Types of SQLXML.

The SQL XML object becomes not writeable when this method is called and may also become not readable depending on implementation.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------|
| [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | a stream to which data can be written. |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value. The getCause() method of the exception may provide a more detailed exception, for example, if the stream does not contain valid characters. An exception is thrown if the state is not writable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setResult

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Result!> setResult(resultClass: Class<T>!): T
```

Returns a Result for setting the XML value designated by this SQLXML instance.

The systemID of the Result is implementation dependent.

The SQL XML object becomes not writeable when this method is called and may also become not readable depending on implementation.

Note that SAX is a callback architecture and the returned SAXResult has a content handler assigned that will receive the SAX events based on the contents of the XML. Call the content handler with the contents of the XML document to assign the values. 

```kotlin
SAXResult saxResult = sqlxml.setResult(SAXResult.class);
    ContentHandler contentHandler = saxResult.getXMLReader().getContentHandler();
    contentHandler.startDocument();
    // set the XML elements and attributes into the result
    contentHandler.endDocument();
  
```

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>!:The class of the result, or null. If resultClass is null, a vendor specific Result implementation will be returned. The following classes are supported at a minimum: ```kotlin javax.xml.transform.dom.DOMResult - returns a DOMResult javax.xml.transform.sax.SAXResult - returns a SAXResult javax.xml.transform.stax.StAXResult - returns a StAXResult javax.xml.transform.stream.StreamResult - returns a StreamResult ``` |

| Return ||
|---|---------------------------------------------|
| T | Returns a Result for setting the XML value. |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value or if this feature is not supported. The getCause() method of the exception may provide a more detailed exception, for example, if an XML parser exception occurs. An exception is thrown if the state is not writable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

### setString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(value: String!): Unit
```

Sets the XML value designated by this SQLXML instance to the given String representation. The format of this String is defined by org.xml.sax.InputSource, where the characters in the stream represent the unicode code points for XML according to section 2 and appendix B of the XML 1.0 specification. Although an encoding declaration other than unicode may be present, the encoding of the String is unicode. The behavior of this method is the same as ResultSet.updateString() when the designated column of the ResultSet has a type java.sql.Types of SQLXML.

The SQL XML object becomes not writeable when this method is called and may also become not readable depending on implementation.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the XML value |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.sql.SQLException` | if there is an error processing the XML value. The getCause() method of the exception may provide a more detailed exception, for example, if the stream does not contain valid characters. An exception is thrown if the state is not writable. |
| `java.sql.SQLFeatureNotSupportedException` | if the JDBC driver does not support this method |

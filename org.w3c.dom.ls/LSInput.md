# LSInput

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LSInput

```
interface LSInput
```

| [org.w3c.dom.ls.LSInput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#) |

This interface represents an input source for data.

This interface allows an application to encapsulate information about an input source in a single object, which may include a public identifier, a system identifier, a byte stream (possibly with a specified encoding), a base URI, and/or a character stream.

The exact definitions of a byte stream and a character stream are binding dependent.

The application is expected to provide objects that implement this interface whenever such objects are needed. The application can either provide its own objects that implement this interface, or it can use the generic factory method`DOMImplementationLS.createLSInput()`to create objects that implement this interface.

The`LSParser`will use the`LSInput`object to determine how to read data. The`LSParser`will look at the different inputs specified in the`LSInput`in the following order to know which one to read from, the first one that is not null and not an empty string will be used:

1. `LSInput.characterStream`
2. `LSInput.byteStream`
3. `LSInput.stringData`
4. `LSInput.systemId`
5. `LSInput.publicId`

If all inputs are null, the`LSParser`will report a`DOMError`with its`DOMError.type`set to`"no-input-specified"`and its`DOMError.severity`set to`DOMError.SEVERITY_FATAL_ERROR`.

`LSInput`objects belong to the application. The DOM implementation will never modify them (though it may make copies and modify the copies, if necessary).

See also the [Document Object Model (DOM) Level 3 Load and Save Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-LS-20040407).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseURI](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getBaseURI())`()` The base URI to be used (see section 5.1.4 in \[ |
| abstract [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getByteStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getByteStream())`()` An attribute of a language and binding dependent type that represents a stream of bytes. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getCertifiedText](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getCertifiedText())`()` If set to true, assume that the input is certified (see section 2.13 in \[ |
| --- | --- |
| abstract [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getCharacterStream())`()` An attribute of a language and binding dependent type that represents a stream of 16-bit units. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getEncoding())`()` The character encoding, if known. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getPublicId())`()` The public identifier for this input source. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getStringData](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getStringData())`()` String data to parse. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#getSystemId())`()` The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this input source. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBaseURI](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setBaseURI(kotlin.String))`(`baseURI:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The base URI to be used (see section 5.1.4 in \[ |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByteStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setByteStream(java.io.InputStream))`(`byteStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` An attribute of a language and binding dependent type that represents a stream of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCertifiedText](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setCertifiedText(kotlin.Boolean))`(`certifiedText:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` If set to true, assume that the input is certified (see section 2.13 in \[ |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setCharacterStream(java.io.Reader))`(`characterStream:` ` [Reader](https://developer.android.com/reference/kotlin/java/io/Reader.html#)!`)` An attribute of a language and binding dependent type that represents a stream of 16-bit units. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setEncoding(kotlin.String))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The character encoding, if known. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicId](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setPublicId(kotlin.String))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The public identifier for this input source. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStringData](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setStringData(kotlin.String))`(`stringData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` String data to parse. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSInput#setSystemId(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this input source. |

## Public methods

### getBaseURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBaseURI(): String!
```

The base URI to be used (see section 5.1.4 in \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\]) for resolving a relative`systemId`to an absolute URI. 
If, when used, the base URI is itself a relative URI, an empty string, or null, the behavior is implementation dependent. 

### getByteStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getByteStream(): InputStream!
```

An attribute of a language and binding dependent type that represents a stream of bytes. 
If the application knows the character encoding of the byte stream, it should set the encoding attribute. Setting the encoding in this way will override any encoding specified in an XML declaration in the data. 

### getCertifiedText

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCertifiedText(): Boolean
```

If set to true, assume that the input is certified (see section 2.13 in \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\]) when parsing \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\]. 

### getCharacterStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(): Reader!
```

An attribute of a language and binding dependent type that represents a stream of 16-bit units. The application must encode the stream using UTF-16 (defined in \[Unicode\] and in \[ISO/IEC 10646\]). It is not a requirement to have an XML declaration when using character streams. If an XML declaration is present, the value of the encoding attribute will be ignored. 

### getEncoding

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoding(): String!
```

The character encoding, if known. The encoding must be a string acceptable for an XML encoding declaration (\ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\] section 4.3.3 "Character Encoding in Entities"). 
This attribute has no effect when the application provides a character stream or string data. For other sources of input, an encoding specified by means of this attribute will override any encoding specified in the XML declaration or the Text declaration, or an encoding obtained from a higher level protocol, such as HTTP \ [[IETF RFC 2616](http://www.ietf.org/rfc/rfc2616.txt)\]. 

### getPublicId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPublicId(): String!
```

The public identifier for this input source. This may be mapped to an input source using an implementation dependent mechanism (such as catalogues or other mappings). The public identifier, if specified, may also be reported as part of the location information when errors are reported. 

### getStringData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getStringData(): String!
```

String data to parse. If provided, this will always be treated as a sequence of 16-bit units (UTF-16 encoded characters). It is not a requirement to have an XML declaration when using`stringData`. If an XML declaration is present, the value of the encoding attribute will be ignored. 

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemId(): String!
```

The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this input source. The system identifier is optional if there is a byte stream, a character stream, or string data. It is still useful to provide one, since the application will use it to resolve any relative URIs and can include it in error messages and warnings. (The LSParser will only attempt to fetch the resource identified by the URI reference if there is no other input available in the input source.) 
If the application knows the character encoding of the object pointed to by the system identifier, it can set the encoding using the`encoding`attribute. 
If the specified system ID is a relative URI reference (see section 5 in \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\]), the DOM implementation will attempt to resolve the relative URI with the`baseURI`as the base, if that fails, the behavior is implementation dependent. 

### setBaseURI

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setBaseURI(baseURI: String!): Unit
```

The base URI to be used (see section 5.1.4 in \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\]) for resolving a relative`systemId`to an absolute URI. 
If, when used, the base URI is itself a relative URI, an empty string, or null, the behavior is implementation dependent. 

### setByteStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setByteStream(byteStream: InputStream!): Unit
```

An attribute of a language and binding dependent type that represents a stream of bytes. 
If the application knows the character encoding of the byte stream, it should set the encoding attribute. Setting the encoding in this way will override any encoding specified in an XML declaration in the data. 

### setCertifiedText

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCertifiedText(certifiedText: Boolean): Unit
```

If set to true, assume that the input is certified (see section 2.13 in \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\]) when parsing \ [[XML 1.1](http://www.w3.org/TR/2004/REC-xml11-20040204/)\]. 

### setCharacterStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(characterStream: Reader!): Unit
```

An attribute of a language and binding dependent type that represents a stream of 16-bit units. The application must encode the stream using UTF-16 (defined in \[Unicode\] and in \[ISO/IEC 10646\]). It is not a requirement to have an XML declaration when using character streams. If an XML declaration is present, the value of the encoding attribute will be ignored. 

### setEncoding

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEncoding(encoding: String!): Unit
```

The character encoding, if known. The encoding must be a string acceptable for an XML encoding declaration (\ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\] section 4.3.3 "Character Encoding in Entities"). 
This attribute has no effect when the application provides a character stream or string data. For other sources of input, an encoding specified by means of this attribute will override any encoding specified in the XML declaration or the Text declaration, or an encoding obtained from a higher level protocol, such as HTTP \ [[IETF RFC 2616](http://www.ietf.org/rfc/rfc2616.txt)\]. 

### setPublicId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPublicId(publicId: String!): Unit
```

The public identifier for this input source. This may be mapped to an input source using an implementation dependent mechanism (such as catalogues or other mappings). The public identifier, if specified, may also be reported as part of the location information when errors are reported. 

### setStringData

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setStringData(stringData: String!): Unit
```

String data to parse. If provided, this will always be treated as a sequence of 16-bit units (UTF-16 encoded characters). It is not a requirement to have an XML declaration when using`stringData`. If an XML declaration is present, the value of the encoding attribute will be ignored. 

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemId(systemId: String!): Unit
```

The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this input source. The system identifier is optional if there is a byte stream, a character stream, or string data. It is still useful to provide one, since the application will use it to resolve any relative URIs and can include it in error messages and warnings. (The LSParser will only attempt to fetch the resource identified by the URI reference if there is no other input available in the input source.) 
If the application knows the character encoding of the object pointed to by the system identifier, it can set the encoding using the`encoding`attribute. 
If the specified system ID is a relative URI reference (see section 5 in \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\]), the DOM implementation will attempt to resolve the relative URI with the`baseURI`as the base, if that fails, the behavior is implementation dependent.

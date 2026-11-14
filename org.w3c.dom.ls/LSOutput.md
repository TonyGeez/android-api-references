# LSOutput

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LSOutput

```
interface LSOutput
```

| [org.w3c.dom.ls.LSOutput](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#) |

This interface represents an output destination for data.

This interface allows an application to encapsulate information about an output destination in a single object, which may include a URI, a byte stream (possibly with a specified encoding), a base URI, and/or a character stream.

The exact definitions of a byte stream and a character stream are binding dependent.

The application is expected to provide objects that implement this interface whenever such objects are needed. The application can either provide its own objects that implement this interface, or it can use the generic factory method`DOMImplementationLS.createLSOutput()`to create objects that implement this interface.

The`LSSerializer`will use the`LSOutput`object to determine where to serialize the output to. The`LSSerializer`will look at the different outputs specified in the`LSOutput`in the following order to know which one to output to, the first one that is not null and not an empty string will be used:

1. `LSOutput.characterStream`
2. `LSOutput.byteStream`
3. `LSOutput.systemId`

`LSOutput`objects belong to the application. The DOM implementation will never modify them (though it may make copies and modify the copies, if necessary).

See also the [Document Object Model (DOM) Level 3 Load and Save Specification](http://www.w3.org/TR/2004/REC-DOM-Level-3-LS-20040407).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getByteStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#getByteStream())`()` An attribute of a language and binding dependent type that represents a writable stream of bytes. |
| abstract [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)! | [getCharacterStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#getCharacterStream())`()` An attribute of a language and binding dependent type that represents a writable stream to which 16-bit units can be output. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#getEncoding())`()` The character encoding to use for the output. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#getSystemId())`()` The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this output destination. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByteStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#setByteStream(java.io.OutputStream))`(`byteStream:` ` [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)!`)` An attribute of a language and binding dependent type that represents a writable stream of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#setCharacterStream(java.io.Writer))`(`characterStream:` ` [Writer](https://developer.android.com/reference/kotlin/java/io/Writer.html#)!`)` An attribute of a language and binding dependent type that represents a writable stream to which 16-bit units can be output. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#setEncoding(kotlin.String))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The character encoding to use for the output. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](https://developer.android.com/reference/kotlin/org/w3c/dom/ls/LSOutput#setSystemId(kotlin.String))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this output destination. |

## Public methods

### getByteStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getByteStream(): OutputStream!
```

An attribute of a language and binding dependent type that represents a writable stream of bytes. 

### getCharacterStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCharacterStream(): Writer!
```

An attribute of a language and binding dependent type that represents a writable stream to which 16-bit units can be output. 

### getEncoding

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoding(): String!
```

The character encoding to use for the output. The encoding must be a string acceptable for an XML encoding declaration (\ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\] section 4.3.3 "Character Encoding in Entities"), it is recommended that character encodings registered (as charsets) with the Internet Assigned Numbers Authority \ [[IANA-CHARSETS](ftp://ftp.isi.edu/in-notes/iana/assignments/character-sets)\] should be referred to using their registered names. 

### getSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSystemId(): String!
```

The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this output destination. 
If the system ID is a relative URI reference (see section 5 in \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\]), the behavior is implementation dependent. 

### setByteStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setByteStream(byteStream: OutputStream!): Unit
```

An attribute of a language and binding dependent type that represents a writable stream of bytes. 

### setCharacterStream

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCharacterStream(characterStream: Writer!): Unit
```

An attribute of a language and binding dependent type that represents a writable stream to which 16-bit units can be output. 

### setEncoding

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEncoding(encoding: String!): Unit
```

The character encoding to use for the output. The encoding must be a string acceptable for an XML encoding declaration (\ [[XML 1.0](http://www.w3.org/TR/2004/REC-xml-20040204)\] section 4.3.3 "Character Encoding in Entities"), it is recommended that character encodings registered (as charsets) with the Internet Assigned Numbers Authority \ [[IANA-CHARSETS](ftp://ftp.isi.edu/in-notes/iana/assignments/character-sets)\] should be referred to using their registered names. 

### setSystemId

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setSystemId(systemId: String!): Unit
```

The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this output destination. 
If the system ID is a relative URI reference (see section 5 in \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\]), the behavior is implementation dependent.

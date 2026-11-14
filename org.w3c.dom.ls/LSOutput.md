# LSOutput

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LSOutput

```
interface LSOutput
```

| [org.w3c.dom.ls.LSOutput](LSOutput.md) |

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
| abstract [OutputStream](../java.io/OutputStream.md)! | [getByteStream](LSOutput.md))`()` An attribute of a language and binding dependent type that represents a writable stream of bytes. |
| abstract [Writer](../java.io/Writer.md)! | [getCharacterStream](LSOutput.md))`()` An attribute of a language and binding dependent type that represents a writable stream to which 16-bit units can be output. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](LSOutput.md))`()` The character encoding to use for the output. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](LSOutput.md))`()` The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this output destination. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByteStream](LSOutput.md))`(`byteStream:` ` [OutputStream](../java.io/OutputStream.md)!`)` An attribute of a language and binding dependent type that represents a writable stream of bytes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](LSOutput.md))`(`characterStream:` ` [Writer](../java.io/Writer.md)!`)` An attribute of a language and binding dependent type that represents a writable stream to which 16-bit units can be output. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](LSOutput.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The character encoding to use for the output. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](LSOutput.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The system identifier, a URI reference \ [[IETF RFC 2396](http://www.ietf.org/rfc/rfc2396.txt)\], for this output destination. |

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

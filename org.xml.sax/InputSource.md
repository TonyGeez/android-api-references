# InputSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputSource

```
open class InputSource
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xml.sax.InputSource](InputSource.md) |

A single input source for an XML entity.*This module, both source code and documentation, is in the Public Domain, and comes with**NO WARRANTY**.* See<http://www.saxproject.org>for further information.

This class allows a SAX application to encapsulate information about an input source in a single object, which may include a public identifier, a system identifier, a byte stream (possibly with a specified encoding), and/or a character stream.

There are two places that the application can deliver an input source to the parser: as the argument to the Parser.parse method, or as the return value of the EntityResolver.resolveEntity method.

The SAX parser will use the InputSource object to determine how to read XML input. If there is a character stream available, the parser will read that stream directly, disregarding any text encoding declaration found in that stream. If there is no character stream, but there is a byte stream, the parser will use that byte stream, using the encoding specified in the InputSource or else (if no encoding is specified) autodetecting the character encoding using an algorithm such as the one in the XML specification. If neither a character stream nor a byte stream is available, the parser will attempt to open a URI connection to the resource identified by the system identifier.

An InputSource object belongs to the application: the SAX parser shall never modify it in any way (it may modify a copy if necessary). However, standard processing of both byte and character streams is to close them on as part of end-of-parse cleanup, so applications should not attempt to re-use such streams after they have been handed to a parser.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InputSource](InputSource.md))`()` Zero-argument default constructor. |
| [InputSource](InputSource.md))`(`byteStream:` ` [InputStream](../java.io/InputStream.md)!`)` Create a new input source with a byte stream. |
| [InputSource](InputSource.md))`(`characterStream:` ` [Reader](../java.io/Reader.md)!`)` Create a new input source with a character stream. |
| [InputSource](InputSource.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a new input source with a system identifier. |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InputStream](../java.io/InputStream.md)! | [getByteStream](InputSource.md))`()` Get the byte stream for this input source. |
| open [Reader](../java.io/Reader.md)! | [getCharacterStream](InputSource.md))`()` Get the character stream for this input source. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](InputSource.md))`()` Get the character encoding for a byte stream or URI. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](InputSource.md))`()` Get the public identifier for this input source. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](InputSource.md))`()` Get the system identifier for this input source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByteStream](InputSource.md))`(`byteStream:` ` [InputStream](../java.io/InputStream.md)!`)` Set the byte stream for this input source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCharacterStream](InputSource.md))`(`characterStream:` ` [Reader](../java.io/Reader.md)!`)` Set the character stream for this input source. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](InputSource.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the character encoding, if known. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicId](InputSource.md))`(`publicId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the public identifier for this input source. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemId](InputSource.md))`(`systemId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the system identifier for this input source. |

## Public constructors

### InputSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputSource()
```

Zero-argument default constructor. 
**See Also**

- [#setPublicId](InputSource.md))
- [#setSystemId](InputSource.md))
- [#setByteStream](InputSource.md))
- [#setCharacterStream](InputSource.md))
- [#setEncoding](InputSource.md)) 

### InputSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputSource(byteStream: InputStream!)
```

Create a new input source with a byte stream.

Application writers should use setSystemId() to provide a base for resolving relative URIs, may use setPublicId to include a public identifier, and may use setEncoding to specify the object's character encoding.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `byteStream` | [InputStream](../java.io/InputStream.md)!:The raw byte stream containing the document. |

**See Also**

- [#setPublicId](InputSource.md))
- [#setSystemId](InputSource.md))
- [#setEncoding](InputSource.md))
- [#setByteStream](InputSource.md))
- [#setCharacterStream](InputSource.md)) 

### InputSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputSource(characterStream: Reader!)
```

Create a new input source with a character stream.

Application writers should use setSystemId() to provide a base for resolving relative URIs, and may use setPublicId to include a public identifier.

The character stream shall not include a byte order mark.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `characterStream` | [Reader](../java.io/Reader.md)!:The raw character stream containing the document. |

**See Also**

- [#setPublicId](InputSource.md))
- [#setSystemId](InputSource.md))
- [#setByteStream](InputSource.md))
- [#setCharacterStream](InputSource.md)) 

### InputSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InputSource(systemId: String!)
```

Create a new input source with a system identifier.

Applications may use setPublicId to include a public identifier as well, or setEncoding to specify the character encoding, if known.

If the system identifier is a URL, it must be fully resolved (it may not be a relative URL).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier (URI). |

**See Also**

- [#setPublicId](InputSource.md))
- [#setSystemId](InputSource.md))
- [#setByteStream](InputSource.md))
- [#setEncoding](InputSource.md))
- [#setCharacterStream](InputSource.md))

## Public methods

### getByteStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getByteStream(): InputStream!
```

Get the byte stream for this input source.

The getEncoding method will return the character encoding for this byte stream, or null if unknown.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------|
| [InputStream](../java.io/InputStream.md)! | The byte stream, or null if none was supplied. |

**See Also**

- [#getEncoding](InputSource.md))
- [#setByteStream](InputSource.md)) 

### getCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharacterStream(): Reader!
```

Get the character stream for this input source.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [Reader](../java.io/Reader.md)! | The character stream, or null if none was supplied. |

**See Also**

- [#setCharacterStream](InputSource.md)) 

### getEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoding(): String!
```

Get the character encoding for a byte stream or URI. This value will be ignored when the application provides a character stream.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The encoding, or null if none was supplied. |

**See Also**

- [#setByteStream](InputSource.md))
- [#getSystemId](InputSource.md))
- [#getByteStream](InputSource.md)) 

### getPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicId(): String!
```

Get the public identifier for this input source.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The public identifier, or null if none was supplied. |

**See Also**

- [#setPublicId](InputSource.md)) 

### getSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSystemId(): String!
```

Get the system identifier for this input source.

The getEncoding method will return the character encoding of the object pointed to, or null if unknown.

If the system ID is a URL, it will be fully resolved.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The system identifier, or null if none was supplied. |

**See Also**

- [#setSystemId](InputSource.md))
- [#getEncoding](InputSource.md)) 

### setByteStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setByteStream(byteStream: InputStream!): Unit
```

Set the byte stream for this input source.

The SAX parser will ignore this if there is also a character stream specified, but it will use a byte stream in preference to opening a URI connection itself.

If the application knows the character encoding of the byte stream, it should set it with the setEncoding method.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `byteStream` | [InputStream](../java.io/InputStream.md)!:A byte stream containing an XML document or other entity. |

**See Also**

- [#setEncoding](InputSource.md))
- [#getByteStream](InputSource.md))
- [#getEncoding](InputSource.md))
- [java.io.InputStream](../java.io/InputStream.md) 

### setCharacterStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCharacterStream(characterStream: Reader!): Unit
```

Set the character stream for this input source.

If there is a character stream specified, the SAX parser will ignore any byte stream and will not attempt to open a URI connection to the system identifier.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `characterStream` | [Reader](../java.io/Reader.md)!:The character stream containing the XML document or other entity. |

**See Also**

- [#getCharacterStream](InputSource.md))
- [java.io.Reader](../java.io/Reader.md) 

### setEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEncoding(encoding: String!): Unit
```

Set the character encoding, if known.

The encoding must be a string acceptable for an XML encoding declaration (see section 4.3.3 of the XML 1.0 recommendation).

This method has no effect when the application provides a character stream.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A string describing the character encoding. |

**See Also**

- [#setSystemId](InputSource.md))
- [#setByteStream](InputSource.md))
- [#getEncoding](InputSource.md)) 

### setPublicId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPublicId(publicId: String!): Unit
```

Set the public identifier for this input source.

The public identifier is always optional: if the application writer includes one, it will be provided as part of the location information.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `publicId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The public identifier as a string. |

**See Also**

- [#getPublicId](InputSource.md))
- [org.xml.sax.Locator#getPublicId](Locator.md))
- [org.xml.sax.SAXParseException#getPublicId](SAXParseException.md)) 

### setSystemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSystemId(systemId: String!): Unit
```

Set the system identifier for this input source.

The system identifier is optional if there is a byte stream or a character stream, but it is still useful to provide one, since the application can use it to resolve relative URIs and can include it in error messages and warnings (the parser will attempt to open a connection to the URI only if there is no byte stream or character stream specified).

If the application knows the character encoding of the object pointed to by the system identifier, it can register the encoding using the setEncoding method.

If the system identifier is a URL, it must be fully resolved (it may not be a relative URL).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `systemId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The system identifier as a string. |

**See Also**

- [#setEncoding](InputSource.md))
- [#getSystemId](InputSource.md))
- [org.xml.sax.Locator#getSystemId](Locator.md))
- [org.xml.sax.SAXParseException#getSystemId](SAXParseException.md))

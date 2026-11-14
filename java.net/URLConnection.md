# URLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLConnection

```
abstract class URLConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.URLConnection](URLConnection.md) |

| Known Direct Subclasses [HttpURLConnection](HttpURLConnection.md), [JarURLConnection](JarURLConnection.md) |------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [HttpURLConnection](HttpURLConnection.md) | A URLConnection with support for HTTP-specific features. | | [JarURLConnection](JarURLConnection.md) | A URL Connection to a Java ARchive (JAR) file or an entry in a JAR file. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [HttpsURLConnection](../javax.net.ssl/HttpsURLConnection.md) |-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [HttpsURLConnection](../javax.net.ssl/HttpsURLConnection.md) | `HttpsURLConnection`extends`HttpURLConnection`with support for https-specific features. | |
| --- | --- | --- | --- | --- | --- | --- |

The abstract class is the superclass of all classes that represent a communications link between the application and a URL. Instances of this class can be used both to read from and to write to the resource referenced by the URL. In general, creating a connection to a URL is a multistep process:

| `openConnection()` | `connect()` |
|--------------------------------------------------------------------------|---------------------------------------------------------------|
| Manipulate parameters that affect the connection to the remote resource. | Interact with the resource; query header fields and contents. |

----------------------------\> 
time

1. The connection object is created by invoking the`openConnection`method on a URL.
2. The setup parameters and general request properties are manipulated.
3. The actual connection to the remote object is made, using the`connect`method.
4. The remote object becomes available. The header fields and the contents of the remote object can be accessed.

<br />

The setup parameters are modified using the following methods:

- `setAllowUserInteraction`
- `setDoInput`
- `setDoOutput`
- `setIfModifiedSince`
- `setUseCaches`

and the general request properties are modified using the method:

- `setRequestProperty`

Default values for the`AllowUserInteraction`and`UseCaches`parameters can be set using the methods`setDefaultAllowUserInteraction`and`setDefaultUseCaches`.

Each of the above`set`methods has a corresponding`get`method to retrieve the value of the parameter or general request property. The specific parameters and general request properties that are applicable are protocol specific.

The following methods are used to access the header fields and the contents after the connection is made to the remote object:

- `getContent`
- `getHeaderField`
- `getInputStream`
- `getOutputStream`

Certain header fields are accessed frequently. The methods:

- `getContentEncoding`
- `getContentLength`
- `getContentType`
- `getDate`
- `getExpiration`
- `getLastModifed`

provide convenient access to these fields. The`getContentType`method is used by the`getContent`method to determine the type of the remote object; subclasses may find it convenient to override the`getContentType`method.

In the common case, all of the pre-connection parameters and general request properties can be ignored: the pre-connection parameters and request properties default to sensible values. For most clients of this interface, there are only two interesting methods:`getInputStream`and`getContent`, which are mirrored in the`URL`class by convenience methods.

More information on the request properties and header fields of an`http`connection can be found at: 

```kotlin
<a href="http://www.ietf.org/rfc/rfc2616.txt">http://www.ietf.org/rfc/rfc2616.txt</a>
```
Invoking the`close()`methods on the`InputStream`or`OutputStream`of an`URLConnection`after a request may free network resources associated with this instance, unless particular protocol specifications specify different behaviours for it.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [URLConnection](URLConnection.md))`(`url:` ` [URL](URL.md)!`)` Constructs a URL connection to the specified URL. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addRequestProperty](URLConnection.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Adds a general request property specified by a key-value pair. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](URLConnection.md))`()` Opens a communications link to the resource referenced by this URL, if such a connection has not already been established. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowUserInteraction](URLConnection.md))`()` Returns the value of the`allowUserInteraction`field for this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectTimeout](URLConnection.md))`()` Returns setting for connect timeout. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContent](URLConnection.md))`()` Retrieves the contents of this URL connection. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContent](URLConnection.md))`(`classes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!>!`)` Retrieves the contents of this URL connection. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getContentEncoding](URLConnection.md))`()` Returns the value of the`content-encoding`header field. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentLength](URLConnection.md))`()` Returns the value of the`content-length`header field. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getContentLengthLong](URLConnection.md))`()` Returns the value of the`content-length`header field as a long. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getContentType](URLConnection.md))`()` Returns the value of the`content-type`header field. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDate](URLConnection.md))`()` Returns the value of the`date`header field. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDefaultAllowUserInteraction](URLConnection.md))`()` Returns the default value of the`allowUserInteraction`field. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultRequestProperty](URLConnection.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value of the default request property. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDefaultUseCaches](URLConnection.md))`()` Returns the default value of a`URLConnection`'s`useCaches`flag. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDoInput](URLConnection.md))`()` Returns the value of this`URLConnection`'s`doInput`flag. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDoOutput](URLConnection.md))`()` Returns the value of this`URLConnection`'s`doOutput`flag. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getExpiration](URLConnection.md))`()` Returns the value of the`expires`header field. |
| openstatic [FileNameMap](FileNameMap.md)! | [getFileNameMap](URLConnection.md))`()` Returns a [FileNameMap](FileNameMap.md) implementation suitable for guessing a content type based on a URL's "file" component. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHeaderField](URLConnection.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value for the`n`th header field. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHeaderField](URLConnection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value of the named header field. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getHeaderFieldDate](URLConnection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `Default:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value of the named field parsed as date. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeaderFieldInt](URLConnection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `Default:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the named field parsed as a number. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHeaderFieldKey](URLConnection.md))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the key for the`n`th header field. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getHeaderFieldLong](URLConnection.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `Default:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the value of the named field parsed as a number. |
| --- | --- |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [getHeaderFields](URLConnection.md))`()` Returns an unmodifiable Map of the header fields. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getIfModifiedSince](URLConnection.md))`()` Returns the value of this object's`ifModifiedSince`field. |
| open [InputStream](../java.io/InputStream.md)! | [getInputStream](URLConnection.md))`()` Returns an input stream that reads from this open connection. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastModified](URLConnection.md))`()` Returns the value of the`last-modified`header field. |
| open [OutputStream](../java.io/OutputStream.md)! | [getOutputStream](URLConnection.md))`()` Returns an output stream that writes to this connection. |
| open [Permission](../java.security/Permission.md)! | [getPermission](URLConnection.md))`()` Returns a permission object representing the permission necessary to make the connection represented by this object. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReadTimeout](URLConnection.md))`()` Returns setting for read timeout. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [getRequestProperties](URLConnection.md))`()` Returns an unmodifiable Map of general request properties for this connection. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRequestProperty](URLConnection.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the value of the named general request property for this connection. |
| --- | --- |
| open [URL](URL.md)! | [getURL](URLConnection.md))`()` Returns the value of this`URLConnection`'s`URL`field. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseCaches](URLConnection.md))`()` Returns the value of this`URLConnection`'s`useCaches`field. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [guessContentTypeFromName](URLConnection.md))`(`fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tries to determine the content type of an object, based on the specified "file" component of a URL. |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [guessContentTypeFromStream](URLConnection.md))`(`is:` ` [InputStream](../java.io/InputStream.md)!`)` Tries to determine the type of an input stream based on the characters at the beginning of the input stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowUserInteraction](URLConnection.md))`(`allowuserinteraction:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the value of the`allowUserInteraction`field of this`URLConnection`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConnectTimeout](URLConnection.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets a specified timeout value, in milliseconds, to be used when opening a communications link to the resource referenced by this URLConnection. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandlerFactory](URLConnection.md))`(`fac:` ` [ContentHandlerFactory](ContentHandlerFactory.md)!`)` Sets the`ContentHandlerFactory`of an application. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultAllowUserInteraction](URLConnection.md))`(`defaultallowuserinteraction:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the default value of the`allowUserInteraction`field for all future`URLConnection`objects to the specified value. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultRequestProperty](URLConnection.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the default value of a general request property. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultUseCaches](URLConnection.md))`(`defaultusecaches:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the default value of the`useCaches`field to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDoInput](URLConnection.md))`(`doinput:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value of the`doInput`field for this`URLConnection`to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDoOutput](URLConnection.md))`(`dooutput:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value of the`doOutput`field for this`URLConnection`to the specified value. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFileNameMap](URLConnection.md))`(`map:` ` [FileNameMap](FileNameMap.md)!`)` Sets the FileNameMap. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIfModifiedSince](URLConnection.md))`(`ifmodifiedsince:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value of the`ifModifiedSince`field of this`URLConnection`to the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadTimeout](URLConnection.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the read timeout to a specified timeout, in milliseconds. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRequestProperty](URLConnection.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the general request property. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseCaches](URLConnection.md))`(`usecaches:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value of the`useCaches`field of this`URLConnection`to the specified value. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](URLConnection.md))`()` Returns a`String`representation of this URL connection. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowUserInteraction](URLConnection.md) If`true`, this`URL`is being examined in a context in which it makes sense to allow user interactions such as popping up an authentication dialog. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connected](URLConnection.md) If`false`, this connection object has not created a communications link to the specified URL. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [doInput](URLConnection.md) This variable is set by the`setDoInput`method. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [doOutput](URLConnection.md) This variable is set by the`setDoOutput`method. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ifModifiedSince](URLConnection.md) Some protocols support skipping the fetching of the object unless the object has been modified more recently than a certain time. |
| [URL](URL.md)! | [url](URLConnection.md) The URL represents the remote object on the World Wide Web to which this connection is opened. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [useCaches](URLConnection.md) If`true`, the protocol is allowed to use caching whenever it can. |

## Protected constructors

### URLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected URLConnection(url: URL!)
```

Constructs a URL connection to the specified URL. A connection to the object referenced by the URL is not created.

| Parameters ||
|-------|----------------------------------------------------------------------------------------|
| `url` | [URL](URL.md)!:the specified URL. |

## Public methods

### addRequestProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addRequestProperty(
    key: String!, 
    value: String!
): Unit
```

Adds a general request property specified by a key-value pair. This method will not overwrite existing values associated with the same key.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword by which the request is known (e.g., "`Accept`"). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value associated with it. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |
| `java.lang.NullPointerException` | if key is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getRequestProperties()> 

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(): Unit
```

Opens a communications link to the resource referenced by this URL, if such a connection has not already been established.

If the`connect`method is called when the connection has already been opened (indicated by the`connected`field having the value`true`), the call is ignored.

URLConnection objects go through two phases: first they are created, then they are connected. After being created, and before being connected, various options can be specified (e.g., doInput and UseCaches). After connecting, it is an error to try to set them. Operations that depend on being connected, like getContentLength, will implicitly perform the connection, if necessary.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------|
| `java.net.SocketTimeoutException` | if the timeout expires before the connection can be established |
| `java.io.IOException` | if an I/O error occurs while opening the connection. |

**See Also**

- [java.net.URLConnection#connected](URLConnection.md)
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getConnectTimeout()>
- [#setConnectTimeout(int)](URLConnection.md)) 

### getAllowUserInteraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllowUserInteraction(): Boolean
```

Returns the value of the`allowUserInteraction`field for this object.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the`allowUserInteraction`field for this object. |

**See Also**

- [#setAllowUserInteraction(boolean)](URLConnection.md)) 

### getConnectTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConnectTimeout(): Int
```

Returns setting for connect timeout.

0 return implies that the option is disabled (i.e., timeout of infinity).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`that indicates the connect timeout value in milliseconds |

**See Also**

- [#setConnectTimeout(int)](URLConnection.md))
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#connect()> 

### getContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContent(): Any!
```

Retrieves the contents of this URL connection.

This method first determines the content type of the object by calling the`getContentType`method. If this is the first time that the application has seen that specific content type, a content handler for that content type is created:

1. If the application has set up a content handler factory instance using the`setContentHandlerFactory`method, the`createContentHandler`method of that instance is called with the content type as an argument; the result is a content handler for that content type.
2. If no content handler factory has yet been set up, or if the factory's`createContentHandler`method returns`null`, then the application loads the class named: 

   ```kotlin
   sun.net.www.content.<<i>contentType</i>>
         
   ```
 where \<*contentType* \> is formed by taking the content-type string, replacing all slash characters with a`period`('.'), and all other non-alphanumeric characters with the underscore character '`_`'. The alphanumeric characters are specifically the 26 uppercase ASCII letters '`A`' through '`Z`', the 26 lowercase ASCII letters '`a`' through '`z`', and the 10 ASCII digits '`0`' through '`9`'. If the specified class does not exist, or is not a subclass of`ContentHandler`, then an`UnknownServiceException`is thrown.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object fetched. The`instanceof`operator should be used to determine the specific kind of object returned. |

| Exceptions ||
|------------------------------------|----------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while getting the content. |
| `java.net.UnknownServiceException` | if the protocol does not support the content type. |

**See Also**

- [java.net.ContentHandlerFactory#createContentHandler(java.lang.String)](ContentHandlerFactory.md))
- [java.net.URLConnection#getContentType()](URLConnection.md))
- [java.net.URLConnection#setContentHandlerFactory(java.net.ContentHandlerFactory)](URLConnection.md)) 

### getContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContent(classes: Array<Class<Any!>!>!): Any!
```

Retrieves the contents of this URL connection.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `classes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>!:the`Class`array indicating the requested types |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object fetched that is the first match of the type specified in the classes array. null if none of the requested types are supported. The`instanceof`operator should be used to determine the specific kind of object returned. |

| Exceptions ||
|------------------------------------|----------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while getting the content. |
| `java.net.UnknownServiceException` | if the protocol does not support the content type. |

**See Also**

- [java.net.URLConnection#getContent()](URLConnection.md))
- [java.net.ContentHandlerFactory#createContentHandler(java.lang.String)](ContentHandlerFactory.md))
- [java.net.URLConnection#getContent(java.lang.Class[])](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent(kotlin.Array))
- [java.net.URLConnection#setContentHandlerFactory(java.net.ContentHandlerFactory)](URLConnection.md)) 

### getContentEncoding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentEncoding(): String!
```

Returns the value of the`content-encoding`header field.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the content encoding of the resource that the URL references, or`null`if not known. |

**See Also**

- [java.net.URLConnection#getHeaderField(java.lang.String)](URLConnection.md)) 

### getContentLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentLength(): Int
```

Returns the value of the`content-length`header field.

**Note** : [getContentLengthLong()](URLConnection.md))should be preferred over this method, since it returns a`long`instead and is therefore more portable.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the content length of the resource that this connection's URL references,`-1`if the content length is not known, or if the content length is greater than Integer.MAX_VALUE. |

### getContentLengthLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentLengthLong(): Long
```

Returns the value of the`content-length`header field as a long.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the content length of the resource that this connection's URL references, or`-1`if the content length is not known. |

### getContentType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentType(): String!
```

Returns the value of the`content-type`header field.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the content type of the resource that the URL references, or`null`if not known. |

**See Also**

- [java.net.URLConnection#getHeaderField(java.lang.String)](URLConnection.md)) 

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDate(): Long
```

Returns the value of the`date`header field.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sending date of the resource that the URL references, or`0`if not known. The value returned is the number of milliseconds since January 1, 1970 GMT. |

**See Also**

- [java.net.URLConnection#getHeaderField(java.lang.String)](URLConnection.md)) 

### getDefaultAllowUserInteraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultAllowUserInteraction(): Boolean
```

Returns the default value of the`allowUserInteraction`field.

Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the default value of the`allowUserInteraction`field. |

**See Also**

- [#setDefaultAllowUserInteraction(boolean)](URLConnection.md)) 

### getDefaultRequestProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefaultRequestProperty(key: String!): String!
```

**Deprecated:** *The instance specific getRequestProperty method should be used after an appropriate instance of URLConnection is obtained.*

Returns the value of the default request property. Default request properties are set for every connection.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword by which the request is known (e.g., "Accept"). |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the default request property for the specified key. |

**See Also**

- [java.net.URLConnection#getRequestProperty(java.lang.String)](URLConnection.md))
- [#setDefaultRequestProperty(java.lang.String, java.lang.String)](URLConnection.md)) 

### getDefaultUseCaches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultUseCaches(): Boolean
```

Returns the default value of a`URLConnection`'s`useCaches`flag.

Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the default value of a`URLConnection`'s`useCaches`flag. |

**See Also**

- [#setDefaultUseCaches(boolean)](URLConnection.md)) 

### getDoInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDoInput(): Boolean
```

Returns the value of this`URLConnection`'s`doInput`flag.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of this`URLConnection`'s`doInput`flag. |

**See Also**

- [#setDoInput(boolean)](URLConnection.md)) 

### getDoOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDoOutput(): Boolean
```

Returns the value of this`URLConnection`'s`doOutput`flag.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of this`URLConnection`'s`doOutput`flag. |

**See Also**

- [#setDoOutput(boolean)](URLConnection.md)) 

### getExpiration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExpiration(): Long
```

Returns the value of the`expires`header field.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the expiration date of the resource that this URL references, or 0 if not known. The value is the number of milliseconds since January 1, 1970 GMT. |

**See Also**

- [java.net.URLConnection#getHeaderField(java.lang.String)](URLConnection.md)) 

### getFileNameMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getFileNameMap(): FileNameMap!
```

Returns a [FileNameMap](FileNameMap.md) implementation suitable for guessing a content type based on a URL's "file" component. 
**See Also**

- [#guessContentTypeFromName(String)](URLConnection.md))
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#setFileNameMap(java.net.FileNameMap)> 

### getHeaderField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderField(n: Int): String!
```

Returns the value for the`n`th header field. It returns`null`if there are fewer than`n+1`fields.

This method can be used in conjunction with the [getHeaderFieldKey](URLConnection.md))method to iterate through all the headers in the message.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index, where`n>=0` |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the`n`th header field or`null`if there are fewer than`n+1`fields |

**See Also**

- [java.net.URLConnection#getHeaderFieldKey(int)](URLConnection.md)) 

### getHeaderField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderField(name: String!): String!
```

Returns the value of the named header field.

If called on a connection that sets the same header multiple times with possibly different values, only the last value is returned.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of a header field. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the named header field, or`null`if there is no such field in the header. |

### getHeaderFieldDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderFieldDate(
    name: String!, 
    Default: Long
): Long
```

Returns the value of the named field parsed as date. The result is the number of milliseconds since January 1, 1970 GMT represented by the named field.

This form of`getHeaderField`exists because some connection types (e.g.,`http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the header field. |
| `Default` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a default value. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of the field, parsed as a date. The value of the`Default`argument is returned if the field is missing or malformed. |

### getHeaderFieldInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderFieldInt(
    name: String!, 
    Default: Int
): Int
```

Returns the value of the named field parsed as a number.

This form of`getHeaderField`exists because some connection types (e.g.,`http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the header field. |
| `Default` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the default value. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the named field, parsed as an integer. The`Default`value is returned if the field is missing or malformed. |

### getHeaderFieldKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderFieldKey(n: Int): String!
```

Returns the key for the`n`th header field. It returns`null`if there are fewer than`n+1`fields.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index, where`n>=0` |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the key for the`n`th header field, or`null`if there are fewer than`n+1`fields. |

### getHeaderFieldLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderFieldLong(
    name: String!, 
    Default: Long
): Long
```

Returns the value of the named field parsed as a number.

This form of`getHeaderField`exists because some connection types (e.g.,`http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the header field. |
| `Default` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the default value. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of the named field, parsed as a long. The`Default`value is returned if the field is missing or malformed. |

### getHeaderFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeaderFields(): MutableMap<String!, MutableList<String!>!>!
```

Returns an unmodifiable Map of the header fields. The Map keys are Strings that represent the response-header field names. Each Map value is an unmodifiable List of Strings that represents the corresponding field values.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | a Map of header fields |

### getIfModifiedSince

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIfModifiedSince(): Long
```

Returns the value of this object's`ifModifiedSince`field.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of this object's`ifModifiedSince`field. |

**See Also**

- [#setIfModifiedSince(long)](URLConnection.md)) 

### getInputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputStream(): InputStream!
```

Returns an input stream that reads from this open connection. A SocketTimeoutException can be thrown when reading from the returned input stream if the read timeout expires before data is available for read.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [InputStream](../java.io/InputStream.md)! | an input stream that reads from this open connection. |

| Exceptions ||
|------------------------------------|---------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the input stream. |
| `java.net.UnknownServiceException` | if the protocol does not support input. |

**See Also**

- [#setReadTimeout(int)](URLConnection.md))
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getReadTimeout()> 

### getLastModified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLastModified(): Long
```

Returns the value of the`last-modified`header field. The result is the number of milliseconds since January 1, 1970 GMT.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the date the resource referenced by this`URLConnection`was last modified, or 0 if not known. |

**See Also**

- [java.net.URLConnection#getHeaderField(java.lang.String)](URLConnection.md)) 

### getOutputStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOutputStream(): OutputStream!
```

Returns an output stream that writes to this connection.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------|
| [OutputStream](../java.io/OutputStream.md)! | an output stream that writes to this connection. |

| Exceptions ||
|------------------------------------|----------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while creating the output stream. |
| `java.net.UnknownServiceException` | if the protocol does not support output. |

### getPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPermission(): Permission!
```

Returns a permission object representing the permission necessary to make the connection represented by this object. This method returns null if no permission is required to make the connection. By default, this method returns`java.security.AllPermission`. Subclasses should override this method and return the permission that best represents the permission required to make a a connection to the URL. For example, a`URLConnection`representing a`file:`URL would return a`java.io.FilePermission`object.

The permission returned may dependent upon the state of the connection. For example, the permission before connecting may be different from that after connecting. For example, an HTTP sever, say foo.com, may redirect the connection to a different host, say bar.com. Before connecting the permission returned by the connection will represent the permission needed to connect to foo.com, while the permission returned after connecting will be to bar.com.

Permissions are generally used for two purposes: to protect caches of objects obtained through URLConnections, and to check the right of a recipient to learn about a particular URL. In the first case, the permission should be obtained*after* the object has been obtained. For example, in an HTTP connection, this will represent the permission to connect to the host from which the data was ultimately fetched. In the second case, the permission should be obtained and tested*before*connecting.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Permission](../java.security/Permission.md)! | the permission object representing the permission necessary to make the connection represented by this URLConnection. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if the computation of the permission requires network or file I/O and an exception occurs while computing it. |

### getReadTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReadTimeout(): Int
```

Returns setting for read timeout. 0 return implies that the option is disabled (i.e., timeout of infinity).

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`that indicates the read timeout value in milliseconds |

**See Also**

- [#setReadTimeout(int)](URLConnection.md))
- [java.io.InputStream#read()](../java.io/InputStream.md)) 

### getRequestProperties

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestProperties(): MutableMap<String!, MutableList<String!>!>!
```

Returns an unmodifiable Map of general request properties for this connection. The Map keys are Strings that represent the request-header field names. Each Map value is a unmodifiable List of Strings that represents the corresponding field values.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | a Map of the general request properties for this connection. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

### getRequestProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestProperty(key: String!): String!
```

Returns the value of the named general request property for this connection.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword by which the request is known (e.g., "Accept"). |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the named general request property for this connection. If key is null, then null is returned. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

**See Also**

- [#setRequestProperty(java.lang.String, java.lang.String)](URLConnection.md)) 

### getURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getURL(): URL!
```

Returns the value of this`URLConnection`'s`URL`field.

| Return ||
|---------------------------------------------------------------------|-----------------------------------------------|
| [URL](URL.md)! | the value of this`URLConnection`'s`URL`field. |

**See Also**

- [java.net.URLConnection#url](URLConnection.md) 

### getUseCaches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUseCaches(): Boolean
```

Returns the value of this`URLConnection`'s`useCaches`field.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of this`URLConnection`'s`useCaches`field. |

**See Also**

- [#setUseCaches(boolean)](URLConnection.md)) 

### guessContentTypeFromName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun guessContentTypeFromName(fname: String!): String!
```

Tries to determine the content type of an object, based on the specified "file" component of a URL. This is a convenience method that can be used by subclasses that override the`getContentType`method.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `fname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a filename. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a guess as to what the content type of the object is, based upon its file name. |

**See Also**

- [java.net.URLConnection#getContentType()](URLConnection.md)) 

### guessContentTypeFromStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun guessContentTypeFromStream(is: InputStream!): String!
```

Tries to determine the type of an input stream based on the characters at the beginning of the input stream. This method can be used by subclasses that override the`getContentType`method.

Ideally, this routine would not be needed. But many`http`servers return the incorrect content type; in addition, there are many nonstandard extensions. Direct inspection of the bytes to determine the content type is often more accurate than believing the content type claimed by the`http`server.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](../java.io/InputStream.md)!:an input stream that supports marks. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a guess at the content type, or`null`if none can be determined. |

| Exceptions ||
|-----------------------|--------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while reading the input stream. |

**See Also**

- [java.io.InputStream#mark(int)](../java.io/InputStream.md))
- [java.io.InputStream#markSupported()](../java.io/InputStream.md))
- [java.net.URLConnection#getContentType()](URLConnection.md)) 

### setAllowUserInteraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAllowUserInteraction(allowuserinteraction: Boolean): Unit
```

Set the value of the`allowUserInteraction`field of this`URLConnection`.

| Parameters ||
|------------------------|---------------------------------------------------------------------------------------------------|
| `allowuserinteraction` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getAllowUserInteraction()> 

### setConnectTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setConnectTimeout(timeout: Int): Unit
```

Sets a specified timeout value, in milliseconds, to be used when opening a communications link to the resource referenced by this URLConnection. If the timeout expires before the connection can be established, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout.

Some non-standard implementation of this method may ignore the specified timeout. To see the connect timeout set, please call getConnectTimeout().

**Warning** : If the hostname resolves to multiple IP addresses, Android's default implementation of [HttpURLConnection](HttpURLConnection.md) will try each in [RFC 3484](http://www.ietf.org/rfc/rfc3484.txt) order. If connecting to each of these addresses fails, multiple timeouts will elapse before the connect attempt throws an exception. Host names that support both IPv6 and IPv4 always have at least 2 IP addresses.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an`int`that specifies the connect timeout value in milliseconds |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if the timeout parameter is negative |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getConnectTimeout()>
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#connect()> 

### setContentHandlerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setContentHandlerFactory(fac: ContentHandlerFactory!): Unit
```

Sets the`ContentHandlerFactory`of an application. It can be called at most once by an application.

The`ContentHandlerFactory`instance is used to construct a content handler from a content type

If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------|
| `fac` | [ContentHandlerFactory](ContentHandlerFactory.md)!:the desired factory. |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.Error` | if the factory has already been defined. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSetFactory`method doesn't allow the operation. |

**See Also**

- [java.net.ContentHandlerFactory](ContentHandlerFactory.md)
- [java.net.URLConnection#getContent()](URLConnection.md))
- [java.lang.SecurityManager#checkSetFactory](../java.lang/SecurityManager.md)) 

### setDefaultAllowUserInteraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefaultAllowUserInteraction(defaultallowuserinteraction: Boolean): Unit
```

Sets the default value of the`allowUserInteraction`field for all future`URLConnection`objects to the specified value.

| Parameters ||
|-------------------------------|---------------------------------------------------------------------------------------------------|
| `defaultallowuserinteraction` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultAllowUserInteraction()> 

### setDefaultRequestProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefaultRequestProperty(
    key: String!, 
    value: String!
): Unit
```

**Deprecated:** *The instance specific setRequestProperty method should be used after an appropriate instance of URLConnection is obtained. Invoking this method will have no effect.*

Sets the default value of a general request property. When a`URLConnection`is created, it is initialized with these properties.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword by which the request is known (e.g., "`Accept`"). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value associated with the key. |

**See Also**

- [java.net.URLConnection#setRequestProperty(java.lang.String,java.lang.String)](URLConnection.md))
- [#getDefaultRequestProperty(java.lang.String)](URLConnection.md)) 

### setDefaultUseCaches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDefaultUseCaches(defaultusecaches: Boolean): Unit
```

Sets the default value of the`useCaches`field to the specified value.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------|
| `defaultusecaches` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultUseCaches()> 

### setDoInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDoInput(doinput: Boolean): Unit
```

Sets the value of the`doInput`field for this`URLConnection`to the specified value.

A URL connection can be used for input and/or output. Set the DoInput flag to true if you intend to use the URL connection for input, false if not. The default is true.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------|
| `doinput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

**See Also**

- [java.net.URLConnection#doInput](URLConnection.md)
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getDoInput()> 

### setDoOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDoOutput(dooutput: Boolean): Unit
```

Sets the value of the`doOutput`field for this`URLConnection`to the specified value.

A URL connection can be used for input and/or output. Set the DoOutput flag to true if you intend to use the URL connection for output, false if not. The default is false.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------|
| `dooutput` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getDoOutput()> 

### setFileNameMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setFileNameMap(map: FileNameMap!): Unit
```

Sets the FileNameMap.

If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `map` | [FileNameMap](FileNameMap.md)!:the FileNameMap to be set |

| Exceptions ||
|-------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSetFactory`method doesn't allow the operation. |

**See Also**

- [java.lang.SecurityManager#checkSetFactory](../java.lang/SecurityManager.md))
- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getFileNameMap()> 

### setIfModifiedSince

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIfModifiedSince(ifmodifiedsince: Long): Unit
```

Sets the value of the`ifModifiedSince`field of this`URLConnection`to the specified value.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------|
| `ifmodifiedsince` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getIfModifiedSince()> 

### setReadTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReadTimeout(timeout: Int): Unit
```

Sets the read timeout to a specified timeout, in milliseconds. A non-zero value specifies the timeout when reading from Input stream when a connection is established to a resource. If the timeout expires before there is data available for read, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout.

Some non-standard implementation of this method ignores the specified timeout. To see the read timeout set, please call getReadTimeout().

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an`int`that specifies the timeout value to be used in milliseconds |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.IllegalArgumentException` | if the timeout parameter is negative |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getReadTimeout()>
- [java.io.InputStream#read()](../java.io/InputStream.md)) 

### setRequestProperty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRequestProperty(
    key: String!, 
    value: String!
): Unit
```

Sets the general request property. If a property with the key already exists, overwrite its value with the new value.

NOTE: HTTP requires all request properties which can legally have multiple instances with the same key to use a comma-separated list syntax which enables multiple properties to be appended into a single property.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword by which the request is known (e.g., "`Accept`"). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value associated with it. |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |
| `java.lang.NullPointerException` | if key is`null` |

**See Also**

- [#getRequestProperty(java.lang.String)](URLConnection.md)) 

### setUseCaches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUseCaches(usecaches: Boolean): Unit
```

Sets the value of the`useCaches`field of this`URLConnection`to the specified value.

Some protocols do caching of documents. Occasionally, it is important to be able to "tunnel through" and ignore the caches (e.g., the "reload" button in a browser). If the UseCaches flag on a connection is true, the connection is allowed to use whatever caches it can. If false, caches are to be ignored. The default value comes from DefaultUseCaches, which defaults to true.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `usecaches` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):a`boolean`indicating whether or not to allow caching |

| Exceptions ||
|-----------------------------------|----------------------|
| `java.lang.IllegalStateException` | if already connected |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/URLConnection#getUseCaches()> 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a`String`representation of this URL connection.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this`URLConnection`. |

## Properties

### allowUserInteraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var allowUserInteraction: Boolean
```

If`true`, this`URL`is being examined in a context in which it makes sense to allow user interactions such as popping up an authentication dialog. If`false`, then no user interaction is allowed.

The value of this field can be set by the`setAllowUserInteraction`method. Its value is returned by the`getAllowUserInteraction`method. Its default value is the value of the argument in the last invocation of the`setDefaultAllowUserInteraction`method. 
**See Also**

- [java.net.URLConnection#getAllowUserInteraction()](URLConnection.md))
- [java.net.URLConnection#setAllowUserInteraction(boolean)](URLConnection.md))
- [java.net.URLConnection#setDefaultAllowUserInteraction(boolean)](URLConnection.md)) 

### connected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var connected: Boolean
```

If`false`, this connection object has not created a communications link to the specified URL. If`true`, the communications link has been established. 

### doInput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var doInput: Boolean
```

This variable is set by the`setDoInput`method. Its value is returned by the`getDoInput`method.

A URL connection can be used for input and/or output. Setting the`doInput`flag to`true`indicates that the application intends to read data from the URL connection.

The default value of this field is`true`. 
**See Also**

- [java.net.URLConnection#getDoInput()](URLConnection.md))
- [java.net.URLConnection#setDoInput(boolean)](URLConnection.md)) 

### doOutput

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var doOutput: Boolean
```

This variable is set by the`setDoOutput`method. Its value is returned by the`getDoOutput`method.

A URL connection can be used for input and/or output. Setting the`doOutput`flag to`true`indicates that the application intends to write data to the URL connection.

The default value of this field is`false`. 
**See Also**

- [java.net.URLConnection#getDoOutput()](URLConnection.md))
- [java.net.URLConnection#setDoOutput(boolean)](URLConnection.md)) 

### ifModifiedSince

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var ifModifiedSince: Long
```

Some protocols support skipping the fetching of the object unless the object has been modified more recently than a certain time.

A nonzero value gives a time as the number of milliseconds since January 1, 1970, GMT. The object is fetched only if it has been modified more recently than that time.

This variable is set by the`setIfModifiedSince`method. Its value is returned by the`getIfModifiedSince`method.

The default value of this field is`0`, indicating that the fetching must always occur. 
**See Also**

- [java.net.URLConnection#getIfModifiedSince()](URLConnection.md))
- [java.net.URLConnection#setIfModifiedSince(long)](URLConnection.md)) 

### url

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var url: URL!
```

The URL represents the remote object on the World Wide Web to which this connection is opened.

The value of this field can be accessed by the`getURL`method.

The default value of this variable is the value of the URL argument in the`URLConnection`constructor. 
**See Also**

- [java.net.URLConnection#getURL()](URLConnection.md))
- [java.net.URLConnection#url](URLConnection.md) 

### useCaches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var useCaches: Boolean
```

If`true`, the protocol is allowed to use caching whenever it can. If`false`, the protocol must always try to get a fresh copy of the object.

This field is set by the`setUseCaches`method. Its value is returned by the`getUseCaches`method.

Its default value is the value given in the last invocation of the`setDefaultUseCaches`method. 
**See Also**

- [java.net.URLConnection#setUseCaches(boolean)](URLConnection.md))
- [java.net.URLConnection#getUseCaches()](URLConnection.md))
- [java.net.URLConnection#setDefaultUseCaches(boolean)](URLConnection.md))

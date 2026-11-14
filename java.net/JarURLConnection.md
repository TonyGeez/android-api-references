# JarURLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JarURLConnection

```
abstract class JarURLConnection : URLConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection) ||
| | ↳ | [java.net.JarURLConnection](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#) |

A URL Connection to a Java ARchive (JAR) file or an entry in a JAR file.

The syntax of a JAR URL is: 

```kotlin
jar:<url>!/{entry}
  
```

for example:

`jar:http://www.foo.com/bar/baz.jar!/COM/foo/Quux.class`

Jar URLs should be used to refer to a JAR file or entries in a JAR file. The example above is a JAR URL which refers to a JAR entry. If the entry name is omitted, the URL refers to the whole JAR file:`jar:http://www.foo.com/bar/baz.jar!/`

Users should cast the generic URLConnection to a JarURLConnection when they know that the URL they created is a JAR URL, and they need JAR-specific functionality. For example: 

```kotlin
URL url = new URL("jar:file:/home/duke/duke.jar!/");
  JarURLConnection jarConnection = (JarURLConnection)url.openConnection();
  Manifest manifest = jarConnection.getManifest();
  
```

JarURLConnection instances can only be used to read from JAR files. It is not possible to get a [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) to modify or write to the underlying JAR file using this class.

Examples:

A Jar entry
: `jar:http://www.foo.com/bar/baz.jar!/COM/foo/Quux.class`

A Jar file
: `jar:http://www.foo.com/bar/baz.jar!/`

A Jar directory
: `jar:http://www.foo.com/bar/baz.jar!/COM/foo/`

`!/`is referred to as the*separator*.

When constructing a JAR url via`new URL(context, spec)`, the following rules apply:

- if there is no context URL and the specification passed to the URL constructor doesn't contain a separator, the URL is considered to refer to a JarFile.
- if there is a context URL, the context URL is assumed to refer to a JAR file or a Jar directory.
- if the specification begins with a '/', the Jar directory is ignored, and the spec is considered to be at the root of the Jar file.Examples:

 context:**jar:http://www.foo.com/bar/jar.jar!/** , spec:**baz/entry.txt**
 : url:**jar:http://www.foo.com/bar/jar.jar!/baz/entry.txt**

 context:**jar:http://www.foo.com/bar/jar.jar!/baz** , spec:**entry.txt**
 : url:**jar:http://www.foo.com/bar/jar.jar!/baz/entry.txt**

 context:**jar:http://www.foo.com/bar/jar.jar!/baz** , spec:**/entry.txt**
 : url:**jar:http://www.foo.com/bar/jar.jar!/entry.txt**

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JarURLConnection](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#JarURLConnection(java.net.URL))`(`url:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL)!`)` Creates the new JarURLConnection to the specified URL. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Attributes](https://developer.android.com/reference/kotlin/java/util/jar/Attributes.html#)! | [getAttributes](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getAttributes())`()` Return the Attributes object for this connection if the URL for it points to a JAR file entry, null otherwise. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!\>! | [getCertificates](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getCertificates())`()` Return the Certificate object for this connection if the URL for it points to a JAR file entry, null otherwise. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEntryName](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getEntryName())`()` Return the entry name for this connection. |
| --- | --- |
| open [JarEntry](https://developer.android.com/reference/kotlin/java/util/jar/JarEntry.html#)! | [getJarEntry](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarEntry())`()` Return the JAR entry object for this connection, if any. |
| abstract [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile.html#)! | [getJarFile](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarFile())`()` Return the JAR file for this connection. |
| open [URL](https://developer.android.com/reference/kotlin/java/net/URL)! | [getJarFileURL](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarFileURL())`()` Returns the URL for the Jar file for this connection. |
| --- | --- |
| open [Attributes](https://developer.android.com/reference/kotlin/java/util/jar/Attributes.html#)! | [getMainAttributes](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getMainAttributes())`()` Returns the main Attributes for the JAR file for this connection. |
| open [Manifest](https://developer.android.com/reference/kotlin/java/util/jar/Manifest.html#)! | [getManifest](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getManifest())`()` Returns the Manifest for this connection, or null if none. |

| Inherited functions ||
|---|---|
| From class [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addRequestProperty](https://developer.android.com/reference/kotlin/java/net/URLConnection#addRequestProperty(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Adds a general request property specified by a key-value pair. This method will not overwrite existing values associated with the same key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/java/net/URLConnection#connect())`()` <br /> Opens a communications link to the resource referenced by this URL, if such a connection has not already been established. If the`connect`method is called when the connection has already been opened (indicated by the`connected`field having the value`true`), the call is ignored. URLConnection objects go through two phases: first they are created, then they are connected. After being created, and before being connected, various options can be specified (e.g., doInput and UseCaches). After connecting, it is an error to try to set them. Operations that depend on being connected, like getContentLength, will implicitly perform the connection, if necessary. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAllowUserInteraction](https://developer.android.com/reference/kotlin/java/net/URLConnection#getAllowUserInteraction())`()` <br /> Returns the value of the`allowUserInteraction`field for this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectTimeout](https://developer.android.com/reference/kotlin/java/net/URLConnection#getConnectTimeout())`()` <br /> Returns setting for connect timeout. 0 return implies that the option is disabled (i.e., timeout of infinity). <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContent](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent())`()` <br /> Retrieves the contents of this URL connection. This method first determines the content type of the object by calling the`getContentType`method. If this is the first time that the application has seen that specific content type, a content handler for that content type is created: 1. If the application has set up a content handler factory instance using the`setContentHandlerFactory`method, the`createContentHandler`method of that instance is called with the content type as an argument; the result is a content handler for that content type. 2. If no content handler factory has yet been set up, or if the factory's`createContentHandler`method returns`null`, then the application loads the class named: ```kotlin sun.net.www.content.<<i>contentType</i>> ``` where \<*contentType* \> is formed by taking the content-type string, replacing all slash characters with a`period`('.'), and all other non-alphanumeric characters with the underscore character '`_`'. The alphanumeric characters are specifically the 26 uppercase ASCII letters '`A`' through '`Z`', the 26 lowercase ASCII letters '`a`' through '`z`', and the 10 ASCII digits '`0`' through '`9`'. If the specified class does not exist, or is not a subclass of`ContentHandler`, then an`UnknownServiceException`is thrown. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getContent](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent(kotlin.Array))`(`classes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!>!`)` <br /> Retrieves the contents of this URL connection. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getContentEncoding](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentEncoding())`()` <br /> Returns the value of the`content-encoding`header field. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getContentLength](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLength())`()` <br /> Returns the value of the`content-length`header field. **Note** : [getContentLengthLong()](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLengthLong())should be preferred over this method, since it returns a`long`instead and is therefore more portable. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getContentLengthLong](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLengthLong())`()` <br /> Returns the value of the`content-length`header field as a long. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getContentType](https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentType())`()` <br /> Returns the value of the`content-type`header field. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDate](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDate())`()` <br /> Returns the value of the`date`header field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDefaultAllowUserInteraction](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultAllowUserInteraction())`()` <br /> Returns the default value of the`allowUserInteraction`field. Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultRequestProperty](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultRequestProperty(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the value of the default request property. Default request properties are set for every connection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDefaultUseCaches](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultUseCaches())`()` <br /> Returns the default value of a`URLConnection`'s`useCaches`flag. Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDoInput](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDoInput())`()` <br /> Returns the value of this`URLConnection`'s`doInput`flag. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDoOutput](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDoOutput())`()` <br /> Returns the value of this`URLConnection`'s`doOutput`flag. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getExpiration](https://developer.android.com/reference/kotlin/java/net/URLConnection#getExpiration())`()` <br /> Returns the value of the`expires`header field. <br /> | | [FileNameMap](https://developer.android.com/reference/kotlin/java/net/FileNameMap)! | [getFileNameMap](https://developer.android.com/reference/kotlin/java/net/URLConnection#getFileNameMap())`()` <br /> Returns a [FileNameMap](https://developer.android.com/reference/kotlin/java/net/FileNameMap) implementation suitable for guessing a content type based on a URL's "file" component. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHeaderField](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderField(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value for the`n`th header field. It returns`null`if there are fewer than`n+1`fields. This method can be used in conjunction with the [getHeaderFieldKey](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldKey(kotlin.Int))method to iterate through all the headers in the message. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHeaderField](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderField(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the value of the named header field. If called on a connection that sets the same header multiple times with possibly different values, only the last value is returned. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getHeaderFieldDate](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldDate(kotlin.String,%20kotlin.Long))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `Default:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Returns the value of the named field parsed as date. The result is the number of milliseconds since January 1, 1970 GMT represented by the named field. This form of`getHeaderField`exists because some connection types (e.g.,`http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeaderFieldInt](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldInt(kotlin.String,%20kotlin.Int))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `Default:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the value of the named field parsed as a number. This form of`getHeaderField`exists because some connection types (e.g.,`http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHeaderFieldKey](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldKey(kotlin.Int))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the key for the`n`th header field. It returns`null`if there are fewer than`n+1`fields. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getHeaderFieldLong](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldLong(kotlin.String,%20kotlin.Long))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `Default:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Returns the value of the named field parsed as a number. This form of`getHeaderField`exists because some connection types (e.g.,`http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | [getHeaderFields](https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFields())`()` <br /> Returns an unmodifiable Map of the header fields. The Map keys are Strings that represent the response-header field names. Each Map value is an unmodifiable List of Strings that represents the corresponding field values. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getIfModifiedSince](https://developer.android.com/reference/kotlin/java/net/URLConnection#getIfModifiedSince())`()` <br /> Returns the value of this object's`ifModifiedSince`field. <br /> | | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getInputStream](https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream())`()` <br /> Returns an input stream that reads from this open connection. A SocketTimeoutException can be thrown when reading from the returned input stream if the read timeout expires before data is available for read. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastModified](https://developer.android.com/reference/kotlin/java/net/URLConnection#getLastModified())`()` <br /> Returns the value of the`last-modified`header field. The result is the number of milliseconds since January 1, 1970 GMT. <br /> | | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getOutputStream](https://developer.android.com/reference/kotlin/java/net/URLConnection#getOutputStream())`()` <br /> Returns an output stream that writes to this connection. <br /> | | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)! | [getPermission](https://developer.android.com/reference/kotlin/java/net/URLConnection#getPermission())`()` <br /> Returns a permission object representing the permission necessary to make the connection represented by this object. This method returns null if no permission is required to make the connection. By default, this method returns`java.security.AllPermission`. Subclasses should override this method and return the permission that best represents the permission required to make a a connection to the URL. For example, a`URLConnection`representing a`file:`URL would return a`java.io.FilePermission`object. The permission returned may dependent upon the state of the connection. For example, the permission before connecting may be different from that after connecting. For example, an HTTP sever, say foo.com, may redirect the connection to a different host, say bar.com. Before connecting the permission returned by the connection will represent the permission needed to connect to foo.com, while the permission returned after connecting will be to bar.com. Permissions are generally used for two purposes: to protect caches of objects obtained through URLConnections, and to check the right of a recipient to learn about a particular URL. In the first case, the permission should be obtained*after* the object has been obtained. For example, in an HTTP connection, this will represent the permission to connect to the host from which the data was ultimately fetched. In the second case, the permission should be obtained and tested*before*connecting. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReadTimeout](https://developer.android.com/reference/kotlin/java/net/URLConnection#getReadTimeout())`()` <br /> Returns setting for read timeout. 0 return implies that the option is disabled (i.e., timeout of infinity). <br /> | | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | [getRequestProperties](https://developer.android.com/reference/kotlin/java/net/URLConnection#getRequestProperties())`()` <br /> Returns an unmodifiable Map of general request properties for this connection. The Map keys are Strings that represent the request-header field names. Each Map value is a unmodifiable List of Strings that represents the corresponding field values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRequestProperty](https://developer.android.com/reference/kotlin/java/net/URLConnection#getRequestProperty(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Returns the value of the named general request property for this connection. <br /> | | [URL](https://developer.android.com/reference/kotlin/java/net/URL)! | [getURL](https://developer.android.com/reference/kotlin/java/net/URLConnection#getURL())`()` <br /> Returns the value of this`URLConnection`'s`URL`field. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getUseCaches](https://developer.android.com/reference/kotlin/java/net/URLConnection#getUseCaches())`()` <br /> Returns the value of this`URLConnection`'s`useCaches`field. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [guessContentTypeFromName](https://developer.android.com/reference/kotlin/java/net/URLConnection#guessContentTypeFromName(kotlin.String))`(`fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Tries to determine the content type of an object, based on the specified "file" component of a URL. This is a convenience method that can be used by subclasses that override the`getContentType`method. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [guessContentTypeFromStream](https://developer.android.com/reference/kotlin/java/net/URLConnection#guessContentTypeFromStream(java.io.InputStream))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` <br /> Tries to determine the type of an input stream based on the characters at the beginning of the input stream. This method can be used by subclasses that override the`getContentType`method. Ideally, this routine would not be needed. But many`http`servers return the incorrect content type; in addition, there are many nonstandard extensions. Direct inspection of the bytes to determine the content type is often more accurate than believing the content type claimed by the`http`server. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAllowUserInteraction](https://developer.android.com/reference/kotlin/java/net/URLConnection#setAllowUserInteraction(kotlin.Boolean))`(`allowuserinteraction:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set the value of the`allowUserInteraction`field of this`URLConnection`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConnectTimeout](https://developer.android.com/reference/kotlin/java/net/URLConnection#setConnectTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets a specified timeout value, in milliseconds, to be used when opening a communications link to the resource referenced by this URLConnection. If the timeout expires before the connection can be established, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout. Some non-standard implementation of this method may ignore the specified timeout. To see the connect timeout set, please call getConnectTimeout(). **Warning** : If the hostname resolves to multiple IP addresses, Android's default implementation of [HttpURLConnection](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection) will try each in [RFC 3484](http://www.ietf.org/rfc/rfc3484.txt) order. If connecting to each of these addresses fails, multiple timeouts will elapse before the connect attempt throws an exception. Host names that support both IPv6 and IPv4 always have at least 2 IP addresses. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLConnection#setContentHandlerFactory(java.net.ContentHandlerFactory))`(`fac:` ` [ContentHandlerFactory](https://developer.android.com/reference/kotlin/java/net/ContentHandlerFactory)!`)` <br /> Sets the`ContentHandlerFactory`of an application. It can be called at most once by an application. The`ContentHandlerFactory`instance is used to construct a content handler from a content type If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultAllowUserInteraction](https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultAllowUserInteraction(kotlin.Boolean))`(`defaultallowuserinteraction:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the default value of the`allowUserInteraction`field for all future`URLConnection`objects to the specified value. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultRequestProperty](https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultRequestProperty(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the default value of a general request property. When a`URLConnection`is created, it is initialized with these properties. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultUseCaches](https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultUseCaches(kotlin.Boolean))`(`defaultusecaches:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the default value of the`useCaches`field to the specified value. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDoInput](https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoInput(kotlin.Boolean))`(`doinput:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the value of the`doInput`field for this`URLConnection`to the specified value. A URL connection can be used for input and/or output. Set the DoInput flag to true if you intend to use the URL connection for input, false if not. The default is true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDoOutput](https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoOutput(kotlin.Boolean))`(`dooutput:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the value of the`doOutput`field for this`URLConnection`to the specified value. A URL connection can be used for input and/or output. Set the DoOutput flag to true if you intend to use the URL connection for output, false if not. The default is false. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFileNameMap](https://developer.android.com/reference/kotlin/java/net/URLConnection#setFileNameMap(java.net.FileNameMap))`(`map:` ` [FileNameMap](https://developer.android.com/reference/kotlin/java/net/FileNameMap)!`)` <br /> Sets the FileNameMap. If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIfModifiedSince](https://developer.android.com/reference/kotlin/java/net/URLConnection#setIfModifiedSince(kotlin.Long))`(`ifmodifiedsince:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the value of the`ifModifiedSince`field of this`URLConnection`to the specified value. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReadTimeout](https://developer.android.com/reference/kotlin/java/net/URLConnection#setReadTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the read timeout to a specified timeout, in milliseconds. A non-zero value specifies the timeout when reading from Input stream when a connection is established to a resource. If the timeout expires before there is data available for read, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout. Some non-standard implementation of this method ignores the specified timeout. To see the read timeout set, please call getReadTimeout(). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRequestProperty](https://developer.android.com/reference/kotlin/java/net/URLConnection#setRequestProperty(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the general request property. If a property with the key already exists, overwrite its value with the new value. NOTE: HTTP requires all request properties which can legally have multiple instances with the same key to use a comma-separated list syntax which enables multiple properties to be appended into a single property. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setUseCaches](https://developer.android.com/reference/kotlin/java/net/URLConnection#setUseCaches(kotlin.Boolean))`(`usecaches:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the value of the`useCaches`field of this`URLConnection`to the specified value. Some protocols do caching of documents. Occasionally, it is important to be able to "tunnel through" and ignore the caches (e.g., the "reload" button in a browser). If the UseCaches flag on a connection is true, the connection is allowed to use whatever caches it can. If false, caches are to be ignored. The default value comes from DefaultUseCaches, which defaults to true. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/net/URLConnection#toString())`()` <br /> Returns a`String`representation of this URL connection. <br /> | ||

| Properties ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection)! | [jarFileURLConnection](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#jarFileURLConnection:java.net.URLConnection) The connection to the JAR file URL, if the connection has been initiated. |

| Inherited properties ||
|---|---|
| From class [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [allowUserInteraction](https://developer.android.com/reference/kotlin/java/net/URLConnection#allowUserInteraction:kotlin.Boolean) <br /> If`true`, this`URL`is being examined in a context in which it makes sense to allow user interactions such as popping up an authentication dialog. If`false`, then no user interaction is allowed. The value of this field can be set by the`setAllowUserInteraction`method. Its value is returned by the`getAllowUserInteraction`method. Its default value is the value of the argument in the last invocation of the`setDefaultAllowUserInteraction`method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connected](https://developer.android.com/reference/kotlin/java/net/URLConnection#connected:kotlin.Boolean) <br /> If`false`, this connection object has not created a communications link to the specified URL. If`true`, the communications link has been established. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [doInput](https://developer.android.com/reference/kotlin/java/net/URLConnection#doInput:kotlin.Boolean) <br /> This variable is set by the`setDoInput`method. Its value is returned by the`getDoInput`method. A URL connection can be used for input and/or output. Setting the`doInput`flag to`true`indicates that the application intends to read data from the URL connection. The default value of this field is`true`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [doOutput](https://developer.android.com/reference/kotlin/java/net/URLConnection#doOutput:kotlin.Boolean) <br /> This variable is set by the`setDoOutput`method. Its value is returned by the`getDoOutput`method. A URL connection can be used for input and/or output. Setting the`doOutput`flag to`true`indicates that the application intends to write data to the URL connection. The default value of this field is`false`. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ifModifiedSince](https://developer.android.com/reference/kotlin/java/net/URLConnection#ifModifiedSince:kotlin.Long) <br /> Some protocols support skipping the fetching of the object unless the object has been modified more recently than a certain time. A nonzero value gives a time as the number of milliseconds since January 1, 1970, GMT. The object is fetched only if it has been modified more recently than that time. This variable is set by the`setIfModifiedSince`method. Its value is returned by the`getIfModifiedSince`method. The default value of this field is`0`, indicating that the fetching must always occur. <br /> | | [URL](https://developer.android.com/reference/kotlin/java/net/URL)! | [url](https://developer.android.com/reference/kotlin/java/net/URLConnection#url:java.net.URL) <br /> The URL represents the remote object on the World Wide Web to which this connection is opened. The value of this field can be accessed by the`getURL`method. The default value of this variable is the value of the URL argument in the`URLConnection`constructor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [useCaches](https://developer.android.com/reference/kotlin/java/net/URLConnection#useCaches:kotlin.Boolean) <br /> If`true`, the protocol is allowed to use caching whenever it can. If`false`, the protocol must always try to get a fresh copy of the object. This field is set by the`setUseCaches`method. Its value is returned by the`getUseCaches`method. Its default value is the value given in the last invocation of the`setDefaultUseCaches`method. <br /> | ||

## Protected constructors

### JarURLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected JarURLConnection(url: URL!)
```

Creates the new JarURLConnection to the specified URL.

| Parameters ||
|-------|-----------------------------------------------------------------------------|
| `url` | [URL](https://developer.android.com/reference/kotlin/java/net/URL)!:the URL |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------|
| `java.net.MalformedURLException` | if no legal protocol could be found in a specification string or the string could not be parsed. |

## Public methods

### getAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAttributes(): Attributes!
```

Return the Attributes object for this connection if the URL for it points to a JAR file entry, null otherwise.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Attributes](https://developer.android.com/reference/kotlin/java/util/jar/Attributes.html#)! | the Attributes object for this connection if the URL for it points to a JAR file entry, null otherwise. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------|
| `java.io.IOException` | if getting the JAR entry causes an IOException to be thrown. |

**See Also**

- [#getJarEntry](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarEntry()) 

### getCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCertificates(): Array<Certificate!>!
```

Return the Certificate object for this connection if the URL for it points to a JAR file entry, null otherwise. This method can only be called once the connection has been completely verified by reading from the input stream until the end of the stream has been reached. Otherwise, this method will return`null`

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#)!>! | the Certificate object for this connection if the URL for it points to a JAR file entry, null otherwise. |

| Exceptions ||
|-----------------------|--------------------------------------------------------------|
| `java.io.IOException` | if getting the JAR entry causes an IOException to be thrown. |

**See Also**

- [#getJarEntry](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarEntry()) 

### getEntryName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntryName(): String!
```

Return the entry name for this connection. This method returns null if the JAR file URL corresponding to this connection points to a JAR file and not a JAR file entry.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the entry name for this connection, if any. |

### getJarEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJarEntry(): JarEntry!
```

Return the JAR entry object for this connection, if any. This method returns null if the JAR file URL corresponding to this connection points to a JAR file and not a JAR file entry.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [JarEntry](https://developer.android.com/reference/kotlin/java/util/jar/JarEntry.html#)! | the JAR entry object for this connection, or null if the JAR URL for this connection points to a JAR file. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | if getting the JAR file for this connection causes an IOException to be thrown. |

**See Also**

- [#getJarFile](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarFile())
- [#getJarEntry](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarEntry()) 

### getJarFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getJarFile(): JarFile!
```

Return the JAR file for this connection.

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [JarFile](https://developer.android.com/reference/kotlin/java/util/jar/JarFile.html#)! | the JAR file for this connection. If the connection is a connection to an entry of a JAR file, the JAR file object is returned |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------------|
| `java.io.IOException` | if an IOException occurs while trying to connect to the JAR file for this connection. |

**See Also**

- [#connect](https://developer.android.com/reference/kotlin/java/net/URLConnection#connect()) 

### getJarFileURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getJarFileURL(): URL!
```

Returns the URL for the Jar file for this connection.

| Return ||
|---------------------------------------------------------------------|-----------------------------------------------|
| [URL](https://developer.android.com/reference/kotlin/java/net/URL)! | the URL for the Jar file for this connection. |

### getMainAttributes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMainAttributes(): Attributes!
```

Returns the main Attributes for the JAR file for this connection.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Attributes](https://developer.android.com/reference/kotlin/java/util/jar/Attributes.html#)! | the main Attributes for the JAR file for this connection. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------|
| `java.io.IOException` | if getting the manifest causes an IOException to be thrown. |

**See Also**

- [#getJarFile](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarFile())
- [#getManifest](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getManifest()) 

### getManifest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getManifest(): Manifest!
```

Returns the Manifest for this connection, or null if none.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Manifest](https://developer.android.com/reference/kotlin/java/util/jar/Manifest.html#)! | the manifest object corresponding to the JAR file object for this connection. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------|
| `java.io.IOException` | if getting the JAR file for this connection causes an IOException to be thrown. |

**See Also**

- [#getJarFile](https://developer.android.com/reference/kotlin/java/net/JarURLConnection#getJarFile())

## Properties

### jarFileURLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var jarFileURLConnection: URLConnection!
```

The connection to the JAR file URL, if the connection has been initiated. This should be set by connect.

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URL

```
class URL : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.URL](URL.md) |

Class `URL` represents a Uniform Resource Locator, a pointer to a "resource" on the World Wide Web. A resource can be something as simple as a file or a directory, or it can be a reference to a more complicated object, such as a query to a database or to a search engine. More information on the types of URLs and their formats can be found at: [*Types of URL*](http://web.archive.org/web/20051219043731/http://archive.ncsa.uiuc.edu/SDG/Software/Mosaic/Demo/url-primer.html)

In general, a URL can be broken into several parts. Consider the following example:

```kotlin
http://www.example.com/docs/resource1.html
  
```

The URL above indicates that the protocol to use is `http` (HyperText Transfer Protocol) and that the information resides on a host machine named `www.example.com`. The information on that host machine is named `/docs/resource1.html`. The exact meaning of this name on the host machine is both protocol dependent and host dependent. The information normally resides in a file, but it could be generated on the fly. This component of the URL is called the *path* component.

A URL can optionally specify a "port", which is the port number to which the TCP connection is made on the remote host machine. If the port is not specified, the default port for the protocol is used instead. For example, the default port for `http` is `80`. An alternative port could be specified as:

```kotlin
http://www.example.com:1080/docs/resource1.html
  
```

The syntax of `URL` is defined by [*RFC 2396: Uniform Resource Identifiers (URI): Generic Syntax*](http://www.ietf.org/rfc/rfc2396.txt), amended by [*RFC 2732: Format for Literal IPv6 Addresses in URLs*](http://www.ietf.org/rfc/rfc2732.txt). The Literal IPv6 address format also supports scope_ids. The syntax and usage of scope_ids is described [here](Inet6Address.md).

A URL may have appended to it a "fragment", also known as a "ref" or a "reference". The fragment is indicated by the sharp sign character "#" followed by more characters. For example,

```kotlin
http://java.sun.com/index.html#chapter1
  
```

This fragment is not technically part of the URL. Rather, it indicates that after the specified resource is retrieved, the application is specifically interested in that part of the document that has the tag `chapter1` attached to it. The meaning of a tag is resource specific.

An application can also specify a "relative URL", which contains only enough information to reach the resource relative to another URL. Relative URLs are frequently used within HTML pages. For example, if the contents of the URL:

```kotlin
http://java.sun.com/index.html
  
```
contained within it the relative URL:

```kotlin
FAQ.html
  
```
it would be a shorthand for:

```kotlin
http://java.sun.com/FAQ.html
  
```

The relative URL need not specify all the components of a URL. If the protocol, host name, or port number is missing, the value is inherited from the fully specified URL. The file component must be specified. The optional fragment is not inherited.

The URL class does not itself encode or decode any URL components according to the escaping mechanism defined in RFC2396. It is the responsibility of the caller to encode any fields, which need to be escaped prior to calling URL, and also to decode any escaped fields, that are returned from URL. Furthermore, because URL has no knowledge of URL escaping, it does not recognise equivalence between the encoded or decoded form of the same URL. For example, the two URLs: 

```kotlin
http://foo.com/hello world/ and http://foo.com/hello%20world
```
would be considered not equal to each other.

Note, the `https://developer.android.com/reference/kotlin/java/net/URI` class does perform escaping of its component fields in certain circumstances. The recommended way to manage the encoding and decoding of URLs is to use `https://developer.android.com/reference/kotlin/java/net/URI`, and to convert between these two classes using `https://developer.android.com/reference/kotlin/java/net/URL#toURI()` and `https://developer.android.com/reference/kotlin/java/net/URI#toURL()`.

The `https://developer.android.com/reference/kotlin/java/net/URLEncoder` and `https://developer.android.com/reference/kotlin/java/net/URLDecoder` classes can also be used, but only for HTML form encoding, which is not the same as the encoding scheme defined in RFC2396.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String)(spec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a `URL` object from the `String` representation. |
| `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)(protocol: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, file: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a `URL` object from the specified `protocol`, `host`, `port` number, and `file`. |
| `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String,%20java.net.URLStreamHandler)(protocol: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, file: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, handler: https://developer.android.com/reference/kotlin/java/net/URLStreamHandler!)` Creates a `URL` object from the specified `protocol`, `host`, `port` number, `file`, and `handler`. |
| `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.String)(protocol: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, host: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, file: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a URL from the specified `protocol` name, `host` name, and `file` name. |
| `https://developer.android.com/reference/kotlin/java/net/URL#URL(java.net.URL,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/java/net/URL#!, spec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a URL by parsing the given spec within a specified context. |
| `https://developer.android.com/reference/kotlin/java/net/URL#URL(java.net.URL,%20kotlin.String,%20java.net.URLStreamHandler)(context: https://developer.android.com/reference/kotlin/java/net/URL#!, spec: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, handler: https://developer.android.com/reference/kotlin/java/net/URLStreamHandler!)` Creates a URL by parsing the given spec with the specified handler within a specified context. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this URL for equality with another object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getAuthority()()` Gets the authority part of this `URL`. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getContent()()` Gets the contents of this URL. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getContent(kotlin.Array)(classes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!>!)` Gets the contents of this URL. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#getDefaultPort()()` Gets the default port number of the protocol associated with this `URL`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getFile()()` Gets the file name of this `URL`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getHost()()` Gets the host name of this `URL`, if applicable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getPath()()` Gets the path part of this `URL`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#getPort()()` Gets the port number of this `URL`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getProtocol()()` Gets the protocol name of this `URL`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getQuery()()` Gets the query part of this `URL`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getRef()()` Gets the anchor (also known as the "reference") of this `URL`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#getUserInfo()()` Gets the userInfo part of this `URL`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#hashCode()()` Creates an integer suitable for hash table indexing. |
| [URLConnection](URLConnection.md)! | `https://developer.android.com/reference/kotlin/java/net/URL#openConnection()()` Returns a `https://developer.android.com/reference/kotlin/java/net/URLConnection` instance that represents a connection to the remote object referred to by the `URL`. |
| --- | --- |
| [URLConnection](URLConnection.md)! | `https://developer.android.com/reference/kotlin/java/net/URL#openConnection(java.net.Proxy)(proxy: https://developer.android.com/reference/kotlin/java/net/Proxy!)` Same as `https://developer.android.com/reference/kotlin/java/net/URL#openConnection()`, except that the connection will be made through the specified proxy; Protocol handlers that do not support proxing will ignore the proxy parameter and make a normal connection. |
| [InputStream](../java.io/InputStream.md)! | `https://developer.android.com/reference/kotlin/java/net/URL#openStream()()` Opens a connection to this `URL` and returns an `InputStream` for reading from that connection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#sameFile(java.net.URL)(other: https://developer.android.com/reference/kotlin/java/net/URL#!)` Compares two URLs, excluding the fragment component. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#setURLStreamHandlerFactory(java.net.URLStreamHandlerFactory)(fac: https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory!)` Sets an application's `URLStreamHandlerFactory`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/URL#toExternalForm()()` Constructs a string representation of this `URL`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/net/URL#toString()()` Constructs a string representation of this `URL`. |
| --- | --- |
| [URI](URI.md)! | `https://developer.android.com/reference/kotlin/java/net/URL#toURI()()` Returns a `https://developer.android.com/reference/kotlin/java/net/URI` equivalent to this URL. |

## Public constructors

### URL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
URL(spec: String!)
```

Creates a `URL` object from the `String` representation.

This constructor is equivalent to a call to the two-argument constructor with a `null` first argument.

| Parameters ||
|---|---|
| `spec` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the `String` to parse as a URL. |

| Exceptions ||
|---|---|
| `java.net.MalformedURLException` | if no protocol is specified, or an unknown protocol is found, or `spec` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(java.net.URL,%20kotlin.String)`

### URL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
URL(
    protocol: String!, 
    host: String!, 
    port: Int, 
    file: String!)
```

Creates a `URL` object from the specified `protocol`, `host`, `port` number, and `file`.

`host` can be expressed as a host name or a literal IP address. If IPv6 literal address is used, it should be enclosed in square brackets (`'['` and `']'`), as specified by [RFC 2732](http://www.ietf.org/rfc/rfc2732.txt); However, the literal IPv6 address format defined in [*RFC 2373: IP Version 6 Addressing Architecture*](http://www.ietf.org/rfc/rfc2373.txt) is also accepted.

Specifying a `port` number of `-1` indicates that the URL should use the default port for the protocol.

If this is the first URL object being created with the specified protocol, a *stream protocol handler* object, an instance of class `URLStreamHandler`, is created for that protocol:

1. If the application has previously set up an instance of `URLStreamHandlerFactory` as the stream handler factory, then the `createURLStreamHandler` method of that instance is called with the protocol string as an argument to create the stream protocol handler.
2. If no `URLStreamHandlerFactory` has yet been set up, or if the factory's `createURLStreamHandler` method returns `null`, then the constructor finds the value of the system property:

   ```kotlin
   java.protocol.handler.pkgs
         
   ```
 If the value of that system property is not `null`, it is interpreted as a list of packages separated by a vertical slash character '`|`'. The constructor tries to load the class named:
| --- | --- |

   ```kotlin
   <<i>package</i>>.<<i>protocol</i>>.Handler
         
   ```
 where \<*package* \> is replaced by the name of the package and \<*protocol* \> is replaced by the name of the protocol. If this class does not exist, or if the class exists but it is not a subclass of `URLStreamHandler`, then the next package in the list is tried.
3. If the previous step fails to find a protocol handler, then the constructor tries to load from a system default package.

   ```kotlin
   <<i>system default package</i>>.<<i>protocol</i>>.Handler
         
   ```
 If this class does not exist, or if the class exists but it is not a subclass of `URLStreamHandler`, then a `MalformedURLException` is thrown.

Protocol handlers for the following protocols are guaranteed to exist on the search path :-

```kotlin
http, https, file, and jar
  
```
Protocol handlers for additional protocols may also be available.

No validation of the inputs is performed by this constructor.

| Parameters ||
|---|---|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the protocol to use. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the host. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port number on the host. |
| --- | --- |
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the file on the host |

| Exceptions ||
|---|---|
| `java.net.MalformedURLException` | if an unknown protocol is specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System.html#getProperty(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URL#setURLStreamHandlerFactory(java.net.URLStreamHandlerFactory)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory#createURLStreamHandler(kotlin.String)`

### URL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
URL(
    protocol: String!, 
    host: String!, 
    port: Int, 
    file: String!, 
    handler: URLStreamHandler!)
```

Creates a `URL` object from the specified `protocol`, `host`, `port` number, `file`, and `handler`. Specifying a `port` number of `-1` indicates that the URL should use the default port for the protocol. Specifying a `handler` of `null` indicates that the URL should use a default stream handler for the protocol, as outlined for: java.net.URL#URL(java.lang.String, java.lang.String, int, java.lang.String)

If the handler is not null and there is a security manager, the security manager's `checkPermission` method is called with a `NetPermission("specifyStreamHandler")` permission. This may result in a SecurityException. No validation of the inputs is performed by this constructor.

| Parameters ||
|---|---|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the protocol to use. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the host. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the port number on the host. |
| --- | --- |
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the file on the host |
| `handler` | [URLStreamHandler](URLStreamHandler.md)!: the stream handler for the URL. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow specifying a stream handler explicitly. |
| `java.net.MalformedURLException` | if an unknown protocol is specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/System.html#getProperty(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URL#setURLStreamHandlerFactory(java.net.URLStreamHandlerFactory)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory#createURLStreamHandler(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/NetPermission`

### URL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
URL(
    protocol: String!, 
    host: String!, 
    file: String!)
```

Creates a URL from the specified `protocol` name, `host` name, and `file` name. The default port for the specified protocol is used.

This method is equivalent to calling the four-argument constructor with the arguments being `protocol`, `host`, `-1`, and `file`. No validation of the inputs is performed by this constructor.

| Parameters ||
|---|---|
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the protocol to use. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the host. |
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the file on the host. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.net.MalformedURLException` | if an unknown protocol is specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`

### URL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
URL(
    context: URL!, 
    spec: String!)
```

Creates a URL by parsing the given spec within a specified context. The new URL is created from the given context URL and the spec argument as described in RFC2396 "Uniform Resource Identifiers : Generic \* Syntax" :

```kotlin
<scheme>://<authority><path>?<query>#<fragment>
  
```
The reference is parsed into the scheme, authority, path, query and fragment parts. If the path component is empty and the scheme, authority, and query components are undefined, then the new URL is a reference to the current document. Otherwise, the fragment and query parts present in the spec are used in the new URL.

<br />

If the scheme component is defined in the given spec and does not match the scheme of the context, then the new URL is created as an absolute URL based on the spec alone. Otherwise the scheme component is inherited from the context URL.

If the authority component is present in the spec then the spec is treated as absolute and the spec authority and path will replace the context authority and path. If the authority component is absent in the spec then the authority of the new URL will be inherited from the context.

If the spec's path component begins with a slash character "/" then the path is treated as absolute and the spec path replaces the context path.

Otherwise, the path is treated as a relative path and is appended to the context path, as described in RFC2396. Also, in this case, the path is canonicalized through the removal of directory changes made by occurrences of ".." and ".".

For a more detailed description of URL parsing, refer to RFC2396.

| Parameters ||
|---|---|
| `context` | [URL](URL.md)!: the context in which to parse the specification. |
| `spec` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the `String` to parse as a URL. |

| Exceptions ||
|---|---|
| `java.net.MalformedURLException` | if no protocol is specified, or an unknown protocol is found, or `spec` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler#parseURL(java.net.URL,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)`

### URL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
URL(
    context: URL!, 
    spec: String!, 
    handler: URLStreamHandler!)
```

Creates a URL by parsing the given spec with the specified handler within a specified context. If the handler is null, the parsing occurs as with the two argument constructor.

| Parameters ||
|---|---|
| `context` | [URL](URL.md)!: the context in which to parse the specification. |
| `spec` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the `String` to parse as a URL. |
| `handler` | [URLStreamHandler](URLStreamHandler.md)!: the stream handler for the URL. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow specifying a stream handler. |
| `java.net.MalformedURLException` | if no protocol is specified, or an unknown protocol is found, or `spec` is `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler#parseURL(java.net.URL,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)`

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares this URL for equality with another object.

If the given object is not a URL then this method immediately returns `false`.

Two URL objects are equal if they have the same protocol, reference equivalent hosts, have the same port number on the host, and the same file and fragment of the file.

Returns true if this URL equals `o`. URLs are equal if they have the same protocol, host, port, file, and reference.

### Network I/O Warning

Some implementations of URL.equals() resolve host names over the network. This is problematic:

- **The network may be slow.** Many classes, including core collections like `https://developer.android.com/reference/kotlin/java/util/Map.html#` and `https://developer.android.com/reference/kotlin/java/util/Set.html#` expect that `equals` and `hashCode` will return quickly. By violating this assumption, this method posed potential performance problems.
- **Equal IP addresses do not imply equal content.** Virtual hosting permits unrelated sites to share an IP address. This method could report two otherwise unrelated URLs to be equal because they're hosted on the same server.
- **The network may not be available.** Two URLs could be equal when a network is available and unequal otherwise.
- **The network may change.** The IP address for a given host name varies by network and over time. This is problematic for mobile devices. Two URLs could be equal on some networks and unequal on others.

This problem is fixed in Android 4.0 (Ice Cream Sandwich). In that release, URLs are only equal if their host names are equal (ignoring case).

| Parameters ||
|---|---|
| `obj` | the URL to compare against. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects are the same; `false` otherwise. |

### getAuthority

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAuthority(): String!
```

Gets the authority part of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the authority part of this `URL` |

### getContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContent(): Any!
```

Gets the contents of this URL. This method is a shorthand for:

```kotlin
openConnection().getContent()
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the contents of this URL. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent()`

### getContent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContent(classes: Array<Class<Any!>!>!): Any!
```

Gets the contents of this URL. This method is a shorthand for:

```kotlin
openConnection().getContent(Class[])
  
```

<br />

| Parameters ||
|---|---|
| `classes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!\>!: an array of Java types |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the content object of this URL that is the first match of the types specified in the classes array. null if none of the requested types are supported. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent(kotlin.Array)`

### getDefaultPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDefaultPort(): Int
```

Gets the default port number of the protocol associated with this `URL`. If the URL scheme or the URLStreamHandler for the URL do not define a default port number, then -1 is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the port number |

### getFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFile(): String!
```

Gets the file name of this `URL`. The returned file portion will be the same as `getPath()`, plus the concatenation of the value of `getQuery()`, if any. If there is no query portion, this method and `getPath()` will return identical results.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the file name of this `URL`, or an empty string if one does not exist |

### getHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getHost(): String!
```

Gets the host name of this `URL`, if applicable. The format of the host conforms to RFC 2732, i.e. for a literal IPv6 address, this method will return the IPv6 address enclosed in square brackets (`'['` and `']'`).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the host name of this `URL`. |

### getPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPath(): String!
```

Gets the path part of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the path part of this `URL`, or an empty string if one does not exist |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPort(): Int
```

Gets the port number of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the port number, or -1 if the port is not set |

### getProtocol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProtocol(): String!
```

Gets the protocol name of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the protocol of this `URL`. |

### getQuery

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQuery(): String!
```

Gets the query part of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the query part of this `URL`, or `null` if one does not exist |

### getRef

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRef(): String!
```

Gets the anchor (also known as the "reference") of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the anchor (also known as the "reference") of this `URL`, or `null` if one does not exist |

### getUserInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUserInfo(): String!
```

Gets the userInfo part of this `URL`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the userInfo part of this `URL`, or `null` if one does not exist |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Creates an integer suitable for hash table indexing.

The hash code is based upon all the URL components relevant for URL comparison. As such, this operation is a blocking operation.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code for this `URL`. |

### openConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openConnection(): URLConnection!
```

Returns a `https://developer.android.com/reference/kotlin/java/net/URLConnection` instance that represents a connection to the remote object referred to by the `URL`.

A new instance of [URLConnection](URLConnection.md) is created every time when invoking the [URLStreamHandler.openConnection(URL)](URLStreamHandler.md)) method of the protocol handler for this URL.

It should be noted that a URLConnection instance does not establish the actual network connection on creation. This will happen only when calling [URLConnection.connect()](URLConnection.md)).

If for the URL's protocol (such as HTTP or JAR), there exists a public, specialized URLConnection subclass belonging to one of the following packages or one of their subpackages: java.lang, java.io, java.util, java.net, the connection returned will be of that subclass. For example, for HTTP an HttpURLConnection will be returned, and for JAR a JarURLConnection will be returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URLConnection!` | a `https://developer.android.com/reference/kotlin/java/net/URLConnection` linking to the URL. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`

### openConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openConnection(proxy: Proxy!): URLConnection!
```

Same as `https://developer.android.com/reference/kotlin/java/net/URL#openConnection()`, except that the connection will be made through the specified proxy; Protocol handlers that do not support proxing will ignore the proxy parameter and make a normal connection. Invoking this method preempts the system's default ProxySelector settings.

| Parameters ||
|---|---|
| `proxy` | [Proxy](Proxy.md)!: the Proxy through which this connection will be made. If direct connection is desired, Proxy.NO_PROXY should be specified. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URLConnection!` | a `URLConnection` to the URL. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs. |
| `java.lang.IllegalArgumentException` | will be thrown if proxy is null, or proxy has the wrong type |
| `java.lang.SecurityException` | if a security manager is present and the caller doesn't have permission to connect to the proxy. |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if the subclass that implements the protocol handler doesn't support this method. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URLConnection`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler#openConnection(java.net.URL,%20java.net.Proxy)`

### openStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openStream(): InputStream!
```

Opens a connection to this `URL` and returns an `InputStream` for reading from that connection. This method is a shorthand for:

```kotlin
openConnection().getInputStream()
  
```

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | an input stream for reading from the URL connection. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O exception occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#openConnection()`
- `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()`

### sameFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sameFile(other: URL!): Boolean
```

Compares two URLs, excluding the fragment component.

Returns `true` if this `URL` and the `other` argument are equal without taking the fragment component into consideration.

| Parameters ||
|---|---|
| `other` | [URL](URL.md)!: the `URL` to compare against. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if they reference the same remote object; `false` otherwise. |

### setURLStreamHandlerFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setURLStreamHandlerFactory(fac: URLStreamHandlerFactory!): Unit
```

Sets an application's `URLStreamHandlerFactory`. This method can be called at most once in a given Java Virtual Machine.

The `URLStreamHandlerFactory` instance is used to construct a stream protocol handler from a protocol name.

If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `fac` | [URLStreamHandlerFactory](URLStreamHandlerFactory.md)!: the desired factory. |

| Exceptions ||
|---|---|
| `java.lang.Error` | if the application has already set a factory. |
| `java.lang.SecurityException` | if a security manager exists and its `checkSetFactory` method doesn't allow the operation. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory`
- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSetFactory()`

### toExternalForm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toExternalForm(): String!
```

Constructs a string representation of this `URL`. The string is created by calling the `toExternalForm` method of the stream protocol handler for this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a string representation of this object. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler#toExternalForm(java.net.URL)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Constructs a string representation of this `URL`. The string is created by calling the `toExternalForm` method of the stream protocol handler for this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this object. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/URL#URL(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/net/URLStreamHandler#toExternalForm(java.net.URL)`

### toURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toURI(): URI!
```

Returns a `https://developer.android.com/reference/kotlin/java/net/URI` equivalent to this URL. This method functions in the same way as `new URI (this.toString())`.

Note, any URL instance that complies with RFC 2396 can be converted to a URI. However, some URLs that are not strictly in compliance can not be converted to a URI.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URI!` | a URI instance equivalent to this URL. |

| Exceptions ||
|---|---|
| `java.net.URISyntaxException` | if this URL is not formatted strictly according to to RFC2396 and cannot be converted to a URI. |

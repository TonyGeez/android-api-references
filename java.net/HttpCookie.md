# HttpCookie

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpCookie

```
class HttpCookie : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.HttpCookie](HttpCookie.md) |

An HttpCookie object represents an HTTP cookie, which carries state information between server and user agent. Cookie is widely adopted to create stateful sessions.

There are 3 HTTP cookie specifications:
Netscape draft 
RFC 2109 - [*http://www.ietf.org/rfc/rfc2109.txt*](http://www.ietf.org/rfc/rfc2109.txt) 
RFC 2965 - [*http://www.ietf.org/rfc/rfc2965.txt*](http://www.ietf.org/rfc/rfc2965.txt)

HttpCookie class can accept all these 3 forms of syntax.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HttpCookie](HttpCookie.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a cookie with a specified name and value. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](HttpCookie.md))`()` Create and return a copy of this object. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [domainMatches](HttpCookie.md))`(`domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` The utility method to check whether a host name is in a domain or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](HttpCookie.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Test the equality of two HTTP cookies. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getComment](HttpCookie.md))`()` Returns the comment describing the purpose of this cookie, or`null`if the cookie has no comment. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCommentURL](HttpCookie.md))`()` Returns the comment URL describing the purpose of this cookie, or`null`if the cookie has no comment URL. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDiscard](HttpCookie.md))`()` Returns the discard attribute of the cookie |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDomain](HttpCookie.md))`()` Returns the domain name set for this cookie. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMaxAge](HttpCookie.md))`()` Returns the maximum age of the cookie, specified in seconds. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](HttpCookie.md))`()` Returns the name of the cookie. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPath](HttpCookie.md))`()` Returns the path on the server to which the browser returns this cookie. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPortlist](HttpCookie.md))`()` Returns the port list attribute of the cookie |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSecure](HttpCookie.md))`()` Returns`true`if sending this cookie should be restricted to a secure protocol, or`false`if the it can be sent using any protocol. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](HttpCookie.md))`()` Returns the value of the cookie. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](HttpCookie.md))`()` Returns the version of the protocol this cookie complies with. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasExpired](HttpCookie.md))`()` Reports whether this HTTP cookie has expired or not. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](HttpCookie.md))`()` Returns the hash code of this HTTP cookie. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHttpOnly](HttpCookie.md))`()` Returns`true`if this cookie contains the*HttpOnly*attribute. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [HttpCookie](HttpCookie.md)!\>! | [parse](HttpCookie.md))`(`header:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs cookies from set-cookie or set-cookie2 header string. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setComment](HttpCookie.md))`(`purpose:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Specifies a comment that describes a cookie's purpose. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCommentURL](HttpCookie.md))`(`purpose:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Specifies a comment URL that describes a cookie's purpose. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDiscard](HttpCookie.md))`(`discard:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specify whether user agent should discard the cookie unconditionally. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDomain](HttpCookie.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Specifies the domain within which this cookie should be presented. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHttpOnly](HttpCookie.md))`(`httpOnly:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the cookie should be considered HTTP Only. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxAge](HttpCookie.md))`(`expiry:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the maximum age of the cookie in seconds. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPath](HttpCookie.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Specifies a path for the cookie to which the client should return the cookie. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPortlist](HttpCookie.md))`(`ports:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Specify the portlist of the cookie, which restricts the port(s) to which a cookie may be sent back in a Cookie header. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSecure](HttpCookie.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Indicates whether the cookie should only be sent using a secure protocol, such as HTTPS or SSL. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValue](HttpCookie.md))`(`newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Assigns a new value to a cookie after the cookie is created. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVersion](HttpCookie.md))`(`v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the version of the cookie protocol this cookie complies with. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](HttpCookie.md))`()` Constructs a cookie header string representation of this cookie, which is in the format defined by corresponding cookie specification, but without the leading "Cookie:" token. |
| --- | --- |

## Public constructors

### HttpCookie

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HttpCookie(
    name: String!, 
    value: String!)
```

Constructs a cookie with a specified name and value.

The name must conform to RFC 2965. That means it can contain only ASCII alphanumeric characters and cannot contain commas, semicolons, or white space or begin with a $ character. The cookie's name cannot be changed after creation.

The value can be anything the server chooses to send. Its value is probably of interest only to the server. The cookie's value can be changed after creation with the`setValue`method.

By default, cookies are created according to the RFC 2965 cookie specification. The version can be changed with the`setVersion`method.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying the name of the cookie |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying the value of the cookie |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the cookie name contains illegal characters |
| `java.lang.NullPointerException` | if`name`is`null` |

**See Also**

- [#setValue](HttpCookie.md))
- [#setVersion](HttpCookie.md))

## Public methods

### clone

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): Any
```

Create and return a copy of this object.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this HTTP cookie |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### domainMatches

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun domainMatches(
    domain: String!, 
    host: String!
): Boolean
```

The utility method to check whether a host name is in a domain or not.

This concept is described in the cookie specification. To understand the concept, some terminologies need to be defined first:
effective host name = hostname if host name contains dot 
or = hostname.local if not

Host A's name domain-matches host B's if:

- their host name strings string-compare equal; or
- A is a HDN string and has the form NB, where N is a non-empty name string, B has the form .B', and B' is a HDN string. (So, x.y.com domain-matches .Y.com but not Y.com.)

A host isn't in a domain (RFC 2965 sec. 3.3.2) if:

- The value for the Domain attribute contains no embedded dots, and the value is not .local.
- The effective host name that derives from the request-host does not domain-match the Domain attribute.
- The request-host is a HDN (not IP address) and has the form HD, where D is the value of the Domain attribute, and H is a string that contains one or more dots.

Examples:

- A Set-Cookie2 from request-host y.x.foo.com for Domain=.foo.com would be rejected, because H is y.x and contains a dot.
- A Set-Cookie2 from request-host x.foo.com for Domain=.foo.com would be accepted.
- A Set-Cookie2 with Domain=.com or Domain=.com., will always be rejected, because there is no embedded dot.
- A Set-Cookie2 from request-host example for Domain=.local will be accepted, because the effective host name for the request- host is example.local, and example.local domain-matches .local.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the domain name to check host name with |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the host name in question |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if they domain-matches;`false`if not |

### equals

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Test the equality of two HTTP cookies.

The result is`true`only if two cookies come from same domain (case-insensitive), have same name (case-insensitive), and have same path (case-sensitive).

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if two HTTP cookies equal to each other; otherwise,`false` |

### getComment

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComment(): String!
```

Returns the comment describing the purpose of this cookie, or`null`if the cookie has no comment.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`containing the comment, or`null`if none |

**See Also**

- [#setComment](HttpCookie.md)) 

### getCommentURL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCommentURL(): String!
```

Returns the comment URL describing the purpose of this cookie, or`null`if the cookie has no comment URL.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`containing the comment URL, or`null`if none |

**See Also**

- [#setCommentURL](HttpCookie.md)) 

### getDiscard

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDiscard(): Boolean
```

Returns the discard attribute of the cookie

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`to represent this cookie's discard attribute |

**See Also**

- [#setDiscard](HttpCookie.md)) 

### getDomain

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomain(): String!
```

Returns the domain name set for this cookie. The form of the domain name is set by RFC 2965.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`containing the domain name |

**See Also**

- [#setDomain](HttpCookie.md)) 

### getMaxAge

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxAge(): Long
```

Returns the maximum age of the cookie, specified in seconds. By default,`-1`indicating the cookie will persist until browser shutdown.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an integer specifying the maximum age of the cookie in seconds |

**See Also**

- [#setMaxAge](HttpCookie.md)) 

### getName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Returns the name of the cookie. The name cannot be changed after creation.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`specifying the cookie's name |

### getPath

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPath(): String!
```

Returns the path on the server to which the browser returns this cookie. The cookie is visible to all subpaths on the server.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`specifying a path that contains a servlet name, for example,*/catalog* |

**See Also**

- [#setPath](HttpCookie.md)) 

### getPortlist

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPortlist(): String!
```

Returns the port list attribute of the cookie

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`contains the port list or`null`if none |

**See Also**

- [#setPortlist](HttpCookie.md)) 

### getSecure

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecure(): Boolean
```

Returns`true`if sending this cookie should be restricted to a secure protocol, or`false`if the it can be sent using any protocol.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if the cookie can be sent over any standard protocol; otherwise,`true` |

**See Also**

- [#setSecure](HttpCookie.md)) 

### getValue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): String!
```

Returns the value of the cookie.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a`String`containing the cookie's present value |

**See Also**

- [#setValue](HttpCookie.md)) 

### getVersion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Returns the version of the protocol this cookie complies with. Version 1 complies with RFC 2965/2109, and version 0 complies with the original cookie specification drafted by Netscape. Cookies provided by a browser use and identify the browser's cookie version.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 if the cookie complies with the original Netscape specification; 1 if the cookie complies with RFC 2965/2109 |

**See Also**

- [#setVersion](HttpCookie.md)) 

### hasExpired

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasExpired(): Boolean
```

Reports whether this HTTP cookie has expired or not.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`to indicate this HTTP cookie has expired; otherwise,`false` |

### hashCode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash code of this HTTP cookie. The result is the sum of hash code value of three significant components of this cookie: name, domain, and path. That is, the hash code is the value of the expression: getName().toLowerCase().hashCode() 
+ getDomain().toLowerCase().hashCode() 
+ getPath().hashCode()

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this HTTP cookie's hash code |

### isHttpOnly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isHttpOnly(): Boolean
```

Returns`true`if this cookie contains the*HttpOnly*attribute. This means that the cookie should not be accessible to scripting engines, like javascript.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this cookie should be considered HTTPOnly |

**See Also**

- [#setHttpOnly(boolean)](HttpCookie.md)) 

### parse

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun parse(header: String!): MutableList<HttpCookie!>!
```

Constructs cookies from set-cookie or set-cookie2 header string. RFC 2965 section 3.2.2 set-cookie2 syntax indicates that one header line may contain more than one cookie definitions, so this is a static utility method instead of another constructor.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `header` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying the set-cookie header. The header should start with "set-cookie", or "set-cookie2" token; or it should have no leading token at all. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [HttpCookie](HttpCookie.md)!>! | a List of cookie parsed from header line string |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if header string violates the cookie specification's syntax or the cookie name contains illegal characters. |
| `java.lang.NullPointerException` | if the header string is`null` |

### setComment

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setComment(purpose: String!): Unit
```

Specifies a comment that describes a cookie's purpose. The comment is useful if the browser presents the cookie to the user. Comments are not supported by Netscape Version 0 cookies.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `purpose` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying the comment to display to the user |

**See Also**

- [#getComment](HttpCookie.md)) 

### setCommentURL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCommentURL(purpose: String!): Unit
```

Specifies a comment URL that describes a cookie's purpose. The comment URL is useful if the browser presents the cookie to the user. Comment URL is RFC 2965 only.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `purpose` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying the comment URL to display to the user |

**See Also**

- [#getCommentURL](HttpCookie.md)) 

### setDiscard

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDiscard(discard: Boolean): Unit
```

Specify whether user agent should discard the cookie unconditionally. This is RFC 2965 only attribute.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `discard` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`indicates to discard cookie unconditionally |

**See Also**

- [#getDiscard](HttpCookie.md)) 

### setDomain

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDomain(pattern: String!): Unit
```

Specifies the domain within which this cookie should be presented.

The form of the domain name is specified by RFC 2965. A domain name begins with a dot (`.foo.com`) and means that the cookie is visible to servers in a specified Domain Name System (DNS) zone (for example,`www.foo.com`, but not`a.b.foo.com`). By default, cookies are only returned to the server that sent them.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`containing the domain name within which this cookie is visible; form is according to RFC 2965 |

**See Also**

- [#getDomain](HttpCookie.md)) 

### setHttpOnly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setHttpOnly(httpOnly: Boolean): Unit
```

Indicates whether the cookie should be considered HTTP Only. If set to`true`it means the cookie should not be accessible to scripting engines like javascript.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `httpOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if`true`make the cookie HTTP only, i.e. only visible as part of an HTTP request. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/HttpCookie#isHttpOnly()> 

### setMaxAge

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMaxAge(expiry: Long): Unit
```

Sets the maximum age of the cookie in seconds.

A positive value indicates that the cookie will expire after that many seconds have passed. Note that the value is the*maximum*age when the cookie will expire, not the cookie's current age.

A negative value means that the cookie is not stored persistently and will be deleted when the Web browser exits. A zero value causes the cookie to be deleted.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `expiry` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):an integer specifying the maximum age of the cookie in seconds; if zero, the cookie should be discarded immediately; otherwise, the cookie's max age is unspecified. |

**See Also**

- [#getMaxAge](HttpCookie.md)) 

### setPath

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPath(uri: String!): Unit
```

Specifies a path for the cookie to which the client should return the cookie.

The cookie is visible to all the pages in the directory you specify, and all the pages in that directory's subdirectories. A cookie's path must include the servlet that set the cookie, for example,*/catalog* , which makes the cookie visible to all directories on the server under*/catalog*.

Consult RFC 2965 (available on the Internet) for more information on setting path names for cookies.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying a path |

**See Also**

- [#getPath](HttpCookie.md)) 

### setPortlist

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPortlist(ports: String!): Unit
```

Specify the portlist of the cookie, which restricts the port(s) to which a cookie may be sent back in a Cookie header.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ports` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specify the port list, which is comma separated series of digits |

**See Also**

- [#getPortlist](HttpCookie.md)) 

### setSecure

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSecure(flag: Boolean): Unit
```

Indicates whether the cookie should only be sent using a secure protocol, such as HTTPS or SSL.

The default value is`false`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`, the cookie can only be sent over a secure protocol like HTTPS. If`false`, it can be sent over any protocol. |

**See Also**

- [#getSecure](HttpCookie.md)) 

### setValue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setValue(newValue: String!): Unit
```

Assigns a new value to a cookie after the cookie is created. If you use a binary value, you may want to use BASE64 encoding.

With Version 0 cookies, values should not contain white space, brackets, parentheses, equals signs, commas, double quotes, slashes, question marks, at signs, colons, and semicolons. Empty values may not behave the same way on all browsers.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`specifying the new value |

**See Also**

- [#getValue](HttpCookie.md)) 

### setVersion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVersion(v: Int): Unit
```

Sets the version of the cookie protocol this cookie complies with. Version 0 complies with the original Netscape cookie specification. Version 1 complies with RFC 2965/2109.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0 if the cookie should comply with the original Netscape specification; 1 if the cookie should comply with RFC 2965/2109 |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if`v`is neither 0 nor 1 |

**See Also**

- [#getVersion](HttpCookie.md)) 

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Constructs a cookie header string representation of this cookie, which is in the format defined by corresponding cookie specification, but without the leading "Cookie:" token.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string form of the cookie. The string has the defined format |

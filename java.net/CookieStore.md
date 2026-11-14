# CookieStore

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CookieStore

```
interface CookieStore
```

| [java.net.CookieStore](CookieStore.md) |

A CookieStore object represents a storage for cookie. Can store and retrieve cookies.

[CookieManager](CookieManager.md) will call`CookieStore.add`to save cookies for every incoming HTTP response, and call`CookieStore.get`to retrieve cookie for every outgoing HTTP request. A CookieStore is responsible for removing HttpCookie instances which have expired.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](CookieStore.md))`(`uri:` ` [URI](URI.md)!`, `cookie:` ` [HttpCookie](HttpCookie.md)!`)` Adds one HTTP cookie to the store. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [HttpCookie](HttpCookie.md)!\>! | [get](CookieStore.md))`(`uri:` ` [URI](URI.md)!`)` Retrieve cookies associated with given URI, or whose domain matches the given URI. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [HttpCookie](HttpCookie.md)!\>! | [getCookies](CookieStore.md))`()` Get all not-expired cookies in cookie store. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [URI](URI.md)!\>! | [getURIs](CookieStore.md))`()` Get all URIs which identify the cookies in this cookie store. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](CookieStore.md))`(`uri:` ` [URI](URI.md)!`, `cookie:` ` [HttpCookie](HttpCookie.md)!`)` Remove a cookie from store. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](CookieStore.md))`()` Remove all cookies in this cookie store. |
| --- | --- |

## Public methods

### add

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(
    uri: URI!, 
    cookie: HttpCookie!
): Unit
```

Adds one HTTP cookie to the store. This is called for every incoming HTTP response.

A cookie to store may or may not be associated with an URI. If it is not associated with an URI, the cookie's domain and path attribute will indicate where it comes from. If it is associated with an URI and its domain and path attribute are not specified, given URI will indicate where this cookie comes from.

If a cookie corresponding to the given URI already exists, then it is replaced with the new one.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](URI.md)!:the uri this cookie associated with. if`null`, this cookie will not be associated with an URI |
| `cookie` | [HttpCookie](HttpCookie.md)!:the cookie to store |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`cookie`is`null` |

**See Also**

- [#get](CookieStore.md)) 

### get

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(uri: URI!): MutableList<HttpCookie!>!
```

Retrieve cookies associated with given URI, or whose domain matches the given URI. Only cookies that have not expired are returned. This is called for every outgoing HTTP request.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](URI.md)!:the uri associated with the cookies to be returned |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [HttpCookie](HttpCookie.md)!>! | an immutable list of HttpCookie, return empty list if no cookies match the given URI |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`uri`is`null` |

**See Also**

- [#add](CookieStore.md)) 

### getCookies

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCookies(): MutableList<HttpCookie!>!
```

Get all not-expired cookies in cookie store.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [HttpCookie](HttpCookie.md)!>! | an immutable list of http cookies; return empty list if there's no http cookie in store |

### getURIs

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getURIs(): MutableList<URI!>!
```

Get all URIs which identify the cookies in this cookie store.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [URI](URI.md)!>! | an immutable list of URIs; return empty list if no cookie in this cookie store is associated with an URI |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(
    uri: URI!, 
    cookie: HttpCookie!
): Boolean
```

Remove a cookie from store.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](URI.md)!:the uri this cookie associated with. if`null`, the cookie to be removed is not associated with an URI when added; if not`null`, the cookie to be removed is associated with the given URI when added. |
| `cookie` | [HttpCookie](HttpCookie.md)!:the cookie to remove |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this store contained the specified cookie |

| Exceptions ||
|----------------------------------|--------------------|
| `java.lang.NullPointerException` | if`cookie`is`null` |

### removeAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeAll(): Boolean
```

Remove all cookies in this cookie store.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this store changed as a result of the call |

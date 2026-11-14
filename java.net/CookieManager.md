# CookieManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CookieManager

```
open class CookieManager : CookieHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.net.CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler) ||
| | ↳ | [java.net.CookieManager](https://developer.android.com/reference/kotlin/java/net/CookieManager#) |

CookieManager provides a concrete implementation of [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler), which separates the storage of cookies from the policy surrounding accepting and rejecting cookies. A CookieManager is initialized with a [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore) which manages storage, and a [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy) object, which makes policy decisions on cookie acceptance/rejection.

The HTTP cookie management in java.net package looks like: 

```kotlin
<code>use
  CookieHandler &lt;------- HttpURLConnection
        ^
        | impl
        |         use
  CookieManager -------&gt; CookiePolicy
              |   use
              |--------&gt; HttpCookie
              |              ^
              |              | use
              |   use        |
              |--------&gt; CookieStore
                             ^
                             | impl
                             |
                   Internal in-memory implementation
  </code>
```

- CookieHandler is at the core of cookie management. User can call CookieHandler.setDefault to set a concrete CookieHanlder implementation to be used.
- CookiePolicy.shouldAccept will be called by CookieManager.put to see whether or not one cookie should be accepted and put into cookie store. User can use any of three pre-defined CookiePolicy, namely ACCEPT_ALL, ACCEPT_NONE and ACCEPT_ORIGINAL_SERVER, or user can define his own CookiePolicy implementation and tell CookieManager to use it.
- CookieStore is the place where any accepted HTTP cookie is stored in. If not specified when created, a CookieManager instance will use an internal in-memory implementation. Or user can implements one and tell CookieManager to use it.
- Currently, only CookieStore.add(URI, HttpCookie) and CookieStore.get(URI) are used by CookieManager. Others are for completeness and might be needed by a more sophisticated CookieStore implementation, e.g. a NetscapeCookieStore.

There're various ways user can hook up his own HTTP cookie management behavior, e.g.

- Use CookieHandler.setDefault to set a brand new [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler) implementation
- Let CookieManager be the default [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler) implementation, but implement user's own [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore) and [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy) and tell default CookieManager to use them: 

  ```kotlin
  // this should be done at the beginning of an HTTP session
          CookieHandler.setDefault(new CookieManager(new MyCookieStore(), new MyCookiePolicy()));
        
  ```
- Let CookieManager be the default [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler) implementation, but use customized [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy): 

  ```kotlin
  // this should be done at the beginning of an HTTP session
          CookieHandler.setDefault(new CookieManager());
          // this can be done at any point of an HTTP session
          ((CookieManager)CookieHandler.getDefault()).setCookiePolicy(new MyCookiePolicy());
        
  ```

The implementation conforms to [RFC 2965](http://www.ietf.org/rfc/rfc2965.txt), section 3.3.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CookieManager](https://developer.android.com/reference/kotlin/java/net/CookieManager#CookieManager())`()` Create a new cookie manager. |
| [CookieManager](https://developer.android.com/reference/kotlin/java/net/CookieManager#CookieManager(java.net.CookieStore,%20java.net.CookiePolicy))`(`store:` ` [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore)!`, `cookiePolicy:` ` [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy)!`)` Create a new cookie manager with specified cookie store and cookie policy. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [get](https://developer.android.com/reference/kotlin/java/net/CookieManager#get(java.net.URI,%20kotlin.collections.MutableMap))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `requestHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` <br /> |
| open [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore)! | [getCookieStore](https://developer.android.com/reference/kotlin/java/net/CookieManager#getCookieStore())`()` To retrieve current cookie store. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/net/CookieManager#put(java.net.URI,%20kotlin.collections.MutableMap))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `responseHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookieManager#setCookiePolicy(java.net.CookiePolicy))`(`cookiePolicy:` ` [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy)!`)` To set the cookie policy of this cookie manager. |

| Inherited functions ||
|---|---|
| From class [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler) |-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler)! | [getDefault](https://developer.android.com/reference/kotlin/java/net/CookieHandler#getDefault())`()` <br /> Gets the system-wide cookie handler. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](https://developer.android.com/reference/kotlin/java/net/CookieHandler#setDefault(java.net.CookieHandler))`(`cHandler:` ` [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler)!`)` <br /> Sets (or unsets) the system-wide cookie handler. Note: non-standard http protocol handlers may ignore this setting. <br /> | ||

## Public constructors

### CookieManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CookieManager()
```

Create a new cookie manager.

This constructor will create new cookie manager with default cookie store and accept policy. The effect is same as`CookieManager(null, null)`. 

### CookieManager

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CookieManager(
    store: CookieStore!, 
    cookiePolicy: CookiePolicy!)
```

Create a new cookie manager with specified cookie store and cookie policy.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `store` | [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore)!:a`CookieStore`to be used by cookie manager. if`null`, cookie manager will use a default one, which is an in-memory CookieStore implementation. |
| `cookiePolicy` | [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy)!:a`CookiePolicy`instance to be used by cookie manager as policy callback. if`null`, ACCEPT_ORIGINAL_SERVER will be used. |

## Public methods

### get

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    uri: URI!, 
    requestHeaders: MutableMap<String!, MutableList<String!>!>!
): MutableMap<String!, MutableList<String!>!>!
```

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:a`URI`representing the intended use for the cookies |
| `requestHeaders` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:- a Map from request header field names to lists of field values representing the current request headers |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | an immutable map from state management headers, with field names "Cookie" or "Cookie2" to a list of cookies containing state information |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if either argument is null |

### getCookieStore

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCookieStore(): CookieStore!
```

To retrieve current cookie store.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [CookieStore](https://developer.android.com/reference/kotlin/java/net/CookieStore)! | the cookie store currently used by cookie manager. |

### put

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(
    uri: URI!, 
    responseHeaders: MutableMap<String!, MutableList<String!>!>!
): Unit
```

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:a`URI`where the cookies come from |
| `responseHeaders` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:an immutable map from field names to lists of field values representing the response header fields returned |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if either argument is null |

### setCookiePolicy

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCookiePolicy(cookiePolicy: CookiePolicy!): Unit
```

To set the cookie policy of this cookie manager.

A instance of`CookieManager`will have cookie policy ACCEPT_ORIGINAL_SERVER by default. Users always can call this method to set another cookie policy.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cookiePolicy` | [CookiePolicy](https://developer.android.com/reference/kotlin/java/net/CookiePolicy)!:the cookie policy. Can be`null`, which has no effects on current cookie policy. |

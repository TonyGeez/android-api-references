Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CookieManager

```
abstract class CookieManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.CookieManager](../android/webkit/CookieManager.md) |

Manages the cookies used by an application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances.

CookieManager represents cookies as strings in the same format as the HTTP `Cookie` and `Set-Cookie` header fields (defined in [RFC6265bis](https://tools.ietf.org/html/draft-ietf-httpbis-rfc6265bis-03)).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#CookieManager()()` <br /> |

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#acceptCookie()()` Gets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances send and accept cookies. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#acceptThirdPartyCookies(android.webkit.WebView)(webview: https://developer.android.com/reference/kotlin/android/webkit/WebView!)` Gets whether the `https://developer.android.com/reference/kotlin/android/webkit/WebView` should allow third party cookies to be set. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#allowFileSchemeCookies()()` Gets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances send and accept cookies for file scheme URLs. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#flush()()` Ensures all cookies currently accessible through the getCookie API are written to persistent storage. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#getCookie(kotlin.String)(url: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets all the cookies for the given URL. |
| open static [CookieManager](../android/webkit/CookieManager.md)! | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#getInstance()()` Gets the singleton CookieManager instance. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#hasCookies()()` Gets whether there are stored cookies. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeAllCookie()()` Removes all cookies. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeAllCookies(android.webkit.ValueCallback)(callback: https://developer.android.com/reference/kotlin/android/webkit/ValueCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>?)` Removes all cookies. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeExpiredCookie()()` Removes all expired cookies. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeSessionCookie()()` Removes all session cookies, which are cookies without an expiration date. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeSessionCookies(android.webkit.ValueCallback)(callback: https://developer.android.com/reference/kotlin/android/webkit/ValueCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>?)` Removes all session cookies, which are cookies without an expiration date. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setAcceptCookie(kotlin.Boolean)(accept: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances should send and accept cookies. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setAcceptFileSchemeCookies(kotlin.Boolean)(accept: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances should send and accept cookies for file scheme URLs. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setAcceptThirdPartyCookies(android.webkit.WebView,%20kotlin.Boolean)(webview: https://developer.android.com/reference/kotlin/android/webkit/WebView!, accept: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the `https://developer.android.com/reference/kotlin/android/webkit/WebView` should allow third party cookies to be set. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setCookie(kotlin.String,%20kotlin.String)(url: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets a single cookie (key-value pair) for the given URL. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setCookie(kotlin.String,%20kotlin.String,%20android.webkit.ValueCallback)(url: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, callback: https://developer.android.com/reference/kotlin/android/webkit/ValueCallback<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html!>?)` Sets a single cookie (key-value pair) for the given URL. |

| Protected methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#clone()()` Creates and returns a copy of this object. |

## Public constructors

### CookieManager

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CookieManager()
```

**Deprecated:** *This class should not be constructed by applications, use `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#getInstance()` instead to fetch the singleton instance.*

## Public methods

### acceptCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun acceptCookie(): Boolean
```

Gets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances send and accept cookies.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances send and accept cookies |

### acceptThirdPartyCookies

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun acceptThirdPartyCookies(webview: WebView!): Boolean
```

Gets whether the `https://developer.android.com/reference/kotlin/android/webkit/WebView` should allow third party cookies to be set.

| Parameters ||
|---|---|
| `webview` | [WebView](../android/webkit/WebView.md)!: the `https://developer.android.com/reference/kotlin/android/webkit/WebView` instance to get the cookie policy for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `https://developer.android.com/reference/kotlin/android/webkit/WebView` accepts third party cookies |

### allowFileSchemeCookies

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun allowFileSchemeCookies(): Boolean
```

Gets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances send and accept cookies for file scheme URLs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances send and accept cookies for file scheme URLs |

### flush

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun flush(): Unit
```

Ensures all cookies currently accessible through the getCookie API are written to persistent storage. This call will block the caller until it is done and may perform I/O.

### getCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCookie(url: String!): String!
```

Gets all the cookies for the given URL. This may return multiple key-value pairs if multiple cookies are associated with this URL, in which case each cookie will be delimited by `"; "` characters (semicolon followed by a space). Each key-value pair will be of the form `"key=value"`.

**Note:** Any cookies set with the `"Partitioned"` attribute will only be returned for the top-level partition of `url`.

| Parameters ||
|---|---|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URL for which the cookies are requested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | value the cookies as a string, using the format of the 'Cookie' HTTP request header |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): CookieManager!
```

Gets the singleton CookieManager instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#!` | the singleton CookieManager instance |

### hasCookies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun hasCookies(): Boolean
```

Gets whether there are stored cookies.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there are stored cookies |

### removeAllCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeAllCookie(): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeAllCookies(android.webkit.ValueCallback)` instead.*

Removes all cookies.

### removeAllCookies

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeAllCookies(callback: ValueCallback<Boolean!>?): Unit
```

Removes all cookies.

This method is asynchronous. If a `https://developer.android.com/reference/kotlin/android/webkit/ValueCallback` is provided, `https://developer.android.com/reference/kotlin/android/webkit/ValueCallback#onReceiveValue(android.webkit.ValueCallback.T)` will be called on the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#` once the operation is complete. The value provided to the callback indicates whether any cookies were removed. You can pass `null` as the callback if you don't need to know when the operation completes or whether any cookies were removed, and in this case it is safe to call the method from a thread without a Looper.

| Parameters ||
|---|---|
| `callback` | [ValueCallback](../android/webkit/ValueCallback.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>?: a callback which is executed when the cookies have been removed. This value may be `null`. |

### removeExpiredCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeExpiredCookie(): Unit
```

**Deprecated:** *The WebView handles removing expired cookies automatically.*

Removes all expired cookies.

### removeSessionCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeSessionCookie(): Unit
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#removeSessionCookies(android.webkit.ValueCallback)` instead.*

Removes all session cookies, which are cookies without an expiration date.

### removeSessionCookies

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeSessionCookies(callback: ValueCallback<Boolean!>?): Unit
```

Removes all session cookies, which are cookies without an expiration date.

This method is asynchronous. If a `https://developer.android.com/reference/kotlin/android/webkit/ValueCallback` is provided, `https://developer.android.com/reference/kotlin/android/webkit/ValueCallback#onReceiveValue(android.webkit.ValueCallback.T)` will be called on the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#` once the operation is complete. The value provided to the callback indicates whether any cookies were removed. You can pass `null` as the callback if you don't need to know when the operation completes or whether any cookie were removed, and in this case it is safe to call the method from a thread without a Looper.

| Parameters ||
|---|---|
| `callback` | [ValueCallback](../android/webkit/ValueCallback.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>?: a callback which is executed when the session cookies have been removed. This value may be `null`. |

### setAcceptCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setAcceptCookie(accept: Boolean): Unit
```

Sets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances should send and accept cookies. By default this is set to `true` and the WebView accepts cookies.

When this is `true` `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setAcceptThirdPartyCookies(android.webkit.WebView,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#setAcceptFileSchemeCookies(kotlin.Boolean)` can be used to control the policy for those specific types of cookie.

| Parameters ||
|---|---|
| `accept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances should send and accept cookies |

### setAcceptFileSchemeCookies

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setAcceptFileSchemeCookies(accept: Boolean): Unit
```

**Deprecated:** *This setting is not secure, please use [androidx.webkit.WebViewAssetLoader](../androidx/webkit/WebViewAssetLoader.md) instead.*

Sets whether the application's `https://developer.android.com/reference/kotlin/android/webkit/WebView` instances should send and accept cookies for file scheme URLs.

Use of cookies with file scheme URLs is potentially insecure and turned off by default. All `file://` URLs share all their cookies, which may lead to leaking private app cookies (ex. any malicious file can access cookies previously set by other (trusted) files).

Loading content via `file://` URLs is generally discouraged. See the note in `https://developer.android.com/reference/kotlin/android/webkit/WebSettings#setAllowFileAccess(kotlin.Boolean)`. Using [androidx.webkit.WebViewAssetLoader](../androidx/webkit/WebViewAssetLoader.md) to load files over `http(s)://` URLs allows the standard web security model to be used for setting and sharing cookies for local files.

Note that calls to this method will have no effect if made after calling other `https://developer.android.com/reference/kotlin/android/webkit/CookieManager#` APIs.

### setAcceptThirdPartyCookies

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setAcceptThirdPartyCookies(
    webview: WebView!, 
    accept: Boolean
): Unit
```

Sets whether the `https://developer.android.com/reference/kotlin/android/webkit/WebView` should allow third party cookies to be set. Allowing third party cookies is a per WebView policy and can be set differently on different WebView instances.

Apps that target `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` or below default to allowing third party cookies. Apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int` or later default to disallowing third party cookies.

| Parameters ||
|---|---|
| `webview` | [WebView](../android/webkit/WebView.md)!: the `https://developer.android.com/reference/kotlin/android/webkit/WebView` instance to set the cookie policy on |
| `accept` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the `https://developer.android.com/reference/kotlin/android/webkit/WebView` instance should accept third party cookies |

### setCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setCookie(
    url: String!, 
    value: String!
): Unit
```

Sets a single cookie (key-value pair) for the given URL. Any existing cookie with the same host, path and name will be replaced with the new cookie. The cookie being set will be ignored if it is expired. To set multiple cookies, your application should invoke this method multiple times.

The `value` parameter must follow the format of the `Set-Cookie` HTTP response header. This is a key-value pair of the form `"key=value"`, optionally followed by a list of cookie attributes delimited with semicolons (ex. `"key=value; Max-Age=123"`). For the header format and attributes supported by WebView, see the [`Set-Cookie` documentation on MDN](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie).

**Notes:**

- If specifying a `value` containing the `"Secure"` attribute, `url` must use the `"https://"` scheme.
- if specifying a `value` containing the `"Partitioned"` attribute, the cookie will be set for the top-level partition of the `url`.

| Parameters ||
|---|---|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URL for which the cookie is to be set |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the cookie as a string, using the format of the 'Set-Cookie' HTTP response header |

### setCookie

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setCookie(
    url: String!, 
    value: String!, 
    callback: ValueCallback<Boolean!>?
): Unit
```

Sets a single cookie (key-value pair) for the given URL. Any existing cookie with the same host, path and name will be replaced with the new cookie. The cookie being set will be ignored if it is expired. To set multiple cookies, your application should invoke this method multiple times.

The `value` parameter must follow the format of the `Set-Cookie` HTTP response header. This is a key-value pair of the form `"key=value"`, optionally followed by a list of cookie attributes delimited with semicolons (ex. `"key=value; Max-Age=123"`). For the header format and attributes supported by WebView, see the [`Set-Cookie` documentation on MDN](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie).

This method is asynchronous. If a `https://developer.android.com/reference/kotlin/android/webkit/ValueCallback` is provided, `https://developer.android.com/reference/kotlin/android/webkit/ValueCallback#onReceiveValue(android.webkit.ValueCallback.T)` will be called on the current thread's `https://developer.android.com/reference/kotlin/android/os/Looper.html#` once the operation is complete. The value provided to the callback indicates whether the cookie was set successfully. You can pass `null` as the callback if you don't need to know when the operation completes or whether it succeeded, and in this case it is safe to call the method from a thread without a Looper.

**Notes:**

- If specifying a `value` containing the `"Secure"` attribute, `url` must use the `"https://"` scheme.
- if specifying a `value` containing the `"Partitioned"` attribute, the cookie will be set for the top-level partition of the `url`.

| Parameters ||
|---|---|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the URL for which the cookie is to be set |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the cookie as a string, using the format of the 'Set-Cookie' HTTP response header |
| `callback` | [ValueCallback](../android/webkit/ValueCallback.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>?: a callback to be executed when the cookie has been set. This value may be `null`. |
| --- | --- |

## Protected methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun clone(): Any!
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

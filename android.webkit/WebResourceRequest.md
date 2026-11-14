# WebResourceRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebResourceRequest

Kotlin| [Java](https://developer.android.com/reference/android/webkit/WebResourceRequest "View this page in Java") 
| --- | --- |

```
interface WebResourceRequest
```

| [android.webkit.WebResourceRequest](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#) |

Encompasses parameters to the android.webkit.WebViewClient#shouldInterceptRequest method.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMethod](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#getMethod())`()` Gets the method associated with the request, for example "GET". |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getRequestHeaders](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#getRequestHeaders())`()` Gets the headers associated with the request. |
| abstract [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getUrl](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#getUrl())`()` Gets the URL for which the resource request was made. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasGesture](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#hasGesture())`()` Gets whether a gesture (such as a click) was associated with the request. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForMainFrame](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#isForMainFrame())`()` Gets whether the request was made in order to fetch the main frame's document. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRedirect](https://developer.android.com/reference/kotlin/android/webkit/WebResourceRequest#isRedirect())`()` Gets whether the request was a result of a server-side redirect. |
| --- | --- |

## Public methods

### getMethod

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMethod(): String!
```

Gets the method associated with the request, for example "GET".

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the method associated with the request. |

### getRequestHeaders

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRequestHeaders(): MutableMap<String!, String!>!
```

Gets the headers associated with the request. These are represented as a mapping of header name to header value.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | the headers associated with the request. |

### getUrl

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUrl(): Uri!
```

Gets the URL for which the resource request was made.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | the URL for which the resource request was made. |

### hasGesture

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasGesture(): Boolean
```

Gets whether a gesture (such as a click) was associated with the request. For security reasons in certain situations this method may return`false`even though the sequence of events which caused the request to be created was initiated by a user gesture.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether a gesture was associated with the request. |

### isForMainFrame

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isForMainFrame(): Boolean
```

Gets whether the request was made in order to fetch the main frame's document.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the request was made for the main frame document. Will be`false`for subresources or iframes, for example. |

### isRedirect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRedirect(): Boolean
```

Gets whether the request was a result of a server-side redirect.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the request was a result of a server-side redirect. |

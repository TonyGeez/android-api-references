# WebResourceResponse

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WebResourceResponse

Kotlin| [Java](WebResourceResponse.md) 
| --- | --- |

```
open class WebResourceResponse
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.WebResourceResponse](WebResourceResponse.md) |

Encapsulates a resource response. Applications can return an instance of this class from android.webkit.WebViewClient#shouldInterceptRequest to provide a custom response when the WebView requests a particular resource.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WebResourceResponse](WebResourceResponse.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `statusCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reasonPhrase:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `responseHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `data:` ` [InputStream](../java.io/InputStream.md)!`)` Constructs a resource response with the given parameters. |
| [WebResourceResponse](WebResourceResponse.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `data:` ` [InputStream](../java.io/InputStream.md)!`)` Constructs a resource response with the given MIME type, character encoding, and input stream. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InputStream](../java.io/InputStream.md)! | [getData](WebResourceResponse.md))`()` Gets the input stream that provides the resource response's data. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEncoding](WebResourceResponse.md))`()` Gets the resource response's encoding. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMimeType](WebResourceResponse.md))`()` Gets the resource response's MIME type. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReasonPhrase](WebResourceResponse.md))`()` Gets the description of the resource response's status code. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getResponseHeaders](WebResourceResponse.md))`()` Gets the headers for the resource response. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStatusCode](WebResourceResponse.md))`()` Gets the resource response's status code. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setData](WebResourceResponse.md))`(`data:` ` [InputStream](../java.io/InputStream.md)!`)` Sets the input stream that provides the resource response's data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEncoding](WebResourceResponse.md))`(`encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the resource response's encoding, for example "UTF-8". |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMimeType](WebResourceResponse.md))`(`mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the resource response's MIME type, for example "text/html". |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResponseHeaders](WebResourceResponse.md))`(`headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the headers for the resource response. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStatusCodeAndReasonPhrase](WebResourceResponse.md))`(`statusCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reasonPhrase:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the resource response's status code and reason phrase. |

## Public constructors

### WebResourceResponse

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebResourceResponse(
    mimeType: String!, 
    encoding: String!, 
    statusCode: Int, 
    reasonPhrase: String, 
    responseHeaders: MutableMap<String!, String!>!, 
    data: InputStream!)
```

Constructs a resource response with the given parameters. Callers must implement[InputStream.read(byte[])](https://developer.android.com/reference/kotlin/java/io/InputStream.html#read(kotlin.ByteArray))for the input stream. java.io.InputStream#close() will be called after the WebView has finished with the response.

**Note:** See [WebResourceResponse(java.lang.String,java.lang.String,java.io.InputStream)](WebResourceResponse.md))for details on what should be specified for`mimeType`and`encoding`.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the resource response's MIME type, for example`"text/html"`. |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the resource response's character encoding, for example`"utf-8"`. |
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the status code needs to be in the ranges \[100, 299\], \[400, 599\]. Causing a redirect by specifying a 3xx code is not supported. |
| --- | --- |
| `reasonPhrase` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the phrase describing the status code, for example "OK". Must be non-empty. This value cannot be`null`. |
| `responseHeaders` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the resource response's headers represented as a mapping of header name -\> header value. |
| `data` | [InputStream](../java.io/InputStream.md)!:the input stream that provides the resource response's data. Must not be a StringBufferInputStream. |
| --- | --- |

### WebResourceResponse

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WebResourceResponse(
    mimeType: String!, 
    encoding: String!, 
    data: InputStream!)
```

Constructs a resource response with the given MIME type, character encoding, and input stream. Callers must implement[InputStream.read(byte[])](https://developer.android.com/reference/kotlin/java/io/InputStream.html#read(kotlin.ByteArray))for the input stream. java.io.InputStream#close() will be called after the WebView has finished with the response.

**Note:** The MIME type and character encoding must be specified as separate parameters (for example`"text/html"`and`"utf-8"`), not a single value like the`"text/html; charset=utf-8"`format used in the HTTP Content-Type header. Do not use the value of a HTTP Content-Encoding header for`encoding`, as that header does not specify a character encoding. Content without a defined character encoding (for example image resources) should pass`null`for`encoding`.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the resource response's MIME type, for example`"text/html"`. |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the resource response's character encoding, for example`"utf-8"`. |
| `data` | [InputStream](../java.io/InputStream.md)!:the input stream that provides the resource response's data. Must not be a StringBufferInputStream. |
| --- | --- |

## Public methods

### getData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getData(): InputStream!
```

Gets the input stream that provides the resource response's data.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [InputStream](../java.io/InputStream.md)! | The input stream that provides the resource response's data |

### getEncoding

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoding(): String!
```

Gets the resource response's encoding.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The resource response's encoding |

### getMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMimeType(): String!
```

Gets the resource response's MIME type.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The resource response's MIME type |

### getReasonPhrase

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReasonPhrase(): String!
```

Gets the description of the resource response's status code.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The description of the resource response's status code. |

### getResponseHeaders

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResponseHeaders(): MutableMap<String!, String!>!
```

Gets the headers for the resource response.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The headers for the resource response. |

### getStatusCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStatusCode(): Int
```

Gets the resource response's status code.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The resource response's status code. |

### setData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setData(data: InputStream!): Unit
```

Sets the input stream that provides the resource response's data. Callers must implement[InputStream.read(byte[])](https://developer.android.com/reference/kotlin/java/io/InputStream.html#read(kotlin.ByteArray)). java.io.InputStream#close() will be called after the WebView has finished with the response.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [InputStream](../java.io/InputStream.md)!:the input stream that provides the resource response's data. Must not be a StringBufferInputStream. |

### setEncoding

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEncoding(encoding: String!): Unit
```

Sets the resource response's encoding, for example "UTF-8". This is used to decode the data from the input stream.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------|
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource response's encoding |

### setMimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMimeType(mimeType: String!): Unit
```

Sets the resource response's MIME type, for example "text/html".

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The resource response's MIME type |

### setResponseHeaders

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setResponseHeaders(headers: MutableMap<String!, String!>!): Unit
```

Sets the headers for the resource response.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Mapping of header name -\> header value. |

### setStatusCodeAndReasonPhrase

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStatusCodeAndReasonPhrase(
    statusCode: Int, 
    reasonPhrase: String
): Unit
```

Sets the resource response's status code and reason phrase.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the status code needs to be in the ranges \[100, 299\], \[400, 599\]. Causing a redirect by specifying a 3xx code is not supported. |
| `reasonPhrase` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the phrase describing the status code, for example "OK". Must be non-empty. This value cannot be`null`. |

# URLUtil

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLUtil

Kotlin| [Java](URLUtil.md) 
| --- | --- |

```
class URLUtil
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.webkit.URLUtil](URLUtil.md) |

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------|---|
| [URLUtil](URLUtil.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [composeSearchUrl](URLUtil.md))`(`inQuery:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `template:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `queryPlaceHolder:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Inserts the`inQuery`in the`template`after URL-encoding it. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [decode](URLUtil.md))`(`url:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [guessFileName](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentDisposition:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Guesses canonical filename that a download would have, using the URL and contentDisposition. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [guessUrl](URLUtil.md))`(`inUrl:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Cleans up (if possible) user-entered web addresses |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAboutUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAssetUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isContentUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCookielessProxyUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDataUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFileUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHttpUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHttpsUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isJavaScriptUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNetworkUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidUrl](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [stripAnchor](URLUtil.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Strips the url of the anchor. |

## Public constructors

### URLUtil

```
URLUtil()
```

## Public methods

### composeSearchUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun composeSearchUrl(
    inQuery: String!, 
    template: String!, 
    queryPlaceHolder: String!
): String!
```

Inserts the`inQuery`in the`template`after URL-encoding it. The encoded query will replace the`queryPlaceHolder`. 

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun decode(url: ByteArray!): ByteArray!
```  

### guessFileName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun guessFileName(
    url: String!, 
    contentDisposition: String?, 
    mimeType: String?
): String!
```

Guesses canonical filename that a download would have, using the URL and contentDisposition.

File extension, if not defined, is added based on the mimetype.

The`contentDisposition`argument will be treated differently depending on targetSdkVersion.

- For targetSDK versions \<`VANILLA_ICE_CREAM`it will be parsed based on RFC 2616.
- For targetSDK versions \>=`VANILLA_ICE_CREAM`it will be parsed based on RFC 6266.

In practice, this means that from`VANILLA_ICE_CREAM`, this method will be able to parse`filename*`directives in the`contentDisposition`string.

The function also changed in the following ways in`VANILLA_ICE_CREAM`:

- If the suggested file type extension doesn't match the passed`mimeType`, the method will append the appropriate extension instead of replacing the current extension.
- If the suggested file name contains a path separator (`"/"`), the method will replace this with the underscore character (`"_"`) instead of splitting the result and only using the last part.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Url to the content |
| `contentDisposition` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Content-Disposition HTTP header or`null` |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Mime-type of the content or`null` |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | suggested filename |

### guessUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun guessUrl(inUrl: String!): String!
```

Cleans up (if possible) user-entered web addresses 

### isAboutUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isAboutUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is an about: url. |

### isAssetUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isAssetUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is an asset file. |

### isContentUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isContentUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is a content: url. |

### isCookielessProxyUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isCookielessProxyUrl(url: String!): Boolean
```

**Deprecated:** *Cookieless proxy is no longer supported.*

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is a proxy url to allow cookieless network requests from a file url. |

### isDataUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isDataUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is a data: url. |

### isFileUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isFileUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is a local file. |

### isHttpUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isHttpUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is an http: url. |

### isHttpsUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isHttpsUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is an https: url. |

### isJavaScriptUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isJavaScriptUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is a javascript: url. |

### isNetworkUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isNetworkUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is a network url. |

### isValidUrl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isValidUrl(url: String!): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the url is valid. |

### stripAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun stripAnchor(url: String!): String!
```

Strips the url of the anchor.

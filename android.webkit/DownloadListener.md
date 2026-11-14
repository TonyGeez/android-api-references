# DownloadListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadListener

Kotlin| [Java](https://developer.android.com/reference/android/webkit/DownloadListener "View this page in Java") 
| --- | --- |

```
interface DownloadListener
```

| [android.webkit.DownloadListener](https://developer.android.com/reference/kotlin/android/webkit/DownloadListener#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDownloadStart](https://developer.android.com/reference/kotlin/android/webkit/DownloadListener#onDownloadStart(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Long))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `userAgent:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentDisposition:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mimetype:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `contentLength:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Notify the host application that a file should be downloaded |

## Public methods

### onDownloadStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDownloadStart(
    url: String!, 
    userAgent: String!, 
    contentDisposition: String!, 
    mimetype: String!, 
    contentLength: Long
): Unit
```

Notify the host application that a file should be downloaded

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The full url to the content that should be downloaded |
| `userAgent` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the user agent to be used for the download. |
| `contentDisposition` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Content-disposition http header, if present. |
| --- | --- |
| `mimetype` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The mimetype of the content reported by the server |
| `contentLength` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The file size reported by the server |

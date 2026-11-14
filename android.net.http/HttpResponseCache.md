# HttpResponseCache

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpResponseCache

Kotlin| [Java](../android/net/http/HttpResponseCache.md) 
| --- | --- |

```
class HttpResponseCache : ResponseCache, Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.ResponseCache](../java/net/ResponseCache.md) ||
| | ↳ | [android.net.http.HttpResponseCache](../android/net/http/HttpResponseCache.md) |

Caches HTTP and HTTPS responses to the filesystem so they may be reused, saving time and bandwidth. This class supports and [javax.net.ssl.HttpsURLConnection](../javax/net/ssl/HttpsURLConnection.md); there is no platform-provided cache for`DefaultHttpClient`or`AndroidHttpClient`. Installation and instances are thread safe.

### Installing an HTTP response cache

Enable caching of all of your application's HTTP requests by installing the cache at application startup. For example, this code installs a 10 MiB cache in the [application-specific](../android/content/Context.md))of the filesystem}: 

```kotlin
<code>protected void onCreate(Bundle savedInstanceState) {
        ...
 
        try {
            File httpCacheDir = new File(context.getCacheDir(), "http");
            long httpCacheSize = 10 * 1024 * 1024; // 10 MiB
            HttpResponseCache.install(httpCacheDir, httpCacheSize);
        } catch (IOException e) {
            Log.i(TAG, "HTTP response cache installation failed:" + e);
        }
    }
 
    protected void onStop() {
        ...
 
        HttpResponseCache cache = HttpResponseCache.getInstalled();
        if (cache != null) {
            cache.flush();
        }
    }</code>
```
This cache will evict entries as necessary to keep its size from exceeding 10 MiB. The best cache size is application specific and depends on the size and frequency of the files being downloaded. Increasing the limit may improve the hit rate, but it may also just waste filesystem space!

<br />

For some applications it may be preferable to create the cache in the external storage directory.**There are no access controls on the external storage directory so it should not be used for caches that could contain private data.** Although it often has more free space, external storage is optional and---even if available---can disappear during use. Retrieve the external cache directory using [android.content.Context#getExternalCacheDir()](../android/content/Context.md)). If this method returns null, your application should fall back to either not caching or caching on non-external storage. If the external storage is removed during use, the cache hit rate will drop to zero and ongoing cache reads will fail.

Flushing the cache forces its data to the filesystem. This ensures that all responses written to the cache will be readable the next time the activity starts.

### Cache Optimization

To measure cache effectiveness, this class tracks three statistics:

- ** [Request Count:](../android/net/http/HttpResponseCache.md))**the number of HTTP requests issued since this cache was created.
- ** [Network Count:](../android/net/http/HttpResponseCache.md))**the number of those requests that required network use.
- ** [Hit Count:](../android/net/http/HttpResponseCache.md))**the number of those requests whose responses were served by the cache.

Sometimes a request will result in a conditional cache hit. If the cache contains a stale copy of the response, the client will issue a conditional`GET`. The server will then send either the updated response if it has changed, or a short 'not modified' response if the client's copy is still valid. Such responses increment both the network count and hit count.

The best way to improve the cache hit rate is by configuring the web server to return cacheable responses. Although this client honors all [HTTP/1.1 (RFC 2068)](http://www.ietf.org/rfc/rfc2616.txt) cache headers, it doesn't cache partial responses.

### Force a Network Response

In some situations, such as after a user clicks a 'refresh' button, it may be necessary to skip the cache, and fetch data directly from the server. To force a full refresh, add the`no-cache`directive: 

```kotlin
<code>connection.addRequestProperty("Cache-Control", "no-cache");
  </code>
```
If it is only necessary to force a cached response to be validated by the server, use the more efficient`max-age=0`instead: 

```kotlin
<code>connection.addRequestProperty("Cache-Control", "max-age=0");
  </code>
```

### Force a Cache Response

Sometimes you'll want to show resources if they are available immediately, but not otherwise. This can be used so your application can show*something* while waiting for the latest data to be downloaded. To restrict a request to locally-cached resources, add the`only-if-cached`directive: 

```kotlin
<code>try {
          connection.addRequestProperty("Cache-Control", "only-if-cached");
          InputStream cached = connection.getInputStream();
          // the resource was cached! show it
      } catch (FileNotFoundException e) {
          // the resource was not cached
      }
  </code>
```
This technique works even better in situations where a stale response is better than no response. To permit stale cached responses, use the`max-stale`directive with the maximum staleness in seconds: 

```kotlin
<code>int maxStale = 60 * 60 * 24 * 28; // tolerate 4-weeks stale
          connection.addRequestProperty("Cache-Control", "max-stale=" + maxStale);
  </code>
```

### Working With Earlier Releases

This class was added in Android 4.0 (Ice Cream Sandwich). Use reflection to enable the response cache without impacting earlier releases: 

```kotlin
<code>try {
            File httpCacheDir = new File(context.getCacheDir(), "http");
            long httpCacheSize = 10 * 1024 * 1024; // 10 MiB
            Class.forName("android.net.http.HttpResponseCache")
                    .getMethod("install", File.class, long.class)
                    .invoke(null, httpCacheDir, httpCacheSize);
        } catch (Exception httpResponseCacheNotAvailable) {
        }</code>
```

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/net/http/HttpResponseCache.md))`()` Uninstalls the cache and releases any active resources. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [delete](../android/net/http/HttpResponseCache.md))`()` Uninstalls the cache and deletes all of its stored contents. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flush](../android/net/http/HttpResponseCache.md))`()` Force buffered operations to the filesystem. |
| --- | --- |
| [CacheResponse](../java/net/CacheResponse.md)! | [get](../android/net/http/HttpResponseCache.md))`(`uri:` ` [URI](../java/net/URI.md)!`, `requestMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `requestHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHitCount](../android/net/http/HttpResponseCache.md))`()` Returns the number of HTTP requests whose response was provided by the cache. |
| static [HttpResponseCache](../android/net/http/HttpResponseCache.md)! | [getInstalled](../android/net/http/HttpResponseCache.md))`()` Returns the currently-installed`HttpResponseCache`, or null if there is no cache installed or it is not a`HttpResponseCache`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkCount](../android/net/http/HttpResponseCache.md))`()` Returns the number of HTTP requests that required the network to either supply a response or validate a locally cached response. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestCount](../android/net/http/HttpResponseCache.md))`()` Returns the total number of HTTP requests that were made. |
| static [HttpResponseCache](../android/net/http/HttpResponseCache.md)! | [install](../android/net/http/HttpResponseCache.md))`(`directory:` ` [File](../java/io/File.md)!`, `maxSize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new HTTP response cache and sets it as the system default cache. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [maxSize](../android/net/http/HttpResponseCache.md))`()` Returns the maximum number of bytes that this cache should use to store its data. |
| [CacheRequest](../java/net/CacheRequest.md)! | [put](../android/net/http/HttpResponseCache.md))`(`uri:` ` [URI](../java/net/URI.md)!`, `urlConnection:` ` [URLConnection](../java/net/URLConnection.md)!`)` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [size](../android/net/http/HttpResponseCache.md))`()` Returns the number of bytes currently being used to store the values in this cache. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ResponseCache](../java/net/ResponseCache.md) |-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ResponseCache](../java/net/ResponseCache.md)! | [getDefault](../java/net/ResponseCache.md))`()` <br /> Gets the system-wide response cache. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](../java/net/ResponseCache.md))`(`responseCache:` ` [ResponseCache](../java/net/ResponseCache.md)!`)` <br /> Sets (or unsets) the system-wide cache. Note: non-standard procotol handlers may ignore this setting. <br /> | ||

## Public methods

### close

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Uninstalls the cache and releases any active resources. Stored contents will remain on the filesystem.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### delete

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun delete(): Unit
```

Uninstalls the cache and deletes all of its stored contents. 

### flush

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flush(): Unit
```

Force buffered operations to the filesystem. This ensures that responses written to the cache will be available the next time the cache is opened, even if this process is killed. 

### get

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(
    uri: URI!, 
    requestMethod: String!, 
    requestHeaders: MutableMap<String!, MutableList<String!>!>!
): CacheResponse!
```

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](../java/net/URI.md)!:a`URI`used to reference the requested network resource |
| `rqstMethod` | a`String`representing the request method |
| `rqstHeaders` | - a Map from request header field names to lists of field values representing the current request headers |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [CacheResponse](../java/net/CacheResponse.md)! | a`CacheResponse`instance if available from cache, or null otherwise |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if any one of the arguments is null |

### getHitCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHitCount(): Int
```

Returns the number of HTTP requests whose response was provided by the cache. This may include conditional`GET`requests that were validated over the network. 

### getInstalled

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstalled(): HttpResponseCache!
```

Returns the currently-installed`HttpResponseCache`, or null if there is no cache installed or it is not a`HttpResponseCache`. 

### getNetworkCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNetworkCount(): Int
```

Returns the number of HTTP requests that required the network to either supply a response or validate a locally cached response. 

### getRequestCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestCount(): Int
```

Returns the total number of HTTP requests that were made. This includes both client requests and requests that were made on the client's behalf to handle a redirects and retries. 

### install

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun install(
    directory: File!, 
    maxSize: Long
): HttpResponseCache!
```

Creates a new HTTP response cache and sets it as the system default cache.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `directory` | [File](../java/io/File.md)!:the directory to hold cache data. |
| `maxSize` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum size of the cache in bytes. |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------|
| [HttpResponseCache](../android/net/http/HttpResponseCache.md)! | the newly-installed cache |

| Exceptions ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if`directory`cannot be used for this cache. Most applications should respond to this exception by logging a warning. |

### maxSize

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun maxSize(): Long
```

Returns the maximum number of bytes that this cache should use to store its data. 

### put

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun put(
    uri: URI!, 
    urlConnection: URLConnection!
): CacheRequest!
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](../java/net/URI.md)!:a`URI`used to reference the requested network resource |
| `conn` | - a URLConnection instance that is used to fetch the response to be cached |

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [CacheRequest](../java/net/CacheRequest.md)! | a`CacheRequest`for recording the response to be cached. Null return indicates that the caller does not intend to cache the response. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if any one of the arguments is null |

### size

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun size(): Long
```

Returns the number of bytes currently being used to store the values in this cache. This may be greater than the [maxSize](../android/net/http/HttpResponseCache.md))if a background deletion is pending.`-1`is returned if the size cannot be determined.

# SSLSessionCache

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionCache

Kotlin| [Java](https://developer.android.com/reference/android/net/SSLSessionCache "View this page in Java") 

```
class SSLSessionCache
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache#) |

File-based cache of established SSL sessions. When re-establishing a connection to the same server, using an SSL session cache can save some time, power, and bandwidth by skipping directly to an encrypted stream. This is a persistent cache which can span executions of the application.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache#SSLSessionCache(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Create a session cache at the default location for this app. |
| [SSLSessionCache](https://developer.android.com/reference/kotlin/android/net/SSLSessionCache#SSLSessionCache(java.io.File))`(`dir:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` Create a session cache using the specified directory. |

## Public constructors

### SSLSessionCache

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSessionCache(context: Context!)
```

Create a session cache at the default location for this app. Multiple instances share data internally.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:for the application |

### SSLSessionCache

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSessionCache(dir: File!)
```

Create a session cache using the specified directory. Individual session entries will be files within the directory. Multiple instances for the same directory share data internally.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `dir` | [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!:to store session files in (created if necessary) |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if the cache can't be opened |

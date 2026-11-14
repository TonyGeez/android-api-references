# SSLSessionCache

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSessionCache

Kotlin| [Java](SSLSessionCache.md) 
| --- | --- |

```
class SSLSessionCache
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.SSLSessionCache](SSLSessionCache.md) |

File-based cache of established SSL sessions. When re-establishing a connection to the same server, using an SSL session cache can save some time, power, and bandwidth by skipping directly to an encrypted stream. This is a persistent cache which can span executions of the application.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLSessionCache](SSLSessionCache.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Create a session cache at the default location for this app. |
| [SSLSessionCache](SSLSessionCache.md))`(`dir:` ` [File](../java.io/File.md)!`)` Create a session cache using the specified directory. |

## Public constructors

### SSLSessionCache

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSessionCache(context: Context!)
```

Create a session cache at the default location for this app. Multiple instances share data internally.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:for the application |

### SSLSessionCache

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLSessionCache(dir: File!)
```

Create a session cache using the specified directory. Individual session entries will be files within the directory. Multiple instances for the same directory share data internally.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `dir` | [File](../java.io/File.md)!:to store session files in (created if necessary) |

| Exceptions ||
|-----------------------|------------------------------|
| `java.io.IOException` | if the cache can't be opened |

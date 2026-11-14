# QuicOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# QuicOptions

Kotlin| [Java](https://developer.android.com/reference/android/net/http/QuicOptions "View this page in Java") 

```
open class QuicOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.http.QuicOptions](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#) |

Configuration options for QUIC.

The settings in this class are only relevant if QUIC is enabled. Use [HttpEngine.Builder.setEnableQuic(boolean)](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine.Builder#setEnableQuic(kotlin.Boolean))to enable / disable QUIC for the HTTP engine.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder) Builder for [QuicOptions](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAllowedQuicHosts](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#getAllowedQuicHosts())`()` See [Builder.addAllowedQuicHost](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#addAllowedQuicHost(kotlin.String)) |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHandshakeUserAgent](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#getHandshakeUserAgent())`()` See [Builder.setHandshakeUserAgent](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setHandshakeUserAgent(kotlin.String)) |
| open [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)? | [getIdleConnectionTimeout](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#getIdleConnectionTimeout())`()` See [Builder.setIdleConnectionTimeout](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setIdleConnectionTimeout(java.time.Duration)) |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInMemoryServerConfigsCacheSize](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#getInMemoryServerConfigsCacheSize())`()` See [Builder.setInMemoryServerConfigsCacheSize](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setInMemoryServerConfigsCacheSize(kotlin.Int)) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasInMemoryServerConfigsCacheSize](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions#hasInMemoryServerConfigsCacheSize())`()` See [Builder.setInMemoryServerConfigsCacheSize](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setInMemoryServerConfigsCacheSize(kotlin.Int)) |

## Public methods

### getAllowedQuicHosts

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getAllowedQuicHosts(): MutableSet<String!>
```

See [Builder.addAllowedQuicHost](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#addAllowedQuicHost(kotlin.String))

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getHandshakeUserAgent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getHandshakeUserAgent(): String?
```

See [Builder.setHandshakeUserAgent](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setHandshakeUserAgent(kotlin.String))

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getIdleConnectionTimeout

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getIdleConnectionTimeout(): Duration?
```

See [Builder.setIdleConnectionTimeout](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setIdleConnectionTimeout(java.time.Duration))

| Return ||
|--------------------------------------------------------------------------------------|--------------------------|
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)? | This value may be`null`. |

### getInMemoryServerConfigsCacheSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getInMemoryServerConfigsCacheSize(): Int
```

See [Builder.setInMemoryServerConfigsCacheSize](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setInMemoryServerConfigsCacheSize(kotlin.Int)) 

### hasInMemoryServerConfigsCacheSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun hasInMemoryServerConfigsCacheSize(): Boolean
```

See [Builder.setInMemoryServerConfigsCacheSize](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions.Builder#setInMemoryServerConfigsCacheSize(kotlin.Int))

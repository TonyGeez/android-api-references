# QuicOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# QuicOptions

Kotlin| [Java](QuicOptions.md) 
| --- | --- |

```
open class QuicOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.QuicOptions](QuicOptions.md) |

Configuration options for QUIC.

The settings in this class are only relevant if QUIC is enabled. Use [HttpEngine.Builder.setEnableQuic(boolean)](../android/net/http/HttpEngine.Builder.md))to enable / disable QUIC for the HTTP engine.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/net/http/QuicOptions.Builder.md) Builder for [QuicOptions](QuicOptions.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getAllowedQuicHosts](QuicOptions.md))`()` See [Builder.addAllowedQuicHost](../android/net/http/QuicOptions.Builder.md)) |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHandshakeUserAgent](QuicOptions.md))`()` See [Builder.setHandshakeUserAgent](../android/net/http/QuicOptions.Builder.md)) |
| open [Duration](../java.time/Duration.md)? | [getIdleConnectionTimeout](QuicOptions.md))`()` See [Builder.setIdleConnectionTimeout](../android/net/http/QuicOptions.Builder.md)) |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInMemoryServerConfigsCacheSize](QuicOptions.md))`()` See [Builder.setInMemoryServerConfigsCacheSize](../android/net/http/QuicOptions.Builder.md)) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasInMemoryServerConfigsCacheSize](QuicOptions.md))`()` See [Builder.setInMemoryServerConfigsCacheSize](../android/net/http/QuicOptions.Builder.md)) |

## Public methods

### getAllowedQuicHosts

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getAllowedQuicHosts(): MutableSet<String!>
```

See [Builder.addAllowedQuicHost](../android/net/http/QuicOptions.Builder.md))

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### getHandshakeUserAgent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getHandshakeUserAgent(): String?
```

See [Builder.setHandshakeUserAgent](../android/net/http/QuicOptions.Builder.md))

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getIdleConnectionTimeout

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getIdleConnectionTimeout(): Duration?
```

See [Builder.setIdleConnectionTimeout](../android/net/http/QuicOptions.Builder.md))

| Return ||
|--------------------------------------------------------------------------------------|--------------------------|
| [Duration](../java.time/Duration.md)? | This value may be`null`. |

### getInMemoryServerConfigsCacheSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun getInMemoryServerConfigsCacheSize(): Int
```

See [Builder.setInMemoryServerConfigsCacheSize](../android/net/http/QuicOptions.Builder.md)) 

### hasInMemoryServerConfigsCacheSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun hasInMemoryServerConfigsCacheSize(): Boolean
```

See [Builder.setInMemoryServerConfigsCacheSize](../android/net/http/QuicOptions.Builder.md))

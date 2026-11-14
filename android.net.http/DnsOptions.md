Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# DnsOptions

Kotlin | [Java](../android/net/http/DnsOptions.md)
| --- | --- |

```
class DnsOptions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.DnsOptions](../android/net/http/DnsOptions.md) |

A class configuring the host resolution functionality. Note that while we refer to `DNS` as the most common mechanism being used for brevity, settings apply to other means of resolving hostnames like hosts file resolution.

Hostnames can be resolved in two ways - either by using the system resolver (using `getaddrinfo` provided by system libraries), or by using a custom resolver which is tailored for the HTTP networking stack.

The built-in stack provides several advantages over using the global system resolver:

- It has been tailored to the needs of the HTTP networking stack, particularly speed and stability.
- `getaddrinfo` is a blocking call which requires dedicating worker threads and makes cancellation impossible (we need to abandon the thread until the call completes)
- The `getaddrinfo` interface gives no insight into the root cause of failures
- `struct addrinfo` provides no TTL (Time To Live) of the returned addresses. This restricts flexibility of handling caching (e.g. allowing the use of stale DNS records) and requires us to either rely on OS DNS caches, or be extremely conservative with the TTL.

Most configuration in this class is only applicable if the built-in DNS resolver is used.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder` Builder for `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#`. |
| | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.StaleDnsOptions` A class configuring the stale DNS functionality. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_DISABLED:kotlin.Int` Option is disabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_ENABLED:kotlin.Int` Option is enabled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_UNSPECIFIED:kotlin.Int` Option is unspecified, platform default value will be used. |
| --- | --- |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#getPersistHostCache()()` See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setPersistHostCache(kotlin.Int)` |
| [Duration](../java/time/Duration.md)? | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#getPersistHostCachePeriod()()` See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setPersistHostCachePeriod(java.time.Duration)` |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#getPreestablishConnectionsToStaleDnsResults()()` See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setPreestablishConnectionsToStaleDnsResults(kotlin.Int)` |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#getStaleDns()()` See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setStaleDns(kotlin.Int)` |
| [DnsOptions.StaleDnsOptions](../android/net/http/DnsOptions.StaleDnsOptions.md)? | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#getStaleDnsOptions()()` See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setStaleDnsOptions(android.net.http.DnsOptions.StaleDnsOptions)` |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#getUseHttpStackDnsResolver()()` See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setUseHttpStackDnsResolver(kotlin.Int)` |
| --- | --- |

## Constants

### DNS_OPTION_DISABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DNS_OPTION_DISABLED: Int
```

Option is disabled.

 Value: 2

### DNS_OPTION_ENABLED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DNS_OPTION_ENABLED: Int
```

Option is enabled.

 Value: 1

### DNS_OPTION_UNSPECIFIED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val DNS_OPTION_UNSPECIFIED: Int
```

Option is unspecified, platform default value will be used.

 Value: 0

## Public methods

### getPersistHostCache

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPersistHostCache(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setPersistHostCache(kotlin.Int)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_DISABLED:kotlin.Int` |

### getPersistHostCachePeriod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPersistHostCachePeriod(): Duration?
```

See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setPersistHostCachePeriod(java.time.Duration)`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#?` | This value may be `null`. |

### getPreestablishConnectionsToStaleDnsResults

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getPreestablishConnectionsToStaleDnsResults(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setPreestablishConnectionsToStaleDnsResults(kotlin.Int)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_DISABLED:kotlin.Int` |

### getStaleDns

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getStaleDns(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setStaleDns(kotlin.Int)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_DISABLED:kotlin.Int` |

### getStaleDnsOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getStaleDnsOptions(): DnsOptions.StaleDnsOptions?
```

See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setStaleDnsOptions(android.net.http.DnsOptions.StaleDnsOptions)`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.StaleDnsOptions?` | This value may be `null`. |

### getUseHttpStackDnsResolver

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
fun getUseHttpStackDnsResolver(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions.Builder#setUseHttpStackDnsResolver(kotlin.Int)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/DnsOptions#DNS_OPTION_DISABLED:kotlin.Int` |

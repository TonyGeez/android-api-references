# DnsResolver

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DnsResolver

Kotlin| [Java](DnsResolver.md) 
| --- | --- |

```
class DnsResolver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.DnsResolver](DnsResolver.md) |

Dns resolver class for asynchronous dns querying Note that if a client sends a query with more than 1 record in the question section but the remote dns server does not support this, it may not respond at all, leading to a timeout.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/net/DnsResolver.Callback.md) Base interface for answer callbacks |
| | [DnsException](../android/net/DnsResolver.DnsException.md) Class to represent DNS error |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLASS_IN](DnsResolver.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PARSE](DnsResolver.md) Indicates that there was an error parsing the response the query. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SYSTEM](DnsResolver.md) Indicates that there was an error sending the query. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_EMPTY](DnsResolver.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_NO_CACHE_LOOKUP](DnsResolver.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_NO_CACHE_STORE](DnsResolver.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_NO_RETRY](DnsResolver.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_A](DnsResolver.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_AAAA](DnsResolver.md) <br /> |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DnsResolver](DnsResolver.md) | [getInstance](DnsResolver.md))`()` Get instance for DnsResolver |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [query](DnsResolver.md))`(`network:` ` [Network](Network.md)?`, `domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `nsType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `callback:` ` [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)<in` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](../java.net/InetAddress.md)!>!>`)` Send a DNS query with the specified name and query type, get back a set of InetAddresses with rfc6724 sorting style asynchronously. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [query](DnsResolver.md))`(`network:` ` [Network](Network.md)?`, `domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `callback:` ` [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)<in` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](../java.net/InetAddress.md)!>!>`)` Send a DNS query with the specified name on a network with both IPv4 and IPv6, get back a set of InetAddresses with rfc6724 sorting style asynchronously. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rawQuery](DnsResolver.md))`(`network:` ` [Network](Network.md)?`, `query:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `callback:` ` [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)<in` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>`)` Send a raw DNS query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rawQuery](DnsResolver.md))`(`network:` ` [Network](Network.md)?`, `domain:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `nsClass:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nsType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java.util.concurrent/Executor.md)`, `cancellationSignal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`, `callback:` ` [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)<in` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>`)` Send a DNS query with the specified name, class and query type. |

## Constants

### CLASS_IN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLASS_IN: Int
```  

 Value: 1

### ERROR_PARSE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PARSE: Int
```

Indicates that there was an error parsing the response the query. The cause of this error is available via getCause() and is a [ParseException](ParseException.md). 

 Value: 0

### ERROR_SYSTEM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SYSTEM: Int
```

Indicates that there was an error sending the query. The cause of this error is available via getCause() and is an ErrnoException. 

 Value: 1

### FLAG_EMPTY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_EMPTY: Int
```  

 Value: 0

### FLAG_NO_CACHE_LOOKUP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_NO_CACHE_LOOKUP: Int
```  

 Value: 4

### FLAG_NO_CACHE_STORE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_NO_CACHE_STORE: Int
```  

 Value: 2

### FLAG_NO_RETRY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_NO_RETRY: Int
```  

 Value: 1

### TYPE_A

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_A: Int
```  

 Value: 1

### TYPE_AAAA

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_AAAA: Int
```  

 Value: 28

## Public methods

### getInstance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): DnsResolver
```

Get instance for DnsResolver

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [DnsResolver](DnsResolver.md) | This value cannot be`null`. |

### query

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    network: Network?, 
    domain: String, 
    nsType: Int, 
    flags: Int, 
    executor: Executor, 
    cancellationSignal: CancellationSignal?, 
    callback: DnsResolver.Callback<in MutableList<InetAddress!>!>
): Unit
```

Send a DNS query with the specified name and query type, get back a set of InetAddresses with rfc6724 sorting style asynchronously. The answer will be provided asynchronously through the provided [Callback](../android/net/DnsResolver.Callback.md).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](Network.md)?: [Network](Network.md) specifying which network to query on.`null`for query on default network. |
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):domain name to query This value cannot be`null`. |
| `nsType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):dns resource record (RR) type as one of the TYPE_\* constants Value is [android.net.DnsResolver#TYPE_A](DnsResolver.md), or [android.net.DnsResolver#TYPE_AAAA](DnsResolver.md) |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags as a combination of the FLAGS_\* constants Value is [android.net.DnsResolver#FLAG_EMPTY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_RETRY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_CACHE_STORE](DnsResolver.md), or [android.net.DnsResolver#FLAG_NO_CACHE_LOOKUP](DnsResolver.md) |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) that the callback should be executed on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:used by the caller to signal if the query should be cancelled. May be`null`. |
| --- | --- |
| `callback` | [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)\<in [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](../java.net/InetAddress.md)!\>!\>:a [Callback](../android/net/DnsResolver.Callback.md) which will be called to notify the caller of the result of dns query. This value cannot be`null`. |

### query

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun query(
    network: Network?, 
    domain: String, 
    flags: Int, 
    executor: Executor, 
    cancellationSignal: CancellationSignal?, 
    callback: DnsResolver.Callback<in MutableList<InetAddress!>!>
): Unit
```

Send a DNS query with the specified name on a network with both IPv4 and IPv6, get back a set of InetAddresses with rfc6724 sorting style asynchronously. This method will examine the connection ability on given network, and query IPv4 and IPv6 if connection is available. If at least one query succeeded with valid answer, rcode will be 0 The answer will be provided asynchronously through the provided [Callback](../android/net/DnsResolver.Callback.md).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](Network.md)?: [Network](Network.md) specifying which network to query on.`null`for query on default network. |
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):domain name to query This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags as a combination of the FLAGS_\* constants Value is [android.net.DnsResolver#FLAG_EMPTY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_RETRY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_CACHE_STORE](DnsResolver.md), or [android.net.DnsResolver#FLAG_NO_CACHE_LOOKUP](DnsResolver.md) |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) that the callback should be executed on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:used by the caller to signal if the query should be cancelled. May be`null`. |
| `callback` | [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)\<in [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](../java.net/InetAddress.md)!\>!\>:a [Callback](../android/net/DnsResolver.Callback.md) which will be called to notify the caller of the result of dns query. This value cannot be`null`. |
| --- | --- |

### rawQuery

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rawQuery(
    network: Network?, 
    query: ByteArray, 
    flags: Int, 
    executor: Executor, 
    cancellationSignal: CancellationSignal?, 
    callback: DnsResolver.Callback<in ByteArray!>
): Unit
```

Send a raw DNS query. The answer will be provided asynchronously through the provided [Callback](../android/net/DnsResolver.Callback.md).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](Network.md)?: [Network](Network.md) specifying which network to query on.`null`for query on default network. |
| `query` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):blob message to query This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags as a combination of the FLAGS_\* constants Value is [android.net.DnsResolver#FLAG_EMPTY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_RETRY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_CACHE_STORE](DnsResolver.md), or [android.net.DnsResolver#FLAG_NO_CACHE_LOOKUP](DnsResolver.md) |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) that the callback should be executed on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:used by the caller to signal if the query should be cancelled. May be`null`. |
| `callback` | [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)\<in [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>:a [Callback](../android/net/DnsResolver.Callback.md) which will be called to notify the caller of the result of dns query. This value cannot be`null`. |
| --- | --- |

### rawQuery

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rawQuery(
    network: Network?, 
    domain: String, 
    nsClass: Int, 
    nsType: Int, 
    flags: Int, 
    executor: Executor, 
    cancellationSignal: CancellationSignal?, 
    callback: DnsResolver.Callback<in ByteArray!>
): Unit
```

Send a DNS query with the specified name, class and query type. The answer will be provided asynchronously through the provided [Callback](../android/net/DnsResolver.Callback.md).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](Network.md)?: [Network](Network.md) specifying which network to query on.`null`for query on default network. |
| `domain` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):domain name to query This value cannot be`null`. |
| `nsClass` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):dns class as one of the CLASS_\* constants Value is [android.net.DnsResolver#CLASS_IN](DnsResolver.md) |
| --- | --- |
| `nsType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):dns resource record (RR) type as one of the TYPE_\* constants Value is [android.net.DnsResolver#TYPE_A](DnsResolver.md), or [android.net.DnsResolver#TYPE_AAAA](DnsResolver.md) |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags as a combination of the FLAGS_\* constants Value is [android.net.DnsResolver#FLAG_EMPTY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_RETRY](DnsResolver.md), [android.net.DnsResolver#FLAG_NO_CACHE_STORE](DnsResolver.md), or [android.net.DnsResolver#FLAG_NO_CACHE_LOOKUP](DnsResolver.md) |
| `executor` | [Executor](../java.util.concurrent/Executor.md):The [Executor](../java.util.concurrent/Executor.md) that the callback should be executed on. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java.util.concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android.content/Context.md)). Otherwise, provide an [Executor](../java.util.concurrent/Executor.md) that dispatches to an appropriate thread. |
| --- | --- |
| `cancellationSignal` | [CancellationSignal](../android.os/CancellationSignal.md)?:used by the caller to signal if the query should be cancelled. May be`null`. |
| `callback` | [DnsResolver.Callback](../android/net/DnsResolver.Callback.md)\<in [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>:a [Callback](../android/net/DnsResolver.Callback.md) which will be called to notify the caller of the result of dns query. This value cannot be`null`. |

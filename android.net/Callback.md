Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin | [Java](../android/net/DnsResolver.Callback.md)
| --- | --- |

```
interface Callback<T : Any!>
```

| [android.net.DnsResolver.Callback](../android/net/DnsResolver.Callback.md) |

Base interface for answer callbacks

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/DnsResolver.Callback#onAnswer(android.net.DnsResolver.Callback.T,%20kotlin.Int)(answer: T, rcode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Success response to android. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/DnsResolver.Callback#onError(android.net.DnsResolver.DnsException)(error: https://developer.android.com/reference/kotlin/android/net/DnsResolver.DnsException)` Error response to android. |

## Public methods

### onAnswer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onAnswer(
    answer: T, 
    rcode: Int
): Unit
```

Success response to android.net.DnsResolver#query or android.net.DnsResolver#rawQuery. Invoked when the answer to a query was successfully parsed.

| Parameters ||
|---|---|
| `answer` | T: answer to the query. This value cannot be `null`. |
| `rcode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The response code in the DNS response. |

**See Also**

### onError

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onError(error: DnsResolver.DnsException): Unit
```

Error response to android.net.DnsResolver#query or android.net.DnsResolver#rawQuery. Invoked when there is no valid answer to android.net.DnsResolver#query android.net.DnsResolver#rawQuery.

| Parameters ||
|---|---|
| `error` | [DnsResolver.DnsException](../android/net/DnsResolver.DnsException.md): a `https://developer.android.com/reference/kotlin/android/net/DnsResolver.DnsException` object with additional detail regarding the failure. This value cannot be `null`. |

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InetAddresses

Kotlin | [Java](https://developer.android.com/reference/android/net/InetAddresses "View this page in Java")
| --- | --- |

```
open class InetAddresses
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.InetAddresses](https://developer.android.com/reference/kotlin/android/net/InetAddresses#) |

Utility methods for `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#` implementations.

## Summary

| Public methods ||
|---|---|
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/InetAddresses#isNumericAddress(kotlin.String)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Checks to see if the `address` is a numeric address (such as `"192.0.2.1"` or `"2001:db8::1:2"`). |
| open static [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) | `https://developer.android.com/reference/kotlin/android/net/InetAddresses#parseNumericAddress(kotlin.String)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns an InetAddress corresponding to the given numeric address (such as `"192.168.0.1"` or `"2001:4860:800d::68"`). |

## Public methods

### isNumericAddress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isNumericAddress(address: String): Boolean
```

Checks to see if the `address` is a numeric address (such as `"192.0.2.1"` or `"2001:db8::1:2"`).

A numeric address is either an IPv4 address containing exactly 4 decimal numbers or an IPv6 numeric address. IPv4 addresses that consist of either hexadecimal or octal digits or do not have exactly 4 numbers are not treated as numeric.

This method will never do a DNS lookup.

| Parameters ||
|---|---|
| `address` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the address to parse. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the supplied address is numeric, false otherwise. |

### parseNumericAddress

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun parseNumericAddress(address: String): InetAddress
```

Returns an InetAddress corresponding to the given numeric address (such as `"192.168.0.1"` or `"2001:4860:800d::68"`).

See `https://developer.android.com/reference/kotlin/android/net/InetAddresses#isNumericAddress(kotlin.String)` (String)} for a definition as to what constitutes a numeric address.

This method will never do a DNS lookup.

| Parameters ||
|---|---|
| `address` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the address to parse, must be numeric. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#` | an `https://developer.android.com/reference/kotlin/java/net/InetAddress.html#` instance corresponding to the address. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `address` is not a numeric address. |

# Formatter

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Formatter

Kotlin| [Java](https://developer.android.com/reference/android/text/format/Formatter "View this page in Java") 

```
class Formatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.format.Formatter](https://developer.android.com/reference/kotlin/android/text/format/Formatter#) |

Utility class to aid in formatting common values that are not covered by the [java.util.Formatter](https://developer.android.com/reference/kotlin/java/util/Formatter.html#) class in [java.util](https://developer.android.com/reference/kotlin/java/util/package-summary.html)

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [Formatter](https://developer.android.com/reference/kotlin/android/text/format/Formatter#Formatter())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatFileSize](https://developer.android.com/reference/kotlin/android/text/format/Formatter#formatFileSize(android.content.Context,%20kotlin.Long))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?`, `sizeBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Formats a content size to be in the form of bytes, kilobytes, megabytes, etc. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatIpAddress](https://developer.android.com/reference/kotlin/android/text/format/Formatter#formatIpAddress(kotlin.Int))`(`ipv4Address:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a string in the canonical IPv4 format ###. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [formatShortFileSize](https://developer.android.com/reference/kotlin/android/text/format/Formatter#formatShortFileSize(android.content.Context,%20kotlin.Long))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?`, `sizeBytes:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Like [formatFileSize](https://developer.android.com/reference/kotlin/android/text/format/Formatter#formatFileSize(android.content.Context,%20kotlin.Long)), but trying to generate shorter numbers (showing fewer digits of precision). |

## Public constructors

### Formatter

```
Formatter()
```

## Public methods

### formatFileSize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun formatFileSize(
    context: Context?, 
    sizeBytes: Long
): String!
```

Formats a content size to be in the form of bytes, kilobytes, megabytes, etc.

As of O, the prefixes are used in their standard meanings in the SI system, so kB = 1000 bytes, MB = 1,000,000 bytes, etc.

In [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) and earlier, powers of 1024 are used instead, with KB = 1024 bytes, MB = 1,048,576 bytes, etc.

If the context has a right-to-left locale, the returned string is wrapped in bidi formatting characters to make sure it's displayed correctly if inserted inside a right-to-left string. (This is useful in cases where the unit strings, like "MB", are left-to-right, but the locale is right-to-left.)

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?:Context to use to load the localized units This value may be`null`. |
| `sizeBytes` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):size value to be formatted, in bytes |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | formatted string with the number |

### formatIpAddress

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun formatIpAddress(ipv4Address: Int): String!
```

**Deprecated:** *Use [java.net.InetAddress#getHostAddress()](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getHostAddress()), which supports both IPv4 and IPv6 addresses. This method does not support IPv6 addresses.*

Returns a string in the canonical IPv4 format ###.###.###.### from a packed integer containing the IP address. The IPv4 address is expected to be in little-endian format (LSB first). That is, 0x01020304 will return "4.3.2.1". 

### formatShortFileSize

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun formatShortFileSize(
    context: Context?, 
    sizeBytes: Long
): String!
```

Like [formatFileSize](https://developer.android.com/reference/kotlin/android/text/format/Formatter#formatFileSize(android.content.Context,%20kotlin.Long)), but trying to generate shorter numbers (showing fewer digits of precision).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)?:This value may be`null`. |

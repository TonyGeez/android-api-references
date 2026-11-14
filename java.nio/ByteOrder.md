# ByteOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ByteOrder

```
class ByteOrder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#) |

A typesafe enumeration for byte orders.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#)! | [nativeOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#nativeOrder())`()` Retrieves the native byte order of the underlying platform. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#toString())`()` Constructs a string describing this object. |

| Properties ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#)! | [BIG_ENDIAN](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder) Constant denoting big-endian byte order. |
| static [ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#)! | [LITTLE_ENDIAN](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#LITTLE_ENDIAN:java.nio.ByteOrder) Constant denoting little-endian byte order. |

## Public methods

### nativeOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun nativeOrder(): ByteOrder!
```

Retrieves the native byte order of the underlying platform.

This method is defined so that performance-sensitive Java code can allocate direct buffers with the same byte order as the hardware. Native code libraries are often more efficient when such buffers are used.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ByteOrder](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#)! | The native byte order of the hardware upon which this Java virtual machine is running |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Constructs a string describing this object.

This method returns the string`"BIG_ENDIAN"`for [BIG_ENDIAN](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#BIG_ENDIAN:java.nio.ByteOrder) and`"LITTLE_ENDIAN"`for [LITTLE_ENDIAN](https://developer.android.com/reference/kotlin/java/nio/ByteOrder#LITTLE_ENDIAN:java.nio.ByteOrder).

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The specified string |

## Properties

### BIG_ENDIAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIG_ENDIAN: ByteOrder!
```

Constant denoting big-endian byte order. In this order, the bytes of a multibyte value are ordered from most significant to least significant. 

### LITTLE_ENDIAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LITTLE_ENDIAN: ByteOrder!
```

Constant denoting little-endian byte order. In this order, the bytes of a multibyte value are ordered from least significant to most significant.

# ByteOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ByteOrder

```
class ByteOrder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.ByteOrder](ByteOrder.md) |

A typesafe enumeration for byte orders.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ByteOrder](ByteOrder.md)! | [nativeOrder](ByteOrder.md))`()` Retrieves the native byte order of the underlying platform. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ByteOrder.md))`()` Constructs a string describing this object. |

| Properties ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ByteOrder](ByteOrder.md)! | [BIG_ENDIAN](ByteOrder.md) Constant denoting big-endian byte order. |
| static [ByteOrder](ByteOrder.md)! | [LITTLE_ENDIAN](ByteOrder.md) Constant denoting little-endian byte order. |

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
| [ByteOrder](ByteOrder.md)! | The native byte order of the hardware upon which this Java virtual machine is running |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Constructs a string describing this object.

This method returns the string`"BIG_ENDIAN"`for [BIG_ENDIAN](ByteOrder.md) and`"LITTLE_ENDIAN"`for [LITTLE_ENDIAN](ByteOrder.md).

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

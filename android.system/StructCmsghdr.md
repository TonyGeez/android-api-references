# StructCmsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructCmsghdr

Kotlin| [Java](StructCmsghdr.md) 
| --- | --- |

```
class StructCmsghdr
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.StructCmsghdr](StructCmsghdr.md) |

Corresponds to C's`struct cmsghdr`.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructCmsghdr](StructCmsghdr.md))`(`cmsg_level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cmsg_type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> |
| [StructCmsghdr](StructCmsghdr.md))`(`cmsg_level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cmsg_type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [cmsg_data](StructCmsghdr.md) message data sent/received |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [cmsg_level](StructCmsghdr.md) Originating protocol |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [cmsg_type](StructCmsghdr.md) Protocol-specific type |
| --- | --- |

## Public constructors

### StructCmsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructCmsghdr(
    cmsg_level: Int, 
    cmsg_type: Int, 
    value: ByteArray)
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `value` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):This value cannot be`null`. |

### StructCmsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructCmsghdr(
    cmsg_level: Int, 
    cmsg_type: Int, 
    value: Short)
```

## Properties

### cmsg_data

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val cmsg_data: ByteArray
```

message data sent/received 

### cmsg_level

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val cmsg_level: Int
```

Originating protocol 

### cmsg_type

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val cmsg_type: Int
```

Protocol-specific type

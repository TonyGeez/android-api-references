# StructCmsghdr

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructCmsghdr

Kotlin| [Java](https://developer.android.com/reference/android/system/StructCmsghdr "View this page in Java") 
| --- | --- |

```
class StructCmsghdr
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.StructCmsghdr](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr#) |

Corresponds to C's`struct cmsghdr`.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructCmsghdr](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr#StructCmsghdr(kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray))`(`cmsg_level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cmsg_type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` <br /> |
| [StructCmsghdr](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr#StructCmsghdr(kotlin.Int,%20kotlin.Int,%20kotlin.Short))`(`cmsg_level:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cmsg_type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [cmsg_data](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr#cmsg_data:kotlin.ByteArray) message data sent/received |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [cmsg_level](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr#cmsg_level:kotlin.Int) Originating protocol |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [cmsg_type](https://developer.android.com/reference/kotlin/android/system/StructCmsghdr#cmsg_type:kotlin.Int) Protocol-specific type |
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

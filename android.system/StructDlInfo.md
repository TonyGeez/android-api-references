# StructDlInfo

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructDlInfo

Kotlin| [Java](https://developer.android.com/reference/android/system/StructDlInfo "View this page in Java") 

```
class StructDlInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.system.StructDlInfo](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#) |

Corresponds to C's`struct Dl_info`.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructDlInfo](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#StructDlInfo(kotlin.String,%20kotlin.Long,%20kotlin.String,%20kotlin.Long))`(`dli_fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dli_fbase:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `dli_sname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dli_saddr:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#toString())`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [dli_fbase](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#dli_fbase:kotlin.Long) Base address at which shared object is loaded |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dli_fname](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#dli_fname:kotlin.String) Pathname of shared object that contains address |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [dli_saddr](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#dli_saddr:kotlin.Long) Exact address of symbol named in dli_sname |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dli_sname](https://developer.android.com/reference/kotlin/android/system/StructDlInfo#dli_sname:kotlin.String) Name of symbol whose definition overlaps addr |

## Public constructors

### StructDlInfo

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructDlInfo(
    dli_fname: String!, 
    dli_fbase: Long, 
    dli_sname: String!, 
    dli_saddr: Long)
```

## Public methods

### toString

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### dli_fbase

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val dli_fbase: Long
```

Base address at which shared object is loaded 

### dli_fname

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val dli_fname: String!
```

Pathname of shared object that contains address 

### dli_saddr

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val dli_saddr: Long
```

Exact address of symbol named in dli_sname 

### dli_sname

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val dli_sname: String!
```

Name of symbol whose definition overlaps addr

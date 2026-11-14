# StructDlInfo

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructDlInfo

Kotlin| [Java](StructDlInfo.md) 
| --- | --- |

```
class StructDlInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.StructDlInfo](StructDlInfo.md) |

Corresponds to C's`struct Dl_info`.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructDlInfo](StructDlInfo.md))`(`dli_fname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dli_fbase:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `dli_sname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dli_saddr:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](StructDlInfo.md))`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [dli_fbase](StructDlInfo.md) Base address at which shared object is loaded |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dli_fname](StructDlInfo.md) Pathname of shared object that contains address |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [dli_saddr](StructDlInfo.md) Exact address of symbol named in dli_sname |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [dli_sname](StructDlInfo.md) Name of symbol whose definition overlaps addr |

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

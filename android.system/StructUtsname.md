# StructUtsname

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructUtsname

Kotlin| [Java](https://developer.android.com/reference/android/system/StructUtsname "View this page in Java") 

```
class StructUtsname
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.system.StructUtsname](https://developer.android.com/reference/kotlin/android/system/StructUtsname#) |

Information returned by [Os.uname](https://developer.android.com/reference/kotlin/android/system/Os#uname()). Corresponds to C's`struct utsname`from`<sys/utsname.h>`.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructUtsname](https://developer.android.com/reference/kotlin/android/system/StructUtsname#StructUtsname(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`sysname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `nodename:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `release:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `version:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `machine:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance with the given field values. |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/system/StructUtsname#toString())`()` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [machine](https://developer.android.com/reference/kotlin/android/system/StructUtsname#machine:kotlin.String) The machine architecture, such as "aarch64", "riscv64" or "x86_64". |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [nodename](https://developer.android.com/reference/kotlin/android/system/StructUtsname#nodename:kotlin.String) The machine's unqualified name on some implementation-defined network. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [release](https://developer.android.com/reference/kotlin/android/system/StructUtsname#release:kotlin.String) The OS release, such as "2. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [sysname](https://developer.android.com/reference/kotlin/android/system/StructUtsname#sysname:kotlin.String) The OS name, such as "Linux". |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [version](https://developer.android.com/reference/kotlin/android/system/StructUtsname#version:kotlin.String) The OS version, such as "#48-Ubuntu SMP Tue Feb 22 20:25:29 UTC 2011" or "#1 SMP PREEMPT 2025-07-09T19:15:06Z". |

## Public constructors

### StructUtsname

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructUtsname(
    sysname: String!, 
    nodename: String!, 
    release: String!, 
    version: String!, 
    machine: String!)
```

Constructs an instance with the given field values.

## Public methods

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### machine

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val machine: String!
```

The machine architecture, such as "aarch64", "riscv64" or "x86_64". 

### nodename

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val nodename: String!
```

The machine's unqualified name on some implementation-defined network. 

### release

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val release: String!
```

The OS release, such as "2.6.35-27-generic" or "6.16.0-rc4-mainline-gefd77156c8e3-4k". 

### sysname

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val sysname: String!
```

The OS name, such as "Linux". 

### version

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val version: String!
```

The OS version, such as "#48-Ubuntu SMP Tue Feb 22 20:25:29 UTC 2011" or "#1 SMP PREEMPT 2025-07-09T19:15:06Z".

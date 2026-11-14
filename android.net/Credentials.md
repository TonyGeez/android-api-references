# Credentials

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Credentials

Kotlin| [Java](https://developer.android.com/reference/android/net/Credentials "View this page in Java") 

```
open class Credentials
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.Credentials](https://developer.android.com/reference/kotlin/android/net/Credentials#) |

A class for representing UNIX credentials passed via ancillary data on UNIX domain sockets. See "man 7 unix" on a desktop linux distro.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Credentials](https://developer.android.com/reference/kotlin/android/net/Credentials#Credentials(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`pid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `gid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGid](https://developer.android.com/reference/kotlin/android/net/Credentials#getGid())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPid](https://developer.android.com/reference/kotlin/android/net/Credentials#getPid())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUid](https://developer.android.com/reference/kotlin/android/net/Credentials#getUid())`()` <br /> |

## Public constructors

### Credentials

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Credentials(
    pid: Int, 
    uid: Int, 
    gid: Int)
```

## Public methods

### getGid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGid(): Int
```  

### getPid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPid(): Int
```  

### getUid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUid(): Int
```

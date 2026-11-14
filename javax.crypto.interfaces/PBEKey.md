# PBEKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PBEKey

```
interface PBEKey : SecretKey
```

| [javax.crypto.interfaces.PBEKey](PBEKey.md) |

The interface to a PBE key.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](PBEKey.md) The class fingerprint that is set to indicate serialization compatibility since J2SE 1. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIterationCount](PBEKey.md))`()` Returns the iteration count or 0 if not specified. |
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getPassword](PBEKey.md))`()` Returns the password. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSalt](PBEKey.md))`()` Returns the salt or null if not specified. |
| --- | --- |

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

The class fingerprint that is set to indicate serialization compatibility since J2SE 1.4. 

 Value: -1430015993304333921L

## Public methods

### getIterationCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIterationCount(): Int
```

Returns the iteration count or 0 if not specified.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the iteration count. |

### getPassword

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPassword(): CharArray!
```

Returns the password.

Note: this method should return a copy of the password. It is the caller's responsibility to zero out the password information after it is no longer needed.

| Return ||
|------------------------------------------------------------------------------------------|---------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | the password. |

### getSalt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSalt(): ByteArray!
```

Returns the salt or null if not specified.

Note: this method should return a copy of the salt. It is the caller's responsibility to zero out the salt information after it is no longer needed.

| Return ||
|------------------------------------------------------------------------------------------|-----------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the salt. |

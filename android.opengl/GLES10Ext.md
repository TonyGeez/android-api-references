# GLES10Ext

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLES10Ext

Kotlin| [Java](GLES10Ext.md) 
| --- | --- |

```
open class GLES10Ext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.GLES10Ext](GLES10Ext.md) |

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------|---|
| [GLES10Ext](GLES10Ext.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glQueryMatrixxOES](GLES10Ext.md))`(`mantissa:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `mantissaOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exponent:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `exponentOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glQueryMatrixxOES](GLES10Ext.md))`(`mantissa:` ` [IntBuffer](../java.nio/IntBuffer.md)!`, `exponent:` ` [IntBuffer](../java.nio/IntBuffer.md)!`)` <br /> |

## Public constructors

### GLES10Ext

```
GLES10Ext()
```

## Public methods

### glQueryMatrixxOES

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun glQueryMatrixxOES(
    mantissa: IntArray!, 
    mantissaOffset: Int, 
    exponent: IntArray!, 
    exponentOffset: Int
): Int
```  

### glQueryMatrixxOES

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun glQueryMatrixxOES(
    mantissa: IntBuffer!, 
    exponent: IntBuffer!
): Int
```

# GLES10Ext

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLES10Ext

Kotlin| [Java](https://developer.android.com/reference/android/opengl/GLES10Ext "View this page in Java") 
| --- | --- |

```
open class GLES10Ext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.opengl.GLES10Ext](https://developer.android.com/reference/kotlin/android/opengl/GLES10Ext#) |

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------|---|
| [GLES10Ext](https://developer.android.com/reference/kotlin/android/opengl/GLES10Ext#GLES10Ext())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glQueryMatrixxOES](https://developer.android.com/reference/kotlin/android/opengl/GLES10Ext#glQueryMatrixxOES(kotlin.IntArray,%20kotlin.Int,%20kotlin.IntArray,%20kotlin.Int))`(`mantissa:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `mantissaOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exponent:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `exponentOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glQueryMatrixxOES](https://developer.android.com/reference/kotlin/android/opengl/GLES10Ext#glQueryMatrixxOES(java.nio.IntBuffer,%20java.nio.IntBuffer))`(`mantissa:` ` [IntBuffer](https://developer.android.com/reference/kotlin/java/nio/IntBuffer.html#)!`, `exponent:` ` [IntBuffer](https://developer.android.com/reference/kotlin/java/nio/IntBuffer.html#)!`)` <br /> |

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

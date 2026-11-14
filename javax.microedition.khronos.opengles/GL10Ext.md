# GL10Ext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GL10Ext

```
interface GL10Ext : GL
```

| [javax.microedition.khronos.opengles.GL10Ext](../javax/microedition/khronos/opengles/GL10Ext.md) |

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glQueryMatrixxOES](../javax/microedition/khronos/opengles/GL10Ext.md))`(`mantissa:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `mantissaOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `exponent:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `exponentOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [glQueryMatrixxOES](../javax/microedition/khronos/opengles/GL10Ext.md))`(`mantissa:` ` [IntBuffer](../java/nio/IntBuffer.md)!`, `exponent:` ` [IntBuffer](../java/nio/IntBuffer.md)!`)` <br /> |

## Public methods

### glQueryMatrixxOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glQueryMatrixxOES(
    mantissa: IntArray!, 
    mantissaOffset: Int, 
    exponent: IntArray!, 
    exponentOffset: Int
): Int
```  

### glQueryMatrixxOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glQueryMatrixxOES(
    mantissa: IntBuffer!, 
    exponent: IntBuffer!
): Int
```

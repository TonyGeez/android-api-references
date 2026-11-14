# GL11Ext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GL11Ext

```
interface GL11Ext : GL
```

| [javax.microedition.khronos.opengles.GL11Ext](../javax/microedition/khronos/opengles/GL11Ext.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_INDEX_ARRAY_BUFFER_BINDING_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_INDEX_ARRAY_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_INDEX_ARRAY_POINTER_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_INDEX_ARRAY_SIZE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_INDEX_ARRAY_STRIDE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_INDEX_ARRAY_TYPE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MATRIX_PALETTE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MAX_PALETTE_MATRICES_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_MAX_VERTEX_UNITS_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_TEXTURE_CROP_RECT_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_WEIGHT_ARRAY_BUFFER_BINDING_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_WEIGHT_ARRAY_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_WEIGHT_ARRAY_POINTER_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_WEIGHT_ARRAY_SIZE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_WEIGHT_ARRAY_STRIDE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_WEIGHT_ARRAY_TYPE_OES](../javax/microedition/khronos/opengles/GL11Ext.md) <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glCurrentPaletteMatrixOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`matrixpaletteindex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexfOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `z:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `width:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `height:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexfvOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexfvOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [FloatBuffer](../java/nio/FloatBuffer.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexiOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `z:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexivOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexivOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [IntBuffer](../java/nio/IntBuffer.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexsOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`x:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `y:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `z:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `width:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`, `height:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexsvOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [ShortBuffer](../java/nio/ShortBuffer.md)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexsvOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexxOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `z:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexxvOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glDrawTexxvOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`coords:` ` [IntBuffer](../java/nio/IntBuffer.md)!`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glEnable](../javax/microedition/khronos/opengles/GL11Ext.md))`(`cap:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glEnableClientState](../javax/microedition/khronos/opengles/GL11Ext.md))`(`array:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glLoadPaletteFromModelViewMatrixOES](../javax/microedition/khronos/opengles/GL11Ext.md))`()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glMatrixIndexPointerOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glMatrixIndexPointerOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointer:` ` [Buffer](../java/nio/Buffer.md)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glTexParameterfv](../javax/microedition/khronos/opengles/GL11Ext.md))`(`target:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pname:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `param:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glWeightPointerOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [glWeightPointerOES](../javax/microedition/khronos/opengles/GL11Ext.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stride:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pointer:` ` [Buffer](../java/nio/Buffer.md)!`)` <br /> |
| --- | --- |

## Constants

### GL_MATRIX_INDEX_ARRAY_BUFFER_BINDING_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_INDEX_ARRAY_BUFFER_BINDING_OES: Int
```  

 Value: 35742

### GL_MATRIX_INDEX_ARRAY_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_INDEX_ARRAY_OES: Int
```  

 Value: 34884

### GL_MATRIX_INDEX_ARRAY_POINTER_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_INDEX_ARRAY_POINTER_OES: Int
```  

 Value: 34889

### GL_MATRIX_INDEX_ARRAY_SIZE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_INDEX_ARRAY_SIZE_OES: Int
```  

 Value: 34886

### GL_MATRIX_INDEX_ARRAY_STRIDE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_INDEX_ARRAY_STRIDE_OES: Int
```  

 Value: 34888

### GL_MATRIX_INDEX_ARRAY_TYPE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_INDEX_ARRAY_TYPE_OES: Int
```  

 Value: 34887

### GL_MATRIX_PALETTE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MATRIX_PALETTE_OES: Int
```  

 Value: 34880

### GL_MAX_PALETTE_MATRICES_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MAX_PALETTE_MATRICES_OES: Int
```  

 Value: 34882

### GL_MAX_VERTEX_UNITS_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_MAX_VERTEX_UNITS_OES: Int
```  

 Value: 34468

### GL_TEXTURE_CROP_RECT_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_TEXTURE_CROP_RECT_OES: Int
```  

 Value: 35741

### GL_WEIGHT_ARRAY_BUFFER_BINDING_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_WEIGHT_ARRAY_BUFFER_BINDING_OES: Int
```  

 Value: 34974

### GL_WEIGHT_ARRAY_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_WEIGHT_ARRAY_OES: Int
```  

 Value: 34477

### GL_WEIGHT_ARRAY_POINTER_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_WEIGHT_ARRAY_POINTER_OES: Int
```  

 Value: 34476

### GL_WEIGHT_ARRAY_SIZE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_WEIGHT_ARRAY_SIZE_OES: Int
```  

 Value: 34475

### GL_WEIGHT_ARRAY_STRIDE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_WEIGHT_ARRAY_STRIDE_OES: Int
```  

 Value: 34474

### GL_WEIGHT_ARRAY_TYPE_OES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_WEIGHT_ARRAY_TYPE_OES: Int
```  

 Value: 34473

## Public methods

### glCurrentPaletteMatrixOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glCurrentPaletteMatrixOES(matrixpaletteindex: Int): Unit
```  

### glDrawTexfOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexfOES(
    x: Float, 
    y: Float, 
    z: Float, 
    width: Float, 
    height: Float
): Unit
```  

### glDrawTexfvOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexfvOES(
    coords: FloatArray!, 
    offset: Int
): Unit
```  

### glDrawTexfvOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexfvOES(coords: FloatBuffer!): Unit
```  

### glDrawTexiOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexiOES(
    x: Int, 
    y: Int, 
    z: Int, 
    width: Int, 
    height: Int
): Unit
```  

### glDrawTexivOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexivOES(
    coords: IntArray!, 
    offset: Int
): Unit
```  

### glDrawTexivOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexivOES(coords: IntBuffer!): Unit
```  

### glDrawTexsOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexsOES(
    x: Short, 
    y: Short, 
    z: Short, 
    width: Short, 
    height: Short
): Unit
```  

### glDrawTexsvOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexsvOES(coords: ShortBuffer!): Unit
```  

### glDrawTexsvOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexsvOES(
    coords: ShortArray!, 
    offset: Int
): Unit
```  

### glDrawTexxOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexxOES(
    x: Int, 
    y: Int, 
    z: Int, 
    width: Int, 
    height: Int
): Unit
```  

### glDrawTexxvOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexxvOES(
    coords: IntArray!, 
    offset: Int
): Unit
```  

### glDrawTexxvOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glDrawTexxvOES(coords: IntBuffer!): Unit
```  

### glEnable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glEnable(cap: Int): Unit
```  

### glEnableClientState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glEnableClientState(array: Int): Unit
```  

### glLoadPaletteFromModelViewMatrixOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glLoadPaletteFromModelViewMatrixOES(): Unit
```  

### glMatrixIndexPointerOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glMatrixIndexPointerOES(
    size: Int, 
    type: Int, 
    stride: Int, 
    offset: Int
): Unit
```  

### glMatrixIndexPointerOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glMatrixIndexPointerOES(
    size: Int, 
    type: Int, 
    stride: Int, 
    pointer: Buffer!
): Unit
```  

### glTexParameterfv

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glTexParameterfv(
    target: Int, 
    pname: Int, 
    param: FloatArray!, 
    offset: Int
): Unit
```  

### glWeightPointerOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glWeightPointerOES(
    size: Int, 
    type: Int, 
    stride: Int, 
    offset: Int
): Unit
```  

### glWeightPointerOES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun glWeightPointerOES(
    size: Int, 
    type: Int, 
    stride: Int, 
    pointer: Buffer!
): Unit
```

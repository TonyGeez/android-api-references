# Array

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Array

```
class Array
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.reflect.Array](../java/lang/reflect/Array.md) |

The`Array`class provides static methods to dynamically create and access Java arrays.

`Array`permits widening conversions to occur during a get or set operation, but throws an`IllegalArgumentException`if a narrowing conversion would occur.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [get](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`boolean`. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getByte](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`byte`. |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getChar](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`char`. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`double`. |
| static [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`float`. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as an`int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`)` Returns the length of the specified array object, as an`int`. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`long`. |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the indexed component in the specified array object, as a`short`. |
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [newInstance](../java/lang/reflect/Array.md))`(`componentType:` ` [Class](../java/lang/Class.md)<*>`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new array with the specified component type and length. |
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [newInstance](../java/lang/reflect/Array.md))`(`componentType:` ` [Class](../java/lang/Class.md)<*>`, `vararg` `dimensions:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new array with the specified component type and dimensions. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Sets the value of the indexed component of the specified array object to the specified new value. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `z:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`boolean`value. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`byte`value. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChar](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`char`value. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`double`value. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`float`value. |
| --- | --- |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`int`value. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `l:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`long`value. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](../java/lang/reflect/Array.md))`(`array:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `s:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the value of the indexed component of the specified array object to the specified`short`value. |
| --- | --- |

## Public methods

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(
    array: Any, 
    index: Int
): Any?
```

Returns the value of the indexed component in the specified array object. The value is automatically wrapped in an object if it has a primitive type.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the (possibly wrapped) value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBoolean(
    array: Any, 
    index: Int
): Boolean
```

Returns the value of the indexed component in the specified array object, as a`boolean`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getByte(
    array: Any, 
    index: Int
): Byte
```

Returns the value of the indexed component in the specified array object, as a`byte`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getChar(
    array: Any, 
    index: Int
): Char
```

Returns the value of the indexed component in the specified array object, as a`char`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDouble(
    array: Any, 
    index: Int
): Double
```

Returns the value of the indexed component in the specified array object, as a`double`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getFloat(
    array: Any, 
    index: Int
): Float
```

Returns the value of the indexed component in the specified array object, as a`float`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInt(
    array: Any, 
    index: Int
): Int
```

Returns the value of the indexed component in the specified array object, as an`int`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLength(array: Any): Int
```

Returns the length of the specified array object, as an`int`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the array |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if the object argument is not an array |

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLong(
    array: Any, 
    index: Int
): Long
```

Returns the value of the indexed component in the specified array object, as a`long`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getShort(
    array: Any, 
    index: Int
): Short
```

Returns the value of the indexed component in the specified array object, as a`short`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the value of the indexed component in the specified array |

| Exceptions ||
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object is null |
| `java.lang.IllegalArgumentException` | If the specified object is not an array, or if the indexed element cannot be converted to the return type by an identity or widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#get](../java/lang/reflect/Array.md)) 

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    componentType: Class<*>, 
    length: Int
): Any
```

Creates a new array with the specified component type and length. Invoking this method is equivalent to creating an array as follows: 

```kotlin
int[] x = {length};
  Array.newInstance(componentType, x);
  
```

<br />

The number of dimensions of the new array must not exceed 255.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `componentType` | [Class](../java/lang/Class.md)\<\*\>:the`Class`object representing the component type of the new array |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the new array |

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | the new array |

| Exceptions ||
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified`componentType`parameter is null |
| `java.lang.IllegalArgumentException` | if componentType is [java.lang.Void#TYPE](../java/lang/Void.md) or if the number of dimensions of the requested array instance exceed 255. |
| `java.lang.NegativeArraySizeException` | if the specified`length`is negative |
| --- | --- |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun newInstance(
    componentType: Class<*>, 
    vararg dimensions: Int
): Any
```

Creates a new array with the specified component type and dimensions. If`componentType`represents a non-array class or interface, the new array has`dimensions.length`dimensions and`componentType`as its component type. If`componentType`represents an array class, the number of dimensions of the new array is equal to the sum of`dimensions.length`and the number of dimensions of`componentType`. In this case, the component type of the new array is the component type of`componentType`.

The number of dimensions of the new array must not exceed 255.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `componentType` | [Class](../java/lang/Class.md)\<\*\>:the`Class`object representing the component type of the new array |
| `dimensions` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an array of`int`representing the dimensions of the new array |

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | the new array |

| Exceptions ||
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified`componentType`argument is null |
| `java.lang.IllegalArgumentException` | if the specified`dimensions`argument is a zero-dimensional array, if componentType is [java.lang.Void#TYPE](../java/lang/Void.md), or if the number of dimensions of the requested array instance exceed 255. |
| `java.lang.NegativeArraySizeException` | if any of the components in the specified`dimensions`argument is negative. |
| --- | --- |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun set(
    array: Any, 
    index: Int, 
    value: Any?
): Unit
```

Sets the value of the indexed component of the specified array object to the specified new value. The new value is first automatically unwrapped if the array has a primitive component type.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the array component type is primitive and an unwrapping conversion fails |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

### setBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setBoolean(
    array: Any, 
    index: Int, 
    z: Boolean
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`boolean`value.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `z` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setByte(
    array: Any, 
    index: Int, 
    b: Byte
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`byte`value.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setChar(
    array: Any, 
    index: Int, 
    c: Char
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`char`value.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setDouble(
    array: Any, 
    index: Int, 
    d: Double
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`double`value.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setFloat(
    array: Any, 
    index: Int, 
    f: Float
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`float`value.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setInt(
    array: Any, 
    index: Int, 
    i: Int
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`int`value.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setLong(
    array: Any, 
    index: Int, 
    l: Long
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`long`value.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md)) 

### setShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setShort(
    array: Any, 
    index: Int, 
    s: Short
): Unit
```

Sets the value of the indexed component of the specified array object to the specified`short`value.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `array` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index into the array |
| `s` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the new value of the indexed component |
| --- | --- |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | If the specified object argument is null |
| `java.lang.IllegalArgumentException` | If the specified object argument is not an array, or if the specified value cannot be converted to the underlying array's component type by an identity or a primitive widening conversion |
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified`index`argument is negative, or if it is greater than or equal to the length of the specified array |
| --- | --- |

**See Also**

- [java.lang.reflect.Array#set](../java/lang/reflect/Array.md))

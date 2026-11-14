# GestureLibraries

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureLibraries

Kotlin| [Java](../android/gesture/GestureLibraries.md) 
| --- | --- |

```
class GestureLibraries
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.gesture.GestureLibraries](../android/gesture/GestureLibraries.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [GestureLibrary](../android/gesture/GestureLibrary.md)! | [fromFile](../android/gesture/GestureLibraries.md))`(`path:` ` [File](../java/io/File.md)!`)` <br /> |
| static [GestureLibrary](../android/gesture/GestureLibrary.md)! | [fromFile](../android/gesture/GestureLibraries.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [GestureLibrary](../android/gesture/GestureLibrary.md) | [fromFileDescriptor](../android/gesture/GestureLibraries.md))`(`pfd:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)`)` <br /> |
| --- | --- |
| static [GestureLibrary](../android/gesture/GestureLibrary.md)! | [fromPrivateFile](../android/gesture/GestureLibraries.md))`(`context:` ` [Context](../android/content/Context.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [GestureLibrary](../android/gesture/GestureLibrary.md)! | [fromRawResource](../android/gesture/GestureLibraries.md))`(`context:` ` [Context](../android/content/Context.md)!`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

## Public methods

### fromFile

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromFile(path: File!): GestureLibrary!
```  

### fromFile

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromFile(path: String!): GestureLibrary!
```  

### fromFileDescriptor

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromFileDescriptor(pfd: ParcelFileDescriptor): GestureLibrary
```

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `pfd` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [GestureLibrary](../android/gesture/GestureLibrary.md) | This value cannot be`null`. |

### fromPrivateFile

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromPrivateFile(
    context: Context!, 
    name: String!
): GestureLibrary!
```  

### fromRawResource

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromRawResource(
    context: Context!, 
    resourceId: Int
): GestureLibrary!
```

# GestureLibraries

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureLibraries

Kotlin| [Java](GestureLibraries.md) 
| --- | --- |

```
class GestureLibraries
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.gesture.GestureLibraries](GestureLibraries.md) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [GestureLibrary](GestureLibrary.md)! | [fromFile](GestureLibraries.md))`(`path:` ` [File](../java.io/File.md)!`)` <br /> |
| static [GestureLibrary](GestureLibrary.md)! | [fromFile](GestureLibraries.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [GestureLibrary](GestureLibrary.md) | [fromFileDescriptor](GestureLibraries.md))`(`pfd:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`)` <br /> |
| --- | --- |
| static [GestureLibrary](GestureLibrary.md)! | [fromPrivateFile](GestureLibraries.md))`(`context:` ` [Context](../android.content/Context.md)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [GestureLibrary](GestureLibrary.md)! | [fromRawResource](GestureLibraries.md))`(`context:` ` [Context](../android.content/Context.md)!`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
| `pfd` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [GestureLibrary](GestureLibrary.md) | This value cannot be`null`. |

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

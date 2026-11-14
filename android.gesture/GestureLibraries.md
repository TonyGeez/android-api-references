# GestureLibraries

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GestureLibraries

Kotlin| [Java](https://developer.android.com/reference/android/gesture/GestureLibraries "View this page in Java") 

```
class GestureLibraries
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.gesture.GestureLibraries](https://developer.android.com/reference/kotlin/android/gesture/GestureLibraries#) |

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary)! | [fromFile](https://developer.android.com/reference/kotlin/android/gesture/GestureLibraries#fromFile(java.io.File))`(`path:` ` [File](https://developer.android.com/reference/kotlin/java/io/File.html#)!`)` <br /> |
| static [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary)! | [fromFile](https://developer.android.com/reference/kotlin/android/gesture/GestureLibraries#fromFile(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary) | [fromFileDescriptor](https://developer.android.com/reference/kotlin/android/gesture/GestureLibraries#fromFileDescriptor(android.os.ParcelFileDescriptor))`(`pfd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`)` <br /> |
| static [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary)! | [fromPrivateFile](https://developer.android.com/reference/kotlin/android/gesture/GestureLibraries#fromPrivateFile(android.content.Context,%20kotlin.String))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| static [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary)! | [fromRawResource](https://developer.android.com/reference/kotlin/android/gesture/GestureLibraries#fromRawResource(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `resourceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

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
| `pfd` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------|
| [GestureLibrary](https://developer.android.com/reference/kotlin/android/gesture/GestureLibrary) | This value cannot be`null`. |

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

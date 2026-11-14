Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssetManager

```
class AssetManager : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.res.AssetManager](https://developer.android.com/reference/kotlin/android/content/res/AssetManager#) |

Provides access to an application's raw asset files; see `https://developer.android.com/reference/kotlin/android/content/res/Resources` for the way most applications will want to retrieve their resource data. This class presents a lower-level API that allows you to open and read raw files that have been bundled with the application as a simple stream of bytes.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager.AssetInputStream` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_BUFFER:kotlin.Int` Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: Attempt to load contents into memory, for fast small reads. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_RANDOM:kotlin.Int` Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: Read chunks, and seek forward and backward. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_STREAMING:kotlin.Int` Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: Read sequentially, with an occasional forward seek. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_UNKNOWN:kotlin.Int` Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: no specific information about how data will be accessed. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#close()()` Close this asset manager. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#getLocales()()` Get the locales that this asset manager contains data for. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#list(kotlin.String)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Return a String array of all the assets at the given path. |
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Open an asset using ACCESS_STREAMING mode. |
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, accessMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Open an asset using an explicit access mode, returning an InputStream to read its contents. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#openFd(kotlin.String)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Open an uncompressed asset by mmapping it and returning an `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor`. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#openNonAssetFd(kotlin.Int,%20kotlin.String)(cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Open a non-asset as an asset by mmapping it and returning an `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor`. |
| [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#openNonAssetFd(kotlin.String)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Open a non-asset as an asset by mmapping it and returning an `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor`. |
| [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#openXmlResourceParser(kotlin.Int,%20kotlin.String)(cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve a parser for a compiled XML file. |
| [XmlResourceParser](https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser) | `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#openXmlResourceParser(kotlin.String)(fileName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Retrieve a parser for a compiled XML file. |

## Constants

### ACCESS_BUFFER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_BUFFER: Int
```

Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: Attempt to load contents into memory, for fast small reads.

 Value: 3

### ACCESS_RANDOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_RANDOM: Int
```

Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: Read chunks, and seek forward and backward.

 Value: 1

### ACCESS_STREAMING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_STREAMING: Int
```

Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: Read sequentially, with an occasional forward seek.

 Value: 2

### ACCESS_UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACCESS_UNKNOWN: Int
```

Mode for `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`: no specific information about how data will be accessed.

 Value: 0

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Close this asset manager.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### getLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLocales(): Array<String!>!
```

Get the locales that this asset manager contains data for.

On SDK 21 (Android 5.0: Lollipop) and above, Locale strings are valid [BCP-47](https://tools.ietf.org/html/bcp47) language tags and can be parsed using `https://developer.android.com/reference/kotlin/java/util/Locale.html#forLanguageTag(kotlin.String)`.

On SDK 20 (Android 4.4W: KitKat for watches) and below, locale strings are of the form `ll_CC` where `ll` is a two letter language code, and `CC` is a two letter country code.

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun list(path: String): Array<String!>?
```

Return a String array of all the assets at the given path.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A relative path within the assets, i.e., "docs/home.html". This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | String\[\] Array of strings, one for each asset. These file names are relative to 'path'. You can open the file by concatenating 'path' and a name in the returned string (via File) and passing that to open(). This value may be `null`. |

**See Also**

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun open(fileName: String): InputStream
```

Open an asset using ACCESS_STREAMING mode. This provides access to files that have been bundled with an application as assets -- that is, files placed in to the "assets" directory.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the asset to open. This name can be hierarchical. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#list(kotlin.String)`

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun open(
    fileName: String, 
    accessMode: Int
): InputStream
```

Open an asset using an explicit access mode, returning an InputStream to read its contents. This provides access to files that have been bundled with an application as assets -- that is, files placed in to the "assets" directory.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the asset to open. This name can be hierarchical. This value cannot be `null`. |
| `accessMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired access mode for retrieving the data. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#` | This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_STREAMING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_RANDOM:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#ACCESS_BUFFER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#open(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/res/AssetManager#list(kotlin.String)`

### openFd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openFd(fileName: String): AssetFileDescriptor
```

Open an uncompressed asset by mmapping it and returning an `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor`. This provides access to files that have been bundled with an application as assets -- that is, files placed in to the "assets" directory. The asset must be uncompressed, or an exception will be thrown.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the asset to open. This name can be hierarchical. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor` | An open AssetFileDescriptor. This value cannot be `null`. |

### openNonAssetFd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openNonAssetFd(
    cookie: Int, 
    fileName: String
): AssetFileDescriptor
```

Open a non-asset as an asset by mmapping it and returning an `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor`. This provides direct access to all of the files included in an application package (not only its assets). Applications should not normally use this. The asset must not be compressed, or an exception will be thrown.

| Parameters ||
|---|---|
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Identifier of the package to be opened. |
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the asset to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor` | This value cannot be `null`. |

### openNonAssetFd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openNonAssetFd(fileName: String): AssetFileDescriptor
```

Open a non-asset as an asset by mmapping it and returning an `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor`. This provides direct access to all of the files included in an application package (not only its assets). Applications should not normally use this. The asset must not be compressed, or an exception will be thrown.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Name of the asset to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor` | This value cannot be `null`. |

### openXmlResourceParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openXmlResourceParser(
    cookie: Int, 
    fileName: String
): XmlResourceParser
```

Retrieve a parser for a compiled XML file.

| Parameters ||
|---|---|
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Identifier of the package to be opened. |
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the file to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser` | This value cannot be `null`. |

### openXmlResourceParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openXmlResourceParser(fileName: String): XmlResourceParser
```

Retrieve a parser for a compiled XML file.

| Parameters ||
|---|---|
| `fileName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the file to retrieve. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/res/XmlResourceParser` | This value cannot be `null`. |

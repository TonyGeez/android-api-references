Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpObjectInfo

Kotlin | [Java](../android/mtp/MtpObjectInfo.md)
| --- | --- |

```
class MtpObjectInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpObjectInfo](../android/mtp/MtpObjectInfo.md) |

This class encapsulates information about an object on an MTP device. This corresponds to the ObjectInfo Dataset described in section 5.3.1 of the MTP specification.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo.Builder` Builds a new object info instance. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getAssociationDesc()()` Returns the association description for the MTP object Will be zero objects that are not of format `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#FORMAT_ASSOCIATION:kotlin.Int` |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getAssociationType()()` Returns the association type for the MTP object Will be zero objects that are not of format `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#FORMAT_ASSOCIATION:kotlin.Int` For directories the association type is typically `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#ASSOCIATION_TYPE_GENERIC_FOLDER:kotlin.Int` |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getCompressedSize()()` Returns the size of the MTP object |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getCompressedSizeLong()()` Returns the size of the MTP object |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getDateCreated()()` Returns the creation date of the MTP object The value is represented as milliseconds since January 1, 1970 |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getDateModified()()` Returns the modification date of the MTP object The value is represented as milliseconds since January 1, 1970 |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getFormat()()` Returns the format code for the MTP object |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getImagePixDepth()()` Returns the depth of the MTP object in bits per pixel Will be zero for non-image objects |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getImagePixDepthLong()()` Returns the depth of the MTP object in bits per pixel Will be zero for non-image objects |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getImagePixHeight()()` Returns the height of the MTP object in pixels Will be zero for non-image objects |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getImagePixHeightLong()()` Returns the height of the MTP object in pixels Will be zero for non-image objects |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getImagePixWidth()()` Returns the width of the MTP object in pixels Will be zero for non-image objects |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getImagePixWidthLong()()` Returns the width of the MTP object in pixels Will be zero for non-image objects |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getKeywords()()` Returns a comma separated list of keywords for the MTP object |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getName()()` Returns the name of the MTP object |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getObjectHandle()()` Returns the object handle for the MTP object |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getParent()()` Returns the object handle for the object's parent Will be zero for the root directory of a storage unit |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getProtectionStatus()()` Returns the protection status for the MTP object Possible values are: - `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#PROTECTION_STATUS_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#PROTECTION_STATUS_READ_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#PROTECTION_STATUS_NON_TRANSFERABLE_DATA:kotlin.Int` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getSequenceNumber()()` Returns the sequence number for the MTP object This field is typically not used for MTP devices, but is sometimes used to define a sequence of photos on PTP cameras. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getSequenceNumberLong()()` Returns the sequence number for the MTP object This field is typically not used for MTP devices, but is sometimes used to define a sequence of photos on PTP cameras. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getStorageId()()` Returns the storage ID for the MTP object's storage unit |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbCompressedSize()()` Returns the size of the MTP object's thumbnail Will be zero for objects with no thumbnail |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbCompressedSizeLong()()` Returns the size of the MTP object's thumbnail Will be zero for objects with no thumbnail |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbFormat()()` Returns the format code for the MTP object's thumbnail Will be zero for objects with no thumbnail |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbPixHeight()()` Returns the height of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbPixHeightLong()()` Returns the height of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbPixWidth()()` Returns the width of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/mtp/MtpObjectInfo#getThumbPixWidthLong()()` Returns the width of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail |

## Public methods

### getAssociationDesc

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAssociationDesc(): Int
```

Returns the association description for the MTP object Will be zero objects that are not of format `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#FORMAT_ASSOCIATION:kotlin.Int`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the object's association description |

### getAssociationType

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAssociationType(): Int
```

Returns the association type for the MTP object Will be zero objects that are not of format `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#FORMAT_ASSOCIATION:kotlin.Int` For directories the association type is typically `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#ASSOCIATION_TYPE_GENERIC_FOLDER:kotlin.Int`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the object's association type |

### getCompressedSize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCompressedSize(): Int
```

Returns the size of the MTP object

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the object size |

### getCompressedSizeLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCompressedSizeLong(): Long
```

Returns the size of the MTP object

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the object size |

### getDateCreated

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDateCreated(): Long
```

Returns the creation date of the MTP object The value is represented as milliseconds since January 1, 1970

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the object's creation date |

### getDateModified

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDateModified(): Long
```

Returns the modification date of the MTP object The value is represented as milliseconds since January 1, 1970

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the object's modification date |

### getFormat

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFormat(): Int
```

Returns the format code for the MTP object

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the format code |

### getImagePixDepth

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImagePixDepth(): Int
```

Returns the depth of the MTP object in bits per pixel Will be zero for non-image objects

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the image depth |

### getImagePixDepthLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImagePixDepthLong(): Long
```

Returns the depth of the MTP object in bits per pixel Will be zero for non-image objects

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the image depth |

### getImagePixHeight

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImagePixHeight(): Int
```

Returns the height of the MTP object in pixels Will be zero for non-image objects

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the image height |

### getImagePixHeightLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImagePixHeightLong(): Long
```

Returns the height of the MTP object in pixels Will be zero for non-image objects

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the image height |

### getImagePixWidth

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImagePixWidth(): Int
```

Returns the width of the MTP object in pixels Will be zero for non-image objects

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the image width |

### getImagePixWidthLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getImagePixWidthLong(): Long
```

Returns the width of the MTP object in pixels Will be zero for non-image objects

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the image width |

### getKeywords

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeywords(): String
```

Returns a comma separated list of keywords for the MTP object

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the object's keyword list. This value cannot be `null`. |

### getName

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

Returns the name of the MTP object

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the object's name. This value cannot be `null`. |

### getObjectHandle

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getObjectHandle(): Int
```

Returns the object handle for the MTP object

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the object handle |

### getParent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParent(): Int
```

Returns the object handle for the object's parent Will be zero for the root directory of a storage unit

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the object's parent |

### getProtectionStatus

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProtectionStatus(): Int
```

Returns the protection status for the MTP object Possible values are:

- `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#PROTECTION_STATUS_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#PROTECTION_STATUS_READ_ONLY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/mtp/MtpConstants#PROTECTION_STATUS_NON_TRANSFERABLE_DATA:kotlin.Int`

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the protection status |

### getSequenceNumber

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSequenceNumber(): Int
```

Returns the sequence number for the MTP object This field is typically not used for MTP devices, but is sometimes used to define a sequence of photos on PTP cameras.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the object's sequence number |

### getSequenceNumberLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSequenceNumberLong(): Long
```

Returns the sequence number for the MTP object This field is typically not used for MTP devices, but is sometimes used to define a sequence of photos on PTP cameras.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the object's sequence number |

### getStorageId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStorageId(): Int
```

Returns the storage ID for the MTP object's storage unit

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the storage ID |

### getThumbCompressedSize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbCompressedSize(): Int
```

Returns the size of the MTP object's thumbnail Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the thumbnail size |

### getThumbCompressedSizeLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbCompressedSizeLong(): Long
```

Returns the size of the MTP object's thumbnail Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the thumbnail size |

### getThumbFormat

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbFormat(): Int
```

Returns the format code for the MTP object's thumbnail Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the thumbnail format code |

### getThumbPixHeight

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbPixHeight(): Int
```

Returns the height of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the thumbnail height |

### getThumbPixHeightLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbPixHeightLong(): Long
```

Returns the height of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the thumbnail height |

### getThumbPixWidth

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbPixWidth(): Int
```

Returns the width of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the thumbnail width |

### getThumbPixWidthLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getThumbPixWidthLong(): Long
```

Returns the width of the MTP object's thumbnail in pixels Will be zero for objects with no thumbnail

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the thumbnail width |

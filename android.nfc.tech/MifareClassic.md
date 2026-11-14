Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MifareClassic

Kotlin | [Java](https://developer.android.com/reference/android/nfc/tech/MifareClassic "View this page in Java")
| --- | --- |

```
class MifareClassic : TagTechnology
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.nfc.tech.MifareClassic](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#) |

Provides access to MIFARE Classic properties and I/O operations on a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#`.

Acquire a `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#` object using `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#get(android.nfc.Tag)`.

MIFARE Classic is also known as MIFARE Standard.

MIFARE Classic tags are divided into sectors, and each sector is sub-divided into blocks. Block size is always 16 bytes (`https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#BLOCK_SIZE:kotlin.Int`. Sector size varies.

- MIFARE Classic Mini are 320 bytes (`https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_MINI:kotlin.Int`), with 5 sectors each of 4 blocks.
- MIFARE Classic 1k are 1024 bytes (`https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_1K:kotlin.Int`), with 16 sectors each of 4 blocks.
- MIFARE Classic 2k are 2048 bytes (`https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_2K:kotlin.Int`), with 32 sectors each of 4 blocks.
- MIFARE Classic 4k are 4096 bytes (`https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_4K:kotlin.Int`). The first 32 sectors contain 4 blocks and the last 8 sectors contain 16 blocks.

MIFARE Classic tags require authentication on a per-sector basis before any other I/O operations on that sector can be performed. There are two keys per sector, and ACL bits determine what I/O operations are allowed on that sector after authenticating with a key. See `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#authenticateSectorWithKeyA(kotlin.Int,%20kotlin.ByteArray)` and `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#authenticateSectorWithKeyB(kotlin.Int,%20kotlin.ByteArray)`.

Three well-known authentication keys are defined in this class: `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_DEFAULT:kotlin.ByteArray`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_MIFARE_APPLICATION_DIRECTORY:kotlin.ByteArray`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_NFC_FORUM:kotlin.ByteArray`.

- `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_DEFAULT:kotlin.ByteArray` is the default factory key for MIFARE Classic.
- `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_MIFARE_APPLICATION_DIRECTORY:kotlin.ByteArray` is the well-known key for MIFARE Classic cards that have been formatted according to the MIFARE Application Directory (MAD) specification.
- `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_NFC_FORUM:kotlin.ByteArray` is the well-known key for MIFARE Classic cards that have been formatted according to the NXP specification for NDEF on MIFARE Classic.

 Implementation of this class on a Android NFC device is optional. If it is not implemented, then `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#` will never be enumerated in `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()`. If it is enumerated, then all `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#` I/O operations will be supported, and `https://developer.android.com/reference/kotlin/android/nfc/tech/Ndef#MIFARE_CLASSIC:kotlin.String` NDEF tags will also be supported. In either case, `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA` will also be enumerated on the tag, because all MIFARE Classic tags are also `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA`.

 **Note:** Methods that perform I/O operations require the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#BLOCK_SIZE:kotlin.Int` Size of a MIFARE Classic block (in bytes) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_1K:kotlin.Int` Tag contains 16 sectors, each with 4 blocks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_2K:kotlin.Int` Tag contains 32 sectors, each with 4 blocks. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_4K:kotlin.Int` Tag contains 40 sectors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_MINI:kotlin.Int` Tag contains 5 sectors, each with 4 blocks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_CLASSIC:kotlin.Int` A MIFARE Classic tag |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_PLUS:kotlin.Int` A MIFARE Plus tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_PRO:kotlin.Int` A MIFARE Pro tag |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_UNKNOWN:kotlin.Int` A MIFARE Classic compatible card of unknown type |
| --- | --- |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#authenticateSectorWithKeyA(kotlin.Int,%20kotlin.ByteArray)(sectorIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Authenticate a sector with key A. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#authenticateSectorWithKeyB(kotlin.Int,%20kotlin.ByteArray)(sectorIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Authenticate a sector with key B. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#blockToSector(kotlin.Int)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the sector that contains a given block. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#close()()` Disable I/O operations to the tag from this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object, and release resources. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#connect()()` Enable I/O operations to the tag from this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#decrement(kotlin.Int,%20kotlin.Int)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Decrement a value block, storing the result in the temporary block on the tag. |
| --- | --- |
| static [MifareClassic](https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#get(android.nfc.Tag)(tag: https://developer.android.com/reference/kotlin/android/nfc/Tag.html#!)` Get an instance of `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#` for the given tag. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getBlockCount()()` Return the total number of MIFARE Classic blocks. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getBlockCountInSector(kotlin.Int)(sectorIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the number of blocks in the given sector. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getMaxTransceiveLength()()` Return the maximum number of bytes that can be sent with `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getSectorCount()()` Return the number of MIFARE Classic sectors. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getSize()()` Return the size of the tag in bytes |
| --- | --- |
| [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getTag()()` Get the `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#` object backing this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getTimeout()()` Get the current `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)` timeout in milliseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getType()()` Return the type of this MIFARE Classic compatible tag. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#increment(kotlin.Int,%20kotlin.Int)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Increment a value block, storing the result in the temporary block on the tag. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#isConnected()()` Helper to indicate if I/O operations should be possible. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#readBlock(kotlin.Int)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Read 16-byte block. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#restore(kotlin.Int)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy from a value block to the temporary block. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#sectorToBlock(kotlin.Int)(sectorIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return the first block of a given sector. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#setTimeout(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)` timeout in milliseconds. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Send raw NfcA data to a tag and receive the response. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transfer(kotlin.Int)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copy from the temporary block to a value block. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#writeBlock(kotlin.Int,%20kotlin.ByteArray)(blockIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Write 16-byte block. |
| --- | --- |

| Properties ||
|---|---|
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_DEFAULT:kotlin.ByteArray` The default factory key. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_MIFARE_APPLICATION_DIRECTORY:kotlin.ByteArray` The well-known key for tags formatted according to the MIFARE Application Directory (MAD) specification. |
| static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#KEY_NFC_FORUM:kotlin.ByteArray` The well-known key for tags formatted according to the NDEF on MIFARE Classic specification. |
| --- | --- |

## Constants

### BLOCK_SIZE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BLOCK_SIZE: Int
```

Size of a MIFARE Classic block (in bytes)

 Value: 16

### SIZE_1K

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE_1K: Int
```

Tag contains 16 sectors, each with 4 blocks.

 Value: 1024

### SIZE_2K

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE_2K: Int
```

Tag contains 32 sectors, each with 4 blocks.

 Value: 2048

### SIZE_4K

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE_4K: Int
```

Tag contains 40 sectors. The first 32 sectors contain 4 blocks and the last 8 sectors contain 16 blocks.

 Value: 4096

### SIZE_MINI

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE_MINI: Int
```

Tag contains 5 sectors, each with 4 blocks.

 Value: 320

### TYPE_CLASSIC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CLASSIC: Int
```

A MIFARE Classic tag

 Value: 0

### TYPE_PLUS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PLUS: Int
```

A MIFARE Plus tag

 Value: 1

### TYPE_PRO

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_PRO: Int
```

A MIFARE Pro tag

 Value: 2

### TYPE_UNKNOWN

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_UNKNOWN: Int
```

A MIFARE Classic compatible card of unknown type

 Value: -1

## Public methods

### authenticateSectorWithKeyA

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun authenticateSectorWithKeyA(
    sectorIndex: Int, 
    key: ByteArray!
): Boolean
```

Authenticate a sector with key A.

Successful authentication of a sector with key A enables other I/O operations on that sector. The set of operations granted by key A key depends on the ACL bits set in that sector. For more information see the MIFARE Classic specification on <http://www.nxp.com>.

A failed authentication attempt causes an implicit reconnection to the tag, so authentication to other sectors will be lost.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `sectorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of sector to authenticate, starting from 0 |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: 6-byte authentication key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on authentication failure |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### authenticateSectorWithKeyB

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun authenticateSectorWithKeyB(
    sectorIndex: Int, 
    key: ByteArray!
): Boolean
```

Authenticate a sector with key B.

Successful authentication of a sector with key B enables other I/O operations on that sector. The set of operations granted by key B depends on the ACL bits set in that sector. For more information see the MIFARE Classic specification on <http://www.nxp.com>.

A failed authentication attempt causes an implicit reconnection to the tag, so authentication to other sectors will be lost.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `sectorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of sector to authenticate, starting from 0 |
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: 6-byte authentication key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on authentication failure |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### blockToSector

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun blockToSector(blockIndex: Int): Int
```

Return the sector that contains a given block.

Does not cause any RF activity and does not block.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to lookup, starting from 0 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | sector index that contains the block |

### close

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Disable I/O operations to the tag from this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object, and release resources.

Also causes all blocked I/O operations on other thread to be canceled and return with `https://developer.android.com/reference/kotlin/java/io/IOException.html#`.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### connect

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connect(): Unit
```

Enable I/O operations to the tag from this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object.

May cause RF activity and may block. Must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` by calling #close from another thread.

Only one `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object can be connected to a `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#` at a time.

Applications must call #close when I/O operations are complete.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or connect is canceled |
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |
| --- | --- |

### decrement

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun decrement(
    blockIndex: Int, 
    value: Int
): Unit
```

Decrement a value block, storing the result in the temporary block on the tag.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to decrement, starting from 0 |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): non-negative to decrement by |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### get

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun get(tag: Tag!): MifareClassic!
```

Get an instance of `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#` for the given tag.

Does not cause any RF activity and does not block.

Returns null if `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#` was not enumerated in `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#getTechList()`. This indicates the tag is not MIFARE Classic compatible, or this Android device does not support MIFARE Classic.

| Parameters ||
|---|---|
| `tag` | [Tag](https://developer.android.com/reference/kotlin/android/nfc/Tag.html#)!: an MIFARE Classic compatible tag |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#!` | MIFARE Classic object |

### getBlockCount

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBlockCount(): Int
```

Return the total number of MIFARE Classic blocks.

Does not cause any RF activity and does not block.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | total number of blocks |

### getBlockCountInSector

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBlockCountInSector(sectorIndex: Int): Int
```

Return the number of blocks in the given sector.

Does not cause any RF activity and does not block.

| Parameters ||
|---|---|
| `sectorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of sector, starting from 0 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of blocks in the sector |

### getMaxTransceiveLength

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxTransceiveLength(): Int
```

Return the maximum number of bytes that can be sent with `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of bytes that can be sent with `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)`. |

### getSectorCount

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSectorCount(): Int
```

Return the number of MIFARE Classic sectors.

Does not cause any RF activity and does not block.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of sectors |

### getSize

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSize(): Int
```

Return the size of the tag in bytes

One of `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_MINI:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_1K:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_2K:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#SIZE_4K:kotlin.Int`. These constants are equal to their respective size in bytes.

Does not cause any RF activity and does not block.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | size in bytes |

### getTag

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTag(): Tag!
```

Get the `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#` object backing this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#!` | the `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#` backing this `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology` object. |

### getTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTimeout(): Int
```

Get the current `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)` timeout in milliseconds.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | timeout value in milliseconds |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### getType

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Return the type of this MIFARE Classic compatible tag.

One of `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_UNKNOWN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_CLASSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_PLUS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#TYPE_PRO:kotlin.Int`.

Does not cause any RF activity and does not block.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | type |

### increment

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun increment(
    blockIndex: Int, 
    value: Int
): Unit
```

Increment a value block, storing the result in the temporary block on the tag.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to increment, starting from 0 |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): non-negative to increment by |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### isConnected

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isConnected(): Boolean
```

Helper to indicate if I/O operations should be possible.

Returns true if `https://developer.android.com/reference/kotlin/android/nfc/tech/TagTechnology#connect()` has completed, and #close has not been called, and the `https://developer.android.com/reference/kotlin/android/nfc/Tag.html#` is not known to be out of range.

Does not cause RF activity, and does not block.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if I/O operations should be possible |

### readBlock

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun readBlock(blockIndex: Int): ByteArray!
```

Read 16-byte block.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to read, starting from 0 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | 16 byte block |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### restore

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun restore(blockIndex: Int): Unit
```

Copy from a value block to the temporary block.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to copy from |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### sectorToBlock

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sectorToBlock(sectorIndex: Int): Int
```

Return the first block of a given sector.

Does not cause any RF activity and does not block.

| Parameters ||
|---|---|
| `sectorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of sector to lookup, starting from 0 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | block index of first block in sector |

### setTimeout

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTimeout(timeout: Int): Unit
```

Set the `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)` timeout in milliseconds.

The timeout only applies to `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)` on this object, and is reset to a default value when #close is called.

Setting a longer timeout may be useful when performing transactions that require a long processing time on the tag such as key generation.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): timeout value in milliseconds |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the tag object is reused after the tag has left the field |

### transceive

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transceive(data: ByteArray!): ByteArray!
```

Send raw NfcA data to a tag and receive the response.

This is equivalent to connecting to this tag via `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA` and calling `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)`. Note that all MIFARE Classic tags are based on `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA` technology.

Use `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#getMaxTransceiveLength()` to retrieve the maximum number of bytes that can be sent with `https://developer.android.com/reference/kotlin/android/nfc/tech/MifareClassic#transceive(kotlin.ByteArray)`.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.
**See Also**

- `https://developer.android.com/reference/kotlin/android/nfc/tech/NfcA#transceive(kotlin.ByteArray)`

### transfer

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transfer(blockIndex: Int): Unit
```

Copy from the temporary block to a value block.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to copy to |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

### writeBlock

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeBlock(
    blockIndex: Int, 
    data: ByteArray!
): Unit
```

Write 16-byte block.

This is an I/O operation and will block until complete. It must not be called from the main application thread. A blocked call will be canceled with `https://developer.android.com/reference/kotlin/java/io/IOException.html#` if #close is called from another thread.

Requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#NFC:kotlin.String` permission.

| Parameters ||
|---|---|
| `blockIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of block to write, starting from 0 |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: 16 bytes of data to write |

| Exceptions ||
|---|---|
| `android.nfc.TagLostException` | if the tag leaves the field |
| `java.io.IOException` | if there is an I/O failure, or the operation is canceled |

## Properties

### KEY_DEFAULT

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DEFAULT: ByteArray!
```

The default factory key.

### KEY_MIFARE_APPLICATION_DIRECTORY

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MIFARE_APPLICATION_DIRECTORY: ByteArray!
```

The well-known key for tags formatted according to the MIFARE Application Directory (MAD) specification.

### KEY_NFC_FORUM

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NFC_FORUM: ByteArray!
```

The well-known key for tags formatted according to the NDEF on MIFARE Classic specification.

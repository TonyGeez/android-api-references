# ContactsContract.FullNameStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FullNameStyle

Kotlin| [Java](../android/provider/ContactsContract.FullNameStyle.md) 
| --- | --- |

```
interface FullNameStyle
```

| [android.provider.ContactsContract.FullNameStyle](../android/provider/ContactsContract.FullNameStyle.md) |

Constants for various styles of combining given name, family name etc into a full name. For example, the western tradition follows the pattern 'given name' 'middle name' 'family name' with the alternative pattern being 'family name', 'given name' 'middle name'. The CJK tradition is 'family name' 'middle name' 'given name', with Japanese favoring a space between the names and Chinese omitting the space.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHINESE](../android/provider/ContactsContract.FullNameStyle.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CJK](../android/provider/ContactsContract.FullNameStyle.md) Used if the name is written in Hanzi/Kanji/Hanja and we could not determine which specific language it belongs to: Chinese, Japanese or Korean. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JAPANESE](../android/provider/ContactsContract.FullNameStyle.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KOREAN](../android/provider/ContactsContract.FullNameStyle.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDEFINED](../android/provider/ContactsContract.FullNameStyle.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WESTERN](../android/provider/ContactsContract.FullNameStyle.md) <br /> |
| --- | --- |

## Constants

### CHINESE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHINESE: Int
```  

 Value: 3

### CJK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CJK: Int
```

Used if the name is written in Hanzi/Kanji/Hanja and we could not determine which specific language it belongs to: Chinese, Japanese or Korean. 

 Value: 2

### JAPANESE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JAPANESE: Int
```  

 Value: 4

### KOREAN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KOREAN: Int
```  

 Value: 5

### UNDEFINED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDEFINED: Int
```  

 Value: 0

### WESTERN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WESTERN: Int
```  

 Value: 1

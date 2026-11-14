# ContactsContract.FullNameStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FullNameStyle

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.FullNameStyle "View this page in Java") 

```
interface FullNameStyle
```

| [android.provider.ContactsContract.FullNameStyle](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#) |

Constants for various styles of combining given name, family name etc into a full name. For example, the western tradition follows the pattern 'given name' 'middle name' 'family name' with the alternative pattern being 'family name', 'given name' 'middle name'. The CJK tradition is 'family name' 'middle name' 'given name', with Japanese favoring a space between the names and Chinese omitting the space.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHINESE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#CHINESE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CJK](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#CJK:kotlin.Int) Used if the name is written in Hanzi/Kanji/Hanja and we could not determine which specific language it belongs to: Chinese, Japanese or Korean. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JAPANESE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#JAPANESE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KOREAN](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#KOREAN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDEFINED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#UNDEFINED:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WESTERN](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.FullNameStyle#WESTERN:kotlin.Int) <br /> |

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

# ContactsContract.PhoneticNameStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PhoneticNameStyle

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.PhoneticNameStyle "View this page in Java") 

```
interface PhoneticNameStyle
```

| [android.provider.ContactsContract.PhoneticNameStyle](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle#) |

Constants for various styles of capturing the pronunciation of a person's name.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JAPANESE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle#JAPANESE:kotlin.Int) Hiragana and Katakana are two common styles of writing out the pronunciation of a Japanese names. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [KOREAN](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle#KOREAN:kotlin.Int) Hangul is the Korean phonetic alphabet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PINYIN](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle#PINYIN:kotlin.Int) Pinyin is a phonetic method of entering Chinese characters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDEFINED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.PhoneticNameStyle#UNDEFINED:kotlin.Int) <br /> |

## Constants

### JAPANESE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JAPANESE: Int
```

Hiragana and Katakana are two common styles of writing out the pronunciation of a Japanese names. 

 Value: 4

### KOREAN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KOREAN: Int
```

Hangul is the Korean phonetic alphabet. 

 Value: 5

### PINYIN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PINYIN: Int
```

Pinyin is a phonetic method of entering Chinese characters. Typically not explicitly shown in UIs, but used for searches and sorting. 

 Value: 3

### UNDEFINED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDEFINED: Int
```  

 Value: 0

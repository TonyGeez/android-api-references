# ContactsContract.DisplayNameSources

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayNameSources

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.DisplayNameSources "View this page in Java") 
| --- | --- |

```
interface DisplayNameSources
```

| [android.provider.ContactsContract.DisplayNameSources](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#) |

Types of data used to produce the display name for a contact. In the order of increasing priority: [EMAIL](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#EMAIL:kotlin.Int), [PHONE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#PHONE:kotlin.Int), [ORGANIZATION](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#ORGANIZATION:kotlin.Int), [NICKNAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#NICKNAME:kotlin.Int), [STRUCTURED_PHONETIC_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#STRUCTURED_PHONETIC_NAME:kotlin.Int), [STRUCTURED_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#STRUCTURED_NAME:kotlin.Int).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMAIL](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#EMAIL:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NICKNAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#NICKNAME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORGANIZATION](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#ORGANIZATION:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHONE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#PHONE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STRUCTURED_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#STRUCTURED_NAME:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STRUCTURED_PHONETIC_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#STRUCTURED_PHONETIC_NAME:kotlin.Int) Display name comes from a structured name that only has phonetic components. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDEFINED](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DisplayNameSources#UNDEFINED:kotlin.Int) <br /> |

## Constants

### EMAIL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMAIL: Int
```  

 Value: 10

### NICKNAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NICKNAME: Int
```  

 Value: 35

### ORGANIZATION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORGANIZATION: Int
```  

 Value: 30

### PHONE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHONE: Int
```  

 Value: 20

### STRUCTURED_NAME

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRUCTURED_NAME: Int
```  

 Value: 40

### STRUCTURED_PHONETIC_NAME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STRUCTURED_PHONETIC_NAME: Int
```

Display name comes from a structured name that only has phonetic components. 

 Value: 37

### UNDEFINED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNDEFINED: Int
```  

 Value: 0

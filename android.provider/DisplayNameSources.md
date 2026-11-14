# ContactsContract.DisplayNameSources

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayNameSources

Kotlin| [Java](../android/provider/ContactsContract.DisplayNameSources.md) 
| --- | --- |

```
interface DisplayNameSources
```

| [android.provider.ContactsContract.DisplayNameSources](../android/provider/ContactsContract.DisplayNameSources.md) |

Types of data used to produce the display name for a contact. In the order of increasing priority: [EMAIL](../android/provider/ContactsContract.DisplayNameSources.md), [PHONE](../android/provider/ContactsContract.DisplayNameSources.md), [ORGANIZATION](../android/provider/ContactsContract.DisplayNameSources.md), [NICKNAME](../android/provider/ContactsContract.DisplayNameSources.md), [STRUCTURED_PHONETIC_NAME](../android/provider/ContactsContract.DisplayNameSources.md), [STRUCTURED_NAME](../android/provider/ContactsContract.DisplayNameSources.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EMAIL](../android/provider/ContactsContract.DisplayNameSources.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NICKNAME](../android/provider/ContactsContract.DisplayNameSources.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORGANIZATION](../android/provider/ContactsContract.DisplayNameSources.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHONE](../android/provider/ContactsContract.DisplayNameSources.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STRUCTURED_NAME](../android/provider/ContactsContract.DisplayNameSources.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STRUCTURED_PHONETIC_NAME](../android/provider/ContactsContract.DisplayNameSources.md) Display name comes from a structured name that only has phonetic components. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNDEFINED](../android/provider/ContactsContract.DisplayNameSources.md) <br /> |

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

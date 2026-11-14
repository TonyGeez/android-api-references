# Collator.ReorderCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReorderCodes

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/Collator.ReorderCodes "View this page in Java") 
| --- | --- |

```
interface ReorderCodes
```

| [android.icu.text.Collator.ReorderCodes](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#) |

Reordering codes for non-script groups that can be reordered under collation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#CURRENCY:kotlin.Int) Characters with the currency property. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#DEFAULT:kotlin.Int) A special reordering code that is used to specify the default reordering codes for a locale. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DIGIT](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#DIGIT:kotlin.Int) Characters with the digit property. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIRST](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#FIRST:kotlin.Int) The first entry in the enumeration of reordering groups. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONE](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#NONE:kotlin.Int) A special reordering code that is used to specify no reordering codes. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OTHERS](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#OTHERS:kotlin.Int) A special reordering code that is used to specify all other codes used for reordering except for the codes listed as ReorderingCodes and those listed explicitly in a reordering. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PUNCTUATION](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#PUNCTUATION:kotlin.Int) Characters with the punctuation property. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPACE](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#SPACE:kotlin.Int) Characters with the space property. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYMBOL](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#SYMBOL:kotlin.Int) Characters with the symbol property. |
| --- | --- |

## Constants

### CURRENCY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY: Int
```

Characters with the currency property. This is equivalent to the rule value "currency". 

 Value: 4099

### DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: Int
```

A special reordering code that is used to specify the default reordering codes for a locale. 

 Value: -1

### DIGIT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DIGIT: Int
```

Characters with the digit property. This is equivalent to the rule value "digit". 

 Value: 4100

### FIRST

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIRST: Int
```

The first entry in the enumeration of reordering groups. This is intended for use in range checking and enumeration of the reorder codes. 

 Value: 4096

### NONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONE: Int
```

A special reordering code that is used to specify no reordering codes. 

 Value: 103

### OTHERS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OTHERS: Int
```

A special reordering code that is used to specify all other codes used for reordering except for the codes listed as ReorderingCodes and those listed explicitly in a reordering. 

 Value: 103

### PUNCTUATION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PUNCTUATION: Int
```

Characters with the punctuation property. This is equivalent to the rule value "punct". 

 Value: 4097

### SPACE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPACE: Int
```

Characters with the space property. This is equivalent to the rule value "space". 

 Value: 4096

### SYMBOL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYMBOL: Int
```

Characters with the symbol property. This is equivalent to the rule value "symbol". 

 Value: 4098

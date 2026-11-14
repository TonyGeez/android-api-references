# CollationKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollationKey

```
abstract class CollationKey : Comparable<CollationKey!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.text.CollationKey](https://developer.android.com/reference/kotlin/java/text/CollationKey#) |

A`CollationKey`represents a`String`under the rules of a specific`Collator`object. Comparing two`CollationKey`s returns the relative order of the`String`s they represent. Using`CollationKey`s to compare`String`s is generally faster than using`Collator.compare`. Thus, when the`String`s must be compared multiple times, for example when sorting a list of`String`s. It's more efficient to use`CollationKey`s.

You can not create`CollationKey`s directly. Rather, generate them by calling`Collator.getCollationKey`. You can only compare`CollationKey`s generated from the same`Collator`object.

Generating a`CollationKey`for a`String`involves examining the entire`String`and converting it to series of bits that can be compared bitwise. This allows fast comparisons once the keys are generated. The cost of generating keys is recouped in faster comparisons when`String`s need to be compared many times. On the other hand, the result of a comparison is often determined by the first couple of characters of each`String`.`Collator.compare`examines only as many characters as it needs which allows it to be faster when doing single comparisons.

The following example shows how`CollationKey`s might be used to sort a list of`String`s. 

```kotlin
<code>// Create an array of CollationKeys for the Strings to be sorted.
  Collator myCollator = Collator.getInstance();
  CollationKey[] keys = new CollationKey[3];
  keys[0] = myCollator.getCollationKey("Tom");
  keys[1] = myCollator.getCollationKey("Dick");
  keys[2] = myCollator.getCollationKey("Harry");
  sort(keys);
 
  //...
 
  // Inside body of sort routine, compare keys this way
  if (keys[i].compareTo(keys[j]) &gt; 0)
     // swap keys[i] and keys[j]
 
  //...
 
  // Finally, when we've returned from sort.
  System.out.println(keys[0].getSourceString());
  System.out.println(keys[1].getSourceString());
  System.out.println(keys[2].getSourceString());
  </code>
```

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CollationKey](https://developer.android.com/reference/kotlin/java/text/CollationKey#CollationKey(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` CollationKey constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/java/text/CollationKey#compareTo(java.text.CollationKey))`(`other:` ` [CollationKey](https://developer.android.com/reference/kotlin/java/text/CollationKey#)!`)` Compare this CollationKey to the target CollationKey. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSourceString](https://developer.android.com/reference/kotlin/java/text/CollationKey#getSourceString())`()` Returns the String that this CollationKey represents. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](https://developer.android.com/reference/kotlin/java/text/CollationKey#toByteArray())`()` Converts the CollationKey to a sequence of bits. |

## Protected constructors

### CollationKey

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CollationKey(source: String!)
```

CollationKey constructor.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source string |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`source`is null |

## Public methods

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compareTo(other: CollationKey!): Int
```

Compare this CollationKey to the target CollationKey. The collation rules of the Collator object which created these keys are applied.**Note:**CollationKeys created by different Collators can not be compared.

| Parameters ||
|----------|----------------------------|
| `o` | the object to be compared. |
| `target` | target CollationKey |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns an integer value. Value is less than zero if this is less than target, value is zero if this and target are equal and value is greater than zero if this is greater than target. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

**See Also**

### getSourceString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSourceString(): String!
```

Returns the String that this CollationKey represents.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the source string of this CollationKey |

### toByteArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toByteArray(): ByteArray!
```

Converts the CollationKey to a sequence of bits. If two CollationKeys could be legitimately compared, then one could compare the byte arrays for each of those keys to obtain the same result. Byte arrays are organized most significant byte first.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array representation of the CollationKey |

# AlphabeticIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlphabeticIndex

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/AlphabeticIndex "View this page in Java") 
| --- | --- |

```
class AlphabeticIndex<V : Any!> : MutableIterable<AlphabeticIndex.Bucket<V>!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#) |

AlphabeticIndex supports the creation of a UI index appropriate for a given language. It can support either direct use, or use with a client that doesn't support localized collation. The following is an example of what an index might look like in a UI: 

```kotlin
<b>... A B C D E F G H I J K L M N O P Q R S T U V W X Y Z  ...</b><b>A</b>Addison
      Albertson
      Azensky
   <b>B</b>Baecker
   ...
  
```
The class can generate a list of labels for use as a UI "index", that is, a list of clickable characters (or character sequences) that allow the user to see a segment (bucket) of a larger "target" list. That is, each label corresponds to a bucket in the target list, where everything in the bucket is greater than or equal to the character (according to the locale's collation). Strings can be added to the index; they will be in sorted order in the right bucket.

<br />

The class also supports having buckets for strings before the first (underflow), after the last (overflow), and between scripts (inflow). For example, if the index is constructed with labels for Russian and English, Greek characters would fall into an inflow bucket between the other two scripts.

*Note:*If you expect to have a lot of ASCII or Latin characters as well as characters from the user's language, then it is a good idea to call addLabels(ULocale.English).

## Direct Use

The following shows an example of building an index directly. The "show..." methods below are just to illustrate usage. 

```kotlin
// Create a simple index where the values for the strings are Integers, and add the strings
 
  AlphabeticIndex<Integer> index = new AlphabeticIndex<Integer>(desiredLocale).addLabels(additionalLocale);
  int counter = 0;
  for (String item : test) {
      index.addRecord(item, counter++);
  }
  ...
  // Show index at top. We could skip or gray out empty buckets
 
  for (AlphabeticIndex.Bucket<Integer> bucket : index) {
      if (showAll || bucket.size() != 0) {
          showLabelAtTop(UI, bucket.getLabel());
      }
  }
   ...
  // Show the buckets with their contents, skipping empty buckets
 
  for (AlphabeticIndex.Bucket<Integer> bucket : index) {
      if (bucket.size() != 0) {
          showLabelInList(UI, bucket.getLabel());
          for (AlphabeticIndex.Record<Integer> item : bucket) {
              showIndexedItem(UI, item.getName(), item.getData());
          }
  
```
The caller can build different UIs using this class. For example, an index character could be omitted or grayed-out if its bucket is empty. Small buckets could also be combined based on size, such as: 

```kotlin
<b>... A-F G-N O-Z ...</b>
```

## Client Support

Callers can also use the [AlphabeticIndex.ImmutableIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.ImmutableIndex), or the AlphabeticIndex itself, to support sorting on a client that doesn't support AlphabeticIndex functionality.

The ImmutableIndex is both immutable and thread-safe. The corresponding AlphabeticIndex methods are not thread-safe because they "lazily" build the index buckets.

- ImmutableIndex.getBucket(index) provides random access to all buckets and their labels and label types.
- AlphabeticIndex.getBucketLabels() or the bucket iterator on either class can be used to get a list of the labels, such as "...", "A", "B",..., and send that list to the client.
- When the client has a new name, it sends that name to the server. The server needs to call the following methods, and communicate the bucketIndex and collationKey back to the client. 

  ```kotlin
  int bucketIndex = index.getBucketIndex(name);
    String label = immutableIndex.getBucket(bucketIndex).getLabel();  // optional
    RawCollationKey collationKey = collator.getRawCollationKey(name, null);
    
  ```
- The client would put the name (and associated information) into its bucket for bucketIndex. The collationKey is a sequence of bytes that can be compared with a binary compare, and produce the right localized result.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Bucket](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.Bucket) An index "bucket" with a label string and type. |
| | [ImmutableIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.ImmutableIndex) Immutable, thread-safe version of [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#). |
| | [Record](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.Record) A (name, data) pair, to be sorted by name into one of the index buckets. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#AlphabeticIndex(android.icu.text.RuleBasedCollator))`(`collator:` ` [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator)!`)` Create an AlphabeticIndex that uses a specific collator. |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#AlphabeticIndex(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Create the index object. |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#AlphabeticIndex(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Create the index object. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [addLabels](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#addLabels(android.icu.text.UnicodeSet))`(`additions:` ` [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!`)` Add more index characters (aside from what are in the locale) |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [addLabels](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#addLabels(android.icu.util.ULocale))`(`vararg` `additions:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Add more index characters (aside from what are in the locale) |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [addLabels](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#addLabels(java.util.Locale))`(`vararg` `additions:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Add more index characters (aside from what are in the locale) |
| --- | --- |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [addRecord](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#addRecord(kotlin.CharSequence,%20android.icu.text.AlphabeticIndex.V))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `data:` `V`)` Add a record (name and data) to the index. |
| [AlphabeticIndex.ImmutableIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.ImmutableIndex)\<V\>! | [buildImmutableIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#buildImmutableIndex())`()` Builds an immutable, thread-safe version of this instance, without data records. |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [clearRecords](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#clearRecords())`()` Clear the index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBucketCount](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getBucketCount())`()` Return the number of buckets in the index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBucketIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getBucketIndex(kotlin.CharSequence))`(`name:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Get the bucket number for the given name. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getBucketLabels](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getBucketLabels())`()` Get the labels. |
| --- | --- |
| [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator)! | [getCollator](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getCollator())`()` Get a clone of the collator used internally. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInflowLabel](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getInflowLabel())`()` Get the default label used for abbreviated buckets*between*other labels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxLabelCount](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getMaxLabelCount())`()` Get the limit on the number of labels in the index. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOverflowLabel](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getOverflowLabel())`()` Get the default label used in the IndexCharacters' locale for overflow, eg the first item in: . |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRecordCount](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getRecordCount())`()` Return the number of records in the index: that is, the total number of distinct \<name,data\> pairs added with addRecord(...), over all the buckets. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUnderflowLabel](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#getUnderflowLabel())`()` Get the default label used in the IndexCharacters' locale for underflow, eg the last item in: X Y Z . |
| --- | --- |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [AlphabeticIndex.Bucket](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.Bucket)\<V\>!\> | [iterator](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#iterator())`()` Return an iterator over the buckets. |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [setInflowLabel](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#setInflowLabel(kotlin.String))`(`inflowLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the inflowLabel label |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [setMaxLabelCount](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#setMaxLabelCount(kotlin.Int))`(`maxLabelCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set a limit on the number of labels in the index. |
| --- | --- |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [setOverflowLabel](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#setOverflowLabel(kotlin.String))`(`overflowLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the overflow label |
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)\<V\>! | [setUnderflowLabel](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#setUnderflowLabel(kotlin.String))`(`underflowLabel:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the underflowLabel label |

## Public constructors

### AlphabeticIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AlphabeticIndex(collator: RuleBasedCollator!)
```

Create an AlphabeticIndex that uses a specific collator.

The index will be created with no labels; the addLabels() function must be called after creation to add the desired labels to the index.

The index will work directly with the supplied collator. If the caller will need to continue working with the collator it should be cloned first, so that the collator provided to the AlphabeticIndex remains unchanged after creation of the index.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `collator` | [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator)!:The collator to use to order the contents of this index. |

### AlphabeticIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AlphabeticIndex(locale: ULocale!)
```

Create the index object.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale for the index. |

### AlphabeticIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AlphabeticIndex(locale: Locale!)
```

Create the index object.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The locale for the index. |

## Public methods

### addLabels

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addLabels(additions: UnicodeSet!): AlphabeticIndex<V>!
```

Add more index characters (aside from what are in the locale)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `additions` | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!:additional characters to add to the index, such as A-Z. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### addLabels

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addLabels(vararg additions: ULocale!): AlphabeticIndex<V>!
```

Add more index characters (aside from what are in the locale)

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `additions` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:additional characters to add to the index, such as those in Swedish. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### addLabels

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addLabels(vararg additions: Locale!): AlphabeticIndex<V>!
```

Add more index characters (aside from what are in the locale)

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `additions` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:additional characters to add to the index, such as those in Swedish. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### addRecord

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addRecord(
    name: CharSequence!, 
    data: V
): AlphabeticIndex<V>!
```

Add a record (name and data) to the index. The name will be used to sort the items into buckets, and to sort within the bucket. Two records may have the same name. When they do, the sort order is according to the order added: the first added comes first.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Name, such as a name |
| `data` | V:Data, such as an address or link |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### buildImmutableIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun buildImmutableIndex(): AlphabeticIndex.ImmutableIndex<V>!
```

Builds an immutable, thread-safe version of this instance, without data records.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [AlphabeticIndex.ImmutableIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.ImmutableIndex)<V>! | an immutable index instance |

### clearRecords

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearRecords(): AlphabeticIndex<V>!
```

Clear the index.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### getBucketCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBucketCount(): Int
```

Return the number of buckets in the index. This will be the same as the number of labels, plus buckets for the underflow, overflow, and inflow(s).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | number of buckets |

### getBucketIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBucketIndex(name: CharSequence!): Int
```

Get the bucket number for the given name. This routine permits callers to implement their own bucket handling mechanisms, including client-server handling. For example, when a new name is created on the client, it can ask the server for the bucket for that name, and the sortkey (using getCollator). Once the client has that information, it can put the name into the right bucket, and sort it within that bucket, without having access to the index or collator.

Note that the bucket number (and sort key) are only valid for the settings of the current AlphabeticIndex; if those are changed, then the bucket number and sort key must be regenerated.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `name` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:Name, such as a name |

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the bucket index for the name |

### getBucketLabels

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBucketLabels(): MutableList<String!>!
```

Get the labels.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The list of bucket labels, after processing. |

### getCollator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCollator(): RuleBasedCollator!
```

Get a clone of the collator used internally. Note that for performance reasons, the clone is only done once, and then stored. The next time it is accessed, the same instance is returned.

***Don't use this method across threads if you are changing the settings on the collator, at least not without synchronizing.***

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator)! | a clone of the collator used internally |

### getInflowLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInflowLabel(): String!
```

Get the default label used for abbreviated buckets*between*other labels. For example, consider the labels for Latin and Greek are used: X Y Z ... Α Β Γ.

| Return ||
|-----------------------------------------------------------------------------------|--------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | inflow label |

### getMaxLabelCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxLabelCount(): Int
```

Get the limit on the number of labels in the index. The number of buckets can be slightly larger: see getBucketCount().

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | maxLabelCount maximum number of labels. |

### getOverflowLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOverflowLabel(): String!
```

Get the default label used in the IndexCharacters' locale for overflow, eg the first item in: ... A B C

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | overflow label |

### getRecordCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRecordCount(): Int
```

Return the number of records in the index: that is, the total number of distinct \<name,data\> pairs added with addRecord(...), over all the buckets.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | total number of records in buckets |

### getUnderflowLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnderflowLabel(): String!
```

Get the default label used in the IndexCharacters' locale for underflow, eg the last item in: X Y Z ...

| Return ||
|-----------------------------------------------------------------------------------|-----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | underflow label |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun iterator(): MutableIterator<AlphabeticIndex.Bucket<V>!>
```

Return an iterator over the buckets.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [AlphabeticIndex.Bucket](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex.Bucket)<V>!> | iterator over buckets. |

### setInflowLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInflowLabel(inflowLabel: String!): AlphabeticIndex<V>!
```

Set the inflowLabel label

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `inflowLabel` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:see class description |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### setMaxLabelCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMaxLabelCount(maxLabelCount: Int): AlphabeticIndex<V>!
```

Set a limit on the number of labels in the index. The number of buckets can be slightly larger: see getBucketCount().

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxLabelCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Set the maximum number of labels. Currently, if the number is exceeded, then every nth item is removed to bring the count down. A more sophisticated mechanism may be available in the future. |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### setOverflowLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOverflowLabel(overflowLabel: String!): AlphabeticIndex<V>!
```

Set the overflow label

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------|
| `overflowLabel` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:see class description |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

### setUnderflowLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setUnderflowLabel(underflowLabel: String!): AlphabeticIndex<V>!
```

Set the underflowLabel label

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------|
| `underflowLabel` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:see class description |

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex#)<V>! | this, for chaining |

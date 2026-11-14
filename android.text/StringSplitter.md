# TextUtils.StringSplitter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringSplitter

Kotlin| [Java](../android/text/TextUtils.StringSplitter.md) 
| --- | --- |

```
interface StringSplitter : MutableIterable<String!>
```

| [android.text.TextUtils.StringSplitter](../android/text/TextUtils.StringSplitter.md) |

| Known Direct Subclasses [TextUtils.SimpleStringSplitter](../android/text/TextUtils.SimpleStringSplitter.md) |------------------------------------------------------------------------------------------------------------------------------|---------------------------| | [TextUtils.SimpleStringSplitter](../android/text/TextUtils.SimpleStringSplitter.md) | A simple string splitter. | |
| --- | --- | --- | --- | --- | --- | --- |

An interface for splitting strings according to rules that are opaque to the user of this interface. This also has less overhead than split, which uses regular expressions and allocates an array to hold the results.

The most efficient way to use this class is: 

```kotlin
// Once
  TextUtils.StringSplitter splitter = new TextUtils.SimpleStringSplitter(delimiter);
 
  // Once per string to split
  splitter.setString(string);
  for (String s : splitter) {
      ...
  }
  
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](../android/text/TextUtils.StringSplitter.md))`(`string:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public methods

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(string: String!): Unit
```

# TextUtils.StringSplitter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringSplitter

Kotlin| [Java](https://developer.android.com/reference/android/text/TextUtils.StringSplitter "View this page in Java") 

```
interface StringSplitter : MutableIterable<String!>
```

| [android.text.TextUtils.StringSplitter](https://developer.android.com/reference/kotlin/android/text/TextUtils.StringSplitter#) |

| Known Direct Subclasses [TextUtils.SimpleStringSplitter](https://developer.android.com/reference/kotlin/android/text/TextUtils.SimpleStringSplitter) |------------------------------------------------------------------------------------------------------------------------------|---------------------------| | [TextUtils.SimpleStringSplitter](https://developer.android.com/reference/kotlin/android/text/TextUtils.SimpleStringSplitter) | A simple string splitter. | |

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
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setString](https://developer.android.com/reference/kotlin/android/text/TextUtils.StringSplitter#setString(kotlin.String))`(`string:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public methods

### setString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setString(string: String!): Unit
```

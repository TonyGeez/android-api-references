# TestTarget

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestTarget

```
@Target([AnnotationTarget.ANNOTATION_CLASS]) class TestTarget
```

| [dalvik.annotation.TestTarget](../dalvik/annotation/TestTarget.md) |

| **This annotation was deprecated in API level 14.**
|
| Obsolete.

Defines an annotation used be used within the TestInfo annotation. It specifies a single method target for the test (but can be used multiple times).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TestTarget](../dalvik/annotation/TestTarget.md))`(`conceptName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `methodArgs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>>`, `methodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Defines an annotation used be used within the TestInfo annotation. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [conceptName](../dalvik/annotation/TestTarget.md) Specifies the name of a concept being tested. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)\<\*\>\> | [methodArgs](../dalvik/annotation/TestTarget.md) Specifies the signature of the method that is being tested, in terms of Java classes. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [methodName](../dalvik/annotation/TestTarget.md) Specifies the name of the method that is being tested. |
| --- | --- |

## Public constructors

### TestTarget

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestTarget(
    conceptName: String, 
    methodArgs: Array<KClass<*>>, 
    methodName: String)
```

**Deprecated:** *Obsolete.*

Defines an annotation used be used within the TestInfo annotation. It specifies a single method target for the test (but can be used multiple times).

## Properties

### conceptName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val conceptName: String
```

**Deprecated:** *Deprecated in Java.*

Specifies the name of a concept being tested. Use this if `methodName` is not accurate enough. E.g. for [java.util.regex.Pattern#compile(String)](../java/util/regex/Pattern.md)) `methodName` is not sufficient since the String contains a pattern with its own syntax which has to be tested with different aspects. Areas concerned are e.g. JDBC (SELECT, INSERT, UPDATE, DELETE, ...), regex (character sets, operators,...), formatters (DecimalFormat, DateFormat, ChoiceFormat, ...), ... 

### methodArgs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val methodArgs: Array<KClass<*>>
```

**Deprecated:** *Deprecated in Java.*

Specifies the signature of the method that is being tested, in terms of Java classes. 

### methodName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val methodName: String
```

**Deprecated:** *Deprecated in Java.*

Specifies the name of the method that is being tested.

# TestTargetClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestTargetClass

```
@Target([AnnotationTarget.CLASS, AnnotationTarget.FILE]) class TestTargetClass
```

| [dalvik.annotation.TestTargetClass](https://developer.android.com/reference/kotlin/dalvik/annotation/TestTargetClass#) |

| **This annotation was deprecated in API level 14.**
|
| Obsolete.

Defines an annotation for test classes that allows to link them to the class that is being tested. The current assumption is that the test are somewhat organized according to the API classes they test. Might be too strict for some cases.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TestTargetClass](https://developer.android.com/reference/kotlin/dalvik/annotation/TestTargetClass#TestTargetClass(kotlin.reflect.KClass))`(`value:` ` [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<*>`)` Defines an annotation for test classes that allows to link them to the class that is being tested. |

| Properties ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)\<\*\> | [value](https://developer.android.com/reference/kotlin/dalvik/annotation/TestTargetClass#value:kotlin.reflect.KClass) Specifies the class being tested. |

## Public constructors

### TestTargetClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestTargetClass(value: KClass<*>)
```

**Deprecated:** *Obsolete.*

Defines an annotation for test classes that allows to link them to the class that is being tested. The current assumption is that the test are somewhat organized according to the API classes they test. Might be too strict for some cases.

## Properties

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: KClass<*>
```

**Deprecated:** *Deprecated in Java.*

Specifies the class being tested.

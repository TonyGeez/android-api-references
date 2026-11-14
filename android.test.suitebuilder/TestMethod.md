# TestMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestMethod

Kotlin| [Java](https://developer.android.com/reference/android/test/suitebuilder/TestMethod "View this page in Java") 
| --- | --- |

```
open class TestMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.suitebuilder.TestMethod](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#) |

| **This class was deprecated in API level 26.**
|
| New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Represents a test to be run. Can be constructed without instantiating the TestCase or even loading the class.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TestMethod](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#TestMethod(java.lang.reflect.Method,%20java.lang.Class))`(`method:` ` [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method.html#)!`, `enclosingClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` `TestCase!>!`)` <br /> |
| [TestMethod](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#TestMethod(kotlin.String,%20java.lang.Class))`(`methodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `enclosingClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` `TestCase!>!`)` <br /> |
| [TestMethod](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#TestMethod(TestCase))`(`testCase:` `TestCase!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openTestCase! | [createTest](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#createTest())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| openT | [getAnnotation](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#getAnnotation(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`)` <br /> |
| --- | --- |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<outTestCase!\>! | [getEnclosingClass](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#getEnclosingClass())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getEnclosingClassname](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#getEnclosingClassname())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#getName())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#hashCode())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestMethod#toString())`()` <br /> |

## Public constructors

### TestMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestMethod(
    method: Method!, 
    enclosingClass: Class<out TestCase!>!)
```  

### TestMethod

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestMethod(
    methodName: String!, 
    enclosingClass: Class<out TestCase!>!)
```  

### TestMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestMethod(testCase: TestCase!)
```

## Public methods

### createTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createTest(): TestCase!
```

**Deprecated:** *Deprecated in Java.* 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Annotation!> getAnnotation(annotationClass: Class<T>!): T
```

**Deprecated:** *Deprecated in Java.* 

### getEnclosingClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnclosingClass(): Class<out TestCase!>!
```

**Deprecated:** *Deprecated in Java.* 

### getEnclosingClassname

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnclosingClassname(): String!
```

**Deprecated:** *Deprecated in Java.* 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

**Deprecated:** *Deprecated in Java.* 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

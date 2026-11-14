# TestSuiteBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestSuiteBuilder

Kotlin| [Java](TestSuiteBuilder.md) 
| --- | --- |

```
open class TestSuiteBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.suitebuilder.TestSuiteBuilder](TestSuiteBuilder.md) |

| Known Direct Subclasses [UnitTestSuiteBuilder](UnitTestSuiteBuilder.md) |-----------------------------------------------------------------------------------------------------------------------|----------------------------------------| | [UnitTestSuiteBuilder](UnitTestSuiteBuilder.md) | A suite builder that finds unit tests. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 26.**
|
| New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Build suites based on a combination of included packages, excluded packages, and predicates that must be satisfied.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [FailedToCreateTests](../android/test/suitebuilder/TestSuiteBuilder.FailedToCreateTests.md) A special junit. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TestSuiteBuilder](TestSuiteBuilder.md))`(`clazz:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` The given name is automatically prefixed with the package containing the tests to be run. |
| [TestSuiteBuilder](TestSuiteBuilder.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TestSuite! | [build](TestSuiteBuilder.md))`()` Call this method once you've configured your builder as desired. |
| open [TestSuiteBuilder](TestSuiteBuilder.md)! | [excludePackages](TestSuiteBuilder.md))`(`vararg` `packageNames:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Exclude all tests in the given packages and all sub-packages, unless otherwise specified. |
| [TestSuiteBuilder](TestSuiteBuilder.md)! | [includeAllPackagesUnderHere](TestSuiteBuilder.md))`()` Include all junit tests that satisfy the requirements in the calling class' package and all sub-packages. |
| --- | --- |
| open [TestSuiteBuilder](TestSuiteBuilder.md)! | [includePackages](TestSuiteBuilder.md))`(`vararg` `packageNames:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Include all tests that satisfy the requirements in the given packages and all sub-packages, unless otherwise specified. |
| open [TestSuiteBuilder](TestSuiteBuilder.md)! | [named](TestSuiteBuilder.md))`(`newSuiteName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Override the default name for the suite being built. |

| Protected methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSuiteName](TestSuiteBuilder.md))`()` Subclasses use this method to determine the name of the suite. |

## Public constructors

### TestSuiteBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestSuiteBuilder(clazz: Class<Any!>!)
```

The given name is automatically prefixed with the package containing the tests to be run. If more than one package is specified, the first is used.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clazz` | [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Use the class from your .apk. Use the class name for the test suite name. Use the class' classloader in order to load classes for testing. This is needed when running in the emulator. |

### TestSuiteBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TestSuiteBuilder(
    name: String!, 
    classLoader: ClassLoader!)
```

## Public methods

### build

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun build(): TestSuite!
```

**Deprecated:** *Deprecated in Java.*

Call this method once you've configured your builder as desired.

| Return ||
|------------|-------------------------------------------|
| TestSuite! | The suite containing the requested tests. |

### excludePackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun excludePackages(vararg packageNames: String!): TestSuiteBuilder!
```

**Deprecated:** *Deprecated in Java.*

Exclude all tests in the given packages and all sub-packages, unless otherwise specified.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------|
| `packageNames` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Names of packages to remove. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [TestSuiteBuilder](TestSuiteBuilder.md)! | The builder for method chaining. |

### includeAllPackagesUnderHere

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun includeAllPackagesUnderHere(): TestSuiteBuilder!
```

**Deprecated:** *Deprecated in Java.*

Include all junit tests that satisfy the requirements in the calling class' package and all sub-packages.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [TestSuiteBuilder](TestSuiteBuilder.md)! | The builder for method chaining. |

### includePackages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun includePackages(vararg packageNames: String!): TestSuiteBuilder!
```

**Deprecated:** *Deprecated in Java.*

Include all tests that satisfy the requirements in the given packages and all sub-packages, unless otherwise specified.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------|
| `packageNames` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Names of packages to add. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [TestSuiteBuilder](TestSuiteBuilder.md)! | The builder for method chaining. |

### named

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun named(newSuiteName: String!): TestSuiteBuilder!
```

**Deprecated:** *Deprecated in Java.*

Override the default name for the suite being built. This should generally be called if you call`addRequirements(com.android.internal.util.Predicate[])`to make it clear which tests will be included. The name you specify is automatically prefixed with the package containing the tests to be run. If more than one package is specified, the first is used.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| `newSuiteName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Prefix of name to give the suite being built. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [TestSuiteBuilder](TestSuiteBuilder.md)! | The builder for method chaining. |

## Protected methods

### getSuiteName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getSuiteName(): String!
```

**Deprecated:** *Deprecated in Java.*

Subclasses use this method to determine the name of the suite.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The package and suite name combined. |

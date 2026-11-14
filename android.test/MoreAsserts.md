# MoreAsserts

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MoreAsserts

Kotlin| [Java](https://developer.android.com/reference/android/test/MoreAsserts "View this page in Java") 

```
class MoreAsserts
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.MoreAsserts](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#) |

| **This class was deprecated in API level 24.**
|
| Use [Hamcrest matchers](https://github.com/hamcrest) instead.

Contains additional assertion methods not found in JUnit.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertAssignableFrom](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertAssignableFrom(java.lang.Class,%20java.lang.Class))`(`expected:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`, `actual:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` Asserts that class`expected`is assignable from the class`actual`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertAssignableFrom](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertAssignableFrom(java.lang.Class,%20kotlin.Any))`(`expected:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`, `actual:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Asserts that the class`expected`is assignable from the object`actual`. |
| static [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult.html#)! | [assertContainsRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContainsRegex(kotlin.String,%20kotlin.String))`(`expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Variant of [assertContainsRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContainsRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. |
| static [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult.html#)! | [assertContainsRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContainsRegex(kotlin.String,%20kotlin.String,%20kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that`expectedRegex`matches any substring of`actual`and fails with`message`if it does not. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertContentsInAnyOrder](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContentsInAnyOrder(kotlin.collections.MutableIterable,%20kotlin.Any))`(`actual:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`, `vararg` `expected:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Variant of assertContentsInAnyOrder(String, Iterable, Object. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertContentsInAnyOrder](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContentsInAnyOrder(kotlin.String,%20kotlin.collections.MutableIterable,%20kotlin.Any))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`, `vararg` `expected:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Asserts that`actual`contains precisely the elements`expected`, but in any order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertContentsInOrder](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContentsInOrder(kotlin.collections.MutableIterable,%20kotlin.Any))`(`actual:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`, `vararg` `expected:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Variant of assertContentsInOrder(String, Iterable, Object. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertContentsInOrder](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContentsInOrder(kotlin.String,%20kotlin.collections.MutableIterable,%20kotlin.Any))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`, `vararg` `expected:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Asserts that`actual`contains precisely the elements`expected`, and in the same order. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.collections.MutableIterable))`(`iterable:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`)` Variant of [assertEmpty(java.lang.String,java.lang.Iterable)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.String,%20kotlin.collections.MutableIterable))using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.String,%20kotlin.collections.MutableIterable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `iterable:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`)` Asserts that`iterable`is empty. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.String,%20kotlin.collections.MutableMap))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<*,` `*>!`)` Asserts that`map`is empty. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.collections.MutableMap))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<*,` `*>!`)` Variant of [assertEmpty(java.lang.String,java.util.Map)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.String,%20kotlin.collections.MutableMap))using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.ByteArray,%20kotlin.ByteArray))`(`expected:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `actual:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Asserts that array`actual`is the same size and every element equals those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.DoubleArray,%20kotlin.DoubleArray))`(`expected:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`, `actual:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`)` Asserts that array`actual`is the same size and every element equals those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.IntArray,%20kotlin.IntArray))`(`expected:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `actual:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Asserts that array`actual`is the same size and every element equals those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.Array,%20kotlin.Array))`(`expected:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `actual:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Asserts that array`actual`is the same size and every element is the same as those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.String,%20kotlin.ByteArray,%20kotlin.ByteArray))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expected:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `actual:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Asserts that array`actual`is the same size and every element equals those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.String,%20kotlin.DoubleArray,%20kotlin.DoubleArray))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expected:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`, `actual:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`)` Asserts that array`actual`is the same size and every element equals those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.String,%20kotlin.IntArray,%20kotlin.IntArray))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expected:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `actual:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Asserts that array`actual`is the same size and every element equals those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.String,%20kotlin.Array,%20kotlin.Array))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expected:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `actual:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Asserts that array`actual`is the same size and every element is the same as those in array`expected`. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.String,%20kotlin.collections.MutableSet,%20kotlin.collections.MutableSet))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expected:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<*>!`, `actual:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<*>!`)` Asserts that two sets contain the same elements. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertEquals](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEquals(kotlin.collections.MutableSet,%20kotlin.collections.MutableSet))`(`expected:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<*>!`, `actual:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<*>!`)` Asserts that two sets contain the same elements. |
| static [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult.html#)! | [assertMatchesRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertMatchesRegex(kotlin.String,%20kotlin.String))`(`expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Variant of [assertMatchesRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertMatchesRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. |
| static [MatchResult](https://developer.android.com/reference/kotlin/java/util/regex/MatchResult.html#)! | [assertMatchesRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertMatchesRegex(kotlin.String,%20kotlin.String,%20kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that`expectedRegex`exactly matches`actual`and fails with`message`if it does not. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotContainsRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotContainsRegex(kotlin.String,%20kotlin.String))`(`expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Variant of [assertNotContainsRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotContainsRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotContainsRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotContainsRegex(kotlin.String,%20kotlin.String,%20kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that`expectedRegex`does not match any substring of`actual`, and fails with`message`if it does. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEmpty(kotlin.collections.MutableIterable))`(`iterable:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`)` Variant of assertNotEmpty(String, Iterable) using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEmpty(kotlin.String,%20kotlin.collections.MutableIterable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `iterable:` ` [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)<*>!`)` Asserts that`iterable`is not empty. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEmpty(kotlin.String,%20kotlin.collections.MutableMap))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<*,` `*>!`)` Asserts that`map`is not empty. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotEmpty](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEmpty(kotlin.collections.MutableMap))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<*,` `*>!`)` Variant of [assertNotEmpty(java.lang.String,java.util.Map)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEmpty(kotlin.String,%20kotlin.collections.MutableMap))using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotEqual](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEqual(kotlin.Any,%20kotlin.Any))`(`unexpected:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `actual:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Variant of [assertNotEqual(java.lang.String,java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEqual(kotlin.String,%20kotlin.Any,%20kotlin.Any))using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotEqual](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEqual(kotlin.String,%20kotlin.Any,%20kotlin.Any))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `unexpected:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `actual:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Asserts that`actual`is not equal`unexpected`, according to both`==`and [Object.equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotMatchesRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotMatchesRegex(kotlin.String,%20kotlin.String))`(`expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Variant of [assertNotMatchesRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotMatchesRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [assertNotMatchesRegex](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotMatchesRegex(kotlin.String,%20kotlin.String,%20kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `expectedRegex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actual:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Asserts that`expectedRegex`does not exactly match`actual`, and fails with`message`if it does. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkEqualsAndHashCodeMethods](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#checkEqualsAndHashCodeMethods(kotlin.Any,%20kotlin.Any,%20kotlin.Boolean))`(`lhs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `rhs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `expectedResult:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Variant of checkEqualsAndHashCodeMethods(String,Object,Object,boolean...)} using a generic message. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkEqualsAndHashCodeMethods](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#checkEqualsAndHashCodeMethods(kotlin.String,%20kotlin.Any,%20kotlin.Any,%20kotlin.Boolean))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `lhs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `rhs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `expectedResult:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Utility for testing equals() and hashCode() results at once. |

## Public methods

### assertAssignableFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertAssignableFrom(
    expected: Class<*>!, 
    actual: Class<*>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that class`expected`is assignable from the class`actual`. This verifies`expected`is a parent class or a interface that`actual`implements. 

### assertAssignableFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertAssignableFrom(
    expected: Class<*>!, 
    actual: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that the class`expected`is assignable from the object`actual`. This verifies`expected`is a parent class or a interface that`actual`implements. 

### assertContainsRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertContainsRegex(
    expectedRegex: String!, 
    actual: String!
): MatchResult!
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertContainsRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertContainsRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. 

### assertContainsRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertContainsRegex(
    message: String!, 
    expectedRegex: String!, 
    actual: String!
): MatchResult!
```

**Deprecated:** *Deprecated in Java.*

Asserts that`expectedRegex`matches any substring of`actual`and fails with`message`if it does not. The Matcher is returned in case the test needs access to any captured groups. Note that you can also use this for a literal string, by wrapping your expected string in [Pattern.quote](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#quote(kotlin.String)). 

### assertContentsInAnyOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertContentsInAnyOrder(
    actual: MutableIterable<*>!, 
    vararg expected: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of assertContentsInAnyOrder(String, Iterable, Object...) using a generic message. 

### assertContentsInAnyOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertContentsInAnyOrder(
    message: String!, 
    actual: MutableIterable<*>!, 
    vararg expected: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`actual`contains precisely the elements`expected`, but in any order. 

### assertContentsInOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertContentsInOrder(
    actual: MutableIterable<*>!, 
    vararg expected: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of assertContentsInOrder(String, Iterable, Object...) using a generic message. 

### assertContentsInOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertContentsInOrder(
    message: String!, 
    actual: MutableIterable<*>!, 
    vararg expected: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`actual`contains precisely the elements`expected`, and in the same order. 

### assertEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEmpty(iterable: MutableIterable<*>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertEmpty(java.lang.String,java.lang.Iterable)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.String,%20kotlin.collections.MutableIterable))using a generic message. 

### assertEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEmpty(
    message: String!, 
    iterable: MutableIterable<*>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`iterable`is empty. 

### assertEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEmpty(
    message: String!, 
    map: MutableMap<*, *>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`map`is empty. 

### assertEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEmpty(map: MutableMap<*, *>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertEmpty(java.lang.String,java.util.Map)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertEmpty(kotlin.String,%20kotlin.collections.MutableMap))using a generic message. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    expected: ByteArray!, 
    actual: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element equals those in array`expected`. On failure, message indicates specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    expected: DoubleArray!, 
    actual: DoubleArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element equals those in array`expected`. On failure, message indicates first specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    expected: IntArray!, 
    actual: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element equals those in array`expected`. On failure, message indicates first specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    expected: Array<Any!>!, 
    actual: Array<Any!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element is the same as those in array`expected`. Note that this uses`==`instead of`equals()`to compare the objects. On failure, message indicates first specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    message: String!, 
    expected: ByteArray!, 
    actual: ByteArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element equals those in array`expected`. On failure, message indicates specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    message: String!, 
    expected: DoubleArray!, 
    actual: DoubleArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element equals those in array`expected`. On failure, message indicates first specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    message: String!, 
    expected: IntArray!, 
    actual: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element equals those in array`expected`. On failure, message indicates first specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    message: String!, 
    expected: Array<Any!>!, 
    actual: Array<Any!>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that array`actual`is the same size and every element is the same as those in array`expected`. Note that this uses`equals()`instead of`==`to compare the objects.`null`will be considered equal to`null`(unlike SQL). On failure, message indicates first specific element mismatch. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    message: String!, 
    expected: MutableSet<*>!, 
    actual: MutableSet<*>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that two sets contain the same elements. 

### assertEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertEquals(
    expected: MutableSet<*>!, 
    actual: MutableSet<*>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that two sets contain the same elements. 

### assertMatchesRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertMatchesRegex(
    expectedRegex: String!, 
    actual: String!
): MatchResult!
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertMatchesRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertMatchesRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. 

### assertMatchesRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertMatchesRegex(
    message: String!, 
    expectedRegex: String!, 
    actual: String!
): MatchResult!
```

**Deprecated:** *Deprecated in Java.*

Asserts that`expectedRegex`exactly matches`actual`and fails with`message`if it does not. The MatchResult is returned in case the test needs access to any captured groups. Note that you can also use this for a literal string, by wrapping your expected string in [Pattern.quote](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#quote(kotlin.String)). 

### assertNotContainsRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotContainsRegex(
    expectedRegex: String!, 
    actual: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertNotContainsRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotContainsRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. 

### assertNotContainsRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotContainsRegex(
    message: String!, 
    expectedRegex: String!, 
    actual: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`expectedRegex`does not match any substring of`actual`, and fails with`message`if it does. Note that you can also use this for a literal string, by wrapping your expected string in [Pattern.quote](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#quote(kotlin.String)). 

### assertNotEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotEmpty(iterable: MutableIterable<*>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of assertNotEmpty(String, Iterable) using a generic message. 

### assertNotEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotEmpty(
    message: String!, 
    iterable: MutableIterable<*>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`iterable`is not empty. 

### assertNotEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotEmpty(
    message: String!, 
    map: MutableMap<*, *>!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`map`is not empty. 

### assertNotEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotEmpty(map: MutableMap<*, *>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertNotEmpty(java.lang.String,java.util.Map)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEmpty(kotlin.String,%20kotlin.collections.MutableMap))using a generic message. 

### assertNotEqual

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotEqual(
    unexpected: Any!, 
    actual: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertNotEqual(java.lang.String,java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotEqual(kotlin.String,%20kotlin.Any,%20kotlin.Any))using a generic message. 

### assertNotEqual

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotEqual(
    message: String!, 
    unexpected: Any!, 
    actual: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`actual`is not equal`unexpected`, according to both`==`and [Object.equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)). 

### assertNotMatchesRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotMatchesRegex(
    expectedRegex: String!, 
    actual: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of [assertNotMatchesRegex(java.lang.String,java.lang.String,java.lang.String)](https://developer.android.com/reference/kotlin/android/test/MoreAsserts#assertNotMatchesRegex(kotlin.String,%20kotlin.String,%20kotlin.String))using a generic message. 

### assertNotMatchesRegex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun assertNotMatchesRegex(
    message: String!, 
    expectedRegex: String!, 
    actual: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Asserts that`expectedRegex`does not exactly match`actual`, and fails with`message`if it does. Note that you can also use this for a literal string, by wrapping your expected string in [Pattern.quote](https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#quote(kotlin.String)). 

### checkEqualsAndHashCodeMethods

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun checkEqualsAndHashCodeMethods(
    lhs: Any!, 
    rhs: Any!, 
    expectedResult: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Variant of checkEqualsAndHashCodeMethods(String,Object,Object,boolean...)} using a generic message. 

### checkEqualsAndHashCodeMethods

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun checkEqualsAndHashCodeMethods(
    message: String!, 
    lhs: Any!, 
    rhs: Any!, 
    expectedResult: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Utility for testing equals() and hashCode() results at once. Tests that lhs.equals(rhs) matches expectedResult, as well as rhs.equals(lhs). Also tests that hashCode() return values are equal if expectedResult is true. (hashCode() is not tested if expectedResult is false, as unequal objects can have equal hashCodes.)

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `lhs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:An Object for which equals() and hashCode() are to be tested. |
| `rhs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:As lhs. |
| `expectedResult` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if the objects should compare equal, false if not. |

# PropertyPath

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions)

# PropertyPath

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/PropertyPath "View this page in Java") 
| --- | --- |

```
open class PropertyPath : MutableIterable<PropertyPath.PathSegment!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.PropertyPath](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#) |

Represents a property path returned from searching the AppSearch Database.

One of the use cases for this class is when searching the AppSearch Database for the snippet matching use case. In this case you will get back [SearchResult.MatchInfo](https://developer.android.com/reference/kotlin/android/app/appsearch/SearchResult.MatchInfo) objects that contain a property path signifying the location of a match within the database. This is a string that may look something like "foo.bar\[0\]". [PropertyPath](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#) parses this string and breaks it up into a List of [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) s. These may represent either a property or a property and a 0-based index into the property. For instance, "foo.bar\[1\]" would be parsed into a [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) with a property name of foo and a [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) with a property name of bar and an index of 1. This allows for easier manipulation of the property path.

This class won't perform any retrievals, it will only parse the path string. As such, it may not necessarily refer to a valid path in the database.

## Summary

| Nested classes ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) A segment of a PropertyPath, which includes the name of the property and a 0-based index into this property. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PropertyPath](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#PropertyPath(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructor that parses a string representing the path to populate a List of PathSegments |
| [PropertyPath](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#PropertyPath(kotlin.collections.MutableList))`(`pathList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PropertyPath.PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment)!>`)` Constructor directly accepting a path list |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [PropertyPath.PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) | [get](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#get(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) at a specified index of the PropertyPath. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#hashCode())`()` <br /> |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [PropertyPath.PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment)!\> | [iterator](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#iterator())`()` Returns an iterator over the PathSegments within the PropertyPath |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#size())`()` Returns the number of [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) s in the PropertyPath. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#toString())`()` Returns a valid path string representing this PropertyPath |
| --- | --- |

## Public constructors

### PropertyPath

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
PropertyPath(path: String)
```

Constructor that parses a string representing the path to populate a List of PathSegments

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be validated and parsed into PathSegments This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.IllegalArgumentException` | when the path is invalid or malformed |

### PropertyPath

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
PropertyPath(pathList: MutableList<PropertyPath.PathSegment!>)
```

Constructor directly accepting a path list

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pathList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PropertyPath.PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment)!\>:a list of PathSegments This value cannot be`null`. |

## Public methods

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### get

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun get(index: Int): PropertyPath.PathSegment
```

Returns the [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) at a specified index of the PropertyPath.

Calling`get(1)`on a [PropertyPath](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath#) representing "foo.bar\[1\]" will return a [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) representing "bar\[1\]". [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) s both with and without a property index of [PathSegment.NON_REPEATED_CARDINALITY](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment#NON_REPEATED_CARDINALITY:kotlin.Int) are retrieved the same.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position into the PropertyPath |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [PropertyPath.PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) | This value cannot be`null`. |

| Exceptions ||
|--------------------------------------------|------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | if index is not a valid index in the path list |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### iterator

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<PropertyPath.PathSegment!>
```

Returns an iterator over the PathSegments within the PropertyPath

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [PropertyPath.PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment)!> | This value cannot be`null`. |

### size

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun size(): Int
```

Returns the number of [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment) s in the PropertyPath.

Paths representing "foo.bar" and "foo\[1\].bar\[1\]" will have the same size, as a property and an index into that property are stored in one [PathSegment](https://developer.android.com/reference/kotlin/android/app/appsearch/PropertyPath.PathSegment). 

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a valid path string representing this PropertyPath

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

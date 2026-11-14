# EnumSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EnumSet

```
abstract class EnumSet<E : Enum<E>!> : AbstractSet<E>, Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> |||
| | ↳ | [java.util.AbstractSet](https://developer.android.com/reference/kotlin/java/util/AbstractSet)\<E\> ||
| | | ↳ | [java.util.EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#) |
| --- | --- | --- | --- |

A specialized [Set](https://developer.android.com/reference/kotlin/java/util/Set) implementation for use with enum types. All of the elements in an enum set must come from a single enum type that is specified, explicitly or implicitly, when the set is created. Enum sets are represented internally as bit vectors. This representation is extremely compact and efficient. The space and time performance of this class should be good enough to allow its use as a high-quality, typesafe alternative to traditional`int`-based "bit flags." Even bulk operations (such as`containsAll`and`retainAll`) should run very quickly if their argument is also an enum set.

The iterator returned by the`iterator`method traverses the elements in their*natural order* (the order in which the enum constants are declared). The returned iterator is*weakly consistent* : it will never throw [ConcurrentModificationException](https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException) and it may or may not show the effects of any modifications to the set that occur while the iteration is in progress.

Null elements are not permitted. Attempts to insert a null element will throw [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#). Attempts to test for the presence of a null element or to remove one will, however, function properly.

Like most collection implementations,`EnumSet`is not synchronized. If multiple threads access an enum set concurrently, and at least one of the threads modifies the set, it should be synchronized externally. This is typically accomplished by synchronizing on some object that naturally encapsulates the enum set. If no such object exists, the set should be "wrapped" using the [Collections.synchronizedSet](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedSet(kotlin.collections.MutableSet))method. This is best done at creation time, to prevent accidental unsynchronized access: 

```kotlin
Set<MyEnum> s = Collections.synchronizedSet(EnumSet.noneOf(MyEnum.class));
  
```

Implementation note: All basic operations execute in constant time. They are likely (though not guaranteed) to be much faster than their [HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet) counterparts. Even bulk operations execute in constant time if their argument is also an enum set.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [allOf](https://developer.android.com/reference/kotlin/java/util/EnumSet#allOf(java.lang.Class))`(`elementType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>!`)` Creates an enum set containing all of the elements in the specified element type. |
| open [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\> | [clone](https://developer.android.com/reference/kotlin/java/util/EnumSet#clone())`()` Returns a copy of this set. |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [complementOf](https://developer.android.com/reference/kotlin/java/util/EnumSet#complementOf(java.util.EnumSet))`(`s:` ` [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>!`)` Creates an enum set with the same element type as the specified enum set, initially containing all the elements of this type that are*not*contained in the specified set. |
| --- | --- |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [copyOf](https://developer.android.com/reference/kotlin/java/util/EnumSet#copyOf(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<E>!`)` Creates an enum set initialized from the specified collection. |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [copyOf](https://developer.android.com/reference/kotlin/java/util/EnumSet#copyOf(java.util.EnumSet))`(`s:` ` [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>!`)` Creates an enum set with the same element type as the specified enum set, initially containing the same elements (if any). |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [noneOf](https://developer.android.com/reference/kotlin/java/util/EnumSet#noneOf(java.lang.Class))`(`elementType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>!`)` Creates an empty enum set with the specified element type. |
| --- | --- |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [of](https://developer.android.com/reference/kotlin/java/util/EnumSet#of(java.util.EnumSet.of.E))`(`e:` `E`)` Creates an enum set initially containing the specified element. |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [of](https://developer.android.com/reference/kotlin/java/util/EnumSet#of(java.util.EnumSet.of.E,%20java.util.EnumSet.of.E))`(`e1:` `E`, `e2:` `E`)` Creates an enum set initially containing the specified elements. |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [of](https://developer.android.com/reference/kotlin/java/util/EnumSet#of(java.util.EnumSet.of.E,%20java.util.EnumSet.of.E,%20java.util.EnumSet.of.E))`(`e1:` `E`, `e2:` `E`, `e3:` `E`)` Creates an enum set initially containing the specified elements. |
| --- | --- |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [of](https://developer.android.com/reference/kotlin/java/util/EnumSet#of(java.util.EnumSet.of.E,%20java.util.EnumSet.of.E,%20java.util.EnumSet.of.E,%20java.util.EnumSet.of.E))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`)` Creates an enum set initially containing the specified elements. |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [of](https://developer.android.com/reference/kotlin/java/util/EnumSet#of(java.util.EnumSet.of.E,%20java.util.EnumSet.of.E,%20java.util.EnumSet.of.E,%20java.util.EnumSet.of.E,%20java.util.EnumSet.of.E))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`)` Creates an enum set initially containing the specified elements. |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [of](https://developer.android.com/reference/kotlin/java/util/EnumSet#of(java.util.EnumSet.of.E,%20java.util.EnumSet.of.E))`(`first:` `E`, `vararg` `rest:` `E`)` Creates an enum set initially containing the specified elements. |
| --- | --- |
| openstatic [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>! | [range](https://developer.android.com/reference/kotlin/java/util/EnumSet#range(java.util.EnumSet.range.E,%20java.util.EnumSet.range.E))`(`from:` `E`, `to:` `E`)` Creates an enum set initially containing all of the elements in the range defined by the two specified endpoints. |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#add(java.util.AbstractCollection.E))`(`element:` `E`)` <br /> Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.) Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added. If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), processing of its elements generally occurs in that order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#clear())`()` <br /> Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty())`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#iterator())`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray())`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString())`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). <br /> | ||
| From class [AbstractSet](https://developer.android.com/reference/kotlin/java/util/AbstractSet) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/util/AbstractSet#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares the specified object with this set for equality. Returns`true`if the given object is also a set, the two sets have the same size, and every member of the given set is contained in this set. This ensures that the`equals`method works properly across different implementations of the`Set`interface. This implementation first checks if the specified object is this set; if so it returns`true`. Then, it checks if the specified object is a set whose size is identical to the size of this set; if not, it returns false. If so, it returns`containsAll((Collection) o)`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/util/AbstractSet#hashCode())`()` <br /> Returns the hash code value for this set. The hash code of a set is defined to be the sum of the hash codes of the elements in the set, where the hash code of a`null`element is defined to be zero. This ensures that`s1.equals(s2)`implies that`s1.hashCode()==s2.hashCode()`for any two sets`s1`and`s2`, as required by the general contract of [Object.hashCode](https://developer.android.com/reference/kotlin/java/lang/Object.html#hashCode()). This implementation iterates over the set, calling the`hashCode`method on each element in the set, and adding up the results. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/AbstractSet#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes from this set all of its elements that are contained in the specified collection (optional operation). If the specified collection is also a set, this operation effectively modifies this set so that its value is the*asymmetric set difference*of the two sets. This implementation determines which is the smaller of this set and the specified collection, by invoking the`size`method on each. If this set has fewer elements, then the implementation iterates over this set, checking each element returned by the iterator in turn to see if it is contained in the specified collection. If it is so contained, it is removed from this set with the iterator's`remove`method. If the specified collection has fewer elements, then the implementation iterates over the specified collection, removing from this set each element returned by the iterator, using this set's`remove`method. Note that this implementation will throw an`UnsupportedOperationException`if the iterator returned by the`iterator`method does not implement the`remove`method. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int) <br /> | ||

## Public methods

### allOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> allOf(elementType: Class<E>!): EnumSet<E>!
```

Creates an enum set containing all of the elements in the specified element type.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | The class of the elements in the set |
| `elementType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>!:the class object of the element type for this enum set |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | An enum set containing all the elements in the specified type. |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`elementType`is null |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): EnumSet<E>
```

Returns a copy of this set.

| Return ||
|---------------------------------------------------------------------------------|--------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E> | a copy of this set |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### complementOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> complementOf(s: EnumSet<E>!): EnumSet<E>!
```

Creates an enum set with the same element type as the specified enum set, initially containing all the elements of this type that are*not*contained in the specified set.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | The class of the elements in the enum set |
| `s` | [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>!:the enum set from whose complement to initialize this enum set |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | The complement of the specified set in this set |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if`s`is null |

### copyOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> copyOf(c: MutableCollection<E>!): EnumSet<E>!
```

Creates an enum set initialized from the specified collection. If the specified collection is an`EnumSet`instance, this static factory method behaves identically to [copyOf(java.util.EnumSet)](https://developer.android.com/reference/kotlin/java/util/EnumSet#copyOf(java.util.EnumSet)). Otherwise, the specified collection must contain at least one element (in order to determine the new enum set's element type).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | The class of the elements in the collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<E\>!:the collection from which to initialize this enum set |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | An enum set initialized from the given collection. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`c`is not an`EnumSet`instance and contains no elements |
| `java.lang.NullPointerException` | if`c`is null |

### copyOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> copyOf(s: EnumSet<E>!): EnumSet<E>!
```

Creates an enum set with the same element type as the specified enum set, initially containing the same elements (if any).

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | The class of the elements in the set |
| `s` | [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)\<E\>!:the enum set from which to initialize this enum set |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | A copy of the specified enum set. |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if`s`is null |

### noneOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> noneOf(elementType: Class<E>!): EnumSet<E>!
```

Creates an empty enum set with the specified element type.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | The class of the elements in the set |
| `elementType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>!:the class object of the element type for this enum set |

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | An empty enum set of the specified type. |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`elementType`is null |

### of

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> of(e: E): EnumSet<E>!
```

Creates an enum set initially containing the specified element. Overloadings of this method exist to initialize an enum set with one through five elements. A sixth overloading is provided that uses the varargs feature. This overloading may be used to create an enum set initially containing an arbitrary number of elements, but is likely to run slower than the overloadings that do not use varargs.

| Parameters ||
|-------|-----------------------------------------------------|
| `<E>` | The class of the specified element and of the set |
| `e` | E:the element that this set is to contain initially |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing the specified element |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if`e`is null |

### of

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> of(
    e1: E, 
    e2: E
): EnumSet<E>!
```

Creates an enum set initially containing the specified elements. Overloadings of this method exist to initialize an enum set with one through five elements. A sixth overloading is provided that uses the varargs feature. This overloading may be used to create an enum set initially containing an arbitrary number of elements, but is likely to run slower than the overloadings that do not use varargs.

| Parameters ||
|-------|---------------------------------------------------------|
| `<E>` | The class of the parameter elements and of the set |
| `e1` | E:an element that this set is to contain initially |
| `e2` | E:another element that this set is to contain initially |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing the specified elements |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if any parameters are null |

### of

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> of(
    e1: E, 
    e2: E, 
    e3: E
): EnumSet<E>!
```

Creates an enum set initially containing the specified elements. Overloadings of this method exist to initialize an enum set with one through five elements. A sixth overloading is provided that uses the varargs feature. This overloading may be used to create an enum set initially containing an arbitrary number of elements, but is likely to run slower than the overloadings that do not use varargs.

| Parameters ||
|-------|---------------------------------------------------------|
| `<E>` | The class of the parameter elements and of the set |
| `e1` | E:an element that this set is to contain initially |
| `e2` | E:another element that this set is to contain initially |
| --- | --- |
| `e3` | E:another element that this set is to contain initially |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing the specified elements |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if any parameters are null |

### of

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E
): EnumSet<E>!
```

Creates an enum set initially containing the specified elements. Overloadings of this method exist to initialize an enum set with one through five elements. A sixth overloading is provided that uses the varargs feature. This overloading may be used to create an enum set initially containing an arbitrary number of elements, but is likely to run slower than the overloadings that do not use varargs.

| Parameters ||
|-------|---------------------------------------------------------|
| `<E>` | The class of the parameter elements and of the set |
| `e1` | E:an element that this set is to contain initially |
| `e2` | E:another element that this set is to contain initially |
| --- | --- |
| `e3` | E:another element that this set is to contain initially |
| `e4` | E:another element that this set is to contain initially |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing the specified elements |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if any parameters are null |

### of

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E
): EnumSet<E>!
```

Creates an enum set initially containing the specified elements. Overloadings of this method exist to initialize an enum set with one through five elements. A sixth overloading is provided that uses the varargs feature. This overloading may be used to create an enum set initially containing an arbitrary number of elements, but is likely to run slower than the overloadings that do not use varargs.

| Parameters ||
|-------|---------------------------------------------------------|
| `<E>` | The class of the parameter elements and of the set |
| `e1` | E:an element that this set is to contain initially |
| `e2` | E:another element that this set is to contain initially |
| --- | --- |
| `e3` | E:another element that this set is to contain initially |
| `e4` | E:another element that this set is to contain initially |
| `e5` | E:another element that this set is to contain initially |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing the specified elements |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if any parameters are null |

### of

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <E : Enum<E>!> of(
    first: E, 
    vararg rest: E
): EnumSet<E>!
```

Creates an enum set initially containing the specified elements. This factory, whose parameter list uses the varargs feature, may be used to create an enum set initially containing an arbitrary number of elements, but it is likely to run slower than the overloadings that do not use varargs.

| Parameters ||
|---------|----------------------------------------------------------|
| `<E>` | The class of the parameter elements and of the set |
| `first` | E:an element that the set is to contain initially |
| `rest` | E:the remaining elements the set is to contain initially |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing the specified elements |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------|
| `java.lang.NullPointerException` | if any of the specified elements are null, or if`rest`is null |

### range

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Enum<E>!> range(
    from: E, 
    to: E
): EnumSet<E>!
```

Creates an enum set initially containing all of the elements in the range defined by the two specified endpoints. The returned set will contain the endpoints themselves, which may be identical but must not be out of order.

| Parameters ||
|--------|----------------------------------------------------|
| `<E>` | The class of the parameter elements and of the set |
| `from` | E:the first element in the range |
| `to` | E:the last element in the range |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [EnumSet](https://developer.android.com/reference/kotlin/java/util/EnumSet#)<E>! | an enum set initially containing all of the elements in the range defined by the two specified endpoints |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.NullPointerException` | if`from`or`to`are null |
| `java.lang.IllegalArgumentException` | if`from.compareTo(to) > 0` |

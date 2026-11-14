# Collections

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Collections

```
open class Collections
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Collections](https://developer.android.com/reference/kotlin/java/util/Collections#) |

This class consists exclusively of static methods that operate on or return collections. It contains polymorphic algorithms that operate on collections, "wrappers", which return a new collection backed by a specified collection, and a few other odds and ends.

The methods of this class all throw a`NullPointerException`if the collections or class objects provided to them are null.

The documentation for the polymorphic algorithms contained in this class generally includes a brief description of the*implementation* . Such descriptions should be regarded as*implementation notes* , rather than parts of the*specification* . Implementors should feel free to substitute other algorithms, so long as the specification itself is adhered to. (For example, the algorithm used by`sort`does not have to be a mergesort, but it does have to be*stable*.)

The "destructive" algorithms contained in this class, that is, the algorithms that modify the collection on which they operate, are specified to throw`UnsupportedOperationException`if the collection does not support the appropriate mutation primitive(s), such as the`set`method. These algorithms may, but are not required to, throw this exception if an invocation would have no effect on the collection. For example, invoking the`sort`method on an unmodifiable list that is already sorted may or may not throw`UnsupportedOperationException`.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/Collections#addAll(kotlin.collections.MutableCollection,%20java.util.Collections.addAll.T))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `T>`, `vararg` `elements:` `T`)` Adds all of the specified elements to the specified collection. |
| openstatic [Queue](https://developer.android.com/reference/kotlin/java/util/Queue)\<T\> | [asLifoQueue](https://developer.android.com/reference/kotlin/java/util/Collections#asLifoQueue(java.util.Deque))`(`deque:` ` [Deque](https://developer.android.com/reference/kotlin/java/util/Deque)<T>`)` Returns a view of a [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) as a Last-in-first-out (Lifo) [Queue](https://developer.android.com/reference/kotlin/java/util/Queue). |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [binarySearch](https://developer.android.com/reference/kotlin/java/util/Collections#binarySearch(kotlin.collections.MutableList,%20java.util.Collections.binarySearch.T))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [Comparable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-comparable/index.html)<T>!>`, `key:` `T`)` Searches the specified list for the specified object using the binary search algorithm. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [binarySearch](https://developer.android.com/reference/kotlin/java/util/Collections#binarySearch(kotlin.collections.MutableList,%20java.util.Collections.binarySearch.T,%20java.util.Comparator))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` `T>`, `key:` `T`, `c:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `T>?`)` Searches the specified list for the specified object using the binary search algorithm. |
| openstatic [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<E\> | [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<E>`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>`)` Returns a dynamically typesafe view of the specified collection. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | [checkedList](https://developer.android.com/reference/kotlin/java/util/Collections#checkedList(kotlin.collections.MutableList,%20java.lang.Class))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<E>`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>`)` Returns a dynamically typesafe view of the specified list. |
| openstatic [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\> | [checkedMap](https://developer.android.com/reference/kotlin/java/util/Collections#checkedMap(kotlin.collections.MutableMap,%20java.lang.Class,%20java.lang.Class))`(`m:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V>`, `keyType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<K>`, `valueType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>`)` Returns a dynamically typesafe view of the specified map. |
| openstatic [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,V\> | [checkedNavigableMap](https://developer.android.com/reference/kotlin/java/util/Collections#checkedNavigableMap(java.util.NavigableMap,%20java.lang.Class,%20java.lang.Class))`(`m:` ` [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `V>`, `keyType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<K>`, `valueType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>`)` Returns a dynamically typesafe view of the specified navigable map. |
| openstatic [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<E\> | [checkedNavigableSet](https://developer.android.com/reference/kotlin/java/util/Collections#checkedNavigableSet(java.util.NavigableSet,%20java.lang.Class))`(`s:` ` [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<E>`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>`)` Returns a dynamically typesafe view of the specified navigable set. |
| openstatic [Queue](https://developer.android.com/reference/kotlin/java/util/Queue)\<E\> | [checkedQueue](https://developer.android.com/reference/kotlin/java/util/Collections#checkedQueue(java.util.Queue,%20java.lang.Class))`(`queue:` ` [Queue](https://developer.android.com/reference/kotlin/java/util/Queue)<E>`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>`)` Returns a dynamically typesafe view of the specified queue. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [checkedSet](https://developer.android.com/reference/kotlin/java/util/Collections#checkedSet(kotlin.collections.MutableSet,%20java.lang.Class))`(`s:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E>`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>`)` Returns a dynamically typesafe view of the specified set. |
| openstatic [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,V\> | [checkedSortedMap](https://developer.android.com/reference/kotlin/java/util/Collections#checkedSortedMap(java.util.SortedMap,%20java.lang.Class,%20java.lang.Class))`(`m:` ` [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `V>`, `keyType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<K>`, `valueType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>`)` Returns a dynamically typesafe view of the specified sorted map. |
| openstatic [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<E\> | [checkedSortedSet](https://developer.android.com/reference/kotlin/java/util/Collections#checkedSortedSet(java.util.SortedSet,%20java.lang.Class))`(`s:` ` [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<E>`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<E>`)` Returns a dynamically typesafe view of the specified sorted set. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copy](https://developer.android.com/reference/kotlin/java/util/Collections#copy(kotlin.collections.MutableList,%20kotlin.collections.MutableList))`(`dest:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<in` `T>`, `src:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` `T>`)` Copies all of the elements from one list into another. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [disjoint](https://developer.android.com/reference/kotlin/java/util/Collections#disjoint(kotlin.collections.MutableCollection,%20kotlin.collections.MutableCollection))`(`c1:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>`, `c2:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>`)` Returns`true`if the two specified collections have no elements in common. |
| openstatic [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<T\> | [emptyEnumeration](https://developer.android.com/reference/kotlin/java/util/Collections#emptyEnumeration())`()` Returns an enumeration that has no elements. |
| openstatic [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\> | [emptyIterator](https://developer.android.com/reference/kotlin/java/util/Collections#emptyIterator())`()` Returns an iterator that has no elements. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [emptyList](https://developer.android.com/reference/kotlin/java/util/Collections#emptyList())`()` Returns an empty list (immutable). |
| openstatic [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<T\> | [emptyListIterator](https://developer.android.com/reference/kotlin/java/util/Collections#emptyListIterator())`()` Returns a list iterator that has no elements. |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\> | [emptyMap](https://developer.android.com/reference/kotlin/java/util/Collections#emptyMap())`()` Returns an empty map (immutable). |
| static [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,V\> | [emptyNavigableMap](https://developer.android.com/reference/kotlin/java/util/Collections#emptyNavigableMap())`()` Returns an empty navigable map (immutable). |
| openstatic [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<E\> | [emptyNavigableSet](https://developer.android.com/reference/kotlin/java/util/Collections#emptyNavigableSet())`()` Returns an empty navigable set (immutable). |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\> | [emptySet](https://developer.android.com/reference/kotlin/java/util/Collections#emptySet())`()` Returns an empty set (immutable). |
| static [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,V\> | [emptySortedMap](https://developer.android.com/reference/kotlin/java/util/Collections#emptySortedMap())`()` Returns an empty sorted map (immutable). |
| openstatic [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<E\> | [emptySortedSet](https://developer.android.com/reference/kotlin/java/util/Collections#emptySortedSet())`()` Returns an empty sorted set (immutable). |
| openstatic [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<T\> | [enumeration](https://developer.android.com/reference/kotlin/java/util/Collections#enumeration(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T>`)` Returns an enumeration over the specified collection. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fill](https://developer.android.com/reference/kotlin/java/util/Collections#fill(kotlin.collections.MutableList,%20java.util.Collections.fill.T))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<in` `T>`, `obj:` `T`)` Replaces all of the elements of the specified list with the specified element. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [frequency](https://developer.android.com/reference/kotlin/java/util/Collections#frequency(kotlin.collections.MutableCollection,%20kotlin.Any))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>`, `o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns the number of elements in the specified collection equal to the specified object. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOfSubList](https://developer.android.com/reference/kotlin/java/util/Collections#indexOfSubList(kotlin.collections.MutableList,%20kotlin.collections.MutableList))`(`source:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`, `target:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`)` Returns the starting position of the first occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOfSubList](https://developer.android.com/reference/kotlin/java/util/Collections#lastIndexOfSubList(kotlin.collections.MutableList,%20kotlin.collections.MutableList))`(`source:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`, `target:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`)` Returns the starting position of the last occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence. |
| openstatic [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList)\<T\> | [list](https://developer.android.com/reference/kotlin/java/util/Collections#list(java.util.Enumeration))`(`e:` ` [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<T>`)` Returns an array list containing the elements returned by the specified enumeration in the order they are returned by the enumeration. |
| openstaticT | [max](https://developer.android.com/reference/kotlin/java/util/Collections#max(kotlin.collections.MutableCollection))`(`coll:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`)` Returns the maximum element of the given collection, according to the*natural ordering*of its elements. |
| openstaticT | [max](https://developer.android.com/reference/kotlin/java/util/Collections#max(kotlin.collections.MutableCollection,%20java.util.Comparator))`(`coll:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`, `comp:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `T>?`)` Returns the maximum element of the given collection, according to the order induced by the specified comparator. |
| openstaticT | [min](https://developer.android.com/reference/kotlin/java/util/Collections#min(kotlin.collections.MutableCollection))`(`coll:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`)` Returns the minimum element of the given collection, according to the*natural ordering*of its elements. |
| openstaticT | [min](https://developer.android.com/reference/kotlin/java/util/Collections#min(kotlin.collections.MutableCollection,%20java.util.Comparator))`(`coll:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`, `comp:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `T>?`)` Returns the minimum element of the given collection, according to the order induced by the specified comparator. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [nCopies](https://developer.android.com/reference/kotlin/java/util/Collections#nCopies(kotlin.Int,%20java.util.Collections.nCopies.T))`(`n:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `o:` `T`)` Returns an immutable list consisting of`n`copies of the specified object. |
| openstatic [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)\<E\> | [newSequencedSetFromMap](https://developer.android.com/reference/kotlin/java/util/Collections#newSequencedSetFromMap(java.util.SequencedMap))`(`map:` ` [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap)<E,` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Returns a sequenced set backed by the specified map. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [newSetFromMap](https://developer.android.com/reference/kotlin/java/util/Collections#newSetFromMap(kotlin.collections.MutableMap))`(`map:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<E,` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!>`)` Returns a set backed by the specified map. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [replaceAll](https://developer.android.com/reference/kotlin/java/util/Collections#replaceAll(kotlin.collections.MutableList,%20java.util.Collections.replaceAll.T,%20java.util.Collections.replaceAll.T))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`, `oldVal:` `T`, `newVal:` `T`)` Replaces all occurrences of one specified value in a list with another. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reverse](https://developer.android.com/reference/kotlin/java/util/Collections#reverse(kotlin.collections.MutableList))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`)` Reverses the order of the elements in the specified list. |
| openstatic [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<T\> | [reverseOrder](https://developer.android.com/reference/kotlin/java/util/Collections#reverseOrder())`()` Returns a comparator that imposes the reverse of the*natural ordering* on a collection of objects that implement the`Comparable`interface. |
| openstatic [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<T\> | [reverseOrder](https://developer.android.com/reference/kotlin/java/util/Collections#reverseOrder(java.util.Comparator))`(`cmp:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<T>?`)` Returns a comparator that imposes the reverse ordering of the specified comparator. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rotate](https://developer.android.com/reference/kotlin/java/util/Collections#rotate(kotlin.collections.MutableList,%20kotlin.Int))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`, `distance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Rotates the elements in the specified list by the specified distance. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shuffle](https://developer.android.com/reference/kotlin/java/util/Collections#shuffle(kotlin.collections.MutableList))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`)` Randomly permutes the specified list using a default source of randomness. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shuffle](https://developer.android.com/reference/kotlin/java/util/Collections#shuffle(kotlin.collections.MutableList,%20java.util.Random))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`, `rnd:` ` [Random](https://developer.android.com/reference/kotlin/java/util/Random)`)` Randomly permute the specified list using the specified source of randomness. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shuffle](https://developer.android.com/reference/kotlin/java/util/Collections#shuffle(kotlin.collections.MutableList,%20java.util.random.RandomGenerator))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`, `rnd:` ` [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator)`)` Randomly permute the specified list using the specified source of randomness. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\> | [singleton](https://developer.android.com/reference/kotlin/java/util/Collections#singleton(java.util.Collections.singleton.T))`(`o:` `T`)` Returns an immutable set containing only the specified object. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [singletonList](https://developer.android.com/reference/kotlin/java/util/Collections#singletonList(java.util.Collections.singletonList.T))`(`o:` `T`)` Returns an immutable list containing only the specified object. |
| openstatic [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\> | [singletonMap](https://developer.android.com/reference/kotlin/java/util/Collections#singletonMap(java.util.Collections.singletonMap.K,%20java.util.Collections.singletonMap.V))`(`key:` `K`, `value:` `V`)` Returns an immutable map, mapping only the specified key to the specified value. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](https://developer.android.com/reference/kotlin/java/util/Collections#sort(kotlin.collections.MutableList))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`)` Sorts the specified list into ascending order, according to the [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its elements. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](https://developer.android.com/reference/kotlin/java/util/Collections#sort(kotlin.collections.MutableList,%20java.util.Comparator))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`, `c:` ` [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<in` `T>?`)` Sorts the specified list according to the order induced by the specified comparator. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swap](https://developer.android.com/reference/kotlin/java/util/Collections#swap(kotlin.collections.MutableList,%20kotlin.Int,%20kotlin.Int))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<*>`, `i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `j:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Swaps the elements at the specified positions in the specified list. |
| openstatic [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<T\> | [synchronizedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedCollection(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T>`)` Returns a synchronized (thread-safe) collection backed by the specified collection. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [synchronizedList](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedList(kotlin.collections.MutableList))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T>`)` Returns a synchronized (thread-safe) list backed by the specified list. |
| openstatic [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\> | [synchronizedMap](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedMap(kotlin.collections.MutableMap))`(`m:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V>`)` Returns a synchronized (thread-safe) map backed by the specified map. |
| openstatic [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,V\> | [synchronizedNavigableMap](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedNavigableMap(java.util.NavigableMap))`(`m:` ` [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `V>`)` Returns a synchronized (thread-safe) navigable map backed by the specified navigable map. |
| openstatic [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<T\> | [synchronizedNavigableSet](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedNavigableSet(java.util.NavigableSet))`(`s:` ` [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<T>`)` Returns a synchronized (thread-safe) navigable set backed by the specified navigable set. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\> | [synchronizedSet](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedSet(kotlin.collections.MutableSet))`(`s:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<T>`)` Returns a synchronized (thread-safe) set backed by the specified set. |
| openstatic [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,V\> | [synchronizedSortedMap](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedSortedMap(java.util.SortedMap))`(`m:` ` [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `V>`)` Returns a synchronized (thread-safe) sorted map backed by the specified sorted map. |
| openstatic [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<T\> | [synchronizedSortedSet](https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedSortedSet(java.util.SortedSet))`(`s:` ` [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<T>`)` Returns a synchronized (thread-safe) sorted set backed by the specified sorted set. |
| openstatic [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<T\> | [unmodifiableCollection](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableCollection(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified collection. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [unmodifiableList](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableList(kotlin.collections.MutableList))`(`list:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` `T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified list. |
| openstatic [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\> | [unmodifiableMap](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableMap(kotlin.collections.MutableMap))`(`m:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<out` `K,` `out` `V>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified map. |
| openstatic [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,V\> | [unmodifiableNavigableMap](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableNavigableMap(java.util.NavigableMap))`(`m:` ` [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `out` `V>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified navigable map. |
| openstatic [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<T\> | [unmodifiableNavigableSet](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableNavigableSet(java.util.NavigableSet))`(`s:` ` [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified navigable set. |
| openstatic [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)\<T\> | [unmodifiableSequencedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableSequencedCollection(java.util.SequencedCollection))`(`c:` ` [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)<out` `T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified`SequencedCollection`. |
| openstatic [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap)\<K,V\> | [unmodifiableSequencedMap](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableSequencedMap(java.util.SequencedMap))`(`m:` ` [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap)<out` `K,` `out` `V>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified`SequencedMap`. |
| openstatic [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)\<T\> | [unmodifiableSequencedSet](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableSequencedSet(java.util.SequencedSet))`(`s:` ` [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)<out` `T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified`SequencedSet`. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\> | [unmodifiableSet](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableSet(kotlin.collections.MutableSet))`(`s:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` `T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified set. |
| openstatic [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,V\> | [unmodifiableSortedMap](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableSortedMap(java.util.SortedMap))`(`m:` ` [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `out` `V>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified sorted map. |
| openstatic [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<T\> | [unmodifiableSortedSet](https://developer.android.com/reference/kotlin/java/util/Collections#unmodifiableSortedSet(java.util.SortedSet))`(`s:` ` [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<T>`)` Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified sorted set. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\> | [EMPTY_LIST](https://developer.android.com/reference/kotlin/java/util/Collections#EMPTY_LIST:kotlin.collections.MutableList) The empty list (immutable). |
| static [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\> | [EMPTY_MAP](https://developer.android.com/reference/kotlin/java/util/Collections#EMPTY_MAP:kotlin.collections.MutableMap) The empty map (immutable). |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?\> | [EMPTY_SET](https://developer.android.com/reference/kotlin/java/util/Collections#EMPTY_SET:kotlin.collections.MutableSet) The empty set (immutable). |

## Public methods

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <T : Any!> addAll(
    c: MutableCollection<in T>, 
    vararg elements: T
): Boolean
```

Adds all of the specified elements to the specified collection. Elements to be added may be specified individually or as an array. The behaviour of this convenience method is similar to that of`c.addAll(Collections.unmodifiableList(Arrays.asList(elements)))`.

When elements are specified individually, this method provides a convenient way to add a few elements to an existing collection: 

```kotlin
Collections.addAll(flavors, "Peaches 'n Plutonium", "Rocky Racoon");
  
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the elements to add and of the collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<inT\>:the collection into which`elements`are to be inserted |
| `elements` | T:the elements to insert into`c` |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the collection changed as a result of the call |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if`c`does not support the`add`operation |
| `java.lang.NullPointerException` | if`elements`contains one or more null values and`c`does not permit null elements, or if`c`or`elements`are`null` |
| `java.lang.IllegalArgumentException` | if some property of a value in`elements`prevents it from being added to`c` |

**See Also**

- [java.util.Collection#addAll(Collection)](https://developer.android.com/reference/kotlin/java/util/Collection#addAll(kotlin.collections.MutableCollection)) 

### asLifoQueue

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> asLifoQueue(deque: Deque<T>): Queue<T>
```

Returns a view of a [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) as a Last-in-first-out (Lifo) [Queue](https://developer.android.com/reference/kotlin/java/util/Queue). Method`add`is mapped to`push`,`remove`is mapped to`pop`and so on. This view can be useful when you would like to use a method requiring a`Queue`but you need Lifo ordering.

Each method invocation on the queue returned by this method results in exactly one method invocation on the backing deque, with one exception. The [addAll](https://developer.android.com/reference/kotlin/java/util/Collection#addAll(kotlin.collections.MutableCollection))method is implemented as a sequence of [addFirst](https://developer.android.com/reference/kotlin/java/util/Deque#addFirst(java.util.Deque.E))invocations on the backing deque.

| Parameters ||
|---------|----------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the deque |
| `deque` | [Deque](https://developer.android.com/reference/kotlin/java/util/Deque)\<T\>:the deque |

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Queue](https://developer.android.com/reference/kotlin/java/util/Queue)<T> | the queue |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> binarySearch(
    list: MutableList<out Comparable<T>!>, 
    key: T
): Int
```

Searches the specified list for the specified object using the binary search algorithm. The list must be sorted into ascending order according to the [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its elements (as by the [sort(java.util.List)](https://developer.android.com/reference/kotlin/java/util/Collections#sort(kotlin.collections.MutableList))method) prior to making this call. If it is not sorted, the results are undefined. If the list contains multiple elements equal to the specified object, there is no guarantee which one will be found.

This method runs in log(n) time for a "random access" list (which provides near-constant-time positional access). If the specified list does not implement the [RandomAccess](https://developer.android.com/reference/kotlin/java/util/RandomAccess) interface and is large, this method will do an iterator-based binary search that performs O(n) link traversals and O(log n) element comparisons.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [Comparable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-comparable/index.html)\<T\>!\>:the list to be searched. |
| `key` | T:the key to be searched for. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the search key, if it is contained in the list; otherwise,`(-(`*insertion point*`) - 1)`. The*insertion point* is defined as the point at which the key would be inserted into the list: the index of the first element greater than the key, or`list.size()`if all elements in the list are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the list contains elements that are not*mutually comparable*(for example, strings and integers), or the search key is not mutually comparable with the elements of the list. |

### binarySearch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> binarySearch(
    list: MutableList<out T>, 
    key: T, 
    c: Comparator<in T>?
): Int
```

Searches the specified list for the specified object using the binary search algorithm. The list must be sorted into ascending order according to the specified comparator (as by the [sort(List, Comparator)](https://developer.android.com/reference/kotlin/java/util/Collections#sort(kotlin.collections.MutableList,%20java.util.Comparator))method), prior to making this call. If it is not sorted, the results are undefined. If the list contains multiple elements equal to the specified object, there is no guarantee which one will be found.

This method runs in log(n) time for a "random access" list (which provides near-constant-time positional access). If the specified list does not implement the [RandomAccess](https://developer.android.com/reference/kotlin/java/util/RandomAccess) interface and is large, this method will do an iterator-based binary search that performs O(n) link traversals and O(log n) element comparisons.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<outT\>:the list to be searched. |
| `key` | T:the key to be searched for. |
| `c` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inT\>?:the comparator by which the list is ordered. A`null`value indicates that the elements' [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) should be used. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the search key, if it is contained in the list; otherwise,`(-(`*insertion point*`) - 1)`. The*insertion point* is defined as the point at which the key would be inserted into the list: the index of the first element greater than the key, or`list.size()`if all elements in the list are less than the specified key. Note that this guarantees that the return value will be \>= 0 if and only if the key is found. |

| Exceptions ||
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the list contains elements that are not*mutually comparable*using the specified comparator, or the search key is not mutually comparable with the elements of the list using this comparator. |

### checkedCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> checkedCollection(
    c: MutableCollection<E>, 
    type: Class<E>
): MutableCollection<E>
```

Returns a dynamically typesafe view of the specified collection. Any attempt to insert an element of the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Assuming a collection contains no incorrectly typed elements prior to the time a dynamically typesafe view is generated, and that all subsequent access to the collection takes place through the view, it is*guaranteed*that the collection cannot contain an incorrectly typed element.

The generics mechanism in the language provides compile-time (static) type checking, but it is possible to defeat this mechanism with unchecked casts. Usually this is not a problem, as the compiler issues warnings on all such unchecked operations. There are, however, times when static type checking alone is not sufficient. For example, suppose a collection is passed to a third-party library and it is imperative that the library code not corrupt the collection by inserting an element of the wrong type.

Another use of dynamically typesafe views is debugging. Suppose a program fails with a`ClassCastException`, indicating that an incorrectly typed element was put into a parameterized collection. Unfortunately, the exception can occur at any time after the erroneous element is inserted, so it typically provides little or no information as to the real source of the problem. If the problem is reproducible, one can quickly determine its source by temporarily modifying the program to wrap the collection with a dynamically typesafe view. For example, this declaration: 

```kotlin
<code>Collection&lt;String&gt; c = new HashSet&lt;&gt;();
  </code>
```
may be replaced temporarily by this one: 

```kotlin
<code>Collection&lt;String&gt; c = Collections.checkedCollection(
          new HashSet&lt;&gt;(), String.class);
  </code>
```
Running the program again will cause it to fail at the point where an incorrectly typed element is inserted into the collection, clearly identifying the source of the problem. Once the problem is fixed, the modified declaration may be reverted back to the original.

The returned collection does*not* pass the hashCode and equals operations through to the backing collection, but relies on`Object`'s`equals`and`hashCode`methods. This is necessary to preserve the contracts of these operations in the case that the backing collection is a set or a list.

The returned collection will be serializable if the specified collection is serializable.

Since`null`is considered to be a value of any reference type, the returned collection permits insertion of null elements whenever the backing collection does.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the objects in the collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<E\>:the collection for which a dynamically typesafe view is to be returned |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>:the type of element that`c`is permitted to hold |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<E> | a dynamically typesafe view of the specified collection |

### checkedList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> checkedList(
    list: MutableList<E>, 
    type: Class<E>
): MutableList<E>
```

Returns a dynamically typesafe view of the specified list. Any attempt to insert an element of the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Assuming a list contains no incorrectly typed elements prior to the time a dynamically typesafe view is generated, and that all subsequent access to the list takes place through the view, it is*guaranteed*that the list cannot contain an incorrectly typed element.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned list will be serializable if the specified list is serializable.

Since`null`is considered to be a value of any reference type, the returned list permits insertion of null elements whenever the backing list does.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\>:the list for which a dynamically typesafe view is to be returned |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>:the type of element that`list`is permitted to hold |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<E> | a dynamically typesafe view of the specified list |

### checkedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> checkedMap(
    m: MutableMap<K, V>, 
    keyType: Class<K>, 
    valueType: Class<V>
): MutableMap<K, V>
```

Returns a dynamically typesafe view of the specified map. Any attempt to insert a mapping whose key or value have the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Similarly, any attempt to modify the value currently associated with a key will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#), whether the modification is attempted directly through the map itself, or through a [Map.Entry](https://developer.android.com/reference/kotlin/java/util/Map.Entry) instance obtained from the map's [entry set](https://developer.android.com/reference/kotlin/java/util/Map#entrySet())view.

Assuming a map contains no incorrectly typed keys or values prior to the time a dynamically typesafe view is generated, and that all subsequent access to the map takes place through the view (or one of its collection views), it is*guaranteed*that the map cannot contain an incorrectly typed key or value.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned map will be serializable if the specified map is serializable.

Since`null`is considered to be a value of any reference type, the returned map permits insertion of null keys or values whenever the backing map does.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\>:the map for which a dynamically typesafe view is to be returned |
| `keyType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<K\>:the type of key that`m`is permitted to hold |
| `valueType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<V\>:the type of value that`m`is permitted to hold |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V> | a dynamically typesafe view of the specified map |

### checkedNavigableMap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> checkedNavigableMap(
    m: NavigableMap<K, V>, 
    keyType: Class<K>, 
    valueType: Class<V>
): NavigableMap<K, V>
```

Returns a dynamically typesafe view of the specified navigable map. Any attempt to insert a mapping whose key or value have the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Similarly, any attempt to modify the value currently associated with a key will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#), whether the modification is attempted directly through the map itself, or through a [Map.Entry](https://developer.android.com/reference/kotlin/java/util/Map.Entry) instance obtained from the map's [entry set](https://developer.android.com/reference/kotlin/java/util/Map#entrySet())view.

Assuming a map contains no incorrectly typed keys or values prior to the time a dynamically typesafe view is generated, and that all subsequent access to the map takes place through the view (or one of its collection views), it is*guaranteed*that the map cannot contain an incorrectly typed key or value.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned map will be serializable if the specified map is serializable.

Since`null`is considered to be a value of any reference type, the returned map permits insertion of null keys or values whenever the backing map does.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | type of map keys |
| `<V>` | type of map values |
| `m` | [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,V\>:the map for which a dynamically typesafe view is to be returned |
| `keyType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<K\>:the type of key that`m`is permitted to hold |
| `valueType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<V\>:the type of value that`m`is permitted to hold |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `V> | a dynamically typesafe view of the specified map |

### checkedNavigableSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> checkedNavigableSet(
    s: NavigableSet<E>, 
    type: Class<E>
): NavigableSet<E>
```

Returns a dynamically typesafe view of the specified navigable set. Any attempt to insert an element of the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Assuming a navigable set contains no incorrectly typed elements prior to the time a dynamically typesafe view is generated, and that all subsequent access to the navigable set takes place through the view, it is*guaranteed*that the navigable set cannot contain an incorrectly typed element.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned navigable set will be serializable if the specified navigable set is serializable.

Since`null`is considered to be a value of any reference type, the returned navigable set permits insertion of null elements whenever the backing sorted set does.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the objects in the set |
| `s` | [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<E\>:the navigable set for which a dynamically typesafe view is to be returned |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>:the type of element that`s`is permitted to hold |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<E> | a dynamically typesafe view of the specified navigable set |

### checkedQueue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> checkedQueue(
    queue: Queue<E>, 
    type: Class<E>
): Queue<E>
```

Returns a dynamically typesafe view of the specified queue. Any attempt to insert an element of the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Assuming a queue contains no incorrectly typed elements prior to the time a dynamically typesafe view is generated, and that all subsequent access to the queue takes place through the view, it is*guaranteed*that the queue cannot contain an incorrectly typed element.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned queue will be serializable if the specified queue is serializable.

Since`null`is considered to be a value of any reference type, the returned queue permits insertion of`null`elements whenever the backing queue does.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the objects in the queue |
| `queue` | [Queue](https://developer.android.com/reference/kotlin/java/util/Queue)\<E\>:the queue for which a dynamically typesafe view is to be returned |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>:the type of element that`queue`is permitted to hold |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Queue](https://developer.android.com/reference/kotlin/java/util/Queue)<E> | a dynamically typesafe view of the specified queue |

### checkedSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> checkedSet(
    s: MutableSet<E>, 
    type: Class<E>
): MutableSet<E>
```

Returns a dynamically typesafe view of the specified set. Any attempt to insert an element of the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Assuming a set contains no incorrectly typed elements prior to the time a dynamically typesafe view is generated, and that all subsequent access to the set takes place through the view, it is*guaranteed*that the set cannot contain an incorrectly typed element.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned set will be serializable if the specified set is serializable.

Since`null`is considered to be a value of any reference type, the returned set permits insertion of null elements whenever the backing set does.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the objects in the set |
| `s` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\>:the set for which a dynamically typesafe view is to be returned |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>:the type of element that`s`is permitted to hold |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a dynamically typesafe view of the specified set |

### checkedSortedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> checkedSortedMap(
    m: SortedMap<K, V>, 
    keyType: Class<K>, 
    valueType: Class<V>
): SortedMap<K, V>
```

Returns a dynamically typesafe view of the specified sorted map. Any attempt to insert a mapping whose key or value have the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Similarly, any attempt to modify the value currently associated with a key will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#), whether the modification is attempted directly through the map itself, or through a [Map.Entry](https://developer.android.com/reference/kotlin/java/util/Map.Entry) instance obtained from the map's [entry set](https://developer.android.com/reference/kotlin/java/util/Map#entrySet())view.

Assuming a map contains no incorrectly typed keys or values prior to the time a dynamically typesafe view is generated, and that all subsequent access to the map takes place through the view (or one of its collection views), it is*guaranteed*that the map cannot contain an incorrectly typed key or value.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned map will be serializable if the specified map is serializable.

Since`null`is considered to be a value of any reference type, the returned map permits insertion of null keys or values whenever the backing map does.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,V\>:the map for which a dynamically typesafe view is to be returned |
| `keyType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<K\>:the type of key that`m`is permitted to hold |
| `valueType` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<V\>:the type of value that`m`is permitted to hold |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `V> | a dynamically typesafe view of the specified map |

### checkedSortedSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> checkedSortedSet(
    s: SortedSet<E>, 
    type: Class<E>
): SortedSet<E>
```

Returns a dynamically typesafe view of the specified sorted set. Any attempt to insert an element of the wrong type will result in an immediate [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#). Assuming a sorted set contains no incorrectly typed elements prior to the time a dynamically typesafe view is generated, and that all subsequent access to the sorted set takes place through the view, it is*guaranteed*that the sorted set cannot contain an incorrectly typed element.

A discussion of the use of dynamically typesafe views may be found in the documentation for the [checkedCollection](https://developer.android.com/reference/kotlin/java/util/Collections#checkedCollection(kotlin.collections.MutableCollection,%20java.lang.Class))method.

The returned sorted set will be serializable if the specified sorted set is serializable.

Since`null`is considered to be a value of any reference type, the returned sorted set permits insertion of null elements whenever the backing sorted set does.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the objects in the set |
| `s` | [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<E\>:the sorted set for which a dynamically typesafe view is to be returned |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<E\>:the type of element that`s`is permitted to hold |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<E> | a dynamically typesafe view of the specified sorted set |

### copy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> copy(
    dest: MutableList<in T>, 
    src: MutableList<out T>
): Unit
```

Copies all of the elements from one list into another. After the operation, the index of each copied element in the destination list will be identical to its index in the source list. The destination list's size must be greater than or equal to the source list's size. If it is greater, the remaining elements in the destination list are unaffected.

This method runs in linear time.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the lists |
| `dest` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<inT\>:The destination list. |
| `src` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<outT\>:The source list. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the destination list is too small to contain the entire source List. |
| `java.lang.UnsupportedOperationException` | if the destination list's list-iterator does not support the`set`operation. |

### disjoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun disjoint(
    c1: MutableCollection<*>, 
    c2: MutableCollection<*>
): Boolean
```

Returns`true`if the two specified collections have no elements in common.

Care must be exercised if this method is used on collections that do not comply with the general contract for`Collection`. Implementations may elect to iterate over either collection and test for containment in the other collection (or to perform any equivalent computation). If either collection uses a nonstandard equality test (as does a [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet) whose ordering is not*compatible with equals* , or the key set of an [IdentityHashMap](https://developer.android.com/reference/kotlin/java/util/IdentityHashMap)), both collections must use the same nonstandard equality test, or the result of this method is undefined.

Care must also be exercised when using collections that have restrictions on the elements that they may contain. Collection implementations are allowed to throw exceptions for any operation involving elements they deem ineligible. For absolute safety the specified collections should contain only elements which are eligible elements for both collections.

Note that it is permissible to pass the same collection in both parameters, in which case the method will return`true`if and only if the collection is empty.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------------------|
| `c1` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>:a collection |
| `c2` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>:a collection |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the two specified collections have no elements in common. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if one collection contains a`null`element and`null`is not an eligible element for the other collection. ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.ClassCastException` | if one collection contains an element that is of a type which is ineligible for the other collection. ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### emptyEnumeration

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> emptyEnumeration(): Enumeration<T>
```

Returns an enumeration that has no elements. More precisely,

- [hasMoreElements](https://developer.android.com/reference/kotlin/java/util/Enumeration#hasMoreElements())always returns`false`.
- [nextElement](https://developer.android.com/reference/kotlin/java/util/Enumeration#nextElement())always throws [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException).

<br />

Implementations of this method are permitted, but not required, to return the same object from multiple invocations.

| Parameters ||
|-------|---------------------------------------------|
| `<T>` | the class of the objects in the enumeration |

| Return ||
|----------------------------------------------------------------------------------------|----------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<T> | an empty enumeration |

### emptyIterator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> emptyIterator(): MutableIterator<T>
```

Returns an iterator that has no elements. More precisely,

- [hasNext](https://developer.android.com/reference/kotlin/java/util/Iterator#hasNext())always returns`false`.
- [next](https://developer.android.com/reference/kotlin/java/util/Iterator#next())always throws [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException).
- [remove](https://developer.android.com/reference/kotlin/java/util/Iterator#remove())always throws [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).

<br />

Implementations of this method are permitted, but not required, to return the same object from multiple invocations.

| Parameters ||
|-------|------------------------------------------------------|
| `<T>` | type of elements, if there were any, in the iterator |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T> | an empty iterator |

### emptyList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> emptyList(): MutableList<T>
```

Returns an empty list (immutable). This list is serializable.

This example illustrates the type-safe way to obtain an empty list: 

```kotlin
List<String> s = Collections.emptyList();
  
```

| Parameters ||
|-------|--------------------------------------------------|
| `<T>` | type of elements, if there were any, in the list |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | an empty immutable list |

**See Also**

- [#EMPTY_LIST](https://developer.android.com/reference/kotlin/java/util/Collections#EMPTY_LIST:kotlin.collections.MutableList) 

### emptyListIterator

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> emptyListIterator(): MutableListIterator<T>
```

Returns a list iterator that has no elements. More precisely,

- [hasNext](https://developer.android.com/reference/kotlin/java/util/Iterator#hasNext())and [hasPrevious](https://developer.android.com/reference/kotlin/java/util/ListIterator#hasPrevious())always return`false`.
- [next](https://developer.android.com/reference/kotlin/java/util/Iterator#next())and [previous](https://developer.android.com/reference/kotlin/java/util/ListIterator#previous())always throw [NoSuchElementException](https://developer.android.com/reference/kotlin/java/util/NoSuchElementException).
- [remove](https://developer.android.com/reference/kotlin/java/util/Iterator#remove())and [set](https://developer.android.com/reference/kotlin/java/util/ListIterator#set(java.util.ListIterator.E))always throw [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#).
- [add](https://developer.android.com/reference/kotlin/java/util/ListIterator#add(java.util.ListIterator.E))always throws [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#).
- [nextIndex](https://developer.android.com/reference/kotlin/java/util/ListIterator#nextIndex())always returns`0`.
- [previousIndex](https://developer.android.com/reference/kotlin/java/util/ListIterator#previousIndex())always returns`-1`.

<br />

Implementations of this method are permitted, but not required, to return the same object from multiple invocations.

| Parameters ||
|-------|------------------------------------------------------|
| `<T>` | type of elements, if there were any, in the iterator |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<T> | an empty list iterator |

### emptyMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <K : Any!, V : Any!> emptyMap(): MutableMap<K, V>
```

Returns an empty map (immutable). This map is serializable.

This example illustrates the type-safe way to obtain an empty map: 

```kotlin
Map<String, Date> s = Collections.emptyMap();
  
```

| Parameters ||
|-------|-----------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V> | an empty map |

**See Also**

- [#EMPTY_MAP](https://developer.android.com/reference/kotlin/java/util/Collections#EMPTY_MAP:kotlin.collections.MutableMap) 

### emptyNavigableMap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <K : Any!, V : Any!> emptyNavigableMap(): NavigableMap<K, V>
```

Returns an empty navigable map (immutable). This map is serializable.

This example illustrates the type-safe way to obtain an empty map: 

```kotlin
<code>NavigableMap&lt;String, Date&gt; s = Collections.emptyNavigableMap();
  </code>
```

| Parameters ||
|-------|-----------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------|
| [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `V> | an empty navigable map |

### emptyNavigableSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> emptyNavigableSet(): NavigableSet<E>
```

Returns an empty navigable set (immutable). This set is serializable.

This example illustrates the type-safe way to obtain an empty navigable set: 

```kotlin
<code>NavigableSet&lt;String&gt; s = Collections.emptyNavigableSet();
  </code>
```

| Parameters ||
|-------|-------------------------------------------------|
| `<E>` | type of elements, if there were any, in the set |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<E> | the empty navigable set |

### emptySet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> emptySet(): MutableSet<T>
```

Returns an empty set (immutable). This set is serializable. Unlike the like-named field, this method is parameterized.

This example illustrates the type-safe way to obtain an empty set: 

```kotlin
Set<String> s = Collections.emptySet();
  
```

| Parameters ||
|-------|-------------------------------------|
| `<T>` | the class of the objects in the set |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<T> | the empty set |

**See Also**

- [#EMPTY_SET](https://developer.android.com/reference/kotlin/java/util/Collections#EMPTY_SET:kotlin.collections.MutableSet) 

### emptySortedMap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <K : Any!, V : Any!> emptySortedMap(): SortedMap<K, V>
```

Returns an empty sorted map (immutable). This map is serializable.

This example illustrates the type-safe way to obtain an empty map: 

```kotlin
<code>SortedMap&lt;String, Date&gt; s = Collections.emptySortedMap();
  </code>
```

| Parameters ||
|-------|-----------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `V> | an empty sorted map |

### emptySortedSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> emptySortedSet(): SortedSet<E>
```

Returns an empty sorted set (immutable). This set is serializable.

This example illustrates the type-safe way to obtain an empty sorted set: 

```kotlin
<code>SortedSet&lt;String&gt; s = Collections.emptySortedSet();
  </code>
```

| Parameters ||
|-------|-------------------------------------------------|
| `<E>` | type of elements, if there were any, in the set |

| Return ||
|------------------------------------------------------------------------------------|----------------------|
| [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<E> | the empty sorted set |

### enumeration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> enumeration(c: MutableCollection<T>): Enumeration<T>
```

Returns an enumeration over the specified collection. This provides interoperability with legacy APIs that require an enumeration as input.

The iterator returned from a call to [Enumeration.asIterator()](https://developer.android.com/reference/kotlin/java/util/Enumeration#asIterator())does not support removal of elements from the specified collection. This is necessary to avoid unintentionally increasing the capabilities of the returned enumeration.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<T\>:the collection for which an enumeration is to be returned. |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)<T> | an enumeration over the specified collection. |

**See Also**

- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration) 

### fill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> fill(
    list: MutableList<in T>, 
    obj: T
): Unit
```

Replaces all of the elements of the specified list with the specified element.

This method runs in linear time.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<inT\>:the list to be filled with the specified element. |
| `obj` | T:The element with which to fill the specified list. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

### frequency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun frequency(
    c: MutableCollection<*>, 
    o: Any?
): Int
```

Returns the number of elements in the specified collection equal to the specified object. More formally, returns the number of elements`e`in the collection such that`Objects.equals(o, e)`.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>:the collection in which to determine the frequency of`o` |
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose frequency is to be determined |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in`c`equal to`o` |

| Exceptions ||
|----------------------------------|--------------|
| `java.lang.NullPointerException` | if`c`is null |

### indexOfSubList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun indexOfSubList(
    source: MutableList<*>, 
    target: MutableList<*>
): Int
```

Returns the starting position of the first occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence. More formally, returns the lowest index`i`such that`source.subList(i, i+target.size()).equals(target)`, or -1 if there is no such index. (Returns -1 if`target.size() > source.size()`)

This implementation uses the "brute force" technique of scanning over the source list, looking for a match with the target at each location in turn.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list in which to search for the first occurrence of`target`. |
| `target` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list to search for as a subList of`source`. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the starting position of the first occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence. |

### lastIndexOfSubList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lastIndexOfSubList(
    source: MutableList<*>, 
    target: MutableList<*>
): Int
```

Returns the starting position of the last occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence. More formally, returns the highest index`i`such that`source.subList(i, i+target.size()).equals(target)`, or -1 if there is no such index. (Returns -1 if`target.size() > source.size()`)

This implementation uses the "brute force" technique of iterating over the source list, looking for a match with the target at each location in turn.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list in which to search for the last occurrence of`target`. |
| `target` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list to search for as a subList of`source`. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the starting position of the last occurrence of the specified target list within the specified source list, or -1 if there is no such occurrence. |

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> list(e: Enumeration<T>): ArrayList<T>
```

Returns an array list containing the elements returned by the specified enumeration in the order they are returned by the enumeration. This method provides interoperability between legacy APIs that return enumerations and new APIs that require collections.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects returned by the enumeration |
| `e` | [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)\<T\>:enumeration providing elements for the returned array list |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList)<T> | an array list containing the elements returned by the specified enumeration. |

**See Also**

- [java.util.Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration)
- [java.util.ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList) 

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T> max(coll: MutableCollection<out T>): T where T : Any!, T : Comparable<T>!
```

Returns the maximum element of the given collection, according to the*natural ordering* of its elements. All elements in the collection must implement the`Comparable`interface. Furthermore, all elements in the collection must be*mutually comparable* (that is,`e1.compareTo(e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the collection).

This method iterates over the entire collection, hence it requires time proportional to the size of the collection.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `coll` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outT\>:the collection whose maximum element is to be determined. |

| Return ||
|---|-------------------------------------------------------------------------------------------------|
| T | the maximum element of the given collection, according to the*natural ordering*of its elements. |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the collection contains elements that are not*mutually comparable*(for example, strings and integers). |
| `java.util.NoSuchElementException` | if the collection is empty. |

**See Also**

- [java.lang.Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) 

### max

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> max(
    coll: MutableCollection<out T>, 
    comp: Comparator<in T>?
): T
```

Returns the maximum element of the given collection, according to the order induced by the specified comparator. All elements in the collection must be*mutually comparable* by the specified comparator (that is,`comp.compare(e1, e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the collection).

This method iterates over the entire collection, hence it requires time proportional to the size of the collection.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `coll` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outT\>:the collection whose maximum element is to be determined. |
| `comp` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inT\>?:the comparator with which to determine the maximum element. A`null`value indicates that the elements'*natural ordering*should be used. |

| Return ||
|---|-------------------------------------------------------------------------------------|
| T | the maximum element of the given collection, according to the specified comparator. |

| Exceptions ||
|------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the collection contains elements that are not*mutually comparable*using the specified comparator. |
| `java.util.NoSuchElementException` | if the collection is empty. |

**See Also**

- [java.lang.Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) 

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T> min(coll: MutableCollection<out T>): T where T : Any!, T : Comparable<T>!
```

Returns the minimum element of the given collection, according to the*natural ordering* of its elements. All elements in the collection must implement the`Comparable`interface. Furthermore, all elements in the collection must be*mutually comparable* (that is,`e1.compareTo(e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the collection).

This method iterates over the entire collection, hence it requires time proportional to the size of the collection.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `coll` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outT\>:the collection whose minimum element is to be determined. |

| Return ||
|---|-------------------------------------------------------------------------------------------------|
| T | the minimum element of the given collection, according to the*natural ordering*of its elements. |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the collection contains elements that are not*mutually comparable*(for example, strings and integers). |
| `java.util.NoSuchElementException` | if the collection is empty. |

**See Also**

- [java.lang.Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) 

### min

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> min(
    coll: MutableCollection<out T>, 
    comp: Comparator<in T>?
): T
```

Returns the minimum element of the given collection, according to the order induced by the specified comparator. All elements in the collection must be*mutually comparable* by the specified comparator (that is,`comp.compare(e1, e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the collection).

This method iterates over the entire collection, hence it requires time proportional to the size of the collection.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `coll` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outT\>:the collection whose minimum element is to be determined. |
| `comp` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inT\>?:the comparator with which to determine the minimum element. A`null`value indicates that the elements'*natural ordering*should be used. |

| Return ||
|---|-------------------------------------------------------------------------------------|
| T | the minimum element of the given collection, according to the specified comparator. |

| Exceptions ||
|------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the collection contains elements that are not*mutually comparable*using the specified comparator. |
| `java.util.NoSuchElementException` | if the collection is empty. |

**See Also**

- [java.lang.Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) 

### nCopies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> nCopies(
    n: Int, 
    o: T
): MutableList<T>
```

Returns an immutable list consisting of`n`copies of the specified object. The newly allocated data object is tiny (it contains a single reference to the data object). This method is useful in combination with the`List.addAll`method to grow lists. The returned list is serializable.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the object to copy and of the objects in the returned list. |
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of elements in the returned list. |
| `o` | T:the element to appear repeatedly in the returned list. |

| Return ||
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | an immutable list consisting of`n`copies of the specified object. |

| Exceptions ||
|--------------------------------------|-----------|
| `java.lang.IllegalArgumentException` | if`n < 0` |

**See Also**

- [java.util.List#addAll(Collection)](https://developer.android.com/reference/kotlin/java/util/List#addAll(kotlin.collections.Collection))
- [java.util.List#addAll(int, Collection)](https://developer.android.com/reference/kotlin/java/util/List#addAll(kotlin.Int,%20kotlin.collections.MutableCollection)) 

### newSequencedSetFromMap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> newSequencedSetFromMap(map: SequencedMap<E, Boolean!>): SequencedSet<E>
```

Returns a sequenced set backed by the specified map. The resulting set displays the same ordering, concurrency, and performance characteristics as the backing map. In essence, this factory method provides a [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet) implementation corresponding to any [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap) implementation.

Each method invocation on the set returned by this method results in exactly one method invocation on the backing map or its`keySet`view, with one exception. The`addAll`method is implemented as a sequence of`put`invocations on the backing map.

The specified map must be empty at the time this method is invoked, and should not be accessed directly after this method returns. These conditions are ensured if the map is created empty, passed directly to this method, and no reference to the map is retained.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the map keys and of the objects in the returned set |
| `map` | [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap)\<E, [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:the backing map |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------|
| [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)<E> | the set backed by the map |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if`map`is not empty |

### newSetFromMap

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> newSetFromMap(map: MutableMap<E, Boolean!>): MutableSet<E>
```

Returns a set backed by the specified map. The resulting set displays the same ordering, concurrency, and performance characteristics as the backing map. In essence, this factory method provides a [Set](https://developer.android.com/reference/kotlin/java/util/Set) implementation corresponding to any [Map](https://developer.android.com/reference/kotlin/java/util/Map) implementation. There is no need to use this method on a [Map](https://developer.android.com/reference/kotlin/java/util/Map) implementation that already has a corresponding [Set](https://developer.android.com/reference/kotlin/java/util/Set) implementation (such as [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap) or [TreeMap](https://developer.android.com/reference/kotlin/java/util/TreeMap)).

Each method invocation on the set returned by this method results in exactly one method invocation on the backing map or its`keySet`view, with one exception. The`addAll`method is implemented as a sequence of`put`invocations on the backing map.

The specified map must be empty at the time this method is invoked, and should not be accessed directly after this method returns. These conditions are ensured if the map is created empty, passed directly to this method, and no reference to the map is retained, as illustrated in the following code fragment: 

```kotlin
Set<Object> weakHashSet = Collections.newSetFromMap(
         new WeakHashMap<Object, Boolean>());
  
```

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the class of the map keys and of the objects in the returned set |
| `map` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<E, [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>:the backing map |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | the set backed by the map |

| Exceptions ||
|--------------------------------------|---------------------|
| `java.lang.IllegalArgumentException` | if`map`is not empty |

### replaceAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> replaceAll(
    list: MutableList<T>, 
    oldVal: T, 
    newVal: T
): Boolean
```

Replaces all occurrences of one specified value in a list with another. More formally, replaces with`newVal`each element`e`in`list`such that`(oldVal==null ? e==null : oldVal.equals(e))`. (This method has no effect on the size of the list.)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:the list in which replacement is to occur. |
| `oldVal` | T:the old value to be replaced. |
| `newVal` | T:the new value with which`oldVal`is to be replaced. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if`list`contained one or more elements`e`such that`(oldVal==null ? e==null : oldVal.equals(e))`. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

### reverse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun reverse(list: MutableList<*>): Unit
```

Reverses the order of the elements in the specified list.

This method runs in linear time.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list whose elements are to be reversed. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

**See Also**

- [java.util.List#reversed](https://developer.android.com/reference/kotlin/java/util/List#reversed()) 

### reverseOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> reverseOrder(): Comparator<T>
```

Returns a comparator that imposes the reverse of the*natural ordering* on a collection of objects that implement the`Comparable`interface. (The natural ordering is the ordering imposed by the objects' own`compareTo`method.) This enables a simple idiom for sorting (or maintaining) collections (or arrays) of objects that implement the`Comparable`interface in reverse-natural-order. For example, suppose`a`is an array of strings. Then: 

```kotlin
Arrays.sort(a, Collections.reverseOrder());
  
```
sorts the array in reverse-lexicographic (alphabetical) order.

<br />

The returned comparator is serializable.

| Parameters ||
|-------|-----------------------------------------------------|
| `<T>` | the class of the objects compared by the comparator |

| Return ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<T> | A comparator that imposes the reverse of the*natural ordering* on a collection of objects that implement the`Comparable`interface. |

**See Also**

- [java.lang.Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) 

### reverseOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> reverseOrder(cmp: Comparator<T>?): Comparator<T>
```

Returns a comparator that imposes the reverse ordering of the specified comparator. If the specified comparator is`null`, this method is equivalent to [reverseOrder()](https://developer.android.com/reference/kotlin/java/util/Collections#reverseOrder())(in other words, it returns a comparator that imposes the reverse of the*natural ordering*on a collection of objects that implement the Comparable interface).

The returned comparator is serializable (assuming the specified comparator is also serializable or`null`).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects compared by the comparator |
| `cmp` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<T\>?:a comparator who's ordering is to be reversed by the returned comparator or`null` |

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)<T> | A comparator that imposes the reverse ordering of the specified comparator. |

### rotate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rotate(
    list: MutableList<*>, 
    distance: Int
): Unit
```

Rotates the elements in the specified list by the specified distance. After calling this method, the element at index`i`will be the element previously at index`(i - distance)`mod`list.size()`, for all values of`i`between`0`and`list.size()-1`, inclusive. (This method has no effect on the size of the list.)

For example, suppose`list`comprises`[t, a, n, k, s]`. After invoking`Collections.rotate(list, 1)`(or`Collections.rotate(list, -4)`),`list`will comprise`[s, t, a, n, k]`.

Note that this method can usefully be applied to sublists to move one or more elements within a list while preserving the order of the remaining elements. For example, the following idiom moves the element at index`j`forward to position`k`(which must be greater than or equal to`j`): 

```kotlin
Collections.rotate(list.subList(j, k+1), -1);
  
```
To make this concrete, suppose`list`comprises`[a, b, c, d, e]`. To move the element at index`1`(`b`) forward two positions, perform the following invocation: 

```kotlin
Collections.rotate(l.subList(1, 4), -1);
  
```
The resulting list is`[a, c, d, b, e]`.

To move more than one element forward, increase the absolute value of the rotation distance. To move elements backward, use a positive shift distance.

If the specified list is small or implements the [RandomAccess](https://developer.android.com/reference/kotlin/java/util/RandomAccess) interface, this implementation exchanges the first element into the location it should go, and then repeatedly exchanges the displaced element into the location it should go until a displaced element is swapped into the first element. If necessary, the process is repeated on the second and successive elements, until the rotation is complete. If the specified list is large and doesn't implement the`RandomAccess`interface, this implementation breaks the list into two sublist views around index`-distance mod size`. Then the [reverse(java.util.List)](https://developer.android.com/reference/kotlin/java/util/Collections#reverse(kotlin.collections.MutableList))method is invoked on each sublist view, and finally it is invoked on the entire list. For a more complete description of both algorithms, see Section 2.3 of Jon Bentley's*Programming Pearls*(Addison-Wesley, 1986).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list to be rotated. |
| `distance` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the distance to rotate the list. There are no constraints on this value; it may be zero, negative, or greater than`list.size()`. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

### shuffle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun shuffle(list: MutableList<*>): Unit
```

Randomly permutes the specified list using a default source of randomness. All permutations occur with approximately equal likelihood.

The hedge "approximately" is used in the foregoing description because default source of randomness is only approximately an unbiased source of independently chosen bits. If it were a perfect source of randomly chosen bits, then the algorithm would choose permutations with perfect uniformity.

This implementation traverses the list backwards, from the last element up to the second, repeatedly swapping a randomly selected element into the "current position". Elements are randomly selected from the portion of the list that runs from the first element to the current position, inclusive.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list to be shuffled. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

### shuffle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun shuffle(
    list: MutableList<*>, 
    rnd: Random
): Unit
```

Randomly permute the specified list using the specified source of randomness.

This method is equivalent to [shuffle(java.util.List,java.util.random.RandomGenerator)](https://developer.android.com/reference/kotlin/java/util/Collections#shuffle(kotlin.collections.MutableList,%20java.util.random.RandomGenerator))and exists for backward compatibility. The [shuffle(java.util.List,java.util.random.RandomGenerator)](https://developer.android.com/reference/kotlin/java/util/Collections#shuffle(kotlin.collections.MutableList,%20java.util.random.RandomGenerator))method is preferred, as it is not limited to random generators that extend the [Random](https://developer.android.com/reference/kotlin/java/util/Random) class.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list to be shuffled. |
| `rnd` | [Random](https://developer.android.com/reference/kotlin/java/util/Random):the source of randomness to use to shuffle the list. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

### shuffle

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun shuffle(
    list: MutableList<*>, 
    rnd: RandomGenerator
): Unit
```

Randomly permute the specified list using the specified source of randomness. All permutations occur with equal likelihood assuming that the source of randomness is fair.

This implementation traverses the list backwards, from the last element up to the second, repeatedly swapping a randomly selected element into the "current position". Elements are randomly selected from the portion of the list that runs from the first element to the current position, inclusive.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:the list to be shuffled. |
| `rnd` | [RandomGenerator](https://developer.android.com/reference/kotlin/java/util/random/RandomGenerator):the source of randomness to use to shuffle the list. |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the specified list or its list-iterator does not support the`set`operation. |

### singleton

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> singleton(o: T): MutableSet<T>
```

Returns an immutable set containing only the specified object. The returned set is serializable.

| Parameters ||
|-------|-----------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `o` | T:the sole object to be stored in the returned set. |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<T> | an immutable set containing only the specified object. |

### singletonList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> singletonList(o: T): MutableList<T>
```

Returns an immutable list containing only the specified object. The returned list is serializable.

| Parameters ||
|-------|------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `o` | T:the sole object to be stored in the returned list. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | an immutable list containing only the specified object. |

### singletonMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> singletonMap(
    key: K, 
    value: V
): MutableMap<K, V>
```

Returns an immutable map, mapping only the specified key to the specified value. The returned map is serializable.

| Parameters ||
|---------|--------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `key` | K:the sole key to be stored in the returned map. |
| `value` | V:the value to which the returned map maps`key`. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V> | an immutable map containing only the specified key-value mapping. |

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Comparable<T>!> sort(list: MutableList<T>): Unit
```

Sorts the specified list into ascending order, according to the [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) of its elements. All elements in the list must implement the [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) interface. Furthermore, all elements in the list must be*mutually comparable* (that is,`e1.compareTo(e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the list).

This sort is guaranteed to be*stable*: equal elements will not be reordered as a result of the sort.

The specified list must be modifiable, but need not be resizable.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:the list to be sorted. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the list contains elements that are not*mutually comparable*(for example, strings and integers). |
| `java.lang.UnsupportedOperationException` | if the specified list's list-iterator does not support the`set`operation. |
| `java.lang.IllegalArgumentException` | (optional) if the implementation detects that the natural ordering of the list elements is found to violate the [Comparable](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) contract |

**See Also**

- [java.util.List#sort(Comparator)](https://developer.android.com/reference/kotlin/java/util/List#sort(java.util.Comparator)) 

### sort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> sort(
    list: MutableList<T>, 
    c: Comparator<in T>?
): Unit
```

Sorts the specified list according to the order induced by the specified comparator. All elements in the list must be*mutually comparable* using the specified comparator (that is,`c.compare(e1, e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the list).

This sort is guaranteed to be*stable*: equal elements will not be reordered as a result of the sort.

The specified list must be modifiable, but need not be resizable.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:the list to be sorted. |
| `c` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<inT\>?:the comparator to determine the order of the list. A`null`value indicates that the elements'*natural ordering*should be used. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the list contains elements that are not*mutually comparable*using the specified comparator. |
| `java.lang.UnsupportedOperationException` | if the specified list's list-iterator does not support the`set`operation. |
| `java.lang.IllegalArgumentException` | (optional) if the comparator is found to violate the [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator) contract |

**See Also**

- [java.util.List#sort(Comparator)](https://developer.android.com/reference/kotlin/java/util/List#sort(java.util.Comparator)) 

### swap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun swap(
    list: MutableList<*>, 
    i: Int, 
    j: Int
): Unit
```

Swaps the elements at the specified positions in the specified list. (If the specified positions are equal, invoking this method leaves the list unchanged.)

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>:The list in which to swap elements. |
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of one element to be swapped. |
| `j` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the other element to be swapped. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if either`i`or`j`is out of range (i \< 0 || i \>= list.size() || j \< 0 || j \>= list.size()). |

### synchronizedCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> synchronizedCollection(c: MutableCollection<T>): MutableCollection<T>
```

Returns a synchronized (thread-safe) collection backed by the specified collection. In order to guarantee serial access, it is critical that**all**access to the backing collection is accomplished through the returned collection.

It is imperative that the user manually synchronize on the returned collection when traversing it via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
Collection c = Collections.synchronizedCollection(myCollection);
      ...
   synchronized (c) {
       Iterator i = c.iterator(); // Must be in the synchronized block
       while (i.hasNext())
          foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned collection does*not* pass the`hashCode`and`equals`operations through to the backing collection, but relies on`Object`'s equals and hashCode methods. This is necessary to preserve the contracts of these operations in the case that the backing collection is a set or a list.

The returned collection will be serializable if the specified collection is serializable.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<T\>:the collection to be "wrapped" in a synchronized collection. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T> | a synchronized view of the specified collection. |

### synchronizedList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> synchronizedList(list: MutableList<T>): MutableList<T>
```

Returns a synchronized (thread-safe) list backed by the specified list. In order to guarantee serial access, it is critical that**all**access to the backing list is accomplished through the returned list.

It is imperative that the user manually synchronize on the returned list when traversing it via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
List list = Collections.synchronizedList(new ArrayList());
       ...
   synchronized (list) {
       Iterator i = list.iterator(); // Must be in synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned list will be serializable if the specified list is serializable.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\>:the list to be "wrapped" in a synchronized list. |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | a synchronized view of the specified list. |

### synchronizedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> synchronizedMap(m: MutableMap<K, V>): MutableMap<K, V>
```

Returns a synchronized (thread-safe) map backed by the specified map. In order to guarantee serial access, it is critical that**all**access to the backing map is accomplished through the returned map.

It is imperative that the user manually synchronize on the returned map when traversing any of its collection views via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
Map m = Collections.synchronizedMap(new HashMap());
       ...
   Set s = m.keySet();  // Needn't be in synchronized block
       ...
   synchronized (m) {  // Synchronizing on m, not s!
       Iterator i = s.iterator(); // Must be in synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned map will be serializable if the specified map is serializable.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<K,V\>:the map to be "wrapped" in a synchronized map. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V> | a synchronized view of the specified map. |

### synchronizedNavigableMap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> synchronizedNavigableMap(m: NavigableMap<K, V>): NavigableMap<K, V>
```

Returns a synchronized (thread-safe) navigable map backed by the specified navigable map. In order to guarantee serial access, it is critical that**all**access to the backing navigable map is accomplished through the returned navigable map (or its views).

It is imperative that the user manually synchronize on the returned navigable map when traversing any of its collection views, or the collections views of any of its`subMap`,`headMap`or`tailMap`views, via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
NavigableMap m = Collections.synchronizedNavigableMap(new TreeMap());
       ...
   Set s = m.keySet();  // Needn't be in synchronized block
       ...
   synchronized (m) {  // Synchronizing on m, not s!
       Iterator i = s.iterator(); // Must be in synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
or: 

```kotlin
NavigableMap m = Collections.synchronizedNavigableMap(new TreeMap());
   NavigableMap m2 = m.subMap(foo, true, bar, false);
       ...
   Set s2 = m2.keySet();  // Needn't be in synchronized block
       ...
   synchronized (m) {  // Synchronizing on m, not m2 or s2!
       Iterator i = s2.iterator(); // Must be in synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned navigable map will be serializable if the specified navigable map is serializable.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,V\>:the navigable map to be "wrapped" in a synchronized navigable map |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `V> | a synchronized view of the specified navigable map. |

### synchronizedNavigableSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> synchronizedNavigableSet(s: NavigableSet<T>): NavigableSet<T>
```

Returns a synchronized (thread-safe) navigable set backed by the specified navigable set. In order to guarantee serial access, it is critical that**all**access to the backing navigable set is accomplished through the returned navigable set (or its views).

It is imperative that the user manually synchronize on the returned navigable set when traversing it, or any of its`subSet`,`headSet`, or`tailSet`views, via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
NavigableSet s = Collections.synchronizedNavigableSet(new TreeSet());
       ...
   synchronized (s) {
       Iterator i = s.iterator(); // Must be in the synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
or: 

```kotlin
NavigableSet s = Collections.synchronizedNavigableSet(new TreeSet());
   NavigableSet s2 = s.headSet(foo, true);
       ...
   synchronized (s) {  // Note: s, not s2!!!
       Iterator i = s2.iterator(); // Must be in the synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned navigable set will be serializable if the specified navigable set is serializable.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<T\>:the navigable set to be "wrapped" in a synchronized navigable set |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<T> | a synchronized view of the specified navigable set |

### synchronizedSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> synchronizedSet(s: MutableSet<T>): MutableSet<T>
```

Returns a synchronized (thread-safe) set backed by the specified set. In order to guarantee serial access, it is critical that**all**access to the backing set is accomplished through the returned set.

It is imperative that the user manually synchronize on the returned collection when traversing it via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
Set s = Collections.synchronizedSet(new HashSet());
       ...
   synchronized (s) {
       Iterator i = s.iterator(); // Must be in the synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned set will be serializable if the specified set is serializable.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<T\>:the set to be "wrapped" in a synchronized set. |

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<T> | a synchronized view of the specified set. |

### synchronizedSortedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> synchronizedSortedMap(m: SortedMap<K, V>): SortedMap<K, V>
```

Returns a synchronized (thread-safe) sorted map backed by the specified sorted map. In order to guarantee serial access, it is critical that**all**access to the backing sorted map is accomplished through the returned sorted map (or its views).

It is imperative that the user manually synchronize on the returned sorted map when traversing any of its collection views, or the collections views of any of its`subMap`,`headMap`or`tailMap`views, via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
SortedMap m = Collections.synchronizedSortedMap(new TreeMap());
       ...
   Set s = m.keySet();  // Needn't be in synchronized block
       ...
   synchronized (m) {  // Synchronizing on m, not s!
       Iterator i = s.iterator(); // Must be in synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
or: 

```kotlin
SortedMap m = Collections.synchronizedSortedMap(new TreeMap());
   SortedMap m2 = m.subMap(foo, bar);
       ...
   Set s2 = m2.keySet();  // Needn't be in synchronized block
       ...
   synchronized (m) {  // Synchronizing on m, not m2 or s2!
       Iterator i = s2.iterator(); // Must be in synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned sorted map will be serializable if the specified sorted map is serializable.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,V\>:the sorted map to be "wrapped" in a synchronized sorted map. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `V> | a synchronized view of the specified sorted map. |

### synchronizedSortedSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> synchronizedSortedSet(s: SortedSet<T>): SortedSet<T>
```

Returns a synchronized (thread-safe) sorted set backed by the specified sorted set. In order to guarantee serial access, it is critical that**all**access to the backing sorted set is accomplished through the returned sorted set (or its views).

It is imperative that the user manually synchronize on the returned sorted set when traversing it or any of its`subSet`,`headSet`, or`tailSet`views via [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator), [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator) or [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream): 

```kotlin
SortedSet s = Collections.synchronizedSortedSet(new TreeSet());
       ...
   synchronized (s) {
       Iterator i = s.iterator(); // Must be in the synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
or: 

```kotlin
SortedSet s = Collections.synchronizedSortedSet(new TreeSet());
   SortedSet s2 = s.headSet(foo);
       ...
   synchronized (s) {  // Note: s, not s2!!!
       Iterator i = s2.iterator(); // Must be in the synchronized block
       while (i.hasNext())
           foo(i.next());
   }
  
```
Failure to follow this advice may result in non-deterministic behavior.

The returned sorted set will be serializable if the specified sorted set is serializable.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<T\>:the sorted set to be "wrapped" in a synchronized sorted set. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<T> | a synchronized view of the specified sorted set. |

### unmodifiableCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableCollection(c: MutableCollection<out T>): MutableCollection<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified collection. Query operations on the returned collection "read through" to the specified collection, and attempts to modify the returned collection, whether direct or via its iterator, result in an`UnsupportedOperationException`.

The returned collection does*not* pass the hashCode and equals operations through to the backing collection, but relies on`Object`'s`equals`and`hashCode`methods. This is necessary to preserve the contracts of these operations in the case that the backing collection is a set or a list.

The returned collection will be serializable if the specified collection is serializable.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outT\>:the collection for which an unmodifiable view is to be returned. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<T> | an unmodifiable view of the specified collection. |

### unmodifiableList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableList(list: MutableList<out T>): MutableList<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified list. Query operations on the returned list "read through" to the specified list, and attempts to modify the returned list, whether direct or via its iterator, result in an`UnsupportedOperationException`.

The returned list will be serializable if the specified list is serializable. Similarly, the returned list will implement [RandomAccess](https://developer.android.com/reference/kotlin/java/util/RandomAccess) if the specified list does.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the list |
| `list` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<outT\>:the list for which an unmodifiable view is to be returned. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | an unmodifiable view of the specified list. |

### unmodifiableMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> unmodifiableMap(m: MutableMap<out K, out V>): MutableMap<K, V>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified map. Query operations on the returned map "read through" to the specified map, and attempts to modify the returned map, whether direct or via its collection views, result in an`UnsupportedOperationException`.

The returned map will be serializable if the specified map is serializable.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\<outK,outV\>:the map for which an unmodifiable view is to be returned. |

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)<K,` `V> | an unmodifiable view of the specified map. |

### unmodifiableNavigableMap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> unmodifiableNavigableMap(m: NavigableMap<K, out V>): NavigableMap<K, V>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified navigable map. Query operations on the returned navigable map "read through" to the specified navigable map. Attempts to modify the returned navigable map, whether direct, via its collection views, or via its`subMap`,`headMap`, or`tailMap`views, result in an`UnsupportedOperationException`.

The returned navigable map will be serializable if the specified navigable map is serializable.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)\<K,outV\>:the navigable map for which an unmodifiable view is to be returned |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [NavigableMap](https://developer.android.com/reference/kotlin/java/util/NavigableMap)<K,` `V> | an unmodifiable view of the specified navigable map |

### unmodifiableNavigableSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableNavigableSet(s: NavigableSet<T>): NavigableSet<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified navigable set. Query operations on the returned navigable set "read through" to the specified navigable set. Attempts to modify the returned navigable set, whether direct, via its iterator, or via its`subSet`,`headSet`, or`tailSet`views, result in an`UnsupportedOperationException`.

The returned navigable set will be serializable if the specified navigable set is serializable.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)\<T\>:the navigable set for which an unmodifiable view is to be returned |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [NavigableSet](https://developer.android.com/reference/kotlin/java/util/NavigableSet)<T> | an unmodifiable view of the specified navigable set |

### unmodifiableSequencedCollection

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableSequencedCollection(c: SequencedCollection<out T>): SequencedCollection<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified`SequencedCollection`. Query operations on the returned collection "read through" to the specified collection, and attempts to modify the returned collection, whether direct or via its iterator, result in an`UnsupportedOperationException`.

The returned collection does*not* pass the`hashCode`and`equals`operations through to the backing collection, but relies on`Object`'s`equals`and`hashCode`methods. This is necessary to preserve the contracts of these operations in the case that the backing collection is a set or a list.

The returned collection will be serializable if the specified collection is serializable.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the collection |
| `c` | [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)\<outT\>:the collection for which an unmodifiable view is to be returned. |

| Return ||
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [SequencedCollection](https://developer.android.com/reference/kotlin/java/util/SequencedCollection)<T> | an unmodifiable view of the specified collection. |

### unmodifiableSequencedMap

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> unmodifiableSequencedMap(m: SequencedMap<out K, out V>): SequencedMap<K, V>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified`SequencedMap`. Query operations on the returned map "read through" to the specified map, and attempts to modify the returned map, whether direct or via its collection views, result in an`UnsupportedOperationException`.

The returned map will be serializable if the specified map is serializable.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap)\<outK,outV\>:the map for which an unmodifiable view is to be returned. |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------|
| [SequencedMap](https://developer.android.com/reference/kotlin/java/util/SequencedMap)<K,` `V> | an unmodifiable view of the specified map. |

### unmodifiableSequencedSet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableSequencedSet(s: SequencedSet<out T>): SequencedSet<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified`SequencedSet`. Query operations on the returned set "read through" to the specified set, and attempts to modify the returned set, whether direct or via its iterator, result in an`UnsupportedOperationException`.

The returned set will be serializable if the specified set is serializable.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)\<outT\>:the set for which an unmodifiable view is to be returned. |

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| [SequencedSet](https://developer.android.com/reference/kotlin/java/util/SequencedSet)<T> | an unmodifiable view of the specified sequenced set. |

### unmodifiableSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableSet(s: MutableSet<out T>): MutableSet<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified set. Query operations on the returned set "read through" to the specified set, and attempts to modify the returned set, whether direct or via its iterator, result in an`UnsupportedOperationException`.

The returned set will be serializable if the specified set is serializable.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<outT\>:the set for which an unmodifiable view is to be returned. |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<T> | an unmodifiable view of the specified set. |

### unmodifiableSortedMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <K : Any!, V : Any!> unmodifiableSortedMap(m: SortedMap<K, out V>): SortedMap<K, V>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified sorted map. Query operations on the returned sorted map "read through" to the specified sorted map. Attempts to modify the returned sorted map, whether direct, via its collection views, or via its`subMap`,`headMap`, or`tailMap`views, result in an`UnsupportedOperationException`.

The returned sorted map will be serializable if the specified sorted map is serializable.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<K>` | the class of the map keys |
| `<V>` | the class of the map values |
| `m` | [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)\<K,outV\>:the sorted map for which an unmodifiable view is to be returned. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------|
| [SortedMap](https://developer.android.com/reference/kotlin/java/util/SortedMap)<K,` `V> | an unmodifiable view of the specified sorted map. |

### unmodifiableSortedSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> unmodifiableSortedSet(s: SortedSet<T>): SortedSet<T>
```

Returns an [unmodifiable view](https://developer.android.com/reference/kotlin/java/util/Collection#unmodview) of the specified sorted set. Query operations on the returned sorted set "read through" to the specified sorted set. Attempts to modify the returned sorted set, whether direct, via its iterator, or via its`subSet`,`headSet`, or`tailSet`views, result in an`UnsupportedOperationException`.

The returned sorted set will be serializable if the specified sorted set is serializable.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the class of the objects in the set |
| `s` | [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)\<T\>:the sorted set for which an unmodifiable view is to be returned. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [SortedSet](https://developer.android.com/reference/kotlin/java/util/SortedSet)<T> | an unmodifiable view of the specified sorted set. |

## Properties

### EMPTY_LIST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMPTY_LIST: MutableList<Any?>
```

The empty list (immutable). This list is serializable. 
**See Also**

- <https://developer.android.com/reference/kotlin/java/util/Collections#emptyList()> 

### EMPTY_MAP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMPTY_MAP: MutableMap<Any?, Any?>
```

The empty map (immutable). This map is serializable. 
**See Also**

- <https://developer.android.com/reference/kotlin/java/util/Collections#emptyMap()> 

### EMPTY_SET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EMPTY_SET: MutableSet<Any?>
```

The empty set (immutable). This set is serializable. 
**See Also**

- <https://developer.android.com/reference/kotlin/java/util/Collections#emptySet()>

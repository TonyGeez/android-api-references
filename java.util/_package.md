# java.util

# java.util

## Interfaces

| [Collection](../java/util/Collection.md) | The root interface in the*collection hierarchy*. |
| --- | --- |
| [Comparator](../java/util/Comparator.md) | A comparison function, which imposes a*total ordering*on some collection of objects. |
| [Deque](../java/util/Deque.md) | A linear collection that supports element insertion and removal at both ends. |
| [Enumeration](../java/util/Enumeration.md) | An object that implements the Enumeration interface generates a series of elements, one at a time. |
| --- | --- |
| [EventListener](../java/util/EventListener.md) | A tagging interface that all event listener interfaces must extend. |
| [Formattable](../java/util/Formattable.md) | The`Formattable`interface must be implemented by any class that needs to perform custom formatting using the`'s'`conversion specifier of [java.util.Formatter](../java/util/Formatter.md). |
| [Iterator](../java/util/Iterator.md) | An iterator over a collection. |
| --- | --- |
| [List](../java/util/List.md) | An ordered collection, where the user has precise control over where in the list each element is inserted. |
| [ListIterator](../java/util/ListIterator.md) | An iterator for lists that allows the programmer to traverse the list in either direction, modify the list during iteration, and obtain the iterator's current position in the list. |
| [Map](../java/util/Map.md) | An object that maps keys to values. |
| --- | --- |
| [NavigableMap](../java/util/NavigableMap.md) | A [SortedMap](../java/util/SortedMap.md) extended with navigation methods returning the closest matches for given search targets. |
| [NavigableSet](../java/util/NavigableSet.md) | A [SortedSet](../java/util/SortedSet.md) extended with navigation methods reporting closest matches for given search targets. |
| [Observer](../java/util/Observer.md) | A class can implement the`Observer`interface when it wants to be informed of changes in observable objects. |
| --- | --- |
| [PrimitiveIterator](../java/util/PrimitiveIterator.md) | A base type for primitive specializations of`Iterator`. |
| [Queue](../java/util/Queue.md) | A collection designed for holding elements prior to processing. |
| [RandomAccess](../java/util/RandomAccess.md) | Marker interface used by`List`implementations to indicate that they support fast (generally constant time) random access. |
| --- | --- |
| [SequencedCollection](../java/util/SequencedCollection.md) | A collection that has a well-defined encounter order, that supports operations at both ends, and that is reversible. |
| [SequencedMap](../java/util/SequencedMap.md) | A Map that has a well-defined encounter order, that supports operations at both ends, and that is reversible. |
| [SequencedSet](../java/util/SequencedSet.md) | A collection that is both a [SequencedCollection](../java/util/SequencedCollection.md) and a [Set](../java/util/Set.md). |
| --- | --- |
| [Provider](../java/util/ServiceLoader.Provider.md) | Represents a service provider located by`ServiceLoader`. |
| [Set](../java/util/Set.md) | A collection that contains no duplicate elements. |
| [SortedMap](../java/util/SortedMap.md) | A [Map](../java/util/Map.md) that further provides a*total ordering*on its keys. |
| --- | --- |
| [SortedSet](../java/util/SortedSet.md) | A [Set](../java/util/Set.md) that further provides a*total ordering*on its elements. |
| [Spliterator](../java/util/Spliterator.md) | An object for traversing and partitioning elements of a source. |

## Classes

| [AbstractCollection](../java/util/AbstractCollection.md) | This class provides a skeletal implementation of the`Collection`interface, to minimize the effort required to implement this interface. |
| --- | --- |
| [AbstractList](../java/util/AbstractList.md) | This class provides a skeletal implementation of the [List](../java/util/List.md) interface to minimize the effort required to implement this interface backed by a "random access" data store (such as an array). |
| [AbstractMap](../java/util/AbstractMap.md) | This class provides a skeletal implementation of the`Map`interface, to minimize the effort required to implement this interface. |
| [AbstractQueue](../java/util/AbstractQueue.md) | This class provides skeletal implementations of some [Queue](../java/util/Queue.md) operations. |
| --- | --- |
| [AbstractSequentialList](../java/util/AbstractSequentialList.md) | This class provides a skeletal implementation of the`List`interface to minimize the effort required to implement this interface backed by a "sequential access" data store (such as a linked list). |
| [AbstractSet](../java/util/AbstractSet.md) | This class provides a skeletal implementation of the`Set`interface to minimize the effort required to implement this interface. |
| [ArrayDeque](../java/util/ArrayDeque.md) | Resizable-array implementation of the [Deque](../java/util/Deque.md) interface. |
| --- | --- |
| [ArrayList](../java/util/ArrayList.md) | Resizable-array implementation of the`List`interface. |
| [Arrays](../java/util/Arrays.md) | This class contains various methods for manipulating arrays (such as sorting and searching). |
| [Base64](../java/util/Base64.md) | This class consists exclusively of static methods for obtaining encoders and decoders for the Base64 encoding scheme. |
| --- | --- |
| [BitSet](../java/util/BitSet.md) | This class implements a vector of bits that grows as needed. |
| [Calendar](../java/util/Calendar.md) | The class is an abstract class that provides methods for converting between a specific instant in time and a set of [calendar fields](../java/util/Calendar.md) such as`YEAR``MONTH``DAY_OF_MONTH``HOUR`, and so on, and for manipulating the calendar fields, such as getting the date of the next week. |
| [Collections](../java/util/Collections.md) | This class consists exclusively of static methods that operate on or return collections. |
| --- | --- |
| [Currency](../java/util/Currency.md) | Represents a currency. |
| [Date](../java/util/Date.md) | The class`Date`represents a specific instant in time, with millisecond precision. |
| [Dictionary](../java/util/Dictionary.md) | The`Dictionary`class is the abstract parent of any class, such as`Hashtable`, which maps keys to values. |
| --- | --- |
| [DoubleSummaryStatistics](../java/util/DoubleSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. |
| [EnumMap](../java/util/EnumMap.md) | A specialized [Map](../java/util/Map.md) implementation for use with enum type keys. |
| [EnumSet](../java/util/EnumSet.md) | A specialized [Set](../java/util/Set.md) implementation for use with enum types. |
| --- | --- |
| [EventListenerProxy](../java/util/EventListenerProxy.md) | An abstract wrapper class for an`EventListener`class which associates a set of additional parameters with the listener. |
| [EventObject](../java/util/EventObject.md) | The root class from which all event state objects shall be derived. |
| [FormattableFlags](../java/util/FormattableFlags.md) | FormattableFlags are passed to the [Formattable.formatTo()](../java/util/Formattable.md))method and modify the output format for [Formattables](../java/util/Formattable.md). |
| --- | --- |
| [Formatter](../java/util/Formatter.md) | An interpreter for printf-style format strings. |
| [GregorianCalendar](../java/util/GregorianCalendar.md) | `GregorianCalendar`is a concrete subclass of`Calendar`and provides the standard calendar system used by most of the world. |
| [HashMap](../java/util/HashMap.md) | Hash table based implementation of the`Map`interface. |
| --- | --- |
| [HashSet](../java/util/HashSet.md) | This class implements the`Set`interface, backed by a hash table (actually a`HashMap`instance). |
| [Hashtable](../java/util/Hashtable.md) | This class implements a hash table, which maps keys to values. |
| [HexFormat](../java/util/HexFormat.md) | `HexFormat`converts between bytes and chars and hex-encoded strings which may include additional formatting markup such as prefixes, suffixes, and delimiters. |
| --- | --- |
| [IdentityHashMap](../java/util/IdentityHashMap.md) | This class implements the`Map`interface with a hash table, using reference-equality in place of object-equality when comparing keys (and values). |
| [IntSummaryStatistics](../java/util/IntSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. |
| [LinkedHashMap](../java/util/LinkedHashMap.md) | Hash table and linked list implementation of the`Map`interface, with well-defined encounter order. |
| --- | --- |
| [LinkedHashSet](../java/util/LinkedHashSet.md) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. |
| [LinkedList](../java/util/LinkedList.md) | Doubly-linked list implementation of the`List`and`Deque`interfaces. |
| [ListResourceBundle](../java/util/ListResourceBundle.md) | `ListResourceBundle`is an abstract subclass of`ResourceBundle`that manages resources for a locale in a convenient and easy to use list. |
| --- | --- |
| [Locale](../java/util/Locale.md) | A object represents a specific geographical, political, or cultural region. |
| [LongSummaryStatistics](../java/util/LongSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. |
| [Objects](../java/util/Objects.md) | This class consists of`static`utility methods for operating on objects, or checking certain conditions before operation. |
| --- | --- |
| [Observable](../java/util/Observable.md) | This class represents an observable object, or "data" in the model-view paradigm. |
| [Optional](../java/util/Optional.md) | A container object which may or may not contain a non-`null`value. |
| [OptionalDouble](../java/util/OptionalDouble.md) | A container object which may or may not contain a`double`value. |
| --- | --- |
| [OptionalInt](../java/util/OptionalInt.md) | A container object which may or may not contain an`int`value. |
| [OptionalLong](../java/util/OptionalLong.md) | A container object which may or may not contain a`long`value. |
| [PriorityQueue](../java/util/PriorityQueue.md) | An unbounded priority [queue](../java/util/Queue.md) based on a priority heap. |
| --- | --- |
| [Properties](../java/util/Properties.md) | The`Properties`class represents a persistent set of properties. |
| [PropertyPermission](../java/util/PropertyPermission.md) | Legacy security code; do not use. |
| [PropertyResourceBundle](../java/util/PropertyResourceBundle.md) | `PropertyResourceBundle`is a concrete subclass of`ResourceBundle`that manages resources for a locale using a set of static strings from a property file. |
| --- | --- |
| [Random](../java/util/Random.md) | An instance of this class is used to generate a stream of pseudorandom numbers; its period is only 248. |
| [ResourceBundle](../java/util/ResourceBundle.md) | Resource bundles contain locale-specific objects. |
| [Scanner](../java/util/Scanner.md) | A simple text scanner which can parse primitive types and strings using regular expressions. |
| --- | --- |
| [ServiceLoader](../java/util/ServiceLoader.md) | A facility to load implementations of a service. |
| [SimpleTimeZone](../java/util/SimpleTimeZone.md) | `SimpleTimeZone`is a concrete subclass of`TimeZone`that represents a time zone for use with a Gregorian calendar. |
| [Spliterators](../java/util/Spliterators.md) | Static classes and methods for operating on or creating instances of [Spliterator](../java/util/Spliterator.md) and its primitive specializations [Spliterator.OfInt](../java/util/Spliterator.OfInt.md), [Spliterator.OfLong](../java/util/Spliterator.OfLong.md), and [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md). |
| --- | --- |
| [SplittableRandom](../java/util/SplittableRandom.md) | A generator of uniform pseudorandom values (with period 264) applicable for use in (among other contexts) isolated parallel computations that may generate subtasks. |
| [Stack](../java/util/Stack.md) | The`Stack`class represents a last-in-first-out (LIFO) stack of objects. |
| [StringJoiner](../java/util/StringJoiner.md) | `StringJoiner`is used to construct a sequence of characters separated by a delimiter and optionally starting with a supplied prefix and ending with a supplied suffix. |
| --- | --- |
| [StringTokenizer](../java/util/StringTokenizer.md) | The string tokenizer class allows an application to break a string into tokens. |
| [Timer](../java/util/Timer.md) | A facility for threads to schedule tasks for future execution in a background thread. |
| [TimerTask](../java/util/TimerTask.md) | A task that can be scheduled for one-time or repeated execution by a [Timer](../java/util/Timer.md). |
| --- | --- |
| [TimeZone](../java/util/TimeZone.md) | represents a time zone offset, and also figures out daylight savings. |
| [TreeMap](../java/util/TreeMap.md) | A Red-Black tree based [NavigableMap](../java/util/NavigableMap.md) implementation. |
| [TreeSet](../java/util/TreeSet.md) | A [NavigableSet](../java/util/NavigableSet.md) implementation based on a [TreeMap](../java/util/TreeMap.md). |
| --- | --- |
| [UUID](../java/util/UUID.md) | A class that represents an immutable universally unique identifier (UUID). |
| [Vector](../java/util/Vector.md) | The`Vector`class implements a growable array of objects. |
| [WeakHashMap](../java/util/WeakHashMap.md) | Hash table based implementation of the`Map`interface, with*weak keys*. |
| --- | --- |

## Exceptions

| [ConcurrentModificationException](../java/util/ConcurrentModificationException.md) | This exception may be thrown by methods that have detected concurrent modification of an object when such modification is not permissible. |
| --- | --- |
| [DuplicateFormatFlagsException](../java/util/DuplicateFormatFlagsException.md) | Unchecked exception thrown when duplicate flags are provided in the format specifier. |
| [EmptyStackException](../java/util/EmptyStackException.md) | Thrown by methods in the`Stack`class to indicate that the stack is empty. |
| [FormatFlagsConversionMismatchException](../java/util/FormatFlagsConversionMismatchException.md) | Unchecked exception thrown when a conversion and flag are incompatible. |
| --- | --- |
| [FormatterClosedException](../java/util/FormatterClosedException.md) | Unchecked exception thrown when the formatter has been closed. |
| [IllegalFormatCodePointException](../java/util/IllegalFormatCodePointException.md) | Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](../java/lang/Character.md))is passed to the [Formatter](../java/util/Formatter.md). |
| [IllegalFormatConversionException](../java/util/IllegalFormatConversionException.md) | Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type. |
| --- | --- |
| [IllegalFormatException](../java/util/IllegalFormatException.md) | Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments. |
| [IllegalFormatFlagsException](../java/util/IllegalFormatFlagsException.md) | Unchecked exception thrown when an illegal combination flags is given. |
| [IllegalFormatPrecisionException](../java/util/IllegalFormatPrecisionException.md) | Unchecked exception thrown when the precision is a negative value other than`-1`, the conversion does not support a precision, or the value is otherwise unsupported. |
| --- | --- |
| [IllegalFormatWidthException](../java/util/IllegalFormatWidthException.md) | Unchecked exception thrown when the format width is a negative value other than`-1`or is otherwise unsupported. |
| [IllformedLocaleException](../java/util/IllformedLocaleException.md) | Thrown by methods in [Locale](../java/util/Locale.md) and [Locale.Builder](../java/util/Locale.Builder.md) to indicate that an argument is not a well-formed BCP 47 tag. |
| [InputMismatchException](../java/util/InputMismatchException.md) | Thrown by a`Scanner`to indicate that the token retrieved does not match the pattern for the expected type, or that the token is out of range for the expected type. |
| --- | --- |
| [InvalidPropertiesFormatException](../java/util/InvalidPropertiesFormatException.md) | Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the [Properties](../java/util/Properties.md) specification. |
| [MissingFormatArgumentException](../java/util/MissingFormatArgumentException.md) | Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist. |
| [MissingFormatWidthException](../java/util/MissingFormatWidthException.md) | Unchecked exception thrown when the format width is required. |
| --- | --- |
| [MissingResourceException](../java/util/MissingResourceException.md) | Signals that a resource is missing. |
| [NoSuchElementException](../java/util/NoSuchElementException.md) | Thrown by various accessor methods to indicate that the element being requested does not exist. |
| [ServiceConfigurationError](../java/util/ServiceConfigurationError.md) | Error thrown when something goes wrong while locating, loading, or instantiating a service provider. |
| --- | --- |
| [TooManyListenersException](../java/util/TooManyListenersException.md) | The`TooManyListenersException `Exception is used as part of the Java Event model to annotate and implement a unicast special case of a multicast Event Source. |
| [UnknownFormatConversionException](../java/util/UnknownFormatConversionException.md) | Unchecked exception thrown when an unknown conversion is given. |
| [UnknownFormatFlagsException](../java/util/UnknownFormatFlagsException.md) | Unchecked exception thrown when an unknown flag is given. |
| --- | --- |

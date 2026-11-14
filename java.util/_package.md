# java.util

# java.util

## Interfaces

| [Collection](Collection.md) | The root interface in the*collection hierarchy*. |
| --- | --- |
| [Comparator](Comparator.md) | A comparison function, which imposes a*total ordering*on some collection of objects. |
| [Deque](Deque.md) | A linear collection that supports element insertion and removal at both ends. |
| [Enumeration](Enumeration.md) | An object that implements the Enumeration interface generates a series of elements, one at a time. |
| --- | --- |
| [EventListener](EventListener.md) | A tagging interface that all event listener interfaces must extend. |
| [Formattable](Formattable.md) | The`Formattable`interface must be implemented by any class that needs to perform custom formatting using the`'s'`conversion specifier of [java.util.Formatter](Formatter.md). |
| [Iterator](Iterator.md) | An iterator over a collection. |
| --- | --- |
| [List](List.md) | An ordered collection, where the user has precise control over where in the list each element is inserted. |
| [ListIterator](ListIterator.md) | An iterator for lists that allows the programmer to traverse the list in either direction, modify the list during iteration, and obtain the iterator's current position in the list. |
| [Map](Map.md) | An object that maps keys to values. |
| --- | --- |
| [NavigableMap](NavigableMap.md) | A [SortedMap](SortedMap.md) extended with navigation methods returning the closest matches for given search targets. |
| [NavigableSet](NavigableSet.md) | A [SortedSet](SortedSet.md) extended with navigation methods reporting closest matches for given search targets. |
| [Observer](Observer.md) | A class can implement the`Observer`interface when it wants to be informed of changes in observable objects. |
| --- | --- |
| [PrimitiveIterator](PrimitiveIterator.md) | A base type for primitive specializations of`Iterator`. |
| [Queue](Queue.md) | A collection designed for holding elements prior to processing. |
| [RandomAccess](RandomAccess.md) | Marker interface used by`List`implementations to indicate that they support fast (generally constant time) random access. |
| --- | --- |
| [SequencedCollection](SequencedCollection.md) | A collection that has a well-defined encounter order, that supports operations at both ends, and that is reversible. |
| [SequencedMap](SequencedMap.md) | A Map that has a well-defined encounter order, that supports operations at both ends, and that is reversible. |
| [SequencedSet](SequencedSet.md) | A collection that is both a [SequencedCollection](SequencedCollection.md) and a [Set](Set.md). |
| --- | --- |
| [Provider](../java/util/ServiceLoader.Provider.md) | Represents a service provider located by`ServiceLoader`. |
| [Set](Set.md) | A collection that contains no duplicate elements. |
| [SortedMap](SortedMap.md) | A [Map](Map.md) that further provides a*total ordering*on its keys. |
| --- | --- |
| [SortedSet](SortedSet.md) | A [Set](Set.md) that further provides a*total ordering*on its elements. |
| [Spliterator](Spliterator.md) | An object for traversing and partitioning elements of a source. |

## Classes

| [AbstractCollection](AbstractCollection.md) | This class provides a skeletal implementation of the`Collection`interface, to minimize the effort required to implement this interface. |
| --- | --- |
| [AbstractList](AbstractList.md) | This class provides a skeletal implementation of the [List](List.md) interface to minimize the effort required to implement this interface backed by a "random access" data store (such as an array). |
| [AbstractMap](AbstractMap.md) | This class provides a skeletal implementation of the`Map`interface, to minimize the effort required to implement this interface. |
| [AbstractQueue](AbstractQueue.md) | This class provides skeletal implementations of some [Queue](Queue.md) operations. |
| --- | --- |
| [AbstractSequentialList](AbstractSequentialList.md) | This class provides a skeletal implementation of the`List`interface to minimize the effort required to implement this interface backed by a "sequential access" data store (such as a linked list). |
| [AbstractSet](AbstractSet.md) | This class provides a skeletal implementation of the`Set`interface to minimize the effort required to implement this interface. |
| [ArrayDeque](ArrayDeque.md) | Resizable-array implementation of the [Deque](Deque.md) interface. |
| --- | --- |
| [ArrayList](ArrayList.md) | Resizable-array implementation of the`List`interface. |
| [Arrays](Arrays.md) | This class contains various methods for manipulating arrays (such as sorting and searching). |
| [Base64](Base64.md) | This class consists exclusively of static methods for obtaining encoders and decoders for the Base64 encoding scheme. |
| --- | --- |
| [BitSet](BitSet.md) | This class implements a vector of bits that grows as needed. |
| [Calendar](Calendar.md) | The class is an abstract class that provides methods for converting between a specific instant in time and a set of [calendar fields](Calendar.md) such as`YEAR``MONTH``DAY_OF_MONTH``HOUR`, and so on, and for manipulating the calendar fields, such as getting the date of the next week. |
| [Collections](Collections.md) | This class consists exclusively of static methods that operate on or return collections. |
| --- | --- |
| [Currency](Currency.md) | Represents a currency. |
| [Date](Date.md) | The class`Date`represents a specific instant in time, with millisecond precision. |
| [Dictionary](Dictionary.md) | The`Dictionary`class is the abstract parent of any class, such as`Hashtable`, which maps keys to values. |
| --- | --- |
| [DoubleSummaryStatistics](DoubleSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. |
| [EnumMap](EnumMap.md) | A specialized [Map](Map.md) implementation for use with enum type keys. |
| [EnumSet](EnumSet.md) | A specialized [Set](Set.md) implementation for use with enum types. |
| --- | --- |
| [EventListenerProxy](EventListenerProxy.md) | An abstract wrapper class for an`EventListener`class which associates a set of additional parameters with the listener. |
| [EventObject](EventObject.md) | The root class from which all event state objects shall be derived. |
| [FormattableFlags](FormattableFlags.md) | FormattableFlags are passed to the [Formattable.formatTo()](Formattable.md))method and modify the output format for [Formattables](Formattable.md). |
| --- | --- |
| [Formatter](Formatter.md) | An interpreter for printf-style format strings. |
| [GregorianCalendar](GregorianCalendar.md) | `GregorianCalendar`is a concrete subclass of`Calendar`and provides the standard calendar system used by most of the world. |
| [HashMap](HashMap.md) | Hash table based implementation of the`Map`interface. |
| --- | --- |
| [HashSet](HashSet.md) | This class implements the`Set`interface, backed by a hash table (actually a`HashMap`instance). |
| [Hashtable](Hashtable.md) | This class implements a hash table, which maps keys to values. |
| [HexFormat](HexFormat.md) | `HexFormat`converts between bytes and chars and hex-encoded strings which may include additional formatting markup such as prefixes, suffixes, and delimiters. |
| --- | --- |
| [IdentityHashMap](IdentityHashMap.md) | This class implements the`Map`interface with a hash table, using reference-equality in place of object-equality when comparing keys (and values). |
| [IntSummaryStatistics](IntSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. |
| [LinkedHashMap](LinkedHashMap.md) | Hash table and linked list implementation of the`Map`interface, with well-defined encounter order. |
| --- | --- |
| [LinkedHashSet](LinkedHashSet.md) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. |
| [LinkedList](LinkedList.md) | Doubly-linked list implementation of the`List`and`Deque`interfaces. |
| [ListResourceBundle](ListResourceBundle.md) | `ListResourceBundle`is an abstract subclass of`ResourceBundle`that manages resources for a locale in a convenient and easy to use list. |
| --- | --- |
| [Locale](Locale.md) | A object represents a specific geographical, political, or cultural region. |
| [LongSummaryStatistics](LongSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. |
| [Objects](Objects.md) | This class consists of`static`utility methods for operating on objects, or checking certain conditions before operation. |
| --- | --- |
| [Observable](Observable.md) | This class represents an observable object, or "data" in the model-view paradigm. |
| [Optional](Optional.md) | A container object which may or may not contain a non-`null`value. |
| [OptionalDouble](OptionalDouble.md) | A container object which may or may not contain a`double`value. |
| --- | --- |
| [OptionalInt](OptionalInt.md) | A container object which may or may not contain an`int`value. |
| [OptionalLong](OptionalLong.md) | A container object which may or may not contain a`long`value. |
| [PriorityQueue](PriorityQueue.md) | An unbounded priority [queue](Queue.md) based on a priority heap. |
| --- | --- |
| [Properties](Properties.md) | The`Properties`class represents a persistent set of properties. |
| [PropertyPermission](PropertyPermission.md) | Legacy security code; do not use. |
| [PropertyResourceBundle](PropertyResourceBundle.md) | `PropertyResourceBundle`is a concrete subclass of`ResourceBundle`that manages resources for a locale using a set of static strings from a property file. |
| --- | --- |
| [Random](Random.md) | An instance of this class is used to generate a stream of pseudorandom numbers; its period is only 248. |
| [ResourceBundle](ResourceBundle.md) | Resource bundles contain locale-specific objects. |
| [Scanner](Scanner.md) | A simple text scanner which can parse primitive types and strings using regular expressions. |
| --- | --- |
| [ServiceLoader](ServiceLoader.md) | A facility to load implementations of a service. |
| [SimpleTimeZone](SimpleTimeZone.md) | `SimpleTimeZone`is a concrete subclass of`TimeZone`that represents a time zone for use with a Gregorian calendar. |
| [Spliterators](Spliterators.md) | Static classes and methods for operating on or creating instances of [Spliterator](Spliterator.md) and its primitive specializations [Spliterator.OfInt](../java/util/Spliterator.OfInt.md), [Spliterator.OfLong](../java/util/Spliterator.OfLong.md), and [Spliterator.OfDouble](../java/util/Spliterator.OfDouble.md). |
| --- | --- |
| [SplittableRandom](SplittableRandom.md) | A generator of uniform pseudorandom values (with period 264) applicable for use in (among other contexts) isolated parallel computations that may generate subtasks. |
| [Stack](Stack.md) | The`Stack`class represents a last-in-first-out (LIFO) stack of objects. |
| [StringJoiner](StringJoiner.md) | `StringJoiner`is used to construct a sequence of characters separated by a delimiter and optionally starting with a supplied prefix and ending with a supplied suffix. |
| --- | --- |
| [StringTokenizer](StringTokenizer.md) | The string tokenizer class allows an application to break a string into tokens. |
| [Timer](Timer.md) | A facility for threads to schedule tasks for future execution in a background thread. |
| [TimerTask](TimerTask.md) | A task that can be scheduled for one-time or repeated execution by a [Timer](Timer.md). |
| --- | --- |
| [TimeZone](TimeZone.md) | represents a time zone offset, and also figures out daylight savings. |
| [TreeMap](TreeMap.md) | A Red-Black tree based [NavigableMap](NavigableMap.md) implementation. |
| [TreeSet](TreeSet.md) | A [NavigableSet](NavigableSet.md) implementation based on a [TreeMap](TreeMap.md). |
| --- | --- |
| [UUID](UUID.md) | A class that represents an immutable universally unique identifier (UUID). |
| [Vector](Vector.md) | The`Vector`class implements a growable array of objects. |
| [WeakHashMap](WeakHashMap.md) | Hash table based implementation of the`Map`interface, with*weak keys*. |
| --- | --- |

## Exceptions

| [ConcurrentModificationException](ConcurrentModificationException.md) | This exception may be thrown by methods that have detected concurrent modification of an object when such modification is not permissible. |
| --- | --- |
| [DuplicateFormatFlagsException](DuplicateFormatFlagsException.md) | Unchecked exception thrown when duplicate flags are provided in the format specifier. |
| [EmptyStackException](EmptyStackException.md) | Thrown by methods in the`Stack`class to indicate that the stack is empty. |
| [FormatFlagsConversionMismatchException](FormatFlagsConversionMismatchException.md) | Unchecked exception thrown when a conversion and flag are incompatible. |
| --- | --- |
| [FormatterClosedException](FormatterClosedException.md) | Unchecked exception thrown when the formatter has been closed. |
| [IllegalFormatCodePointException](IllegalFormatCodePointException.md) | Unchecked exception thrown when a character with an invalid Unicode code point as defined by [Character.isValidCodePoint](../java.lang/Character.md))is passed to the [Formatter](Formatter.md). |
| [IllegalFormatConversionException](IllegalFormatConversionException.md) | Unchecked exception thrown when the argument corresponding to the format specifier is of an incompatible type. |
| --- | --- |
| [IllegalFormatException](IllegalFormatException.md) | Unchecked exception thrown when a format string contains an illegal syntax or a format specifier that is incompatible with the given arguments. |
| [IllegalFormatFlagsException](IllegalFormatFlagsException.md) | Unchecked exception thrown when an illegal combination flags is given. |
| [IllegalFormatPrecisionException](IllegalFormatPrecisionException.md) | Unchecked exception thrown when the precision is a negative value other than`-1`, the conversion does not support a precision, or the value is otherwise unsupported. |
| --- | --- |
| [IllegalFormatWidthException](IllegalFormatWidthException.md) | Unchecked exception thrown when the format width is a negative value other than`-1`or is otherwise unsupported. |
| [IllformedLocaleException](IllformedLocaleException.md) | Thrown by methods in [Locale](Locale.md) and [Locale.Builder](../java/util/Locale.Builder.md) to indicate that an argument is not a well-formed BCP 47 tag. |
| [InputMismatchException](InputMismatchException.md) | Thrown by a`Scanner`to indicate that the token retrieved does not match the pattern for the expected type, or that the token is out of range for the expected type. |
| --- | --- |
| [InvalidPropertiesFormatException](InvalidPropertiesFormatException.md) | Thrown to indicate that an operation could not complete because the input did not conform to the appropriate XML document type for a collection of properties, as per the [Properties](Properties.md) specification. |
| [MissingFormatArgumentException](MissingFormatArgumentException.md) | Unchecked exception thrown when there is a format specifier which does not have a corresponding argument or if an argument index refers to an argument that does not exist. |
| [MissingFormatWidthException](MissingFormatWidthException.md) | Unchecked exception thrown when the format width is required. |
| --- | --- |
| [MissingResourceException](MissingResourceException.md) | Signals that a resource is missing. |
| [NoSuchElementException](NoSuchElementException.md) | Thrown by various accessor methods to indicate that the element being requested does not exist. |
| [ServiceConfigurationError](ServiceConfigurationError.md) | Error thrown when something goes wrong while locating, loading, or instantiating a service provider. |
| --- | --- |
| [TooManyListenersException](TooManyListenersException.md) | The`TooManyListenersException `Exception is used as part of the Java Event model to annotate and implement a unicast special case of a multicast Event Source. |
| [UnknownFormatConversionException](UnknownFormatConversionException.md) | Unchecked exception thrown when an unknown conversion is given. |
| [UnknownFormatFlagsException](UnknownFormatFlagsException.md) | Unchecked exception thrown when an unknown flag is given. |
| --- | --- |

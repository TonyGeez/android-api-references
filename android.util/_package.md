# android.util

# android.util

Kotlin| [Java](https://developer.android.com/reference/android/util/package-summary "View this page in Java")

## Interfaces

| [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet) | A collection of attributes, as found associated with a tag in an XML document. |
| [Dumpable](https://developer.android.com/reference/kotlin/android/util/Dumpable) | Represents an object whose state can be dumped into a [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#). |
| [DumpableContainer](https://developer.android.com/reference/kotlin/android/util/DumpableContainer) | Represents a container that manages [dumpables](https://developer.android.com/reference/kotlin/android/util/Dumpable). |
| [Printer](https://developer.android.com/reference/kotlin/android/util/Printer) | Simple interface for printing text, allowing redirection to various targets. |

## Classes

| [ArrayMap](https://developer.android.com/reference/kotlin/android/util/ArrayMap) | ArrayMap is a generic key-\>value mapping data structure that is designed to be more memory efficient than a traditional [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#). |
| [ArraySet](https://developer.android.com/reference/kotlin/android/util/ArraySet) | ArraySet is a generic set data structure that is designed to be more memory efficient than a traditional [java.util.HashSet](https://developer.android.com/reference/kotlin/java/util/HashSet.html#). |
| [AtomicFile](https://developer.android.com/reference/kotlin/android/util/AtomicFile) | Helper class for performing atomic operations on a file by writing to a new file and renaming it into the place of the original file after the write has successfully completed. |
| [Base64](https://developer.android.com/reference/kotlin/android/util/Base64) | Utilities for encoding and decoding the Base64 representation of binary data. |
| [Base64InputStream](https://developer.android.com/reference/kotlin/android/util/Base64InputStream) | An InputStream that does Base64 decoding on the data read through it. |
| [Base64OutputStream](https://developer.android.com/reference/kotlin/android/util/Base64OutputStream) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. |
| [CloseGuard](https://developer.android.com/reference/kotlin/android/util/CloseGuard) | CloseGuard is a mechanism for flagging implicit finalizer cleanup of resources that should have been cleaned up by explicit close methods (aka "explicit termination methods" in Effective Java). |
| [Config](https://developer.android.com/reference/kotlin/android/util/Config) | <br /> |
| [DebugUtils](https://developer.android.com/reference/kotlin/android/util/DebugUtils) | Various utilities for debugging and logging. |
| [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics) | A structure describing general information about a display, such as its size, density, and font scaling. |
| [EventLog](https://developer.android.com/reference/kotlin/android/util/EventLog) | Access to the system diagnostic event record. |
| [EventLogTags](https://developer.android.com/reference/kotlin/android/util/EventLogTags) | <br /> |
| [FloatMath](https://developer.android.com/reference/kotlin/android/util/FloatMath) | Math routines similar to those found in [java.lang.Math](https://developer.android.com/reference/kotlin/java/lang/Math.html#). |
| [FloatProperty](https://developer.android.com/reference/kotlin/android/util/FloatProperty) | An implementation of [android.util.Property](https://developer.android.com/reference/kotlin/android/util/Property) to be used specifically with fields of type`float`. |
| [Half](https://developer.android.com/reference/kotlin/android/util/Half) | The`Half`class is a wrapper and a utility class to manipulate half-precision 16-bit [IEEE 754](https://en.wikipedia.org/wiki/Half-precision_floating-point_format) floating point data types (also called fp16 or binary16). |
| [IntProperty](https://developer.android.com/reference/kotlin/android/util/IntProperty) | An implementation of [android.util.Property](https://developer.android.com/reference/kotlin/android/util/Property) to be used specifically with fields of type`int`. |
| [JsonReader](https://developer.android.com/reference/kotlin/android/util/JsonReader) | Reads a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value as a stream of tokens. |
| [JsonWriter](https://developer.android.com/reference/kotlin/android/util/JsonWriter) | Writes a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value to a stream, one token at a time. |
| [LayoutDirection](https://developer.android.com/reference/kotlin/android/util/LayoutDirection) | A class for defining layout directions. |
| [Log](https://developer.android.com/reference/kotlin/android/util/Log) | API for sending log output. |
| [LogPrinter](https://developer.android.com/reference/kotlin/android/util/LogPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to the system log. |
| [LongSparseArray](https://developer.android.com/reference/kotlin/android/util/LongSparseArray) | SparseArray mapping longs to Objects. |
| [LruCache](https://developer.android.com/reference/kotlin/android/util/LruCache) | A cache that holds strong references to a limited number of values. |
| [MonthDisplayHelper](https://developer.android.com/reference/kotlin/android/util/MonthDisplayHelper) | Helps answer common questions that come up when displaying a month in a 6 row calendar grid format. |
| [MutableBoolean](https://developer.android.com/reference/kotlin/android/util/MutableBoolean) | <br /> |
| [MutableByte](https://developer.android.com/reference/kotlin/android/util/MutableByte) | <br /> |
| [MutableChar](https://developer.android.com/reference/kotlin/android/util/MutableChar) | <br /> |
| [MutableDouble](https://developer.android.com/reference/kotlin/android/util/MutableDouble) | <br /> |
| [MutableFloat](https://developer.android.com/reference/kotlin/android/util/MutableFloat) | <br /> |
| [MutableInt](https://developer.android.com/reference/kotlin/android/util/MutableInt) | <br /> |
| [MutableLong](https://developer.android.com/reference/kotlin/android/util/MutableLong) | <br /> |
| [MutableShort](https://developer.android.com/reference/kotlin/android/util/MutableShort) | <br /> |
| [Pair](https://developer.android.com/reference/kotlin/android/util/Pair) | Container to ease passing around a tuple of two objects. |
| [Patterns](https://developer.android.com/reference/kotlin/android/util/Patterns) | Commonly used regular expression patterns. |
| [PrintStreamPrinter](https://developer.android.com/reference/kotlin/android/util/PrintStreamPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to a [java.io.PrintStream](https://developer.android.com/reference/kotlin/java/io/PrintStream.html#). |
| [PrintWriterPrinter](https://developer.android.com/reference/kotlin/android/util/PrintWriterPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to a [java.io.PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#). |
| [Property](https://developer.android.com/reference/kotlin/android/util/Property) | A property is an abstraction that can be used to represent a mutable value that is held in a*host* object. The Property's [set(java.lang.Object,java.lang.Object)](https://developer.android.com/reference/kotlin/android/util/Property#set(android.util.Property.T,%20android.util.Property.V))or [get(java.lang.Object)](https://developer.android.com/reference/kotlin/android/util/Property#get(android.util.Property.T))methods can be implemented in terms of the private fields of the host object, or via "setter" and "getter" methods or by some other mechanism, as appropriate. |
| [Range](https://developer.android.com/reference/kotlin/android/util/Range) | Immutable class for describing the range of two numeric values. |
| [Rational](https://developer.android.com/reference/kotlin/android/util/Rational) | An immutable data type representation a rational number. |
| [Size](https://developer.android.com/reference/kotlin/android/util/Size) | Immutable class for describing width and height dimensions in pixels. |
| [SizeF](https://developer.android.com/reference/kotlin/android/util/SizeF) | Immutable class for describing width and height dimensions in some arbitrary unit. |
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray) | `SparseArray`maps integers to Objects and, unlike a normal array of Objects, its indices can contain gaps. |
| [SparseBooleanArray](https://developer.android.com/reference/kotlin/android/util/SparseBooleanArray) | SparseBooleanArrays map integers to booleans. |
| [SparseIntArray](https://developer.android.com/reference/kotlin/android/util/SparseIntArray) | SparseIntArrays map integers to integers. |
| [SparseLongArray](https://developer.android.com/reference/kotlin/android/util/SparseLongArray) | SparseLongArrays map integers to longs. |
| [StateSet](https://developer.android.com/reference/kotlin/android/util/StateSet) | State sets are arrays of positive ints where each element represents the state of a [android.view.View](https://developer.android.com/reference/kotlin/android/view/View.html#)(e.g. focused, selected, visible, etc.). |
| [StatsLog](https://developer.android.com/reference/kotlin/android/util/StatsLog) | StatsLog provides an API for developers to send events to statsd. |
| [StringBuilderPrinter](https://developer.android.com/reference/kotlin/android/util/StringBuilderPrinter) | Implementation of a [android.util.Printer](https://developer.android.com/reference/kotlin/android/util/Printer) that sends its output to a [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#). |
| [TimeUtils](https://developer.android.com/reference/kotlin/android/util/TimeUtils) | A class containing utility methods related to time zones. |
| [TimingLogger](https://developer.android.com/reference/kotlin/android/util/TimingLogger) | A utility class to help log timings splits throughout a method call. |
| [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue) | Container for a dynamically typed data value. |
| [Xml](https://developer.android.com/reference/kotlin/android/util/Xml) | XML utility methods. |

## Exceptions

| [AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException) | Base class for all checked exceptions thrown by the Android frameworks. |
| [AndroidRuntimeException](https://developer.android.com/reference/kotlin/android/util/AndroidRuntimeException) | Base class for all unchecked exceptions thrown by the Android frameworks. |
| [Base64DataException](https://developer.android.com/reference/kotlin/android/util/Base64DataException) | This exception is thrown by [Base64InputStream](https://developer.android.com/reference/kotlin/android/util/Base64InputStream) or [Base64OutputStream](https://developer.android.com/reference/kotlin/android/util/Base64OutputStream) when an error is detected in the data being decoded. |
| [MalformedJsonException](https://developer.android.com/reference/kotlin/android/util/MalformedJsonException) | Thrown when a reader encounters malformed JSON. |
| [NoSuchPropertyException](https://developer.android.com/reference/kotlin/android/util/NoSuchPropertyException) | Thrown when code requests a [Property](https://developer.android.com/reference/kotlin/android/util/Property) on a class that does not expose the appropriate method or field. |
| [TimeFormatException](https://developer.android.com/reference/kotlin/android/util/TimeFormatException) | <br /> |

## Enums

| [JsonToken](https://developer.android.com/reference/kotlin/android/util/JsonToken) | A structure, name or value type in a JSON-encoded string. |

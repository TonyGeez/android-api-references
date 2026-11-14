# android.util

# android.util

Kotlin| [Java](../android/util/_package.md)
| --- | --- |

## Interfaces

| [AttributeSet](../android/util/AttributeSet.md) | A collection of attributes, as found associated with a tag in an XML document. |
| --- | --- |
| [Dumpable](../android/util/Dumpable.md) | Represents an object whose state can be dumped into a [PrintWriter](../java/io/PrintWriter.md). |
| [DumpableContainer](../android/util/DumpableContainer.md) | Represents a container that manages [dumpables](../android/util/Dumpable.md). |
| [Printer](../android/util/Printer.md) | Simple interface for printing text, allowing redirection to various targets. |
| --- | --- |

## Classes

| [ArrayMap](../android/util/ArrayMap.md) | ArrayMap is a generic key-\>value mapping data structure that is designed to be more memory efficient than a traditional [java.util.HashMap](../java/util/HashMap.md). |
| --- | --- |
| [ArraySet](../android/util/ArraySet.md) | ArraySet is a generic set data structure that is designed to be more memory efficient than a traditional [java.util.HashSet](../java/util/HashSet.md). |
| [AtomicFile](../android/util/AtomicFile.md) | Helper class for performing atomic operations on a file by writing to a new file and renaming it into the place of the original file after the write has successfully completed. |
| [Base64](../android/util/Base64.md) | Utilities for encoding and decoding the Base64 representation of binary data. |
| --- | --- |
| [Base64InputStream](../android/util/Base64InputStream.md) | An InputStream that does Base64 decoding on the data read through it. |
| [Base64OutputStream](../android/util/Base64OutputStream.md) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. |
| [CloseGuard](../android/util/CloseGuard.md) | CloseGuard is a mechanism for flagging implicit finalizer cleanup of resources that should have been cleaned up by explicit close methods (aka "explicit termination methods" in Effective Java). |
| --- | --- |
| [Config](../android/util/Config.md) | <br /> |
| [DebugUtils](../android/util/DebugUtils.md) | Various utilities for debugging and logging. |
| [DisplayMetrics](../android/util/DisplayMetrics.md) | A structure describing general information about a display, such as its size, density, and font scaling. |
| --- | --- |
| [EventLog](../android/util/EventLog.md) | Access to the system diagnostic event record. |
| [EventLogTags](../android/util/EventLogTags.md) | <br /> |
| [FloatMath](../android/util/FloatMath.md) | Math routines similar to those found in [java.lang.Math](../java/lang/Math.md). |
| --- | --- |
| [FloatProperty](../android/util/FloatProperty.md) | An implementation of [android.util.Property](../android/util/Property.md) to be used specifically with fields of type`float`. |
| [Half](../android/util/Half.md) | The`Half`class is a wrapper and a utility class to manipulate half-precision 16-bit [IEEE 754](https://en.wikipedia.org/wiki/Half-precision_floating-point_format) floating point data types (also called fp16 or binary16). |
| [IntProperty](../android/util/IntProperty.md) | An implementation of [android.util.Property](../android/util/Property.md) to be used specifically with fields of type`int`. |
| --- | --- |
| [JsonReader](../android/util/JsonReader.md) | Reads a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value as a stream of tokens. |
| [JsonWriter](../android/util/JsonWriter.md) | Writes a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value to a stream, one token at a time. |
| [LayoutDirection](../android/util/LayoutDirection.md) | A class for defining layout directions. |
| --- | --- |
| [Log](../android/util/Log.md) | API for sending log output. |
| [LogPrinter](../android/util/LogPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to the system log. |
| [LongSparseArray](../android/util/LongSparseArray.md) | SparseArray mapping longs to Objects. |
| --- | --- |
| [LruCache](../android/util/LruCache.md) | A cache that holds strong references to a limited number of values. |
| [MonthDisplayHelper](../android/util/MonthDisplayHelper.md) | Helps answer common questions that come up when displaying a month in a 6 row calendar grid format. |
| [MutableBoolean](../android/util/MutableBoolean.md) | <br /> |
| --- | --- |
| [MutableByte](../android/util/MutableByte.md) | <br /> |
| [MutableChar](../android/util/MutableChar.md) | <br /> |
| [MutableDouble](../android/util/MutableDouble.md) | <br /> |
| --- | --- |
| [MutableFloat](../android/util/MutableFloat.md) | <br /> |
| [MutableInt](../android/util/MutableInt.md) | <br /> |
| [MutableLong](../android/util/MutableLong.md) | <br /> |
| --- | --- |
| [MutableShort](../android/util/MutableShort.md) | <br /> |
| [Pair](../android/util/Pair.md) | Container to ease passing around a tuple of two objects. |
| [Patterns](../android/util/Patterns.md) | Commonly used regular expression patterns. |
| --- | --- |
| [PrintStreamPrinter](../android/util/PrintStreamPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [java.io.PrintStream](../java/io/PrintStream.md). |
| [PrintWriterPrinter](../android/util/PrintWriterPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [java.io.PrintWriter](../java/io/PrintWriter.md). |
| [Property](../android/util/Property.md) | A property is an abstraction that can be used to represent a mutable value that is held in a*host* object. The Property's [set(java.lang.Object,java.lang.Object)](../android/util/Property.md))or [get(java.lang.Object)](../android/util/Property.md))methods can be implemented in terms of the private fields of the host object, or via "setter" and "getter" methods or by some other mechanism, as appropriate. |
| --- | --- |
| [Range](../android/util/Range.md) | Immutable class for describing the range of two numeric values. |
| [Rational](../android/util/Rational.md) | An immutable data type representation a rational number. |
| [Size](../android/util/Size.md) | Immutable class for describing width and height dimensions in pixels. |
| --- | --- |
| [SizeF](../android/util/SizeF.md) | Immutable class for describing width and height dimensions in some arbitrary unit. |
| [SparseArray](../android/util/SparseArray.md) | `SparseArray`maps integers to Objects and, unlike a normal array of Objects, its indices can contain gaps. |
| [SparseBooleanArray](../android/util/SparseBooleanArray.md) | SparseBooleanArrays map integers to booleans. |
| --- | --- |
| [SparseIntArray](../android/util/SparseIntArray.md) | SparseIntArrays map integers to integers. |
| [SparseLongArray](../android/util/SparseLongArray.md) | SparseLongArrays map integers to longs. |
| [StateSet](../android/util/StateSet.md) | State sets are arrays of positive ints where each element represents the state of a [android.view.View](../android/view/View.md)(e.g. focused, selected, visible, etc.). |
| --- | --- |
| [StatsLog](../android/util/StatsLog.md) | StatsLog provides an API for developers to send events to statsd. |
| [StringBuilderPrinter](../android/util/StringBuilderPrinter.md) | Implementation of a [android.util.Printer](../android/util/Printer.md) that sends its output to a [StringBuilder](../java/lang/StringBuilder.md). |
| [TimeUtils](../android/util/TimeUtils.md) | A class containing utility methods related to time zones. |
| --- | --- |
| [TimingLogger](../android/util/TimingLogger.md) | A utility class to help log timings splits throughout a method call. |
| [TypedValue](../android/util/TypedValue.md) | Container for a dynamically typed data value. |
| [Xml](../android/util/Xml.md) | XML utility methods. |
| --- | --- |

## Exceptions

| [AndroidException](../android/util/AndroidException.md) | Base class for all checked exceptions thrown by the Android frameworks. |
| --- | --- |
| [AndroidRuntimeException](../android/util/AndroidRuntimeException.md) | Base class for all unchecked exceptions thrown by the Android frameworks. |
| [Base64DataException](../android/util/Base64DataException.md) | This exception is thrown by [Base64InputStream](../android/util/Base64InputStream.md) or [Base64OutputStream](../android/util/Base64OutputStream.md) when an error is detected in the data being decoded. |
| [MalformedJsonException](../android/util/MalformedJsonException.md) | Thrown when a reader encounters malformed JSON. |
| --- | --- |
| [NoSuchPropertyException](../android/util/NoSuchPropertyException.md) | Thrown when code requests a [Property](../android/util/Property.md) on a class that does not expose the appropriate method or field. |
| [TimeFormatException](../android/util/TimeFormatException.md) | <br /> |

## Enums

| [JsonToken](../android/util/JsonToken.md) | A structure, name or value type in a JSON-encoded string. |
| --- | --- |

# android.util

# android.util

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [AttributeSet](AttributeSet.md) | A collection of attributes, as found associated with a tag in an XML document. |
| --- | --- |
| [Dumpable](Dumpable.md) | Represents an object whose state can be dumped into a [PrintWriter](../java.io/PrintWriter.md). |
| [DumpableContainer](DumpableContainer.md) | Represents a container that manages [dumpables](Dumpable.md). |
| [Printer](Printer.md) | Simple interface for printing text, allowing redirection to various targets. |
| --- | --- |

## Classes

| [ArrayMap](ArrayMap.md) | ArrayMap is a generic key-\>value mapping data structure that is designed to be more memory efficient than a traditional [java.util.HashMap](../java.util/HashMap.md). |
| --- | --- |
| [ArraySet](ArraySet.md) | ArraySet is a generic set data structure that is designed to be more memory efficient than a traditional [java.util.HashSet](../java.util/HashSet.md). |
| [AtomicFile](AtomicFile.md) | Helper class for performing atomic operations on a file by writing to a new file and renaming it into the place of the original file after the write has successfully completed. |
| [Base64](Base64.md) | Utilities for encoding and decoding the Base64 representation of binary data. |
| --- | --- |
| [Base64InputStream](Base64InputStream.md) | An InputStream that does Base64 decoding on the data read through it. |
| [Base64OutputStream](Base64OutputStream.md) | An OutputStream that does Base64 encoding on the data written to it, writing the resulting data to another OutputStream. |
| [CloseGuard](CloseGuard.md) | CloseGuard is a mechanism for flagging implicit finalizer cleanup of resources that should have been cleaned up by explicit close methods (aka "explicit termination methods" in Effective Java). |
| --- | --- |
| [Config](Config.md) | <br /> |
| [DebugUtils](DebugUtils.md) | Various utilities for debugging and logging. |
| [DisplayMetrics](DisplayMetrics.md) | A structure describing general information about a display, such as its size, density, and font scaling. |
| --- | --- |
| [EventLog](EventLog.md) | Access to the system diagnostic event record. |
| [EventLogTags](EventLogTags.md) | <br /> |
| [FloatMath](FloatMath.md) | Math routines similar to those found in [java.lang.Math](../java.lang/Math.md). |
| --- | --- |
| [FloatProperty](FloatProperty.md) | An implementation of [android.util.Property](Property.md) to be used specifically with fields of type`float`. |
| [Half](Half.md) | The`Half`class is a wrapper and a utility class to manipulate half-precision 16-bit [IEEE 754](https://en.wikipedia.org/wiki/Half-precision_floating-point_format) floating point data types (also called fp16 or binary16). |
| [IntProperty](IntProperty.md) | An implementation of [android.util.Property](Property.md) to be used specifically with fields of type`int`. |
| --- | --- |
| [JsonReader](JsonReader.md) | Reads a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value as a stream of tokens. |
| [JsonWriter](JsonWriter.md) | Writes a JSON ([RFC 4627](http://www.ietf.org/rfc/rfc4627.txt)) encoded value to a stream, one token at a time. |
| [LayoutDirection](LayoutDirection.md) | A class for defining layout directions. |
| --- | --- |
| [Log](Log.md) | API for sending log output. |
| [LogPrinter](LogPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to the system log. |
| [LongSparseArray](LongSparseArray.md) | SparseArray mapping longs to Objects. |
| --- | --- |
| [LruCache](LruCache.md) | A cache that holds strong references to a limited number of values. |
| [MonthDisplayHelper](MonthDisplayHelper.md) | Helps answer common questions that come up when displaying a month in a 6 row calendar grid format. |
| [MutableBoolean](MutableBoolean.md) | <br /> |
| --- | --- |
| [MutableByte](MutableByte.md) | <br /> |
| [MutableChar](MutableChar.md) | <br /> |
| [MutableDouble](MutableDouble.md) | <br /> |
| --- | --- |
| [MutableFloat](MutableFloat.md) | <br /> |
| [MutableInt](MutableInt.md) | <br /> |
| [MutableLong](MutableLong.md) | <br /> |
| --- | --- |
| [MutableShort](MutableShort.md) | <br /> |
| [Pair](Pair.md) | Container to ease passing around a tuple of two objects. |
| [Patterns](Patterns.md) | Commonly used regular expression patterns. |
| --- | --- |
| [PrintStreamPrinter](PrintStreamPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to a [java.io.PrintStream](../java.io/PrintStream.md). |
| [PrintWriterPrinter](PrintWriterPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to a [java.io.PrintWriter](../java.io/PrintWriter.md). |
| [Property](Property.md) | A property is an abstraction that can be used to represent a mutable value that is held in a*host* object. The Property's [set(java.lang.Object,java.lang.Object)](Property.md))or [get(java.lang.Object)](Property.md))methods can be implemented in terms of the private fields of the host object, or via "setter" and "getter" methods or by some other mechanism, as appropriate. |
| --- | --- |
| [Range](Range.md) | Immutable class for describing the range of two numeric values. |
| [Rational](Rational.md) | An immutable data type representation a rational number. |
| [Size](Size.md) | Immutable class for describing width and height dimensions in pixels. |
| --- | --- |
| [SizeF](SizeF.md) | Immutable class for describing width and height dimensions in some arbitrary unit. |
| [SparseArray](SparseArray.md) | `SparseArray`maps integers to Objects and, unlike a normal array of Objects, its indices can contain gaps. |
| [SparseBooleanArray](SparseBooleanArray.md) | SparseBooleanArrays map integers to booleans. |
| --- | --- |
| [SparseIntArray](SparseIntArray.md) | SparseIntArrays map integers to integers. |
| [SparseLongArray](SparseLongArray.md) | SparseLongArrays map integers to longs. |
| [StateSet](StateSet.md) | State sets are arrays of positive ints where each element represents the state of a [android.view.View](../android.view/View.md)(e.g. focused, selected, visible, etc.). |
| --- | --- |
| [StatsLog](StatsLog.md) | StatsLog provides an API for developers to send events to statsd. |
| [StringBuilderPrinter](StringBuilderPrinter.md) | Implementation of a [android.util.Printer](Printer.md) that sends its output to a [StringBuilder](../java.lang/StringBuilder.md). |
| [TimeUtils](TimeUtils.md) | A class containing utility methods related to time zones. |
| --- | --- |
| [TimingLogger](TimingLogger.md) | A utility class to help log timings splits throughout a method call. |
| [TypedValue](TypedValue.md) | Container for a dynamically typed data value. |
| [Xml](Xml.md) | XML utility methods. |
| --- | --- |

## Exceptions

| [AndroidException](AndroidException.md) | Base class for all checked exceptions thrown by the Android frameworks. |
| --- | --- |
| [AndroidRuntimeException](AndroidRuntimeException.md) | Base class for all unchecked exceptions thrown by the Android frameworks. |
| [Base64DataException](Base64DataException.md) | This exception is thrown by [Base64InputStream](Base64InputStream.md) or [Base64OutputStream](Base64OutputStream.md) when an error is detected in the data being decoded. |
| [MalformedJsonException](MalformedJsonException.md) | Thrown when a reader encounters malformed JSON. |
| --- | --- |
| [NoSuchPropertyException](NoSuchPropertyException.md) | Thrown when code requests a [Property](Property.md) on a class that does not expose the appropriate method or field. |
| [TimeFormatException](TimeFormatException.md) | <br /> |

## Enums

| [JsonToken](JsonToken.md) | A structure, name or value type in a JSON-encoded string. |
| --- | --- |

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StackFrame

```
interface StackFrame
```

| [java.lang.StackWalker.StackFrame](https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#) |

A `StackFrame` object represents a method invocation returned by `https://developer.android.com/reference/kotlin/java/lang/StackWalker`.

The `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getDeclaringClass()` method may be unsupported as determined by the [stack walking options](https://developer.android.com/reference/kotlin/java/lang/StackWalker.Option) of a [stack walker](https://developer.android.com/reference/kotlin/java/lang/StackWalker).

## Summary

| Public methods ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getByteCodeIndex()()` Returns the index to the `insns` array of a `code_item` containing the execution point represented by this stack frame. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getClassName()()` Gets the [binary name](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#binary-name) of the declaring class of the method represented by this stack frame. |
| abstract [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\<\*\>! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getDeclaringClass()()` Gets the declaring `Class` for the method represented by this stack frame. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getDescriptor()()` Returns the *descriptor* of the method represented by this stack frame as defined by The Java Virtual Machine Specification. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getFileName()()` Returns the name of the source file containing the execution point represented by this stack frame. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getLineNumber()()` Returns the line number of the source line containing the execution point represented by this stack frame. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getMethodName()()` Gets the name of the method represented by this stack frame. |
| open [MethodType](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType)! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#getMethodType()()` Returns the `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType` representing the parameter types and the return type for the method represented by this stack frame. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#isNativeMethod()()` Returns `true` if the method containing the execution point represented by this stack frame is a native method. |
| abstract [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement)! | `https://developer.android.com/reference/kotlin/java/lang/StackWalker.StackFrame#toStackTraceElement()()` Gets a `StackTraceElement` for this stack frame. |

## Public methods

### getByteCodeIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getByteCodeIndex(): Int
```

Returns the index to the `insns` array of a `code_item` containing the execution point represented by this stack frame. The code array gives the actual bytes of Dalvik bytecode that implement the method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index to the `insns` array of the `code_item` attribute containing the execution point represented by this stack frame, or a negative number if the method is native. |

### getClassName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getClassName(): String!
```

Gets the [binary name](https://developer.android.com/reference/kotlin/java/lang/ClassLoader#binary-name) of the declaring class of the method represented by this stack frame.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the binary name of the declaring class of the method represented by this stack frame |

### getDeclaringClass

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDeclaringClass(): Class<*>!
```

Gets the declaring `Class` for the method represented by this stack frame.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class<*>!` | the declaring `Class` of the method represented by this stack frame |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this `StackWalker` is not configured with `https://developer.android.com/reference/kotlin/java/lang/StackWalker.Option`. |

### getDescriptor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDescriptor(): String!
```

Returns the *descriptor* of the method represented by this stack frame as defined by The Java Virtual Machine Specification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the descriptor of the method represented by this stack frame |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType#fromMethodDescriptorString(kotlin.String,%20java.lang.ClassLoader)`
- `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType#toMethodDescriptorString()`

### getFileName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFileName(): String!
```

Returns the name of the source file containing the execution point represented by this stack frame. Generally, this corresponds to the `SourceFile` attribute of the relevant `class` file as defined by The Java Virtual Machine Specification. In some systems, the name may refer to some source code unit other than a file, such as an entry in a source repository.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of the file containing the execution point represented by this stack frame, or `null` if this information is unavailable. |

### getLineNumber

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLineNumber(): Int
```

Returns the line number of the source line containing the execution point represented by this stack frame. Generally, this is derived from the `LineNumberTable` attribute of the relevant `class` file as defined by The Java Virtual Machine Specification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the line number of the source line containing the execution point represented by this stack frame, or a negative number if this information is unavailable. |

### getMethodName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMethodName(): String!
```

Gets the name of the method represented by this stack frame.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the name of the method represented by this stack frame |

### getMethodType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMethodType(): MethodType!
```

Returns the `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType` representing the parameter types and the return type for the method represented by this stack frame.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/invoke/MethodType!` | the `MethodType` for this stack frame |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this `StackWalker` is not configured with `https://developer.android.com/reference/kotlin/java/lang/StackWalker.Option`. |

### isNativeMethod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isNativeMethod(): Boolean
```

Returns `true` if the method containing the execution point represented by this stack frame is a native method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the method containing the execution point represented by this stack frame is a native method. |

### toStackTraceElement

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toStackTraceElement(): StackTraceElement!
```

Gets a `StackTraceElement` for this stack frame.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/StackTraceElement!` | `StackTraceElement` for this stack frame. |

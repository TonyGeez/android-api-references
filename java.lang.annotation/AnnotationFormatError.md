Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnnotationFormatError

```
open class AnnotationFormatError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [java.lang.annotation.AnnotationFormatError](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError#) |
| --- | --- | --- | --- |

Thrown when the annotation parser attempts to read an annotation from a class file and determines that the annotation is malformed. This error can be thrown by the [API used to read annotations](https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement.html#).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError#AnnotationFormatError(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs a new `AnnotationFormatError` with the specified detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError#AnnotationFormatError(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new `AnnotationFormatError` with the specified detail message and cause. |
| `https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError#AnnotationFormatError(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new `AnnotationFormatError` with the specified cause and a detail message of `(cause == null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

## Public constructors

### AnnotationFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnnotationFormatError(message: String!)
```

Constructs a new `AnnotationFormatError` with the specified detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |

### AnnotationFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnnotationFormatError(
    message: String!, 
    cause: Throwable!)
```

Constructs a new `AnnotationFormatError` with the specified detail message and cause. Note that the detail message associated with `cause` is *not* automatically incorporated in this error's detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### AnnotationFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnnotationFormatError(cause: Throwable!)
```

Constructs a new `AnnotationFormatError` with the specified cause and a detail message of `(cause == null ? null : cause.toString())` (which typically contains the class and detail message of `cause`).

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrorListener

```
interface ErrorListener
```

| [javax.xml.transform.ErrorListener](https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener#) |

To provide customized error handling, implement this interface and use the `setErrorListener` method to register an instance of the implementation with the `https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer`. The `Transformer` then reports all errors and warnings through this interface.

If an application does *not* register its own custom `ErrorListener`, the default `ErrorListener` is used which reports all warnings and errors to `System.err` and does not throw any `Exception`s. Applications are *strongly* encouraged to register and use `ErrorListener`s that insure proper behavior for warnings and errors.

For transformation errors, a `Transformer` must use this interface instead of throwing an `Exception`: it is up to the application to decide whether to throw an `Exception` for different types of errors and warnings. Note however that the `Transformer` is not required to continue with the transformation after a call to `https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener#fatalError(javax.xml.transform.TransformerException)`.

`Transformer`s may use this mechanism to report XML parsing errors as well as transformation errors.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener#error(javax.xml.transform.TransformerException)(exception: https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException!)` Receive notification of a recoverable error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener#fatalError(javax.xml.transform.TransformerException)(exception: https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException!)` Receive notification of a non-recoverable error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/javax/xml/transform/ErrorListener#warning(javax.xml.transform.TransformerException)(exception: https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException!)` Receive notification of a warning. |
| --- | --- |

## Public methods

### error

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun error(exception: TransformerException!): Unit
```

Receive notification of a recoverable error.

The transformer must continue to try and provide normal transformation after invoking this method. It should still be possible for the application to process the document through to the end if no other errors are encountered.

| Parameters ||
|---|---|
| `exception` | [TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException)!: The error information encapsulated in a transformer exception. |

| Exceptions ||
|---|---|
| `javax.xml.transform.TransformerException` | if the application chooses to discontinue the transformation. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException`

### fatalError

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun fatalError(exception: TransformerException!): Unit
```

Receive notification of a non-recoverable error.

The `Transformer` must continue to try and provide normal transformation after invoking this method. It should still be possible for the application to process the document through to the end if no other errors are encountered, but there is no guarantee that the output will be useable.

| Parameters ||
|---|---|
| `exception` | [TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException)!: The error information encapsulated in a `TransformerException`. |

| Exceptions ||
|---|---|
| `javax.xml.transform.TransformerException` | if the application chooses to discontinue the transformation. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException`

### warning

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun warning(exception: TransformerException!): Unit
```

Receive notification of a warning.

`https://developer.android.com/reference/kotlin/javax/xml/transform/Transformer` can use this method to report conditions that are not errors or fatal errors. The default behavior is to take no action.

After invoking this method, the Transformer must continue with the transformation. It should still be possible for the application to process the document through to the end.

| Parameters ||
|---|---|
| `exception` | [TransformerException](https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException)!: The warning information encapsulated in a transformer exception. |

| Exceptions ||
|---|---|
| `javax.xml.transform.TransformerException` | if the application chooses to discontinue the transformation. |

**See Also**

- `https://developer.android.com/reference/kotlin/javax/xml/transform/TransformerException`

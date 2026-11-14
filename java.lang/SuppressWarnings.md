# SuppressWarnings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuppressWarnings

```
@Target([AnnotationTarget.CLASS, AnnotationTarget.FILE, AnnotationTarget.FIELD, AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.VALUE_PARAMETER, AnnotationTarget.CONSTRUCTOR, AnnotationTarget.LOCAL_VARIABLE]) class SuppressWarnings
```

| [java.lang.SuppressWarnings](../java/lang/SuppressWarnings.md) |

Indicates that the named compiler warnings should be suppressed in the annotated element (and in all program elements contained in the annotated element). Note that the set of warnings suppressed in a given element is a superset of the warnings suppressed in all containing elements. For example, if you annotate a class to suppress one warning and annotate a method to suppress another, both warnings will be suppressed in the method.

As a matter of style, programmers should always use this annotation on the most deeply nested element where it is effective. If you want to suppress a warning in a particular method, you should annotate that method rather than its class.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SuppressWarnings](../java/lang/SuppressWarnings.md))`(`vararg` `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Indicates that the named compiler warnings should be suppressed in the annotated element (and in all program elements contained in the annotated element). |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)\> | [value](../java/lang/SuppressWarnings.md) The set of warnings that are to be suppressed by the compiler in the annotated element. |

## Public constructors

### SuppressWarnings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SuppressWarnings(vararg value: String)
```

Indicates that the named compiler warnings should be suppressed in the annotated element (and in all program elements contained in the annotated element). Note that the set of warnings suppressed in a given element is a superset of the warnings suppressed in all containing elements. For example, if you annotate a class to suppress one warning and annotate a method to suppress another, both warnings will be suppressed in the method.

As a matter of style, programmers should always use this annotation on the most deeply nested element where it is effective. If you want to suppress a warning in a particular method, you should annotate that method rather than its class.

## Properties

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: Array<String>
```

The set of warnings that are to be suppressed by the compiler in the annotated element. Duplicate names are permitted. The second and successive occurrences of a name are ignored. The presence of unrecognized warning names is *not* an error: Compilers must ignore any warning names they do not recognize. They are, however, free to emit a warning if an annotation contains an unrecognized warning name.

The string `"unchecked"` is used to suppress unchecked warnings. Compiler vendors should document the additional warning names they support in conjunction with this annotation type. They are encouraged to cooperate to ensure that the same names work across multiple compilers.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)> | the set of warnings to be suppressed |

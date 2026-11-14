# Deprecated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Deprecated

```
@Target([AnnotationTarget.CONSTRUCTOR, AnnotationTarget.FIELD, AnnotationTarget.LOCAL_VARIABLE, AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.VALUE_PARAMETER, AnnotationTarget.CLASS, AnnotationTarget.FILE]) class Deprecated
```

| [java.lang.Deprecated](../java/lang/Deprecated.md) |

A program element annotated`@Deprecated`is one that programmers are discouraged from using. An element may be deprecated for any of several reasons, for example, its usage is likely to lead to errors; it may be changed incompatibly or removed in a future version; it has been superseded by a newer, usually preferable alternative; or it is obsolete.

Compilers issue warnings when a deprecated program element is used or overridden in non-deprecated code. Use of the`@Deprecated`annotation on a local variable declaration or on a parameter declaration or a package declaration has no effect on the warnings issued by a compiler.

When a module is deprecated, the use of that module in`requires`, but not in`exports`or`opens`clauses causes a warning to be issued. A module being deprecated does*not*cause warnings to be issued for uses of types within the module.

This annotation type has a string-valued element`since`. The value of this element indicates the version in which the annotated program element was first deprecated.

This annotation type has a boolean-valued element`forRemoval`. A value of`true`indicates intent to remove the annotated program element in a future version. A value of`false`indicates that use of the annotated program element is discouraged, but at the time the program element was annotated, there was no specific intent to remove it.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Deprecated](../java/lang/Deprecated.md))`(`forRemoval:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `since:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` A program element annotated`@Deprecated`is one that programmers are discouraged from using. |

| Properties ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [forRemoval](../java/lang/Deprecated.md) Indicates whether the annotated element is subject to removal in a future version. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [since](../java/lang/Deprecated.md) Returns the version in which the annotated element became deprecated. |

## Public constructors

### Deprecated

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Deprecated(
    forRemoval: Boolean, 
    since: String)
```

A program element annotated`@Deprecated`is one that programmers are discouraged from using. An element may be deprecated for any of several reasons, for example, its usage is likely to lead to errors; it may be changed incompatibly or removed in a future version; it has been superseded by a newer, usually preferable alternative; or it is obsolete.

Compilers issue warnings when a deprecated program element is used or overridden in non-deprecated code. Use of the`@Deprecated`annotation on a local variable declaration or on a parameter declaration or a package declaration has no effect on the warnings issued by a compiler.

When a module is deprecated, the use of that module in`requires`, but not in`exports`or`opens`clauses causes a warning to be issued. A module being deprecated does*not*cause warnings to be issued for uses of types within the module.

This annotation type has a string-valued element`since`. The value of this element indicates the version in which the annotated program element was first deprecated.

This annotation type has a boolean-valued element`forRemoval`. A value of`true`indicates intent to remove the annotated program element in a future version. A value of`false`indicates that use of the annotated program element is discouraged, but at the time the program element was annotated, there was no specific intent to remove it.

## Properties

### forRemoval

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val forRemoval: Boolean
```

Indicates whether the annotated element is subject to removal in a future version. The default value is`false`.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the element is subject to removal |

### since

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val since: String
```

Returns the version in which the annotated element became deprecated. The version string is in the same format and namespace as the value of the`@since`javadoc tag. The default value is the empty string.

| Return ||
|----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the version string |

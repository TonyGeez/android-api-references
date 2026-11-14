# Override

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Override

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class Override
```

| [java.lang.Override](../java/lang/Override.md) |

Indicates that a method declaration is intended to override a method declaration in a supertype. If a method is annotated with this annotation type compilers are required to generate an error message unless at least one of the following conditions hold:

- The method does override or implement a method declared in a supertype.
- The method has a signature that is override-equivalent to that of any public method declared in [Object](../java/lang/Object.md).

<br />

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Override](../java/lang/Override.md))`()` Indicates that a method declaration is intended to override a method declaration in a supertype. |

## Public constructors

### Override

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Override()
```

Indicates that a method declaration is intended to override a method declaration in a supertype. If a method is annotated with this annotation type compilers are required to generate an error message unless at least one of the following conditions hold:

- The method does override or implement a method declared in a supertype.
- The method has a signature that is override-equivalent to that of any public method declared in [Object](../java/lang/Object.md).

<br />

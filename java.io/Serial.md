# Serial

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Serial

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.FIELD]) class Serial
```

| [java.io.Serial](Serial.md) |

Indicates that an annotated field or method is part of the [serialization mechanism](Serializable.md) defined by the Java Object Serialization Specification. This annotation type is intended to allow compile-time checking of serialization-related declarations, analogous to the checking enabled by the [java.lang.Override](../java.lang/Override.md) annotation type to validate method overriding. classes are encouraged to use annotations to help a compiler catch mis-declared serialization-related fields and methods, mis-declarations that may otherwise be difficult to detect.

Specifically, annotations of this type should be applied to serialization-related methods and fields in classes declared to be`Serializable`. The five serialization-related methods are:

- `private void writeObject(java.io.ObjectOutputStream stream) throws IOException`
- `private void readObject(java.io.ObjectInputStream stream) throws IOException, ClassNotFoundException`
- `private void readObjectNoData() throws ObjectStreamException`
- *ANY-ACCESS-MODIFIER* `Object writeReplace() throws ObjectStreamException`
- *ANY-ACCESS-MODIFIER* `Object readResolve() throws ObjectStreamException`

The two serialization-related fields are:

<!-- -->

- `private static final ObjectStreamField[] serialPersistentFields`
- `private static final long serialVersionUID`

Compilers are encouraged to validate that a method or field marked with a`@Serial`annotation is one of the defined serialization-related methods or fields declared in a meaningful context and issue a warning if that is not the case.

It is a semantic error to apply this annotation to other fields or methods, including:

- fields or methods in a class that is not`Serializable`
- fields or methods of the proper structural declaration, but in a type where they are ineffectual. For example,`enum`types are defined to have a`serialVersionUID`of`0L`so a`serialVersionUID`field declared in an`enum`type is ignored. The five serialization-related methods identified above are likewise ignored for an`enum`type.
- in a class that is`Externalizable`:
 - method declarations of`writeObject`,`readObject`, and`readObjectNoData`
 - a field declaration for`serialPersistentFields`

 While the`Externalizable`interface extends`Serializable`, the three methods and one field above are*not*used for externalizable classes.

Note that serialization mechanism accesses its designated fields and methods reflectively and those fields and methods may appear otherwise unused in a`Serializable`class.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Serial](Serial.md))`()` Indicates that an annotated field or method is part of the [serialization mechanism](Serializable.md) defined by the Java Object Serialization Specification. |

## Public constructors

### Serial

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Serial()
```

Indicates that an annotated field or method is part of the [serialization mechanism](Serializable.md) defined by the Java Object Serialization Specification. This annotation type is intended to allow compile-time checking of serialization-related declarations, analogous to the checking enabled by the [java.lang.Override](../java.lang/Override.md) annotation type to validate method overriding. classes are encouraged to use annotations to help a compiler catch mis-declared serialization-related fields and methods, mis-declarations that may otherwise be difficult to detect.

Specifically, annotations of this type should be applied to serialization-related methods and fields in classes declared to be`Serializable`. The five serialization-related methods are:

- `private void writeObject(java.io.ObjectOutputStream stream) throws IOException`
- `private void readObject(java.io.ObjectInputStream stream) throws IOException, ClassNotFoundException`
- `private void readObjectNoData() throws ObjectStreamException`
- *ANY-ACCESS-MODIFIER* `Object writeReplace() throws ObjectStreamException`
- *ANY-ACCESS-MODIFIER* `Object readResolve() throws ObjectStreamException`

The two serialization-related fields are:

<!-- -->

- `private static final ObjectStreamField[] serialPersistentFields`
- `private static final long serialVersionUID`

Compilers are encouraged to validate that a method or field marked with a`@Serial`annotation is one of the defined serialization-related methods or fields declared in a meaningful context and issue a warning if that is not the case.

It is a semantic error to apply this annotation to other fields or methods, including:

- fields or methods in a class that is not`Serializable`
- fields or methods of the proper structural declaration, but in a type where they are ineffectual. For example,`enum`types are defined to have a`serialVersionUID`of`0L`so a`serialVersionUID`field declared in an`enum`type is ignored. The five serialization-related methods identified above are likewise ignored for an`enum`type.
- in a class that is`Externalizable`:
 - method declarations of`writeObject`,`readObject`, and`readObjectNoData`
 - a field declaration for`serialPersistentFields`

 While the`Externalizable`interface extends`Serializable`, the three methods and one field above are*not*used for externalizable classes.

Note that serialization mechanism accesses its designated fields and methods reflectively and those fields and methods may appear otherwise unused in a`Serializable`class. 
**See Also**

- [java.io.Serializable](Serializable.md)
- [java.io.Externalizable](Externalizable.md)

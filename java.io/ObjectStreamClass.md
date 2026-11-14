# ObjectStreamClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectStreamClass

```
open class ObjectStreamClass : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.ObjectStreamClass](../java/io/ObjectStreamClass.md) |

Serialization's descriptor for classes. It contains the name and serialVersionUID of the class. The ObjectStreamClass for a specific class loaded in this Java VM can be found/created using the lookup method.

The algorithm to compute the SerialVersionUID is described in [Object Serialization Specification, Section 4.6, Stream Unique Identifiers](https://docs.oracle.com/javase/8/docs/platform/serialization/spec/class.html#4100).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Class](../java/lang/Class.md)\<\*\>! | [forClass](../java/io/ObjectStreamClass.md))`()` Return the class in the local VM that this version is mapped to. |
| open [ObjectStreamField](../java/io/ObjectStreamField.md)! | [getField](../java/io/ObjectStreamClass.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Get the field of this class by name. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ObjectStreamField](../java/io/ObjectStreamField.md)!\>! | [getFields](../java/io/ObjectStreamClass.md))`()` Return an array of the fields of this serializable class. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/io/ObjectStreamClass.md))`()` Returns the name of the class described by this descriptor. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSerialVersionUID](../java/io/ObjectStreamClass.md))`()` Return the serialVersionUID for this class. |
| openstatic [ObjectStreamClass](../java/io/ObjectStreamClass.md)! | [lookup](../java/io/ObjectStreamClass.md))`(`cl:` ` [Class](../java/lang/Class.md)<*>!`)` Find the descriptor for a class that can be serialized. |
| --- | --- |
| openstatic [ObjectStreamClass](../java/io/ObjectStreamClass.md)! | [lookupAny](../java/io/ObjectStreamClass.md))`(`cl:` ` [Class](../java/lang/Class.md)<*>!`)` Returns the descriptor for any class, regardless of whether it implements [Serializable](../java/io/Serializable.md). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/io/ObjectStreamClass.md))`()` Return a string describing this ObjectStreamClass. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ObjectStreamField](../java/io/ObjectStreamField.md)!\>! | [NO_FIELDS](../java/io/ObjectStreamClass.md) serialPersistentFields value indicating no serializable fields |

## Public methods

### forClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forClass(): Class<*>!
```

Return the class in the local VM that this version is mapped to. Null is returned if there is no corresponding local class.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | the`Class`instance that this descriptor represents |

### getField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getField(name: String!): ObjectStreamField!
```

Get the field of this class by name.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the data field to look for |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [ObjectStreamField](../java/io/ObjectStreamField.md)! | The ObjectStreamField object of the named field or null if there is no such named field. |

### getFields

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFields(): Array<ObjectStreamField!>!
```

Return an array of the fields of this serializable class.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ObjectStreamField](../java/io/ObjectStreamField.md)!>! | an array containing an element for each persistent field of this class. Returns an array of length zero if there are no fields. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the name of the class described by this descriptor. This method returns the name of the class in the format that is used by the [Class.getName](../java/lang/Class.md))method.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representing the name of the class |

### getSerialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSerialVersionUID(): Long
```

Return the serialVersionUID for this class. The serialVersionUID defines a set of classes all with the same name that have evolved from a common root class and agree to be serialized and deserialized using a common format. NonSerializable classes have a serialVersionUID of 0L.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the SUID of the class described by this descriptor |

### lookup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lookup(cl: Class<*>!): ObjectStreamClass!
```

Find the descriptor for a class that can be serialized. Creates an ObjectStreamClass instance if one does not exist yet for class. Null is returned if the specified class does not implement java.io.Serializable or java.io.Externalizable.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `cl` | [Class](../java/lang/Class.md)\<\*\>!:class for which to get the descriptor |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ObjectStreamClass](../java/io/ObjectStreamClass.md)! | the class descriptor for the specified class |

### lookupAny

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lookupAny(cl: Class<*>!): ObjectStreamClass!
```

Returns the descriptor for any class, regardless of whether it implements [Serializable](../java/io/Serializable.md).

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------------|
| `cl` | [Class](../java/lang/Class.md)\<\*\>!:class for which to get the descriptor |

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------|
| [ObjectStreamClass](../java/io/ObjectStreamClass.md)! | the class descriptor for the specified class |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a string describing this ObjectStreamClass.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### NO_FIELDS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_FIELDS: Array<ObjectStreamField!>!
```

serialPersistentFields value indicating no serializable fields

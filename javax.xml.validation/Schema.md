# Schema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Schema

```
abstract class Schema
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.Schema](../javax/xml/validation/Schema.md) |

Immutable in-memory representation of grammar.

This object represents a set of constraints that can be checked/ enforced against an XML document.

A [Schema](../javax/xml/validation/Schema.md) object is thread safe and applications are encouraged to share it across many parsers in many threads.

A [Schema](../javax/xml/validation/Schema.md) object is immutable in the sense that it shouldn't change the set of constraints once it is created. In other words, if an application validates the same document twice against the same [Schema](../javax/xml/validation/Schema.md), it must always produce the same result.

A [Schema](../javax/xml/validation/Schema.md) object is usually created from [SchemaFactory](../javax/xml/validation/SchemaFactory.md).

Two kinds of validators can be created from a [Schema](../javax/xml/validation/Schema.md) object. One is [Validator](../javax/xml/validation/Validator.md), which provides highly-level validation operations that cover typical use cases. The other is [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md), which works on top of SAX for better modularity.

This specification does not refine the [java.lang.Object#equals(java.lang.Object)](../java/lang/Object.md))method. In other words, if you parse the same schema twice, you may still get`!schemaA.equals(schemaB)`.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------|---|
| [Schema](../javax/xml/validation/Schema.md))`()` Constructor for the derived class. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Validator](../javax/xml/validation/Validator.md)! | [newValidator](../javax/xml/validation/Schema.md))`()` Creates a new [Validator](../javax/xml/validation/Validator.md) for this [Schema](../javax/xml/validation/Schema.md). |
| abstract [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md)! | [newValidatorHandler](../javax/xml/validation/Schema.md))`()` Creates a new [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md) for this [Schema](../javax/xml/validation/Schema.md). |

## Protected constructors

### Schema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Schema()
```

Constructor for the derived class.

The constructor does nothing.

## Public methods

### newValidator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newValidator(): Validator!
```

Creates a new [Validator](../javax/xml/validation/Validator.md) for this [Schema](../javax/xml/validation/Schema.md).

A validator enforces/checks the set of constraints this object represents.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------|
| [Validator](../javax/xml/validation/Validator.md)! | Always return a non-null valid object. |

### newValidatorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newValidatorHandler(): ValidatorHandler!
```

Creates a new [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md) for this [Schema](../javax/xml/validation/Schema.md).

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------|
| [ValidatorHandler](../javax/xml/validation/ValidatorHandler.md)! | Always return a non-null valid object. |

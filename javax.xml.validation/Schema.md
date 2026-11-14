# Schema

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Schema

```
abstract class Schema
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#) |

Immutable in-memory representation of grammar.

This object represents a set of constraints that can be checked/ enforced against an XML document.

A [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#) object is thread safe and applications are encouraged to share it across many parsers in many threads.

A [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#) object is immutable in the sense that it shouldn't change the set of constraints once it is created. In other words, if an application validates the same document twice against the same [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#), it must always produce the same result.

A [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#) object is usually created from [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory).

Two kinds of validators can be created from a [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#) object. One is [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator), which provides highly-level validation operations that cover typical use cases. The other is [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler), which works on top of SAX for better modularity.

This specification does not refine the [java.lang.Object#equals(java.lang.Object)](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method. In other words, if you parse the same schema twice, you may still get`!schemaA.equals(schemaB)`.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------|---|
| [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#Schema())`()` Constructor for the derived class. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator)! | [newValidator](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#newValidator())`()` Creates a new [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator) for this [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#). |
| abstract [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler)! | [newValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#newValidatorHandler())`()` Creates a new [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler) for this [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#). |

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

Creates a new [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator) for this [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#).

A validator enforces/checks the set of constraints this object represents.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------|
| [Validator](https://developer.android.com/reference/kotlin/javax/xml/validation/Validator)! | Always return a non-null valid object. |

### newValidatorHandler

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newValidatorHandler(): ValidatorHandler!
```

Creates a new [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler) for this [Schema](https://developer.android.com/reference/kotlin/javax/xml/validation/Schema#).

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------|
| [ValidatorHandler](https://developer.android.com/reference/kotlin/javax/xml/validation/ValidatorHandler)! | Always return a non-null valid object. |

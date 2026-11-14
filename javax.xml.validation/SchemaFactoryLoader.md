# SchemaFactoryLoader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SchemaFactoryLoader

```
abstract class SchemaFactoryLoader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.xml.validation.SchemaFactoryLoader](../javax/xml/validation/SchemaFactoryLoader.md) |

This class was removed from JAXP 1.3 before it was finalized but was mistakenly included in Java 5. It only exists now for compatibility reasons. Applications should avoid using it.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SchemaFactoryLoader](../javax/xml/validation/SchemaFactoryLoader.md))`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SchemaFactory](../javax/xml/validation/SchemaFactory.md)! | [newFactory](../javax/xml/validation/SchemaFactoryLoader.md))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Protected constructors

### SchemaFactoryLoader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SchemaFactoryLoader()
```

## Public methods

### newFactory

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newFactory(schemaLanguage: String!): SchemaFactory!
```

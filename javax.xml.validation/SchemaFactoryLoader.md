# SchemaFactoryLoader

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SchemaFactoryLoader

```
abstract class SchemaFactoryLoader
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.xml.validation.SchemaFactoryLoader](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactoryLoader#) |

This class was removed from JAXP 1.3 before it was finalized but was mistakenly included in Java 5. It only exists now for compatibility reasons. Applications should avoid using it.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SchemaFactoryLoader](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactoryLoader#SchemaFactoryLoader())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [SchemaFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactory)! | [newFactory](https://developer.android.com/reference/kotlin/javax/xml/validation/SchemaFactoryLoader#newFactory(kotlin.String))`(`schemaLanguage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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

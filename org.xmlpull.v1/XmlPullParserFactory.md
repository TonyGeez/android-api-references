# XmlPullParserFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XmlPullParserFactory

```
open class XmlPullParserFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [org.xmlpull.v1.XmlPullParserFactory](XmlPullParserFactory.md) |

This class is used to create implementations of XML Pull Parser defined in XMPULL V1 API.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_NAME](XmlPullParserFactory.md) <br /> |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XmlPullParserFactory](XmlPullParserFactory.md))`()` Protected constructor to be called by factory implementations. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](XmlPullParserFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the current value of the feature with given name. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNamespaceAware](XmlPullParserFactory.md))`()` Indicates whether or not the factory is configured to produce parsers which are namespace aware (it simply set feature XmlPullParser.FEATURE_PROCESS_NAMESPACES to true or false). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidating](XmlPullParserFactory.md))`()` Indicates whether or not the factory is configured to produce parsers which validate the XML content during parse. |
| --- | --- |
| openstatic [XmlPullParserFactory](XmlPullParserFactory.md)! | [newInstance](XmlPullParserFactory.md))`()` Creates a new instance of a PullParserFactory that can be used to create XML pull parsers. |
| openstatic [XmlPullParserFactory](XmlPullParserFactory.md)! | [newInstance](XmlPullParserFactory.md))`(`unused:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `unused2:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a factory that always returns instances of Android's built-in [XmlPullParser](XmlPullParser.md) and [XmlSerializer](XmlSerializer.md) implementation. |
| open [XmlPullParser](XmlPullParser.md)! | [newPullParser](XmlPullParserFactory.md))`()` Creates a new instance of a XML Pull Parser using the currently configured factory features. |
| --- | --- |
| open [XmlSerializer](XmlSerializer.md)! | [newSerializer](XmlPullParserFactory.md))`()` Creates a new instance of a XML Serializer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](XmlPullParserFactory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `state:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the features to be set when XML Pull Parser is created by this factory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNamespaceAware](XmlPullParserFactory.md))`(`awareness:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specifies that the parser produced by this factory will provide support for XML namespaces. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValidating](XmlPullParserFactory.md))`(`validating:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specifies that the parser produced by this factory will be validating (it simply set feature XmlPullParser.FEATURE_VALIDATION to true or false). |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [classNamesLocation](XmlPullParserFactory.md) Unused, but we have to keep it because it's public API. |
| [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | [features](XmlPullParserFactory.md) <br /> |
| [ArrayList](../java.util/ArrayList.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parserClasses](XmlPullParserFactory.md) <br /> |
| --- | --- |
| [ArrayList](../java.util/ArrayList.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [serializerClasses](XmlPullParserFactory.md) <br /> |

## Constants

### PROPERTY_NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_NAME: String
```  

 Value: "org.xmlpull.v1.XmlPullParserFactory"

## Protected constructors

### XmlPullParserFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected XmlPullParserFactory()
```

Protected constructor to be called by factory implementations.

## Public methods

### getFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFeature(name: String!): Boolean
```

Return the current value of the feature with given name.

**NOTE:**factory features are not used for XML Serializer.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of feature to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The value of named feature. Unknown features are always returned as false |

### isNamespaceAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isNamespaceAware(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which are namespace aware (it simply set feature XmlPullParser.FEATURE_PROCESS_NAMESPACES to true or false).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the factory is configured to produce parsers which are namespace aware; false otherwise. |

### isValidating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isValidating(): Boolean
```

Indicates whether or not the factory is configured to produce parsers which validate the XML content during parse.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the factory is configured to produce parsers which validate the XML content during parse; false otherwise. |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): XmlPullParserFactory!
```

Creates a new instance of a PullParserFactory that can be used to create XML pull parsers. The factory will always return instances of Android's built-in [XmlPullParser](XmlPullParser.md) and [XmlSerializer](XmlSerializer.md). 

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    unused: String!, 
    unused2: Class<Any!>!
): XmlPullParserFactory!
```

Creates a factory that always returns instances of Android's built-in [XmlPullParser](XmlPullParser.md) and [XmlSerializer](XmlSerializer.md) implementation. This**does not**support factories capable of creating arbitrary parser and serializer implementations. Both arguments to this method are unused. 

### newPullParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newPullParser(): XmlPullParser!
```

Creates a new instance of a XML Pull Parser using the currently configured factory features.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| [XmlPullParser](XmlPullParser.md)! | A new instance of a XML Pull Parser. |

### newSerializer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newSerializer(): XmlSerializer!
```

Creates a new instance of a XML Serializer.

**NOTE:**factory features are not used for XML Serializer.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| [XmlSerializer](XmlSerializer.md)! | A new instance of a XML Serializer. |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------|
| `org.xmlpull.v1.XmlPullParserException` | if a parser cannot be created which satisfies the requested configuration. |

### setFeature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFeature(
    name: String!, 
    state: Boolean
): Unit
```

Set the features to be set when XML Pull Parser is created by this factory.

**NOTE:**factory features are not used for XML Serializer.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string with URI identifying feature |
| `state` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true feature will be set; if false will be ignored |

### setNamespaceAware

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNamespaceAware(awareness: Boolean): Unit
```

Specifies that the parser produced by this factory will provide support for XML namespaces. By default the value of this is set to false.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `awareness` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the parser produced by this code will provide support for XML namespaces; false otherwise. |

### setValidating

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValidating(validating: Boolean): Unit
```

Specifies that the parser produced by this factory will be validating (it simply set feature XmlPullParser.FEATURE_VALIDATION to true or false). By default the value of this is set to false.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `validating` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):- if true the parsers created by this factory must be validating. |

## Properties

### classNamesLocation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var classNamesLocation: String!
```

Unused, but we have to keep it because it's public API. 

### features

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var features: HashMap<String!, Boolean!>!
```  

### parserClasses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var parserClasses: ArrayList<Any!>!
```  

### serializerClasses

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var serializerClasses: ArrayList<Any!>!
```

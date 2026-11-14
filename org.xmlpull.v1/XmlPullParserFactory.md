# XmlPullParserFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# XmlPullParserFactory

```
open class XmlPullParserFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [org.xmlpull.v1.XmlPullParserFactory](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#) |

This class is used to create implementations of XML Pull Parser defined in XMPULL V1 API.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_NAME](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#PROPERTY_NAME:kotlin.String) <br /> |

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [XmlPullParserFactory](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#XmlPullParserFactory())`()` Protected constructor to be called by factory implementations. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#getFeature(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Return the current value of the feature with given name. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNamespaceAware](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#isNamespaceAware())`()` Indicates whether or not the factory is configured to produce parsers which are namespace aware (it simply set feature XmlPullParser.FEATURE_PROCESS_NAMESPACES to true or false). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidating](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#isValidating())`()` Indicates whether or not the factory is configured to produce parsers which validate the XML content during parse. |
| openstatic [XmlPullParserFactory](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#newInstance())`()` Creates a new instance of a PullParserFactory that can be used to create XML pull parsers. |
| openstatic [XmlPullParserFactory](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#)! | [newInstance](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#newInstance(kotlin.String,%20java.lang.Class))`(`unused:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `unused2:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Creates a factory that always returns instances of Android's built-in [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser) and [XmlSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlSerializer) implementation. |
| open [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser)! | [newPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#newPullParser())`()` Creates a new instance of a XML Pull Parser using the currently configured factory features. |
| open [XmlSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlSerializer)! | [newSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#newSerializer())`()` Creates a new instance of a XML Serializer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFeature](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#setFeature(kotlin.String,%20kotlin.Boolean))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `state:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the features to be set when XML Pull Parser is created by this factory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNamespaceAware](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#setNamespaceAware(kotlin.Boolean))`(`awareness:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specifies that the parser produced by this factory will provide support for XML namespaces. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValidating](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#setValidating(kotlin.Boolean))`(`validating:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Specifies that the parser produced by this factory will be validating (it simply set feature XmlPullParser.FEATURE_VALIDATION to true or false). |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [classNamesLocation](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#classNamesLocation:kotlin.String) Unused, but we have to keep it because it's public API. |
| [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!\>! | [features](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#features:java.util.HashMap) <br /> |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [parserClasses](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#parserClasses:java.util.ArrayList) <br /> |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [serializerClasses](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParserFactory#serializerClasses:java.util.ArrayList) <br /> |

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

Creates a new instance of a PullParserFactory that can be used to create XML pull parsers. The factory will always return instances of Android's built-in [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser) and [XmlSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlSerializer). 

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    unused: String!, 
    unused2: Class<Any!>!
): XmlPullParserFactory!
```

Creates a factory that always returns instances of Android's built-in [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser) and [XmlSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlSerializer) implementation. This**does not**support factories capable of creating arbitrary parser and serializer implementations. Both arguments to this method are unused. 

### newPullParser

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newPullParser(): XmlPullParser!
```

Creates a new instance of a XML Pull Parser using the currently configured factory features.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| [XmlPullParser](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlPullParser)! | A new instance of a XML Pull Parser. |

### newSerializer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newSerializer(): XmlSerializer!
```

Creates a new instance of a XML Serializer.

**NOTE:**factory features are not used for XML Serializer.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| [XmlSerializer](https://developer.android.com/reference/kotlin/org/xmlpull/v1/XmlSerializer)! | A new instance of a XML Serializer. |

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

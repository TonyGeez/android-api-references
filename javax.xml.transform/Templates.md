# Templates

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Templates

```
interface Templates
```

| [javax.xml.transform.Templates](Templates.md) |

An object that implements this interface is the runtime representation of processed transformation instructions.

Templates must be thread-safe for a given instance over multiple threads running concurrently, and may be used multiple times in a given session.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Properties](../java.util/Properties.md)! | [getOutputProperties](Templates.md))`()` Get the properties corresponding to the effective xsl:output element. |
| abstract [Transformer](Transformer.md)! | [newTransformer](Templates.md))`()` Create a new transformation context for this Templates object. |

## Public methods

### getOutputProperties

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOutputProperties(): Properties!
```

Get the properties corresponding to the effective xsl:output element. The object returned will be a clone of the internal values. Accordingly, it can be mutated without mutating the Templates object, and then handed in to [javax.xml.transform.Transformer#setOutputProperties](Transformer.md)).

The properties returned should contain properties set by the stylesheet, and these properties are "defaulted" by default properties specified by [section 16 of the XSL Transformations (XSLT) W3C Recommendation](http://www.w3.org/TR/xslt#output). The properties that were specifically set by the stylesheet should be in the base Properties list, while the XSLT default properties that were not specifically set should be in the "default" Properties list. Thus, getOutputProperties().getProperty(String key) will obtain any property in that was set by the stylesheet,*or*the default properties, while getOutputProperties().get(String key) will only retrieve properties that were explicitly set in the stylesheet.

For XSLT, [Attribute Value Templates](http://www.w3.org/TR/xslt#attribute-value-templates) attribute values will be returned unexpanded (since there is no context at this point). The namespace prefixes inside Attribute Value Templates will be unexpanded, so that they remain valid XPath values.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [Properties](../java.util/Properties.md)! | A Properties object, never null. |

### newTransformer

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newTransformer(): Transformer!
```

Create a new transformation context for this Templates object.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------|
| [Transformer](Transformer.md)! | A valid non-null instance of a Transformer. |

| Exceptions ||
|---------------------------------------------------------|--------------------------------------|
| `javax.xml.transform.TransformerConfigurationException` | if a Transformer can not be created. |

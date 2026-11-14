# DOMLocator

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DOMLocator

```
interface DOMLocator : SourceLocator
```

| [javax.xml.transform.dom.DOMLocator](DOMLocator.md) |

Indicates the position of a node in a source DOM, intended primarily for error reporting. To use a DOMLocator, the receiver of an error must downcast the [javax.xml.transform.SourceLocator](../javax.xml.transform/SourceLocator.md) object returned by an exception. A [javax.xml.transform.Transformer](../javax.xml.transform/Transformer.md) may use this object for purposes other than error reporting, for instance, to indicate the source node that originated a result node.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | [getOriginatingNode](DOMLocator.md))`()` Return the node where the event occurred. |

| Inherited functions ||
|---|---|
| From class [SourceLocator](../javax.xml.transform/SourceLocator.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColumnNumber](../javax.xml.transform/SourceLocator.md))`()` <br /> Return the character position where the current document event ends. **Warning:**The return value from the method is intended only as an approximation for the sake of error reporting; it is not intended to provide sufficient information to edit the character content of the original XML document. The return value is an approximation of the column number in the document entity or external parsed entity where the markup that triggered the event appears. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLineNumber](../javax.xml.transform/SourceLocator.md))`()` <br /> Return the line number where the current document event ends. **Warning:**The return value from the method is intended only as an approximation for the sake of error reporting; it is not intended to provide sufficient information to edit the character content of the original XML document. The return value is an approximation of the line number in the document entity or external parsed entity where the markup that triggered the event appears. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPublicId](../javax.xml.transform/SourceLocator.md))`()` <br /> Return the public identifier for the current document event. The return value is the public identifier of the document entity or of the external parsed entity in which the markup that triggered the event appears. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSystemId](../javax.xml.transform/SourceLocator.md))`()` <br /> Return the system identifier for the current document event. The return value is the system identifier of the document entity or of the external parsed entity in which the markup that triggered the event appears. If the system identifier is a URL, the parser must resolve it fully before passing it to the application. <br /> | ||

## Public methods

### getOriginatingNode

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOriginatingNode(): Node!
```

Return the node where the event occurred.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Node](https://kotlinlang.org/api/latest/jvm/stdlib/org.w3c.dom/-node/index.html)! | The node that is the location for the event. |

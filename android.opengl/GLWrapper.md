# GLSurfaceView.GLWrapper

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GLWrapper

Kotlin| [Java](../android/opengl/GLSurfaceView.GLWrapper.md) 
| --- | --- |

```
interface GLWrapper
```

| [android.opengl.GLSurfaceView.GLWrapper](../android/opengl/GLSurfaceView.GLWrapper.md) |

An interface used to wrap a GL interface.

Typically used for implementing debugging and tracing on top of the default GL interface. You would typically use this by creating your own class that implemented all the GL methods by delegating to another GL instance. Then you could add your own behavior before or after calling the delegate. All the GLWrapper would do was instantiate and return the wrapper GL instance: 

```kotlin
class MyGLWrapper implements GLWrapper {
      GL wrap(GL gl) {
          return new MyGLImplementation(gl);
      }
      static class MyGLImplementation implements GL,GL10,GL11,... {
          ...
      }
  }
  
```

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [GL](../javax/microedition/khronos/opengles/GL.md)! | [wrap](../android/opengl/GLSurfaceView.GLWrapper.md))`(`gl:` ` [GL](../javax/microedition/khronos/opengles/GL.md)!`)` Wraps a gl interface in another gl interface. |

## Public methods

### wrap

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun wrap(gl: GL!): GL!
```

Wraps a gl interface in another gl interface.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------|
| `gl` | [GL](../javax/microedition/khronos/opengles/GL.md)!:a GL interface that is to be wrapped. |

| Return ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [GL](../javax/microedition/khronos/opengles/GL.md)! | either the input argument or another GL object that wraps the input argument. |

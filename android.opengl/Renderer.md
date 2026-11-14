# GLSurfaceView.Renderer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Renderer

Kotlin| [Java](../android/opengl/GLSurfaceView.Renderer.md) 
| --- | --- |

```
interface Renderer
```

| [android.opengl.GLSurfaceView.Renderer](../android/opengl/GLSurfaceView.Renderer.md) |

A generic renderer interface.

The renderer is responsible for making OpenGL calls to render a frame.

GLSurfaceView clients typically create their own classes that implement this interface, and then call [GLSurfaceView.setRenderer](../android/opengl/GLSurfaceView.md))to register the renderer with the GLSurfaceView.

<br />

| ### Developer Guides
|
| For more information about how to use OpenGL, read the [OpenGL](https://developer.android.com/guide/topics/graphics/opengl.html) developer guide.

### Threading

The renderer will be called on a separate thread, so that rendering performance is decoupled from the UI thread. Clients typically need to communicate with the renderer from the UI thread, because that's where input events are received. Clients can communicate using any of the standard Java techniques for cross-thread communication, or they can use the [GLSurfaceView.queueEvent(Runnable)](../android/opengl/GLSurfaceView.md))convenience method.

<br />

### EGL Context Lost

There are situations where the EGL rendering context will be lost. This typically happens when device wakes up after going to sleep. When the EGL context is lost, all OpenGL resources (such as textures) that are associated with that context will be automatically deleted. In order to keep rendering correctly, a renderer must recreate any lost resources that it still needs. The [onSurfaceCreated(javax.microedition.khronos.opengles.GL10,javax.microedition.khronos.egl.EGLConfig)](../android/opengl/GLSurfaceView.Renderer.md))method is a convenient place to do this.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrawFrame](../android/opengl/GLSurfaceView.Renderer.md))`(`gl:` ` [GL10](../javax/microedition/khronos/opengles/GL10.md)!`)` Called to draw the current frame. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceChanged](../android/opengl/GLSurfaceView.Renderer.md))`(`gl:` ` [GL10](../javax/microedition/khronos/opengles/GL10.md)!`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the surface changed size. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSurfaceCreated](../android/opengl/GLSurfaceView.Renderer.md))`(`gl:` ` [GL10](../javax/microedition/khronos/opengles/GL10.md)!`, `config:` ` [EGLConfig](../javax/microedition/khronos/egl/EGLConfig.md)!`)` Called when the surface is created or recreated. |
| --- | --- |

## Public methods

### onDrawFrame

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrawFrame(gl: GL10!): Unit
```

Called to draw the current frame.

This method is responsible for drawing the current frame.

The implementation of this method typically looks like this: 

```kotlin
void onDrawFrame(GL10 gl) {
      gl.glClear(GL10.GL_COLOR_BUFFER_BIT | GL10.GL_DEPTH_BUFFER_BIT);
      //... other gl calls to render the scene ...
  }
  
```

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gl` | [GL10](../javax/microedition/khronos/opengles/GL10.md)!:the GL interface. Use`instanceof`to test if the interface supports GL11 or higher interfaces. |

### onSurfaceChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceChanged(
    gl: GL10!, 
    width: Int, 
    height: Int
): Unit
```

Called when the surface changed size.

Called after the surface is created and whenever the OpenGL ES surface size changes.

Typically you will set your viewport here. If your camera is fixed then you could also set your projection matrix here: 

```kotlin
void onSurfaceChanged(GL10 gl, int width, int height) {
      gl.glViewport(0, 0, width, height);
      // for a fixed camera, set the projection too
      float ratio = (float) width / height;
      gl.glMatrixMode(GL10.GL_PROJECTION);
      gl.glLoadIdentity();
      gl.glFrustumf(-ratio, ratio, -1, 1, 1, 10);
  }
  
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gl` | [GL10](../javax/microedition/khronos/opengles/GL10.md)!:the GL interface. Use`instanceof`to test if the interface supports GL11 or higher interfaces. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| --- | --- |

### onSurfaceCreated

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSurfaceCreated(
    gl: GL10!, 
    config: EGLConfig!
): Unit
```

Called when the surface is created or recreated.

Called when the rendering thread starts and whenever the EGL context is lost. The EGL context will typically be lost when the Android device awakes after going to sleep.

Since this method is called at the beginning of rendering, as well as every time the EGL context is lost, this method is a convenient place to put code to create resources that need to be created when the rendering starts, and that need to be recreated when the EGL context is lost. Textures are an example of a resource that you might want to create here.

Note that when the EGL context is lost, all OpenGL resources associated with that context will be automatically deleted. You do not need to call the corresponding "glDelete" methods such as glDeleteTextures to manually delete these lost resources.

<br />

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `gl` | [GL10](../javax/microedition/khronos/opengles/GL10.md)!:the GL interface. Use`instanceof`to test if the interface supports GL11 or higher interfaces. |
| `config` | [EGLConfig](../javax/microedition/khronos/egl/EGLConfig.md)!:the EGLConfig of the created surface. Can be used to create matching pbuffers. |

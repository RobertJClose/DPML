# Matrix4x4d

Unity equivalent documentation: [https://docs.unity3d.com/ScriptReference/Matrix4x4.html](https://docs.unity3d.com/ScriptReference/Matrix4x4.html)

## Unimplemented Methods

None.

## Known Differences Between Implemented Methods

* [`TRS()`](https://docs.unity3d.com/ScriptReference/Matrix4x4.TRS.html) and [`SetTRS()`](https://docs.unity3d.com/ScriptReference/Matrix4x4.SetTRS.html) - When given a non-unit quaternion as input, the Unity implementations of these methods log an error, before some matrix is constructed. My implementation in this case does not log an error, but normalises the input quaternion before constructing a valid TRS matrix. In the standard case when the input quaternion has unit magnitude, the methods behave identically.
* [`rotation`](https://docs.unity3d.com/ScriptReference/Matrix4x4-rotation.html) - There is a special case for matrices which sometimes results in different output between this library and the Unity `rotation` property. When a matrix contains a net reflection in its `scale` vector, the axis of reflection is ambiguous. A reflection along any one axis is equivalent to a reflection along a different axis, combined with a rotation. If you change which axis you consider the reflection to have occurred along, then you can get the same transformation by changing the rotation. My `rotation` property always considers a net reflection to have occurred along the x-axis. The Unity `rotation` property appears to change which axis it considers the reflection along. The combined `scale` and `rotation` properties taken together as a transformation should still be consistent with the Unity implementation.
* [`Equals()` and `== (Operator)`](https://docs.unity3d.com/ScriptReference/Matrix4x4.html) - There is no Unity documentation on these operations, but they do exist for the built in `Matrix4x4`. I believe that the `==` operator uses the `Mathf.Approximately()` method in order to test for approximate equality, while the `Equals()` method tests for exact equality. This is the behaviour implemented in this library.
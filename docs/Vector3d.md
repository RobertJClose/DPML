# Vector3d

Unity equivalent documentation: [https://docs.unity3d.com/ScriptReference/Vector3.html](https://docs.unity3d.com/ScriptReference/Vector3.html)

## Unimplemented Methods

* [`RotateTowards()`](https://docs.unity3d.com/ScriptReference/Vector3.RotateTowards.html)
* [`SmoothDamp()`](https://docs.unity3d.com/ScriptReference/Vector3.SmoothDamp.html)

## Known Differences Between Implemented Methods

* [`Slerp()`](https://docs.unity3d.com/ScriptReference/Vector3.Slerp.html) and [`SlerpUnclamped()`](https://docs.unity3d.com/ScriptReference/Vector3.SlerpUnclamped.html) - When slerping between directions separated by 180 degrees, there is no unique path to slerp along. This library will produce a valid `Slerp()`, but in general it will not exactly match the `Slerp()` produced by the built-in Unity methods.
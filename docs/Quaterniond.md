# Quaternion

Unity equivalent documentation: [https://docs.unity3d.com/ScriptReference/Quaternion.html](https://docs.unity3d.com/ScriptReference/Quaternion.html)

## Unimplemented Methods

* [`RotateTowards()`](https://docs.unity3d.com/ScriptReference/Quaternion.RotateTowards.html)

## Known Differences Between Implemented Methods

* [`Slerp()`](https://docs.unity3d.com/ScriptReference/Quaternion.Slerp.html) and [`SlerpUnclamped()`](https://docs.unity3d.com/ScriptReference/Quaternion.SlerpUnclamped.html) - When slerping between directions separated by 180 degrees, there is no unique path to slerp along. This library will produce a valid `Slerp()`, but in general it will not exactly match the `Slerp()` produced by the Unity methods.
# Introduction

The Double Precision Maths Library is a free code library for users of the Unity game engine. 

The library contains classes such as `Vector3d` and `Quaterniond`, which should be instantly familiar to users of Unity. While the Unity maths and physics classes are backed by single precision floating-point data types, the classes of this library are backed by double precision floats. 

The higher precision types allow for more accurate physical simulations, as floating-point rounding errors are minimised. This may be helpful when performing simulations of orbital mechanics for example, where centimetre precision may still be required across astronomical distances.

# Installation

The library may be found for free on the Unity Asset Store [here](https://assetstore.unity.com/packages/tools/physics/double-precision-maths-library-282105). Once you have added the asset to your account, you can install it into your projects via the Unity Package Manager.

# Style Of This Documentation

Every class in this library has an equivalent class in the built-in Unity scripting API. These classes have been designed to be as similar to their Unity equivalents as possible. For that reason, the standard Unity documentation can largely serve as documentation for this library. 

However, there are a handful of places where the behaviour of this library differs slightly from the Unity implementation. There are also some methods from the Unity classes which are not implemented by this library. This documentation seeks only to record all the differences and missing methods.

# Contents Of This Library

The classes included in this library are the following:

* `Mathd`
* `Matrix4x4d`
* `Quaterniond`
* `Vector2d`
* `Vector3d` 
* `Vector4d`

As mentioned above, some of equivalent Unity methods are not implemented by this library. This was done for one of two reasons:

1. A double precision version of the method seemed unlikely to offer much practical benefit.
2. The behaviour of the Unity method could not be reproduced with sufficient accuracy.

If there a method missing from this library that you feel should be implemented, please feel free to [get in touch](mailto:robertclose@pm.me?subject=DPML) and I will look into it.

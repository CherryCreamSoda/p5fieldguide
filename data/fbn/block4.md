---
description: FBN Block 4
---

# Adjusting Spawn Points

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Viewable in 010 Editor using the .FBN Binary Template</p></figcaption></figure>

This is an **FBN** with 3 Entrances. Each Entry in Block 4 is one Spawn Point/Entrance. When opening an **FBN**, you will likely see many Blocks. In the **Value** column of the 010 Template Output will be the Block Type and therefore you need to open Block 4.\
\
Each Entry looks like this:

```clike
s32 Field00;
s32 Field04;
Vector3 Position;
Vector3 Rotation;
s16 Id;
s16 Field22;
```

It's currently unknown what **Field00** and **Field04** do, but the next 3 values are important. Ingame, walk to a location you deem for a Spawn Point and open the Mod Menu or simply place a node in 3DSMax. These are the **XYZ** values to be filled into the **Position** Vector. The same applies to the **Rotation** Vector as long as the rotations are in **FBN Standard Rotation**.&#x20;

{% hint style="info" %}
FBN Standard Rotation is different from Euler Degrees. If you don't know how to convert Euler Degrees into FBN Standard Rotation, [THIS](../../basics/rotation-conversions.md#euler-degrees-to-fbn-standard-rotation) is how.
{% endhint %}

To add a new field to this table, Copy and Paste an Entry and change the **Entry Count** on top. Make sure to add the Entry size to the **Size** value _( 36 bytes )._

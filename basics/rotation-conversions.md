---
description: I bet you haven't even HEARD of Quaternion tbh
---

# Rotation Conversions

{% hint style="info" %}
Remember, Persona 5 occasionally shifts from Y-Up to Z-Up so it's best to test rotations converted Ingame before proceeding.&#x20;
{% endhint %}

## Euler Degrees to Quaternion

A reliable way to convert the traditional XYZ Rotations into Quaternion XYZW Rotations used occasionally by Persona 5 is [https://www.andre-gaschler.com/rotationconverter/](https://www.andre-gaschler.com/rotationconverter/).

On the site, set Input to Degrees and Output to Radians and type in your desired rotations into Euler angles of multiple axis rotations ( degrees ).

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Make sure the dropdown is XYZ and nothing else</p></figcaption></figure>

Subsequently, your output will be printed out in Quaternion \[ x,y,z,w ].

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>The Quaternion conversion of ( 35, 90, 0 )</p></figcaption></figure>

## Euler Degrees to FBN Standard Rotation

Using the site mentioned above, set Input to Euler angles of multiple axis rotations ( degrees ).

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>Make sure the dropdown is XYZ and nothing else</p></figcaption></figure>

On the right side of the screen will be the Rotation Matrix. Grab the rightmost column of values and treat this as XYZ.

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption><p>The FBN Standard conversion of ( 35, 90, 0 )</p></figcaption></figure>

---
description: field/fldResident.pac/ftd/fldPlayerSpeed.ftd
---

# Adjusting Joker's Speed

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>Viewable in 010 Editor using my fork of the .FTD Binary Template</p></figcaption></figure>

This is the _entirety_ of **fldPlayerSpeed** in Persona 5. It's quite a small file because while fully functional, ATLUS did not find many uses for it. So few, in fact, it actually makes this slightly more annoying to edit because of how they designed it.\
\
In the template, under the 0th List, you should see two Entries. This is somewhat deceiving as ATLUS **** hardcoded the game to **ignore** the last entry. Luckily, the game only ignores the "last" entry and functions perfectly for any Entries added _before_ the last one.\
\
Each Entry looks like this:

```aspnet
short FieldMajorID;
short FieldMinorID;
short WalkSpeed;
short RunSpeed;
u8 AccelFrames;
u8 DecelFrames;
u8 StaticTurnFrames;
```

This is exactly as it appears. The **Field Major ID** and **Minor ID** tell the game what field to target with the subsequent values. \
\
**Walk Speed** is used when the Analog Stick is hardly tilted and **Run Speed** is for full directional tilt. **Accel and Decel Frames** are the time in frames required for Joker to reach full speed when the Stick is tilted from Idle and full stop when the Stick stops moving. **Static Turn Frames** is an overworld value for how long it takes Joker's rotation to face an opposite direction if the stick is flipped in direction.

{% hint style="warning" %}
NOTE: The default values for Joker when not modified in this table have not been found yet! Experiment with Trial and Error until it feels right to you. &#x20;
{% endhint %}

To add a new field to this table, Copy and Paste an Entry and change the **Entry Count** on top. Make sure to add the Entry size to the **Data Size** value _( 12 bytes )._

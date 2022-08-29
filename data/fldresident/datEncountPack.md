---
description: field/fldResident.pac/ftd/datEncountPack.ftd
---

# Assigning Palace Encounters

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Viewable in 010 Editor using my fork of the .FTD Binary Template</p></figcaption></figure>

This is a standard Entry found in the **Encounter Pack Data**. It contains the data used for rotating CHANCE ( Ambush ) Encounters as well as many variants used for PINCH and Encounters with Strong Shadows. \
[fldDngPack.ftd](fldDngPack.md) picks out one Entry from this table to apply to any particular Palace field.\
\
Ingame, Ambushing a Shadow from behind rotates between **8 Encounters,** while getting detected randomizes the Encounter ID based on several conditions entering battle, with the maximum being a random list of **13 Encounters** for being detected but being able to strike first, and a standard of **5 Encounters** for any other condition.\
\
Each Entry looks like this:

```clike
u8 field_0;
u8 UnusedSlot[ 7 ];
u16 AmbushList[ 8 ];
ENC NormalEncounter[ 13 ];
ENC NormalPinchEncounter[ 5 ];
ENC AlternateNormalEncounter[ 5 ];
ENC AlternatePinchEncounter[ 5 ];
ENC StrongEncounter[ 5 ];
ENC StrongPinchEncounter[ 5 ];
ENC TreasureEncounter[ 5 ];
ENC ReaperEncounter[ 1 ];

//ENC Data Type:
u16 EncounterID;
u8 Weight;
```

Each one of the 8 **AmbushList** Shorts is an Encounter ID in **ENCOUNT.TBL** and is rotated after every Victory. However, for the various other Encounter Lists there is also a **Weight** value out of 100 which acts as the Bias for that particular Encounter to be picked.

To add a new Entry to this table, Copy and Paste an Entry and change the **Entry Count** on top before editing the appropriate _DngPack_ Entry to point to the new _EncountPack_ Entry. Make sure to add the Entry size to the **Data Size** value _( 16 bytes )._

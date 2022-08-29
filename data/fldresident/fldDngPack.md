---
description: field/fldResident.pac/ftd/fldDngPack.ftd
---

# Editing Palace Loot & Enemies

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Viewable in 010 Editor using my fork of the .FTD Binary Template</p></figcaption></figure>

This is the **Dungeon Pack** table for Madarame's Museum. Every 16 bytes is one DngPack Entry and represents one Palace field. DngPack is responsible for assigning what **Shadows** are available to a field as well as what is inside of **Chests** and **Search Objects**. \
Due to the conditions in which this table is triggered, it is **impossible** to transplant any of this data to apply on a Overworld field.\
\
In **Persona 5,** any field with a Major ID over 100 is considered a Palace field. Most Palaces in the game stick to one Major ID while using multiple Minor IDs to store each field in the Palace. \
When a Palace field is loading, the game uses math to calculate which DngPack Entry applies to the target field.

{% hint style="warning" %}
Palaces by themselves are not hardcoded to stay under one Major ID. Kamoshida's Castle, for example, takes up 2. However, many other mechanics relating to Palaces are hardcoded and therefore not easy to work with.
{% endhint %}

When opening the **FTD** in the Template, you may notice there are several Lists with Entries under each. The game uses the Lists as a way to organize Major IDs and Entries for Minor IDs. \
\
The game subtracts 150 from the target field's Major ID and that is used as the List #, while the Minor ID is used as the Entry # under the calculated List.

```
f151_019 - Field Major ID 151 || Field Minor ID 019

151 - 150 = 001
List Number 1
019 --> Entry

f151_019 --> fldDngPack List 1, Entry 19
```

Each Entry looks like this:

```clike
u16 EncountPackEntry;
u16 ObjFlagEntry;
u16 TboxRndEntry;
```

These are all **value pointers** to various Entries in _other_ FTD files within the Field Resident which will subsequently be applied to the target Palace field. \
( [datEncountPack.ftd](datEncountPack.md), fldObjFlag.ftd, datTBoxRnd.ftd )\
A short blurb on their intended functions can be found in the [Editing Field Resident Tables main page](./).

To add a new field to a List, Copy and Paste an Entry and change the **Entry Count** on top. Make sure to add the Entry size to the **Data Size** value _( 16 bytes )._

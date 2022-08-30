---
description: field/fldResident.pac/ftd/fldObjFlag.ftd
---

# Creating Treasure Chests

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Viewable in 010 Editor using my fork of the .FTD Binary Template</p></figcaption></figure>

This is a standard Entry in the **Field Object Flag FTD**, an admittedly confusingly named table used specifically for assigning items to Treasure Chests ( internally known as **TBox** ). Each Entry contains **10** Chest Objects and each Chest contains **6** Item Slots for a total maximum of **60** Items.\
****\
****Each Entry is not applied to a field by default, but instead referenced via Data Pointer in **fldDngPack.ftd**, **** which is covered under **** [**Editing Field Resident Tables > Editing Palace Loot & Enemies**](fldDngPack.md).\
Item IDs are not strictly used in the table. They, as well, are defined in a different **FTD**, **datTBox.ftd**, which is covered under [**Editing Field Resident Tables > Adjusting Palace Items**](datTBox.md). \
\
Each Entry looks like this:

```clike
u32 Flag;
struct fldObj Object[10];
```

```clike
// fldObj Struct Definition
u32 Flag;
u16 datTBox_Entry[6]; 
```

The **Flag** value is the **"TBox Flag"**, a value that's grabbed by most Chest scripts ( or "box" scripts ) via **FLD\_GET\_TBOX\_FLAG**() returning this value. It's a Bitflag used to keep track of whether a Chest has or has not been opened. Most functions in box scripts also come with a fail-safe to not open if the returned **TBox Flag value** is NULL or 0.\
\
When opening this **FTD** with the Template, the 6 Items in each Chest should be labelled. You can use these to select anu changes but keep in mind that they are not the Item IDs, but references to **datTBox.ftd,** which you will need to edit to customize things further. ****&#x20;

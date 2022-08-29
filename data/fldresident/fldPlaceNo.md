---
description: >-
  field/fldResident.pac/ftd/fldPlaceNo.ftd
  field/fldResident.pac/ftd/fldDngPlaceNo.ftd
---

# Editing Field Subtitles

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Viewable in 010 Editor using my fork of the .FTD Binary Template</p></figcaption></figure>

This is a standard set of entries in the **Place Number FTD file**. When loading a field, the game references the Place Number **FTD** with the target Field Major and Minor ID and prints the associated **fldPlaceName.ftd** Entry on the lower right hand corner of the GUI. \
\
When a field is loading, the game uses simple math to calculate which PlaceNo Entry applies to the target field. The **Field Major ID** is applied to the List while the **Field Minor ID** is applied to the Entry under the List. Field 006\_001 would use List 6, Entry 1.\
\
Editing the **fldPlaceName FTD**, as well as other **String Table FTD** files, is covered in [**Editing Field Resident Tables > Generating String Tables**](string.md).

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>fldPlaceName.ftd Entry 267</p></figcaption></figure>

Each Entry looks like this:

```
u16 PlaceName_Entry;
u16 PlaceName_Subtitle_Entry;
u32 Padding;
```

Each value here is a pointer to an entry in **fldPlaceName.ftd,** with Subtitle being for the 2nd Row seen in sublocations.

Adding a value to this table is very tedious compared to editing an unused entry, as it requires copying a previous List / Entry, adding a new 4 byte **Data Pointer**, then adjusting every _other_ **Data Pointer** with the new offset locations of the Lists and Entries. ****&#x20;

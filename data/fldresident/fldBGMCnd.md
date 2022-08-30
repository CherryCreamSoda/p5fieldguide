---
description: field/fldResident.pac/ftd/fldBGMCnd.ftd
---

# Reworking Music Conditions

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Viewable in 010 Editor using the BGMCND Fork of the .FTD Binary Template</p></figcaption></figure>

This is the Entry in the **Background Music Conditions** that plays _"Beneath The Mask - Rain"_ from May onward during Rainy days. Each Entry in this file contains similar conditions that control **when and where** a music track should play. \
\
This is not _exclusively_ how music is triggered, as cutscenes and various scripts do have their own overrides, but this file is what registers the default looping music for a field at any given time and story progress. \
\
Each Entry looks like this:

```
int16 fldMajorID;
int16 fldMinorID;
byte monthStart;
byte dayStart;
byte monthEnd;
byte dayEnd;
byte Weather;
short musicID;
int16 flagCondition;
```

{% hint style="warning" %}
It should be noted this list excludes values in the real struct which are **unknown** and truncates Enums to their **original** data type.&#x20;
{% endhint %}

Each value is partially self-explanatory. The **Field Major ID** and **Minor ID** tell the game what field to target with the subsequent values. \
The **Month/Day Start** and **End** indicate the timeframe for the music condition to be true and the **Weather** indicates the same for specific weather conditions. \
\
The **musicID** is the Cue ID in the bgm.acb that links to the corresponding music track.  \
**flagCondition** specifies that the condition can only play the assigned music if it's parameters are met _and_ the specific BitFlag is on. A negative 1 in any field indicates that it's **infinite**, such as applying to all days or all fields.\
\
To add a new condition to this table, Copy and Paste an Entry and change the **Entry Count** on top. Make sure to add the Entry size to the **Data Size** value _( 20 bytes )._ Make sure the condition isn't overwritten by any others on top of it.

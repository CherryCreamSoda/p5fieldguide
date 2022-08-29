---
description: >-
  fldCheckName.ftd fldDngCheckName.ftd fldKFECheckName.ftd fldNPCName.ftd
  fldPlaceName.ftd
---

# Generating String Tables

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>Viewable in 010 Editor using the .FTD Binary Template</p></figcaption></figure>

This is a standard set of Entries in a String Table **FTD**. In the Header of every **FTD** is a value that tells the game whether to parse the **FTD** as values or text. \
Note that Persona 5 Strings are both Length-Specific _and_ Null Terminated. This means that while the Strings have a dedicated **Length** value, the game also stops reading when it reaches a Null character.&#x20;

{% hint style="info" %}
This is not to be confused with a space character. The Null that acts as an escape character is 00 while a standard space is 20.
{% endhint %}

The general structure of a String Table is the **Header,** a list of **Data Pointers** and the **Strings**. \
The issue with Data Pointers is that editing the **FTD** becomes challenging when it means that any increase or decrease in Size will require editing every single **Data Pointer**. \
Luckily, there is an easier solution.&#x20;

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption><p>fldCheckName.ftd converted with p5FTDStringConverter</p></figcaption></figure>

The _P5FTDStringConverter_ Program converts **String Table FTD** files into standard .TXT and back again. Simply drag your intended **FTD** onto the Program and make any edits you need in the TXT file.

{% hint style="danger" %}
Remember to work within the limitations of the **FTD** format. No String can be longer than 255 Characters and there can be no more than 32,766 Entries
{% endhint %}

---
description: Touch and Go
---

# Editing Interactables

Most field PAC files contains an **.FBN** file as well as one or more **.HTB** files, or _Hit Tables_. Hit Table files are files that assign an interactable range in the **FBN** with various properties to form one basic Interactable.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption><p>A visual representation of an Interactable</p></figcaption></figure>

For basic Interactables, there are 14 different "Prompt Tables" values which control both the type of Prompt that appears as well as what **Field Resident FTD** is used to populate the Prompt with text. &#x20;

{% hint style="info" %}
Some Interactables are invisible and do not have an assigned Prompt Table. Perplexingly, the only 2 modes of Interactables are 0 for invisible and 2 for Prompt.&#x20;
{% endhint %}

For convenience, here is every known Prompt Table value. &#x20;

| ID # |         | Prompt Table                                  | Icon                                                                  |
| ---- | ------- | --------------------------------------------- | --------------------------------------------------------------------- |
| 0    | Examine | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Examine.png" alt="" data-size="line">    |
| 1    | Go      | ( Blank )                                     | <img src="../.gitbook/assets/Go.png" alt="" data-size="line">         |
| 2    | Examine | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Examine.png" alt="" data-size="line">    |
| 3    | Examine | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Examine.png" alt="" data-size="line">    |
| 4    | Examine | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Examine.png" alt="" data-size="line">    |
| 5    | Examine | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Examine.png" alt="" data-size="line">    |
| 6    | Steal   | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Steal.png" alt="" data-size="line">      |
| 7    | Action  | field/fldResident.pac/ftd/fldActionName.ftd   | <img src="../.gitbook/assets/Action.png" alt="" data-size="line">     |
| 8    | Action  | field/fldResident.pac/ftd/fldActionName.ftd   | <img src="../.gitbook/assets/Action (1).png" alt="" data-size="line"> |
| 9    | Action  | field/fldResident.pac/ftd/fldActionName.ftd   | <img src="../.gitbook/assets/Action (2).png" alt="" data-size="line"> |
| 10   | Talk    | field/fldResident.pac/ftd/fldNPCName.ftd      | <img src="../.gitbook/assets/Talk.png" alt="" data-size="line">       |
| 11   | Go      | field/fldResident.pac/ftd/fldPlaceName.ftd    | <img src="../.gitbook/assets/Go.png" alt="" data-size="line">         |
| 12   | Shop    | field/fldResident.pac/ftd/fldCheckName.ftd    | <img src="../.gitbook/assets/Shop.png" alt="" data-size="line">       |
| 13   | Examine | field/fldResident.pac/ftd/fldKFECheckName.ftd | <img src="../.gitbook/assets/Examine.png" alt="" data-size="line">    |

{% hint style="warning" %}
In a Palace Field, any Interactable referencing a **fldCheckName.ftd** Prompt Table becomes **fldDngCheckName.ftd,** adjust accordingly.
{% endhint %}

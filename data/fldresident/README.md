---
description: The real Peat and Motatos.
---

# Editing Field Resident Tables

Found in **field/fldResident.pac**, Field Resident is a large container loaded on boot that contains a few dozen tables in the form of **.FTD** files that control various parameters and features of fields.

For a field to truly be considered "functional", you will most likely need to edit the Field Resident FTD files at some point.&#x20;

| Filename                                                                                                    | Function                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| <p>fldCheckName.ftd<br>fldDngCheckName.ftd<br>fldKFECheckName.ftd<br>fldNPCName.ftd<br>fldPlaceName.ftd</p> | Contains a long list of strings used in interactable prompts or GUI Elements.                                                          |
| <p>fldPlaceNo.ftd<br>fldDngPlaceNo.ftd</p>                                                                  | Contains a list tying each field ID / Palace field ID to a string in fldPlaceName to put on the lower right hand corner of the GUI.    |
| [datEncountPack.ftd](datEncountPack.md)                                                                     | Contains blocks of available Encounters and their chances per field, as well as multiple variations.                                   |
| datTBox.ftd                                                                                                 | Contains the Item ID and quantity of every item you can obtain in a Treasure Chest or Search Object.                                   |
| datTBoxRnd.ftd                                                                                              | Contains the RNG% Chances for specific datTBox Items in a Palace field's Search Objects.                                               |
| fldBFldPack.ftd                                                                                             | Contains unique IDs that tell the game what battlefield ID is used in regular Encounters when not specified in the ENCOUNT.TBL.        |
| fldBGMCnd.ftd                                                                                               | Contains an index of what BGM Cue plays on any given field depending on the date, weather and story conditions.                        |
| [fldDngPack.ftd](fldDngPack.md)                                                                             | Contains values tying each Palace field ID to an entry in datEncountPack, fldObjFlag and TboxRnd.                                      |
| fldEnvList.ftd                                                                                              | Contains an index of what .ENV file is applied to a field as well as which fields can have their ENV changed with the weather.         |
| fldFootStepCnd.ftd                                                                                          | Contains a list of field IDs that can have footstep sounds, as well as what the sound is ( although this can be changed in the GFS ).  |
| fldObjFlag.ftd                                                                                              | Contains entries of 6 datTbox Items which specify the contents of any particular Treasure Chest.                                       |
| [fldPlayerSpeed.ftd](fldPlayerSpeed.md)                                                                     | Contains mostly unused data that controls Joker's maximum speed and acceleration/deceleration on any given field ID.                   |
| fldSaveDataPlace.ftd                                                                                        | Contains a field ID and string to tie to the Save Menu Journal according to the current field ID.                                      |


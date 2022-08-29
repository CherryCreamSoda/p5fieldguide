---
description: ACHSUALLY IT'S HEXADECIMAL HURRR
---

# Editing Field Binary Files

Each field **.PAC** contains a **.FBN** file, or Field Binary Data. In it's various Blocks, each FBN controls various placements and properties of each field.&#x20;

Without an FBN, your field will not function correctly or load. It is essential at the base level and for more high-level creations.&#x20;

<table><thead><tr><th data-type="number">#</th><th>Block Name</th><th>Block Function</th></tr></thead><tbody><tr><td>1</td><td>Trigger Block</td><td>Adds ranges of coordinates used to place invisible interactable zone hitboxes of various shapes and sizes.  </td></tr><tr><td>4</td><td><a href="block4.md">Entrance Block</a></td><td>Specifies multiple places where Joker can spawn into a field along with an ID used for scripting events to certain Entrances.</td></tr><tr><td>9</td><td><a href="block9.md">Chest Block</a></td><td>Places any object model from <strong>model/field_tex/object</strong> that the game prepares to be a Treasure Chest at runtime.   </td></tr><tr><td>10</td><td>Cover Block</td><td>Adds locations where Joker can press X to Hide from incoming Shadows in Palace fields, as well as travelling between them. </td></tr><tr><td>11</td><td>Symbol Block</td><td>Spawns Shadows ( internally known as <strong>"Symbols"</strong> ) and charts out each's path to travel on when not chasing Joker.</td></tr><tr><td>14</td><td>Field NPC Block</td><td>Specifies the ID and position ( or path of positions ) for each interactable NPC. </td></tr><tr><td>18</td><td>Search Block</td><td>Places any object model from <strong>model/field_tex/object</strong> that the game prepares to be a Search Object at runtime.</td></tr><tr><td>19</td><td>Search Hit Block</td><td>Adds ranges of coordinates used to place invisible interactable zones meant specifically for Search Objects. </td></tr><tr><td>22</td><td>Voice Hit Block</td><td>Adds ranges of coordinates used to place invisible interactable zones meant specifically for voicelines in Palace fields.</td></tr></tbody></table>


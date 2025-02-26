------------------------------------------------------
Version 1.4.0
------------------------------------------------------
Updated to 1.20.4

**Mod Interactions**
- REI no longer appears on the RPG dialogue screen variant

------------------------------------------------------
Version 1.3.1
------------------------------------------------------
**Fixes**
- Fixed the `/blabber` command failing to find dialogues added through regular datapacks

------------------------------------------------------
Version 1.3.0
------------------------------------------------------
**Additions**
- Added a new `DialogueActionV2` interface that lets mods act upon the interlocutor in a dialogue

------------------------------------------------------
Version 1.2.0
------------------------------------------------------
**Additions**
- Dialogues now support advanced text components, like entity selectors and scores
- You can now specify an *interlocutor* when starting a dialogue
- The interlocutor entity can be referred to in commands and texts using a new entity selector, `@interlocutor`
- It can also be referred to using a new loot condition, `blabber:interlocutor_properties`

**Changes**
- Dialogues can now be reloaded using the `/reload` command

------------------------------------------------------
Version 1.1.0
------------------------------------------------------
**Additions**
- A new dialogue screen you can use : the RPG layout, ideal for dynamic NPC dialogues with short choices
  - This new layout can be chosen on a per-dialogue basis - look at [the documentation](https://ladysnake.org/wiki/blabber#layout) for details

**Changes**
- Updated the French localization

**Fixes**
- Fixed scrolling in the dialogue screen behaving erratically

------------------------------------------------------
Version 1.0.0
------------------------------------------------------
- Updated to MC 1.20.2
- First version available on Modrinth

**Additions**
- _Conditional choices !_
  - A dialogue choice can require an arbitrary condition in the form of a JSON predicate
  - You can make it so that, when a choice is unavailable, it displays as either grayed out or hidden entirely
  - Grayed out choices display a customizable explanation when hovered
  - Conditions are refreshed every tick while a dialogue is active
  - Blabber will warn you in the logs at initialization if a dialogue has a risk of leaving a player without choices
- You can now see a little arrow icon next to the currently selected choice
  - This icon gets replaced with a lock when the choice is unavailable
- If despite all validation a player ends up on a dialogue screen with no choice available, they will now see an "escape hatch" choice suggesting they report the issue

**Changes**
- **BREAKING :** Dialogues are now loaded from `data/<namespace>/blabber/dialogues/` instead of `data/<namespace>/blabber_dialogues/`
- **BREAKING (for modders) :** The maven group and package are now `org.ladysnake` instead of `io.github.ladysnake`

**Mod Interactions**
- REI and EMI no longer appear on the dialogue screen

------------------------------------------------------
Version 0.6.0
------------------------------------------------------
Updated to MC 1.19.4

------------------------------------------------------
Version 0.5.1
------------------------------------------------------
Fixes
- Fixed quilt incompatibility caused by unsupported API

------------------------------------------------------
Version 0.5.0
------------------------------------------------------
Updated to MC 1.19.3

------------------------------------------------------
Version 0.4.0
------------------------------------------------------
Updated to MC 1.19.1

------------------------------------------------------
Version 0.3.0
------------------------------------------------------
Updated to MC 1.19

Additions
- Dialogues now get validated upon world loading - the following issues will cause failures :
  - Infinite loops preventing users from reaching a dialogue state with type `dialogue_end`
  - Dialogue states that are not endings but offer no choice either (unless it is guaranteed that players cannot reach them)

------------------------------------------------------
Version 0.2.0
------------------------------------------------------
- Updated to 1.18.2

------------------------------------------------------
Version 0.1.3
------------------------------------------------------
- Updated CCA dependency => **Update your dependencies: `io.github.onyxstudios.Cardinal-Components-API` -> `dev.onyxstudios.cardinal-components-api`

------------------------------------------------------
Version 0.1.2
------------------------------------------------------
- Fixed `unskippable` not being actually optional
- Made more errors appear when loading an invalid dialogue definition file

------------------------------------------------------
Version 0.1.1
------------------------------------------------------
- Add localization for dialogue instructions (thanks cominixo01, Tijmen, BingQI, and AwsAlex!)

------------------------------------------------------
Version 0.1.0
------------------------------------------------------
Initial version

Additions
- Data-driven dialogues
- In-game command to start a dialogue

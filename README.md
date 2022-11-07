# CRuncher
Foundry VTT mod for creating or adjusting NPCs CR dynamically within the D&D 5e ruleset

#### Video Demo:  <URL HERE> 

# Purpose
<p>
This module is meant for building individual NPCs allowing you to adjust features and dynamically see the resulting change to the creatures Challenge Rating. Allowing you to tailor an NPC to your needs. It's not meant to be an "encounter builder", there are other modules and services out there for that. 
</p>
<p>
The CR calculators I've tried in the past didn't quite work for me, I remember one didn't even have all the options that adjust CR listed in the DMG for instance. Also of the ones I tried they didn't dynamically update the CR as I was making adjustments so it was a process that wasn't as smooth as I'd hoped it'd be.
</p>
<p>
To set expectations up front I'd like to say that although supporting other systems would be cool, I don't currently play other systems and so I'm not familiar with how they handle Challenge Rating. I may take it on as a project to gain experience coding but not likely in the near future.
</p>

# Features
  ## Must haves
  - Character sheet UI
  - Ability to choose either a default set of stats or drag and drop an actor onto the sheet to populate starting stats
  - Any changes to stats, features, spells, etc update the CR of the actor dynamically
  - All features from the DMG that adjust CR
  - A field for calculated Offensive and Defensive CRs to help with understanding the breakdown of how the CR calculated
  - A new attribute which can be modified for any feature, item, spell, etc. which can be modified by the user allowing them to customize how much they think something   would adjust a creatures CR.
  - Fully respect user permissions setup by the GM for what players can or can't see.
  - Create module with language localization in mind for non-english speaker's
  
  ## Would like to haves
  - View inventory on an NPC sheet, or legendary actions and lair actions on the PC sheet. 
  -- When I'm making main NPCs that are special I like to set them with actual inventory when I create them to streamline things during game play. The default NPC sheet doesn't allow this, so I usually end up using the PC sheet, but that one doesn't show legendary actions and lair actions so I have to choose which I want to do without. I'd like to fix that with this module, either with a custom character sheet, or perhaps my module can simply have a toggle to show or hide those things on each sheet?
  - Allow the GM a suite of user preferences
  -- Allow the players to use the module, while respecting what compendia they can draw from or save to
  -- Set what they'd like the default stats for a new actor is. Perhaps with choice for random generation methods like 4d6 drop the lowest etc
  -- Set a default of where new actors are saved to, whether it's the actors tab or a compendium.
  -- Set hotkeys for things like launching the module, quick saving an actor they're working on, reset stats to default, maybe one to re-roll stats.
  - Ability to randomly generate a new actor
  -- Perhaps be able to say generate 10 goblins randomly or whatever
  -- Maybe the user could set a base creature, set the things they want everyone to have, then any field they don't fill in is randomly generated?
  - Support of other systems?

# Files and their purposes
- module.json defines the module and describes the features of the module. Somewhat similar to a requirements.txt this file is the key for Foundry knowing the files within this data structure are part of a module. {userData}/Data/modules/CRuncher/module.json for example.

- /lang/*.* Files for language localization
- /scripts/*.* Javascript files just like for a web page project.
- /templates/*.* For Html templates, like /scripts/ it's just like for a web page
- /styles/*.* CSS files
- /packs/*.* These files are the database files for compendium content used by Founder, basically json files, or a file of json items.
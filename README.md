## PPMeter - Baldur's Gate 3 damage counter mod
Party Performance Meter mod - shows how much damage and healing each character deals and takes.

[Mod page on mods.io](https://mod.io/g/baldursgate3/m/ppmeter-damage-statistics-by-slafniy)

![ppmeter_description.png](images/ppmeter_description.png)

### Compatibility
I believe this mod is atomic and compatible with any other mod.  

Important notes:
- Requires Keyboard+Mouse UI, won't work with a Controller!
- Does not require a new game.
- Does not break a game if you disable it mid-game.
- Will work if you re-enable it, but will reset data on the first fight.
- Should be compatible with other GUI mods. Please let me know if you have issues.
- Does **not** use ScriptExtender, written entirely in Osiris.


### What it does
PPMeter accumulates combat data for party members and shows it in a table.
- It counts rounds in combat per character.
- It counts damage dealt by party characters, including damage from summons and barrels.
- It counts damage taken from enemies.
- It counts healing done and received. 
- It calculates averages per combat round: 
  - DPR (Damage Per Round)
  - DTPR (Damage Taken Per Round)
  - HPR (Healing Per Round)
  - EHPR (External Healing Per Round)
  - SHPR (Self-Healing Per Round)
- It stores data for different time ranges:
  - Combat - resets when character enters combat.
  - Day - resets on long rest.
  - Level - resets when character accepts levelup.
  - Overall - never resets.

    
### Known limitations
- Cannot guarantee correct healer detection if two or more healers use their heal abilities simultaneously, PPMeter needs at least 0.1 sec window between them.
- Healing from [Amulet of the Drunkard](https://bg3.wiki/wiki/Amulet_of_the_Drunkard) does not count.
- Temporary HPs do not count, except from [Boots of Aid and Comfort](https://bg3.wiki/wiki/Boots_of_Aid_and_Comfort).
- Damage made while hiding does not count.


### Development and future plans
 [List of bugs/suggestions on Github](https://github.com/slafniy/PPMeterProject/issues) - feel free to add issues there, or in comments on Nexus or mod.io.

Features I'd like to implement:
- Count CC and debuffs time on enemies
- Count buffs time on allies
- Count damage outside of combat
- Count healing outside of combat
- Count other little stats like killing blows, downed time, friendly fire etc.


##### About me and this project
This project exists because I was too lazy to calculate damage by hands, and I needed data for my Global [DedTuned balance mod](https://mod.io/g/baldursgate3/m/dedtuned).

I'm developing this in my free time, so I cannot guarantee quick bugfixes or updates. Also, I'm not a GUI programmer and I struggle with Noesis/XAML, so if someone wants to help me please contact :) I'd really want to reduce the amount of boilerplate code and make headers prettier. Also, I'd listen very carefully if you have better idea how to bind data from Osiris to GUI without ScriptExtender (current version uses hidden ActionResources).
#Raiding and Parties
##Post Random Dungeon LFG Message in LFG Channel
```
/run local a,b,c,d,t,h,r,l,z;a,b=UnitClass("player");c=UnitLevel("player");l,t,h,d=GetLFGRoles();r="";if d then r=r.."DPS " end;if t then r=r.."TANK " end;if h then r=r.."HEALER" end;z= a.." LEVEL "..c.." LFG RDF "..r;SendChatMessage(z,"CHANNEL",nil,4)
```

* Use: Post a Random Dungeon Looking for Group Message in LookingForGroup channel.
* Note: That macro collect information about your class, level, and the functions in a party you have signed for in the dungeon finder and send a looking for group message, with the collected information, to LookingForGroup channel.

##Reload UI and notify group
```
/afk reloading UI
/run SendChatMessage("reloading my UI - afk for a sec", ((UnitInRaid("player")and "RAID")or(GetNumPartyMembers()>0 and "PARTY")or "AFK")); 
/console reloadui
```

* Use: Reload your UI, send a message to your party/raid telling them you're doing so and set an appropriate /afk message.
* Works in 3.2.0a

##Autoassist tank if the tank's target can be attacked
```
/target [@focustarget, harm, nodead]
```

* Use /focus to set focus on the main tank (or right click on the tank and select focus).
Your target will be set to the main tank's target, but only if the tank is targeting an enemy which is alive.
* Works in 3.3
```
#show Attack
/target [@focustarget, harm, nodead]
/startattack
```

The melee dps version also starts attacking, and sets the icon to your attack ability.

##Multi-Purpose Party/Solo Attack Spell
```
#showtooltip <spellname>
/cast [harm] [@targettarget, harm] [@focus, harm] [@focustarget, harm] <spellname>
```

* Use: Cast an attack spell with limited need to change target. Is not useful for AoE spells as they often do not use a direct target.
* Note: Replace <spellname> (including the <> signs) with the name of the ability you want to cast and don't forget to replace both places <spellname> shows up.
* Tested and working in 4.0.6

This macro works a little differently than some others, as it does not perform a change to your playstyle, but merely limits mouse clicks (if desired) and encourages coordinated assaults. This casts a spell or ability on a priority based target. If you are targetting an enemy, it will cast at your target; if you are targeting a friend who is attacking a mob, it will cast at their target; if you have no target, but your focus is a mob (i.e. boss fight), it will cast at the mob; and finally if you have no target but your focus is friendly and has an enemy target, it will cast at the enemy.

This has been particularly useful for our guild, allowing us to easily coordinate assaults without the requirement for mad AoE damage. Our Off-tanks typically select the main tank as their focus, while our DPS (ranged and melee) select their particular tank or off tank. When the focus changes targets, the DPS are immediately updated to the new target. Quite Handy! For soloing or special circumstances where each person needs their own target, the macros don't hinder us in anyway because it chooses OUR target first.

Example
```
#showtooltip Fire Blast
/cast [harm] [@targettarget, harm] [@focus, harm] [@focustarget, harm] Fire Blast
```

##Multi-Purpose Party Healing
```
#showtooltip <spellname>
/cast [help] [@targettarget, help] [@focustarget, help] [@focus, help] [@player] <spellname>
```

* Use: Cast an healing/buff spell with limited need to change target. Is not useful for AoE spells as they often do not use a direct target.
* Note: Replace <spellname> with the name of the ability you want to cast. This includes the <>! And don't forget both places!
* Tested and working in 4.0.6

This macro works like the above, save the order of priority is switched a little (based on observed need). It can be used with a number of strategies, particularly when combined with the above macro. Priorities are as follows: If you are targeting a friendly, cast at them; if your target is targeting a friendly, cast at the friendly (useful for quick adds and bosses with random targeting); if your focus is targeting a friendly, cast at the friendly (useful for bosses); if your focus is friendly, cast at the focus; otherwise, cast at yourself.

Particular bonus when you are using the Multi-Purpose Attack Spell above, as it means you may keep the same person targeted for both healing and harming. You may also create awesome heal groups, for parties with weak AoE heals setting one person as the "main heal". These are just a couple of uses.

#Parties
##Announce Vent in Party
```
/party My Guild Vent | abc.leetvent.com
/party My Guild Vent | 1234
/party My Guild Vent | secretpassword
/party Normalize Vent - http://some.vent.server/somewhere
/threshold rare
```

* Use: Announces your Vent details to your party, sets your loot threshold Rare if you are the leader.
* Works in 3.1.1

#Raiding
##Announce Vent in Raid
```
/rw Vent Details Posted
/raid My Guild Vent | abc.leetvent.com
/raid My Guild Vent | 1234
/raid My Guild Vent | secretpassword
/raid Normalize Vent - http://some.vent.server/somewhere
/threshold epic
/master player
```

* Use: Announces your Vent details to your raid, sets your loot threshold Epic master looter (with yourself as the master looter) if you are the leader.
* Works in 3.1.1

##List raid members without a food buff

Use this version to list members without a food buff to yourself:
```
/run nfb="[Eat!]: ";for i=1,GetNumRaidMembers()do for b=1,40 do ua=UnitAura('raid'..i,b);if ua=="Well Fed"or ua=="Food"then break;elseif b==40 and ua~="Well Fed"then nfb=nfb..UnitName('raid'..i).." ";end;end;end;print(nfb);
```

Use this version to send the list to raid chat:
```
/run nfb="[Eat!]: ";for i=1,GetNumRaidMembers()do for b=1,40 do ua=UnitAura('raid'..i,b);if ua=="Well Fed"or ua=="Food"then break;elseif b==40 and ua~="Well Fed"then nfb=nfb..UnitName('raid'..i).." ";end;end;end;SendChatMessage(nfb,"raid");
```

* Use: Click the macro to report members in raid that are neither food buffed nor eating.
* Works in 3.3.3a

##List raid members without a flask active

Use this version to list members without an active flask to yourself:
```
/run nf="[Flask!]: ";for i=1,GetNumRaidMembers()do for b=1,41 do ufl=UnitAura('raid'..i,b);if ufl then if strfind(ufl,"Flask")or strfind(ufl,"Distilled")then break;end;elseif b==41 then nf=nf..UnitName('raid'..i).." ";end;end;end;print(nf);
```

Use this version to send the list to raid chat:
```
/run nf="[Flask!]: ";for i=1,GetNumRaidMembers()do for b=1,41 do ufl=UnitAura('raid'..i,b);if ufl then if strfind(ufl,"Flask")or strfind(ufl,"Distilled")then break;end;elseif b==41 then nf=nf..UnitName('raid'..i).." ";end;end;end;SendChatMessage(nf,"raid");
```

* Use: Click the macro to report members in raid that are neither food buffed nor eating.
* Works in 3.3.3a

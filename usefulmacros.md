##General macros
Categorized list of generally useful custom macros.

#Determine current map coordinates
```
/run px,py=GetPlayerMapPosition("player"); DEFAULT_CHAT_FRAME:AddMessage(format("You are at: %s (%0.1f, %0.1f)",GetZoneText(),px*100,py*100));
```
* Use: This macro will display in your chat frame your current map coordinates with one decimal place precision. "You are at:" is flavor text.

#Swapping Talents, Equipment and Stances
##Swap Current Dual-Spec
```
/run if( GetActiveTalentGroup() == 1 ) then DEFAULT_CHAT_FRAME:AddMessage("Spec1...");SetActiveTalentGroup(2) else DEFAULT_CHAT_FRAME:AddMessage("Spec2...");SetActiveTalentGroup(1) end
/in 6 /equipset [spec:2]Eq1;Eq2
```
* Use: "Quickly" swaps your Primary/Secondary talent specs.
* Note: Also changes your equipped item set, only need to change the name of Eq1 and Eq2
* Requires: Libraries such as Ace or Chronos, that supply '/in' as a command, and will not work without.
* Works in 3.1.1

##Swap Set then Spec
```
/equipset [spec:1] PSS ; SSS
/usetalents [spec:1] 2; [spec:2] 1
```
* Use: Here is one that switches the set before the spec (may avoid some errors).
* Note: Just have to replace PSS with the name of your primary spec set, and SSS with the name of your secondary spec set.</span>

##Swap Equipment and Stance
```
/equipset [spec:1] <Secondary Set Name>; <Primary Set Name> 
/cast [spec:1] <Secondary Stance>; <Primary Stance> 
/usetalents [spec:1] 2; 1
```
* Use: This macro will switch your talent spec and put you into the respective gear and stance.

##Swap Equipment and Stance 2
```
#show [spec:1] <Secondary Stance>; [spec:2] <Primary Stance> 
/usetalents [button:1,spec:1] 2; [button:1,spec:2] 1 
/equipset [button:2,spec:1] <Primary Set Name>; [button:2,spec:2] <Secondary Set Name> 
/cast [spec:1] <Primary Stance>; [spec:2] <Secondary Stance>
```

* Use: Here is an alternate version for fury warriors that cannot use the above macro due to Titan's Grip.
* Note: Left click swaps the talent spec, right click swaps gear and stance.

##One Button Spec, Stance, Equipment
```
/cast [stance:3] Defensive Stance; [Stance:1] Berserker Stance
/usetalents [spec:1] 2; [spec:2] 1
/in 5.30 /equipset [spec:1] Tank ; DPS
```

* Use: A one button spec, stance and equipment interchanger, caters for Furry Warriors Titan's Grip

##Offhand Weapon Switching
```
#showtooltip [mod] 0 16; 17
/equipslot 17 0 16
```

* Use: manage off-hand weapons
* Note: You might find yourself in a situation where you have two offhand weapons with the same name but different poisons on them and you want to switch between them quickly. Or perhaps you just want to alternate between two offhand weapons with just one hotkey.
Keep your alternate dagger in the sixteenth slot (lower right corner) of your main (rightmost) backpack.
The number 17 refers to your offhand weapon slot. #showtooltip makes the macro's icon and tooltip display the icon of the equipped weapon, or hold down a modifier key (say Alt) and it will display the icon of the weapon that's ready to be switched in.
*Works in 3.2.2

#Suppressing Sound and Error Messages
##No Error Text or Sound (Improved)
```
/run sfx=GetCVar("Sound_EnableSFX");
/console Sound_EnableSFX 0
/cast ExampleTrinket1
/cast ExampleSpell2
/run UIErrorsFrame:Clear() 
/run SetCVar("Sound_EnableSFX",sfx); 
```

* Use: Replace "ExampleTrinket1" and "ExampleSpell2" with your cd(s) and abilities, then drag to your bar like a normal macro.
* Note: For people that macro cd's into normal spells, such as petattacks, trinkets, everlasting potions, etc. it gets annoying being spammed with "This ability is not ready" and that fun error sound. I've seen a common solution online (similar to the macro above) that fixes this problem with a single issue that's almost as bad as the problem it's fixing.
For people who play without sound to begin with, these macro will -enable your sound- every time you use them. So here is my solution. The overall effect is the same, but my macro checks to see what you sound currently is set to (enabled or disabled), disables it for the error, and then sets it back where you had it. (ex: if your sound was already off, it will prevent the text error without turning your sound on at the end)

* Works in 3.3.3a

##No Error Text or Sound (Improved Again)
```
#showtooltip ExampleSpell1
/run sfx=GetCVar("Sound_EnableSFX");
/console Sound_EnableSFX 0
/use ExampleTrinket2
/run UIErrorsFrame:Clear() 
/run SetCVar("Sound_EnableSFX",sfx);
/cast ExampleSpell1
```

* Use: Replace "ExampleTrinket2" and "ExampleSpell1" With your cooldowns and abilities, then drag to your bar like a normal macro.
* Note: This is just like the one above but with an added tooltip that matches the original skill, and doesn't disable sound for the skill's error messages. Sound and error messages for the trinket use are still suppressed though. If you set the name of the macro to a blank space, you can't even tell it's a macro. This one is designed more for trinket use than anything else, but it's here for when you only want to silence one of the two skills this macro uses
If you're running low on characters and you're using this for a trinket, you can replace the use command with "use 13" (for upper trinket) or "use 14" (for lower trinket).
* Works in 4.2

Training and Leveling
Tank check avoid, dist to def-cap
Tanks: Check unhittability, avoidance, and dist to hard-defcap

/run local b,d,p,r,a=GetBlockChance(),GetDodgeChance(),GetParryChance(),GetCombatRating(CR_DEFENSE_SKILL) a=1/(.0625+.956/(r/122.9625)) ChatFrame1:AddMessage(format("Unhittable: %.2f%%  Avoidance: %.2f%%  Defense %+.0f rating",b+d+p+5+a,d+p+5+a,r-689))
*Use Check unhittability and avoidance (+ how far away hard-defcap).
Trading, Bags and Money
Print money & currency to chat
Print Money and Currencies to Chat Frame

/script local cu = GetMoney(); print(GetCoinTextureString(cu,"12"))
/stopmacro [btn:1]
/script yy = GetNumWatchedTokens(); for xx = 1, yy,1 do aa, bb, cc, dd, ee = GetBackpackCurrencyInfo(xx); print(bb, aa) end
Left click to display your total money in the chat window.
Click any other way to display your money and all your watched currencies.
Works in 3.3.2

Sell all grey items
/run local c,i,n,v=0;for b=0,4 do for s=1,GetContainerNumSlots(b)do i={GetContainerItemInfo(b,s)}n=i[7]if n and string.find(n,"9d9d9d")then v={GetItemInfo(n)}q=i[2]c=c+v[11]*q;UseContainerItem(b,s)print(n,q)end;end;end;print(GetCoinText(c))
Use: sells all grey items, shows what was sold and how much money was made from selling
Works in 4.0.3a

Destroy all grey items
/run local i,n=0;for b=0,4 do for s=1,GetContainerNumSlots(b) do ClearCursor();i={GetContainerItemInfo(b,s)};n=i[7];if n and string.find(n,"9d9d9d") then PickupContainerItem(b,s); DeleteCursorItem() end end end
Use: destroy all grey items without confirmation
Works in 4.0.6

Item Link
/run local s={"10000"} for i=1,#s do DEFAULT_CHAT_FRAME:AddMessage("\124c00ffffff\Item Link: \124c00FF0033\124Hitem:"..s[i]..":0:0:0:0:0:0:0:0\124h[ID: "..s[i].."]\124h\124r\124c00ffffff - Click ID for item info.")end
Use: Displays an item link in the default chat frame.
Replace "10000" with the desired item ID #.
Works in 3.3.2

Spell Link
/run local s={"10000"} for i=1,#s do DEFAULT_CHAT_FRAME:AddMessage("\124c00ffffff\Spell Link: \124c00ff0033\[ID: "..s[i].."] \124c00ffffff\- "..GetSpellLink(""..s[i])..".")end
Use: Displays a spell link in the default chat frame.
Replace "10000" with the desired spell ID #.
Works in 3.3.2

Professions
Link professions in trade
Link your professions in the trade channel

Link a single profession
/script CastSpellByName(#prof#);SendChatMessage("I'll create items against mats, look out: "..GetTradeSkillListLink(),"CHANNEL",nil,GetChannelName("Trade - City"));CloseTradeSkill();
This macro sends a link with your Profession recipes to a Channel.

Replace #prof# with your profession. If your Profession is Engineering, then write:

/script CastSpellByName("Engineering");SendChatMessage("I'll create items against mats, look out: "..GetTradeSkillListLink(),"CHANNEL",nil,GetChannelName("Trade - City"));CloseTradeSkill();
Link two professions
One button to link both of your professions to trade chat and guild chat. Just replace "Inscription" and "Enchanting" with your two professions. Also, trade chat is not necessarily always your number 2 channel. Make sure you check it and adjust accordingly. Replace channel with guild to link it to your guild, or raid to link to raid chat.

/cast Inscription
/run SendChatMessage("Free with your mats "..GetTradeSkillListLink(), "channel", nil, "2")
/cast Enchanting
/run SendChatMessage(GetTradeSkillListLink().." I'll even give you 5g if I skill up!", "channel", nil, "2") CloseTradeSkill()

One-button disenchant/mill/prospect
One-Button Disenchant/Milling/Prospecting

#showtooltip
/use [nomod] Disenchant; [mod:alt] Milling;
You can of course change the order, skill and modifier to suit your needs

AIO Profession Button
#showtooltip [nomod] Enchanting; [mod:alt] Inscription; [mod:ctrl] Cooking;[mod:shift] First Aid;
 /use [nomod] Enchanting; [mod:alt] Inscription; [mod:ctrl] Cooking; [mod:shift] First Aid;
You can of course change the order, skill and modifier to suit your needs

Fishing
Fishing w/ weather-beaten fishing hat
Fishing with your Weather-Beaten Fishing Hat

#showtooltip fishing
/equip Weather-Beaten Fishing Hat;
/equip Mastercraft Kalu'ak Fishing Pole;
/use Weather-Beaten Fishing Hat
/run UIErrorsFrame:Clear()
/cast fishing
This macro will equip your fishing pole and Weather-Beaten Fishing Hat, attach lure and start fishing just by repeatedly clicking the button. One-button fishing never was easier.
Change the name of your fishing pole if you are not exalted with the Tuskar yet.
Works in 4.3.4

Fishing equipset w/ error supp
Fishing using Equipset with Error Sound/Text suppression

#showtooltip fishing
/run sfx=GetCVar("Sound_EnableSFX");
/console Sound_EnableSFX 0
/equipset [noequipped:Fishing Pole, nomod] Fish!;
/use 1
/use [equipped:Fishing Pole, nomod] Fishing
/run UIErrorsFrame:Clear()
/run SetCVar("Sound_EnableSFX",sfx);
Use: Equips fishing gear, uses item in head slot, and casts Fishing but suppresses error text/sound and ignores Equipset soundFX on repeated execution while allowing normal fishing soundFX.
This macro will equip a set named "Fish!".
You must create the equipment set, which can include all your fishing gear, especially Weather-Beaten Fishing Hat.
If you want to use a name other than "Fish!", choose a set name that is 11 characters or less (255 limit).
Drag the new macro button to an available slot and click to cast your line.
Works in 5.0.4
Equip Set With Find Fish Toggle
/equipset [equipped:Fishing Poles] 1; Fishing
/run SetTracking(1,false)
/stopmacro [equipped:Fishing Poles]
/run SetTracking(1,true)
Equips your "Fishing" set if you don't have a pole equipped and enables fish tracking, or equips set 1 if you do have a pole equipped and disables Find Fish.
The tracking toggle is set up for the first item in the tracking drop down menu. If Find Fish is the 2nd or 3rd item on the drop down, you will need to change the 1, to 2 or 3.
Useful if you're a miner/herbalist and you don't want to confuse fish with Firebloom.
Works with v4.0.3
Modifier Swap
#showtooltip
/cast [nomod] Fishing
/equip [noequipped:Fishing Poles, mod] Nat Pagle's Extreme Angler FC-5000
/equip [equipped:Fishing Poles, mod] Titansteel Guardian
/equip [equipped:Fishing Poles, mod] Matriarch's Spawn
Credit: Xaeros of Shadowmoon
Use:(Make sure to replace the fishing pole/weapons with your own)
On click, you will attempt to cast fishing.
On mod+click you will switch between your fishing pole and your weapon(s).
Works in 3.3.3a
Set Swap
/equipset [noequipped:Fishing Pole, mod] Fishing; [noequipped:Fishing Pole, nomod, spec:1] [mod, spec:1] Set1; [noequipped:Fishing Pole, nomod, spec:2] [mod, spec:2] Set2
/use [equipped:Fishing Pole, nomod] Fishing
Uses the Blizzard Equipment Manager
Requires one set called Fishing that contains your fishing pole and any equipment you want to wear while fishing (fishing hat, gloves or similar) and two sets that fit your specs (replace Set1 and Set2 with your names)
If your fishing set is equipped, click will cast Fishing, mod-click will equip the set fitting your current spec. Otherwise, mod-click will equip your fishing set, normal click will equip the spec-relevant set.

Alternate version for toons with just one spec or equipment set:

/equipset [noequipped:Fishing Pole, mod] Fishing;  [noequipped:Fishing Pole, nomod] [mod] Set1
/use [equipped:Fishing Pole, nomod] Fishing
Auto equip manager fishing
Automated Equipment Manager Fishing & Lure Macro

/equipset [noequipped:Fishing Poles, nomod] Fishing
/cast [equipped:Fishing Poles, nomod] Fishing
/use [mod:shift] Bright Baubles
/use [mod:shift] 16
/equipset [mod:alt] Normal
/equipset [mod:ctrl] DPS
Credit: Taurolyon of Sargeras-US --Taurolyon (talk) 15:53, October 14, 2009 (UTC)
To use:
Create a Fishing outfit in your equipment manager (or if you use the Outfitter Addon, save the outfit to server)
Outfit must be named Fishing
Create a Normal outfit for your primary spec
Create a DPS outfit for your secondary spec (or remove the last line in the macro if you only have one set of gear/spec)
If you don't have your fishing pole equipped, it will automatically equip your "Fishing" outfit from your equipment manager
Clicking on this macro after your fishing pole is equipped, will automatically cast your line and start fishing.
Shift-Clicking on this macro will apply a lure to your equipped fishing pole (Change Bright Baubles to any lure you'd like. I.E. Weather-Beaten Fishing Hat)
Alt-Clicking on this macro will equip your Normal set of gear.
Ctrl-Clicking on this macro will equip your DPS set of gear.
Binding this macro to a button on your mouse will allow for easy one handed casting and reeling. --Taurolyon (talk) 15:53, October 14, 2009 (UTC)

Multi Gathering Macro
#showtooltip
/cast [nomodifier] <Mount of your choice>
/cast [modifier:ctrl] Find Minerals
/cast [modifier:shift] Find Herbs
/cast [modifier:alt] Smelting
Can of course be modified to your liking and professions

Not holding down a button: Will summon a mount of your choice (Note:<Mount of your choice> has to be swapped with a mount in your possession).
Holding down ctrl: Will make mining nodes appear on your minimap.
Holding down shift: Will make herb nodes appear on your minimap.
Holding down alt: Will show the Smelting pane, where you can smelt your ore bars.

##Enchant to Vellum Macro
```
/run DoTradeSkill(GetTradeSkillSelectionIndex());
/run for i=0,4,1 do for l=1,GetContainerNumSlots(i),1 do if GetContainerItemID(i,l)==38682 then UseContainerItem(i,l);end;end;end;
/run ReplaceEnchant();
/run ClearCursor();
```

To Use:
* Open Enchanting Skill
* Select Enchantment in skill panel to apply
* Have Enchanting Vellum in your inventory
* Press macro

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

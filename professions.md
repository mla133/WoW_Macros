#Professions
##Link your professions in the trade channel

##Link a single profession
```
/script CastSpellByName("Engineering");SendChatMessage("I'll create items against mats, look out: "..GetTradeSkillListLink(),"CHANNEL",nil,GetChannelName("Trade - City"));CloseTradeSkill();
```

##Link two professions
One button to link both of your professions to trade chat and guild chat. Just replace "Inscription" and "Enchanting" with your two professions. Also, trade chat is not necessarily always your number 2 channel. Make sure you check it and adjust accordingly. Replace channel with guild to link it to your guild, or raid to link to raid chat.
```
/cast Inscription
/run SendChatMessage("Free with your mats "..GetTradeSkillListLink(), "channel", nil, "2")
/cast Enchanting
/run SendChatMessage(GetTradeSkillListLink().." I'll even give you 5g if I skill up!", "channel", nil, "2") CloseTradeSkill()
```

##One-Button Disenchant/Milling/Prospecting
```
#showtooltip
/use [nomod] Disenchant; [mod:alt] Milling;
```

You can of course change the order, skill and modifier to suit your needs

##AIO Profession Button
```
#showtooltip [nomod] Enchanting; [mod:alt] Inscription; [mod:ctrl] Cooking;[mod:shift] First Aid;
/use [nomod] Enchanting; [mod:alt] Inscription; [mod:ctrl] Cooking; [mod:shift] First Aid;
```

You can of course change the order, skill and modifier to suit your needs

##Multi Gathering Macro
```
#showtooltip
/cast [nomodifier] <Mount of your choice>
/cast [modifier:ctrl] Find Minerals
/cast [modifier:shift] Find Herbs
/cast [modifier:alt] Smelting
```

Can of course be modified to your liking and professions

* Not holding down a button: Will summon a mount of your choice (Note:<Mount of your choice> has to be swapped with a mount in your possession).
* Holding down ctrl: Will make mining nodes appear on your minimap.
* Holding down shift: Will make herb nodes appear on your minimap.
* Holding down alt: Will show the Smelting pane, where you can smelt your ore bars.

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


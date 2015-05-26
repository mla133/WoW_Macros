#Swapping Specs/Equipment
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
* Works in 3.2.2

## Speed/DPS/Heal Swapping Sets
```
#showtooltip Explorer's Walking stick
/equipset [noequipped:Staves, spec:2] Speed Dps
/equipset [equipped:Staves, spec:2] dps
/equipset [noequipped:Staves, spec:1] Speed Heal
/equipset [equipped:Staves, spec:1] healer
```
So in 6.0.2 they changed the way movement speed buffs work. They no longer stack multiplicative but they also allowed you do stack multiple movement speed buffs.

If you collect all of these items you will be moving at 150% in just normal form without any buffs or glyphs.

[Fleet Primal Diamond](http://www.wowhead.com/item=76887/fleet-primal-diamond) Easy 200 gold on auction house. Equip a random helm and gem it.

[Defiler's Cloth Boots](http://www.wowhead.com/item=20159) Any defiler boots are fine. They cost 85 honor. Alliance Horde

[Explorer's Walking Stick](http://www.wowhead.com/item=25835/explorers-walking-stick) Requires honored Cenarion Expedition OR [Runeblade of Baron Rivendare](http://www.wowhead.com/item=13505) both give the same movement speed buff. Fury warriors can equip both for a extra 10% movement speed boost (total of 160%)

Enchant the boots with any of the normal movement speed enchants like [Pandaren's Step](http://www.wowhead.com/spell=104414/pandarens-step)

[Figurine - Golden Hare] JC only! Recipe is a world drop. I found mine for 98g hold on auction house. Mats are dirt cheap.

If you wear all of those items you will have 150%(160% fury warrior) movement speed. This will still stack with all the normal movement speed buffs like Burst of speed, Ghost wolf, Stampeding Roar.

Ideally you want to have a separate armor set for all of these items so you can use a macro to swap. I named my armor set "Speed" 

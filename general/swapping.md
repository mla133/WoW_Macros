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


#General Mage Macros
##Escape Macro
```
/cast Blink
/cast Blazing Speed
```
##Ice Block
```
#showtooltip Ice Block
/stopcasting
/cancelaura Alliance Flag
/cancelaura Horde Flag
/cast Ice Block
```

##Polymorph mouseover, Remove Curse, Frostbolt macro
```
#showtooltip
/cast [@mouseover, exists, harm] Polymorph; [@focus, exists, mod:shift] Remove Curse; [@target, exists, nomod] Frostbolt
```
Attemps to Sheep the mouseover target, else Remove Curse on focus, but only if you hold Shift key, else it casts Frostbolt on your target, if it exists.

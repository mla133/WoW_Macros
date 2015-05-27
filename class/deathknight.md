#All specs
##Death Grip with Motivation!
```
#showtooltip
/cast Death Grip
/script PlaySoundFile("Sound\\Creature\\Ashbringer\\ASH_SPEAK_12.wav")
```
Use: Casts your typical Death Grip, but with an inspirational Lich King saying afterwards.

## Mouse-over Death Grip
```
#showtooltip Death Grip
/cast [target=mouseover, exists] Death Grip; Death Grip
```
Useful to quickly grip targets without having to target them first.

## PL/UB Talent Switching
```
#showtooltip
/cast [talent:1/2] Plague Leech; [talent:1/3] Unholy Blight
```
This allows you to use the same button for Plague Leech and Unholy Blight without having to move the ability from the talents pane to your action bar.

## Presence Shifting
```
#showtooltip
/cast Blood Presence
/cast Unholy Presence
```
This allows you to easily switch between Blood and Unholy presence within one button.

#Omni-Disease
```
#showtooltip
#show
/castsequence reset=target Icy Touch, Plague Strike
```

Use: This casts Icy Touch when you press the button for the first time, then when you press it for the second time it casts Plague Strike. You can (and Should) add Blood Boil to the list if you usually fight more than 1 enemy.
Works in 6.0.0

#Omni-Interrupt
```
#showtooltip
#show
/castsequence [modifier:shift, target=focus][nomod, @target] reset=15 Mind Freeze, strangulate, mind freeze
```

Use: This casts Mind Freeze the first time you press it then Strangulate if you press it again before Mind Freeze comes off cooldown. After that each time you press it, you will attempt to cast mind freeze again until Strangulate becomes available again.
Mod:Shift allows you to hold shift while clicking to use these abilities on focus target.
Replace "strangulate" with "asphyxiate" if you have that talent.
Works in 6.0.0

#Omni-Taunt
```
#showtooltip
show
/castsequence reset=8 Dark Command, Death Grip
```

Use: This casts Dark command if it's not on cooldown, if it is it will cast Death Grip.
Working on 6.0.0

#Frost
##I WIN Macro
```
#showtooltip
#show
/castsequence reset=target Icy Touch, Plague Strike, Blood Strike, Blood Strike, Obliterate, Frost Strike, Howling Blast
```

Use: Just spam it in combat and it will sicken the target, Blood Strike it twice, Obliterate it, burn Runic Power, and then cast Howling Blast.
Works in 4.0.6

Does not always work (Icy Touch and Plague strike generate 24 runic power, not enough for 2 frost strikes costing 40 runic power in total).

##Super Panic Button Macro
```
#showtooltip
#show
/cast Lichborne
/cast [@player] Death Coil
/castsequence Icebound Fortitude, Pillar of Frost, Hungering Cold, Anti-Magic Shell, Raise Dead, Death Pact
```

Use: When you're surrounded by too many enemies.
Note: Spam it while you run and be sure to have some Runic Power. It will heal yourself with the Lichborne + Death Coil on self combo (see below). Then it will cast IBF and PoF to reduce your damage and avoid that stuns or external movements block you, freeze your enemies with Hungering Cold, make you immune to magic with A-M Shell,summon your ghoul and sacrifice it while you run to heal yourself with Death Pact.
Works in 5.4.7

##Self Heal (Lichborne+Death Coil)
```
#showtooltip
#show
/cast Lichborne
/cast [@player] Death Coil
```

Use: This will cast Lichborne, making you undead, and then cast Death Coil on yourself.
Note: Since Death Coil damages the enemy but heals the friendly undead,it will heal you. And since Lichborne isn't on the GCD,there is no need to spam the macro,since LB and DC will be cast together.
Works in 5.0.5, but make sure you have 40+ runic power.
Blood
##General Tanking Macro
```
#showtooltip
/targetnearestenemy
/castsequence reset=combat/10 Dark Command, Heart Strike, Blood Boil, Death Coil, Heart Strike,
```
Use: Tanking rotation (spamable).
Note: I like this macro because it is well balanced and can be mashed throughout a fight, meaning you can concentrate whilst working on other things such as interrupts and ads.
Works in Cataclysm, level 71 DK
##Super Panic Button Mode
```
/cast Death Pact
/cast Bone Shield
/cast Icebound Fortitude
/cast Rune Tap
/cast Vampiric Blood
/cast Anti-Magic Shell
/cast Oralius' Whispering Crystal
/cast Lichborne
/castsequence [@player] Death Coil, Death Coil, Death Coil
```
Use: In a pinch. Heal, defense, defense, defense, bonus health, magic defense, stamina.
None of these are on GCD so they all cast instantly, no castsequence required.
Play around with this to get it working right for you, these are all the defensive abilities I had at the time I made this, you may have more.
Note: Death Pact is a talent and the Crystal is an item. This works if you have them or not, but if you don't have Death Pact the button may be grayed out.
##Lower Level Tanking Macro
```
#showtooltip
/castsequence reset=combat/6 Heart Strike, Death Strike, Heart Strike, Death Strike, Death Coil
```
Use: Lower level takning rotation (spamable). 
Note: Spam this on your enemies, and it allows you to change enemies when ever you need to while still spamming it. You can focus on anything while just pressing one constantly, so tanking requires no skill.
Works with DKs at 60+
Heartstrike has been removed
##Panic Button
```
#showtooltip
/Cast Vampiric Blood
/Cast Rune Tap
/Cast Bone Shield
/cast Anti-Magic Shell
```
Use: Press this in combat and it will increase healing done.
Note: Heals you a bit add a shield and reduce magic damage. Add in Gift of the Naaru or other race specials for healing if you want a bigger boost. Useful for if you have a bad healer or they're out of mana etc. It lasts a couple of seconds, but it's very useful in combat.
Works in Cataclysm, level 71 DK
##Take All Aggro button
```
/castsequence reset=combat/4 Blood Boil, target=random, Dark Command, Death and Decay
```
Use: Very effective for ending all aggro on your teammates.
Note: Press this to unleash Blood Boil to hold argo, randomly target a enemy, Dark Command them, and then release Death and Decay to get the rest of the aggro.
Works in Cataclysm, level 73 DK
#Unholy
##Offensive/Heal Death Coil
```
/cast [Mod:shift,@pet] Death Coil
/cast [nomod] Death Coil
```
Use: If you're specced into unholy you have a permanent ghoul.
Note: This macro basically heals your ghoul with death coil while holding shift otherwise it will just use Death Coil as usual.
Works in 4.1
##Offensive/Heal + Mouseover Death Coil
```
#showtooltip Death Coil
/cast [@mouseover,exists]Death Coil;[@target,exists]Death Coil;[@pet]Death Coil
```
Use: If you're specced into unholy & have your permanent ghoul summoned.
Can also be used in other specs as well.
Note: This macro is usefull if you don't like key modifiers or if you need an alternative to modifiers.
This macro will cast Death Coil at your mouseover target*, at your current selected target if no mouseover target exists, or if you have no targets it will heal your pet.
(*) If you have the Lichborne talent, you can mouse over your own portrait or select yourself to heal yourself rather than deal damage to a hostile target.
(*) If you have the Major Glyph "Death Coil", you can mouse-over or select a friendly target to heal them.
Works in 5.4.7

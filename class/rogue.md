#Rogue Macros
##Stealth Eat Macro
```
#showtooltip
/cast *food here*
/cast Stealth
```
##Gouge or Prem + Cheapshot or Cheap Shot
```
#showtooltip
/cast [stealth] [stance:3] Premeditation;
/cast [nostance] Gouge; [stance:2]Shadow Dance; Cheap Shot
```
This macro takes into consideration your Shadow Dance ability.
If you are non-stealthed. You will Gouge.
If you go either Stealth or Shadow Dance, you will still be able to Cheap Shot.
In stealth, you will be able to Premed+Cheap Shot.
Comes in handy to those of us use to using a particular button for Cheap Shot, and wishing to continue using that button.

##Tricks of the Trade without losing target
```
#showtooltip Tricks of the Trade
/cast [@targettarget] Tricks of the Trade
```

This is a simple macro that will tricks of the trade your tank without losing your target. It casts on whatever your current target is targeting.

##Weapon Targetted Poison Macros

This is a simple one-click macro that applies Instant Poison to your mainhand.
```
#showtooltip 
/use Instant Poison
/use 16
```

This is a simple one-click macro that applies Deadly Poison to your offhand.
```
#showtooltip 
/use Deadly Poison
/use 17
```

##Hunger For Blood Macro
```
#showtooltip
/cast Hunger for Blood
/stopwatch reset
/stopwatch 1:0
/stopwatch play
/in 60 /run PlaySound("LEVELUPSOUND")
/in 60 /stopwatch
```

Activates Hunger for Blood
Initializes a Timer on your screen with a 1 minute countdown
After 1 Minute has passed, plays the "BWONG" as people call it, Level Up Sound
Closes the Timer
* Works as of 3.3.5

Can likely be used for any buff with a short duration, that one might forget to renew mid battle. (Warrior's Shouts, DK's HoW, Warlock's LifeTap Glyphed Spirit Buff)
Only one timer may be up on your screen, to my knowledge.

##All-in-one Opener/CP Generator
```
/cast [stealth,nodead,exists,harm,spec:1] Ambush; [stealth,harm,exists,spec:2] Cheap Shot
/cast [combat] Mutilate; [nocombat,nostealth] [stealth,nocombat,help] [stealth,dead] [noexists] Stealth
```

Ambushes if you have a harmful target that is not dead and you are stealthed and in spec 1 (your PvE spec). Cheap Shots if same conditions but in spec 2 (your PvP spec)
Mutilates if in combat. Stealths if not in combat and not stealthed, Unstealths if stealthed, not in combat, and have a helpful target, or if you are stealthed and your target is dead, or if you have no target.
I found this to work really well with a 5-button mouse. Use Spellbinder to bind the macro to Button 4, then just spam button 4 with your thumb. Frees up several action bar slots.

##All-in-one Finisher
```
#showtooltip [spec:2] Kidney Shot; [nogroup] Eviscerate; Envenom
/castsequence [spec:2] reset=combat/6 Eviscerate, Kidney Shot; [spec:1,nogroup,combat] Eviscerate; [spec:1,group:party,combat] [spec:1,group:raid,combat] Envenom
```

Shows Kidney Shot if in spec 2 (PvP), Evisc in other spec and not grouped, and Envenom if grouped
In spec 2 casts Evisc, then KS, but resets to Evisc after 6 seconds (in case KS is on cd). In spec 1 if not grouped and in combat casts Evisc. In spec 1 if grouped (party or raid) and in combat, casts Envenom
This works really well with a 5-button mouse also. Use Spellbinder to bind the macro to Button 5, then when you need to do your finisher, hit button 5 once, then back to button 4.


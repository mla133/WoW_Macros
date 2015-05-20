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

```
#showtooltip Vanish
/cast [combat] Cloak of Shadows; !Stealth
/cast [nostealth,combat] Vanish
/cast [stealth] Shadow Walk
```
This macro will put you in stealth if not in combat, if in combat and cloak of shadows and vanish are not on cd it will cast both, if only one is up it will cast which ever is up, it will also show you if vanish is up so be aware if your in combat and vanish isnt up you dont want to hit this or you will most likely waste your cos which has a shorter cd then vanish
Hitting the button twice wont pull you out of stealth
This new version will cast your shadow walk when clicked if in stealth, helpful when sneaking up on hunters.

```
#showtooltip Killing Spree
/target [target=target, help] targettarget; party1
/cast [help] Tricks of the Trade; [harm] Killing Spree
```

If your target is a party member, targets their target, otherwise targets the party leader (often tank), allowing you to switch targets between the tank and what you should be DPSing.
Casts Tricks of the Trade if your target is a party member or casts Killing Spree if your target is an enemy.
This macro is useful for helping a tank establish or maintain aggro during a pull. Hit it twice and you'll TotT the tank while Killing Spree-ing everything else, without losing your target.
A line similar to "/use [harm] Sphere of Red Dragon's Blood" may be added to the end of the macro to boost the power of your Killing Spree to maximize effectiveness, as long as the used item or spell doesn't trigger GCD.
Works in 3.1.3, both with and without the "/use" line.

##PvP Opener
This macro allow for high burst damage while keeping the opponent stunned. Works best with [Vigor] and [Filthy Tricks] as they allow for two Ambushes with the reduced energy cost.
```
#showtooltip
/castsequence reset=30 Premeditation, Cheap Shot, Eviscerate(Rank 11), Dismantle, Shadow Dance, Shadowstep, Ambush(Rank 9), Ambush(Rank 9), Kidney Shot(Rank 2)
```
##Backstabber
This macro stuns the target, quickly damages them for around 6000 health at 80, and then opens them for attack.
```
#showtooltip
/castsequence reset=20 Gouge, Shadowstep, Backstab(Rank 11), Hemorrhage(Rank 4), Kidney Shot(Rank 2)
```
##Anti-Caster
Similar to Backstabber, but focuses on interrupting spells and bringing in high damage, very effective against healers.
```
/castsequence reset=20 Gouge, Shadowstep, Kick, Backstab(Rank 11), Hemorrhage(Rank 4), Eviscerate(Rank 11)
```
##Super Prep
Use every ability refreshed by Preparation except Shadowstep. Remove the nocombat condition on Vanish for PvP.

The rather elaborate-looking code simply clears any errors or error sounds (such as "That item isn't ready yet") produced by the trinkets being on cooldown.
```
#showtooltip Sinister Strike
/console Sound_EnableSFX 0
/use Bladefist's Breadth
/cast Sinister Strike
/console Sound_EnableSFX 1
/script UIErrorsFrame:Clear()
```

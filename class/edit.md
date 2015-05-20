

Useful macros for rogues
Last edited on January 1, 2015
by Anonymous
Classese												
Class races		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Quests		Dk	Dr	Hu	Ma	 Mo	Pa	Pr	Ro	Sh	Wl	Wr
Abilities		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Spec		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Talents		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Trainers		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Glyphs		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Builds		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Tactics		Dk	Dr	Hu	Ma	 Mo	Pa	Pr	Ro	Sh	Wl	Wr
Armor sets		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Starting a		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
PvE		Dk	Dr	Hu	Ma	 Mo	Pa	Pr	Ro	Sh	Wl	Wr
PvP		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr
Macros		Dk	Dr	Hu	Ma	Mo	Pa	Pr	Ro	Sh	Wl	Wr

advertisement

Formatting Macros
Note: Commands for some of the older macros have been modified significantly. Where possible, please validate and mark with last working patch or version number.
When editing a macro on the Wiki please:

name it, describe what it does, and use a 'space' before each command for the 'code box'
note the version of WoW that you tested it in
if moving from another page, remove it from the old page
follow this Macro formatting example:
==== Macro Name ====
 /y Hooray, I made a macro!
* Use: This yells, "Hooray, I made a macro!"
* Works in 5.4.2
which creates:
Macro Name

/y Hooray, I made a macro!
Use: This yells, "Hooray, I made a macro!"
Works in 5.4.2
Macrose
Useful macros 
Macro commands 
General guides
Beginner's guide 
FAQs 
Making a macro 
Wiki Formatting 
Category:Macros 
UI Customization 
Class Macros
           
        
General Macros
Shadowmeld > Stealth (Night Elf only)
/cast Shadowmeld
/cast Stealth
This macro will use Shadowmeld and immediately go into Stealth. This makes Shadowmeld to another Vanish.
This works only for Night Elves
Shadowmeld no longer resets threat meters as of 3.2
Only viable in player versus player.

Stealth Eat Macro
#showtooltip
/cast *food here*
/cast Stealth
Eat while Stealthed.
Works in 5.4.2
Stealth Cannabalize Macro (Undead only)
#showtooltip Cannibalize
/cast Cannibalize
/cast Stealth
Cannibalize while Stealthed.
Works in 4.0.3a

Gouge or Prem + Cheapshot or Cheap Shot
#showtooltip
/cast [stealth] [stance:3] Premeditation;
/cast [nostance] Gouge; [stance:2]Shadow Dance; Cheap Shot
This macro takes into consideration your Shadow Dance ability.
If you are non-stealthed. You will Gouge.
If you go either Stealth or Shadow Dance, you will still be able to Cheap Shot.
In stealth, you will be able to Premed+Cheap Shot.
Comes in handy to those of us use to using a particular button for Cheap Shot, and wishing to continue using that button.
If someone knows how to include the Premed to this during Shadow Dance. Please do. Or send me a tell.

Evasion/Combat Readiness Macro
#showtooltip
/castsequence reset=178 Evasion, Combat Readiness
Casts Evasion
If Evasion is on CD, casts Combat Readiness

Offhand weapon switching
 #showtooltip [mod] 0 16; 17
 /equipslot 17 0 16
You might find yourself in a situation where you have two offhand weapons with the same name but different poisons on them and you want to switch between them quickly. Or perhaps you just want to alternate between two offhand weapons with just one hotkey.

Keep your alternate dagger in the sixteenth slot (lower right corner) of your main (rightmost) backpack.
The number 17 refers to your offhand weapon slot.
#showtooltip makes the macro's icon and tooltip display the icon of the equipped weapon, or hold down a modifier key (say Alt) and it will display the icon of the weapon that's ready to be switched in.
Works in 3.2.2

Multipurpose Hemorrhage/Kick/Shiv
#showtooltip Hemorrhage
/console Sound_EnableSFX 0
/use 13
/console Sound_EnableSFX 1
/cast [modifier:alt] Kick
/cast [modifier:shift] Shiv
/cast Hemorrhage
/stopmacro [help] [noexists]
/cancelaura Blessing of Protection
/startattack
/use 13 and /use 14 are your trinket slots. (easier than typing the name of the trinket)
Holding alt will Kick, and holding shift will Shiv.
Additionally, if you are trying to attack a target with Blessing of Protection on you, it will be automatically taken off of you, to let you melee attack.
I'd recommend binding it to your mouses up scrolling.
Other
Macro 1
#showtooltip marked for death 
/castsequence reset=4 Eviscerate, Marked for Death, Eviscerate
Macro 2
#showtooltip Adrenaline Rush 
/cast Shadow Blades 
/cast Adrenaline Rush 
/use Prideful Gladiator's Badge of Conquest 
/use Virmen's Bite 
submitted by 107.204.241.95 on February 25, 2014‎ in wrong place. (not sure if valid)
Cloak of Shadows/Vanish Macros
Gone and now back again

#showtooltip
/cast preparation
/cast Cloak of Shadows
/cast [nostealth,combat] Vanish
This macro works similar to "new and improved steath,cos,vanish" in that it will if in combat cast prep finish your cd on vanish cast cos if not on cd and will cast vanish. Used this macro all the time before the nerf now its back and Im so happy.
Vanish and Cloak of Shadows

#showtooltip [nocombat] Stealth;[mod] Cloak of Shadows;Vanish
/cast [nocombat] !Stealth
/stopmacro [nocombat]
/cast [mod] Cloak of Shadows
/stopmacro [mod]
/cast [button:1] Cloak of Shadows; [button:2] Vanish
/stopmacro [button:2]
/cast [nostealth] Vanish
When not in combat simply enters stealth.
When in combat: Left click will cast Vanish and Cloak of Shadow, Right click to just cast Vanish, and shift+Left click to just cast Cloak of Shadow
Macro last tested patch 4.3.4, June 15th, 2012
New and improved Stealth,Cloak of Shadow, and Vanish

#showtooltip Vanish
/cast [combat] Cloak of Shadows; !Stealth
/cast [nostealth,combat] Vanish
/cast [stealth] Shadow Walk
This macro will put you in stealth if not in combat, if in combat and cloak of shadows and vanish are not on cd it will cast both, if only one is up it will cast which ever is up, it will also show you if vanish is up so be aware if your in combat and vanish isnt up you dont want to hit this or you will most likely waste your cos which has a shorter cd then vanish
Hitting the button twice wont pull you out of stealth
This new version will cast your shadow walk when clicked if in stealth, helpful when sneaking up on hunters.
Cloak of Shadows Vanish

#showicon Vanish
/cast Cloak of Shadows
/cast Vanish
Will Cast CoS first (removes DoTs that would immediately cancel your Stealth if you had only used Vanish), then safely Stealth.
CoS won't remove physical DoTs such as Rend or Gouge, so it's not foolproof or as useful when up against Warriors or other Rogues.

Stealth, Cloak of Shadows and Vanish

#showtooltip
/castsequence [combat] reset=60 Cloak of Shadows, Vanish; Stealth
This macro allow rogues to stealth if no combat other ways you'll able Cloak of Shadows on first click and Vanish on the second click with reset 1 min for Cloak of Shadows.

Tricks of the Trade Macros
One button Tricks of the Trade on Focus macro

This macro performs two functions: Focus setting and actually casting Tricks of the Trade.

#showtooltip Tricks of the Trade
/clearfocus [button:2]
/stopmacro [button:2]
/focus [@focus,noexists][mod:shift] target
/stopmacro [help]
/cast [@focus,help][help] Tricks of the Trade
Usage :

If you have no Focus and you target a friendly (usually a Tank in a party/raid), your friendly target will be set as your Focus target.
If you already have a Focus target and want to change to another friendly target, hold down Shift and press/click macro while targeting the new target.
If you already have a Focus target set and wish to clear it, right click the macro icon.
After you are satisfied with your Focus target, either target nothing or an enemy and pressing/clicking the macro will perform Tricks of the Trade aimed at the Focus target. Never have to switch target in the middle of the boss fight again!
Set Tricks of the Trades Target Macro

/run ToT = UnitName("target")
/run if not InCombatLockdown() then EditMacro('TotT', nil, nil, '#showtooltip\n/cast [target='.. ToT ..'] Tricks of the Trade', nil); print('Tricks of the Trade set to : ' .. ToT); else print('Cannot change TotT now!'); end;
This is a two macro system, One macro to cast Tricks of the Trade and another to set the target of that macro.

The set macro cannot be used in combat since the game will not allow macro editing during combat.
AutoPartyButtons addon adds a single button that automatically puts TotT on the tank.
Step 1: Create a blank macro named TotT
Step 2: Create the following macro named as you please, for this example SeTTotT
Usage :

Target the player you want to set as your Tricks of the Trade recipient and use the set macro (SeTTotT), you will see a chatlog message confirming the macro worked.
Use the TotT macro whenever you want to use Tricks of the Trade.
Works in 3.2.2

Tricks of the Trade without losing target

#showtooltip Tricks of the Trade
/cast [@targettarget] Tricks of the Trade
This is a simple macro that will tricks of the trade your tank without losing your target. It casts on whatever your current target is targeting.

#showtooltip Tricks of the Trade
/cast [help] [@targettarget] Tricks of the Trade
Another useful macro, an extension of the first example, is to be able to preemptively throw tricks on a target if you wish, or to use it as the macro is intended, and toss it on the mob or boss's target.
This macro dictates that if your target is a friendly target, it will cast Tricks; if not, it will cast it on your target's target. Note that it won't work if you're trying to pop it because a mob is targeting you, of course.

#showtooltip Tricks of the Trade
/cast [@focus] Tricks of the Trade
This is another macro that is useful for Trading tricks (make sure the rogue that you're trading with is set as your Focus Target for this macro)
Poison Macros
One Macro, 3 Different Poisons

/use [button:1] POISONNAMEHERE; [button:2] POISONNAMEHERE; [button:3] POISONNAMEHERE
/use [button:1] 16; [button:2] 17; [button:3] 18
/click StaticPopup1Button1
Applies POISONNAMEHERE to your MH if you left click on the macro
Applies POISONNAMEHERE to your OH if you right click on the macro
Applies POISONNAMEHERE to your TW (Throw Weapon) if you click with the scroll button on the macro
This works in Patch 4.2
If you have any questions about this macro send me a mail
Credit: Saluthia (Rogue) EU Realm Kul' Tiras

Rzdrsfo at Kul Tiras Eu, sorry for not being able to help you with this macro


Here is the Macro I'm using today (20 February 2012) make sure you doesn't accidently remove any of the ; in the macro and that the poisons name starts with a big letter, for example (D)eadly (P)oison

/use [button:1] Instant Poison; [button:2] Deadly Poison; [button:3] Deadly Poison
/use [button:1] 16; [button:2] 17; [button:3] 18
/click StaticPopup1Button1
One Button Poisons

#showtooltip
/use POISONNAMEHERE
/use [button:1] 16 
/use [button:2] 17
/click StaticPopup1Button1
Applies POISONNAMEHERE to your MH if you left click
Applies POISONNAMEHERE to your OH if you right click
The last line will click the "OK" button when it asks you if you want to replace the poison that may already be on the weapon.
I set one up for each of my poisons and keep the macros handy, especially for PvP.
Works in 4.1
One Button Different Poisons

#showtooltip
/use [button:1] POISON1NAMEHERE; POISON2NAMEHERE
/use [button:1] 16; 17
/click StaticPopup1Button1
This variation of One Button Poisons allows you to use two different types of poison instead of one
Applies POISON1NAMEHERE to your MH if you left click
Applies POISON2NAMEHERE to your OH if you right click or activate the macro through any other means than a left click.
The last line will click the "OK" button when it asks you if you want to replace the poison that may already be on the weapon.
Working as of 4.2
One Button Different Poisons - Advanced

#showtooltip
/use [mod] POISON1NAMEHERE; POISON2NAMEHERE
/use [button:1] 16; 17
/click StaticPopup1Button1
This variation of the above variation of One Button Poisons allows you to choose between two potions separately from which weapon to apply it to
To clarify, with poisons A and B, and weapons 1 and 2, this allows you to choose between poison-weapon combinations A1, A2, B1, and B2, as opposed to just A1 and B2
Applies POISON1NAMEHERE if you press with a modifier, or POISON2NAMEHERE otherwise.
Applies the poison to your main hand if you left click, or your off hand otherwise.
The possible poisons can be further expanded via [mod:specificmod], for a total of 4 on one macro
The last line will click the "OK" button when it asks you if you want to replace the poison that may already be on the weapon. You may remove this if preferred.
Please verify; I think I have the theory correct, but have no rogue of high enough level to test it with.
Credit: Souldude (aka Sneakfellow) of Thrall (US)

One Button All Five Poisons

One Button All Five Poisons applied to MH, OH, or thrown weapon slots macro
#showtooltip
/use [mod:ctrl, mod:alt] Mind-Numbing Poison;[mod:shift] Instant Poison; [mod:ctrl] Crippling Poison; [mod:alt] Wound Poison; Deadly Poison
/use [button:1] 16; [button:2] 17; [button:4] 18
/click StaticPopup1Button1
This is a further variation of the above One Button Poison macro that allows you to choose between five poisons and your MH, OH, or thrown weapon slots
#showtooltip will switch icon to correspond with poison being applied
Remove "[button:4] 18" from the third line if you do not have a mouse with back and forward buttons. You can still left click to apply poisons to your MH or right click to apply to OH
Applies Mind-Numbing Poison to MH if you hold control AND alt and left click, OH if you hold control AND alt and right click, or thrown if you hold control AND alt and click Mouse4
Applies Instant Poison to MH if you hold shift and left click, OH if you hold shift and right click, or thrown if you hold shift and click Mouse4
Applies Crippling Poison to MH if you hold control and left click, OH if you hold control and right click; or thrown if you hold control and click Mouse4
Applies Wound Poison to MH if you hold alt and left click, OH if you hold alt and right click, or thrown if you hold alt and click Mouse4
Applies Deadly Poison to MH if you simply left click, OH if you simply right click, or thrown if you simply click Mouse4
The last line will click the "OK" button when it asks you if you want to replace the poison that may already be on the weapon. You may remove this if preferred.
Works with 4.0.3a
--M0kin (talk) 10:19, April 16, 2011 (UTC)

Weapon Targetted Poison Macros

This is a simple one-click macro that applies Instant Poison to your mainhand.

#showtooltip 
/use Instant Poison
/use 16

This is a simple one-click macro that applies Deadly Poison to your offhand.

#showtooltip 
/use Deadly Poison
/use 17
Assassination Macros
Cold Blood & Eviscerate/Ambush w/o Global CD
#showtooltip [stealth] Ambush; Eviscerate
/cast Cold Blood
/cast [stealth] Ambush; Eviscerate
Activates Cold Blood just before using Eviscerate or Ambush (if stealthed)
Cold Blood does not trigger Global CD, so both spells cast at the same time.
by Shxdxws - Vek'nilash
Works in 4.0.1
Hunger For Blood Macro
#showtooltip
/cast Hunger for Blood
/stopwatch reset
/stopwatch 1:0
/stopwatch play
/in 60 /run PlaySound("LEVELUPSOUND")
/in 60 /stopwatch
Activates Hunger for Blood
Initializes a Timer on your screen with a 1 minute countdown
After 1 Minute has passed, plays the "BWONG" as people call it, Level Up Sound
Closes the Timer
Works as of 3.3.5
Can likely be used for any buff with a short duration, that one might forget to renew mid battle. (Warrior's Shouts, DK's HoW, Warlock's LifeTap Glyphed Spirit Buff)
Only one timer may be up on your screen, to my knowledge.
All-in-one Opener/CP Generator
/cast [stealth,nodead,exists,harm,spec:1] Ambush; [stealth,harm,exists,spec:2] Cheap Shot
/cast [combat] Mutilate; [nocombat,nostealth] [stealth,nocombat,help] [stealth,dead] [noexists] Stealth
Ambushes if you have a harmful target that is not dead and you are stealthed and in spec 1 (your PvE spec). Cheap Shots if same conditions but in spec 2 (your PvP spec)
Mutilates if in combat. Stealths if not in combat and not stealthed, Unstealths if stealthed, not in combat, and have a helpful target, or if you are stealthed and your target is dead, or if you have no target.
I found this to work really well with a 5-button mouse. Use Spellbinder to bind the macro to Button 4, then just spam button 4 with your thumb. Frees up several action bar slots.
All-in-one Finisher
#showtooltip [spec:2] Kidney Shot; [nogroup] Eviscerate; Envenom
/castsequence [spec:2] reset=combat/6 Eviscerate, Kidney Shot; [spec:1,nogroup,combat] Eviscerate; [spec:1,group:party,combat] [spec:1,group:raid,combat] Envenom
Shows Kidney Shot if in spec 2 (PvP), Evisc in other spec and not grouped, and Envenom if grouped
In spec 2 casts Evisc, then KS, but resets to Evisc after 6 seconds (in case KS is on cd). In spec 1 if not grouped and in combat casts Evisc. In spec 1 if grouped (party or raid) and in combat, casts Envenom
This works really well with a 5-button mouse also. Use Spellbinder to bind the macro to Button 5, then when you need to do your finisher, hit button 5 once, then back to button 4.
Combat Macros
TotT + Killing Spree
#showtooltip Killing Spree
/target [target=target, help] targettarget; party1
/cast [help] Tricks of the Trade; [harm] Killing Spree
If your target is a party member, targets their target, otherwise targets the party leader (often tank), allowing you to switch targets between the tank and what you should be DPSing.
Casts Tricks of the Trade if your target is a party member or casts Killing Spree if your target is an enemy.
This macro is useful for helping a tank establish or maintain aggro during a pull. Hit it twice and you'll TotT the tank while Killing Spree-ing everything else, without losing your target.
A line similar to "/use [harm] Sphere of Red Dragon's Blood" may be added to the end of the macro to boost the power of your Killing Spree to maximize effectiveness, as long as the used item or spell doesn't trigger GCD.
Works in 3.1.3, both with and without the "/use" line.
Garrote in Stealth, or Sinister Strike Otherwise
#showtooltip
/cast [stealth] Garrote
/castrandom [nostealth] Sinister Strike, Riposte
Ambush or Garrote
/cast [equipped:Daggers] Ambush; Garrote
This lets you use Ambush if you have a dagger equipped otherwise will default to Garrote. You can change it to Garrote with a certin kind of weapon by adding [equipped:Mace] after Ambush like so:
/cast [equipped:Daggers] Ambush;[equipped:Mace] Garrote
By Sqeeks
Rupture or Slice and Dice in one button
#showtooltip [modifier:shift] Rupture; Slice and Dice
/cast [modifier:shift] Rupture; Slice and Dice
Activates both finishing moves in one button using the modifier shift to choose which one.
The default image should be question mark so it will show the tool tips for the finisher you are about to use.
Will not change and stay you must hold down the shift key or any modifier key you chose to use.
Slice and Dice will always be default without holding shift down (unless you replace it with another finisher).
Great for PvP or a raid when fighting a boss to keep doing DPS without the burst damage.
Made by Sqeeks
Eviscerate or Envenom
#showtooltip [modifier:shift] Eviscerate; Envenom
/cast [modifier:shift] Eviscerate; Envenom
This macro is just like the one above it except it is more ideal for solo killing or doing burst damage against a boss if he/she is close to death.
Also good for PvP for burst scare damage or fast kills of clothies.
Envenom is default to show and as mentioned above holding shift down will allow you to use Eviscerate.
If you use the question mark icon then the image will match the finisher you aim to use so there is no confusion.
Having both macros will allow you to use fewer action slots for other items or skills and use the one you want at any given time.
You can add a third or even fourth modifier to include more then just the two written above.
#showtooltip [modifier:shift] Eviscerate;[modifier:ctrl] Envenom; Expose Armor
/cast [modifier:shift] Eviscerate;[modifier:ctrl] Envenom; Expose Armor
With this macro if you look at the icon using the question mark the icon and tooltips for Expose Armor will be default, pressing and holding shift will allow use of Eviscerate and see the tooltips and finally pressing and holding the ctrl button will allow you to use Envenom and see the tooltips.
Made by Sqeeks
Stealth and Ambush with One Handed Weapons
#showtooltip Stealth
/cast !Stealth
/equipslot 16 *name of main hand dagger*
/equipslot 17 *name of off hand dagger*
Use: Goes into Stealth and switches your weapons to daggers.
The "!Stealth" means you can mash it's keybind and not worry about toggling off Stealth.
Note: You need to switch your off hand weapon first only if you have a "Main Hand" weapon in your main hand. If not, the macro will attempt to switch your weapons, and fail because "Main hand" can only be equipped in your main hand. (Only affected if your main hand dagger is currently in your off hand)
Works in 3.3.2
#showtooltip Ambush
/cast Ambush
/equipslot 16 *name of Main Hand weapon*
/equipslot 17 *name of off Hand weapon*
Use: Uses Ambush, then switches you back to your Combat Weapons.
Note: If you fail to cast Ambush (not in right position, tank pulling mob out of range as you ambush) the macro will still switch your weapons, and you must reapply your Stealth macro.
Works in 3.3.2
Blade Flurry / Killing Spree
#showtooltip [mod:shift] Blade Flurry; Killing Spree
/castsequence reset=30 Blade Flurry, Killing Spree
The first time you hit the macro, it activates Blade Flurry (I suggest you wait until S&D is already up), the next time (within 30 secs.) you *hit it, it activates Killing Spree. Since both abilities have 2m CD, you can go by the CD of Killing Spree, which is the default tooltip shown; however, if you want to see the Blade Flurry CD, just press the Shift key.
This macro is useful if your group pulls a large group all at once and you need to do some mega DPS, FAST!
by Shxdxws - Vek'nilash
Works in 4.0.1
Feint & Evasion w/o Global CD
#showtooltip Evasion
/cast Feint
/cast Evasion
Use: Triggers Feint and Evasion simultaneously, since Feint doesn't trigger the global cooldown.
Useful when you start to pull aggro from the tank, as most Rogues do at some point.
by Shxdxws - Vek'nilash
Works in 4.0.3a
Subtlety Macros
PvP Opener
This macro allow for high burst damage while keeping the opponent stunned. Works best with [Vigor] and [Filthy Tricks] as they allow for two Ambushes with the reduced energy cost.

#showtooltip
/castsequence reset=30 Premeditation, Cheap Shot, Eviscerate(Rank 11), Dismantle, Shadow Dance, Shadowstep, Ambush(Rank 9), Ambush(Rank 9), Kidney Shot(Rank 2)
Backstabber
This macro stuns the target, quickly damages them for around 6000 health at 80, and then opens them for attack.

#showtooltip
/castsequence reset=20 Gouge, Shadowstep, Backstab(Rank 11), Hemorrhage(Rank 4), Kidney Shot(Rank 2)
Anti-Caster
Similar to Backstabber, but focuses on interrupting spells and bringing in high damage, very effective against healers.

/castsequence reset=20 Gouge, Shadowstep, Kick, Backstab(Rank 11), Hemorrhage(Rank 4), Eviscerate(Rank 11)
Super Prep
Use every ability refreshed by Preparation except Shadowstep. Remove the nocombat condition on Vanish for PvP.

#showtooltip Preparation
/cast [nostealth] Evasion
/cast [nocombat] Vanish
/cast Cold Blood
/cast Sprint
/cast Preparation
Swap Dagger + Ambush
This macro can be used in pvp in general and is useful if you want to stay with your fast main and offhand :

/equip Your1hDagger   
/cast ambush                    
/equip YourOldMainHand
Old Macros
The macros below this line have not been validated to work in 3.1. They should be tested and moved to the appropriate section above.

Vanish and Shadowstep and Cloak of Shadows
If you hold ctrl it will Vanish + Shadowstep the target. If you hold alt you can quickly Cloak of Shadows + Vanish.

/cast [modifier:ctrl] Shadowstep
/cast [modifier:alt] Cloak of Shadows
/cast vanish
/stopattack
Cancel Blessing of Protection with Combo point attack.
Cancels Blessing of Protection automatically when you are trying to cast Hemorrhage on the enemy. Possible to be used with any other Combo point attack, like Mutilate, Backstab, Sinister Strike.

/cast Hemorrhage
/stopmacro [help] [noexists]
/cancelaura Blessing of Protection
Unified Mount Macro
One button, one press to: Mount an appropriate mount if not mounted. Dismount and drop into stealth if you are not flying, but do it anyway if you have an enemy target. Lacking a conditional test for how far above the ground you are, this seems the best balance of combat function vs. going splat from an accidental, high altitude key press.

/use [nomounted, flyable] Swift Purple Windrider; [nomounted, noflyable] Horn of the Frostwolf Howler
/cast [mounted, nocombat] Stealth
/dismount [mounted, noflying]
/dismount [exists, harm]
/cast [nomounted] Stealth
Trinket activation
Many favorite level 60+ rogue trinkets can be used to provide 10-20 second buffs (attack power, crit rating, or haste) which are on different 2 min cooldowns. If you have 2 of these equipped, you can activate whichever is out of cooldown with a macro like this. If the first listed item is on cooldown, the macro will use the second.

/use Bladefist's Breadth
/use Ancient Draenei War Talisman
A simpler way, as per Useful_macros#Use_either_Trinket, is to use:

/use 13
/use 14
The following macro will automatically activate your trinkets for you. You can chain as many items with uses - and which don't trigger the global cooldown - into the /castrandom as you have. It's not a good idea to add abilities that cost energy (like Adrenaline Rush) or which might break crowd control (like Blade Flurry).

The rather elaborate-looking code simply clears any errors or error sounds (such as "That item isn't ready yet") produced by the trinkets being on cooldown.

#showtooltip Sinister Strike
/console Sound_EnableSFX 0
/use Bladefist's Breadth
/cast Sinister Strike
/console Sound_EnableSFX 1
/script UIErrorsFrame:Clear()
Sinister Strike => Riposte version A
A very primitive way to bypass the restrictions. You have to mash this non-stop and it works fine.

/castrandom Sinister Strike, Riposte
Sinister Strike => Riposte version B
This will cast Sinister Strike on the first press, and on the next press, Riposte. The macro resets in 1 second. The problem with this macro is that you have to Sinister Strike before you can Riposte.

/castsequence reset=1 Sinister Strike, Riposte
Sinister Strike => Riposte version C
This will cast Sinister Strike on a normal click, and when Riposte becomes available, right-click to use Riposte. I use this because the Sinister Strike + Riposte listed above seems buggy, and sometimes wont reset, so you're stuck trying to do Riposte over and over, when it's not available.

/cast [button:1] Sinister Strike; [button:2] Riposte
Sinister Strike => Riposte version D
This works like a lot of trinket macros I have used, you get the "not ready" message a lot, but it casts Riposte every time it is available, otherwise Sinister Strike.

/cast Riposte
/cast Sinister Strike
Note: As of at least 2.0, this macro no longer works. See here.

Dagger Switch to use Backstab after Pick Pocketing the enemy
This switches to your dagger, casts Pick Pocket if you are stealthed, Backstab, then switches back to your original setup

/equipslot 16 [Dagger]
/cast [stealth] Pick Pocket
/cast Backstab
/equipslot 16 [Original Weapon]
Note that this macro requires that you have autoloot enabled, or an addon such as AutoLootPocket [1]

Dagger Switch to do a Mutilate, then back to normal weapons
This is to switch to your highest DPS, slowest dagger to Mutilate, then back to your standard sword.

/equipslot17 [insert lowest DPS dagger for MH]
/equipslot18 [insert highest DPS dagger for OH]
/cast Mutilate
/equipslot17 [normal MH wep]
/equipslot [normal OH wep]
Note: Only thing with this is that switch weapons invokes the Global Cooldown. And it resets the swing timer which might not make this even useful.

Mashable Stealth / Unstealth
This will only turn Stealth on.

/cast !Stealth
To leave Stealth if you're in it:

/cast [stance] Stealth
Backstab if mainhanding a dagger, Sinister Strike otherwise
This will Backstab if you have a dagger in your mainhand, or Sinister Strike if you have a fist weapon. This is useful for situations such as the Flame Wreath in the Shade of Aran encounter where you have to spend prolonged periods in front of a mob unable to move behind it to Backstab. Just click your fist weapon on your bar and then Sinister Strike a few times while you wait so you don't waste energy.

The reason you have to do it this way is you likely have a dagger in your offhand, so the macro will just keep trying to Backstab if you say [equipped:Daggers] [noequipped:Daggers] instead

Note: You'll have to change "Fist Weapon" to "Sword" or "Mace" as appropriate if you don't have a fist weapon

/cast [noequipped:Fist Weapon] Backstab; /cast [equipped:Fist Weapon] Sinister Strike
(macro by Raymond from Nazjatar US) Or you can

/cast [equipped:Dagger]Backstab; /cast Sinister Strike
Making it only backstab when you have daggers for what ever else it sinister strikes

Alucian

Ambush if Stealthed, otherwise Backstab
This will cast Ambush if the player is stealthed, Backstab if not.

/cast [stealth] Ambush; Backstab
- OR -

/cast [nostealth] Backstab; Ambush
Note: The action bar changes while Stealth is activated. Therefore Ambush is only used on Stealth's action bar. When Stealth is deactivated, the action bar will swap back to the standard action bar. Backstab should only be on the standard action bar and Ambush should only be used on the Stealth action bar.

Ambush if Dagger, otherwise Cheapshot
This will Ambush your target if you have a dagger equipped, and Cheap S
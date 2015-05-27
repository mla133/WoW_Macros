#Macro Guide
##Simplest `/cast` macro
```
#showtooltip
/cast <spellname>
```
##Conditional `/cast` macros
```
#showtooltip
/command [conditionals] <item> or <spell>
```
There are different macro syntax methods as follows:
```
#showtooltip
/cast [condition, AND condition] <spell>

/cast [condition] [OR condition] <spell>
```
Stringing multiple conditions together like this:
```
#showtooltip
/cast [@focus,exists] <spell>; [@player] <spell>
```
This macro will first look to cast `<spell>` at your focus, if that fails, then it casts it on yourself.

##`#showtooltip` examples
Proper syntax:
```
#showtooltip [conditionals] thingtoshow; [conditionals] thingtoshow
```
Spell Example:
```
#showtooltip Flash of Light
```
Item Example:
```
#showtooltip Balanced Heartseeker
```
Item in backpack in a specific location of your bag (bagid 0):
```
#showtooltip 0 4
```
Example with conditionals:
```
#showtooltip [nomod] Flash of Light; [mod:shift] Balanced Heartseeker
```
##`/castsequence` macros
Syntax:
```
/castsequence [conditionals] resetparameter <spell>, <spell>, <spell>
```
A cast sequence macro always loops until it hits the `resetparameter`.  It can be a number of seconds since the last time you clicked the macro, switch targets, leave combat, or press a modifier.
```
/castsequence reset=10 spell, spell, spell
```
You can also have multiple resets like this:
```
/castsequenc reset=10/target/combat spell, spell, spell
```
##Mouseover macros
```
/cast [@mouseover] <spell>
```
Here is one with more conditionals:
```
/cast [@mouseover, exists, harm] <spell>; [@target, exists] <spell>
```
This one will cast the spell at your mouseover target IF it exists and is a harmful target.  If not, then it proceeds to the next set of conditionals and spells.
Please note that you need to include the "exists" or "harm" conditionals if you want the spell to return FALSE and move on to the next step.

##Macro Conditionals
| Macro Conditional 	| Syntax | Notes |
| -----------------	| ------ | ----- |
| target		| [target=unittype] or [@target] | can also use @target or @name |	   	 
| harm			| [harm] | |	
| help			| [help] | |	
| exists		| [exists] | also can check if you have a focus with @focus, always use with @mouseover |
| dead			| [dead] | |
| party			| [party] | TRUE if you are in a party |
| raid			| [raid] | TRUE if you are in a raid |
| group			| [group:type] | TRUE without type (raid/party) |
| stance		| [stance:#] or [form:#] | also works with forms for druids |
| stealth		| [stealth] | |
| nostealth		| [nostealth] | |
| combat		| [combat] | |
| channeling		| [channeling:spell] | can be used without a spell to determine if you are channeling at all |
| modifier		| [modifier:type] or [mod] | Valid modifiers: shift,ctrl, alt, use just [mod] for any modifier press |
| button		| [button:#] or [btn:#] | Keybind is same as left mouse click (1).  Returns TRUE if button was used to activate macro |
| equipped		| [equipped:item_name] | TRUE if item_name is equipped.  Can also use shield, two-hand, one-hand |
| pet			| [pet:type/name] | |
| mounted		| [mounted] | |
| flying		| [flying] | Returns TRUE if on a flying mount |
| swimming		| [swimming] | Returns TRUE if swimming |
| flyable		| [flyable] | Returns TRUE if in a location a flying mount can be used |
| indoors		| [indoors] | |
| outdoors		| [outdoors] | |
| nomod			| [nomod] | Returns TRUE if no modifier (shift,alt,ctrl) is pressed |
| spec	 		| [spec:1] | Returns TRUE depending on what spec you are using.  1 & 2 for your different specs |
| worn			| [worn:item] | same as equipped |
| nodead		| [nodead] | Returns TRUE is target is alive |
| actionbar		| [actionbar:1] | Returns TRUE if that specific actionbar is shown (action bar pages) |

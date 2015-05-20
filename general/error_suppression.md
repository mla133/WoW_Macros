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


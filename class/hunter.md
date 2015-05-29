## Hunter Macros (Multi-boxing)

```
#showtooltip Hunter's Mark
/petattack [target=focus,harm,nodead]
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Hunter's Mark
```


```
#showtooltip Hunter's Mark
/petattack [target=focus,harm,nodead][target=focustarget,harm,nodead]
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Hunter's Mark
/script SetRaidTarget( "target" , 8 )
```


```
#showtooltip steady shot
/target [target=focustarget,harm,nodead][target=party1target,harm,nodead]
/stopmacro [noharm][dead]
/cast !Auto Shot
/cast Steady Shot
/cast [target=pettarget,exists] Kill Command
```


```
#showtooltip [target=focus,exists,harm] Scorpid Sting; Arcane Shot
/cast [target=focus,harm,nodead] Scorpid Sting
/cast [target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Arcane Shot
```


```
#showtooltip Multi-Shot
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Multi-Shot
```


```
#showtooltip Concussive Shot
/castsequence [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] reset=12 Concussive Shot,,,,
```


```
#showtooltip Raptor Strike
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Raptor Strike
```


```
#showtooltip Mongoose Bite
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Mongoose Bite
```


```
#showtooltip Serpent Sting
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Serpent Sting
```


```
#showtooltip Wing Clip
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Wing Clip
```


```
#showtooltip Disengage
/cast [target=focus,harm,nodead][target=focustarget,harm,nodead][target=party1target,harm,nodead][target=target,harm,nodead] Disengage
```


```
#showtooltip [pet,dead] Revive Pet; [nopet] Call Pet; [pet] Mend Pet
/cast [pet,dead] Revive Pet; [nopet] Call Pet; [pet] Mend Pet
```


```
#showtooltip Call Pet
/petpassive
/petfollow
```


```
/use 14
/use 15
/cast blood fury
/cast bestial wrath
```

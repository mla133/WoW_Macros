# Shaman Macros (Multi-Boxing)
```
#showtooltip lesser healing wave
/cast [target=focustargettarget,nodead] [target=focustarget,nodead] [target=focus,nodead] [target=self] lesser healing wave
```

```
#showtooltip lightning bolt
/cast [target=focustarget,nodead,harm] [target=target,nodead,harm] lightning bolt; [target=focustarget,nodead,help] [target=target,nodead,help] lesser healing wave
```


```
#showtooltip chain lightning
/cast [target=focustarget] chain lightning
```


```
#showtooltip chain heal
/cast [target=ftf,nodead] [target=rtf,nodead] [target=mtf,nodead] [target=btf,nodead] [target=ltf,nodead] chain heal
```


```
#showtooltip frost shock
/cast [target=focustarget,nodead,harm] [target=target,nodead,harm] frost shock
```


```
#showtooltip flame shock
/cast [target=focustarget,nodead,harm] [target=target,nodead,harm] flame shock
```


```
#showtooltip earth shock
/castsequence [target=focustarget,nodead,harm] [target=target,nodead,harm] reset=5 earth shock,,,,
```


```
/use 14
/use 15
/cast blood fury
/cast elemental mastery
```


```
#showtooltip healing wave
/cast [target=focustargettarget,nodead] [target=focustarget,nodead] [target=focus,nodead] [target=self] healing wave
```


```
#showtooltip bloodlust
/castsequence reset=600 bloodlust
```


```
#showtooltip astral recall
/castsequence reset=900 astral recall,hearthstone
```


```
#showtooltip earth elemental totem
/castsequence reset=1200 earth elemental totem,,,,
```


```
#showtooltip fire elemental totem
/castsequence reset=1200 fire elemental totem,,,,
```


```
#showtooltip tremor totem
/castsequence reset=15 tremor totem,,,,
```


```
#showtooltip lightning bolt
/cast [target=focustarget,nodead,harm] [target=target,nodead,harm] lightning bolt
```


```
#showtooltip earth shock
/stopcasting
/cast [target=focustarget,nodead,harm] [target=target,nodead,harm] earth shock
```


```
#showtooltip earthbind totem
/castsequence reset=15 earthbind totem,,,,
```


```
#showtooltip purge
/cast [target=focustarget] purge
```

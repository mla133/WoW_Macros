# Some handy boxing macros

##Invite All (for leveling)
```
/i alt1
/i alt2
/i alt3
/i alt4
/ffa
```


##Invite All (for boosting)
```
/i alt1
/i alt2
/i alt3
/i alt4
/run SetLootMethod(“Master”,”MainChar”)
/run SetLootThreshold(3)
/run SetOptOutOfLoot(1)
```

The above code will set loot threshold to rare, your main as the master looter, and to opt out of random loot. Only corpses with rare loot will sparkle now! If you would like uncommon simply set loot threshold to 2.

## Set Focus
(will only work when in the same party/raid)
```
/focus main
/follow main
```

(otherwise use this)

```
/target main
/focus
/follow
```

## Accept All
```
/script AcceptGroup();
/script AcceptQuest();
/script AcceptTrade();
/script RetrieveCorpse();
/script RepopMe();
/script ConfirmAcceptQuest();
/script StaticPopup_Hide(“PARTY_INVITE”);
/script SelectGossipOption(1)
```

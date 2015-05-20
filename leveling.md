#Training and Leveling
##Tanks: Check unhittability, avoidance, and dist to hard-defcap
```
/run local b,d,p,r,a=GetBlockChance(),GetDodgeChance(),GetParryChance(),GetCombatRating(CR_DEFENSE_SKILL) a=1/(.0625+.956/(r/122.9625)) ChatFrame1:AddMessage(format("Unhittable: %.2f%%  Avoidance: %.2f%%  Defense %+.0f rating",b+d+p+5+a,d+p+5+a,r-689))
```

* Use Check unhittability and avoidance (+ how far away hard-defcap).

#Trading, Bags and Money
##Print Money and Currencies to Chat Frame
```
/script local cu = GetMoney(); print(GetCoinTextureString(cu,"12"))
/stopmacro [btn:1]
/script yy = GetNumWatchedTokens(); for xx = 1, yy,1 do aa, bb, cc, dd, ee = GetBackpackCurrencyInfo(xx); print(bb, aa) end
```

* Use: Left click to display your total money in the chat window.
* Click any other way to display your money and all your watched currencies.
* Works in 3.3.2

##Sell all grey items
```
/run local c,i,n,v=0;for b=0,4 do for s=1,GetContainerNumSlots(b)do i={GetContainerItemInfo(b,s)}n=i[7]if n and string.find(n,"9d9d9d")then v={GetItemInfo(n)}q=i[2]c=c+v[11]*q;UseContainerItem(b,s)print(n,q)end;end;end;print(GetCoinText(c))
```

* Use: sells all grey items, shows what was sold and how much money was made from selling
* Works in 4.0.3a

##Destroy all grey items
```
/run local i,n=0;for b=0,4 do for s=1,GetContainerNumSlots(b) do ClearCursor();i={GetContainerItemInfo(b,s)};n=i[7];if n and string.find(n,"9d9d9d") then PickupContainerItem(b,s); DeleteCursorItem() end end end
```

* Use: destroy all grey items without confirmation
* Works in 4.0.6

##Item Link
```
/run local s={"10000"} for i=1,#s do DEFAULT_CHAT_FRAME:AddMessage("\124c00ffffff\Item Link: \124c00FF0033\124Hitem:"..s[i]..":0:0:0:0:0:0:0:0\124h[ID: "..s[i].."]\124h\124r\124c00ffffff - Click ID for item info.")end
```

* Use: Displays an item link in the default chat frame.
Replace "10000" with the desired item ID #.
* Works in 3.3.2

##Spell Link
```
/run local s={"10000"} for i=1,#s do DEFAULT_CHAT_FRAME:AddMessage("\124c00ffffff\Spell Link: \124c00ff0033\[ID: "..s[i].."] \124c00ffffff\- "..GetSpellLink(""..s[i])..".")end
```

* Use: Displays a spell link in the default chat frame.
Replace "10000" with the desired spell ID #.
* Works in 3.3.2


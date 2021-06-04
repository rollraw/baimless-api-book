---
description: Functions to work with cheat configuration variables
---

# config

> Description: functions to work with cheat configuration variables

:construction: _API of this file is not finished yet and could be changed in any time_

## Enumerations

Description: variables indexes to be used in \[Set\\(\\)\]\(\#set\)/\[Get\\(\\)\]\(\#get\) functions, passed as `nVariableIndex` argument

ℹ **Note:** for consistent naming and ease of understanding, all variable names begin with the prefix of their data types:

* prefix `b` - `bool` type
* prefix `i` - `int` type
* prefix `n` - `bitflag (int)` type
* prefix `key` - `int` type
* prefix `fl` - `float` type
* prefix `col` - `Color` type
* prefix `sz` - `string` type
* prefix `vec` - `vector` type, you can find out the type of values \(such as `bool`/`int`/`float`\) in the vector using the menu

| Indentifiers |
| :---: |
| bRage |
| bRageAutoFire |
| bRageScanFakeDuckFull |
| iRageAutoZeusDelay |
| iRageHeadScale |
| iRageBodyScale |
| keyRageDoubleTap |
| iRageDoubleTapType |
| iRageDoubleTapTolerance |
| iRageDoubleTapTrigger |
| bRageDoubleTapInstant |
| bRageDoubleTapPreferBody |
| keyRageHideShots |
| keyRageForceOverrideResolver |
| keyRageForceBackShoot |
| nRageLogicLocal |
| iRageLogicLocalTrigger |
| iRageLogicLocalLowHealth |
| nRageLogicEnemy |
| iRageLogicEnemyTrigger |
| iRageLogicEnemyLowHealth |
| bRageFakeLag |
| iRageFakeLagType |
| iRageFakeLagTicks |
| iRageFakeLagJitter |
| nRageFakeLagTriggers |
| iRageFakeLagTriggersTicks |
| bRageBreakLC |
| bRageHoldFireAnimation |
| keyRageAntiAimForceLowDelta |

## Functions

 \#\#\# Get :warning: \*\*Warning:\*\* if you want to get single value and not all values table of vector, use \[GetVector\\(\\)\]\(\#get-vector\) function instead Parameters: \| Name \| Type \| Description \| \| :------------- \| :------------ \| :---------------------------------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of variable to get value of \| Returns: \| Type \| Description \| \| :--- \| :---------- \| \| any \| automatic variable value, for a checkbox/toggle, returns boolean. for a sliderint/combo/multicombo, returns an integer. for a sliderfloat, returns a float. for a hotkey, returns true if the hotkey is active. for a color picker, returns \[Color\]\(../datatypes/color.md\). for a vector \(also any type of supported e.g. \`bool\`, \`int\`, \`float\`\), returns table \| Code: \`\`\`lua local bValue = Config.Get\(Vars.bRageAutoFire\) local colValue = Config.Get\(Vars.colEspMainBoxEnemies\) \`\`\` \# \#\#\# GetVector Parameters: \| Name \| Type \| Description \| \| :------------- \| :---- \| :------------------------------------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of vector variable \| \| nVectorIndex \| uint32 \| index of vector entry to get value of \| Returns: \| Type \| Description \| \| :--- \| :--------------------------------------------------------------- \| \| any \| automatic variable value of given vector at given \`nVectorIndex\` \| Code: \`\`\`lua local bValue = Config.GetVector\(Vars.vecRagePreferSafePoints, 1\) -- prefer safe points checkbox state in deagle/relolver \(revolver icon\) ragebot tab local iValue = Config.GetVectorInt\(Vars.vecRageHitChance, 3\) -- hitchance value in snipers \(scar-20 icon\) ragebot tab \`\`\` \# \#\#\# Set :warning: \*\*Warning:\*\* if you want to set single value and not all values table of vector, use \[SetVector\\(\\)\]\(\#set-vector\) function instead Parameters: \| Name \| Type \| Description \| \| :------------- \| :----- \| :---------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of variable to set value for \| \| value \| any \| automatic variable value, for a checkbox/toggle - bool. for a sliderint/combo/multicombo - integer. for a sliderfloat - float. for a hotkey - bool. for a color picker - \[Color\]\(../datatypes/color.md\). for a vector \(also any type of supported e.g. \`bool\`, \`int\`, \`float\`\) - table of \*\*ALL\*\* values \| Code: \`\`\`lua Config.Set\(Vars.bRageAutoFire, true\) Config.Set\(Vars.colEspMainBoxEnemies, Color.new\(255, 255, 255\)\) \`\`\` \# \#\#\# SetVector Parameters: \| Name \| Type \| Description \| \| :------------- \| :----- \| :---------------------------------------------------------------------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of vector variable \| \| nVectorIndex \| uint32 \| index of vector entry to set value for \| \| value \| any \| automatic variable value to set to given vector at given \`nVectorIndex\` \| Code: \`\`\`lua Config.SetVector\(Vars.vecRagePreferSafePoints, 1, true\) -- enable prefer safe points checkbox in deagle/relolver \(revolver icon\) ragebot tab Config.SetVector\(Vars.vecRageHitChance, 3, 50\) -- set 50% hitchance value in snipers \(scar-20 icon\) tab \`\`\`

 \#\#\# Get :warning: \*\*Warning:\*\* if you want to get single value and not all values table of vector, use \[GetVector\\(\\)\]\(\#get-vector\) function instead Parameters: \| Name \| Type \| Description \| \| :---------------------- \| :----- \| :-------------------------------- \| \| \[nVariableIndex\]\(\#vars\) \| uint32 \| index of variable to get value of \| Returns: \| Type \| Description \| \| :--- \| :---------- \| \| any \| automatic variable value, for a checkbox/toggle, returns boolean. for a sliderint/combo/multicombo, returns an integer. for a sliderfloat, returns a float. for a hotkey, returns true if the hotkey is active. for a color picker, returns \[Color\]\(../datatypes/color.md\). for a vector \(also any type of supported e.g. \`bool\`, \`int\`, \`float\`\), returns table \| Code: \`\`\`lua local bValue = Config.Get\(Vars.bRageAutoFire\) local colValue = Config.Get\(Vars.colEspMainBoxEnemies\) \`\`\` \# \#\#\# GetVector Parameters: \| Name \| Type \| Description \| \| :---------------------- \| :----- \| :------------------------------------ \| \| \[nVariableIndex\]\(\#vars\) \| uint32 \| index of vector variable \| \| nVectorIndex \| uint32 \| index of vector entry to get value of \| Returns: \| Type \| Description \| \| :--- \| :--------------------------------------------------------------- \| \| any \| automatic variable value of given vector at given \`nVectorIndex\` \| Code: \`\`\`lua local bValue = Config.GetVector\(Vars.vecRagePreferSafePoints, 1\) -- prefer safe points checkbox state in deagle/relolver \(revolver icon\) ragebot tab local iValue = Config.GetVectorInt\(Vars.vecRageHitChance, 3\) -- hitchance value in snipers \(scar-20 icon\) ragebot tab \`\`\` \# \#\#\# Set :warning: \*\*Warning:\*\* if you want to set single value and not all values table of vector, use \[SetVector\\(\\)\]\(\#set-vector\) function instead Parameters: \| Name \| Type \| Description \| \| :---------------------- \| :----- \| :--------------------------------- \| \| \[nVariableIndex\]\(\#vars\) \| uint32 \| index of variable to set value for \| \| value \| any \| automatic variable value, for a checkbox/toggle - bool. for a sliderint/combo/multicombo - integer. for a sliderfloat - float. for a hotkey - bool. for a color picker - \[Color\]\(../datatypes/color.md\). for a vector \(also any type of supported e.g. \`bool\`, \`int\`, \`float\`\) - table of \*\*ALL\*\* values \| Code: \`\`\`lua Config.Set\(Vars.bRageAutoFire, true\) Config.Set\(Vars.colEspMainBoxEnemies, Color.new\(255, 255, 255\)\) \`\`\` \# \#\#\# SetVector Parameters: \| Name \| Type \| Description \| \| :------------- \| :----- \| :---------------------------------------------------------------------- \| \| \[nVariableIndex\]\(\#vars\) \| uint32 \| index of vector variable \| \| nVectorIndex \| uint32 \| index of vector entry to set value for \| \| value \| any \| automatic variable value to set to given vector at given \`nVectorIndex\` \| Code: \`\`\`lua Config.SetVector\(Vars.vecRagePreferSafePoints, 1, true\) -- enable prefer safe points checkbox in deagle/relolver \(revolver icon\) ragebot tab Config.SetVector\(Vars.vecRageHitChance, 3, 50\) -- set 50% hitchance value in snipers \(scar-20 icon\) tab \`\`\`

Parameters:

\| Name \| Type \| Description \| \| :------------- \| :------------ \| :---------------------------------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of variable to get value of \| Returns: \| Type \| Description \| \| :--- \| :---------- \| \| any \| automatic variable value, for a checkbox/toggle, returns boolean. for a sliderint/combo/multicombo, returns an integer. for a sliderfloat, returns a float. for a hotkey, returns true if the hotkey is active. for a color picker, returns \[Color\]\(../datatypes/color.md\). for a vector \(also any type of supported e.g. \`bool\`, \`int\`, \`float\`\), returns table \| Code: \`\`\`lua local bValue = Config.Get\(Vars.bRageAutoFire\) local colValue = Config.Get\(Vars.colEspMainBoxEnemies\) \`\`\` \# \#\#\# GetVector Parameters: \| Name \| Type \| Description \| \| :------------- \| :---- \| :------------------------------------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of vector variable \| \| nVectorIndex \| uint32 \| index of vector entry to get value of \| Returns: \| Type \| Description \| \| :--- \| :--------------------------------------------------------------- \| \| any \| automatic variable value of given vector at given \`nVectorIndex\` \| Code: \`\`\`lua local bValue = Config.GetVector\(Vars.vecRagePreferSafePoints, 1\) -- prefer safe points checkbox state in deagle/relolver \(revolver icon\) ragebot tab local iValue = Config.GetVectorInt\(Vars.vecRageHitChance, 3\) -- hitchance value in snipers \(scar-20 icon\) ragebot tab \`\`\` \# \#\#\# Set :warning: \*\*Warning:\*\* if you want to set single value and not all values table of vector, use \[SetVector\\(\\)\]\(\#set-vector\) function instead Parameters: \| Name \| Type \| Description \| \| :------------- \| :----- \| :---------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of variable to set value for \| \| value \| any \| automatic variable value, for a checkbox/toggle - bool. for a sliderint/combo/multicombo - integer. for a sliderfloat - float. for a hotkey - bool. for a color picker - \[Color\]\(../datatypes/color.md\). for a vector \(also any type of supported e.g. \`bool\`, \`int\`, \`float\`\) - table of \*\*ALL\*\* values \| Code: \`\`\`lua Config.Set\(Vars.bRageAutoFire, true\) Config.Set\(Vars.colEspMainBoxEnemies, Color.new\(255, 255, 255\)\) \`\`\` \# \#\#\# SetVector Parameters: \| Name \| Type \| Description \| \| :------------- \| :----- \| :---------------------------------------------------------------------- \| \| nVariableIndex \| \[uint32\]\(\#vars\) \| index of vector variable \| \| nVectorIndex \| uint32 \| index of vector entry to set value for \| \| value \| any \| automatic variable value to set to given vector at given \`nVectorIndex\` \| Code: \`\`\`lua Config.SetVector\(Vars.vecRagePreferSafePoints, 1, true\) -- enable prefer safe points checkbox in deagle/relolver \(revolver icon\) ragebot tab Config.SetVector\(Vars.vecRageHitChance, 3, 50\) -- set 50% hitchance value in snipers \(scar-20 icon\) tab \`\`\`


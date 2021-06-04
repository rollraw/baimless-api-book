# IEntityList interface

## Functions

 \#\#\# GetClientEntity Parameters: \| Name \| Type \| Description \| \| :----- \| :--- \| :--------------------- \| \| nIndex \| int \| index of entity to get \| Returns: \| Type \| Description \| \| :-------------- \| :---------------------------- \| \| IClientEntity\\* \| entity pointer of given index \| Code: \`\`\`lua local pLocal = IEntityList.GetClientEntity\(IEngine.GetLocalPlayer\(\)\) \`\`\` \# \#\#\# GetClientEntityFromHandle Parameters: \| Name \| Type \| Description \| \| :------ \| :---------- \| :---------------------- \| \| hHandle \| CBaseHandle \| handle of entity to get \| Returns: \| Type \| Description \| \| :-------------- \| :----------------------------- \| \| IClientEntity\\* \| entity pointer of given handle \| Code: \`\`\`lua local pLocalWeapon = IEntityList.GetClientEntity\(pLocal.GetWeaponHandle\(\)\) \`\`\` \# \#\#\# GetHighestEntityIndex Returns: \| Type \| Description \| \| :--- \| :------------------- \| \| int \| highest entity index \| Code: \`\`\`lua local nHighestEntityIndex = IEntityList.GetHighestEntityIndex\(\) \`\`\`


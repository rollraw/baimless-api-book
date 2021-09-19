---
description: Functions to work with cheat configuration variables
---

# config

🚧 _API of this file is not finished yet and could be changed in any time_

## Enumerations

### Vars

Description: variables indexes to be used in [Set\(\)](config.md#set)/[Get\(\)](config.md#get) functions, passed as `nVariableIndex` argument

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
| :--- |
| bRage                                  |
| bRageAutoFire                          |
| iRageAutoZeusDelay                     |
| iRageHeadScale                         |
| iRageBodyScale                         |
| keyRageDoubleTap                       |
| keyRageHideShots                       |
| keyRageForceOverrideResolver           |
| keyRageForceBackShoot                  |
| bRageForceFullScanInAir                |
| nRageLogicLocal                        |
| iRageLogicLocalTrigger                 |
| iRageLogicLocalLowHealth               |
| nRageLogicEnemy                        |
| iRageLogicEnemyTrigger                 |
| iRageLogicEnemyLowHealth               |
| bRageFakeLag                           |
| iRageFakeLagType                       |
| iRageFakeLagTicks                      |
| iRageLegBreakerTicks                   |
| iRageFakeLagJitter                     |
| nRageFakeLagTriggers                   |
| iRageFakeLagTriggersTicks              |
| bRageBreakLC                           |
| bRageHoldFireAnimation                 |
| bRageStaticLegsMove                    |
| bRageJitterLegsMove                    |
| bRageStaticLegsAir                     |
| iRageAntiAimForceLowDeltaMode          |
| nRageAntiAimForceLowDeltaConditions    |
| keyRageAntiAimForceLowDelta            |
| keyRageSlowWalk                        |
| iRageSlowWalkMode                      |
| keyRageFakeDuck                        |
| bRageScanFakeDuckFull                  |
| keyRageAntiAimManualLeft               |
| keyRageAntiAimManualRight              |
| keyRageAntiAimManualBack               |
| keyRageSafeAntiAim                     |
| iRageSafeAntiAimYaw                    |
| iRageSafeAntiAimYawInverted            |
| bRageSafeAntiAimForceLowDelta          |
| bRageSafeAntiAimAtTarget               |
| bRageSafeAntiAimHideReal               |
| vecRageAntiAim                         |
| vecRageAntiAimManual                   |
| vecRageAntiAimTimerSwitch              |
| vecRageAntiAimTimerJitter              |
| vecRageAntiAimYaw                      |
| vecRageAntiAimYawInverted              |
| vecRageAntiAimYawRandomMin             |
| vecRageAntiAimYawRandomMax             |
| vecRageAntiAimJitter                   |
| vecRageAntiAimJitterInverted           |
| vecRageAntiAimFakeYaw                  |
| vecRageAntiAimSideToSide               |
| vecRageAntiAimSideToSideOverlap        |
| vecRageAntiAimFreestand                |
| vecRageAntiAimAtTarget                 |
| vecRageAntiAimHideReal                 |
| vecRageAntiAimInvertMode               |
| keyRageAntiAimInvert                   |
| vecRageAntiAimAntiResolver             |
| vecRageAntiAimAntiResolverConditions   |
| vecRageAntiAimAntiLBY                  |
| vecRageAntiAimDesyncOnShot             |
| vecRageMultiPoint                      |
| vecRageHitScan                         |
| vecRageFOV                             |
| vecRageSilent                          |
| vecRageAutoStop                        |
| vecRageAutoStopEarly                   |
| vecRageAutoStopForcePrecision          |
| vecRageAutoStopEarlyTime               |
| vecRageAutoStopTriggers                |
| vecRageAutoScope                       |
| vecRageDoubleTapWaitRecharge           |
| vecRageDoubleTapRechargeDelay          |
| vecRageRechargeTicks                   |
| vecRageDoubleTapAdaptiveSelection      |
| vecRageDoubleTapHitChance              |
| vecRageDoubleTapFastTeleport           |
| vecRageForceDamage                     |
| vecRageForceDamageHealthLess           |
| vecRageShiftMinusChoke                 |
| vecRagePreferBody                      |
| vecRagePreferSafePoints                |
| vecRageHitChanceMode                   |
| vecRageHitChance                       |
| vecRageHitChanceStand                  |
| vecRageHitChanceAir                    |
| vecRageHitChanceMove                   |
| vecRageHitChanceSlowWalk               |
| vecRageHitChanceFakeDuck               |
| vecRageMinimalDamageVisible            |
| vecRageMinimalDamageInvisible          |
| keyRageMinimalDamageOverride           |
| vecRageMinimalDamageOverride           |
| bLegit                                 |
| keyLegit                               |
| bLegitFlashCheck                       |
| bLegitSmokeCheck                       |
| bLegitJumpCheck                        |
| bLegitAutoFire                         |
| bLegitShowFOV                          |
| bLegitShowSilentFOV                    |
| colLegitFOV                            |
| colLegitSilentFOV                      |
| bLegitStandaloneRCS                    |
| flLegitStandaloneRCSPowerX             |
| flLegitStandaloneRCSPowerY             |
| bLegitBackTracking                     |
| iLegitBackTrackTime                    |
| bLegitAimAtBackTrack                   |
| bLegitResolver                         |
| bLegitAntiAim                          |
| bLegitAntiAimShowSide                  |
| iLegitAntiAimSwitchKey                 |
| vecLegitEnable                         |
| vecLegitScopeCheck                     |
| vecLegitFirstShotDelay                 |
| vecLegitKillDelay                      |
| vecLegitSilent                         |
| vecLegitSilentJumpShot                 |
| vecLegitSilentBullets                  |
| vecLegitSilentFOV                      |
| vecLegitHitbox                         |
| vecLegitDistanceBasedFOV               |
| vecLegitFOV                            |
| vecLegitSmooth                         |
| bTrigger                               |
| keyTrigger                             |
| bTriggerFlashCheck                     |
| bTriggerSmokeCheck                     |
| bTriggerJumpCheck                      |
| iTriggerDelay                          |
| bTriggerAutoWall                       |
| iTriggerMinimalDamage                  |
| bTriggerHead                           |
| bTriggerChest                          |
| bTriggerStomach                        |
| bTriggerArms                           |
| bTriggerLegs                           |
| bTriggerAutoZeusKnife                  |
| keyTriggerAutoZeusKnife                |
| iTriggerAutoZeusKnifePreference        |
| bEspMain                               |
| bEspMainEnemies                        |
| bEspMainAllies                         |
| bEspMainWeapons                        |
| bEspMainGrenades                       |
| bEspMainBomb                           |
| iEspMainPlayerBox                      |
| colEspMainBoxEnemies                   |
| colEspMainBoxEnemiesWall               |
| colEspMainBoxAllies                    |
| colEspMainBoxAlliesWall                |
| bEspMainPlayerSkeleton                 |
| colEspMainSkeletonEnemies              |
| colEspMainSkeletonAllies               |
| bEspMainPlayerOutOfScreen              |
| flEspMainPlayerOutOfScreenRadius       |
| flEspMainPlayerOutOfScreenSize         |
| flEspMainPlayerOutOfScreenThickness    |
| colEspMainPlayerOutOfScreenEnemies     |
| colEspMainPlayerOutOfScreenAllies      |
| bEspMainPlayerSoundRings               |
| flEspMainPlayerSoundRingsTime          |
| flEspMainPlayerSoundRingsRadius        |
| colEspMainPlayerSoundRings             |
| bEspMainPlayerInfo                     |
| bEspMainPlayerHealth                   |
| iEspMainPlayerHealthSide               |
| bEspMainPlayerHealthPoints             |
| iEspMainPlayerHealthPointsSide         |
| iEspMainPlayerHealthPointsChildSide    |
| bEspMainPlayerMoney                    |
| iEspMainPlayerMoneySide                |
| iEspMainPlayerMoneyChildSide           |
| bEspMainPlayerRank                     |
| iEspMainPlayerRankSide                 |
| iEspMainPlayerRankChildSide            |
| bEspMainPlayerName                     |
| iEspMainPlayerNameSide                 |
| iEspMainPlayerNameChildSide            |
| bEspMainPlayerFlash                    |
| iEspMainPlayerFlashSide                |
| iEspMainPlayerFlagsMode                |
| nEspMainPlayerFlags                    |
| iEspMainPlayerHelmetSide               |
| iEspMainPlayerHelmetChildSide          |
| iEspMainPlayerKevlarSide               |
| iEspMainPlayerKevlarChildSide          |
| iEspMainPlayerKitSide                  |
| iEspMainPlayerKitChildSide             |
| iEspMainPlayerZoomSide                 |
| iEspMainPlayerZoomChildSide            |
| iEspMainPlayerFakeDuckSide             |
| iEspMainPlayerFakeDuckChildSide        |
| iEspMainPlayerWeaponsMode              |
| nEspMainPlayerWeaponsFlags             |
| iEspMainPlayerWeaponsSide              |
| iEspMainPlayerWeaponsChildSide         |
| iEspMainPlayerGrenadesSide             |
| iEspMainPlayerGrenadesChildSide        |
| bEspMainPlayerAmmo                     |
| iEspMainPlayerAmmoSide                 |
| bEspMainPlayerDistance                 |
| iEspMainPlayerDistanceSide             |
| iEspMainPlayerDistanceChildSide        |
| iEspMainWeaponBox                      |
| colEspMainBoxWeapons                   |
| bEspMainWeaponInfo                     |
| bEspMainWeaponIcon                     |
| bEspMainWeaponAmmo                     |
| bEspMainWeaponDistance                 |
| bEspMainGrenadeTimer                   |
| bEspMainGrenadeHull                    |
| bEspMainGrenadeWarning                 |
| bEspMainGrenadeTrail                   |
| flEspMainGrenadeTrailTime              |
| colEspMainGrenadeTrail                 |
| iEspPreviewCurrent                     |
| bEspGlow                               |
| bEspGlowEnemies                        |
| bEspGlowAllies                         |
| bEspGlowLocal                          |
| bEspGlowWeapons                        |
| bEspGlowGrenades                       |
| bEspGlowBomb                           |
| iEspGlowPlayers                        |
| iEspGlowLocal                          |
| iEspGlowWeapons                        |
| iEspGlowGrenades                       |
| iEspGlowBomb                           |
| bEspGlowBloom                          |
| colEspGlowEnemies                      |
| colEspGlowEnemiesWall                  |
| colEspGlowAllies                       |
| colEspGlowAlliesWall                   |
| colEspGlowLocal                        |
| colEspGlowLocalWall                    |
| colEspGlowWeapons                      |
| colEspGlowGrenades                     |
| colEspGlowBomb                         |
| colEspGlowBombPlanted                  |
| bEspChams                              |
| bEspChamsDisable                       |
| bEspChamsEnemies                       |
| bEspChamsAllies                        |
| bEspChamsLocal                         |
| bEspChamsViewModel                     |
| iEspChamsPlayers                       |
| iEspChamsPlayersCustom                 |
| bEspChamsPlayersXQZ                    |
| bEspChamsPlayersWireframe              |
| flEspChamsPlayersPearlescent           |
| bEspChamsPlayersRagdoll                |
| colEspChamsEnemies                     |
| colEspChamsEnemiesWall                 |
| colEspChamsEnemiesAdditional           |
| colEspChamsEnemiesAdditionalWall       |
| colEspChamsAllies                      |
| colEspChamsAlliesWall                  |
| colEspChamsAlliesAdditional            |
| colEspChamsAlliesAdditionalWall        |
| iEspChamsPreserveHit                   |
| iEspChamsPreserveHitCustom             |
| bEspChamsPreserveHitXQZ                |
| flEspChamsPreserveHitTime              |
| colEspChamsPreserveHit                 |
| colEspChamsPreserveHitWall             |
| colEspChamsPreserveHitAdditional       |
| colEspChamsPreserveHitAdditionalWall   |
| iEspChamsBackTrack                     |
| iEspChamsBackTrackMode                 |
| iEspChamsBackTrackCustom               |
| bEspChamsBackTrackXQZ                  |
| bEspChamsBackTrackWireframe            |
| colEspChamsBackTrackFirst              |
| colEspChamsBackTrackFirstAdditional    |
| colEspChamsBackTrackLast               |
| colEspChamsBackTrackLastAdditional     |
| iEspChamsLocal                         |
| iEspChamsLocalCustom                   |
| bEspChamsLocalXQZ                      |
| bEspChamsLocalWireframe                |
| flEspChamsLocalPearlescent             |
| iEspChamsLocalDesync                   |
| iEspChamsLocalDesyncCustom             |
| colEspChamsLocal                       |
| colEspChamsLocalWall                   |
| colEspChamsLocalAdditional             |
| colEspChamsLocalAdditionalWall         |
| colEspChamsLocalDesync                 |
| colEspChamsLocalDesyncAdditional       |
| bEspChamsViewModelNoDraw               |
| iEspChamsViewModel                     |
| iEspChamsViewModelCustom               |
| bEspChamsViewModelXQZ                  |
| bEspChamsViewModelWireframe            |
| flEspChamsViewModelPearlescent         |
| colEspChamsViewModel                   |
| colEspChamsViewModelWall               |
| colEspChamsViewModelAdditional         |
| colEspChamsViewModelAdditionalWall     |
| vecEspChamsCustomMaterials             |
| bWorld                                 |
| iWorldSkyBox                           |
| szWorldSkyBoxCustom                    |
| nWorldRemovalsFlags                    |
| colWorldRemovalsNoScopeCrosshair       |
| iWorldScopeType                        |
| iWorldMaxFlash                         |
| bWorldRagdollGravity                   |
| bWorldMovementTrail                    |
| bWorldMovementTrailDashed              |
| flWorldMovementTrailTime               |
| flWorldMovementTrailThickness          |
| colWorldMovementTrail                  |
| colWorldMovementTrailDash              |
| keyWorldThirdPerson                    |
| flWorldThirdPersonOffset               |
| bWorldThirdPersonForceSpectate         |
| bWorldThirdPersonDisableGrenade        |
| bWorldExposure                         |
| flWorldExposureFactor                  |
| bWorldBloom                            |
| flWorldBloomFactor                     |
| bWorldFog                              |
| flWorldFogStart                        |
| flWorldFogEnd                          |
| flWorldFogDensity                      |
| colWorldFog                            |
| iWorldWeather                          |
| flWorldWeatherParticleLenght           |
| iWorldWeatherWindPower                 |
| flWorldNightFactor                     |
| bWorldOverrideColor                    |
| colWorldOverride                       |
| bWorldPropertiesOverrideColor          |
| colWorldPropertiesOverride             |
| bWorldSkyBoxOverrideColor              |
| colWorldSkyBoxOverride                 |
| bWorldMolotovOverrideColor             |
| colWorldMolotovOverride                |
| bWorldSmokeOverrideColor               |
| colWorldSmokeOverride                  |
| bWorldBulletTracer                     |
| nWorldBulletTracerShowTrace            |
| colWorldBulletTracer                   |
| colWorldBulletTracerHit                |
| nWorldBulletTracerShowImpact           |
| colWorldBulletTracerBox                |
| colWorldBulletTracerBoxHit             |
| flWorldBulletTracerTime                |
| bScreen                                |
| bScreenSpectatorList                   |
| flScreenSpectatorListBackgroundAlpha   |
| bScreenIndicators                      |
| flScreenIndicatorsBackgroundAlpha      |
| bScreenVelocityIndicator               |
| bScreenVelocityIndicatorGraph          |
| bScreenVelocityIndicatorJumpDifference |
| flScreenVelocityIndicatorGraphSpeed    |
| bScreenEventLog                        |
| iScreenEventLogMaxCount                |
| flScreenEventLogTime                   |
| bScreenGrenadePathPrediction           |
| bScreenGrenadePathPredictionAlways     |
| bScreenPenetrationIndicator            |
| bScreenVisualizeKnifeZeusRange         |
| colScreenKnifeZeusRange                |
| bScreenPreserveKillFeed                |
| bScreenPreserveKillFeedOnlyHS          |
| bScreenForceCompass                    |
| flScreenAspectRatio                    |
| flScreenCameraFOV                      |
| bScreenCameraFOVIgnoreScope            |
| flScreenViewModelFOV                   |
| vecScreenViewModelPosition             |
| vecScreenViewModelAngles               |
| bScreenRadar                           |
| bScreenRadarInGame                     |
| bScreenRadarEnemies                    |
| bScreenRadarAllies                     |
| bScreenRadarWeapons                    |
| bScreenRadarBomb                       |
| bScreenRadarSpottedCheck               |
| bScreenRadarPlayerName                 |
| flScreenRadarScale                     |
| bScreenCustomHUD                       |
| bScreenCustomHUDHideOriginal           |
| bScreenHealth                          |
| iScreenHealthStyle                     |
| flScreenHealthBackgroundAlpha          |
| colScreenHealth                        |
| bScreenArmor                           |
| iScreenArmorStyle                      |
| flScreenArmorBackgroundAlpha           |
| colScreenArmor                         |
| bScreenWeaponSelection                 |
| bScreenWeaponSelectionAmmoFill         |
| colScreenWeaponSelectionActive         |
| colScreenWeaponSelectionActiveFill     |
| colScreenWeaponSelectionInactive       |
| colScreenWeaponSelectionInactiveFill   |
| bScreenAmmo                            |
| flScreenAmmoBackgroundAlpha            |
| colScreenAmmo                          |
| colScreenAmmoReserve                   |
| colScreenAmmoLow                       |
| bScreenLastPlace                       |
| flScreenLastPlaceBackgroundAlpha       |
| colScreenLastPlace                     |
| bScreenMoney                           |
| colScreenMoney                         |
| flScreenMoneyBackgroundAlpha           |
| bScreenMiniScoreboard                  |
| bScreenKillStreaks                     |
| flScreenKillStreaksTime                |
| bScreenCrosshair                       |
| bScreenCrosshairOnlySniper             |
| bScreenCrosshairRecoilBased            |
| bScreenCrosshairDot                    |
| flScreenCrosshairGap                   |
| flScreenCrosshairLenght                |
| flScreenCrosshairThickness             |
| flScreenCrosshairOutline               |
| vecScreenCrosshairSides                |
| colScreenCrosshair                     |
| bScreenHitMarker                       |
| bScreenHitMarkerDamage                 |
| iScreenHitMarkerSound                  |
| bScreenHitMarkerKillEffect             |
| flScreenHitMarkerTime                  |
| flScreenHitMarkerGap                   |
| flScreenHitMarkerLenght                |
| flScreenHitMarkerThickness             |
| colScreenHitMarker                     |
| colScreenHitMarkerDamage               |
| bScreenBombInfo                        |
| bScreenBombInfoDamage                  |
| flScreenBombInfoBackgroundAlpha        |
| bMiscBunnyHop                          |
| iMiscBunnyHopChance                    |
| iMiscAutoStrafe                        |
| keyMiscAutoStrafe                      |
| iMiscWalkMode                          |
| bMiscEdgeJump                          |
| keyMiscEdgeJump                        |
| bMiscEdgeJumpAutoDuck                  |
| keyMiscEdgeBug                         |
| keyMiscJumpBug                         |
| bMiscJumpBugAutoJump                   |
| keyMiscCrouchBug                       |
| keyMiscBlockBot                        |
| keyMiscRunBoostBot                     |
| keyMiscDoorSpam                        |
| bMiscAutoAccept                        |
| keyMiscAutoPeek                        |
| bMiscAutoPistol                        |
| bMiscQuickReload                       |
| bMiscAccurateWalk                      |
| bMiscFastStop                          |
| bMiscNoCrouchCooldown                  |
| bMiscBuyBot                            |
| iMiscBuyBotPrimary                     |
| iMiscBuyBotSecondary                   |
| iMiscBuyBotEquipment                   |
| bMiscRecorder                          |
| iMiscRecorderShowPath                  |
| bMiscRecorderAutoPoint                 |
| bMiscRecorderFreeLook                  |
| flMiscRecorderSmooth                   |
| iMiscRecorderKey                       |
| iMiscRecorderPlayKey                   |
| iMiscRecorderCutKey                    |
| iMiscRecorderCutAndResumeKey           |
| bMiscGrenadeHelper                     |
| iMiscGrenadeHelperShowInfo             |
| keyMiscGrenadeHelperAim                |
| flMiscGrenadeHelperFOV                 |
| flMiscGrenadeHelperSmooth              |
| bMiscPingSpike                         |
| keyMiscPingSpike                       |
| flMiscLatencyFactor                    |
| bMiscRevealRanks                       |
| bMiscRevealOverwatch                   |
| bMiscUnlockInventory                   |
| bMiscAntiUntrusted                     |
| bMenuKeyBinds                          |
| bMenuKeyBindsShowOnlyActive            |
| flMenyKeyBindsBackgroundAlpha          |
| iMenuKey                               |
| iPanicKey                              |
| bMenuWatermark                         |
| bMenuRainbowBar                        |
| iMenuBlurFactor                        |
| colMenuAccentFirst                     |
| colMenuAccentSecond                    |
| colMenuAccentThird                     |
| bModelChangerEnable                    |
| bProfileNameChanger                    |
| bProfileNameChangerSpam                |
| bProfileNameChangerSteal               |
| szProfileNameChangerName               |
| bProfileClanTag                        |
| bProfileChatSpam                       |
| bProfileChatSpamTeamOnly               |
| flProfileChatSpamDelay                 |
| szProfileChatSpamMessage               |
| bProfileLobby                          |
| bProfileLobbyRankChanger               |
| iProfileLevel                          |
| iProfileLevelXP                        |
| iProfileCommendsLeader                 |
| iProfileCommendsTeacher                |
| iProfileCommendsFriendly               |
| iProfileMatchMakingRank                |
| iProfileMatchMakingWins                |
| iProfileWingmanRank                    |
| iProfileWingmanWins                    |
| iProfileDangerZoneRank                 |
| iProfileDangerZoneWins                 |
## Functions

### Get

⚠️ **Warning:** if you want to get single value and not all values table of vector, use [GetVector\(\)](config.md#getvector) function instead

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| [nVariableIndex](config.md#vars) | uint32 | index of variable to get value of |

Returns:

| Type | Description |
| :--- | :--- |
| any | automatic variable value, for a checkbox/toggle, returns boolean. for a sliderint/combo/multicombo, returns an integer. for a sliderfloat, returns a float. for a hotkey, returns true if the hotkey is active. for a color picker, returns [Color](../datatypes/color.md). for a vector \(also any type of supported e.g. `bool`, `int`, `float`\), returns table |

Code:

```text
local bValue = Config.Get(Vars.bRageAutoFire)
local colValue = Config.Get(Vars.colEspMainBoxEnemies)
```

### GetVector

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| [nVariableIndex](config.md#vars) | uint32 | index of vector variable |
| nVectorIndex | uint32 | index of vector entry to get value of |

Returns:

| Type | Description |
| :--- | :--- |
| any | automatic variable value of given vector at given `nVectorIndex` |

Code:

```lua
local bValue = Config.GetVector(Vars.vecRagePreferSafePoints, 1) -- prefer safe points checkbox state in deagle/relolver (revolver icon) ragebot tab
local iValue = Config.GetVectorInt(Vars.vecRageHitChance, 3) -- hitchance value in snipers (scar-20 icon) ragebot tab
```

### Set

⚠️ **Warning:** if you want to set single value and not all values table of vector, use [SetVector\(\)](config.md#setvector) function instead

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| [nVariableIndex](config.md#vars) | uint32 | index of variable to set value for |
| value | any | automatic variable value, for a checkbox/toggle - bool. for a sliderint/combo/multicombo - integer. for a sliderfloat - float. for a hotkey - bool. for a color picker - [Color](../datatypes/color.md). for a vector \(also any type of supported e.g. `bool`, `int`, `float`\) - table of **ALL** values |

Code:

```lua
Config.Set(Vars.bRageAutoFire, true)
Config.Set(Vars.colEspMainBoxEnemies, Color.new(255, 255, 255))
```

### SetVector

Parameters:

| Name | Type | Description |
| :--- | :--- | :--- |
| [nVariableIndex](config.md#vars) | uint32 | index of vector variable |
| nVectorIndex | uint32 | index of vector entry to set value for |
| value | any | automatic variable value to set to given vector at given `nVectorIndex` |

Code:

```lua
Config.SetVector(Vars.vecRagePreferSafePoints, 1, true) -- enable prefer safe points checkbox in deagle/relolver (revolver icon) ragebot tab
Config.SetVector(Vars.vecRageHitChance, 3, 50) -- set 50% hitchance value in snipers (scar-20 icon) tab
```


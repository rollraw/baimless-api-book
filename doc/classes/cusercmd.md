# CUserCmd class

## Enumerations

 \#\#\# EButtonFlags Description: button states bitflags for \`iButtons\` variable \| Indentifiers \| \| ---------------- \| \| IN\_ATTACK \| \| IN\_JUMP \| \| IN\_DUCK \| \| IN\_BACK \| \| IN\_USE \| \| IN\_CANCEL \| \| IN\_RIGHT \| \| IN\_MOVELEFT \| \| IN\_MOVERIGHT \| \| IN\_SECOND\_ATTACK \| \| IN\_RUN \| \| IN\_RELOAD \| \| IN\_LEFT\_ALT \| \| IN\_RIGHT\_ALT \| \| IN\_SCORE \| \| IN\_SPEED \| \| IN\_WALK \| \| IN\_ZOOM \| \| IN\_FIRST\_WEAPON \| \| IN\_SECOND\_WEAPON \| \| IN\_BULLRUSH \| \| IN\_FIRST\_GRENADE \| \| IN\_SECOND\_GRENAD \| \| IN\_MIDDLE\_ATTACK \|

## Variables

  
 \| Name \| Type \| Description \| \| :---------------- \| :------ \| :--------------------------------------------------------------------- \| \| iCommandNumber \| int \| for matching server and client commands for debugging \| \| iTickCount \| int \| the tick the client created this command \| \| angViewPoint \| QAngle \| player instantaneous view angles \| \| flForwardMove \| float \| forward velocity \| \| flSideMove \| float \| sideways velocity \| \| flUpMove \| float \| upward velocity \| \| \[iButtons\]\(\#button-flags\) \| bitflag \| button states flags \| \| uImpulse \| byte \| impulse command issued \| \| iWeaponSelect \| int \| current weapon index \| \| iWeaponSubType \| int \| current weapon subtype \| \| iRandomSeed \| int \| for shared random functions \| \| sMouseDeltaX \| int \| mouse accumulate in x from create move \| \| sMouseDeltaY \| int \| mouse accumulate in y from create move \| \| bHasBeenPredicted \| int \| client only, tracks whether we've predicted this command at least once \|


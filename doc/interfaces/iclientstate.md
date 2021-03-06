# iclientstate

## Variables

| Name | Type | Description |
| :--- | :--- | :--- |
| iChallengeNr | int | connection challenge number |
| iSignonState | int | sign on state |
| flNextCmdTime | float | time when we can send the next command packet |
| nServerCount | int | server identification for prespawns |
| iCurrentSequence | int | sequence number of the current incoming packet |
| iDeltaTick | int | last valid received snapshot \(server\) tick |
| bPaused | bool | send over by server |
| iViewEntity | int | player point of view override |
| iPlayerSlot | int | own player entity index-1. skips world. add 1 to get cl\_entitites index |
| nMaxClients | int | max clients on server |
| flLastServerTickTime | float | the timestamp of last message |
| bInSimulation | bool | - |
| iOldTickcount | int | previous tick |
| flTickRemainder | float | client copy of tick remainder |
| flFrameTime | float | dt of the current frame |
| iLastOutgoingCommand | int | sequence number of last outgoing command |
| nChokedCommands | int | number of choked commands |
| iLastCommandAck | int | last command sequence number acknowledged by server |
| iCommandAck | int | current command sequence acknowledged by server |
| iSoundSequence | int | current processed reliable sound sequence number |
| angViewPoint | [QAngle](../datatypes/qangle.md) | - |


# IGlobals interface

## Variables

  
 \| Name \| Type \| Description \| \| :-------------------- \| :----- \| :-------------------------------------------------------------------- \| \| flRealTime \| float \| absolute time \| \| iFrameCount \| int \| absolute frame counter - continues to increase even if game is paused \| \| flAbsFrameTime \| float \| non-paused frametime \| \| flAbsFrameStartTime \| float \| - \| \| flCurrentTime \| float \| current time depends on host\_timescale \| \| flFrameTime \| float \| time spent on last server or client frame \| \| nMaxClients \| int \| current max players setting \| \| iTickCount \| int \| simluation ticks - doesn't increase when game is paused \| \| flIntervalPerTick \| float \| simulation tick interval. tickrate = 1.0/flIntervalPerTick \| \| flInterpolationAmount \| float \| interpolation amount based on fraction of next tick \| \| nFrameSimulationTicks \| int \| simulation ticks this frame \| \| iNetworkProtocol \| int \| - \|


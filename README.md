# blueprints
HA blueprints

Tasmota rules to add on the device:

Backlog Rule2 on var1#State do L1MusicSync %value%,x,x endon on var1#State do Publish %topic%/musicsync %value% endon on var2#State do L1MusicSync 1,%value%,x endon on var2#state do Publish %topic%/sensitive %value% endon on var3#State do L1MusicSync 1,x,%value% endon on var3#State do Publish %topic%/speed %value% endon; Rule2 1

Backlog Rule3 on L1MusicSync#Mode do var1 %value% endon on L1MusicSync#Sensitive do var2 %value% endon on L1MusicSync#Speed do var3 %value% endon; Rule3 1


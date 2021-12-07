# blueprints
HA blueprints

Tasmota rules to add on the device:

Rule2 on var1#State do Backlog L1MusicSync %value%,x,x; Event checkvar=%var1% endon on Event#checkvar=1 do Publish %topic%/musicsync ON endon on Event#checkvar=0 do Publish %topic%/musicsync OFF endon on var2#State do L1MusicSync 1,%value%,x endon on var2#state do Publish %topic%/sensitive %value% endon on var3#State do L1MusicSync 1,x,%value% endon on var3#State do Publish %topic%/speed %value% endon

Rule2 1

Backlog Rule3 on L1MusicSync#Mode do Publish %topic%/musicsync %value% endon on L1MusicSync#Sensitive do Publish %topic%/sensitive %value% endon on L1MusicSync#Speed do Publish %topic%/speed %value% endon; Rule3 1

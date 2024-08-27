// ##################################################################
//                 #3 LABELS v0.4
// ##################################################################

GroundLabel=1
GroundLabel_Font=EuroScope
GroundLabel_FontStyle=1000,0,0,0
GroundLabel_FontSize=11
GroundLabel_Transparency_Bg=100
TowerLabel_FontSize=11
AppLabel_FontSize=11

Label=GND:ARR:0:ALRT,0,0:COMM,0,1 
Label=GND:ARR:1:CALLSIGN,0,0:STAND,0,1 
Label=GND:ARR:2:ATYP,0,0:WTC,0,1,0
Label=GND:ARR:3:RMK,0,1 

Label=GND:DEP:0:ALRT,0,0:ASSR_E,0,1:COMM,0,1 
Label=GND:DEP:1:CALLSIGN,0,0:DRWY,0,1,1 
Label=GND:DEP:2:ATYP,0,0:WTC,0,1,0
Label=GND:DEP:3:DEP,0,0:GS,2,1,0:RMK,0,1 

Label=TWR:ARR:0:ALRT,0,0:COMM,0,1 
Label=TWR:ARR:1:CALLSIGN,0,0:ARWY,0,1 
Label=TWR:ARR:2:AFL+VS,0,1,20:GS,0,1
Label=TWR:ARR:3:ATYP,0,0:RMK,0,1 

Label=TWR:DEP:0:ALRT,0,0:COMM,0,1 
Label=TWR:DEP:1:CALLSIGN,0,0:ATYP,0,1
Label=TWR:DEP:2:AFL+VS,0,1,20:GS,0,1
Label=TWR:DEP:3:DEP,0,0:RMK,0,1

Label=APP:ARR:0:ALRT,0,0:COMM,0,1
Label=APP:ARR:1:CALLSIGN,0,0
Label=APP:ARR:2:AFL+VS,0,1,20

Label=APP:DEP:0:ALRT,0,0:COMM,0,1
Label=APP:DEP:1:CALLSIGN,0,0
Label=APP:DEP:2:AFL+VS,0,1,20

Label_AFL+VS=1,1,1,1
Label_ARWY=0,0,0
Label_ATYP=0,0,0
Label_DEP=0,1,0
Label_DRWY=0,1,0
Label_RMK=0,1,1
Label_STAND=0,1,0
Label_GS=0,1,1,0
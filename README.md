define LTrigger = XB1_LT;
define RTrigger = XB1_RT; 
define Fire = XB1_RT;
define ADS = XB1_LT;
define PickupB = XB1_X;
define N_Weapon = XB1_RB;
define P_Weapon = XB1_LB;
define Pickaxe = XB1_LS;
define Jump = XB1_A;
define Crouch = XB1_RS;
define Ping = XB1_UP;
define Edit = XB1_Y; 
define Switch = XB1_B;
define Build = XB1_B;           
define Wall = XB1_RT;
define Floor = XB1_RB;
define Ramp = XB1_LT;
define Cone = XB1_LB;
define Select = XB1_RT;
define Confirm = XB1_LB;
define Reset = XB1_RS;

define Up = XB1_UP; 
define Down = XB1_DOWN; 
define Left = XB1_LEFT; 
define Right = XB1_RIGHT;
define RX = XB1_RX;   
define RY = XB1_RY;   
define LX = XB1_LX;   
define LY = XB1_LY;  

define PY = POLAR_RY;
define PX = POLAR_RX;
define PS = POLAR_RS;
define On = TRUE;
define Off = FALSE;
define ON = TRUE;
define OFF = FALSE;

int Modswitch;

int StickyAA = On; 
int StickyAAHipFire = On;
int PolarAA = On; 
int PolarTimed = On; 
int PolarHipFire = On; 
int AntiRecoil = Off;
int AntiRecoilHipFire = Off;
int AntiRecoilTimed = Off;
int Headshot = On;
int HeadshotHipFire = On;

int BuildTracker = Off;
int BuilderPro = Off;
int PS5 = Off;
int bunnyhop = Off;
int InstantReset = Off; 
int PickupM = Off;
int InstantResetDelay = 20; 
define InstantResetB = PS4_CROSS;
define pickupmacrobutton = XB1_X;

int PolarPower = 1.99;
int PolarTime = 1000; 

int ConsoleV = 10; 
int ConsoleH = 10;
int ConsoleL = 22;
int StickyAATime = 900;
int ConsoleDelay = 10;


int AntiRecoilPower = 40; 
int AntiRecoilVertical = 54; 
int AntiRecoilTime = 80;



int LessInputDelay = Off;
int InstantTriggers = On;
define InputDelay = 5; 
int BuildSyncTime = 100;

define YCX  = 5;define YCY  = 6;define YCX2 = 4;define YCY2 = 4;define YCX3 = 3;define YCY3 = 4;define YCX4 = 3;define YCY4 = 5;
																																																										int BraveAimAutoConfirm = Off; int BraveAimAutoReset = Off;  
																																																										const string TextLineName []  = {"CoffeCat,""}; const string TextLine1 []  = {"Discord.GG/",""}; const string TextLine2 [] = {"BraveAim! Join",""}; const string TextLine4 [] = {"Twitter @BraveZenScripts",""};const string TextLine3 [] = {"For Best Scripts!",""}; 
																																																										define BACAPX  = YCX; define BACAPY  = YCY; define BACAPX2 = YCX2; define BACAPY2 = YCY2; define BACAPX3 = YCX3; define BACAPY3 = YCY3; define BACAPX4 = YCX4; define BACAPY4 = YCY4;  define BARRHP = 2;define BAHHAP = 2;int Nine,Ten,Cos,Sin,PolarSD,BraveAimStrafe,InputTime,AxisR,AV,AH,ARV,ARH,BT,BC,Y1,Y2,YS,BS,T,A,CA,SA,X,Y,M,MM; int inc = 1, dec, color[3];  define BA = On;int BAT = 4; int BAS = On; define BAPD = 1; int BACAD = 10; int BACA2D = 8; int BACA3D = 16; int BACA4D = 12; int BHFRR = On; int BAPS = 32767; int BAPP = 32767; int BraveAimAARX = 6;int BraveAimAALX = 6;int BraveAimAA1 = 3;int BraveAimAABooster5 = 3;int BraveAimAA3 = 3;int BraveAimAARelease = 5;

define  LSDeadZone = 10;

int     BraveAimTouchPadFix          = FALSE;
int     BraveAimHeadLock             = TRUE;
int     BraveAimHeadAssist           = TRUE;
int     BraveAimMagnet               = TRUE;
int     BraveAimPickUpMacro          = FALSE;
int     BraveAimAA                   = TRUE;
int     BraveAimCA                   = TRUE;
define  BraveAimHeadAssistPower      = 0;
define  BraveAimHeadShotAssistPower  = -4;
define  BraveAimStickyRange          = 12;
define  BraveAimStickyRangeSpeed     = 36;

int BRAV = 10;
int K    = 10:




define  Stair = XB1_LT;  

define  Trap = XB1_X;




define  Pickup = XB1_X; 
define BraveAimResetMacro = XB1_RS;





define Assist_Fire_Exploit = FALSE;

int Fire_Assist_Strength= 90; 
int LinearAA = Off;  
int LinearHipFire = Off; 



int BloomReducer = On;  



int TouchPad = Off;  

define LinearPower = 2.4;  
define AntiRecoilStrength = 10;   
define AntiRecoilDisplacement =  15;   
define HeadshotMax = 60;  
define HeadshotSteps = 40;  


int BloomRTime = 60;


 
main{ if (InstantReset) { if (event_press(InstantResetB)) { combo_run(FastReset); } } if(PS5) { swap(PS4_SHARE, PS4_TOUCH) } block_rumble(); if(LessInputDelay) { VM(InputDelay); } if (BuilderPro) { if (get_ival(Switch)) { BuildPro = On; if (BuildTracker) BuildTrack = On; } if (BuildPro && event_release(Switch)) { combo_run(BuildPro); BuildPro = Off; if (BuildTracker) BuildTrack = Off; } }if (BuildTracker) { if (event_press(Build)) { BuildTrack = !BuildTrack; } if (BuildTrack && !BuildPro) { BuildCount += get_rtime(); if (event_press(Pickaxe) || BuildCount == BuildSyncccTime) { BuildTrack = Off; BuildCount = 0; } if (get_ival(Cone) || get_ival(Floor) || get_ival(Ramp) || get_ival(Wall)) BuildCount = 0; } } 
if (InstantTriggers) {deadzone(LTrigger, RTrigger,100 ,100) } if (!BuildTrack) if (StickyAA){ if ((get_ival(ADS)) || (get_ival(Fire) && StickyAAHipFire)) { if (abs(get_ival(RX)) <= StickyAATime && abs(get_ival(RY)) <= StickyAATime) { combo_run(Sticky); } } else { combo_stop(Sticky); } } { if (Headshot) { if (get_ival(ADS) && get_ival(Fire) || StickyAAHipFire && get_ival(Fire)) { if (abs(get_ival(RY)) < HeadshotMax) { Head += HeadshotSteps; combo_run(HeadshotS); } } if (!get_ival(Fire)) Head = 0; if (Head >= HeadshotMax) combo_stop(HeadshotS); } if (AntiRecoil) { if (get_ival(ADS) >= 95 && get_ival(Fire) || (AntiRecoilHipFire && get_ival(Fire))) { TimeValue += get_rtime(); if (TimeValue > 30) { AxisLY = get_lval(RY); AxisCY = get_ival(RY); } if (abs(AxisCY) != abs(AxisLY)) BoostAR = ((AxisCY - AxisLY) * 4); if ((BoostAR != 0) && (TimeValue > 40)) { BoostAR = 0; TimeValue = 0; } if (AntiRecoilTimed) { RecoilTimer += get_rtime(); if (RecoilTimer > AntiRecoilTime) { ARValue = AntiRecoilPower; RecoilTimer = 0; } else { ARValue = 0; } } AROutPut = (AntiRecoilVertical + ARValue + BoostAR); Set_Val(RY,AROutPut); } if (!get_ival(Fire)) { RecoilTimer = 0; TimeValue = 0; BoostAR = 0; } } if (PolarAA) { if (PolarTimed) { if (get_ival(ADS) && get_ptime(ADS) <= PolarTime || PolarHipFire && get_ival(Fire) && get_ptime(Fire) <= PolarTime) { AimAssist(); 
} } else if (get_ival(ADS)|| PolarHipFire && get_ival(Fire)) { AimAssist(); } if (!get_ival(ADS) && !get_ival(Fire)) { AAT = 0; Axis = 0; } } } 
 vm_tctrl(-9);
block_rumble();
deadzone(XB1_LT,XB1_RT,100,100);
if (BraveAimTouchPadFix) { swap(PS4_SHARE, PS4_TOUCH); }
if (BraveAimAutoReset && !get_ival(ADS) && event_press(BraveAimResetMacro)) { BS = BraveAimResetMacro;combo_run(BraveAimResetMacro); } if (BraveAimAutoConfirm) {if (BA && get_ival(Edit) && get_ptime(Edit) > BAT || !BA && event_press(Edit)) { Y1 = On; Y2 = On; BT = On; } if (Y2) { if (event_release(Select)) {  Y1 = Off;Y2 = Off;BT = Off; }}}if (Y1 || Y2) {if (BAS) { }if (event_press(Reset)) { combo_run (BraveAimResetConfirm);Y1 = Off;Y2 = Off; }if (event_press(Pickaxe) || event_press(Build) || event_press(ADS)) { Y1 = Off; Y2 = Off;BT = Off; }}
if (BuildTracker) {if(event_press(Build)) {BT = !BT;}if(BT) {BC += get_rtime();if(event_press(Pickaxe) || BC == BuildSyncTime) {BT = Off;BC = 0;}if(get_ival(Wall) || get_ival(Stair) || get_ival(Floor) || get_ival(Cone) || get_ival(Build)) {BC = 0;}}}
if (!BT) {
if (BraveAimHeadAssist) { if(get_ival(ADS) && get_ival(Fire) || BHFRR && get_ival(Fire)) { combo_run(BraveAimHeadAssist); } } combo_run (BraveAimRBGFlow);
if (BraveAimMagnet) { if(get_ival(Fire)) { combo_run(BraveAimMagnet); } }
if (BraveAimPickUpMacro && get_val(Pickup)) { combo_run(BraveAimPickUpMacro); } 
if (BraveAimCA) {combo_run(BraveAimConstantAimBooster1);combo_run(BraveAimConstantAimBooster2);combo_run(BraveAimConstantAimBooster3);combo_run(BraveAimConstantAimBooster4);} InputTime += get_rtime();
if (BraveAimAA) {X = get_val(RX);Y = get_val(RY);M = isqrt(pow(X, 2) + pow(Y, 2)); MM = (M < 100);if(!(T++ % BAPD)){A += BraveAimStickyRangeSpeed;}A = A % 360; SA = BraveAimData[A % 360]; CA = BraveAimData[(A + 270) % 360];CA = (CA * BraveAimStickyRange) / 100;SA = (SA * BraveAimStickyRange) / 100;if((get_val(ADS)) || get_val(Fire)) { if(M <= BraveAimStickyRange){SA -= Y;CA -= X;}else {SA = (SA * (200 - ((abs(Y) + M) / 10) * 10) / 200) * MM;CA = (CA * (200 - ((abs(X) + M) / 10) * 10) / 200) * MM;} set_val(RX, clamp(X + CA, -100, 100));set_val(RY, clamp(Y + SA, -100, 100));}}
combo_run(BraveAimAABooster1);if (get_val(RX)<-BraveAimAA1||get_val(RX)>BraveAimAA1||get_val(RY)<-BraveAimAA1||get_val(RY)>BraveAimAA1||get_val(RX)<-BraveAimAA1||get_val(RX)>BraveAimAA1||get_val(RY)<-BraveAimAA1||get_val(RY)>BraveAimAA1){combo_stop(BraveAimAABooster1);}BraveAimStrafe = (isqrt(pow(get_ival(PS4_RX), 2) + pow(get_ival(PS4_RY), 2)));combo_run(BraveAimAABooster2);combo_run(BraveAimAABooster5);combo_run(BraveAimStrafe);combo_run(BraveAimAABooster4);AxisR  = isqrt(abs(event_press(RX)) * abs(event_press(RX)) + abs(event_press(RY)) * abs(event_press(RY)));if (event_press(RX) || event_press(RY) && event_press(RY) && AxisR <= BraveAimAARelease || event_press(RY) && AxisR > BraveAimAARelease) {combo_run(BraveAimAABooster3);}
if (BraveAimHeadLock) {if (get_val(ADS) && (get_val(Fire))) {combo_run(BraveAimHeadLock); } if(abs(get_val(XB1_LX)) > LSDeadZone || abs(get_val(XB1_LY)) > LSDeadZone){ combo_stop(BraveAimHeadLock); } }
}
combo_run(B)
combo_run(R)
combo_run(A)
combo_run(V)


if (Assist_Fire_Exploit) {
if (get_ival(Fire)) {
if (abs(get_ival(PS4_LX)) <= 40 && abs(get_ival(PS4_LZ)) <= 35) {combo_run(Assist_Fire_Exploit);} else {combo_stop(Assist_Fire_Exploit);}}}
vm_tctrl(-5); block_rumble(); if(LessInputDelay) if(TouchPad) { swap(PS4_TOUCH, PS4_SHARE); } if (InstantTriggers) { deadzone(LTrigger,RTrigger,99,99); }
if (BuildTracker) { if (event_press(Build)) {BuildTrack = !BuildTrack;} if (BuildTrack) {BuildCount += get_rtime();if (event_press(Pickaxe) || BuildCount == BuildSyncTime) {BuildTrack = Off;BuildCount = Off;}if (get_ival(Floor) || get_ival(Cone) || get_ival(Ramp) || get_ival(Wall) || get_ival(Trap)) { BuildCount = Off;}} }
{ if(BloomReducer) { if(get_ival(ADS) && (get_ival(Fire))) { combo_run(AntiBloom); } if(abs(get_ival(LX)) > 40 || abs(get_ival(LY)) > 40) { combo_stop(AntiBloom); } } if (LinearAA) { if (get_ival(ADS) || LinearHipFire && get_ival(Fire)) { AimAssist(); } if (!get_ival(ADS) && !get_ival(Fire)) { AAT = 0; Axis = 0; } } if(AntiRecoil) { if(get_ival(ADS) && get_ival(Fire)) { combo_run(AntiRecoilS); } } if (Headshot) { if (get_ival(ADS) && get_ival(Fire) || HeadshotHipFire && get_ival(Fire)) { if (abs(get_ival(RY)) < HeadshotMax) { Head += HeadshotSteps; combo_run(HeadshotS); } } if (!get_ival(Fire)) Head = 0; if (Head >= HeadshotMax) combo_stop(HeadshotS); } } 

} 


combo BuildPro { set_val(Build,0); wait(50); set_val(Build,100); wait(50); }combo HeadshotS { set_val(RY,inv(Head) + get_val(RY)); }combo ConsoleAAs { set_val(RX, (ConsoleV)); wait(10) set_val(RY, (ConsoleV)); wait(10) set_val(RX, ConsoleV * -1); wait(10) set_val(RY, ConsoleV * -1); wait(10) } function AimAssist() { AAT += get_rtime(); 
if (!Axis) set_Val(RY,AAT * PolarPower / 10); if (Axis == 1) set_Val(RX,AAT * PolarPower / 10); if (Axis == 2) set_Val(RY,inv(AAT * PolarPower / 10)); if (Axis == 3) { set_Val(RX,inv(AAT * PolarPower / 10)); if (AAT > 50) { AAT = 0; Axis = 0; } } else if (AAT > 50) { AAT = 0; Axis += 1; } } combo Sticky { Set_Val(RY,ConsoleV); wait(ConsoleDelay); Set_Val(RX,ConsoleH); if (abs(get_ival(LX)) < 20) Set_Val(LX,ConsoleL); wait(ConsoleDelay); Set_Val(RY,ConsoleV * -1); wait(ConsoleDelay); Set_Val(RX,ConsoleH * -1); if (abs(get_ival(LX)) < 20) Set_Val(LX,ConsoleL * -1); wait(ConsoleDelay); }function VM (f_speed) { if (f_speed == 0) vm_tctrl(-0); else if(f_speed == 1) 
vm_tctrl(-2); else if(f_speed == 2) vm_tctrl(-4); else if(f_speed == 3) vm_tctrl(-6); else if(f_speed == 4) vm_tctrl(-8); else if(f_speed == 5) vm_tctrl(-9); } function set_Val(Input,Output) { set_val(Input,clamp(Output * (100 - abs(get_ival(Input))) / 100 + get_ival(Input),-100,100)); return; } function Set_Val(Input,Output) { set_val(Input,clamp(Output * (100 - abs(get_val(Input))) 
/ 100 + get_val(Input),-100,100)); return; } int BuildTrack, BuildCount, AAT, Axis, TimeValue, AxisLY, AxisCY, ARValue, AROutPut, BoostAR, RecoilTimer, Head,BuildPro;  combo walltake100{ set_val(Fire, 100); 
 set_val(Build, 100);  set_val(Cone, 100);  set_val(Wall, 100); wait(10); set_val(Build, 100); } combo bhop{ set_val(XB1_A,100); wait(1); set_val(XB1_A,0);} combo Pickup { set_val(PickupB,32767); wait(1); set_val(PickupB,0); wait(1); } main { if(bunnyhop){ if(get_val(XB1_A) && get_ptime(XB1_A) > 200){ combo_run(bhop);}} } main {if (PickupM) if (get_val(XB1_B)) { combo_run(Pickup); } else { combo_stop(Pickup); } } combo FastReset { set_val(InstantResetB,1); wait(InstantResetDelay); set_val(Edit,1); wait(InstantResetDelay); set_val(Reset,1); wait(InstantResetDelay); combo_run(Confirm); } combo Confirm { set_val(Confirm,100); wait(100); set_val(Confirm,0); wait(10); set_val(Reset,0); wait(10); } 

combo V{ set_val(LX,BRAV1(LX,BRAV + 1));set_val(LX,BRAV1(LX,BRAV  - 2));set_val(LY,BRAV1(LY,BRAV + 1));set_val(LX,BRAV1(LX,BRAV + 1));set_val(LY,BRAV1(LY,BRAV - 2));set_val(LX,BRAV1(LX,BRAV + 1));set_val(LY,BRAV1(LY,BRAV + 1));}
combo A {set_val(LX,BRAV2(LX,BRAV + 1));set_val(LX,BRAV2(LX,BRAV  - 2));set_val(LY,BRAV2(LY,BRAV + 1));set_val(LX,BRAV2(LX,BRAV + 1));set_val(LY,BRAV2(LY,BRAV - 2));set_val(LX,BRAV2(LX,BRAV + 1));set_val(LY,BRAV2(LY,BRAV + 1));}
combo R {set_val(RX,BRAV3(RX,K + 1));set_val(RX,BRAV3(RX,K  - 2));set_val(RY,BRAV3(RY,K + 1));set_val(RX,BRAV3(RX,K + 1));set_val(RY,BRAV3(RY,K - 2));set_val(RX,BRAV3(RX,K + 1));set_val(RY,BRAV3(RY,K + 1));}
combo B {set_val(RX,BRAV4(RX,K + 1));set_val(RX,BRAV4(RX,K  - 2));set_val(RY,BRAV4(RY,K + 1));set_val(RX,BRAV4(RX,K + 1));set_val(RY,BRAV4(RY,K - 2));set_val(RX,BRAV4(RX,K + 1));set_val(RY,BRAV4(RY,K + 1));}
combo BraveAimRBGFlow { wait(1);set_rgb(color, color[1], color[2]);color[dec] -= 1; color[inc] += 1;if(!color[dec]) { inc = (inc + 1) % 3; dec = (dec + 1) % 3; }}
function center_x(f_chars,f_font) {return (OLED_WIDTH / 2) - ((f_chars * f_font) / 2);} 
combo BraveAimConfirmMacro  { set_val(Confirm,100);wait(10);set_val(Confirm,0);wait(10);}
combo BraveAimResetMacro    { wait(50);set_val(Reset,100); wait(50);combo_run(BraveAimConfirmMacro);}
combo BraveAimResetConfirm  { wait(20);combo_run(BraveAimConfirmMacro);}
combo BraveAimHeadLock  { set_val(XB1_LX,-34); wait(50); set_val(XB1_LY,17); wait(30); set_val(XB1_LX,34); wait(50); set_val(XB1_LY,-17); wait(30); }
combo BraveAimHeadAssist { ARV = get_val(PS4_RY) + BraveAimHeadAssistPower; if(ARV > 100) ARV = 100; if(abs(get_val(PS4_RY)) < abs(BraveAimHeadAssistPower) + 5) set_val(PS4_RY, (ARV)); ARH = get_val(PS4_RX) + BARRHP; if(ARH > 100) ARH = 100; if(abs(get_val(PS4_RX)) < abs(BARRHP) + 5) set_val(PS4_RX, ARH); }
combo BraveAimMagnet { AV = get_val(PS4_RY) + BraveAimHeadShotAssistPower; if(AV > 100) AV = 100; if(abs(get_val(PS4_RY)) < abs(BraveAimHeadShotAssistPower) + 5) set_val(PS4_RY, (AV)); AH = get_val(PS4_RX) + BAHHAP; if(AH > 100) AH = 100; if(abs(get_val(PS4_RX)) < abs(BAHHAP) + 5) set_val(PS4_RX, AH); }
combo BraveAimConstantAimBooster1  { set_val(RY,y_val(RY, BACAPY));wait(BACAD);set_val(RX,x_val(RX, BACAPX));wait(BACAD);set_val(RY,y_val(RY, BACAPY * -1));wait(BACAD);set_val(RX,x_val(RX, BACAPX * -1));wait(BACAD);}
combo BraveAimConstantAimBooster2  { set_val(RY,y_val(RY, BACAPY2));wait(BACA2D);set_val(RX,x_val(RX, BACAPX2));wait(BACA2D);set_val(RY,y_val(RY, BACAPY2 * -1));wait(BACA2D);set_val(RX,x_val(RX, BACAPX2 * -1));wait(BACA2D);}
combo BraveAimConstantAimBooster3  { set_val(RY,y_val(RY, BACAPY3));wait(BACA3D);set_val(RX,x_val(RX, BACAPX3));wait(BACA3D);set_val(RY,y_val(RY, BACAPY3 * -1));wait(BACA3D);set_val(RX,x_val(RX, BACAPX3 * -1));wait(BACA3D);}
combo BraveAimConstantAimBooster4  { set_val(RY,y_val(RY, BACAPY4));wait(BACA4D);set_val(RX,x_val(RX, BACAPX4));wait(BACA4D);set_val(RY,y_val(RY, BACAPY4 * -1));wait(BACA4D);set_val(RX,x_val(RX, BACAPX4 * -1));wait(BACA4D);}
combo BraveAimPickUpMacro          { set_val(Pickup, 100); wait(1);set_val(Pickup, 0);wait(1);}
const int16 BraveAimData[] = {100,100,100,100,100,100,100,100,99,99,99,99,98,98,97,97,97,96,95,95,94,94,93,92,92,91,90,89,89,88,87,86,85,84,83,82,81,80,79,78,77,75,74,73,72,71,70,69,67,66,65,63,62,61,59,58,56,55,53,52,50,49,47,46,44,43,41,40,38,36,35,33,31,30,28,26,25,23,21,20,18,16,14,13,11,9,7,6,4,2,0,-1,-3,-5,-7,-8,-10,-12,-13,-15,-17,-19,-20,-22,-24,-25,-27,-29,-30,-32,-34,-35,-37,-39,-40,-42,-43,-45,-46,-48,-50,-51,-53,-54,-55,-57,-58,-60,-61,-62,-64,-65,-66,-68,-69,-70,-71,-73,-74,-75,-76,-77,-78,-79,-80,-81,-82,-83,-84,-85,-86,-87,-88,-89,-89,-90,-91,-92,-92,-93,-93,-94,-95,-95,-96,-96,-97,-97,-97,-98,-98,-99,-99,-99,-99,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-99,-99,-99,-98,-98,-98,-97,-97,-96,-96,-95,-94,-94,-93,-93,-92,-91,-90,-90,-89,-88,-87,-86,-85,-84,-83,-82,-81,-80,-79,-78,-77,-76,-75,-74,-72,-71,-70,-69,-67,-66,-65,-63,-62,-61,-59,-58,-56,-55,-53,-52,-50,-49,-47,-46,-44,-43,-41,-40,-38,-36,-35,-33,-31,-30,-28,-26,-25,-23,-21,-20,-18,-16,-14,-13,-11,-9,-7,-6,-4,-2,0,2,4,6,7,9,11,13,14,16,18,20,21,23,25,26,28,30,31,33,35,36,38,40,41,43,44,46,47,49,51,52,54,55,56,58,59,61,62,63,65,66,67,69,70,70,72,73,74,75,77,78,79,80,81,82,83,84,85,86,87,88,89,89,90,91,92,92,93,94,94,95,95,96,97,97,97,98,98,99,99,99,99,100,100,100,100,100,100,100};
function x_val(f_axis,f_val) {if(abs(get_val(f_axis)) < (BACAPX + 1))  return f_val;return get_val(f_axis);}
function y_val(f_axis,f_val) {if(abs(get_val(f_axis)) < (BACAPY + 1))  return f_val;return get_val(f_axis);}
combo BraveAimAABooster1 {set_val(RY, (BraveAimAA1));wait(1)set_val(RX, (BraveAimAA1));wait(1)set_val(RY, (-BraveAimAA1));wait(1)set_val(RX, (-BraveAimAA1));wait(1)set_val(RY, (BraveAimAA1));wait(1)set_val(RX, (BraveAimAA1));wait(1)set_val(RY, (-BraveAimAA1));wait(1)set_val(RX, (-BraveAimAA1));wait(1);}	
combo BraveAimAABooster2 {BraveAimAABooster5 = random(-1, 1)set_val(RY,  get_ival (RY)  + BraveAimAABooster5);wait(2);set_val(RX, get_ival (RX)+ BraveAimAABooster5);set_val(LX, get_ival (LX)+ BraveAimAABooster5);wait(2);set_val(RY, get_ival(RY)+ BraveAimAABooster5*-1);wait(2);set_val(RX, get_ival (RX)  + BraveAimAABooster5*-1);set_val(LX, get_ival (LX) + BraveAimAABooster5*-1);wait(2);}
combo BraveAimAABooster3 {offset(RX,BraveAimAA3);offset(RY,BraveAimAA3);wait(6);offset(RX,BraveAimAA3 * -1);offset(RY,BraveAimAA3 * -1);wait(6);}	
combo BraveAimAABooster4{if(!(InputTime++ % 4))BraveAimSP(POLAR_RS, PolarSD = (PolarSD + BAPS) % 360, BAPP * 359);InputTime = 0;}
combo BraveAimAABooster5 {set_val(RX, SetVal(RX,BraveAimAARX + 1));wait (3);set_val(RX,SetVal(RX,BraveAimAARX - 1));wait (3);}
combo BraveAimStrafe {set_val(LX, SetVal(LX,BraveAimAALX + 1));wait (3);set_val(LX, SetVal(LX,BraveAimAALX - 1));wait (3);}	
function SetVal(Axis1 , Value1) {if(abs(get_val(Axis1)) < (BraveAimAARX - 1))  return Value1;return get_val(Axis1);}
function offset(int axis, int offset_val) {set_val(axis, clamp(offset_val * (100 - abs(get_val(axis))) / 100 + get_val(axis), -100, 100));return}
function BraveAimSP(Axis, bRave, Axis5){Nine = 9 + Axis;Ten = 10 + Axis;if(bRave < 0) bRave = 360 + (bRave % 360);bRave = (bRave + 90) % 360;Axis5 = clamp(Axis5, 0, 100);Sin = BraveAimData[bRave];Cos = BraveAimData[(bRave + 90) % 360];offset(Nine, inv(Axis5 * Cos / 100));offset(Ten, inv(Axis5 * Sin / 100))return;}
function BRAV3(BRAVAIMBOT,SOFTAIM) {if(abs(get_val(BRAVAIMBOT)) < (K  - 1))  return SOFTAIM;return get_val(BRAVAIMBOT);}
function BRAV2(BRAVAIMBOT,SOFTAIM) {if(abs(get_val(BRAVAIMBOT)) < (BRAV  - 1))  return SOFTAIM;return get_val(BRAVAIMBOT);}
function BRAV4(BRAVAIMBOT,SOFTAIM) {if(abs(get_val(BRAVAIMBOT)) < (K + 1))  return SOFTAIM;return get_val(BRAVAIMBOT);}
function BRAV1(BRAVAIMBOT,SOFTAIM) {if(abs(get_val(BRAVAIMBOT)) < (BRAV + 1))  return SOFTAIM;return get_val(BRAVAIMBOT);}

 


combo AntiBloom { set_val(LX,-40); wait(BloomRTime); set_val(LX, 40); wait(BloomRTime); if(BloomRTime < 160){BloomRTime = BloomRTime + 10;} else {BloomRTime = 100; } } combo AntiRecoilS { AntiRecoilVert = get_val(RY) + AntiRecoilStrength; if(AntiRecoilVert > 100) AntiRecoilVert = 100; if(abs(get_val(RY)) < abs(AntiRecoilStrength) + 5) set_val(RY, (AntiRecoilVert)); AntiRecoilHoriz = get_val(RX) + AntiRecoilDisplacement; if(AntiRecoilHoriz > 100) AntiRecoilHoriz = 100; if(abs(get_val(RX)) < abs(AntiRecoilDisplacement) + 5) set_val(RX, AntiRecoilHoriz); } 



const char Polar_Array[]={100,100,100,100,100,100,100,100,99,99,99,99,98,98,97,97,97,96,95,95,94,94,93,92,92,91,90,89,89,88,87,86,85,84,83,82,81,80,79,78,77,75,74,73,72,71,70,69,67,66,65,63,62,61,59,58,56,55,53,52,50,49,47,46,44,43,41,40,38,36,35,33,31,30,28,26,25,23,21,20,18,16,14,13,11,9,7,6,4,2,0,-1,-3,-5,-7,-8,-10,-12,-13,-15,-17,-19,-20,-22,-24,-25,-27,-29,-30,-32,-34,-35,-37,-39,-40,-42,-43,-45,-46,-48,-50,-51,-53,-54,-55,-57,-58,-60,-61,-62,-64,-65,-66,-68,-69,-70,-71,-73,-74,-75,-76,-77,-78,-79,-80,-81,-82,-83,-84,-85,-86,-87,-88,-89,-89,-90,-91,-92,-92,-93,-93,-94,-95,-95,-96,-96,-97,-97,-97,-98,-98,-99,-99,-99,-99,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-100,-99,-99,-99,-98,-98,-98,-97,-97,-96,-96,-95,-94,-94,-93,-93,-92,-91,-90,-90,-89,-88,-87,-86,-85,-84,-83,-82,-81,-80,-79,-78,-77,-76,-75,-74,-72,-71,-70,-69,-67,-66,-65,-63,-62,-61,-59,-58,-56,-55,-53,-52,-50,-49,-47,-46,-44,-43,-41,-40,-38,-36,-35,-33,-31,-30,-28,-26,-25,-23,-21,-20,-18,-16,-14,-13,-11,-9,-7,-6,-4,-2,0,2,4,6,7,9,11,13,14,16,18,20,21,23,25,26,28,30,31,33,35,36,38,40,41,43,44,46,47,49,51,52,54,55,56,58,59,61,62,63,65,66,67,69,70,70,72,73,74,75,77,78,79,80,81,82,83,84,85,86,87,88,89,89,90,91,92,92,93,94,94,95,95,96,97,97,97,98,98,99,99,99,99,100,100,100,100,100,100,100}; int   actual_X, actual_Y, actual_Magnitude, max_Magnitude, time, angle, cos_angle, sin_angle, AntiRecoilVert, AntiRecoilHoriz;
combo Assist_Fire_Exploit {set_val(XB1_LX,-100);wait(Fire_Assist_Strength);set_val(XB1_LX,100);wait(Fire_Assist_Strength);}


define RecoilReducer    	= TRUE;
int RecoilReducerPower 	= 15;
int AntiRecoilTuning = 200;




main {
if (RecoilReducer) { if (get_val (ADS) && get_val (Fire)) { combo_run (RecoilReducer); } } if (RecoilReducer) { if (get_val (ADS) && get_val (Fire)) { combo_run (RecoilReducer); } } if (get_ival (XB1_LB) && get_ptime (XB1_LB) > 350) { Disable(); RecoilReducerPower = ValueChangeRR(RecoilReducerPower, XB1_LEFT, -1); RecoilReducerPower = ValueChangeRR(RecoilReducerPower, XB1_RIGHT, 1); RecoilReducerPower = ValueChangeRR(RecoilReducerPower, XB1_DOWN, -10); RecoilReducerPower = ValueChangeRR(RecoilReducerPower, XB1_UP, 10); }
       
if (AccuracyExploit) 
{
	if (event_press(FireBtn) && !get_ival(HoldButtonStop)) 
    {
         combo_run(Accuracy100);
    }
}

}


function ValueChangeRR (RecoilReducerPower, Input, Tune) { if(Initiate(Input)) { RecoilReducerPower += Tune; if (RecoilReducerPower < inv(AntiRecoilTuning)) { RecoilReducerPower = inv(AntiRecoilTuning); } if(RecoilReducerPower > AntiRecoilTuning) { RecoilReducerPower = AntiRecoilTuning; } } return RecoilReducerPower; }
combo RecoilReducer { set_val (RY, get_ival (RY) + (RecoilReducerPower)); wait(5); }
function Disable () { set_val(XB1_UP, 0); set_val(XB1_DOWN, 0); set_val(XB1_LEFT, 0); set_val(XB1_RIGHT, 0);set_val(XB1_A, 0); set_val(XB1_B, 0);set_val(XB1_X, 0);}
function Initiate (Input) { return event_press(Input) || get_val(Input) && get_ptime(Input) > 250 && get_ptime(Input) % (get_rtime() * 8) == 0; }

int RapidFire                         = FALSE;
int RapidFireDelay                    = 80;
int RapidFireOnButton                 = XB1_RB;
int RapidFireOffButton                = XB1_LB;


main {
if (RapidFire) { if (get_val (RapidFireOnButton) && get_val (XB1_RT)) { combo_run (RapidFireOn); } if (get_val (RapidFireOffButton) && get_val (XB1_RT)) { combo_run (RapidFireOff); } } if ((RapidFireToggle) && get_val (Fire)) { combo_run (RapidFire); } else { combo_stop(RapidFire); }

}

int RapidFireToggle;
 combo RapidFireOn { RapidFireToggle = TRUE; } combo RapidFireOff { RapidFireToggle = FALSE; } combo RapidFire { set_val(Fire, 100); wait(RapidFireDelay); set_val(Fire, 0); wait(RapidFireDelay); set_val(Fire, 0); }
 
 int LED = TRUE;
main {
   
if (LED) { set_rgb (0,0,255) } else { set_rgb (0,0,255) }
}

function Text (Character, Font) { 
return (OLED_WIDTH / 2 + 1) - (( Character * Font) / 2 + 1);
}
init {
cls_oled(1);
print (Text (18, OLED_FONT_SMALL_WIDTH), 3 , OLED_FONT_SMALL,OLED_BLACK, T1 [0]);
print (Text (18, OLED_FONT_SMALL_WIDTH), 15, OLED_FONT_SMALL,OLED_BLACK, T2 [0]);
print (Text (18, OLED_FONT_SMALL_WIDTH), 26, OLED_FONT_SMALL,OLED_BLACK, T3 [0]);
print (Text (18, OLED_FONT_SMALL_WIDTH), 38, OLED_FONT_SMALL,OLED_BLACK, T4 [0]);
print (Text (18, OLED_FONT_SMALL_WIDTH), 50, OLED_FONT_SMALL,OLED_BLACK, T5 [0]);
}
const string T1[]={" WelshArab ",""}
const string T2[]={" ArabZens",""}
const string T3[]={" ""}
const string T4[]={" ",""}
const string T5[]={" Carca      A13",""}

int AccuracyExploit   = FALSE;
define FireBtn    = XB1_RT; 
define AdsBtn = XB1_LT;

define HoldButtonStop  = PS4_R3;

//A13

main {
       
if (AccuracyExploit) 
{
	if (event_press(FireBtn) && !get_ival(HoldButtonStop)) 
    {
         combo_run(Accuracy100);
    }
}
}
int Spam_Accuracy:

combo Accuracy100 
{
    set_val(AdsBtn,100);
    wait(Spam_Accuracy);
}

init {
Spam_Accuracy       = get_pvar(SPVAR_14, 50, 100, 100);}
  ����������������

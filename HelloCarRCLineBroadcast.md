
```
//Notify that a object is part of a tag group
// STAG is an append and can be done in several pieces.
// S set the tag to given,   A Append the tag,     R Remove tag of group
// TAG Won't be use a variable that need to change oftne but can be use to manage state as ALIVE DISABLE 
// NO SPACE IN TAG, You can use '_' LEVEL_1 if you need
nPJfL0:STAG:S:BALL TEAMBLUE 
ldsjfl:STAG:S:DRONE PLAYER ALIVE 
ldsjfl:STAG:A:FLYING INDEX2 TEAMBLUE
ldsjfl:STAG:R:ALIVE



// Blade information
// Percent 0-1 of the blade speed percent
//2400 Is the max angle rotation speed of the blade
ldsjfl:SAA0:C: 1 1 1 1 2400

// Car wheel information
// 33 angle lt, rt, lb,rb, of the wheel as clock type 0-360
// 240 rotation angle per second 0 = motor off
// 33 is the exact angle when 240 is to interpolate rotation.
ldsjfl:SAA1:D: 33 33 33 33| 240 240 240 240




// Loaded scene name
G:METAINFORMATION

// Given Key value maybe useful to the player
GKV:Key:Value
// What is the scene of the game
GKV:SCENE:BATTLEARENA
// How many player are in game
GKV:PLAYERCOUNT:12
// Is the game considered as official
GKV:OFFICIALMATCH:False

// You can only play if you are identify with a private key message (see future doc)
GKV:CRYPTOKEYONLY:False

GKV:MATCHTYPE: LUABATTLE  // The match is offline with LUA script loaded
GKV:MATCHTYPE: RASPBERRYBATTLE  // The match is offline with script running on raspberry pi
GKV:MATCHTYPE: WEBDEVOFFLINEBATTLE  // The match is offline with script running on webpage
GKV:MATCHTYPE: WEBDEVONLINEBATTLE  // The match is offline with script running on webpage on the web
GKV:MATCHTYPE: TWITCHPLAYBATTLE  // Any one can play the current game
GKV:MATCHTYPE: MATCHBATTLE  // Interaction only for accepted player


SL: Server Log Message to the player
AL: Admin Message to the player
DL: Developer Message to the player
CL: Community Message to the player
SLID:1  Server Id of prerecored message
ALID:53 Admin Id of prerecored message
DLID:75 Developer Id of prerecored message
CLID:89 Community Id of prerecored message


// Group of id element in game
nPJfL0:SIDS:532de1f9-a8ef-47b1-bc2f-f7e07f03490c:Red Car 0:-54678

// Start sending information to the players
START

// Stop sending information to the players
STOP

TIME:DateTime.Now() Tick
TIME:

// Position
// t = euleur rotation, T = Quaternion rotation
nPJfL0:t:Vx Vy Vz|Ex Ey Ez 
nPJfL0:T:Vx Vy Vz|Qx Qy Qz Qw

// SXXX for Status S for status XXX for format id.
// TB:: for Trigger Broadcast
// TB:ID: for Trigger Broadcast by an item.
// GXXX information on the game state

// Match State
G:SAAA:SetBlue SetRed  PointBlue  PointRed

// Trigger broadcast are information that are useful but not necessary to the game
TB::Game Started
TB::Game Terminated
// If an id is given it is linked on this element.
TB:nPJfL0:Car death

// A new elemented had be created
TB:nPJfL0:Created

// A elemented had be removed
TB:nPJfL0:Destroyed


// Log broadcast
// Just use for developer to log the game
// Disable during official game
LB: I am a log message.



ID:StatusInfo: Format  based on status info
ID:S

// Basic shape
// {0} (D) drone   (C) Car
nPJfL0:SAAB: C Horizontal Heihgt  Depth
nPJfL0:SAAB: D Radius

//// Complex Shape Drone

// ID of the skin to use from the Munity DB
nPJfL0:S3DM: 8668c072-6974-45ff-abff-50976fa9cd14

// If lua battle, id of the lua code use for the element
nPJfL0:SLUA: 8668c072-6974-45ff-abff-50976fa9cd14


ID:SBBC:C:-0.1486 -0.0001 0.0990|0.1486 0.0000 0.0990|-0.1486 -0.0001 -0.0990|0.1486 0.0000 -0.0990|0.2139097|0.4046267|0.0000 0.0000 0.0000|0.177476|0.3711486|0.3608634|0.0000 0.0000 0.0000|0.1299788|0.188309|0.2907836
nPJfL0:SBBC:C:
Vector3 m_wheelOffsetFrontLeft;
|Vector3 m_wheelOffsetFrontRight;
|Vector3 m_wheelOffsetBackLeft;
|Vector3 m_wheelOffsetBackRight;
|float m_radiusOfWheels;
|float m_heightOfWheels;
|Vector3 m_boxCarColliderOffset;
|float m_heightOfCarCollider;
|float m_widthOfCarCollider;
|float m_depthOfCarCollider;
|Vector3 m_boxCarBodyColliderOffset;
|float m_heightOfCarBodyCollider;
|float m_widthOfCarBodyCollider;
|float m_depthOfCarBodyCollider;nPJfL0:SAAC: D Radius


ID:SBBC:D:-0.0586 0.0135 0.0471|0.0566 0.0135 0.0468|-0.0586 0.0135 -0.0407|0.0566 0.0135 -0.0410|0.03835154|0.01718658|0.0000 0.0000 0.0000|0.0637337|0.1857896|0.1997235
nPJfL0:SBBC:D:
Vector3 m_bladeOffsetFrontLeft;
|Vector3 m_bladeOffsetFrontRight;
|Vector3 m_bladeOffsetBackLeft;
|Vector3 m_bladeOffsetBackRight;

|float m_radiusOfBlade;
|float m_heightOfBlade;

|Vector3 m_boxColliderOffset;
|float   m_heightOfBoxCollider;
|float   m_widthOfBoxCollider;
|float   m_depthOfBoxCollider;


//Give meta information that can be usefull as Key value info. Dynamic list.
ID:SKVS:KEY:VALUE

//TO ADD
// Player COLOR RGBA
string.Format($"{id}:SCOL:P:{ColFF(r)}{ColFF(g)}{ColFF(b)}{ColFF(a)}") 
nPJfL0:SKVS:CP:FF00FFFF
// Team COLOR RGBA
string.Format($"{id}:SCOL:P:{ColFF(r)}{ColFF(g)}{ColFF(b)}{ColFF(a)}") 
nPJfL0:SKVS:CT:FF0010FF

```



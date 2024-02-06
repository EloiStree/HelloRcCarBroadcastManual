
```
// Group of id element in game
nPJfL0:SIDS:532de1f9-a8ef-47b1-bc2f-f7e07f03490c:Red Car 0:-54678


Time:DateTime.Now() Tick

// Position
// t = euleur rotation, T = Quaternion rotation
nPJfL0:t:Vx Vy Vz Ex Ey Ez 
nPJfL0:T:Vx Vy Vz Qx Qy Qz Qw

// S for Status
// TB for Trigger Broadcast

// Match State  
nPJfL0:SAAA:SetBlue SetRed  PointBlue  PointRed

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


nPJfL0:SBBC: C {Complex shape}
|Vector3 m_wheelOffsetFrontLeft;
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



nPJfL0:SBBC: C {Complex shape}
|Vector3 m_bladeOffsetFrontLeft;
|Vector3 m_bladeOffsetFrontRight;
|Vector3 m_bladeOffsetBackLeft;
|Vector3 m_bladeOffsetBackRight;

|float m_radiusOfBlade;
|float m_heightOfBlade;

|Vector3 m_boxColliderOffset;
|float   m_heightOfBoxCollider;
|float   m_widthOfBoxCollider;
|float   m_depthOfBoxCollider;


```



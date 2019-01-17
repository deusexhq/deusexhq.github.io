#Actor
`abstract, native, nativereplication`
	
```
Actor: The base class of all actors.
This is a built-in Unreal class and it shouldn't be modified.
```

##Properties

```java
// DEUS_EX STM
enum EAIEventState
{
	EAISTATE_Begin,
	EAISTATE_End,
	EAISTATE_Pulse,
	EAISTATE_ChangeBest
};

enum EAIEventType
{
	EAITYPE_Visual,
	EAITYPE_Audio,
	EAITYPE_Olifactory
};

struct XAIParams
{
	var actor BestActor;
	var float Score;
	var float Visibility;
	var float Volume;
	var float Smell;
};

// DEUS_EX AJY 
enum EBarkModes 
{
	BM_Idle,
	BM_CriticalDamage,
	BM_AreaSecure,
	BM_TargetAcquired,
	BM_TargetLost,
	BM_GoingForAlarm,
	BM_OutOfAmmo,
	BM_Scanning,
	BM_Futz,
	BM_OnFire,
	BM_TearGas,
	BM_Gore,
	BM_Surprise,
	BM_PreAttackSearching,
	BM_PreAttackSighting,
	BM_PostAttackSearching,
	BM_SearchGiveUp,
	BM_AllianceHostile,
	BM_AllianceFriendly
};

// Flags.
var(Advanced) const bool  bStatic;       // Does not move or change over time.
var(Advanced) bool        bHidden;       // Is hidden during gameplay.
var(Advanced) const bool  bNoDelete;     // Cannot be deleted during play.
var bool				  bAnimFinished; // Unlooped animation sequence has finished.
var bool				  bAnimLoop;     // Whether animation is looping.
var bool				  bAnimNotify;   // Whether a notify is applied to the current sequence.
var bool				  bAnimByOwner;	 // Animation dictated by owner.
var const bool            bDeleteMe;     // About to be deleted.
var transient const bool  bAssimilated;  // Actor dynamics are assimilated in world geometry.
var transient const bool  bTicked;       // Actor has been updated.
var transient bool        bLightChanged; // Recalculate this light's lighting now.
var bool                  bDynamicLight; // Temporarily treat this as a dynamic light.
var bool                  bTimerLoop;    // Timer loops (else is one-shot).

// Other flags.
var(Advanced) bool        bCanTeleport;  // This actor can be teleported.
var(Advanced) bool        bIsSecretGoal; // This actor counts in the "secret" total.
var(Advanced) bool        bIsKillGoal;   // This actor counts in the "death" toll.
var(Advanced) bool        bIsItemGoal;   // This actor counts in the "item" count.
var(Advanced) bool		  bCollideWhenPlacing; // This actor collides with the world when placing.
var(Advanced) bool		  bTravel;       // Actor is capable of travelling among servers.
var(Advanced) bool		  bMovable;      // Actor is capable of travelling among servers.
var(Advanced) bool        bHighDetail;	 // Only show up on high-detail.
var(Advanced) bool		  bStasis;		 // In StandAlone games, turn off if not in a recently rendered zone turned off if  bCanStasis  and physics = PHYS_None or PHYS_Rotating.
var(Advanced) bool		  bForceStasis;	 // Force stasis when not recently rendered, even if physics not none or rotating.
var const	  bool		  bIsPawn;		 // True only for pawns.
var(Advanced) const bool  bNetTemporary; // Tear-off simulation in network play.
var(Advanced) const bool  bNetOptional;  // Actor should only be replicated if bandwidth available.
var			  bool		  bReplicateInstigator;	// Replicate instigator to client (used by bNetTemporary projectiles).
var			  bool		  bTrailerSameRotation;	// If PHYS_Trailer and true, have same rotation as owner.
var			  bool		  bTrailerPrePivot;	// If PHYS_Trailer and true, offset from owner by PrePivot.
var			  bool		  bClientAnim;
var			  bool		  bSimFall;			// dumb proxy should simulate fall

// DEUS_EX STM - added new flags
var(Advanced) bool        bBlockSight;   // True if pawns can't see through this actor.
var(Advanced) bool        bDetectable;   // True if this actor can be detected (by sight, sound, etc).
var(Advanced) bool        bTransient;    // True if this actor should be destroyed when it goes into stasis
var           bool        bIgnore;       // True if this actor should be generally ignored; compliance is voluntary

// Priority Parameters
// Actor's current physics mode.
var(Movement) const enum EPhysics
{
	PHYS_None,
	PHYS_Walking,
	PHYS_Falling,
	PHYS_Swimming,
	PHYS_Flying,
	PHYS_Rotating,
	PHYS_Projectile,
	PHYS_Rolling,
	PHYS_Interpolating,
	PHYS_MovingBrush,
	PHYS_Spider,
	PHYS_Trailer
} Physics;

// Net variables.
enum ENetRole
{
	ROLE_None,              // No role at all.
	ROLE_DumbProxy,			// Dumb proxy of this actor.
	ROLE_SimulatedProxy,	// Locally simulated proxy of this actor.
	ROLE_AutonomousProxy,	// Locally autonomous proxy of this actor.
	ROLE_Authority,			// Authoritative control over the actor.
};
var ENetRole Role;
var(Networking) ENetRole RemoteRole;

// DEUS_EX STM - added for stasis
var float LastRenderTime;
var float DistanceFromPlayer;

// Owner.
var         const Actor   Owner;         // Owner actor.
var(Object) name InitialState;
var(Object) name Group;

// Execution and timer variables.
var float                 TimerRate;     // Timer event, 0=no timer.
var const float           TimerCounter;	 // Counts up until it reaches TimerRate.
var(Advanced) float		  LifeSpan;      // How old the object lives before dying, 0=forever.

// Animation variables.
var(Display) name         AnimSequence;  // Animation sequence we're playing.
var(Display) float        AnimFrame;     // Current animation frame, 0.0 to 1.0.
var(Display) float        AnimRate;      // Animation rate in frames per second, 0=none, negative=velocity scaled.
var          float        TweenRate;     // Tween-into rate.

var(Display) float		  LODBias;

// Blending animation variables - DEUS_EX CNN
var name	BlendAnimSequence[4];
var float	BlendAnimFrame[4];
var float	BlendAnimRate[4];
var float	BlendTweenRate[4];

//-----------------------------------------------------------------------------
// Structures.

// Identifies a unique convex volume in the world.
struct PointRegion
{
	var zoneinfo Zone;       // Zone.
	var int      iLeaf;      // Bsp leaf.
	var byte     ZoneNumber; // Zone number.
};

//-----------------------------------------------------------------------------
// Major actor properties.

// Scriptable.
var       const LevelInfo Level;         // Level this actor is on.
var transient const Level XLevel;        // Level object.
var(Events) name		  Tag;			 // Actor's tag name.
var(Events) name          Event;         // The event this actor causes.
var Actor                 Target;        // Actor we're aiming at (other uses as well).
var Pawn                  Instigator;    // Pawn responsible for damage.
var travel Inventory      Inventory;     // Inventory chain.  (DEUS_EX STM - added "travel")
var const Actor           Base;          // Moving brush actor we're standing on.
var const PointRegion     Region;        // Region this actor is in.
var(Movement)	name	  AttachTag;

// Internal.
var const byte            StandingCount; // Count of actors standing on this actor.
var const byte            MiscNumber;    // Internal use.
var const byte            LatentByte;    // Internal latent function use.
var const int             LatentInt;     // Internal latent function use.
var const float           LatentFloat;   // Internal latent function use.
var const actor           LatentActor;   // Internal latent function use.
var const actor           Touching[4];   // List of touching actors.
var const actor           Deleted;       // Next actor in just-deleted chain.

// Internal tags.
var const transient int CollisionTag, LightingTag, NetTag, OtherTag, ExtraTag, SpecialTag;

// The actor's position and rotation.
var(Movement) const vector Location;     // Actor's location; use Move to set.
var(Movement) const rotator Rotation;    // Rotation.
var       const vector    OldLocation;   // Actor's old location one tick ago.
var       const vector    ColLocation;   // Actor's old location one move ago.
var(Movement) vector      Velocity;      // Velocity.
var       vector          Acceleration;  // Acceleration.

//Editing flags
var(Advanced) bool        bHiddenEd;     // Is hidden during editing.
var(Advanced) bool        bDirectional;  // Actor shows direction arrow during editing.
var const bool            bSelected;     // Selected in UnrealEd.
var const bool            bMemorized;    // Remembered in UnrealEd.
var const bool            bHighlighted;  // Highlighted in UnrealEd.
var bool                  bEdLocked;     // Locked in editor (no movement or rotation).
var(Advanced) bool        bEdShouldSnap; // Snap to grid in editor.
var transient bool        bEdSnap;       // Should snap to grid in UnrealEd.
var transient const bool  bTempEditor;   // Internal UnrealEd.

// What kind of gameplay scenarios to appear in.
var(Filter) bool          bDifficulty0;  // Appear in difficulty 0.
var(Filter) bool          bDifficulty1;  // Appear in difficulty 1.
var(Filter) bool          bDifficulty2;  // Appear in difficulty 2.
var(Filter) bool          bDifficulty3;  // Appear in difficulty 3.
var(Filter) bool          bSinglePlayer; // Appear in single player.
var(Filter) bool          bNet;          // Appear in regular network play.
var(Filter) bool          bNetSpecial;   // Appear in special network play mode.
var(Filter) float		  OddsOfAppearing; // 0-1 - chance actor will appear in relevant game modes.

//-----------------------------------------------------------------------------
// Display properties.

// Drawing effect.
var(Display) enum EDrawType
{
	DT_None,
	DT_Sprite,
	DT_Mesh,
	DT_Brush,
	DT_RopeSprite,
	DT_VerticalSprite,
	DT_Terraform,
	DT_SpriteAnimOnce,
} DrawType;

// Style for rendering sprites, meshes.
var(Display) enum ERenderStyle
{
	STY_None,
	STY_Normal,
	STY_Masked,
	STY_Translucent,
	STY_Modulated,
} Style;

// Other display properties.
var(Display) texture    Sprite;			 // Sprite texture if DrawType=DT_Sprite.
var(Display) texture    Texture;		 // Misc texture.
var(Display) texture    Skin;            // Special skin or enviro map texture.
var(Display) mesh       Mesh;            // Mesh if DrawType=DT_Mesh.
var const export model  Brush;           // Brush if DrawType=DT_Brush.
var(Display) float      DrawScale;		 // Scaling factor, 1.0=normal size.
var			 vector		PrePivot;		 // Offset from box center for drawing.
var(Display) float      ScaleGlow;		 // Multiplies lighting.
var(Display) byte       AmbientGlow;     // Ambient brightness, or 255=pulsing.
var(Display) byte       Fatness;         // Fatness (mesh distortion).

// Display.
var(Display)  bool      bUnlit;          // Lights don't affect actor.
var(Display)  bool      bNoSmooth;       // Don't smooth actor's texture.
var(Display)  bool      bParticles;      // Mesh is a particle system.
var(Display)  bool      bRandomFrame;    // Particles use a random texture from among the default texture and the multiskins textures
var(Display)  bool      bMeshEnviroMap;  // Environment-map the mesh.
var(Display)  bool      bMeshCurvy;      // Curvy mesh.
var(Display)  float     VisibilityRadius;// Actor is drawn if viewer is within its visibility
var(Display)  float     VisibilityHeight;// cylinder.  Zero=infinite visibility.

// Not yet implemented.
var(Display) bool       bShadowCast;     // Casts shadows.

// Advanced.
var(Advanced) bool		bOwnerNoSee;	 // Everything but the owner can see this actor.
var(Advanced) bool      bOnlyOwnerSee;   // Only owner can see this actor.
var Const     bool		bIsMover;		 // Is a mover.
var(Advanced) bool		bAlwaysRelevant; // Always relevant for network.
var Const	  bool		bAlwaysTick;     // Update even when players-only.
var			  bool		bHurtEntry;	     // keep HurtRadius from being reentrant
var(Advanced) bool		bGameRelevant;	 // Always relevant for game
var			  bool		bCarriedItem;	 // being carried, and not responsible for displaying self, so don't replicated location and rotation
var			  bool		bForcePhysicsUpdate; // force a physics update for simulated pawns


// Multiple skin support.
var(Display) texture MultiSkins[8];

//-----------------------------------------------------------------------------
// Sound.

// Ambient sound.
var(Sound) byte         SoundRadius;	 // Radius of ambient sound.
var(Sound) byte         SoundVolume;	 // Volume of amient sound.
var(Sound) byte         SoundPitch;	     // Sound pitch shift, 64.0=none.
var(Sound) sound        AmbientSound;    // Ambient sound effect.

// Regular sounds.
var(Sound) float TransientSoundVolume;
var(Sound) float TransientSoundRadius;

// Sound slots for actors.
enum ESoundSlot
{
	SLOT_None,
	SLOT_Misc,
	SLOT_Pain,
	SLOT_Interact,
	SLOT_Ambient,
	SLOT_Talk,
	SLOT_Interface,
};

// Music transitions.
enum EMusicTransition
{
	MTRAN_None,
	MTRAN_Instant,
	MTRAN_Segue,
	MTRAN_Fade,
	MTRAN_FastFade,
	MTRAN_SlowFade,
};

//-----------------------------------------------------------------------------
// Collision.

// Collision size.
var(Collision) const float CollisionRadius; // Radius of collision cyllinder.
var(Collision) const float CollisionHeight; // Half-height cyllinder.

// Collision flags.
var(Collision) const bool bCollideActors;   // Collides with other actors.
var(Collision) bool       bCollideWorld;    // Collides with the world.
var(Collision) bool       bBlockActors;	    // Blocks other nonplayer actors.
var(Collision) bool       bBlockPlayers;    // Blocks other player actors.
var(Collision) bool       bProjTarget;      // Projectiles should potentially target this actor.

//-----------------------------------------------------------------------------
// Lighting.

// Light modulation.
var(Lighting) enum ELightType
{
	LT_None,
	LT_Steady,
	LT_Pulse,
	LT_Blink,
	LT_Flicker,
	LT_Strobe,
	LT_BackdropLight,
	LT_SubtlePulse,
	LT_TexturePaletteOnce,
	LT_TexturePaletteLoop
} LightType;

// Spatial light effect to use.
var(Lighting) enum ELightEffect
{
	LE_None,
	LE_TorchWaver,
	LE_FireWaver,
	LE_WateryShimmer,
	LE_Searchlight,
	LE_SlowWave,
	LE_FastWave,
	LE_CloudCast,
	LE_StaticSpot,
	LE_Shock,
	LE_Disco,
	LE_Warp,
	LE_Spotlight,
	LE_NonIncidence,
	LE_Shell,
	LE_OmniBumpMap,
	LE_Interference,
	LE_Cylinder,
	LE_Rotor,
	LE_Unused
} LightEffect;

// Lighting info.
var(LightColor) byte
	LightBrightness,
	LightHue,
	LightSaturation;

// Light properties.
var(Lighting) byte
	LightRadius,
	LightPeriod,
	LightPhase,
	LightCone,
	VolumeBrightness,
	VolumeRadius,
	VolumeFog;

// Lighting.
var(Lighting) bool	     bSpecialLit;	 // Only affects special-lit surfaces.
var(Lighting) bool	     bActorShadows;  // Light casts actor shadows.
var(Lighting) bool	     bCorona;        // Light uses Skin as a corona.
var(Lighting) bool	     bLensFlare;     // Whether to use zone lens flare.

//-----------------------------------------------------------------------------
// Physics.

// Options.
var(Movement) bool        bBounce;           // Bounces when hits ground fast.
var(Movement) bool		  bFixedRotationDir; // Fixed direction of rotation.
var(Movement) bool		  bRotateToDesired;  // Rotate to DesiredRotation.
var           bool        bInterpolating;    // Performing interpolating.
var			  const bool  bJustTeleported;   // Used by engine physics - not valid for scripts.

// Dodge move direction.
var enum EDodgeDir
{
	DODGE_None,
	DODGE_Left,
	DODGE_Right,
	DODGE_Forward,
	DODGE_Back,
	DODGE_Active,
	DODGE_Done
} DodgeDir;

// Physics properties.
var(Movement) float       Mass;            // Mass of this actor.
var(Movement) float       Buoyancy;        // Water buoyancy.
var(Movement) rotator	  RotationRate;    // Change in rotation per second.
var(Movement) rotator     DesiredRotation; // Physics will rotate pawn to this if bRotateToDesired.
var           float       PhysAlpha;       // Interpolating position, 0.0-1.0.
var           float       PhysRate;        // Interpolation rate per second.
var			  Actor		  PendingTouch;		// Actor touched during move which wants to add an effect after the movement completes 
//-----------------------------------------------------------------------------
// Animation.

// Animation control.
var          float        AnimLast;        // Last frame.
var          float        AnimMinRate;     // Minimum rate for velocity-scaled animation.
var			 float		  OldAnimRate;	   // Animation rate of previous animation (= AnimRate until animation completes).
var			 plane		  SimAnim;		   // replicated to simulated proxies.

// Blending Animation control - DEUS_EX CNN
var          float        BlendAnimLast[4];        // Last frame.
var          float        BlendAnimMinRate[4];     // Minimum rate for velocity-scaled animation.
var			 float		  OldBlendAnimRate[4];	   // Animation rate of previous animation (= AnimRate until animation completes).
var			 plane		  SimBlendAnim[4];		   // replicated to simulated proxies.

// Conversation Related Variables - DEUS_EX AJY
var(Conversation) String BindName;					// Used to bind conversations
var(Conversation) String BarkBindName;				// Used to bind Barks!
var(Conversation) localized String FamiliarName;	// For display in Conversations
var(Conversation) localized String UnfamiliarName;	// For display in Conversations
var transient Object     ConListItems;				// List of ConListItems for this Actor
var	travel   float       LastConEndTime;			// Time when last conversation ended
var(Conversation) float  ConStartInterval;			// Amount of time required between two convos.

// Additional variables for AI - DEUS_EX STM
var			 float		  VisUpdateTime;
var			 float		  CurrentVisibility;
var			 float		  LastVisibility;

var(Smell)   class<SmellNode> SmellClass;
var          SmellNode        LastSmellNode;

var(Advanced) bool            bOwned;
// End additional variables - DEUS_EX STM

// DEUS_EX AMSD Added to make vision aug run faster.  If true, the vision aug needs to check this object more closely.
// Used for heat sources as well as things that blind.
var bool bVisionImportant;

//-----------------------------------------------------------------------------
// Networking.

// Network control.
var(Networking) float NetPriority; // Higher priorities means update it more frequently.
var(Networking) float NetUpdateFrequency; // How many seconds between net updates.
var(Networking) float RelevantRadius; //Radius in which things are always relevant.

// Symmetric network flags, valid during replication only.
var const bool bNetInitial;       // Initial network update.
var const bool bNetOwner;         // Player owns this actor.
var const bool bNetRelevant;      // Actor is currently relevant. Only valid server side, only when replicating variables.
var const bool bNetSee;           // Player sees it in network play.
var const bool bNetHear;          // Player hears it in network play.
var const bool bNetFeel;          // Player collides with/feels it in network play.
var const bool bSimulatedPawn;	  // True if Pawn and simulated proxy.
var const bool bDemoRecording;	  // True we are currently demo recording
var const bool bClientDemoRecording;// True we are currently recording a client-side demo
var const bool bClientDemoNetFunc;// True if we're client-side demo recording and this call originated from the remote.


//-----------------------------------------------------------------------------
// Enums.

// Travelling from server to server.
enum ETravelType
{
	TRAVEL_Absolute,	// Absolute URL.
	TRAVEL_Partial,		// Partial (carry name, reset server).
	TRAVEL_Relative,	// Relative URL.
};

// Input system states.
enum EInputAction
{
	IST_None,    // Not performing special input processing.
	IST_Press,   // Handling a keypress or button press.
	IST_Hold,    // Handling holding a key or button.
	IST_Release, // Handling a key or button release.
	IST_Axis,    // Handling analog axis movement.
};

// Input keys.
enum EInputKey
{
/*00*/	IK_None			,IK_LeftMouse	,IK_RightMouse	,IK_Cancel		,
/*04*/	IK_MiddleMouse	,IK_Unknown05	,IK_Unknown06	,IK_Unknown07	,
/*08*/	IK_Backspace	,IK_Tab         ,IK_Unknown0A	,IK_Unknown0B	,
/*0C*/	IK_Unknown0C	,IK_Enter	    ,IK_Unknown0E	,IK_Unknown0F	,
/*10*/	IK_Shift		,IK_Ctrl	    ,IK_Alt			,IK_Pause       ,
/*14*/	IK_CapsLock		,IK_Unknown15	,IK_Unknown16	,IK_Unknown17	,
/*18*/	IK_Unknown18	,IK_Unknown19	,IK_Unknown1A	,IK_Escape		,
/*1C*/	IK_Unknown1C	,IK_Unknown1D	,IK_Unknown1E	,IK_Unknown1F	,
/*20*/	IK_Space		,IK_PageUp      ,IK_PageDown    ,IK_End         ,
/*24*/	IK_Home			,IK_Left        ,IK_Up          ,IK_Right       ,
/*28*/	IK_Down			,IK_Select      ,IK_Print       ,IK_Execute     ,
/*2C*/	IK_PrintScrn	,IK_Insert      ,IK_Delete      ,IK_Help		,
/*30*/	IK_0			,IK_1			,IK_2			,IK_3			,
/*34*/	IK_4			,IK_5			,IK_6			,IK_7			,
/*38*/	IK_8			,IK_9			,IK_Unknown3A	,IK_Unknown3B	,
/*3C*/	IK_Unknown3C	,IK_Unknown3D	,IK_Unknown3E	,IK_Unknown3F	,
/*40*/	IK_Unknown40	,IK_A			,IK_B			,IK_C			,
/*44*/	IK_D			,IK_E			,IK_F			,IK_G			,
/*48*/	IK_H			,IK_I			,IK_J			,IK_K			,
/*4C*/	IK_L			,IK_M			,IK_N			,IK_O			,
/*50*/	IK_P			,IK_Q			,IK_R			,IK_S			,
/*54*/	IK_T			,IK_U			,IK_V			,IK_W			,
/*58*/	IK_X			,IK_Y			,IK_Z			,IK_Unknown5B	,
/*5C*/	IK_Unknown5C	,IK_Unknown5D	,IK_Unknown5E	,IK_Unknown5F	,
/*60*/	IK_NumPad0		,IK_NumPad1     ,IK_NumPad2     ,IK_NumPad3     ,
/*64*/	IK_NumPad4		,IK_NumPad5     ,IK_NumPad6     ,IK_NumPad7     ,
/*68*/	IK_NumPad8		,IK_NumPad9     ,IK_GreyStar    ,IK_GreyPlus    ,
/*6C*/	IK_Separator	,IK_GreyMinus	,IK_NumPadPeriod,IK_GreySlash   ,
/*70*/	IK_F1			,IK_F2          ,IK_F3          ,IK_F4          ,
/*74*/	IK_F5			,IK_F6          ,IK_F7          ,IK_F8          ,
/*78*/	IK_F9           ,IK_F10         ,IK_F11         ,IK_F12         ,
/*7C*/	IK_F13			,IK_F14         ,IK_F15         ,IK_F16         ,
/*80*/	IK_F17			,IK_F18         ,IK_F19         ,IK_F20         ,
/*84*/	IK_F21			,IK_F22         ,IK_F23         ,IK_F24         ,
/*88*/	IK_Unknown88	,IK_Unknown89	,IK_Unknown8A	,IK_Unknown8B	,
/*8C*/	IK_Unknown8C	,IK_Unknown8D	,IK_Unknown8E	,IK_Unknown8F	,
/*90*/	IK_NumLock		,IK_ScrollLock  ,IK_Unknown92	,IK_Unknown93	,
/*94*/	IK_Unknown94	,IK_Unknown95	,IK_Unknown96	,IK_Unknown97	,
/*98*/	IK_Unknown98	,IK_Unknown99	,IK_Unknown9A	,IK_Unknown9B	,
/*9C*/	IK_Unknown9C	,IK_Unknown9D	,IK_Unknown9E	,IK_Unknown9F	,
/*A0*/	IK_LShift		,IK_RShift      ,IK_LControl    ,IK_RControl    ,
/*A4*/	IK_UnknownA4	,IK_UnknownA5	,IK_UnknownA6	,IK_UnknownA7	,
/*A8*/	IK_UnknownA8	,IK_UnknownA9	,IK_UnknownAA	,IK_UnknownAB	,
/*AC*/	IK_UnknownAC	,IK_UnknownAD	,IK_UnknownAE	,IK_UnknownAF	,
/*B0*/	IK_UnknownB0	,IK_UnknownB1	,IK_UnknownB2	,IK_UnknownB3	,
/*B4*/	IK_UnknownB4	,IK_UnknownB5	,IK_UnknownB6	,IK_UnknownB7	,
/*B8*/	IK_UnknownB8	,IK_UnknownB9	,IK_Semicolon	,IK_Equals		,
/*BC*/	IK_Comma		,IK_Minus		,IK_Period		,IK_Slash		,
/*C0*/	IK_Tilde		,IK_UnknownC1	,IK_UnknownC2	,IK_UnknownC3	,
/*C4*/	IK_UnknownC4	,IK_UnknownC5	,IK_UnknownC6	,IK_UnknownC7	,
/*C8*/	IK_Joy1	        ,IK_Joy2	    ,IK_Joy3	    ,IK_Joy4	    ,
/*CC*/	IK_Joy5	        ,IK_Joy6	    ,IK_Joy7	    ,IK_Joy8	    ,
/*D0*/	IK_Joy9	        ,IK_Joy10	    ,IK_Joy11	    ,IK_Joy12		,
/*D4*/	IK_Joy13		,IK_Joy14	    ,IK_Joy15	    ,IK_Joy16	    ,
/*D8*/	IK_UnknownD8	,IK_UnknownD9	,IK_UnknownDA	,IK_LeftBracket	,
/*DC*/	IK_Backslash	,IK_RightBracket,IK_SingleQuote	,IK_UnknownDF	,
/*E0*/  IK_JoyX			,IK_JoyY		,IK_JoyZ		,IK_JoyR		,
/*E4*/	IK_MouseX		,IK_MouseY		,IK_MouseZ		,IK_MouseW		,
/*E8*/	IK_JoyU			,IK_JoyV		,IK_UnknownEA	,IK_UnknownEB	,
/*EC*/	IK_MouseWheelUp ,IK_MouseWheelDown,IK_Unknown10E,UK_Unknown10F  ,
/*F0*/	IK_JoyPovUp     ,IK_JoyPovDown	,IK_JoyPovLeft	,IK_JoyPovRight	,
/*F4*/	IK_UnknownF4	,IK_UnknownF5	,IK_Attn		,IK_CrSel		,
/*F8*/	IK_ExSel		,IK_ErEof		,IK_Play		,IK_Zoom		,
/*FC*/	IK_NoName		,IK_PA1			,IK_OEMClear
};

var(Display) class<RenderIterator> RenderIteratorClass;	// class to instantiate as the actor's RenderInterface
var transient RenderIterator RenderInterface;		// abstract iterator initialized in the Rendering engine
```

### Network replication

```java
replication
{
	// Relationships.
	unreliable if( Role==ROLE_Authority )
		Owner, Role, RemoteRole;
	unreliable if( bNetOwner && Role==ROLE_Authority )
		bNetOwner, Inventory;
	unreliable if( bReplicateInstigator && (RemoteRole>=ROLE_SimulatedProxy) && (Role==ROLE_Authority) )
		Instigator;

	// Ambient sound.
	unreliable if( (Role==ROLE_Authority) && (!bNetOwner || !bClientAnim) )
		AmbientSound;
	unreliable if( AmbientSound!=None && Role==ROLE_Authority  && (!bNetOwner || !bClientAnim) )
		SoundRadius, SoundVolume, SoundPitch;
	unreliable if( bDemoRecording )
		DemoPlaySound;

	// Collision.
	unreliable if( Role==ROLE_Authority )
		bCollideActors, bCollideWorld;
	unreliable if( (bCollideActors || bCollideWorld) && Role==ROLE_Authority )
		bProjTarget, bBlockActors, bBlockPlayers, CollisionRadius, CollisionHeight;

	// Location.
	unreliable if( !bCarriedItem && (bNetInitial || bSimulatedPawn || RemoteRole<ROLE_SimulatedProxy) && Role==ROLE_Authority )
		Location;
	unreliable if( !bCarriedItem && (DrawType==DT_Mesh || DrawType==DT_Brush) && (bNetInitial || bSimulatedPawn || RemoteRole<ROLE_SimulatedProxy) && Role==ROLE_Authority )
		Rotation;
	unreliable if( RemoteRole==ROLE_SimulatedProxy )
		Base;

   // Events
   unreliable if( Role==ROLE_authority)
      Event, Tag;

	// Velocity.
	unreliable if( bSimFall || ((RemoteRole==ROLE_SimulatedProxy && (bNetInitial || bSimulatedPawn)) || bIsMover) )
		Velocity;

	// Physics.
	unreliable if( bSimFall || (RemoteRole==ROLE_SimulatedProxy && bNetInitial && !bSimulatedPawn) )
		Physics, Acceleration, bBounce;
	unreliable if( RemoteRole==ROLE_SimulatedProxy && Physics==PHYS_Rotating && bNetInitial )
		bFixedRotationDir, bRotateToDesired, RotationRate, DesiredRotation;

	// Animation. 
	unreliable if( DrawType==DT_Mesh && ((RemoteRole<=ROLE_SimulatedProxy && (!bNetOwner || !bClientAnim)) || bDemoRecording) )
		AnimSequence, BlendAnimSequence;						// blended anims added - DEUS_EX CNN
	unreliable if( DrawType==DT_Mesh && (RemoteRole==ROLE_SimulatedProxy))
		bAnimNotify;
	unreliable if( DrawType==DT_Mesh && (RemoteRole<ROLE_SimulatedProxy))
		SimAnim, AnimMinRate, SimBlendAnim, BlendAnimMinRate;	// blended anims added - DEUS_EX CNN


	// Rendering.
	unreliable if( Role==ROLE_Authority )
		bHidden, bOnlyOwnerSee;
	unreliable if( Role==ROLE_Authority )
		Texture, DrawScale, PrePivot, DrawType, AmbientGlow, Fatness, ScaleGlow, bUnlit, Style;
	unreliable if( DrawType==DT_Sprite && !bHidden && (!bOnlyOwnerSee || bNetOwner) && Role==ROLE_Authority)
		Sprite;
	unreliable if( DrawType==DT_Mesh && Role==ROLE_Authority )
		Mesh, bMeshEnviroMap, Skin, MultiSkins;
	unreliable if( DrawType==DT_Brush && Role==ROLE_Authority )
		Brush;

	// Lighting.
	unreliable if( Role==ROLE_Authority )
		LightType;
	unreliable if( LightType!=LT_None && Role==ROLE_Authority )
		LightEffect, LightBrightness, LightHue, LightSaturation,
		LightRadius, LightPeriod, LightPhase,
		VolumeBrightness, VolumeRadius,
		bSpecialLit;

	// Messages
	reliable if( Role<ROLE_Authority )
		BroadcastMessage, BroadcastLocalizedMessage;
}
```

##Functions

###ConsoleCommand
```java
native function string ConsoleCommand( string Command );
```
>Execute a console command in the context of the current level and game engine.

###Error
```
native(233) final function Error( coerce string S );
```
>Actor error handling.
>Handle an error and kill this one actor.

###Sleep
```
native(256) final latent function Sleep( float Seconds );
```

###Collision

```
native(262) final function SetCollision( optional bool NewColActors, optional bool NewBlockActors, optional bool NewBlockPlayers );
native(283) final function bool SetCollisionSize( float NewRadius, float NewHeight );
```

###Movement

```
native(266) final function bool Move( vector Delta );
native(267) final function bool SetLocation( vector NewLocation );
native(299) final function bool SetRotation( rotator NewRotation );
native(3969) final function bool MoveSmooth( vector Delta );
native(3971) final function AutonomousPhysics(float DeltaSeconds);
```


###Relations

```
native(298) final function SetBase( actor NewBase );
native(272) final function SetOwner( actor NewOwner );
```

###AI Functions 
`added DEUS_EX STM`

```
native(700) final function float AIGetLightLevel( vector Location );
native(701) final function float AIVisibility(optional bool bIncludeVelocity);
native(710) final function AISetEventCallback(name eventName, name callback,
                                              optional name scoreCallback,
                                              optional bool bCheckVisibility,
                                              optional bool bCheckDir,
                                              optional bool bCheckCylinder,
                                              optional bool bCheckLOS);
native(711) final function AIClearEventCallback(name eventName);
native(713) final function AISendEvent(name eventName, EAIEventType eventType,
                                       optional float Value, optional float Radius);
native(714) final function AIStartEvent(name eventName, EAIEventType eventType,
                                        optional float Value, optional float Radius);
native(715) final function AIEndEvent(name eventName, EAIEventType eventType);
native(716) final function AIClearEvent(name eventName);
native(717) final function rotator RandomBiasedRotation(int centralYaw, float yawDistribution,
                                                        int centralPitch, float pitchDistribution);
native(718) final function bool IsOverlapping(actor checkActor);
native(720) final function PlayerPawn GetPlayerPawn();
native(721) final function bool InStasis();
native(722) final function float ParabolicTrace(out      vector finalLocation,
                                                optional vector startVelocity,
                                                optional vector startLocation,
                                                optional bool   bCheckActors,
                                                optional vector cylinder,
                                                optional float  maxTime,
                                                optional float  elasticity,
                                                optional bool   bBounce,
                                                optional float  landingSpeed,
                                                optional float  granularity);
native(723) final function float LastRendered();
native(724) final function bool GetBoundingBox(out vector MinVect, out vector MaxVect,
                                               optional bool bExact,
                                               optional vector testLocation,
                                               optional rotator testRotation);
```

###Animation

```
native(259) final function PlayAnim( name Sequence, optional float Rate, optional float TweenTime );
native(260) final function LoopAnim( name Sequence, optional float Rate, optional float TweenTime, optional float MinRate );
native(294) final function TweenAnim( name Sequence, float Time );
native(282) final function bool IsAnimating();
native(293) final function name GetAnimGroup( name Sequence );
native(261) final latent function FinishAnim();
native(263) final function bool HasAnim( name Sequence );

// Blending animation function - DEUS_EX CNN
native(1010) final function PlayBlendAnim( name Sequence, optional float Rate, optional float TweenTime, optional int BlendSlot );
native(1012) final function TweenBlendAnim( name Sequence, float Time, optional int BlendSlot );

// Gets any numbered texture from a mesh - DEUS_EX CNN
native(1013) final function Texture GetMeshTexture( optional int texnum );

// Animation notifications.
event AnimEnd();

```

###Physics

```
// Physics control.
native(301) final latent function FinishInterpolation();
// DEUS_EX STM - added optional param to SetPhysics()
//native(3970) final function SetPhysics( EPhysics newPhysics );
native(3970) final function SetPhysics( EPhysics newPhysics, optional Actor newFloor );
```

##Engine notification functions

###Major notifications

####Spawned
```
event Spawned();
```
>Called when actor is Spawned. See also `PostBeginPlay`, `BeginPlay`, `PreBeginPlay`, `PostPostBeginPlay`.

####Destroyed
```
event Destroyed();
```
>Called when actor is destroyed and removed from the game.

####Expired
```
event Expired();
```
>Unknown.

####Children
```
event GainedChild( Actor Other );
event LostChild( Actor Other );
```
>Called when actor gains/looses a child actor.

####Tick
```
event Tick( float DeltaTime );
```
>Called every tick, or frame, of the game.

###Triggers
```
event Trigger( Actor Other, Pawn EventInstigator );
```
>Called when actor is 'Triggered' by the Trigger function.


```
event UnTrigger( Actor Other, Pawn EventInstigator );
```
>Called when actor de-activates, e.i. triggered again to turn off.


```
event BeginEvent();
event EndEvent();
```
>Unknown effects.

###Physics & world interaction.
####Timer
```
event Timer();
```
>Called when `SetTimer()` expires. (See `SetTimer`)<br>

  
####HitWall
```
event HitWall( vector HitNormal, actor HitWall );
```
>Called when object hits the wall.<br>
>`HitNormal`: The vector direction that the actor hit from.<br>
>`HitWall`: The wall being hit.<br>

####Falling
```
event Falling();
```
>Called when actor is falling through the air.

####Landed
```
event Landed( vector HitNormal );
```
>Called when actor hits the ground.<br>
>`HitNormal`: Firection actor landed from

####ZoneChange
```
event ZoneChange( ZoneInfo NewZone );
```
>Called when actor changes between Zones in the world.<br>
>`NewZone`: The ZoneInfo actor controlling the entered zone.


####Bump/Touch
```
event Bump( Actor Other );
event Touch( Actor Other );
```
>Called when actor hits in to another actor physically.<br>
>`Other`: The actor being touched.
```
event PostTouch( Actor Other );
event UnTouch( Actor Other );
```
> Called for PendingTouch actor after physics completes.


####BaseChange
```
event BaseChange();
```
> Called when actor changes base, meaning the actor that is supporting this one. For example, players standing on a crate, and then standing on the floor, is a BaseChange.


####Attachment
```
event Attach( Actor Other );
event Detach( Actor Other );
```
> Used for attaching and detaching actors from another. Mostly used for making buttons and switches follow elevators.


####KillCredit
```
event KillCredit( Actor Other );
```
> Called when something is killed.<br>
>`Other`: Actor being credited for a kill.

####Interpolating
```
event InterpolateEnd( actor Other );
```
> Called when actor finishes its interpolating path.

####EndedRotation
```
event EndedRotation();
```
> Called when actor stops rotating.<br>

####Others
```
event Actor SpecialHandling(Pawn Other);
event bool EncroachingOn( actor Other );
event EncroachedBy( actor Other );
```


`DEUS_EX STM -- added`
####BumpWall
```
event BumpWall( vector HitLocation, vector HitNormal );
```
>Called when actor hits the wall.<br>
>`HitLocation`: The location of the wall being hit.<br>
>`HitNormal`: The direction being hit from.<br>

####SupportActor
```
event SupportActor( actor StandingActor )
{
	StandingActor.SetBase( self );
}
```
>Called when actor is being stood on.<br>


####OutOfWorld
```
event FellOutOfWorld()
{
	SetPhysics(PHYS_None);
	Destroy();
}	
```
>Called when actor falls out of the world, e.g. fell through the geometry and no longer is in the normal play area.

####Damage and kills
```
event KilledBy( pawn EventInstigator );
```

>Called when actor is killed.<br>
>`EventInstigator`: The `pawn` that killed this actor.

```
event TakeDamage( int Damage, Pawn EventInstigator, vector HitLocation, vector Momentum, name DamageType);
```

>Called when the actor takes any damage.<br>
>`Damage`: The raw damage being dealt to this actor.<br>
>`EventInstigator`: The pawn dealing the damage.<br>
>`HitLocation`: The location this actor was hit at.<br>
>`Momentum`: The direction this actor will be pushed in.<br>
>`DamageType`: The string damage type being dealt.<br>


##Tracing

###Trace
```java
native(277) final function Actor Trace
(
	out vector      HitLocation,
	out vector      HitNormal,
	vector          TraceEnd,
	optional vector TraceStart,
	optional bool   bTraceActors,
	optional vector Extent
);
```
>Traces a line and see what it collides with first.<br>
>Takes this actor's collision properties into account.<br>
>Returns first hit actor, Level if hit level, or None if hit nothing.<br>
>`HitLocation`: The location we've hit. (`out` means the variable is usable after the function is called)<br>
>`HitNormal`: Not sure. (WIP)<br>
>`TraceEnd`: Where we want to trace to.<br>
>`TraceStart`: Where the trace starts from. Uses `<actor>.location` if left out.<br>
>`bTraceActors`: Where we collide with actors or not.<br>
>`Extent`: The range of the trace `(?)`<br>

###FastTrace
```
native(548) final function bool FastTrace
(
	vector          TraceEnd,
	optional vector TraceStart
);
```
>returns true if did not hit world geometry
>`TraceEnd`: Where we want to trace to.<br>
>`TraceStart`: Where the trace starts from. Uses `<actor>.location` if left out.<br>

##Spawn
```
native(278) final function actor Spawn
(
	class<actor>      SpawnClass,
	optional actor	  SpawnOwner,
	optional name     SpawnTag,
	optional vector   SpawnLocation,
	optional rotator  SpawnRotation
);
```

>Spawn an actor. **Returns** an actor of the specified class, not
>of class Actor (this is hardcoded in the compiler). Returns None
>if the actor could not be spawned (either the actor wouldn't fit in
>the specified location, or the actor list is full).<br>
>Defaults to spawning at the spawner's location.<br>
>`SpawnClass`: The class we want to spawn. Example: `class'DeusEx.Medkit'`<br>
>`SpawnOwner`: The actor that owns the newly spawned actor.<br>
>`SpawnTag`: Sets the `Tag` of the new actor.<br>
>`SpawnLocation`: Location to spawn at. Uses `self.location` if left out.<br>
>`SpawnRotation`: Rocation to spawn at. Uses `self.rotation` if left out.<br>

##Destroy
```
native(279) final function bool Destroy();
```
>Destroy this actor. **Returns** true if destroyed, false if indestructable.
>Destruction is latent. It occurs at the end of the tick.

##Timer
```
native(280) final function SetTimer( float NewTimerRate, bool bLoop );
```
>Triggers the `Timer()` event after `NewTimerRate` ticks. <br>
>If `bLoop` is `True` then then timer will continue looping, else only triggers once.<br>

##Sound

###PlaySound
```
native(264) final function int PlaySound
(
	sound				Sound,
	optional ESoundSlot Slot,
	optional float		Volume,
	optional bool		bNoOverride,
	optional float		Radius,
	optional float		Pitch
);

//Same as PlaySound, but only plays for the client. (No server propogation)
native simulated final function PlayOwnedSound();

//PlaySound call used for Demorec system.
native simulated event DemoPlaySound();
```

>Play a sound effect.<br>
>`*DEUS_EX - CNN* changed to return the channel ID of the sound so you can call StopSound later`<br>
>`Sound`: A sound class in the game. Example: `sound'LogNoteAdded'`<br>
>`ESoundSlot`: The slot to play the sound in to. See `ESoundSlot` variable.<br>
>`Volume`: Volume of the sound.<br>
>`bNoOverride`: Wether this sound can be overwritten with other sounds on the same slot or not.<br>
>`Radius`: Physical hearable radius of the sound.<br>
>`Pitch`: Sounds pitch modifier.<br>


###StopSound

```
native(265) final function StopSound(int Id);
```
>DEUS_EX CNN - Stop a sound given the sound's ID

###SetInstantVolume 

```
native(268) final function SetInstantSoundVolume(byte newSoundVolume);
native(269) final function SetInstantSpeechVolume(byte newSpeechVolume);
native(270) final function SetInstantMusicVolume(byte newMusicVolume);
```
>DEUS_EX CNN - Set the sound system volumes without waiting for a tick event

###GetSoundDuration

```
native final function float GetSoundDuration( sound Sound );
```
>Get a sound duration.


##AI functions.

###MakeNoise

```
native(512) final function MakeNoise( float Loudness );
```
>Inform other creatures that you've made a noise
>they might hear (they are sent a HearNoise message)<br>
>Senders of MakeNoise should have an instigator if they are not pawns.

###PlayerCanSeeMe

```
native(532) final function bool PlayerCanSeeMe();
```
>`Returns` true if some player has a line of sight to actor's location.

##Teleportation

```
event bool PreTeleport( Teleporter InTeleporter );
```
>Called before actor teleports using a `Teleporter` actor.

```
event PostTeleport( Teleporter OutTeleporter );
```
>Called after actor teleports using a `Teleporter` actor.

##BeginPlay

```
event BeginPlay();
```
>Called when actor enters the game.

```
event PostBeginPlay();
```
>Called immediately after gameplay begins.


```
event PostPostBeginPlay();
```
>`DEUS_EX AJY`
>Called immediately after Initial State, and always
>called when loading a map *AND* when loading savegame

```
simulated event SetInitialState()
{
	if( InitialState!='' )
		GotoState( InitialState );
	else
		GotoState( 'Auto' );
}
```
>Called after PostBeginPlay.


```
simulated event PostNetBeginPlay();
```
>`MBCODE`
>Called after a net game begins.

```
event PreBeginPlay()
{
	// fake shrink to fix faked collision with floor problems - DEUS_EX CNN
	if ((IsA('Decoration') || IsA('Inventory')) && (CollisionHeight > 0.75))
		SetCollisionSize(CollisionRadius, CollisionHeight - 0.75);
	else if (IsA('Pawn'))
	{
		if (CollisionHeight > 9)
			SetCollisionSize(CollisionRadius, CollisionHeight - 4.5);
		else
			SetCollisionSize(CollisionRadius, CollisionHeight*0.5);
	}

	// Handle autodestruction if desired.
	if( !bGameRelevant && (Level.NetMode != NM_Client) && !Level.Game.IsRelevant(Self) )
		Destroy();
}
```
>Called immediately before gameplay begins.

##Disk access.

```
// Find files.
native(539) final function string GetMapName( string NameEnding, string MapName, int Dir );
native(545) final function GetNextSkin( string Prefix, string CurrentSkin, int Dir, out string SkinName, out string SkinDesc );
native(547) final function string GetURLMap();
native final function string GetNextInt( string ClassName, int Num );
native final function GetNextIntDesc( string ClassName, int Num, out string Entry, out string Description );
```

##Iterator functions.

```
native(304) final iterator function AllActors     ( class<actor> BaseClass, out actor Actor, optional name MatchTag );
native(305) final iterator function ChildActors   ( class<actor> BaseClass, out actor Actor );
native(306) final iterator function BasedActors   ( class<actor> BaseClass, out actor Actor );
native(307) final iterator function TouchingActors( class<actor> BaseClass, out actor Actor );
native(309) final iterator function TraceActors   ( class<actor> BaseClass, out actor Actor, out vector HitLoc, out vector HitNorm, vector End, optional vector Start, optional vector Extent );
native(310) final iterator function RadiusActors  ( class<actor> BaseClass, out actor Actor, float Radius, optional vector Loc );
native(311) final iterator function VisibleActors ( class<actor> BaseClass, out actor Actor, optional float Radius, optional vector Loc );
native(312) final iterator function VisibleCollidingActors ( class<actor> BaseClass, out actor Actor, optional float Radius, optional vector Loc, optional bool bIgnoreHidden );

// added by DEUS_EX CNN
native(1000) final iterator function TraceTexture (class<actor> BaseClass, out actor Actor, out name texName, out name texGroup, out int flags, out vector HitLoc, out vector HitNorm, vector End, optional vector Start, optional vector Extent);

// added by DEUS_EX STM
native(1002) final iterator function CycleActors (class<actor> BaseClass, out actor Actor, out int Index );
native(1003) final iterator function TraceVisibleActors(class<actor> BaseClass, out actor Actor, out vector HitLoc, out vector HitNorm, vector End, optional vector Start, optional vector Extent );
```
>Iterators are used in the format of;

```
//Destroy all medkits
local Medkit MD;
foreach AllActors(class'DeusEx.Medkit', MD)
	MD.Destroy()
```

##Color operators

```
native(549) static final operator(20)  color -     ( color A, color B );
native(550) static final operator(16) color *     ( float A, color B );
native(551) static final operator(20) color +     ( color A, color B );
native(552) static final operator(16) color *     ( color A, float B );
```

##Scripted Actor functions

```
event RenderOverlays( canvas Canvas );
```
>draw on canvas before flash and fog are applied (used for drawing weapons)


###BroadcastMessage

```
event BroadcastMessage( coerce string Msg, optional bool bBeep, optional name Type )
{
	local Pawn P;

	if (Type == '')
		Type = 'Event';

//	if ( Level.Game.AllowsBroadcast(self, Len(Msg)) )
		for( P=Level.PawnList; P!=None; P=P.nextPawn )
			if( P.bIsPlayer || P.IsA('MessagingSpectator') )
				P.ClientMessage( Msg, Type, bBeep );
}
```
>Broadcast a message to all players.<br>
>Can be called as a function; `BroadcastMessage("This is seen by everyone.")`<br>
>`bBeep`: Defines if the message triggers a chat message beep. (Maybe doesn't work?)<br>
>`Type`: Unsure.<br>

```
event BroadcastLocalizedMessage( class<LocalMessage> Message, optional int Switch, optional PlayerReplicationInfo RelatedPRI_1, optional PlayerReplicationInfo RelatedPRI_2, optional Object OptionalObject )
{
	local Pawn P;

	for ( P=Level.PawnList; P != None; P=P.nextPawn )
		if ( P.bIsPlayer || P.IsA('MessagingSpectator') )
			P.ReceiveLocalizedMessage( Message, Switch, RelatedPRI_1, RelatedPRI_2, OptionalObject );
}
```
>Broadcast a localized message to all players.<br>
>Most message deal with 0 to 2 related PRIs.<br>
>The LocalMessage class defines how the PRI's and optional actor are used.<br>

###HurtRadius

```
final function HurtRadius( float DamageAmount, float DamageRadius, name DamageName, float Momentum, vector HitLocation, optional bool bIgnoreLOS )
{
	local actor Victims;
	local float damageScale, dist;
	local vector dir;

	// DEUS_EX CNN
	local Mover M;				
	
	if( bHurtEntry )
		return;

	bHurtEntry = true;
   if (!bIgnoreLOS)
   {
      foreach VisibleCollidingActors( class 'Actor', Victims, DamageRadius, HitLocation )
      {
         if( Victims != self )
         {
            dir = Victims.Location - HitLocation;
            dist = FMax(1,VSize(dir));
            dir = dir/dist; 
            damageScale = 1 - FMax(0,(dist - Victims.CollisionRadius)/DamageRadius);
            Victims.TakeDamage
               (
               damageScale * DamageAmount,
               Instigator, 
               Victims.Location - 0.5 * (Victims.CollisionHeight + Victims.CollisionRadius) * dir,
               (damageScale * Momentum * dir),
               DamageName
               );
         } 
      }
   }
   else
   {
      foreach RadiusActors(class 'Actor', Victims, DamageRadius, HitLocation )
      {
         if( Victims != self )
         {
            dir = Victims.Location - HitLocation;
            dist = FMax(1,VSize(dir));
            dir = dir/dist; 
            damageScale = 1 - FMax(0,(dist - Victims.CollisionRadius)/DamageRadius);
            Victims.TakeDamage
               (
               damageScale * DamageAmount,
               Instigator, 
               Victims.Location - 0.5 * (Victims.CollisionHeight + Victims.CollisionRadius) * dir,
               (damageScale * Momentum * dir),
               DamageName
               );
         } 
      }
   }

	//
	// DEUS_EX - CNN - damage the movers, also
	//
	foreach RadiusActors(class 'Mover', M, DamageRadius, HitLocation)
	{
		if( M != self )
		{
			dir = M.Location - HitLocation;
			dist = FMax(1,VSize(dir));
			dir = dir/dist; 
			damageScale = 1 - FMax(0,(dist - M.CollisionRadius)/DamageRadius);
			M.TakeDamage
			(
				damageScale * DamageAmount,
				Instigator, 
				M.Location - 0.5 * (M.CollisionHeight + M.CollisionRadius) * dir,
				(damageScale * Momentum * dir),
				DamageName
			);
		} 
	}

	bHurtEntry = false;
}
```
>Hurt actors within the radius.<br>
>`DamageAmount`: Damage done to the actors.<br>
>`DamageRadius`: Range of actors to damage.<br>
>`DamageName`: Name of the damage.<br>
>`Momentum`: Vector to push the damaged actor in.<br>
>`HitLocation`: Location to deal the damage to. Only relevant for Pawn actors to damage body parts.<br>
>`bIgnoreLOS` : Unsure.<br>

###Travel

```
event TravelPreAccept();
```
>Called when carried onto a new level, before AcceptInventory.

```
event TravelPostAccept();
```
>Called when carried into a new level, after AcceptInventory.

###Frob

```
function Frob(Actor Frobber, Inventory frobWith)
{
}
```
>`DEUS_EX CNN`
>Called to frob an object, the subclass is responsible for implementing this
>`Frobber` will be the actor frobbing this actor.
>`frobWith`: Unsure.

###StopBlendAnims

```
function StopBlendAnims()
{
	local int i;

	for (i=0; i<ArrayCount(BlendAnimSequence); i++)
		BlendAnimSequence[i] = '';
}
```
>`DEUS_EX CNN`
>Stops animations from blending

###RenderTexture

```
event RenderTexture(ScriptedTexture Tex);
```
>Called when a scripted texture needs rendering

###BecomeViewTarget

```
function BecomeViewTarget();
```
>Called by PlayerPawn when this actor becomes its ViewTarget.


###GetItemName

```
function String GetItemName( string FullName )
{
	local int pos;

	pos = InStr(FullName, ".");
	While ( pos != -1 )
	{
		FullName = Right(FullName, Len(FullName) - pos - 1);
		pos = InStr(FullName, ".");
	}

	return FullName;
}
```
>Returns the string representation of the name of an object without the package prefixes.

###GetHumanName

```
function String GetHumanName()
{
	return GetItemName(string(class));
}
```
>Returns the human readable string representation of an object.


###SetDisplayProperties

```
function SetDisplayProperties(ERenderStyle NewStyle, texture NewTexture, bool bLighting, bool bEnviroMap )
{
	Style = NewStyle;
	texture = NewTexture;
	bUnlit = bLighting;
	bMeshEnviromap = bEnviromap;
}

function SetDefaultDisplayProperties()
{
	Style = Default.Style;
	texture = Default.Texture;
	bUnlit = Default.bUnlit;
	bMeshEnviromap = Default.bMeshEnviromap;
}
```
>Set the display properties of an actor.  By setting them through this function, it allows
>the actor to modify other components (such as a Pawn's weapon) or to adjust the result
>based on other factors (such as a Pawn's other inventory wanting to affect the result)

###EndConversation

```
function EndConversation()
{
	LastConEndTime = Level.TimeSeconds;
}
```
>Save the time this conversation ended `DEUS_EX AJY`

##DefaultProperties

```
defaultproperties
{
     bMovable=True
     bDetectable=True
     Role=ROLE_Authority
     RemoteRole=ROLE_DumbProxy
     LastRenderTime=-10.000000
     LODBias=1.000000
     bDifficulty0=True
     bDifficulty1=True
     bDifficulty2=True
     bDifficulty3=True
     bSinglePlayer=True
     bNet=True
     bNetSpecial=True
     OddsOfAppearing=1.000000
     DrawType=DT_Sprite
     Style=STY_Normal
     Texture=Texture'Engine.S_Actor'
     DrawScale=1.000000
     ScaleGlow=1.000000
     Fatness=128
     SoundRadius=32
     SoundVolume=128
     SoundPitch=64
     TransientSoundVolume=1.000000
     CollisionRadius=22.000000
     CollisionHeight=22.000000
     bJustTeleported=True
     Mass=100.000000
     ConStartInterval=5.000000
     NetPriority=1.000000
     NetUpdateFrequency=100.000000
}
```

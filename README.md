# sbModRacialStart
Starbound mod - changes the intro quest script to be more modular

## Intro Quest Terms
..* Pester - sends the player a radio message after x time has passed
..* Area - defined by a stagehand with the given uniqueID

## MISSION STAGES

### 1 - start -> exit bed
..* Player starts lounging on the closest loungeable (within 10 spaces)
..* SAIL pesters the player to leave the bed

### 2 - dorm room
..* SAIL message protectorateDormRoomTutorial
..* SAIL messages protectorateDormRoomPester after 40s

### 3 - lounge
..* indicators on 'uniformLocker'
..* SAIL message protectorateLoungeTutorial

### 4 - has uniform (optional)
..* Resets indicators
..* In courtyard area

### 5 - auditorium cutscene
..* Transitions music to midpointMusicTracks
..* Plays midpointCinematic
..* Teleports to midpointTeleportPosition during cinematic
..* Set indicators to beamaxe
..* Sets new quest objective - 'matterManipulator'
..* SAIL message protectorateStage5

### 6 - has MM
..* Resets indicators
..* Give player the MM
..* Beamaxe cinematic
..* Sets new quest objective - 'escape'
..* On entering "collapsedGallery" SAIL radios "protectorateCollapsedGalleryNoMM" or "protectorateCollapsedGallery" and pesters "protectorateCollapsedGalleryPester"
..* On entering "pastCollapsedGallery"  - clears pesters
..* In "floodedDoor" area - "protectorateFloodedDoor" radio message
..* In "rooftop" area - "protectorateRooftop" radio message
..* In "duct" area - "protectorateDuct" radio message

### 7 - storeroom
..* Set indicators to weaponChest
..* SAIL message protectorateGetWeapon
..* SAIL messages protectorateWeaponPester until weapon is picked up
..* On approaching the tentacleBarrier enemy - sends protectorateTentacleBarrier message

### 8 - has weapon
..* Resets indicators

### 9 -

### 10 - reach ship -> finish
..* Transitions music to playAltMusic
..* Radios "protectorateShipPlatform" message
..* Plays endpointCinematic
..* When missionCompleteTimer runs out, player teleports to ship + quest completes

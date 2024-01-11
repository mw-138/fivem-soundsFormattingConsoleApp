# FiveM Sounds Formatting Console App

## About
Formats native GTA V sounds from https://gist.github.com/Sainan/021bd2f48f1c68d3eb002caab635b5a4 into a dictionary/table form.

## Example (TypeScript)
```
class Sound {
  name: string;
  ref: string;

  constructor(name: string, ref: string) {
    this.name = name;
    this.ref = ref;
  }

  public play(
    soundId: number = -1,
    p3: boolean = true,
    p4: number = 0,
    p5: boolean = true
  ): void {
    PlaySound(soundId, this.name, this.ref, p3, p4, p5);
  }

  public playFrontend(soundId: number = -1, p3: boolean = true): void {
    PlaySoundFrontend(soundId, this.name, this.ref, p3);
  }

  public playFromEntity(
    entity: number,
    isNetwork: boolean,
    soundId: number = -1,
    p5: number = 0
  ): void {
    PlaySoundFromEntity(soundId, this.name, entity, this.ref, isNetwork, p5);
  }

  public playFromCoord(
    x: number,
    y: number,
    z: number,
    range: number,
    isNetwork: boolean,
    soundId: number = -1,
    p8: boolean = false
  ): void {
    PlaySoundFromCoord(
      soundId,
      this.name,
      x,
      y,
      z,
      this.ref,
      isNetwork,
      range,
      p8
    );
  }
}

interface SoundCategory {
  [sound: string]: Sound;
}

interface SoundData {
  [category: string]: SoundCategory;
}

export const Sounds: SoundData = {
  DLC_EXEC_ARC_MAC_SOUNDS: {
    Crash: new Sound("Crash", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Crash_NPC: new Sound("Crash_NPC", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Trail_1: new Sound("Trail_1", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Trail_2: new Sound("Trail_2", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Trail_3: new Sound("Trail_3", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Trail_4: new Sound("Trail_4", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Turn: new Sound("Turn", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Turn_NPC: new Sound("Turn_NPC", "DLC_EXEC_ARC_MAC_SOUNDS"),
    THREE_TWO_ONE: new Sound("321", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Degenatron_Logo: new Sound("Degenatron_Logo", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Degenatron_Star: new Sound("Degenatron_Star", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Go: new Sound("Go", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Music_Game_Over: new Sound("Music_Game_Over", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Music_Win: new Sound("Music_Win", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Ready: new Sound("Ready", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Background: new Sound("Background", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Cancel: new Sound("Cancel", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Insert_Coin: new Sound("Insert_Coin", "DLC_EXEC_ARC_MAC_SOUNDS"),
    Game_Over_Blink: new Sound("Game_Over_Blink", "DLC_EXEC_ARC_MAC_SOUNDS"),
  }
}
```

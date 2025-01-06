## 🔊 AUDIO

- audio types
    
    ```lua
    audio.SFX  -- Used for short sound sample, one shots, etc. The sound is loaded directly in memory. Must be a .wav files under 65k samples.
    audio.WAV  -- Used for audio streaming. Must be a .wav file.
    audio.CDDA -- Used for CDDA audio streaming. Filename will be the track number (0-99) and the file must be placed in the audio directory at the root of the engine.
    ```
    
- *source*
    
    ```lua
    local source = {
      loaded    = false,
      id        = 0,
      channel   = -1,
      volume    = 220, --0, 254
      isPlaying = false,
      type      = audio.SFX,
    }
    ```
    

| **audio.load(filename, type)** | Loads a .wav (audio.SFX or audio.WAV) file. Returns a *source.* Type must be audio.SFX, audio.WAV or audio.CDDA |
| --- | --- |
| **audio.play(source, *volume, loop*)** | Plays a *source* at 0-255 volume. |
| **audio.setVolume(source, volume)** | Sets the volume of a playing *source*. |
| **audio.free(source)** | Frees the memory of a loaded *source*. |
| **audio.isPlaying(source)** |  |
| **audio.pause(source)** |  |
| **audio.stop(source)** |  |
| **audio.setPan(source, pan)** | Sets pan. 128 is center, 0 is full left, 255 is full right. Only works on .SFX type sound. |
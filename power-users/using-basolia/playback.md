---
description: Play your music!
---

# 🎼 Playback

The playback tools in the Basolia library contains two separate sections: the actual playback tools and the playback positioning tools.

## Playback Tools

The playback tools shipped with the Basolia library is a key feature for every single music player.

### Playing music

There are two ways to play the music: synchronously and asynchronously. For normal console applications, you'd typically use `Play()` for a single audio player, or this function in a thread for a music player, such as BassBoom.Cli.

```csharp
public static void Play()
```

However, for GUI application, it's best to use the asynchronous version whenever possible, `PlayAsync()`, to avoid blocking the main thread.

```csharp
public static async Task PlayAsync()
```

### Pausing and stopping music

If you want to pause the music, you can use the `Pause()` function. It'll stop the music, but stays at the current position. If you want to start over, you can use the `Stop()` function.

```csharp
public static void Pause()
public static void Stop()
```

### Volume Controls

For controlling the volume that the Basolia library controls, you can use both the `SetVolume()` and the `GetVolume()` functions. `SetVolume()` allows you to set the current volume to the new volume from 0.0 (0%) to 1.0 (100%).

```csharp
public static void SetVolume(double volume)
```

Getting the current volume using the `GetVolume()` function returns three variables that describe the following:

* `baseLinear`: The base linear volume from 0.0 to 1.0
* `actualLinear`: The actual linear volume from 0.0 to 1.0
* `decibelsRva`: The RVA value in decibels (dB)

```csharp
public static (double baseLinear, double actualLinear, double decibelsRva) GetVolume()
```

### Playback states

When either Play(), Pause(), or Stop() functions are called, the playback state changes, depending on the action. You can get the current playback state by using the `State` property.

```csharp
public static PlaybackState State
```

You can also quickly determine whether Basolia is busy playing a song using the `Playing` property:

```csharp
public static bool Playing
```

The playback states are the following:

* `Stopped`: Music has either stopped or not played yet
* `Playing`: Music is playing
* `Paused`: Music has been paused by the user or by the call to the `Pause()` function

## Positioning tools

In addition to the playback tools, you can also get access to the positioning tools to perform seek operations to jump to a specific section of a song, regardless of whether the song is playing or not.

### Current duration

You can get the current duration in two units: Samples and time span. If you want to get the current duration using the samples, you can use the `GetCurrentDuration()` function:

```csharp
public static int GetCurrentDuration()
```

Similarly, you can also get the current duration in the timespan for easier representation by using the `GetCurrentDurationSpan()` function:

```csharp
public static TimeSpan GetCurrentDurationSpan()
```

### Seeking controls

If you want to seek the music file either to a selected position using a frame number or to the beginning of the song (frame 0), you can simply use one of the two functions:

```csharp
// For seeking to the beginning
public static void SeekToTheBeginning()

// For seeking to a specific MPEG frame
public static void SeekToFrame(int frame)
```

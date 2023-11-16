---
description: This is just the beginning!
---

# 💎 API v1.0 series

This series is the first version series that actually defines the multiplatform music player to the .NET environment. The first version of BassBoom, 0.0.1, was out on October 1st, 2023.

## Version 0.0.2

This version was released on November 14th, 2023, as a celebration of the .NET 8.0 release! This version serves as an enhancement release over the previous version.

### Improvements (Basolia)

* Updated MPG123 to 1.32.3
* Updated targeting to .NET 8.0
* Added support for macOS 64-bit (ARM64 support not done yet)
* Added getting frame length and samples per frame
* Added synthesis to Native (currently unused)

### Improvements (CLI music player)

* Updated Terminaux
* Show song name and duration in the music list
* Don't show genre in the titles
* Use music file name instead of "unknown song"
* Only populate music info if necessary
* You can remove songs from the playlist

### Improvements (GUI music player)

* Updated Avalonia
* Show song name and duration in the music list

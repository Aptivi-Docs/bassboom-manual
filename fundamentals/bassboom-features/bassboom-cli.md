---
description: Music player in your console!
---

# 🎶 BassBoom CLI

<figure><img src="../../.gitbook/assets/BB.Cli.png" alt=""><figcaption></figcaption></figure>

BassBoom provides you its CLI version that allows you to play any music using just your terminal emulator. You can use this version if you need no GUI and just want to play music using just the textual UI.

{% hint style="info" %}
Since the TUI version uses Terminaux to render its elements, you need to have a terminal emulator which supports VT sequences out of the box.
{% endhint %}

## Usage

You can run this program by either double-clicking an executable file, which will prompt you for the full path to a music file, or by opening the command prompt to the BassBoom.Cli binaries directory and writing the command like this:

* For Windows, `BassBoom.Cli.exe path/to/music.mp3`
* For Linux, `dotnet BassBoom.Cli.dll path/to/music.mp3`

Once done, BassBoom opens your music file to be ready for playing. Just play your music by pressing the spacebar.

## Controls

You can use the following keys to navigate through the entire music player. However, there are keys that don't do anything in modes that don't define such keys.

### Idle mode

When BassBoom.Cli is in idle mode (music not playing, music paused, etc.), you can use the following controls:

<table><thead><tr><th width="191">Control</th><th>Action</th></tr></thead><tbody><tr><td><code>UP</code></td><td>Raises the volume</td></tr><tr><td><code>DOWN</code></td><td>Lowers the volume</td></tr><tr><td><code>SPACE</code></td><td>Plays the music</td></tr><tr><td><code>B</code></td><td>Goes back to the previous song in the playlist and plays it</td></tr><tr><td><code>N</code></td><td>Goes to the next song in the playlist and plays it</td></tr><tr><td><code>H</code></td><td>Shows the help menu</td></tr><tr><td><code>I</code></td><td>Shows the song information, including the bit rate, artist, genre, etc.</td></tr><tr><td><code>A</code></td><td>Adds a single song to the playlist</td></tr><tr><td><code>S</code></td><td>Adds songs from a music library directory to the playlist</td></tr><tr><td><code>R</code></td><td>Removes the current song</td></tr><tr><td><code>CTRL + R</code></td><td>Removes all the songs</td></tr><tr><td><code>E</code></td><td>Opens the interactive equalizer</td></tr><tr><td><code>Z</code></td><td>Shows BassBoom and platform information</td></tr><tr><td><code>Q</code></td><td>Exits the program</td></tr></tbody></table>

### Playing mode

When BassBoom.Cli goes into this mode by playing any music, you can use these controls:

<table><thead><tr><th width="192">Control</th><th>Action</th></tr></thead><tbody><tr><td><code>UP</code></td><td>Raises the volume</td></tr><tr><td><code>DOWN</code></td><td>Lowers the volume</td></tr><tr><td><code>RIGHT</code></td><td>Seeks the music forward by the set seek rate</td></tr><tr><td><code>CTRL + RIGHT</code></td><td>Increases the seek rate by 50 milliseconds</td></tr><tr><td><code>LEFT</code></td><td>Seeks the music backward by the set seek rate</td></tr><tr><td><code>CTRL + LEFT</code></td><td>Decreases the seek rate by 50 milliseconds</td></tr><tr><td><code>B</code></td><td>Goes back to the previous song in the playlist and plays it</td></tr><tr><td><code>N</code></td><td>Goes to the next song in the playlist and plays it</td></tr><tr><td><code>SPACE</code></td><td>Pauses the music</td></tr><tr><td><code>R</code></td><td>Removes the currently playing song</td></tr><tr><td><code>CTRL + R</code></td><td>Removes all the songs</td></tr><tr><td><code>ESC</code></td><td>Stops the song</td></tr><tr><td><code>H</code></td><td>Shows the help screen</td></tr><tr><td><code>I</code></td><td>Shows the song info</td></tr><tr><td><code>E</code></td><td>Opens the interactive equalizer</td></tr><tr><td><code>D</code></td><td>Shows all devices and drivers probed by MPG123</td></tr><tr><td><code>Z</code></td><td>Shows BassBoom and platform information</td></tr><tr><td><code>Q</code></td><td>Exits BassBoom.Cli</td></tr></tbody></table>

### Equalizer screen

You can also modify how your song plays like in real-time using the interactive equalizer. You can use these controls:

| Control       | Action                                     |
| ------------- | ------------------------------------------ |
| `<-` / `->`   | Changes the current equalizer band's value |
| `UP` / `DOWN` | Selects the equalizer band                 |
| `R`           | Resets all values                          |
| `Q`           | Goes back to the player                    |

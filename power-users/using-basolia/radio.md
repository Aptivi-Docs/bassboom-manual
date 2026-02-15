---
description: You're now listening to an FM radio station!
icon: radio
---

# Radio

BassBoom provides you with the Internet radio features, such as playing them and getting information about your favorite radio station.

***

## <mark style="color:$primary;">Usage</mark>

You can use the `FileTools.OpenUrl()` function to open the MPG123 handle to the radio station URL, assuming that said station uses MPEG and not AAC or other formats. Use the `PlaybackTools.Play()`, as usual, to play the radio station.

If you want to get your favorite internet radio station's information, you can use the `GetRadioInfo` function from the `RadioTools` class in the `BassBoom.Basolia.Radio` namespace. Afterwards, you can call either `Refresh()` or `RefreshAsync()` to fetch info.

<details>

<summary>Server info properties</summary>

The following info is obtained from the server:

<table><thead><tr><th width="170">Property</th><th>Description</th></tr></thead><tbody><tr><td><code>ServerHost</code></td><td>Server IP address</td></tr><tr><td><code>ServerPort</code></td><td>Server port used by Shoutcast</td></tr><tr><td><code>ServerHostFull</code></td><td>Server IP address with port</td></tr><tr><td><code>ServerHttps</code></td><td>Whether the Shoutcast server is using HTTPS or not</td></tr><tr><td><code>ServerType</code></td><td>Radio server type</td></tr><tr><td><code>ServerVersion</code></td><td>[SHOUTcast] Server version (1.x, 2.x)</td></tr><tr><td><code>TotalStreams</code></td><td>Total number of streams in the server</td></tr><tr><td><code>ActiveStreams</code></td><td>Active streams in the server</td></tr><tr><td><code>CurrentListeners</code></td><td>How many people are listening to the server at this time?</td></tr><tr><td><code>PeakListeners</code></td><td>How many listeners did the server ever get at peak times?</td></tr><tr><td><code>MaxListeners</code></td><td>[SHOUTcast] How many people can listen to the server?</td></tr><tr><td><code>UniqueListeners</code></td><td>[SHOUTcast] How many unique listeners are there?</td></tr><tr><td><code>AverageTime</code></td><td>[SHOUTcast] Average time on any active listener connections in seconds</td></tr><tr><td><code>AverageTimeSpan</code></td><td>[SHOUTcast] Average time on any active listener connections in the time span</td></tr><tr><td><code>Streams</code></td><td>Available streams and their statistics</td></tr></tbody></table>

</details>

<details>

<summary>Stream info class properties</summary>

Stream information class, `StreamInfo`, contains the following variables:

| Property                        | Description                                                                   |
| ------------------------------- | ----------------------------------------------------------------------------- |
| `StreamId`                      | Stream ID starting from number one (1)                                        |
| `CurrentListeners`              | How many people are listening to the stream at this time?                     |
| `PeakListeners`                 | How many listeners did the stream ever get at peak times?                     |
| `MaxListeners`                  | \[SHOUTcast] How many people can listen to the stream?                        |
| `UniqueListeners`               | \[SHOUTcast] How many unique listeners are there?                             |
| `AverageTime`                   | \[SHOUTcast] Average time on any active listener connections in seconds       |
| `AverageTimeSpan`               | \[SHOUTcast] Average time on any active listener connections in the time span |
| `StreamGenre` -> `StreamGenre5` | The stream genre                                                              |
| `StreamHomepage`                | Link to the stream homepage                                                   |
| `StreamTitle`                   | Stream title                                                                  |
| `SongTitle`                     | Song title                                                                    |
| `StreamHits`                    | \[SHOUTcast] Stream hits                                                      |
| `StreamStatus`                  | \[SHOUTcast] Stream status                                                    |
| `BackupStatus`                  | \[SHOUTcast] Backup stream status                                             |
| `StreamListed`                  | Is the stream listed?                                                         |
| `StreamPath`                    | Path to stream                                                                |
| `StreamUptime`                  | \[SHOUTcast] Stream uptime in seconds                                         |
| `StreamUptimeSpan`              | \[SHOUTcast] Stream uptime in the time span                                   |
| `BitRate`                       | Stream bitrate in kbps                                                        |
| `SampleRate`                    | \[SHOUTcast] Sampling rate in Hz                                              |
| `MimeInfo`                      | MIME info for stream, usually audio/mpeg.                                     |

</details>

You can use this library to make an application that fetches info from your Shoutcast server for analytical purposes.

{% hint style="info" %}
For web development and other cases where asynchronous code is acceptable, use the `Async` version of the functions as outlined in the beginning of this page to avoid blocking the main thread.
{% endhint %}

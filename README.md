---
icon: hand-wave
description: Welcome to BassBoom!
---

# Welcome!

<figure><img src=".gitbook/assets/BB.Cli.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
BassBoom will be upgraded with a new backend. It's in early development stage, so expect inconsistencies and bugs. You can track its development [here](https://github.com/Aptivi/BassBoom). For the mpg123 version, check [here](https://github.com/Aptivi/BassBoom/tree/x/oob/v0.2.x). Both v0.2.x and v0.1.x will be supported until the new version gets launched.
{% endhint %}

BassBoom is a music player made with C# using the fast mpg123 library as the native backend that handles the music playback and song information, including the playback device information.

This library is a viable library aimed for cross-platform music playing because we've selected mpg123 as the MP3 backend library for its ease of use and for its fast music playback. This library is frictionless as it aims for stability and cross-platform compatibility.

In addition to your regular music files, BassBoom also supports online MPEG radio stations that you can use to play your own favorite radio stations, as long as they don't use AAC or any other codec that BassBoom doesn't support.

{% hint style="info" %}
When using BassBoom, here are the notes to consider:

* This library only supports MPEG audio files. Unfortunately, this means no AAC and AAC+ support and no support for other non-MPEG audio files.
* If you found a radio station that only uses AAC, try to consult the radio station host for an MPEG version of the radio station stream, if available.
{% endhint %}

To learn more about mpg123, visit this site:

{% embed url="https://mpg123.de/" %}

## This documentation

To get started, select a page on the left edge of the screen to get started.

mpg123 is licensed with [LGPL 2.1](https://mpg123.de/trunk/COPYING).

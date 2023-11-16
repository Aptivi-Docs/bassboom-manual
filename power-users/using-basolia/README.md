---
description: How to use BassBoom.Basolia
---

# 💻 Using Basolia

Usage of the Basolia library may not look easy at first, but they will look easy once you get used to it and its syntax. In order to be able to use BassBoom Basolia functions, you need to initialize it using a function  called `InitBasolia.Init()`. This allows you to initialize the Basolia library either using your default executable directory or using your customized directory that contains the `runtimes` folder that contains the mpg123 libraries, such as in the case of Nitrocid.BassBoom addon.

{% code title="Somewhere in your code" lineNumbers="true" %}
```csharp
InitBasolia.Init();
```
{% endcode %}

A music player built with BassBoom is provided with the base BassBoom source code. You can read its source code [here](https://github.com/Aptivi/BassBoom/blob/main/BassBoom.Cli/CliBase/).

The Basolia library is categorized to five categories:

* Devices: Provides you functions that manipulate with the sound devices probed by the MPG123 library.
* File: Provides you functions that allow you to open and close the music file.
* Format: Provides you audio format tools, audio metadata tools, and audio decode tools.
* Lyrics: Provides you a basic lyrics (.LRC) support.
* Playback: Provides you playback functions, such as playing, pausing, and stopping the music.

Each category has its own page, so click on one of the pages in the left side pane.

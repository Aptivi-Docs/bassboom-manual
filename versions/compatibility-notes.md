---
description: If you want to upgrade, here's your guide to update your apps.
---

# 🗒 Compatibility Notes

When you upgrade BassBoom to a version that contains a higher API version that you have, you'll need to follow the compatibility notes.

## From 0.0.2.x to 0.0.3.x

When upgrading BassBoom from 0.0.2.x to 0.0.3.x, you need to consider the following changes:

### Removed fugitive mode

{% code title="InitBasolia.cs" lineNumbers="true" %}
```csharp
public static void Init(string root = "", bool Fugitive = false)
```
{% endcode %}

The Fugitive mode was implemented to enable dangerous operations, such as an ability to get music info while the music is playing. However, these operations cause MPG123 to error out with random errors, causing playback to be distorted.

As a result, we've removed fugitive mode.

{% hint style="danger" %}
We advise you to stop using this mode.
{% endhint %}

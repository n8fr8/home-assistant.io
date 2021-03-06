---
layout: page
title: "Sonos"
description: "Instructions how to integrate Sonos devices into Home Assistant."
date: 2015-09-12 13:00
sidebar: true
comments: false
sharing: true
footer: true
logo: sonos.png
ha_category: Media Player
featured: true
ha_release: 0.7.3
---

The `sonos` platform allows you to control your [Sonos](http://www.sonos.com) HiFi wireless speakers and audio components from Home Assistant.

To add your Sonos components to your installation, add the following to your `configuration.yaml` file.  It will perform auto-discovery of your connected speakers.

```yaml
# Example configuration.yaml entry
media_player:
  platform: sonos
```

You can also specify hosts to connect to if they cannot be found with auto-discovery.

```yaml
# Example configuration.yaml entry
media_player:
  platform: sonos
  hosts: IP
```

### {% linkable_title Service %}

There are two extra services exposed that will allow you to take a snapshot of what is currently playing and restore it afterwards. This is useful if you want to play a doorbell or notification sound and resume playback afterwards.

The services are called `sonos_snapshot` and `snapshot_restore`.

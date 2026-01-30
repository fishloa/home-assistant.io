---
title: Lyngdorf
description: Instructions on how to integrate Lyngdorf audio processors into Home Assistant.
ha_category:
  - Media player
ha_release: 2026.3
ha_iot_class: Local Push
ha_config_flow: true
ha_codeowners:
  - '@fishloa'
ha_domain: lyngdorf
ha_ssdp: true
ha_platforms:
  - media_player
  - number
  - select
ha_integration_type: device
ha_quality_scale: bronze
---

The Lyngdorf integration allows you to control Lyngdorf audio processors from Home Assistant.

Lyngdorf Audio manufactures high-end audio processors and amplifiers featuring advanced room correction technology called RoomPerfect. This integration provides control over power, volume, source selection, audio modes, and various audio processing parameters.

{% include integrations/config_flow.md %}

## Supported devices

The following Lyngdorf models are supported:

- MP-60 2.1 (author tested)
- MP-50
- MP-40
- MXA-8400
- TDAI-1120
- TDAI-2170
- TDAI-3400

## Entities

The integration will create the following entities:

### Media player

The media player entity provides control over:

- Power on/off
- Volume control
- Mute/unmute
- Source selection
- Media information display

### Number entities

Number entities allow you to adjust audio trim levels:

- Bass trim
- Treble trim
- Center trim
- LFE (Low Frequency Effects) trim
- Surround trim
- Height trim

Each trim control has a range of -120 to +120 (in 0.1 dB steps).

### Select entities

Select entities provide options for:

- **Audio mode**: Choose between None, Stereo, Party, and other audio processing modes
- **Source**: Select the active audio source
- **Zone source**: Select the source for zone 2 (if supported)
- **RoomPerfect focus**: Choose the RoomPerfect listening position
- **RoomPerfect voicing**: Select the RoomPerfect voicing preset

## Discovery

The integration supports automatic discovery via SSDP. If your Lyngdorf device is on the same network as Home Assistant, it will be automatically discovered and can be configured through the UI.

## Manual configuration

If automatic discovery doesn't work, you can manually add the integration by providing the hostname or IP address of your Lyngdorf device.

---
title: Room Testing
---

> [!CAUTION]
> This documentation is a work in progress.

## Equipment for testing

- Laptop to connect to A/V Net
  - Ethernet cable
  - HDMI cable
- Presentor laptop

## Procedure

- Open controller page
  - Adjust camera
  - Verify presentor disply
- Open mixer WebUI
  - Check levels, start from unity (0 gains and level)
- Open rtsp stream (in VLC or GStreamer)
  - Verify audio level
- Adjust room level as needed.

## Troubleshooting

### Speaker Hum

Symptom:
Hum or buzz over the room speakers when using the 3.5mm audio cable.

Resolution:
On the D1 box, flip the "lift" switch. If that fails to resove the issue, replace the D1 box.

Context:
The hum is most likely due to a ground issue.

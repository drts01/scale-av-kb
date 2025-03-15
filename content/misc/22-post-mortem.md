---
title: SCALE 22x Post-Mortem
description: A/V team Post-Mortem for SCALE 22x
linkTitle: 22x Post-Mortem
date: 2025-03-09
tags: [post-mortem, 2025, 22x]
---

## Post Con Retrospective

- Have signage inside the room
- Suggestions for tech would help with network setup, network mixer, camera and computer before network is set down.
- Checklist (some were missing) – Miguel to send email list to Carlos.
- Stops in tripods. (some photos would help of parts)
- Skirt instructions (installation and takedown)
- Some camera tripod mounts were missing the tightening screws.
- Room monitors- good number rotating.
- Thursday and Friday morning- not enough bodies- felt like couldn’t go to the sessions
- Have a radio at the monitoring station when in session
- Speaker reroute some of the equipment was an issue
- Triage process – not as clear at the monitoring station- when to report things. How and what.
- Digital recording of room monitoring issues. Intake form (google sheets, mothership)
- Adding monitoring levels to monitoring station screen
- Testing connection with monitoring station prior to speaker
- Red box to identify which room is actively being monitored
- Giant clock in Room and real time av contextual schedule.
- Window location persistence on monitoring station.
- Needing flashlight during setup.
- Timing from AV and network setup.
- Setup documentation (photos) / Teardown documentation (photos)
- Orientation before teardown
- Teardown check in process
- Radio checkout / checkin log
- Noting for different setup pieces
- Setup- some people want to see even if they are not on the list. (maybe create a video?)
- Headphones for testing laptops
- Setup- add photos to tech what we expect – location of switch etc.
- Redo bracket to protect line in on camera
- Waited for AVP and tech for setup
- What do we correct or delegate for setup (xlr cable, batteries, etc), what is our role?
- Training program for test leads- Caleb, Kenneth, BenBen, David and Ming
- Room tests- 106 people kicking the camera
- Improvement to webpage
- What responsibility during the week- who to go to ask to replace battery, etc.
- Hakeem/Kenneth- workshop setup- recording- clear expectations of what is being tested by the test leads.
- As setup leads- need to trust each persons’ work.
- Bug tracking system , rationale system. Some rooms were set up differently due to issues. So we know why thing were done. Put it on MPS google sheet.
- Need multiple screens in AV NOC. Calendar, google sheet etc.
- Proactive in a/v training, how to put on the mic. Room proctor training. Write in Phil’s notes and responsibility. Co-located room.
- Lan invented post-processing especially ff they have laptops. AV cutting.
- Several radios being returned with on- disruptive to the room.
- Better acknowledgement thru radios
- Wait time for UHAUL parking in front
- Monitoring relief was a frustration

## Carlos' Notes

- Request turning on A/C for A/V room durning setup
  - This should be possible as the Tech Team has A/C durning setup
  - Not having A/C is hard on the team and we enter the conference exhaugusted
- Repair tripods
  - Get 3D model files (from Dave?)
  - Print parts
- Get A/V team stickers
  - Swag
  - Use on our equipment
- Get velcro ties for podium cable managment
- Get HDMI cable tester
- Reprint podium sign on neon paper.
- Deligate more tasks to volunteers, i.e.:
  - Tape speaker notes to podium
  - Drop off and stand up tripods \
    (across from podium, avoid in between doors)
  - Drop off equipment (boxed)
    - mixer, A/V computer, camera
  - Pick up empty boxes
- Create a A/V monitoring dashboard
  - Pings to A/V box
  - Pings to mixers
  - Pings to cameras
  - Health checks to above mentioned equiment
- Dispose of old Samsung cameras
  - Sell
  - Donate
  - They are not apprciating in value and taking up space in storage
- Gather anonymous feedback from all volunteers
- Track setup, testing, and issues digitally instead of whiteboard
  - whiteboards are not always updated
  - inconsistent in how the information is presented
- Give room monitors printed instructions:
  - Which mics to use and why, headset is better for the recording and stream
  - How to use the handheld mic
  - MPS has asked use to update the [Room Proctor info](https://docs.google.com/document/d/1MdhXHYx6t4aTHzSjjKjJb_FyJtoZZTu1q43u8xeWxNw/)
- Improve setup staffing structure:
  - point person in A/V room w/ 2 runners
  - 2 setup leads (one per building)
  - 2 addition volunteers for a 3 person setup team \
    (1 person to connect computer, another for the mixer, and another for the camera)
- Improve NOC station
  - Make it obvious which window is active by modifying desktop environment
  - Use a tileling window manager for VLC streams to make layout consistant
  - Enable focus following mouse to select active window to make easy to switch active room
  - Larger mouse icon to make it easier find
  - Enable Ctrl mouse find

### Room

- Post radio channels for Tech, A/V, A/V Vendor (if applicable)
- Put a sign to be considerate of the noise level
- Setup desible meter for the A/V room.
- Do not allow non-A/V team people to rumage through the room
- A table was block and not usuable by the A/V team all of Sunday

### Testing Laptops

- Resolve laptops had issues
  - Disable power save mode
  - gstreamer-play reports computer may be too slow
    - Tune kernel and use non-free drivers
      - [Configure VA-API Video decoding on Intel](https://fedoraproject.org/wiki/Firefox_Hardware_acceleration#Configure_VA-API_Video_decoding_on_Intel)
      - [Intel Graphics - Best practices and settings for hardware acceleration?](https://discussion.fedoraproject.org/t/intel-graphics-best-practices-and-settings-for-hardware-acceleration/69944)
        ```
        options i915 enable_guc=2
        options i915 enable_fbc=1
        ```

#### Setup notes

- Pin applications
  - Web browser
  - VLC
- Local copy of docs/bible
- Local test video
- Local html w/ :
  - links to room mix
  - links to stream feed
- create simple tui to launch any room with `clvc` or `gst-play-1.0`
- VLC open history with all the rooms
- Disable IPv6
- Set sleep / logout
- Set SCALE WiFi to share w/ all users
- install `gstreamer1-plugins-base-tools`
  - `gst-play-1.0 rtsp://room-105-cam.scaleav.us/1`

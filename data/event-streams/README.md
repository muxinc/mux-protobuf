<p align="center">
  <a href="https://mux.com/">
    <img src="https://avatars.githubusercontent.com/u/16199997?s=200&v=4" alt="Mux Logo">
  </a>
</p>

# Mux Data Event Stream

Events are activities that happen during the course of a video view. A comprehensive list of events is available in the [Mux Data Docs](https://docs.mux.com/docs/mux-playback-events). Note that you may receive events not mentioned in the documentation.

Each event will include the following details:
- Type (name of event)
- Event sequence number
- Server time (timestamp of when the event was received by Mux servers)
- Viewer time (timestamp of when the event occurred on the device)
- Playhead time (position in the stream)
- At most one of the following additional details:
  - Device orientation info, in the case of an ‘orientationchange’ event
  - Rendition info, in the case of a ‘renditionchange’ event


[Proto v1](proto/v1/eventstream_v1.proto)

Version 1 Event Stream proto spec.


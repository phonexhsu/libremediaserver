# Introduction #

Libremediaserver is a software to manage visuals and audio in a real time context: stage arts, concerts, events, art instalations, visual jockeys,...

<lms is controlled through the [Open Lighting Arquitecture](http://opendmx.net/index.php/OLA), so we have a lot of lighting protocols and/or USB-DMX devices to choose: ArtNet, Open Sound Control, PathPort, ShowNet, ACN, Enttec USB DMX Pro, Velleman usbdmx, Anyuma, DMXKing,...

Libremediaserver uses Pure Data and Gem running in the background like audio and video engine. Communicates with Pure Data process trough Unix Domain Sockets

Requires an OpenGl capable grapics card and the driver correctly installed.

# Features #

  * Free Soft. GPL License.
  * 8 video layers + 8 audio layers.
  * Each video layer can play one video, one picture or one line of text.
  * Video formats: mov, mpeg, ogg, mp4, avi
  * Audio formats: ogg
  * Picture formats: jpeg, tiff
  * Each video layer can be maped by 4 Bézier points.
  * Position (16 bits), rotation in 3 axis, and size channels.
  * Advanced playback: Entry and exit points, loop or one shot modes, normal, backwards or ping-pong modes, speed playback.
  * Diferents alpha blending methods.
  * High pass and low pass pixel filters by RGB (luma, croma and masks).
  * CITP/MSEx 1.0: Thumbnails and mix preview.
  * Video previews in GUI.

<img src='https://libremediaserver.googlecode.com/files/libremediaserver_v004_red.png' alt='libremediaserver screenshot'>
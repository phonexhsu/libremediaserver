# Introduction #

LMS is a program to manage visuals and audio in a real time context: stage arts, concerts, events, art instalations, visual jockeys,...

We can control it through the [Open Lighting Arquitecture](http://opendmx.net/index.php/OLA), so we have a lot of lighting protocols and/or USB-DMX devices to choose: ArtNet, PathPort, ShowNet, ACN, Enttec USB DMX Pro, Velleman usbdm, Anyuma, DMXKing,...

LMS uses Pure Data and Gem runnig in the background like audio and video engine. Comunicates with pure data process trough TCP and Unix Domain Sockets

The supported platforms are Debian Wheezy and Ubuntu Precise 12.04 LTS

Requires an OpenGl capable grapics card and the driver correctly installed.

# Features #

  * Free Soft. GPL License.
  * 8 video layers + 8 audio layers.
  * Each video layer can play video, picture or one line of text.
  * Video formatas: mov, mpeg, ogg, mp4, avi
  * Audio formats: ogg
  * Picture formats: jpeg, tiff
  * 16 video effects.
  * Each video layer can be maped by 4 Bézier points.
  * Position (16 bits), rotation in 3 axis, and size channels.
  * Advanced playback: Entry and exit points, loop or one shot modes, normal backwards or ping-pong modes, speed playback.
  * Diferents alpha blending methods.
  * High pass and low pass pixel filters by RGB (luma, croma and masks).
  * Volume control in 16 bits and logaritmic.
  * CITP/MSEx 1.0: Thumbnails and mix preview.
  * Videp previews in GUI.

<img src='https://libremediaserver.googlecode.com/files/libremediaserver_startup_capture.png' alt='libremediaserver screenshot'>
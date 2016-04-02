## Introduction ##

LibreMediaServer needs some packages and some settings to work. In the folder "scripts" there are two scripts to install in Precise and Debian, but you can do it at hand if you prefer it. You need root to install.

## Ubuntu Precise 12.04 LTS ##

  * The script is named install\_precise.sh
  * Add the Open Lighting Arquitecture repository to your Apt sources list: echo deb http://apt.openlighting.org/debian/ precise main" >> /etc/apt/sources.list
  * Update the sources: apt-get update
  * Install: apt-get install ola puredata libqtcore4 libqtgui4 libav-tools libmagick++4
  * If apt asks you to init olad at startup, answer "no".

## Debian Wheezy ##

  * The script is named install\_wheezy.sh
  * Install the ola package from the "script" folder: dpkg -i ola\_0.8.26-1\_i386.deb
  * If dpkg asks you to init olad at startup, answer "no".
  * Install dependencies: apt-get -f install
  * Install: apt-get install puredata libav-tools libqtcore4 libqtgui4 libmagick++5

## Setting ##

  * The media files have to be in a special folder tree. See example media folder tree in the downloads page or the manual.txt to see the structure for it.
  * You need set up the path to your medias in the script make\_thumbs.sh and run it to generate the thumbs for your media. This is only for CITP/MSEx, if you are not planning using it you can skip this step.
<img src='http://libremediaserver.googlecode.com/files/libremediaserver_startup_capture.png' alt='LibreMediaServer Screenshot' height='500' width='600'>
<ul><li>Run libremediaserver executable file and set up the path to you medias with the "Change Media Path" button. Set up the ola universe, the window configuration and the DMX address by layer. The IP address configuration is used to determine the interface will be used for CITP/MSEx. "0.0.0.0" will work in all the network interfaces.<br>
</li><li>You need patch the OLA universe to the protocol/device you want use. Point a web browser to localhost:9090, set up one universe in input mode and bind to you prefered lighting protocol/device, or two universes if you want use the audio and the video at the same time. You can test the input data is arriving correctly in the tab "DMX Monitor".<br>
<img src='http://opendmx.net/upload/f/f9/Llad_home.png' alt='ola configuration page'>
</li><li>This setup process is only needed the first time. The setup will be recorded and will be loaded at startup.<br>
</li><li>Then you can init the video/audio process clicking in "video" or "audio", and when you see "Loadbang received" in the terminal, click in "ReadDMX" and "Window". Click in "Init CITP/MSEx" to start the Peer Information Socket and the protocol.</li></ul>

It should be working now...
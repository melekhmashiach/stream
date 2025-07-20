# stream

stream desktop audio over network

// check your audio device

pacmd list-sources | grep name

//run on server machine

cvlc -vvv pulse://alsa_output.pci-0000_00_1b.0.analog-stereo.monitor –live-caching 100 –sout ‘#standard{access=http,mux=ogg,dst=0.0.0.0:8080}’

//run on client (put your server ip)

cvlc http://___.___.___.___:8080/

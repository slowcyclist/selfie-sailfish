# selfie-sailfish
minimal python script showing how to control the camera with gstreamer in sailfish phones

The simple selfie.py script takes a selfie after 1 second (the time for the camera to adjust focus and brightness)

It builds a gstreamer pipeline connecting the camera (droidcamsrc) viewfinder pad to a fakesink and the photo pad to a filesink, and triggers the shot ("start-capture") after a delay. When the "photo-capture-end" message is seen, the program quits.

The HDR.py script is a simple variation on the above, using the main camera and a "multifilesink". It shoots a series of pictures with different exposure correction. Needs to be operated on a fixed stand. Note : I do not claim it is actually suited for HDR photography, it is just a toy example. For practical HDR shots, one would want many more things : a real viewfinder, freeze the focus between shots, etc.

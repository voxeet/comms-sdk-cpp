# Dolby.io Communications C++ SDK

The Dolby.io Communications C++ SDK provides both Client and Server applications the ability to create HD voice and video for fully immersive real-time communications and streaming experiences. The C++SDK allows creating an application that can join Dolby.io conferences.

The C++ SDK is responsible for communicating with the Dolby.io backend and providing conferencing functionalities, such as opening and closing sessions, joining and leaving conferences, sending and receiving messages, as well as
receiving and injecting WebRTC media streams.

Currently, an instance of the C++ SDK can connect to only one conference at a time. Joining multiple conferences at a time requires running multiple instances of the application.

## Client Applications

Using the Dolby.io Communications C++SDK Client applications have the ability to join Dolby Voice Conferences where they can send and receive HD voice streams, including spatial audio and shared scenes. This functionality is useful for integrating the HD Dolby Voice experience into your own game engine or virtual world experience.
To offer this functionality, the C++ SDK provides applications the ability to capture and playback audio, manage input/output Audio Devices, add spatial placement for participants as well as partake in a shared spatial scene.

## Server Applications

Using the Dolby.io Communications C++ SDK, Server applications have the ability to record and store high-quality voice and video calls on your server. This functionality is especially useful if you want full control over the audio and video recording. The C++ SDK also provides the ability to inject audio and video streams from the server into the conference. This functionality can be used to inject the audio and
video stored in some media file on the server into the conference. After joining a Dolby.io conference, the C++ SDK offers the functionality to record the incoming audio and video streams for desired conference participants. This application runs in your infrastructure and not on Dolby.io.

For information about building basic applications using the C++ SDK, see the [Getting Started](https://dolbyio.github.io/comms-sdk-cpp/other/getting_started.html) guide.

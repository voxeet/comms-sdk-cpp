# Dolby.io Communications Server C++ SDK

The Dolby.io Communications Server C++ SDK provides the ability to record and store high-quality voice and video calls on your server. This functionality is especially useful if you want full control over the audio and video recording.

The Server C++ SDK allows creating an application that joins Dolby.io conferences and records the incoming audio and video streams for desired conference participants. This application runs in your infrastructure, not on Dolby.io.

The Server C++ SDK is responsible for communicating with the Dolby.io backend and providing conferencing functionalities, such as opening and closing sessions, joining and leaving conferences, and receiving WebRTC media streams. To record conferences, the SDK uses a Media Recorder that allows processing and storing video frames from the incoming WebRTC media streams. The Server C++ SDK provides a default media recorder plugin and access to the Media Recorder API to create a custom Media Recorder. The default media recorder plugin is a ready-to-use library that can be easily configured and included in an application. The plugin automatically records the incoming media streams for conference participants and stores the recorded streams in either raw or encoded format. If you have specific recording requirements, use the Media Recorder API to create a custom recording module.

For information about building a basic application using the Server C++ SDK, see the [Getting Started](https://docs.dolby.io/communications-apis/docs/scpp-getting-started) guide.

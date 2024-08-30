# :warning: This repository is no longer maintained :warning:

# Dolby.io Communications C++ SDK

[Reference Documentation](https://api-references.dolby.io/comms-sdk-cpp/index.html)

[Getting Started Guide](https://api-references.dolby.io/comms-sdk-cpp/other/getting_started.html)

The Dolby.io Communications C++ SDK provides applications with the ability to create high-quality voice and video for fully immersive real-time communications experiences. The C++ SDK allows creating an application that can join Dolby.io conferences.

The C++ SDK is responsible for communicating with the Dolby.io backend and providing conferencing functionalities, such as opening and closing sessions, joining and leaving conferences, sending and receiving messages, as well as receiving and injecting WebRTC media streams.

Currently, an instance of the C++ SDK can connect to only one conference at a time. Joining multiple conferences at a time requires running multiple instances of the application.

Core SDK
========
The [Core C++ SDK](https://api-references.dolby.io/comms-sdk-cpp/api/coresdk.html) handles all of the signalling with the Dolby.io backend as well as providing various events, messages and other valuable information to users. The Dolby.io Communications C++ SDK allows joining Dolby Voice Conferences where participants can send and receive high-quality voice streams, including spatial audio and shared scenes. This functionality is useful for integrating the Dolby Voice experience into your own game engine or virtual world experience. The C++ SDK provides applications with the ability to capture and playback audio and video, manage input and output audio devices and input video devices, add spatial placement for participants, as well as partake in a shared spatial scene.

The Audio captured using the Core C++ SDK features is processed using Dolby Voice audio processing, allowing for clear, crisp conversations without echo or background noise and provides the option to use Dolby's world class 3D audio spatialization.

The C++ SDK offers full control of the video capture pipeline to applications. For instance, allowing developers to implement video filters and apply them to a user’s camera feed. As part of our documentation we provide [an example](https://api-references.dolby.io/comms-sdk-cpp/other/getting_started.html#video-processor) of how this can be done.

Media IO
========
In addition to the Core features, the Dolby.io Communications C++ SDK also provides [Media IO](https://api-references.dolby.io/comms-sdk-cpp/api/media_io.html) features. These include injecting audio from custom sources into conferences, connecting audio sinks to receive decoded PCM audio data and receiving encoded video frames before they are decoded. These features allow applications to connect as a client to a Dolby.io conference and record all of the present participants' video and audio. Think of it as recording a conference on your own machine without needing to pay for recording minutes. Additionally, you can inject some media from an external source (a file for instance) into the conference (especially applicable for Virtual Worlds for example). Note that using the Media IO features for Audio currently forces the use of the Opus Codec.

Plugins
=======
The C++ SDK also allows applications to make use of our ready-to-use [plugins](https://api-references.dolby.io/comms-sdk-cpp/api/plugins.html#plugins-api). The C++ SDK provides a default media recorder plugin: a ready-to-use library that can be easily configured and included in an application. The plugin automatically records the incoming media streams for conference participants and stores the recorded streams in either raw or encoded format.

The C++ SDK provides two default media injection plugins that are able to receive raw media frames and pass them to the SDK. One of the default plugins is the Pacing Injector. This injector exposes interfaces for an application to provide the injector with decoded audio and video frames. Then, the injector provides these frames into the SDK at specified intervals. The other default plugin is the Passthrough-Injector, which exposes interfaces for passing decoded audio/video frames that are directly provided to the SDK.

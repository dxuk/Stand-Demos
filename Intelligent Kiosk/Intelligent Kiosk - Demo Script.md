UNDER CONSTRUCTION
# Intelligent Kiosk Realtime crowd demo
This goes through one portion of the Intelligent Kisos demo, the Realtime crowd demo is a usefull way 
of showing a group of people how to use the face and emotion API.



Technologies: **Microsoft Cognitive Services (Age, Gender, Emotion, Face Identification and Face Tracking)**

Technical Depth: **Some Familiarity with UWP**

Time: **5 minutes**

Software: **Visual Studio 2015 with the Windows SDK installed**

Hardware: **Webcam**

Video: 
 
Supporting files: N/A

Accounts: Face API Key: Emotion API Key: Workspace ID: 6fa46477-3e06-4a81-8d45-b0a8dc25d384

## Setup
1. Download the app from: https://github.com/Microsoft/Cognitive-Samples-IntelligentKiosk
2. Go to settings in the app and add the Workspace Id, Face API and Emotion API above.


## Explain the demo
A realtime workflow for processing frames from a web camera to derive realtime crowd insights such as demographics, emotion and unique face counting. 
The sample uses a hybrid approach in order to obtain a fluid user interface. It calls the APIs at a rate of 1fps to compute age, gender, identification and emotion of all the faces in the frame, but it uses the built-in face tracking in Windows 10, running at 15fps, to associate and display the metadata about each face as the faces move around (using a simple heuristic based on the geometry of the faces).
This sample also shows how to use FaceLists to track unique faces.

- RealTimeDemo: Main page that drives the demo. It hosts the CameraControl (see below) to display the live camera feed, creates a background loop to capture and process frames from the camera at 1fps, implements the IRealTimeDataProvider interface used by the camera control to visualize data in realtime and maintains state about the demographics and overall stats.
- CameraControl: The code that contains the camera feed and runs a background loop to perform several tasks (track faces, draw face rectangles and display the realtime data about each face).
- FaceListManager: A management layer on top of the FaceList functionality.
- EmotionResponseTimelineControl: The control that displays the Crowd Average Emotion Timeline.
- AgeGenderDistributionControl: The control that displays the Demographis data.
- OverallStatsControl: The control that displays the Overall Stats data.
- RealTimeFaceIdentificationBorder: The control that displays the realtime feedback over the faces in the camera feed. It consists entirely of text elements - even the emotion feedback is just using an emoji font (see EmotionEmojiControl).
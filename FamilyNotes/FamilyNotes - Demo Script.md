# Family notes app demo
-------------------------

** This demonstrates using the camera and speech features in UWP to filter and add user-centric notes in a Universal Windows App as well as the Cognitive Services Face API for facial recognition.**

Technologies: **Universal Windows Platform**

Technical Depth: **None, Pre-Canned**

Time: **5-10 minutes**

Software: **Windows 10, FamilyNotes app**

Hardware: **Standard Camera, Microphone**

Supporting files: **N/A**

Accounts: Configure the machine under ONE demo account.


App Setup
---------
1. Download either the source and build / run in VS2015 (from this repo https://github.com/Microsoft/Windows-appsample-familynotes)

OR get the precompiled version from https://devdemwfnstac.blob.core.windows.net/fdddemo/FamilyNotes_1.0.0.0_Debug_Test.zip

** Note that not all of the features work in the debugger, some only seem to work once installed (Dictation), and some will silently fail if you enter an incorrect Face API key with no error message as the code seems to randomly swallow exceptions from the face api (but hey its demo code right!).

2. Install the app and let it set up it's cortana actions on first run.
3. Run the app and hit the setup button (the cog on the bottom right)
4. Paste the API key for the Cognitive Services Face API into the correct box.
5. To turn on Face Detection / Recogition, Click the picture frame icon on the bottom right

** Will has a key pre-setup that you can use if you need one. **

Create a dummy note for *Everyone* 

Select the everyone user in the top left of the screen.

Select the new note icon in the bottom left hand corner of the screen and set up both a text and an inked note.

Per Face User Setup
-------------------
You need to add YOUR account / face to the machines being used to demo in the MPC area and set up some notes

1. Click the New Person Icon (Third from the bottom right)
2. Enter your name and click 'Take Snapshot', then get a decent piccie! (this uses the CameraCaptureUI API https://msdn.microsoft.com/en-us/library/windows/apps/windows.media.capture.cameracaptureui.aspx)
3. Then click 'Add', at this point your Face is added to a FaceList in Project Oxford. https://dev.projectoxford.ai/docs/services/563879b61984550e40cbbe8d/operations/563879b61984550f30395250


This will set up your face and account.

Then set up some notes :- 

1. Select your user on the left hand side of the screen that you just created.
2. Select the new note icon in the bottom left hand corner of the screen and set up both a text and a inked note.


Explain the demo
----------------
** There are 4 key points to this demo. ** 

Face Detection, Facial Recognition, Cortana, Voice Dictation, Ink Notes 

#1... Face Detection / Recognition 

1. Ensure that 'Everyone' is the selected user, and that two or more people are visible to the camera (the bottom bar should light up with 'Detected Faces : x' and nothing should be selected yet. 

The app is using the MediaCapture API here, to take pictures without displaying the UI of the camera. 
https://msdn.microsoft.com/en-us/library/windows/apps/windows.media.capture.mediacapture.aspx

Explain the privacy implications and toggle the capture button on the bottom right

2. Now if your demoee moves away from the screen, the app should recognise YOU, and highlight your notes only, and greet you by name.

What has happened here is that the app has used the FaceDetectionEffect api https://msdn.microsoft.com/en-us/library/windows/apps/windows.media.core.facedetectioneffect.aspx to count the number of faces in the camera input stream (this makes sure that there is only one person looking at the screen), then used the Cognitive Services Face - Find Similar API to work out who it is. 

https://dev.projectoxford.ai/docs/services/563879b61984550e40cbbe8d/operations/563879b61984550f30395237

Then the app can highlight the appropriate notes for that user.

Now turn away from the camera (everyone) so there are no faces detected, and after a short while - the notes will unfilter back to 'everyone'. 

# 2 ... Cortana Integration






** Code snippets and examples can be found here **

https://blogs.windows.com/buildingapps/2016/06/28/familynotes-using-the-camera-to-detect-a-user/#qwXMzWAgi5XfOrQM.97


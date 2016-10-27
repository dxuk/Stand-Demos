# Family notes app demo
-------------------------

** This demonstrates using the camera and speech features in UWP to filter and add user-centric notes in a Universal Windows App as well as the Cognitive Services Face API for facial recognition.**

Technologies: **Universal Windows Platform**

Technical Depth: **None, Pre-Canned**

Time: **5-10 minutes**

Software: **Windows 10, FamilyNotes app**

Hardware: **Camera, Microphone**

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

** Will has one pre-setup that you can use if you need one. **

Create a dummy note for *Everyone* 

Select the everyone user in the top left of the screen.

Select the new note icon in the bottom left hand corner of the screen and set up both a text and an inked note.

Per Face User Setup
-------------------
You need to add YOUR account / face to the machines being used to demo in the MPC area and set up some notes

1. Click the New Person Icon (Third from the bottom right)
2. Enter your name and click 'Take Snapshot', then get a decent piccie! 
3. Then click 'Add' 

This will set up your face and account.

Then set up some notes :- 

1. Select your user on the left hand side of the screen that you just created.
2. Select the new note icon in the bottom left hand corner of the screen and set up both a text and a inked note.


Explain the demo
----------------
** There are 4 key points to this demo. ** 

Face Detection, Facial Recognition, 


** Make the following points clear:- **

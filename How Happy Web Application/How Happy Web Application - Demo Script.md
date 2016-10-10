# How Happy Web Application
HowHappy.co.uk is an ASP.Net web application that uses the Emotion API and Language Understanding Intelligent Service API (LUIS) from Microsoft Cognitive Services to assess and  order with human faces in a group photo. In this demo you'll take a photo using the device's camera or optionally upload a file which you'll then use the HowHappy.co.uk web site to explore the emotions shown in the photo. You'll also look at the LUIS backend model that supports the application.

Technologies: **Microsoft Cognitive Services (Emotion and LUIS)**
Technical Depth: **Anyone**
Time: **5 minutes**
Software: **Edge Browser**
Hardware: **Webcam good to have, but not mandatory**
Supporting files: **a-justin-bieber-concert-summed-up-in-one-picture.jpg**(only needed if the device does not have a web cam)
Accounts: **FDStand2016@outlook.com** (password is **FutureDecoded2016**)

## Take a photo
Using the devices 'camera' app, take a photo.

The more human faces in the photo, the better (aim for at least 3, but less than 64). If you are demonstrating to a single person, get some other stand volenteers in the photo.

If you cannot take a picture, use **a-justin-bieber-concert-summed-up-in-one-picture.jpg**

## Explore the Emotion API
Key talking points:
* The emotion api assess 8 emotions shown in photos of human faces
* The emotions detected are anger, contempt, disgust, fear, happiness, neutral, sadness, and surprise. These emotions are understood to be cross-culturally and universally communicated with particular facial expressions.
* It will recognise up to 64 faces
* It return JSON showing the location of each face on the photo and a score for how strongly each emotion is being shown on each face

---

Visit https://www.microsoft.com/cognitive-services

Go to Apis > Emotion

Use the test application (about half way down the page) to upload the photo you just took

Explore the result
* Faces are identified using coloured rectangles
* Each face is asses for their score on 8 emotions
* The result is given in JSON format

## Upload to HowHappy.co.uk
Key talking points:
* Simple ASP.net web application that uses the Emotion and LUIS apis
* Uses LUIS to convert natural language to one of 4 'intents'
* Uses emotion API to sort faces based on emotio
---

Visit http://HowHappy.co.uk

Upload the photo

Explore the initial result which will show all faces sorted by happiness
* Note how many faces were detected
* Notice that happiness is the default emotion used
* Click on random faces and see the full set of emotions for the selected face

Type "Who is the happiest one here"
* Note that only the happiest person is highlighted

Type "Show me all the angry people"
* Note that all the faces are highlight and ranked based on level of anger shown

Type "Who is the 3rd most surprised person"
* Note that the emotion is now surprised and we're singling out the 3rd most surprised person

Type "Show me the least happy person"
* Happiness is the emotion again
* This time we're looking for the least happiest

## Explore the LUIS model
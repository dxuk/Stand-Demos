# ExcelBot
Excelbot demonstrates the use of a chat bot /conversational UI to enable to the user to interact with an Excel Workbook using natural language queries from various channels including Skype, Facebook and web.
Access to the workbook is via the Microsoft Graph API (O365).


Technologies: **Microsoft bot Frameowork, Microsoft cognitive services (LUIS), Microsoft Graph API (AAD authentication, Onedrive for Business, Excel) **

Technical Depth: **Anyone**

Time: **5 minutes**

Software: **Edge Browser**

Hardware: **None**

Video: **Coming soon**
 
Supporting files: **[loancalc.xlsx](https://raw.githubusercontent.com/dxuk/Future-Decoded-2016-Stand-Demos/master/ExcelBot/loancalc.xlsx)** 

Accounts: **need to authenticate using Microsoft Corp account** 

## Set-up
These steps should already have been done but for cases where it has not:

1. Copy the loancalc.xlsx file to the root of your Corporate Onedrive for Business.


## ExcelBot demo
Key talking points:
* The emotion api assess 8 emotions shown in photos of human faces
* The emotions detected are anger, contempt, disgust, fear, happiness, neutral, sadness, and surprise. These emotions are understood to be cross-culturally and universally communicated with particular facial expressions.
* It will recognise up to 64 faces
* It return JSON showing the location of each face on the photo and a score for how strongly each emotion is being shown on each face

---

1. Visit https://www.microsoft.com/cognitive-services

2. Go to Apis > Emotion

3. Use the test application (about half way down the page) to upload the photo you just took

4. Explore the result
  * Faces are identified using coloured rectangles
  * Each face is asses for their score on 8 emotions
  * The result is given in JSON format

## Upload to HowHappy.co.uk
Key talking points:
* Simple ASP.net web application that uses the Emotion and LUIS apis
* Uses LUIS to convert natural language to one of 4 'intents'
* Uses emotion API to sort faces based on emotion

---

1. Visit http://HowHappy.co.uk

2. Upload the photo from the start of the demo

3. Explore the initial result which will show all faces sorted by happiness
  * Note how many faces were detected
  * Notice that happiness is the default emotion used
  * Click on random faces and see the full set of emotions for the selected face

4. Type "Who is the happiest one here"
  * Note that only the happiest person is highlighted

5. Type "Show me all the angry people"
  * Note that all the faces are highlight and ranked based on level of anger shown

6. Type "Who is the 3rd most surprised person"
  * Note that the emotion is now surprised and we're singling out the 3rd most surprised person

7. Type "Show me the least happy person"
  * Happiness is the emotion again
  * This time we're looking for the least happiest

## Explore the LUIS model
Key talking points:
* LUIS converts natural language to an intent and set of entities
* Train the model using a few sample utterances
* Publish as a rest API which returns JSON

---

1. Go to https://www.luis.ai/

2. Login in as **FDStand2016@outlook.com** (password is **FutureDecoded2016**)

3. Open the How Happy LUIS model
  * An export of the model is also avaliable here: 

4. Explore the intents

5. Explore the entities
  * `Emotion` the 8 emotions that the model is trained for
  * `Ordinal` a built in numeric entity tat allows use to say things like "2nd happiest"

6. Enter "Show me the angriest people" as a `New Utterance`
  * The tag "angriest" as the "angry" emotion enity
  * Ensure the `SortedByEmotion` intent is selected

7. Review labels
  * Show previously labelled utterances

8. Train 

9. Publish

10. Add "Show me the angriest people" as a query and show JSON result

11. Go back to the main website and search for "Show me the angriest people"

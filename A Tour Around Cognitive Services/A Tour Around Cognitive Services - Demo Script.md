# A Tour Around Cognitive Services
This demo uses the sample apps provided in the Cognitive Services web site to show the range of APIs. This demo can be as short or as long as required and requires very little prep. These are some of the more interesting / significant API functions.

Technologies: **Microsoft Cognitive Services**

Technical Depth: **Anyone**

Time: **1-20 minutes**

Software: **Edge Browser**

Hardware: **None**

Video: **[To do]()**
 
Supporting files: **None**

Accounts: **None**

Background notes: **Use your choice of the sample images, videos, text etc provided in [microsoft.com/cognitive-services](https://www.microsoft.com/cognitive-services) to showcase the APIs using the built-in sample apps. Optionally, you could use photos takes on the devices camera app for the apis that require pictures of humans or scenes**

## Computer Vision > Analyse an image
Analyses the content of an image

Key Talking Points
* Identifies the subjtect matter of the image via description and tags
* Adult/Racy Score and content flags
* Categories
* Built-in Face API call for human faces
* Colours

## Computer Vision > Recognise Celebrities
Built on the computer vision API with a domain-specific mode. This API is able to identify celebrities

Key Talking Points
* Trained with 200k celebrities
* Identifies celebrity and provides found rectangle bounds

## Computer Vision > Read text in images
OCR capabilities

Key Talking Points
* OCR for most text types

## Computer Vision > Generate a thumbnail
Resizes images to dimensions specific, optionally centering on eth region of interest

Key Talking Points
* Specify your own width and height dimensions
* Enable smart cropping to focus on the region of interest

## Emotion > Recognize Emotions in Images 
https://www.microsoft.com/cognitive-services/en-us/emotion-api
Recognises and scores emotions in humans faces in photos

Key Talking Points
* Anger, contempt, disgust, fear, happiness, neutral, sadness, and surprise
* > 64 faces
* Supports video by uploading individual frames
* Free for 30,000 API calls or 300 videos per month

## Face > Face Detection 
https://www.microsoft.com/cognitive-services/en-us/face-api
Detect one or more human faces in an image and get back face rectangles for where in the image the faces are, along with face attributes which contain machine learning-based predictions of facial features

Key Talking Points
* Age, Gender, Pose, Smile, and Facial Hair along with 27 landmarks for each face in the image
* Free for 30,000 API calls per month

## Face > Face Verification  
https://www.microsoft.com/cognitive-services/en-us/face-api
Check the likelihood that two faces belong to the same person

Key Talking Points
* The API will return a confidence score about how likely it is that the two faces belong to one person
* Free for 30,000 API calls per month

## Face > Face Identification 
https://www.microsoft.com/cognitive-services/en-us/face-api
Search and identify faces. Tag people and groups with user-provided data and then search those for a match with previously unseen faces.

Key Talking Points
* Build a data set of known faces
* Free for 30,000 API calls per month

## Face > Similar Face Searching
https://www.microsoft.com/cognitive-services/en-us/face-api
Easily find similar-looking faces

Key Talking Points
* Free for 30,000 API calls per month

## Face > Face Grouping
https://www.microsoft.com/cognitive-services/en-us/face-api
Organize many unidentified faces together into groups, based on their visual similarity

Key Talking Points
* Free for 30,000 API calls per month

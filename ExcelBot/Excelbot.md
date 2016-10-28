# ExcelBot
Excelbot demonstrates the use of a chat bot /conversational UI to enable to the user to interact with an Excel Workbook using natural language queries from various channels including Skype, Facebook and web.
Access to the workbook is via the Microsoft Graph API (O365).


Technologies: **Microsoft bot Framework, Microsoft cognitive services (LUIS), Microsoft Graph API (AAD authentication, Onedrive for Business, Excel)**

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
2. Open a browser, navigate to http://aka.ms/excelbot and type 'hi'. If this is the first time then it will prompt you to authenticate. Click on the link which will open a seperate browser window.
Now enter your Corp credentials that correspond to the account that you have saved the excel file under. Once you see the sign-in successful message then return to the bot and re-type 'hi'. You should now
see the message 'Hi, <username>'.

## ExcelBot demo
Key talking points:
* Use of conversational UI (Bot framework) to interact with O365 documents - in this case Excel - but could be mail, calendar, one Note etc.
* The power of the Microsoft Graph API as a single endpoint for accessing user and document data within an O365 tenant.
* Use of natural language processing (LUIS) to allow for more natural conversational style interrogration of Excel sheet
* Ability to view and modify Excel sheet values
* Ability to request Excel sheet charts

---

1. Ensure that the loancalc.xlsx file is in the root of your Corp Onedrive for Business
2. In a browser (Edge or Chrome), navigate to the Excel sheet and display it in 2/3rd of the screen (left hand side)
3. Open a seperate a browser (Edge or Chrome) and navigate to http://aka.ms/excelbot and display this within the remaining 3rd of the screen (on right hand side)
4. You should now have the excel sheet on the left hand side and chat window on the right hand side - sitting side-by-side. Explain that whilst we are using this chat window as a web-frame, this could 
easily be made available in other channels such as Facebook messenger, Slack, Skype, Telegram etc. because we are using the MS Bot Framework.
5. Talk about the loancalc sheet - describe how it is a simple example that takes loan amount, interest rate and calculates payments
6. The Excelbot can be used to interact with the sheet, interrogate values and update them.
7. First type 'hi'. The bot should say 'Hi, <username>'. If not then you will need to authenticate by following steo 2 of the 'set-up' section above.
8. Type 'look at loancalc'. The bot should respond with 'ready to work with 'loan calculator in loancalc.xlsx'. This has used the Onedrive Graph API call to open the file ready for editing/viewing.
9. Type 'what is the value of C4'.The bot should return value of cell C4. Show the corresponding value in the sheet
10. Type 'what names are in the workbook?'. The bot should return a list of named ranges.
11. Type 'What is the value of 'totalloancost'? The bot will return the value of the totalloancost cell. Show the corresponding value in the sheet
12. Type 'change that to 7000'. The bot will confirm value has changed and you can show the value changing in the excel sheet in near real-time and all values updated.
13. Type 'What are the charts in the workbook?' . A list of charts are returned - in this case there is only one.
14. Type 'show me chart2'. The chart image is returned and you can click on this to open it larger in a seperate window

Emphasise the value of the conversational UI for simplifying both customer facing and internal task/processes.




# ics-final-2016
Final project for AP Computer Science 2016 class

# Prerequisites

1. Chrome browser
2. Google account - for example a gmail account and familiarity with using Google spreadsheets
2. Github account (if you do not have one) 
3. c9.io Cloud IDE account
   - Either: Use your Github account created above to sign up at c9.io
   - Or: Create a new c9.io account (with its own username and password) then go to this page to 
     connect your Gihub and c9.io accounts: https://c9.io/account/services

# Goals of the project
Create your own mobile web application that shows the list of restaurants in your vicinty as you're traveling. Learn how to use a Cloud IDE and create live HTML5 web site for testing.

# Milestone 0 - Fork the Github repository
1. Sign in to Github using your account created above (see "Prerequisites").
2. Go to this URL: https://github.com/surendermohan/ics-final-2016
3. Click "Fork"
4. This will allow you to create a copy of the entire project into your own Github account where you can make your own edits. 
   You will now have your own Github repository with a URL that looks something like:
   https://github.com/YOURNAME/ics-final-2016

# Milestone 1 - Clone base files from Github
1. Sign in to c9.io using your account created above (see "Prerequisites").
2. Click on "new workspace" or go this URL: https://c9.io/new
3. Enter "ics-final-2016" as the workspace name and "[your_name]'s Final Project" as description.
4. Keep the default for "Hosted Workspace" as "Public"
4. Enter the following Github the "Clone from Git or Mercurial URL" field: https://github.com/YOURNAME/ics-final-2016.git
5. Keep the default the "Choose a template" as "HTML5"
6. Click "Create Workspace" button

Congratulations! You cloned the project on c9.io. You will see this Readme file open in the IDE.

# Milestone 2 - Run your mobile web app
1. Select index.html file in the left pane of the IDE.
2. Press "CTRL-F" and find the word "TODO" 
3. Change the name "surender" in line 42 of index.html with your own name.
4. Press "Run" in the toolbar to start the Apache web server.
5. Notice the URL shown in the console below when the application runs.
>> Starting Apache httpd, serving https://ics-final-2016-surendermohan.c9users.io/index.html.
6. Your mobile web application is now live at this web site. You can verify it in your browser.
7. You should be able to access this URL (e.g. https://ics-final-2016-surendermohan.c9users.io) from your mobile phone also.
8. Share your workspace with RW (Read-Write) access to my c9.io account (username: surendermohan, email: smohan36@gmail.com). 
9. This will allow me to run your project. Share button in on the top right corner of the IDE after you open the workspace.

# Milestone 3 - Push your changes to your Github repository
1. In the "bash" tab at the bottom of the c9.io IDE, type the following:
   - git add index.html
     - (this tells Git that you have made some changes to index.html that you intend 
        to commit to the repository)
   - git commit
     - (this commits the changes you made to the local copy of your repository within 
        c9.io; type a short description of your change in the editor that appears, then
        press Control-O, Enter, Control-X to save your description and commit the change)
   - git push
     - (this pushes the changes you have commited in the local c9.io repository back
        to Github)
2. Go back to your Githib repository (see "Milestone 0") and verify that you can see
   your changes.

# Milestone 4 - Create your own Stores catalog
1. Login with your Google account in the Chrome browser.
2. This application reads the stores data from a Google Sheet located at https://docs.google.com/spreadsheets/d/1gLEpxDmimsuPdVNNvIpOgTUO9T5XL5qDIRdx6gPbM70/edit#gid=907053173
3. Open that spreadsheet and make copy by going to "File->Make a copy.."
4. Name it as "[your_name] Customers List" and check "Share it with same people". If you do not see the "Share it with some people" option, or forget to click it: After creating the copy, click on the "Share" button (in the top-right corener) and chose "On - Anyone with the link".
5. Now go back to index.html file in the c9.io and look for next "TODO"
6. Go to line 134 and replace the value of the customer sheet variable with the URL of your google sheet.
7. Save your changes, commit them and push them to Github (see "Milestone 3")

# Milestone 5 - Modify name and location of 5-10 stores in your neighborhood
1. You will need to use Google Maps for this and then use "Right-Click"->"Whats Here" to get the Latitude and Longitude
2. Open the Spreadsheet you created for yourself and update columns A-H to modify a store from your locality
3. Open the web link of your application and you should see your nealy added store.
4. Repeat steps 2,3 for other stores
5. Document your steps to explain how you updated the stores.

# jsFiddle and Geolocation Learning Exercise
1. Go to http://doc.jsfiddle.net/tutorial.html and run the tutorial
2. Read about Geolocation at http://www.w3schools.com/html/html5_geolocation.asp
3. Try the code at http://www.w3schools.com/html/tryit.asp?filename=tryhtml5_geolocation
4. Create a jsFiddle for Geolocation based on the code in Part 3. Save it and add the link in your notes. (Note: you will have to split the file in HTML and JavaScript portions). For example: https://jsfiddle.net/cxjwj80c/

# Reading Exercise 
1. Read about HTML5 and CSS at high level.
2. Read about jQuery and JavaScript at high level.
3. Read about jQuery Mobile
4. There will be report due with short 100-200 words questions about these topics.

# YouTube Video for Chrome Debugging
1. Watch this video about Chrome Debugging https://www.youtube.com/watch?v=JzZFccCEgGA
2. We will then walk through the code for geolocationWatchSuccess_helper(lat, lng) function in s2m.js
3. (Optional) watch first 7 videos in this playlist: https://www.youtube.com/playlist?list=PL4cUxeGkcC9i9Ae2D9Ee1RvylH38dKuET 

# Milestone 6 - Fix various bugs and enable unit testing of code on pressing "Go"
##### Goal of this milestone is to fix some bugs in the code and learn how a developer would make temporary changes to test the code.
##### Bug-1: Mixed Content warning in console for the images
   - **Steps to reproduce:** (for my mobile app, your link will be different)
   - Open the application in Chrome at https://ics-final-2016-surendermohan.c9users.io/index.html
   - Open "Developer Tools" in Chrome by pressing "Ctrl+Shift+I" on Windows (or from the menu for Mac folks)
   - Open the Console tab (if it is not open) in the "Developer Tool"
   - Refresh the web page and notice the messages in the Console
   - **Actual Result:**
   - Following warning is thrown: Mixed Content: The page at 'https://ics-final-2016-surendermohan.c9users.io/index.html' was loaded over HTTPS, but requested an insecure image 'http://drive.google.com/uc?export=view&id=0B2SwyE8hza2BanJ4R3d0R2pCS3c'. This content should also be served over HTTPS.
   - **Expected Result:**
   - No Warning is thrown when the page is refreshed.

##### Bug-2: Stores display does not refresh on change of location 
   - **Steps to reproduce:** (for my mobile app, your link will be different)
   - Open the application in Chrome at https://ics-final-2016-surendermohan.c9users.io/index.html
   - Open "Developer Tools" in Chrome by pressing "Ctrl+Shift+I" on Windows (or from the menu for Mac folks)
   - Open the Console tab in the "Developer Tool"
   - Look up the Lat/Long of a store from your own catalog.
   - Update the Lat (first text box at the top) of that store in the application and press "Go"
   - You will notice that the display of stores changes the order.
   - Wait for the refresh interval (10 seconds by default) to kick in by noticing the updated status message
   - **Actual Result:**
   - The List of stores displayed does not change order.
   - **Expected Result:**
   - Stores should be displayed in the order of the distance when location gets updated.

# Milestone 7 - Push your changes to your Github repository
1. In the "bash" tab at the bottom of the c9.io IDE, type the following:
   - git add js/s2m.js (note that this Linux and folder takes a forward slash)
     - (this tells Git that you have made some changes to js/s2m.js that you intend 
        to commit to the repository)
   - git commit
     - (this commits the changes you made to the local copy of your repository within 
        c9.io; type a short description of your change in the editor that appears (e.g. Milestone 6), then
        press Control-O, Enter, Control-X to save your description and commit the change)
   - git push (enter your Github username/password, if required)
     - (this pushes the changes you have commited in the local c9.io repository back
        to Github)
2. Go back to your Githib repository (see "Milestone 6") and verify that you can see
   your changes.


##### Grading Rubric:
   - Total 100 points, with possibility to earn upto 20 MORE EXTRA CREDIT points until 6/10/2016, 11:59 PM)
   - 10 : Milestone 1
   - 20 : Milestone 2
   - 10 : Milestone 3
   - 20 : Milestone 5
   - 10 : Mobile App Part 1 description part.
   - 10 : Milestone 6 : Bug #1
   - 15 : Milestone 6 : Bug #2
   - 5  : Milestone 7 : Push your code back in your Github repo
   - Extra Credit - upto 20 points for Questions and Milestone 8


# Milestone 8 - Implement the feature to use ProximityRadius value from the Catalog (up to 10 points of Extra Credit)
##### Goal of this milestone is to implement a feature to use the ProximityRadius value read from the column V in the catalog.
##### Feature-1 Update s2m.js to use the proximity value read from the catalog instead of the hard-coded value of 300 to display the proximity notification.
   - Line 254 has logic to display the notification when the user is within the proximity of a store.
   - Code in this line is hard-coded to check for closestStoreDistance being less than 300
   - You are supposed to use the values stored in column V of your catalog instead of this hard coded value.
   - Hint: Take a look at the global variables being set in Lines 532-562 of s2m.js file and then figure out how you will use that information.
   


# Foodo
Food Donation App

## Table of Content
- [Proposed System](#proposed-system)
- [Activities](#activities)
  * [1. HOME PAGE](#1-home-page)
  * [2. DONATE](#2-donate)
  * [3. PICK-UP INFO](#3-pick-up-info)
  * [4. LOGIN](#4-login)
  * [5. DONOR INFORMATION](#5-donor-information)
  * [6. CHECK QUALITY](#6-check-quality)
  * [7. THANK YOU](#7-thank-you)
  * [8. ABOUT US](#8-about-us)
- [Database Structure](#database-structure)
- [Location API](#location-api)
- [Video](#video)

## Proposed System 

   The application ‘FooDo’ will first ask the user if they just want to donate some food (if they are a donor) or if they want to login as a volunteer (if the user is a volunteer). A user can also know more about the app by clicking on the ‘about us’ button.
  
  If the user is a volunteer, (s)he will have to login. Once (s)he logs in, they will be alerted of a new donation that requires a volunteer. If (s)he chooses to accept the delivery, (s)he will be asked to enter basic information, like his/her name, mobile number and current location. Once (s)he reaches the location of the donation, (s)he will have to check the quality of food and verify the quantity available. Once (s)he has delivered the food to the NGO, they will click on a button to confirm the completion of the delivery. If the user however is a new volunteer, (s)he can register by entering email-id, a password and his/her mobile number after which (s)he can login using the login page.
  
  If the user is a donor, the application will ask him/her to enter their full name, mobile number, address, type of food they are donating ( veg/ non-veg), and quantity (in number of people it will serve). After confirmation of the details, the donor will be taken to another page which will show the information about the pickup. The volunteer coming to pick up will also perform a quality check of the product so as to ensure the food delivered is in good condition. If the donation is verified, it is delivered to an NGO and the donor will get a notification and a thank you message. 

## Activities
### 1. HOME PAGE

This is the page that will open the moment you click on the application. 
This page will have three buttons: 1.Donate  2.Login   3.About us

### 2. DONATE 

After clicking on the donate button on the homepage user will be taken to this page. Here the user will have to enter the details about the donation he/she is about to make. It is compulsory for the user to enter the following details for smooth pickup of the donation:
* Full name of the donor
* Mobile number of donor
* Address 
* Type of food ( Veg/ Non-veg)
* Quantity of the donation ( in number of people it would feed)

	Once the user is done he/she can click on the button “Donate”  to go to the next page.

### 3. PICK-UP INFO

This page is displayed after the user enters the details for the donation. Here the user will find the details about the volunteer that is going to pick up the donation. The user will also be shown the volunteer’s phone number, in case he/she wants to contact them and, and the estimated time of arrival to the address entered in donation page. The donor now has to wait for the volunteer to come to the address and check the donation for quality and quantity. After the donated food is delivered to NGO, the donor will be taken to a Thank You page.

### 4. LOGIN

From the homepage, if a person wants to register/ login as a volunteer, they can click on the register button on the home page. This will take them to a form that asks for email address and a password to register. Here the system will check if the email already exists in the database, if not, the user is now registered as a volunteer. If the user is already exists, they can enter their credentials and login. Here, if the credentials don't match, the user will be displayed a message "invalid userid or password.

### 5. DONOR INFORMATION 

This is the page volunteer will be sent to after he/she logs into the app. Here they will get to know where their next pickup is and the phone number and name of the donor. To help the volunteer navigate to donor’s address, we have also added a google maps option.

### 6. CHECK QUALITY

Now that the volunteer has reached the donor’s address, the next task is to check for quality and the quantity of food. This page has a list of things that need to be checked like quality, quantity and the type of food. If the volunteer finds it okay, the donation can be taken to the NGO. 

### 7. THANK YOU 

By donating food, one makes sure that there is one less hungry person that day. After the donation reaches the NGO the donor will be directed to a thank you page which will tell the user that the donation was successful.

### 8. ABOUT US

This page will explain how to use this app to help those in need. 

## Database Structure 

We have created Two separate Databases for this application:
1. To store donation information
2. To store volunteer information

TABLES

1. Donor_info :
	1. Each donation has a unique ID which is the primary key. 
	1. The details submitted by the donor are stored in this table.
	
	D_fullname | D_mobile | D_address | D_type | D_quantity
	---------- | -------- | --------- | ------ | -----------
	
2. Volunteer_info :
	1. This table stores personal information about the volunteer.
	1. The volunteer id (V_ID) is the same id generated at the time of registration. 
	
	V_fullname | V_mobile | V_address 
	---------- | -------- | --------- 

3. Login_volunteer
	1. This table saves the volunteer’s details that he/she entered at the time of registration and uses them to match credentials while the volunteer tries to log in.
	
	V_email | V_password | V_mobile 
	---------- | -------- | --------- 
	
## Location API

FooDo uses the MAPS API from Google API package. As the app involves a volunteer going to a location specified by the donor, integrating maps into the app helps a lot. The API automatically handles access to Google Maps servers, data downloading, map display, and response to map gestures.

To mark the donor's or volunteer’s location on the map we use API calls to add markers, polygons, and overlays to a basic map, and to change the user's view of a particular map area. These objects provide additional information for map locations, and allow user interaction with the map. To request for user’s location from the device we have added a uses-permissions tag in the manifest file. The app will use the fine and coarse permissions.

Privacy is taken very seriously in our application and the app only uses and updates location data when required by the app. We notify the users when their location is being tracked. If one doesn't want to share his/her location, the app allows this To optimize efficiency and minimize cost and power use, we have specified the minimum time and the minimum distance between location change updates. The update rate is kept as high as possible to avoid utilizing a lot of battery life.

**To get an API key:**
1. Visit the Google Cloud Platform Console.
1. Click the project drop-down and select or create the project for which you want to add an API key.
1. Click the menu button  and select APIs & Services > Credentials.
1. On the Credentials page, click Create credentials > API key.
1. The API key created dialog displays your newly created API key.
1. Click Close.
1. The new API key is listed on the Credentials page under API keys.

## Video

We provide a detailed tutorial about “how to use” to our about-us page. This video will explain all the steps to make a donation.  The video player in the app won’t restart the video when it is not visible thus saving resources. All the controls will be displayed to give users option to play or pause the video.




Created By Shaily Pandey, Chandrakantha Sruthi and Pratiksha Naik.

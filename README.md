# Foodo
Food Donation App

## Proposed System 

  The app 'FooDo' first asks the user whether he/she wishes to give a food (if he/a she's Donor) (if the user is a volunteer). More information about the app may also be found by clicking on the 'Aboutus' icon.
  
  If you are a volunteer, you must login. Once he signs in, a new donation requiring a volunteer will be alerted. (s)will be prompted to submit basic information, such as his/her name, mobile number and present placement if he/she choose to accept the delivery. Once the donation is reached I the donation place, the quality of the food must be checked and the quantity available verified. After delivery of the food to the NGO, they click a button to confirm that the delivery has been completed. If, however, the user is a new volunteer, he or she is enabling users to register utilising the Login Page using the email identification, password and mobile number.
  
  If the user is a donor, he or she will be asked to input his or her name, cellphone number, address, food type (veg/non-veg) and quantity (in number of people it will serve). After the details have been confirmed, the donor will be led to another page that shows the pickup information. In order for the supplied food to be in good shape, the volunteers coming to pick up will also carry out a quality test for the goods. The donation is sent to an NGO when the donation is verified, and the donor receives a notice and a note of thanks.

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

This page appears when the user has entered the donation details. Here the user will get the information concerning the volunteer that collects the donation. In case you wish to contact and the expected time of arrival at the address specified on the contribution page, a user will also reveal the volunteer telephone number. The donor must now wait till the volunteer arrives at his address and verifies the quality and amount of the donation. The donor is transferred to a Thank You page when the donated food is given to NGOs.

### 4. LOGIN

On the homepage you may click the registration button on the homepage to register / log in as a volunteer. They are then taken to a form for registering an e-mail address and a password. In this case, the system checks whether the email already exists in the database, otherwise the user is currently registered as a volunteer. You can input your credentials and login if you already have the user. Here, if the credentials are not matched, a "invalid userid or password" notice will be shown.

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

### Stay Up to date
It is important for you stay up to date with the new improvements, latest updates and bug fixing. Ensure to Star( * ) the project on Github and get notified whenever any update coming.

## That's all folks!
Feel free to mail me for any doubts/query 
:email: abhi.yalamaddi@gmail.com


Feel free to **file a new issue** with a respective title and description on the the [Foodo](https://github.com/hipstermartin/Foodo/issues) repository. If you already found a solution to your problem, **I would love to review your pull request**! 

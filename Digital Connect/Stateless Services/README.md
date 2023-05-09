# Digital Connect Stateless Services

Digital Connect (DC) Stateless Services are lightweight, flexible API that let you customize the flight booking experience. Travel ecosystem is complex and with our stateless services offering we offer a simple, straightforward solution that is needed to get a particular job done. By taking away the need for completing a big list of prerequisites to make a request, our APIs can now be seamlessly integrated into any flow, in the order you prefer to create the best experience for your users.

This source code repo contains all of the Postman files our teams have built demonstrating the use of our [Stateless services](https://developer.sabre.com/node/10077).

## Current Release 

The services available are listed below:
1.	Seats Service
2.	Ancillaries Service
3.	Payment Service
4.	Fulfillment Service

> Note: This Postman collection was created to showcase Sabre DC Stateless Services and provide developers the ability to test them freely. Sabre APIs Test credentials are required to successfully test these services, if you are an existing Sabre APIs customer and do not have your CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

To get the collection up and running:

* Please download the [Postman](https://www.postman.com/) app
* Request for your [Sabre APIs CERT- environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/)

### Setup and Build

Here are one-time steps for getting your test environment set up:

1. Run the Postman app on your local development machine 
2. Import the [environment file](https://github.com/SabreDevStudio/postman-collections/blob/master/Digital%20Connect/Stateless%20Services/beta/DC_Stateless-DefaultEnv.postman_environment.json) into Postman using the File -> Import option
3. Import the [latest collection file](https://github.com/SabreDevStudio/postman-collections/blob/master/Digital%20Connect/Stateless%20Services/beta/DC_Stateless_Services_Beta.postman_collection.json) into Postman using the File -> Import option
4. Add your credentials and airline information to the environment file. This file has a list of key/value pairs. The following variables needs to be populated with your airline information: 
    * organization
    * domain
    * posCountry
    * posOfficeCode
    * posAccountingCity
    * posStation
    * lniata
    * pcc
    * secret: The 'secret' variable needs to b e populated with you base64-encoded string that you got after checking instructions in [Sabre APIs CERT- environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/)
 
Steps to update the values with your official credentials:
  1. Click the gear icon to go to the manage environments pop-up dialog box.
  2. Click on the name of your imported environment file to see a list of all key/value pairs.
  3. Enter your credentials, and press the "Update" button.    

## Running the Tests
1. Authenticate. In the DC Stateless Services collection you'll find a folder named `Setup` and an item called `Create Auth Token`. Select it. Click the **Send** button. Look for a 200 Success result. If it failed review your environment credentials.
2. Examples are available in the individual folders under `Sample Use Cases`. Simply open one of the folders, go to "Display PNR" request in the folder, then in "Pre-request Script" area update PNR infromation and finally click the **Send** button - look for a 200 Success result. After that you can proceed e execute subsequent requests in the folder.

For more information regarding our DC Stateless offering please [read through its documentation.](https://LINK GOES HERE) 

### Running the Tests using the Collection Runner. 
The Collection Runner allows you to run sets of requests in a specified sequence. The Collection Runner will log your request test results, and your scripts can pass data between requests as well as alter the request workflow. You can use the Runner for any of the folders under `Sample Use Cases` folder in the collection.

1.	Make sure that you go to "Display PNR" request in the specific use case folder, then in "Pre-request Script" tab update PNR information and save request.
2.	Click on the root folder of the use case you want to run. 
3.	Click on “run” icon.
4.	Choose desired requests from the run order list. 
5.	Click on the blue “run” button in order to start execution. 

## License

Copyright (c) 2023 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

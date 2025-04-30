
# Sabre's Lodging APIs Postman files

Sabre’s Lodging APIs support the shopping, booking and servicing of hotel content in the Sabre system. This repository will incorporate different examples on how to transact with Sabre's Lodging portfolio.

> Note: Sabre API test credentials are required to successfully test these APIs, if you are an existing Sabre API customer and do not have your CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Things you need to install:

* [Postman](https://www.postman.com/) app

You'll also need your  [Sabre APIs CERT-environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/).


### Installing

Here are one-time steps for getting your test environment set up:

* Run the Postman application on your local development machine 
* Import the [environment file](./Sabre_APIs_CERT.postman_environment.json) into Postman using the File -> Import option
* Import the Sabre Lodging collection file into Postman using the File -> Import option 


### Use Your Credentials

The environment file you imported has a list of key/value pairs that you need to update with your SOAP API credentials. The following variables have been populated with dummy values:
 
  * `username` - also known as EPR (employee profile record)    
  * `password` - your Sabre provisioned password
  * `pcc` - your pseudo city code (your agency's unique identifier)

Update these values with your credentials by following these steps:

  * Click on the "Environments" icon on the left hand side and then click on "Import", a pop-up dialog box is displayed and you can either drag and drop the environemnt file or navigate to it using the files or folders link
  * Click on the name of your imported environment file to see a list of all key/value pairs
  * Enter your credentials, and press the "Save" icon

![environment variables](https://github.com/SabreDevStudio/postman-collections/blob/master/Booking-Management/Credentials.png)

For more information on Sabre's API portfolio access: [Sabre Dev Studio.](https://developer.sabre.com) 

## License

Copyright (c) 2025 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

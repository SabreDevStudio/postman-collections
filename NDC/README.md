
# Offer and Order APIs Postman files

Sabre’s Offer and Order, REST/JSON-based APIs support the shopping, booking, fulfillment and servicing of NDC content via a new Offer and Order model. The Offers and Orders APIs features the ability to:

* Shop for Air Offers with various qulifiers
* Obtain detailed pricing informatin for a specific offer
* Create an order
* Display an order
* Cancel an order (pre-fulfillment) 
* Fulfill an order
* Determine cancellation information for a fulfiled order
* Cancel a fulfilled order and void/refund the ticket
* Update passenger information in an order
* Display a seat map with pricing information and seat attributes based on an offer or a confirmed order
* Reserve a seat
* Fulfill a paid seat
* Reshop a fulfilled order and complete a voluntary change (rebook the passenger and exchange the ticekt)
* Synchronize an order with the airline's order


This Postman collection was created to showcase Sabre APIs and provide developers the ability to test them freely.

> Note: Sabre API test credentials are required to successfully test these APIs, if you are an existing Sabre API customer and do not have your CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Things you need to install:

* [Postman](https://www.postman.com/) app

You'll also need your  [Sabre APIs CERT-environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/) and for some APIs you will need an [Application ID](https://developer.sabre.com/guides/travel-agency/sabre-api-customer-application-ids)

Note that as of 13 January 2025, the Postman version in use is: 11.27.3, the Javascript within the collection has been udpated to reflect changes where some functions have been deprecated.

### Installing

Here are one-time steps for getting your test environment set up:

* Run the Postman application on your local development machine 
* Import the [environment file](./NDC_Demo.postman_environment.json) into Postman using the File -> Import option
* Import the Offers and Orders collection file into Postman using the File -> Import option 


### Use Your Credentials

The environment file you imported has a list of key/value pairs that you need to update with your SOAP API credentials. The following variables have been populated with dummy values:
 
  * `username` - also known as EPR (employee profile record)    
  * `password` - your Sabre provisioned password
  * `pcc` - your pseudo city code (your agency's unique identifier)

Update these values with your credentials by following these steps:

  * Click on the "Environments" icon on the left hand side and then click on "Import", a pop-up dialog box is displayed and you can either drag and drop the environemnt file or navigate to it using the files or folders link
  * Click on the name of your imported environment file to see a list of all key/value pairs
  * Enter your credentials, and press the "Save" icon

![environment varaibles](./postman_environ_vars.jpg)

## Running the Tests

1. Authenticate. In the NDC collection you'll find an item called `0.REST Authorize ATK`. Select it. Click the **Send** button. Look for a 200 Success result. If it failed review your environment credentials.
2. Shop for air offers. In the NDC collection you'll find an item called `1.Bargain Finder Max /v1`. Select it. Click the **Send** button, and look for a 200 Success result. 

For more information on Sabre's approach to NDC and how you can send content up in requests [read through its documentation.](https://developer.sabre.com/docs/travel-agency/NDC) 

## License

Copyright (c) 2020 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

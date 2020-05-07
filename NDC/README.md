
# New Distribution Capability (NDC) APIs Postman files

Sabre’s NDC-enabled, REST/JSON-based APIs support the shopping, booking and fulfillment of NDC content via a new Offer and Order model. NDC APIs features the ability to:

* Shop for Air Offers
* Price an Air Offer
* Create an Order
* Cancel an Order (pre-fulfillment) 
* Fulfill an Order
* Update an Order
* Display an Order
* Get a Seat Map from an Order


This Postman collection was created to showcase Sabre APIs and provide developers the ability to test them freely.

> Note: Sabre APIs Test credentials are required to successfully test these APIs, if you are an existing Sabre APIs customer and do not have your CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Things you need to install:

* [Postman](https://www.postman.com/) app

You'll also need your  [Sabre APIs CERT-environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/)

### Installing

Here are one-time steps for getting your test environment set up:

* Run the Postman app on your local development machine 
* Import the [environment file](./NDC_Demo.postman_environment.json) into Postman using the File -> Import option
* Import the latest NDC collection file(see below) into Postman using the File -> Import option 


| Collection version | Comments |
| - | - | 
| [2020.04](./NDC%20Demo%20v2020.04.postman_collection.json) | Version incorporates:</br>- Get Seat Map API examples</br>- Order Change Fulfill example with additional form of payment </br>- Order Change examples for Order updates </br>- Inclusion of normalized Get Booking & Cancel Booking services</br>- Additional workflows (incl. State Management examples) | 
| [2019.10](./NDC%20Demo%20v2019.10.postman_collection.json) | Version incorporates scripting logic to seamlessly transition from shop -> price -> book |
| [2019.06](./NDC%20Demo%20v2019.06.postman_collection.json) | Version published during Sabre's 2019 STX event which includes initial set of samples for Sabre's Offer & Order APIs supporting booking of NDC content | 

### Use Your Credentials

The environment file you imported has a list of key/value pairs that you need to update with your SOAP API credentials. The following variables have been marked out with dummy values:
 
  * `username` - also known as EPR (employee profile record)    
  * `password` - your Sabre provisioned password
  * `pcc` - also known as pseudo city code (your agency's unique identifier)

Update the dummy values with your official credentials. To do that follow these steps:

  * Click the gear icon to go to the manage environments pop-up dialog box.
  * Click on the name of your imported environment file to see a list of all key/value pairs.
  * Enter your credentials, and press the "Update" button.    

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

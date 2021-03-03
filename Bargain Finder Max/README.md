# BFM Postman files

The [Bargain Finder Max API](https://developer.sabre.com/docs/rest_apis/air/search/bargain_finder_max) (BFM) is Sabre's shopping service, which computes a vast array of airline schedules and fares across multiple dates to deliver the best set of itinerary offers that meet search criteria in a matter of seconds.

## Current Release 

This API collection encompasses a series of request examples, combining different search attribuetes as listed below:

| Description | What it does |  
|-------------|--------------|
| Basic request | Bare minimum, mandatory search criteria (travel dates, city pair, quantity of passengers, request type and PCC) |
| Alternative Airport (radius) | Alternative airports for both outbound and inbound, based upon a radius around one predefined airport |
| Alternative Airport (list) | Alternative airports for both outbound and inbound are defined by a list of specific airports |
| Alternative Dates | Alternative dates for both outbound and inbound defined via "AD7" type, which drives +/- 7 days around main travel date; further refinement (DateFlexibility parameter) allows to narrow down the range, since the only accepted values are AD1, AD3 and AD7 |
| Stops + Connections | Example to impose minimum and maximum duration of flight connections, along with exclusion of overnight connections, additional non-stop itinerary bucket and subset of itineraries with long connections (10 to 24 hours) |
| Carrier Filters | Carrier exclusion/inclusion, code-share flights being filtered out and validating carrier exclusions |
| Fare Filters | Cabin preference, child (CNN), branded fares data and negotiated fare codes (Account Code + Corporate ID) |
| Attribute Filters | Baggage Allowance info (with charges, if any), along with changes/refunds data, branded fares data and brand attributes |
| Multiple Branded Fares | Example to ask BFM to return multiple branded fares per itinerary, along with its brand attributes; this example limits quantity of brands to 3 via the "UpsellLimit" attribute |
| Multiple Fares Per Itinerary | Comprehensive sample that defines several additional criteria for BFM to return multiple price points per itinerary, including lowest fare for special passenger type, lowest fare in Business cabin, lowest fare that allows at least one free checked bag, lowest negotiated fare and lowest fare that allows changes and refunds |
| Anchored Search | BFM sample request where outbound is fixed to a predefined flight, then BFM will return multiple itinerary options with exactly the same outbound flight |
| Multi-ticket | This request aims to pack three sets of itinerary options in one response: lowest available round trip fares (up to 100 options), 30 one way fares for outbound and another 30 one way fares for inbound; while all the round trip options are always meant to be sold on the same ticket, all one way itinerary options can be combined in any way the client wants, always in two separate tickets, two separate PNRs |
| Multiple Branded Fares | Example to ask BFM to return multiple branded fares per itinerary, along with its brand attributes; this example limits quantity of brands to 3 via the "UpsellLimit" attribute |



This Postman collection was created to showcase Sabre APIs and provide developers the ability to test them freely.

> Note: Sabre APIs Test credentials are required to successfully test these APIs, if you are an existing Sabre APIs customer and do not have your CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Things you need to install:

* [Postman](https://www.postman.com/) app

You'll also need your [Sabre APIs CERT-environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/)

### Installing

Here are one-time steps for getting your test environment set up:

* Run the Postman app on your local development machine 
* Import the [environment file](https://github.com/SabreDevStudio/postman-collections/blob/master/Sabre-APIs/Sabre_APIs_CERT.postman_environment.json) into Postman using the File -> Import option
* Import the latest collection file (see below) into Postman using the File -> Import option

| Collection version | Comments |
| - | - | 
| [2021.03](./VDB_20210302.postman_collection.json) | Launch version for this API collection, all samples are JSON REST | 

### Use Your Credentials

The environment file you imported has a list of key/value pairs that you need to update with your REST API credentials. The following variables have been marked out with dummy values:
 
  * `username` - also known as EPR (employee profile record)    
  * `password` - your Sabre provisioned password
  * `pcc` - also known as pseudo city code (your agency's unique identifier)

Update the dummy values with your official credentials. To do that follow these steps:

  * Click the gear icon to go to the manage environments pop-up dialog box.
  * Click on the name of your imported environment file to see a list of all key/value pairs.
  * Enter your credentials, and press the "Update" button.    

![environment variables](https://github.com/SabreDevStudio/postman-collections/blob/master/Sabre-APIs/postman_environ_vars.jpg)

## Running the Tests

Please ensure to authenticate by generating a stateless token.  There will be a item named `Authentication` in this collection.  Please select it and click the **Send** button. Look for a 200 Success result. If it failed review your environment credentials. Postman environment collection can be downloaded from [here](https://github.com/SabreDevStudio/postman-collections/blob/master/Sabre-APIs/Sabre_APIs_CERT.postman_environment.json). 


## License

Copyright (c) 2020 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

# Content Services for Lodging API Postman files

The [Content Services for Lodging (CSL)](https://developer.sabre.com/content-services-for-lodging) product collection houses APIs to help you find properties, get information about properties, check prices, and much more.

Two types of APIs are currently available through CSL to match the needs of your solution:

**Orchestrated APIs**: Supports common use cases for both shopping and booking properties across fewer requests.

**Granular APIs**: Power the Orchestrated APIs. Using granular APIs,  integrate content directly into your workflow, allowing for a more customized experience.

## Purpose

This Postman collection was created to showcase Sabre CSL API and provide developers the ability to test them freely.

> Note: Sabre APIs Test credentials are required to successfully test these API, if you are an existing Sabre API customer and do not have your CERT credentials, please contact your Sabre account manager.

## Why use it?
Enhance your booking tool with the value that CSL delivers, including:

**More Content**: </br>
Integrating over a million lodging property and rate options from GDS and aggregator sources through modern, flexible APIs, allowing you to compare rates from different sources side-by-side.

**New Search and Preferencing Capabilities**: </br>
Delivering enhanced capabilities such as polygon searching and agency preferencing, enabling new shopping experiences and more efficient workflows

**Product Normalization**: </br>
Supporting attribute-based rate comparison across content sources allowing your agents and travelers to easily and efficiently find the best rate that meets their needs

**Modern APIs**: </br>
CSL offers a modern set of SOAP/XML and REST/JSON APIs that leverage improved data structures and are supported by robust documentation.

## Releases

| Collection version | Comments |
| - | - | 
| [2025.09](./Lodging%20v2025.09.postman_collection.json)| Version incorporates: new refreshed view with more API and examples plus </br> - Shopping Folder </br> - Booking Folder </br> - Post-Booking folder </br> - Content Folder </br> - Workflow Folder (with samples and scenarios) </br> - Granular API Folder </br> - Sabre Travel AI™ - Lodging AI Folders with Hotel Alternative Finder and Hotel Cross Sell examples </br> - Polygon Search Folder </br>
| [2025.04](./Lodging%20v2025.04.postman_collection.json)| Version incorporates: a new 2025 collection including  </br> - Authentication folder with several examples, </br> - Lodging Retailer Preferencing folder with examples


## Current Release 

The services available in this API product collection are listed below:

| Service | Description | Endpoint | Type |  
|---------|-------------|----------|------|
|**ORCHESTRATED**|
|[Get Hotel Avail](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_avail)| Search hotels by different criteria | `POST /v5/get/hotelavail` |REST/JSON|
|[Get Hotel Details](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_details)| Select a hotel, get all rates and choose a room | `POST /v5/get/hoteldetails` |REST/JSON|
|[Hotel Price Check](https://developer.sabre.com/docs/rest_apis/hotel/search/hotel_price_check)| Verify selected rate and return up-to-date pricing and the BookingKey for booking. | `POST /v5/get/hotel/pricecheck` |REST/JSON|
|[Get Hotel Content](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_content)|  Delivers complete hotel descriptive and media content for a specified property ID, including location details, property information, and visual assets, with customizable description fields. | `POST /v4/get/hotelcontent` |REST/JSON|
|**GRANULAR**|
|[Geo Search](https://developer.sabre.com/rest-api/geo-search)| Performs radius-based searches to locate airports, hotels, rail stations, and car rental points within a specified geographic area. | `POST /v4/geo/search` |REST/JSON|
|[Get Hotel Lead Rate](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_lead_rate)| Lookup the lowest available rate based on search criteria | `POST /v5/get/hotelleadrate` |REST/JSON|
|[Get Hotel Rate Info](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_rate_info)| Retrieves all available property rates from multiple sources, including GDS and aggregators, based on specified stay criteria. | `POST /v5/get/hotelrateinfo` |REST/JSON|
|[Get Hotel List](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_list_v410)| Fetch up to a maximum limit of 5,000 hotels based on search parameters| `POST /v4.1.0/get/hotellist`|REST/JSON|
|[Get Hotel Media](https://developer.sabre.com/rest-api/get-hotel-media/)| Returns hotel media content by Hotel Codes, including image URLs in multiple sizes, metadata (type, caption, last updated, ordering), and multilingual support for flexible integration.| `POST /v2.0.0/get/hotelmedia`|REST/JSON|
|[Get Hotel Image](https://developer.sabre.com/rest-api/get-hotel-image)| Provides hotel image URLs for up-to 300 hotels URLs with metadata from our visual platform, offering 5 sizes, 23 OpenTravel categories in up to 8 languages, captions, sequencing, and last-updated timestamps..| `POST /v1.0.0/shop/hotels/image`|REST/JSON|
|[Get Hotel Descriptive Info](https://developer.sabre.com/docs/rest_apis/hotel/search/get_hotel_descriptive_info)| Retrieves location and detailed property information for specified Sabre or global hotel IDs.| `POST /v4.0.0/get/hoteldescriptiveinfo`|REST/JSON|
|[Get Polygon Info](https://developer.sabre.com/rest-api/get-polygon-info/)| Returns polygon details from the Geo database based on criteria like ID, area, city, state, or country code, with optional date-range filters for created or updated polygons.| `POST /v1/get/polygoninfo`|REST/JSON|
|[Geo Auto Complete](https://developer.sabre.com/rest-api/geo-autocomplete/)| Provides up to five real-time location predictions—airports, cities, or rail stations—by matching full words or substrings in a geographic search query. | `POST /v2/geo/autocomplete` |REST/JSON|
|[Hotel Search](https://developer.sabre.com/rest-api/hotel-search/)| Enables hotel property searches using multiple location resolution methods, including polygon search, to retrieve matching content without availability data. | `POST /v2.0.0/hotel/search` |REST/JSON|
|[Get Hotel Chain Info](https://developer.sabre.com/rest-api/get-hotel-chain-info/)| Returns the complete list of hotel marketers with their names, marketer chain codes, and corresponding chain code names. | `POST /v1.0.0/shop/hotels/chain` |REST/JSON|
|[Get Hotel Content Change](https://developer.sabre.com/docs/rest_apis/hotel/utility/get_hotel_content_change)| Provides a list of new and updated hotel content within a specified date range (up to 10 days). | `POST /v1.0.0/shop/hotels/content/change` |REST/JSON|
|[Property Name Autocomplete](https://developer.sabre.com/rest-api/property-name-autocomplete/)| Returns up to five real-time property name predictions for text-based hotel searches, powered by the CSL platform. | `POST /v1/hotels/utilities/autocomplete/hotelname` |REST/JSON|


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

### Use Your Credentials

The environment file you imported has a list of key/value pairs that you need to update with your SOAP API credentials. The following variables have been marked out with dummy values:
 
  * `username` - also known as EPR (employee profile record)    
  * `password` - your Sabre provisioned password
  * `pcc` - also known as pseudo city code (your agency's unique identifier)

Update the dummy values with your official credentials. To do that follow these steps:

  * Click the gear icon to go to the manage environments pop-up dialog box.
  * Click on the name of your imported environment file to see a list of all key/value pairs.
  * Enter your credentials, and press the "Update" button.    

![environment variables](https://github.com/SabreDevStudio/postman-collections/blob/master/Booking-Management/Credentials.png)


## License

Copyright (c) 2025 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

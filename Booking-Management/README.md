# Sabre Booking Management API Postman files

The [Booking Management API](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management) (integral part of Sabre's Business Services) facilitates working with Sabre reservations (bookings) by providing a normalized set of services for the most common travel related use-cases.

## Current Release 

The services available in this API are listed below:

| Service | Description | Endpoint | Type |  
|---------|-------------|----------|------|
|[Get Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management/help?page=get-booking)| Normalized view of the Sabre Booking | /trip/orders/getBooking |RPC/JSON|
|[Create Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management/help?page=get-booking)| Create Booking provides a single, unified service to create an air booking for different content sources (NDC, Traditional, LCC). | /trip/orders/createBooking |RPC/JSON|
|[Modify Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management_beta)| Modify Booking provides a single, unified service to modify non-itinerary content of a booking. Current  implementation supports modification of CSL hotel bookings, PNR elements, NDC order elements, group bookings etc. In the future, we are planning to enhance the API with such features as: addition of ancillaries (seats/baggage) for existing booking, and more! | /trip/orders/modifyBooking |RPC/JSON|
|[Cancel Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management/help?page=cancel-booking)| Normalized cancel of Sabre Products within a Booking. Also, lets you process a refund/void offer for NDC orders| /trip/orders/cancelBooking |RPC/JSON|
|[Check Flight Tickets](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Check Flight Tickets provides a single, unified service to verify exchangeability, voidability and refundablity for a list of electronic documents (ATPCO). The endpoint also lets you check if the NDC order may be voided or refunded. | /trip/orders/checkFlightTickets |RPC/JSON|
|[Void Flight Tickets](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Void Flight Tickets provides a single, unified service to void a list of electronic documents (ATPCO). This includes electronic tickets as well as electronic miscellaneous documents (EMD). | /trip/orders/voidFlightTickets |RPC/JSON|
|[Refund Flight Tickets](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Refund Flight Tickets provides a single, unified service to refund a list of electronic documents (ATPCO). The service allows to specify refund qualifiers. This is currently limited electronic tickets. | /trip/orders/refundFlightTickets |RPC/JSON|
|[Fulfill Flight Tickets](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management)| Fulfill Flight Tickets provides a single, unified service to facilitate document issuance in a single, seamless API call. This includes electronic tickets, electronic miscellaneous documents (EMDs) as well as NDC orders. | /trip/orders/fulfillFlightTickets |RPC/JSON|


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
| [2025.02](./Booking%20Management%20API%20v2025.02.postman_collection.json)| Version incorporates a number of new workflows related to form of payment modifications : </br> - ModifyBooking -> add/delete/update form of payment. </br>
| [2024.11](./Booking%20Management%20API%20v2024.11.postman_collection.json)| Version incorporates a number of new workflows : </br> - ModifyBooking/Flight_modification_flows/SSR (identity documents/special service) modifications -> add/delete/update. </br>
| [2024.10](./Booking%20Management%20API%20v2024.10.postman_collection.json)| Version incorporates a number of new workflows : </br> - ModifyBooking/Flight_modification_flows/Seat_modifications -> add/delete/update seats for ATPCO flight content, </br> - ModifyBooking/NDC_modifications_flows/Modify_seats -> add/delete/update seats for NDC flight content, </br> - Workflows/20-LCC-Air_Shop_Ancillaries,_Book -> shop for ancillaries for low cost airline, book flights with ancillaries (check Pre-request scripts to modify airlines and airports).
| [2024.08](./Booking%20Management%20API%20v2024.08.postman_collection.json)| Version incorporates:</br>- New workflows and scenarios related to fulfillFlightTickets andpoint (dedicated section). Also includes a new workflow example related to ancillaries. 
| [2023.12](./Booking%20Management%20API%20v2023.12.postman_collection.json)| Version incorporates:</br>- New workflow scenario for NDC order creation for multiple traveler types. Also, there are additional examples related to retention line (OTH segment) processing (createBooking, cancelBooking).
| [2023.10](./Booking%20Management%20API%20v2023.10.postman_collection.json)| Version incorporates:</br>- New workflow scenarios focused on modifying order elements via modifyBooking.
| [2023.08](./Booking%20Management%20API%20v2023.08.postman_collection.json)| Version incorporates:</br>- New workflow scenarios focused on checking ticket rules and refundability/exchangeability.
| [2023.04](./Booking%20Management%20API%20v2023.04.postman_collection.json)| Version incorporates:</br>- New workflow scenarios focused on NDC content.
| [2023.03](./Booking%20Management%20API%20v2023.03.postman_collection.json)| Version incorporates:</br>- a number of minor corrections for various scenarios.|
| [2022.11](./Booking%20Management%20API%20v2022.11.postman_collection.json)| Version incorporates:</br>- a number of minor corrections for various scenarios.|
| [2022.10](./Booking%20Management%20API%20v2022.10.postman_collection.json)| Version incorporates:</br>- modifyBooking service examples for ATPCO modifications. Each use case scenario is presented as a workflow. We hope that this would simplify tests and integration. On top of that, we added data preparation scenarios for createBooking service, which may help you build up flight/hotel/car flow|
| [2022.06](./Booking%20Management%20API%20v2022.06.postman_collection.json)| Version incorporates:</br>- new modifyBooking service examples for changing CSL hotel bookings. Each use case scenario is presented as a workflow. We hope that this should simplify tests and integration. |
| [2021.12](./Booking%20Management%20API%20v2021.12.postman_collection.json)| Version incorporates:</br>- new CreateBooking examples for booking vehicle content,</br>- an extra CreateBooking example for CSL hotel + strong customer authentication, </br>- 'Workflows' folder has been updated and revised (added new vehicle workflow, corrected wrong REST endpoints, updated various variables). |
| [2021.09](https://github.com/SabreDevStudio/postman-collections/blob/master/Booking-Management/Booking%20Management%20API%20v2021.09.postman_collection.json) | Version incorporates:</br>- CreateBooking samples for booking ancillaries |
| [2021.06](./Booking%20Management%20API%20v2020.06.postman_collection.json) | Version incorporates:</br>- CreateBooking samples for booking hotel content |
| [2021.04](./Booking%20Management%20API%20v2020.05.postman_collection.json) | Version incorporates:</br>- CreateBooking samples for sending other service information (OSI) </br>- CreateBooking sample using a profile filtered by the ID </br>- CheckFlightTickets request by confirmationId. This allows you to check all ATPCO tickets of a reservation and check the refund or void option of a NDC Order </br>- CancelBooking samples for voids or refunds for NDC orders |
| [2021.02](./Booking%20Management%20API%20v2021.02.postman_collection.json) | Version incorporates:</br>- CreateBooking RPC/JSON service to book air content  (NDC, Traditional, LCC). </br>- Check Flight Tickets samples </br>- Void Flight Tickets samples </br>- Refund Flight Tickets samples </br>- New e2e workflows | 
| [2020.08](./Booking_Management_API_v2020.08.postman_collection.json) | Version incorporates:</br>- Cancel Flight Tickets samples (RPC/JSON) </br>- Additional Cancel Booking samples| 
| [2020.05](./Booking%20Management%20API%20v2020.05.postman_collection.json) | Version incorporates:</br>- Patch fix to ensure compatibility with Postman v7.25.0 as latest version caused a problem in the scripting logic | 
| [2020.04](./Booking_Management_API_v2020.04.postman_collection.json) | Launch version for this API, which contains:</br>- Get Booking samples (RPC/JSON)</br>- Get Booking samples (GraphQL) </br>- Cancel Booking samples (RPC/JSON) | 

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

## Running the Tests

1. Authenticate. In the Booking Management API collection you'll find a folder named `Authentication` and an item called `REST Authorize`. Select it. Click the **Send** button. Look for a 200 Success result. If it failed review your environment credentials.
2. Both the GetBooking and CancelBooking services require a confirmation id (PNR locator) in order to properly function, make sure you have one available in order to test. Examples are available in the individual folders: `Get Booking` and `Cancel Booking`. Simply open one of these folders, select an example to test, click the **Send** button, and look for a 200 Success result. 

For more information regarding our Booking Management API offering please [read through its documentation.](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management) 

## Running the Tests using the Collection Runner. 

The Collection Runner allows you to run sets of requests in a specified sequence. The Collection Runner will log your request test results, and your scripts can pass data between requests as well as alter the request workflow. You can use the Runner for the `Deep Dive into E2E NDC Reservation Management with the Booking Management` API collection.

1.	Click on the root folder of the project. 
2.	Click on “run” icon.
3.	Choose desired requests from the run order list. 
4.	Click on the blue “run” button in order to start execution. 

![1](https://user-images.githubusercontent.com/83339794/130613211-a4ff734c-65f4-46da-b4c0-807c8fc93c83.png)
![2](https://user-images.githubusercontent.com/83339794/130613217-697810e2-ff1d-44a5-b623-ce1f8d1df769.png)

## License

Copyright (c) 2023 Sabre Corp Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

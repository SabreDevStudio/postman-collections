# Sabre Booking Management API Postman files

The [Booking Management API](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management) is an integral part of Sabre's Business Services. It helps developers work with Sabre reservations (bookings) by providing a normalized set of services for the most common travel-related use cases.

## Current Release

The services available in this API are listed below:

| Service | Description | Endpoint | Type |  
| ------- | ----------- | -------- | ---- |
| [Get Booking](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/get-booking.html) | Normalized view of the Sabre Booking (ATPCO and/or NDC) | /trip/orders/getBooking | RPC/JSON |
| [Create Booking](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/create-booking.html) | Create Booking provides a single, unified service to create an air booking for different content sources (NDC, ATPCO, LCC). | /trip/orders/createBooking | RPC/JSON |
| [Modify Booking](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/modify-booking-0.html)| Modify Booking provides a single, unified service to modify non-itinerary content of a booking. Current  implementation supports modification of CSL hotel bookings, PNR elements, NDC order elements (including seats)  , group bookings etc. In the future, we are planning to enhance the API with such features as: addition of paid ancillaries (like baggage) for existing booking, and more! | /trip/orders/modifyBooking | RPC/JSON |
| [Cancel Booking](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management/help?page=cancel-booking)| Normalized cancel of Sabre Products within a Booking. Also, lets you process a refund/void offer for NDC orders. Finally, it lets you cancel and refund an LCC booking | /trip/orders/cancelBooking | RPC/JSON |
| [Check Flight Tickets](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/check-flight-tickets.html) | Check Flight Tickets provides a single, unified service to verify exchangeability, voidability and refundablity for a list of electronic documents (ATPCO). The endpoint lets you check if the NDC order may be voided or refunded or if the LCC booking can be refunded. | /trip/orders/checkFlightTickets | RPC/JSON |
| [Void Flight Tickets](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/void-flight-tickets.html)| Void Flight Tickets provides a single, unified service to void a list of electronic documents (ATPCO). This includes electronic tickets as well as electronic miscellaneous documents (EMD). | /trip/orders/voidFlightTickets | RPC/JSON |
| [Refund Flight Tickets](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/refund-flight-tickets.html) | Refund Flight Tickets provides a single, unified service to refund a list of electronic documents (ATPCO). The service allows to specify refund qualifiers. The service supports refunds of electronic documents (TKT) as well as miscelleaneous documents issued for ancillary services (EMD) . | /trip/orders/refundFlightTickets | RPC/JSON |
| [Fulfill Flight Tickets](https://developer.sabre.com/rest-api/booking-management-api/v1/help-documentation/fulfill-flight-tickets.html) | Fulfill Flight Tickets provides a single, unified service to facilitate document issuance in a single, seamless API call. This includes electronic tickets, electronic miscellaneous documents (EMDs) as well as NDC orders. | /trip/orders/fulfillFlightTickets | RPC/JSON |
| [Flight Reshop](https://developer.sabre.com/rest-api/flight-reshop-api/1.0/help-documentation/sabre-flight-reshop.html) | The Sabre Flight Reshop method is designed to allow you to retrieve alternative itinerary options when a passenger needs to change their fulfilled itinerary (ATPCO/NDC). | /offers/flightReshop | RPC/JSON |

This Postman collection was created to showcase Sabre APIs and to give developers a free and flexible way to test them.

> Note: Sabre API test credentials are required to successfully use these APIs. If you are an existing Sabre API customer and do not have CERT credentials, please contact your Sabre account manager.

## Getting Started

These instructions will help you get the project running on your local machine for development and testing. See the deployment notes for information on how to use it in a live system.

### Prerequisites

Software you need to install:

* [Postman](https://www.postman.com/) app

You will also need your [Sabre API CERT environment credentials](https://developer.sabre.com/resources/getting_started_with_sabre_apis/).

### Installing

Here are the one-time steps for setting up your test environment:

* Run the Postman app on your local development machine.
* Import the [environment file](./BM_API_V2_Environment.postman_environment.json) into Postman using the File -> Import option.
* Import the latest collection file (see below) into Postman using the File -> Import option.

| Collection version | Comments |
| - | - |
| [2026.08](./Booking_Management_API_v2_2026.08.postman_collection.json) | First iteration of a complete redesign of the collection. The scripts were rewritten and are mainly stored within the collection itself (previously they were part of the individual API calls). Migrated from legacy offer APIs to modern ones (Flight Shop and Flight Check). The collection is compatible with the new [environment file](./BM_API_V2_Environment.postman_environment.json). </br> This version incorporates new workflows: </br> - Create Booking -> ATPCO booking with new VISA subtypes </br> - Fulfill Flight Tickets -> ATPCO ticket reissue </br> - Fulfill Flight Tickets -> ATPCO fulfillment with form of payment referencing </br> - Fulfill Flight Tickets -> NDC fulfillment with form of payment referencing |
| [2026.04](./Booking%20Management%20API%20v2026.04.postman_collection.json) | Version incorporates new workflows: </br> - ModifyBooking -> Flight Modification Flows -> Ancillary Modifications (ATPCO) </br> - ModifyBooking -> NDC Modification Flows -> Ancillary Modifications |
| [2026.03](./Booking%20Management%20API%20v2026.03.postman_collection.json) | Version incorporates updates to existing workflows and examples, plus changes to variables related to NDC booking creation. |
| [2026.02](./Booking%20Management%20API%20v2026.02.postman_collection.json) | Version incorporates a number of new workflows: </br> - ModifyBooking -> Flight Modification Flows -> Stored Price Quote Deletion (ATPCO) </br> - ModifyBooking -> General Modifications -> Modify Remarks (workflow) </br> - ModifyBooking -> General Modifications -> Modify Name Associated Remarks </br> - Workflows -> 34 - NDC - Agency address (BA requirement - requires agency access to BA content) |

### Use Your Credentials

The environment file you imported contains a list of key/value pairs that you need to update with your API credentials. The following variables are shown with placeholder values:

* `username` - also known as EPR (employee profile record)
* `password` - your Sabre-provisioned password
* `pcc` - also known as pseudo city code (your agency's unique identifier)
* `clientId` - a unique signature for internal or external customer applications; only applicable if you authenticate with `OAuth Token Create - V3 ClientId`
* `clientSecret` - the client secret; applicable if you authenticate with `OAuth Token Create - V3 ClientId`

Update the values with your official credentials by following these steps:

* Click the gear icon to open the Manage Environments dialog box.
* Click the name of your imported environment file to see a list of all key/value pairs.
* Enter your credentials and press the "Update" button.

![environment variables](https://github.com/SabreDevStudio/postman-collections/blob/master/Booking-Management/Credentials.png)

## Running the Tests

1. Authenticate. In the Booking Management API collection, you'll find a folder named `Authentication` and an item called `REST Authorize`. Select it and click the **Send** button. Look for a 200 Success result. If it fails, review your environment credentials.
2. Multiple APIs require a confirmation ID (PNR locator) to function properly. Make sure you have one available before testing. Examples are available in the individual folders. Simply open one of these folders, select an example to test, click the **Send** button, and look for a 200 Success result.

For more information about the Booking Management API offering, please [read the documentation](https://developer.sabre.com/docs/rest_apis/trip/orders/booking_management).

## Running the Tests using the Collection Runner

The Collection Runner allows you to run sets of requests in a specified sequence. The Collection Runner will log your request test results, and your scripts can pass data between requests as well as alter the request workflow. You can use the Runner for the `Deep Dive into E2E NDC Reservation Management with the Booking Management` API collection.

1. Click on the root folder of the project.
2. Click on “run” icon.
3. Choose desired requests from the run order list.
4. Click on the blue “run” button in order to start execution.

![1](https://user-images.githubusercontent.com/83339794/130613211-a4ff734c-65f4-46da-b4c0-807c8fc93c83.png)
![2](https://user-images.githubusercontent.com/83339794/130613217-697810e2-ff1d-44a5-b623-ce1f8d1df769.png)

## License

Copyright (c) 2026 Sabre Corp. Licensed under the MIT license.

## Disclaimer of Warranty and Limitation of Liability

This software and any compiled programs created using this software are furnished “as is” without warranty of any kind, including but not limited to the implied warranties of merchantability and fitness for a particular purpose. No oral or written information or advice given by Sabre, its agents or employees shall create a warranty or in any way increase the scope of this warranty, and you may not rely on any such information or advice.
Sabre does not warrant, guarantee, or make any representations regarding the use, or the results of the use, of this software, compiled programs created using this software, or written materials in terms of correctness, accuracy, reliability, currentness, or otherwise. The entire risk as to the results and performance of this software and any compiled applications created using this software is assumed by you. Neither Sabre nor anyone else who has been involved in the creation, production or delivery of this software shall be liable for any direct, indirect, consequential, or incidental damages (including damages for loss of business profits, business interruption, loss of business information, and the like) arising out of the use of or inability to use such product even if Sabre has been advised of the possibility of such damages.

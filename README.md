# Rideo-Book-My-Ride
##Problem Statement:

Today customer has to log into different ride-hailing applications to find the cheapest & quickest available vehicle by doing manual comparisons.

User has to install multiple applications.

User has to maintain multiple login credentials.

If the user books the cab for the same ride in multiple applications, User has to take care of multiple cancellations in different applications bearing the cancellation charges.

##Solution:

"Rideo: Book My Ride" application allows retail customers to find & book rides in a single place, to get the cheapest, quickest available vehicle in a convenient manner.
##Business Outcomes
One-stop application to book available vehicles from different vendors like Uber, Ola, etc.

Consolidation of vehicles availability with cost from multiple vendors.

##Benefits
No pain point of using multiple hail trip apps to search for available vehicles, comparing rates and arrival time

Selection of 1 or more available vehicles, auto-selection in case of multiple selections

Cancellation of the ride before cab arrival

Tracking of cab status

Can be used in multiple countries/cities

Supports multi-ride types

Easy addition of any vendors, in future

Time save as we get consolidated data in a single app

It also paves the way for the local vendors in the market amidst massive vendors

##Applicability in Other Domains
This product idea can be extended to any customer searchable parameters. Use cases include comparing prices & availability of

Food in apps like Swiggy, Zomato, Door dash, Uber Eats

Flight ticket across various airlines

Medicines in apps like Netmeds, OneMg

Products in online shopping apps like Amazon, Flipkart

##Functional & Non-Functional Requirements
Functional Requirements:

User should be able to book a ride by selecting ride type, pick up & drop location

Upon entering the ride details, the user should be able to view the complete list of service providers along with fare and ETA details

User should be able to select one or more rides from the list based on his/her preference (Cost Vs ETA factors)

The service provider, giving the first response upon user's preference, should be assigned the ride while the other selected rides should be automatically rejected

Users should be able to cancel the ride after their ride is confirmed until the cab arrival

Non-Functional Requirements:

Auto-fill suggestions of Pick Up and Drop Location based on real-time typing of alphabets in these fields

App capacity to handle many requests at a time

Update ETA at ping frequency of 30 seconds, after the cab has been confirmed until the cab arrival

Simple and user intuitive User Interface design

Providing secure environment for both service providers and users as per PEGA security guidelines

Displaying the rating of the service providers (Extendable)

Showing the possible routes to reach the destination (Extendable)

Showing the real time traffic conditions (Extendable)
Design Considerations & Assumptions
Tool used for Implementation: Pega Cloud v 8.6

##Design considerations:

Use of Pega Cosmos UI

Use of Google Maps integration with Pega to allow user to select pick up and drop location

Use of Pega case management feature for creating and managing ride case

Use of configurable DB to add/remove supported vendors, vehicle type and end-point URL

Use of Connect-REST in PEGA for API calls to the service providers

Pega has inbuilt horizontal & vertical scaling to support huge user base

##Assumptions:

Service providers to expose the following APIs:

i) List the available rides with cost and ETA based on the ride type, pick up and drop location

ii) Confirm the booking

iii) Update the cab arrival status and ETA

iv) Cancel the booking
##Scalability
Pega Platform operates on a large scale with a single cluster supporting tens of thousands of simultaneous users and millions of cases per day. Both horizontal and vertical scaling is supported:

• Horizontal scaling with near-linear scalability within a certain range of scaling can be supported by deploying Pega JVM nodes across multiple load-balanced servers. Shared database architecture is used across a horizontal cluster, with certain instances of communication between the nodes taking place throughout the database. Hazelcast is generally used as a clustering solution for the nodes. If needed, database scalability is provided by the database vendor's clustering capabilities.

• Vertical scaling is supported by running multiple Pega JVM nodes on a multi-CPU server. Pega Platform adds capabilities for failover in the case of node server crashes.

Browser crashes are also handled by recovering the user session.
##Scalability
Pega Platform operates on a large scale with a single cluster supporting tens of thousands of simultaneous users and millions of cases per day. Both horizontal and vertical scaling is supported:

• Horizontal scaling with near-linear scalability within a certain range of scaling can be supported by deploying Pega JVM nodes across multiple load-balanced servers. Shared database architecture is used across a horizontal cluster, with certain instances of communication between the nodes taking place throughout the database. Hazelcast is generally used as a clustering solution for the nodes. If needed, database scalability is provided by the database vendor's clustering capabilities.

• Vertical scaling is supported by running multiple Pega JVM nodes on a multi-CPU server. Pega Platform adds capabilities for failover in the case of node server crashes.

Browser crashes are also handled by recovering the user session.

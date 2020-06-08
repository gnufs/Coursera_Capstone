##### Coursera_Capstone
IBM Data Science Professional Certificate program's capstone project on Coursera

# Restaurant Delivery Clusters in Berlin
### Ali Gündüz
##### June, 2020

## Introduction
#### Background
With rapid urbanization on a global scale and an increased labor participation of women has led to a greater demand for delivery of restaurant food services all around the world. Different markets are approaching this challenge in different ways. Whereas restaurants in some countries such as Turkey, due to their lower labor costs, mostly offer home delivery via their own delivery personnel, the developed countries have seen the arrival of food delivery companies such as takeaway.com, Uber Eats, GrubHub that offer delivery services between restaurants and consumers. There are also delivery-focused restaurant chains like Domino’s that offer their own delivery service even in developed countries.

#### Business Problem
The COVID-19 shutdowns have revealed the [problematic side](https://www.bbc.com/news/business-52651931) of restaurants’ dependence on food delivery apps. They can charge fees that seem exorbitant to restaurant owners. Depending on an large corporation also means that the restaurant doesn’t have control over a significant part of the food ordering experience of the customer such as delivery speed and service quality.

On the other hand, employing their own delivery personnel is not economically feasible for most independent restaurants in the developed countries where labor costs are considerable.

One possible solution we would like to explore is to have local (think neighborhood or district) food delivery contractors or cooperatives where the end consumers order directly from the restaurant and the restaurant uses a local network of riders for quick delivery. To try out such a delivery service, we would need a location with a dense concentration of restaurants which we could approach for cooperation. Failing to find such a suitable location would mean that our riders wouldn’t have enough orders to service throughout the day or that it would take a long time for our riders to deliver the orders. Once we find a suitable cluster of restaurants, we would ideally have a small servicing/waiting station for riders in the cluster’s middle.

In our example, we will look for such a location candidate around the city center of Berlin, Germany. 

We believe such an experiment would be interesting for independent restauranteurs, city planners and entrepreneurs as possible stakeholders.

## Data
We will use the **Foursquare API** to get local restaurant information in Berlin. In particular, Foursquare API’s `explore` functionality returns us a venue list for a given coordinate and radius. We will download venue data for a large section of Berlin’s city center and save the **name**, **category**, **id number** and **coordinates** (latitude and longitude) for each restaurant.

We will also use the **OpenStreetMap Nominatim** geolocation service via the `geopy` library to reverse search street addresses for the cluster center coordinates.

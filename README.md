# RideOut
HackSC

Inspiration
Many of us are not able to afford a private mode of transportation. Thankfully, we do have other options like Uber or Lyft which enable us to commute effectively. But unfortunately, it can still get expensive for everyday commutes. So we decided to work on creating a system that provides a cheap as well as consistent solution to this problem.

What it does
RideOut is a ride sharing application that allows people to pool cars to go from one point to another. It is different from other car pooling or cab applications out there in the sense that it takes into account driver's priorities - drivers post their ride as per their itinerary.

For example a person X wants to go shopping from his home and return. X can reduce his/her fuel cost by picking up maybe a couple of people on his way who are also looking to go for a similar errand. As a result, the price is considerably lower than other cabs. The riders benefit from this model since they get a similar ride at deflated price.

People who wish to commute between places can look up for available drivers who have planned their journey on a similar route.

How I built it
We created an iOS application to showcase our MVP. Coding was done in Swift to speed up development. Back-end was hosted with Parse for the time being. We used Google Maps APIs to carry out all travel and map operations.

Challenges I ran into
Drivers can post rides from source S to destination D with several additional points (way-points) in between. With huge number of drivers posting, this creates a graph of available stops (nodes) and paths (edges). Now the challenge is to provide all possible paths when a rider searches for a ride from source S’ to destination D’. There can be multiple paths using those intermediate way-points which can be tough to find since the Google Maps API returns only points in path A to B (it doesn’t consider all points around its near proximity). But our application should provide all such paths.

Since time was a constraint, we designed an algorithm which finds rides which uses all such way-points in a x mile radius from source and destination only. But it can be extended in future to use all such 1 mile radius way-points along the entire path (not just source and destination).

Accomplishments that I'm proud of
With the time constraint, we are happy to create a close MVP for a ride-sharing app which incorporates a custom routing algorithm as per the novel idea of making the app driver centric and yet keeping the cost cheap for the riders.

What I learned
We learnt to use Google Maps APIs better than ever before since we never needed to explore the API to the edge. There was this great real world graph problems which further strengthened our knowledge of the most interesting and effective field of Computer Science.

What's next for RideOut
We wish to provide every transit method for a person who is planning to go from A to B. This could be by walk, bike or other transport methods available, to make the system fully complete for a person.

As we gather more and more users on the system, and consequently more data, we plan to mine the data to gather meaningful insights out of it. A rating system can be created where drivers can rate passengers and vice-versa. A recommendation engine can be incorporated to make the experience better for both parties.


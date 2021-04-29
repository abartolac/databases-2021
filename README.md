# Campus Food Delivery System
## ***Introduction***

Hello everyone! This is a project that features enhancements to a food delivery system for college campuses. The main enhancement will be the addition of a rating system for delivery drivers and customers. The rating system will be a five-star rating system in which customers can express their happiness, disappointment, etc. of their devliery experience. They will rate both the delivery driver and the restaurant. Sometimes, the delivery driver is not at fault for a bad experience, so the separation between delivery driver and restaurant rating is important. This system also allows the database to compare ratings across multiple deliveries for a specific delivery driver. If there are many negative reviews about one driver, the campus controllers can look into the negative experiences and take further action as needed. The rating system overall enhances the effectiveness of the delivery system.
This project was created by Ashley Bartolac, Ethan Bemis, and Jai Hall.

## ***Use Case for Rating System***

## ***Business Rules***
1)	Persons (campus faculty, staff, students) have accounts in the system with personid (PK), name, email, cell, etc.  For faculty we also keep title, highest degree, and degreecollege.  For staff we keep Position and AdminYorN.  For students we keep GradYear and major plus type (undergraduate, graduate).  Only faculty, staff and students are included.
2)	We have Locations which are spots on campus where food can be delivered.  Some examples are dorms, the student center, and approved classroom buildings.  LocationID, LocationName, LocationAddress and (optional) Latitude and Longitude are maintained in the database. Additionally, a food delivery drop-off point is included (designated place for meeting or delivering food in the location – this can be a brief description).
3)	Persons can also be drivers (delivery personnel which have to be approved). Drivers have licensenumber and datehired plus ratings. You may also want to keep vehicle information (relative to the vehicle that the driver uses).
a.	UNCC will start with 8 approved delivery personnel – the system is in test mode.  You can assume all individuals have been cleared and they can be included in the database.  
b.	All delivery personnel are students.
4)	There is a flat fee of $5 for each delivery.  A person orders food one to many times.  An individual delivery is tied to one and only one person for the order.  The order is for one and only one restaurant.  For the items on the order we will only need to keep the total price and delivery charge, along with the driver and delivery times.  There should also be a unique identifier (ID) that ties to the id for the order at the individual restaurant.  You can assume that the actual items on the order need to come from the restaurant database.
5)	Food providers or restaurants have to be approved in order to be included in the database. Food providers/restaurants will have RestaurantID, location, schedule, pricerange, and rating. 
6)	The rating system will be a five-star rating system that is required after receiving an order. It is a two-part system: rating the delivery driver and rating the restaurant. Each rating will be linked to only one food order. There is a minimum of zero and a maximum of one rating per order. 

## ***EERD (full database)***
<img width="867" alt="Organized Campus Eats Diagram" src="https://user-images.githubusercontent.com/81598050/116302958-cbf56e80-a76f-11eb-8c05-ddcf704215de.png">



## ***MySQL Queries***
a) **display an average rating from the ratings table where restaurantid = 1**

SELECT avg(overall_rating)

FROM ratings, orders,

WHERE ratings.order_id = orders.order_id

AND orders.restaurant_id = 1;

<img width="124" alt="Screen Shot 2021-04-29 at 10 15 05 AM" src="https://user-images.githubusercontent.com/81598050/116565619-08da7600-a8d4-11eb-9a96-a4a70270e2eb.png">

b) **display an average rating from the restaurant table where restaurantid = 1**

c) **display all average rating from the drivers table where restaurantid = 1**

d) **display all of the orders made by a customer over a week**

SELECT *

FROM orders, delivery

WHERE orders.delivery_id = delivery.delivery_id

AND orders.person_id = 1

AND delivery_time BETWEEN  '2004-04-15 12:00:00' AND '2004-04-22 12:00:00';

<img width="889" alt="Screen Shot 2021-04-29 at 7 49 09 PM" src="https://user-images.githubusercontent.com/81598050/116631956-00aa2700-a924-11eb-8ae9-8b255fa1f72f.png">


## ***Stored Procedure***

## ***Web/App Implementation/Description of Future Work***

As described in our project, this database design is an enhancement to delivery systems on college campuses. Our improvement on the system comes in the form of the web and as an application as well. This system would be similar to those college campuses use, which allows it to be accessed by preference with a person’s campus logins and passwords. Creating a system like this serves two purposes, the first being a centralizing measure that allows for easy access across campus, and second, allowing restaurants and students to access information such as the menus and directions to delivery locations.

On the site/application, restaurant menus would be linked in and it would make access much easier for people to order food. The information included here would also be the estimated time of delivery, hours for the restaurant, and any other information provided by the restaurants such as the contact information.

This application would have options and prompts that allow students and faculty to register and get what they want to be delivered. During the delivery time, students and faculty would be provided with information on their delivery driver and details of the car so that they know when and what to expect. Further, once the food is delivered and confirmation is received, the recipients would be prompted to rate the experience and the delivery which would serve to improve the system and keep it running well. 

## ***MySQL dump***

## ***PPT Video***

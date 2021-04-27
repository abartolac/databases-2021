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

## ***Stored Procedure***

## ***Web/App Implementation/Description of Future Work***

## ***MySQL dump***

## ***PPT Video***

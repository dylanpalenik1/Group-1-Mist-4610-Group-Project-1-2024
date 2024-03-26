# Group 1 Mist4610 Group Project (Fall 2024)

## Team Name: 
61608 Group 1

## Team Members:

1. Dylan Palenik [@dylanpalenik1](https://github.com/dylanpalenik1)
2. Jordan Beal[@dylanpalenik1](https://github.com/dylanpalenik1)
3. Hayley Daniels[@hayleydaniels](https://github.com/hayleydaniels)
4. Aakash Dholakia[@dylanpalenik1](https://github.com/dylanpalenik1)
5. Dan Kerik[@dylanpalenik1](https://github.com/dylanpalenik1)
6. Lexie-anne Rodkey[@lexieRodkey](https://github.com/lexieRodkey)

## Problem Description:
The objective of this project is to model and develop a relational database that comprehensively covers all aspects of a soccer club’s operations. This includes Facilities, Training Sessions, Players, Managers, Squads, Matches, Sponsors, Injuries, and Player Stats. 

The database will be populated with valid sample data to reflect real-life scenarios and will be optimized for queries that help extract insights into player performance, squad efficiency, match outcomes, facility utilization, and the financial landscape of sponsorships.

By incorporating these entities and their relationships into the database, efficient management of club operations is ensured, encompassing tasks such as scheduling sessions, monitoring player participation, analyzing performance metrics, managing injuries, and facilitating sponsorship agreements. The database will serve as an informational hub for stakeholders and help the team make strategic decisions and achieve operational effectiveness within the soccer club

## Data Model:
In regards to the data model best suited for our scenario of a soccer club, twelve entities are required. These include Facilities, Training Sessions, Training Session Attendance, Manager, Players, Squad, Squad Composition, Matches, Match Sponsor, Sponsor, Injury, and Player Stats.

Starting with facilities, each facility can have multiple training sessions, and sometimes training sessions can exist without a facility, just like a facility can exist without any current training sessions. As such, having a non-identifying 1-M relationship, in this case, allows for more flexibility and independence between these entities.
In regards to training sessions, each training session can have one facility, but can also have multiple individuals in attendance at these sessions. Multiple training sessions can have multiple attendees. Therefore, an associative entity called Training Session Attendance was created. This entity links the Training Sessions with Players and Managers. This Training Session Attendance entity allows users to view who is and is not attending each training session by receiving the primary keys from the associated entities as foreign keys.

Players is a large entity related to multiple other entities. Players can attend training sessions, be part of a Squad, have multiple injuries, and play multiple matches. The relationship between Players and Training Sessions was previously mentioned as an M-M relationship with an associated entity named Training Session Attendance. The relationship between Player and Squad is also an M-M identifying relationship. Therefore, the associative entity named Squad Composition was created. Many players can play on many squads.

The relationship between Players and Matches is a M-M relationship. Multiple players can play multiple matches, and multiple matches can have multiple players. Because it is M-M, the associative entity labeled Player Stats was created. This entity contains the primary keys from Players and Matches as foreign keys.

It should also be noted that Players can receive injuries through their time in the club. Therefore the relationship between Players and Injury is 1-M. One player can obtain multiple injuries.

Squads can consist of multiple players, have one manager, and play multiple matches. Therefore there are three relationships defined in this case. These include the previously mentioned M-M relation between Players and Squad, a M-1 non-identifying relationship between Squad and Manager, and a 1-M non-identifying relationship between Squad and Matches. Each Manager can manage multiple squads, but each squad may only have one manager
<img width="815" alt="Screenshot 2024-03-25 at 10 37 48 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/98e0aea9-52d9-4c8e-b32d-d29f3eb1088b">

## Data Dictionary:
<img width="605" alt="Screenshot 2024-03-25 at 5 59 43 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/40ec4797-21c9-43d2-a46f-705a1ea5b11e">

<img width="614" alt="Screenshot 2024-03-25 at 5 59 24 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/fcbcfa7c-451d-47a3-852d-877c934e4219">

<img width="604" alt="Screenshot 2024-03-25 at 10 40 12 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/561e20dd-9a00-481f-b190-1d9cc298a1f1">

<img width="609" alt="Screenshot 2024-03-25 at 6 01 22 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/7dd9180d-3dff-4851-b4ab-b6cb88dfcb17">

<img width="611" alt="Screenshot 2024-03-25 at 6 00 47 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/d1cbd8ec-ad92-4e63-9ddd-8f3e8f9604a3">

<img width="612" alt="Screenshot 2024-03-25 at 6 00 11 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/939617ca-7ac3-4f22-92ee-073ef48afc82">

<img width="599" alt="Screenshot 2024-03-25 at 6 01 29 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/679f8fe9-fe8c-4061-84dc-3bf6005920a5">

<img width="595" alt="Screenshot 2024-03-25 at 6 00 58 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/2afb20ba-fee7-4ab4-8036-1ac2577bb9fe">

<img width="619" alt="Screenshot 2024-03-25 at 6 00 25 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/c1fdeed0-74a3-4dd5-aa1f-80cd83e7e0ae">

<img width="622" alt="Screenshot 2024-03-25 at 6 01 36 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/d89372c2-66ea-48d2-a312-7c7ae0b3ef26">

<img width="594" alt="Screenshot 2024-03-25 at 6 01 15 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/e532ee3f-2d37-4931-bf7b-2a5ede1c7b7e">

<img width="604" alt="Screenshot 2024-03-25 at 6 00 35 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/09f7d41d-a440-4abe-817e-0b0cac6b4c2e">

## Queries:

## Database information:

Name of the database: ns_Sp24_61608_Group1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format:

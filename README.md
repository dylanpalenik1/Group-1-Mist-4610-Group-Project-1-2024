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

<img width="692" alt="Screenshot 2024-03-26 at 5 59 51 PM" src="https://github.com/dylanpalenik1/Group-1-Mist-4610-Group-Project-1-2024/assets/164935337/ec64138e-6082-4c74-a2a9-f4c569a6b1ec">

## Data Dictionary:


## Queries:

## Database information:

Name of the database: ns_Sp24_61608_Group1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format:

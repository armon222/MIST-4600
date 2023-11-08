# Team 4 MIST 4610 Group Project 1

## Team Name
15061 Group 4

## Team Members
1) Joey Lund [@jl4600](https://github.com/jl4600) 
2) Armon Parsa [@armon222](https://github.com/armon222)
3) Kyle Szabo [@kszabo2390](https://github.com/kszabo2390)

## Problem Description:

The challenge is to model and build a relational database for the operations of a new football club called the Georgia Lions. In the model, the main entity is Players, which describes all of the players personal information and statistics on the field. The other entities either support, magnify, monetize, or track player performance and relationships with other parts of the Georgia Lions operation. For this new team, we want to comprehensively model these relationships, obtain data for the entities, and use queries to answer questions which will help evaluate performance on and off the field of the club. 

## Data Model:

### Explanation of data model:

The data model is based off the necessary operations for a football club. The managers entity describes all the different types of people who work in the front office of the club in scouting, player development, and overall team evaluation. The managers hire many coaches, who report to the many managers as their bosses. This creates the many to many relationship between Coaches and Managers, with Managers_has_Coaches as the weak entity. The coaches entity describes the many coaches in the organization by name, role, and salary. 
The coaches have many players that they coach, but each player has one coach that trains them specifically (ex. Defensive coach trains the defensive players). This establishes the one to many relationship between Players and Coaches. As described earlier, Players is the main entry in the database, representing information about the players name, nationality, individual statistics, and who is their coach. 


The Players table branches off in a few different directions, the Youth Academy table represents all the players who are on the youth squad. This table gives the youth player’s name, birthday, position, nationality, and ID. There are many players in the youth academy, but players can only belong to the one Youth Academy, creating a one to many relationship. Going to another branch, Players can play in many Matches, and this creates a many to many relationship where Injuries is the associative entity. Matches allow for all team results on the schedule to be tracked. The Injuries table illustrates injury type and severity for a player in a match. 


The external factors of the club are tracked as well, The Fans table shows a fan’s name, email address, the amount of team merchandise they have purchased, and whether or not they are a season ticket holder. Fans attend many Matches, and Matches have many Fans, so this creates another many to many relationship, creating an associative entity we called Stadiums. The stadium's entity uniquely identifies each stadium, which fans are in attendance, which match is being played at the stadium, as well as the stadium name and capacity. 


The sponsors table describes the important details about our club sponsors like sponsor name, contact information, and the value of their contract with the club. Sponsors are at many Matches, and Matches have many Sponsors, so we created an associative entity called Sponsorship, giving more granular detail about each individual sponsorship at each match. 


Lastly, the Fans entity and Players entity has a many to many relationship, because fans like many Players, and Players have many Fans. We created the Favorite Players entity to track which Players are fan favorites!

### The Data Model
![image](https://github.com/armon222/MIST-4600/assets/62662242/88d1fe69-6064-4164-99c0-42c5e63dd189)


## Data Dictionary

### Table: Matches

![image](https://github.com/armon222/MIST-4600/assets/62662242/01413aaf-676a-4f17-8228-649b64891ad2)

### Table: Coaches

![image](https://github.com/armon222/MIST-4600/assets/62662242/4198559d-c50f-432b-85f3-eafee03ce2f1)

### Table: Fans

![image](https://github.com/armon222/MIST-4600/assets/62662242/849c54d3-6325-4d3e-90f5-cdaea535b1d2)

### Table: FavoritePlayers

![image](https://github.com/armon222/MIST-4600/assets/62662242/fe1c7831-8955-4ac7-9025-079289afdb13)

### Table: Managers

![image](https://github.com/armon222/MIST-4600/assets/62662242/3197194d-230f-4120-83ab-db6fb6c3bc17)

### Table: Sponsors

![image](https://github.com/armon222/MIST-4600/assets/62662242/9ab5d236-dd7f-4cd2-8112-bd1dc90cfe26)

### Table: Sponsorships

![image](https://github.com/armon222/MIST-4600/assets/62662242/87f9e193-17af-45bc-8437-0d5cae01705f)

### Table: Stadium

![image](https://github.com/armon222/MIST-4600/assets/62662242/ee7a2190-da5c-4673-a4cc-e62543e02b5e)

### Table: Youth Academy

![image](https://github.com/armon222/MIST-4600/assets/62662242/ff190c37-fb64-44e2-bc3e-bb50d5e8511b)

### Table: Players

![image](https://github.com/armon222/MIST-4600/assets/62662242/62799eb1-8107-4790-b10e-04c54bcab042)

### Table: Injuries

![image](https://github.com/armon222/MIST-4600/assets/62662242/6414d925-7bcb-40c0-a2db-47d1aee66724)

### Table: Manager_has_Coaches

![image](https://github.com/armon222/MIST-4600/assets/62662242/e2c73b61-41cd-4fc4-aa45-82172287582d)

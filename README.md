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




![image](https://github.com/armon222/MIST-4600/assets/62662242/18813714-7174-4a80-85ed-7fb77afd6a6a)


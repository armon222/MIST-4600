# Team 4 MIST 4610 Group Project 1

## Team Name
15061 Group 4

## Team Members
1) Joey Lund [@jl4600](https://github.com/jl4600) 
2) Armon Parsa [@armon222](https://github.com/armon222)
3) Kyle Szabo [@kszabo2390](https://github.com/kszabo2390)

## Problem Description:

The challenge is to model and build a relational database for the operations of a new football club called the Georgia Lions. In the model, the main entity is Players, which describes all of the player's personal information and statistics on the field. The other entities either support, magnify, monetize, or track player performance and relationships with other parts of the Georgia Lions operation. For this new team, we want to comprehensively model these relationships, obtain data for the entities, and use queries to answer questions that will help evaluate performance of the club. 

## Data Model:

### Explanation of data model:

The data model is based on the necessary operations for a football club. The managers entity describes all the different types of people who work in the front office of the club in scouting, player development, and overall team evaluation. The managers hire many coaches, who report to the many managers as their bosses. This creates a many-to-many relationship between Coaches and Managers, with Managers_has_Coaches as the weak entity. The coaches entity describes the many coaches in the organization by name, role, and salary. 
The coaches have many players that they coach, but each player has one coach that trains them specifically (ex. Defensive coach trains the defensive players). This establishes the one-to-many relationship between Players and Coaches. As described earlier, Players is the main entry in the database, representing information about the player's name, nationality, individual statistics, and who is their coach. 


The Players table branches off in a few different directions, the Youth Academy table represents all the players who are on the youth squad. This table gives the youth player’s name, birthday, position, nationality, and ID. There are many players in the youth academy, but players can only belong to one Youth Academy, creating a one-to-many relationship. Going to another branch, Players can play in many Matches, and this creates a many-to-many relationship where Injuries are the associative entity. Matches allow for all team results on the schedule to be tracked. The Injuries table illustrates injury type and severity for a player in a match. 


The external factors of the club are tracked as well, The Fans table shows a fan’s name, email address, the amount of team merchandise they have purchased, and whether or not they are a season ticket holder. Fans attend many Matches, and Matches have many Fans, so this creates another many-to-many relationship, creating an associative entity we call Stadiums. The stadium's entity uniquely identifies each stadium, which fans are in attendance, which match is being played at the stadium, as well as the stadium name and capacity. 


The sponsors table describes the important details about our club sponsors like sponsor name, contact information, and the value of their contract with the club. Sponsors are at many Matches, and Matches have many Sponsors, so we created an associative entity called Sponsorship, giving more granular detail about each individual sponsorship at each match. 


Lastly, the Fans entity and Players entity have a many-to-many relationship, because fans like many Players, and Players have many Fans. We created the Favorite Players entity to track which Players are fan favorites!

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


## Queries

### Feature Matrix

![image](https://github.com/armon222/MIST-4600/assets/62662242/d30d178b-a4c1-4835-b00a-44f96d633f64)

### Query 1

Query lists the injuries players on the Lions have suffered playing at their home field. Results are ordered by Player's Last Name in descending order.


![image](https://github.com/armon222/MIST-4600/assets/62662242/a531848b-c179-4214-9e79-383586a95f40)

Query one allows the managers to see the number and type of injuries occurring to players on the Lions' home field. This shows potential dangers that might arise from the design or texture of the playing surface. This query influences managers' decisions on how to design the field in the future, as well as lets the medical and training staff better prepare for injuries that may occur during a game

### Query 2

Query 2 lists the favorite players of fans who are from the United States. The query concatenates the player's first and last name, and results are ordered by the player's first and last name descending.

![image](https://github.com/armon222/MIST-4600/assets/62662242/4fb2e766-906b-46fd-a573-4e6f2813c9c6)

Query 2 allows the managers to see who the most popular players on the team are who are from the United States. This is particularly important since the Lions play in Georgia the American players might be more marketable to the fans. Seeing this information might help the management team figure out which players to use in community events or to promote the team locally. 

### Query 3

Query 3 lists the Fan's first and last name, email address, and amount spent on team merchandise that are season ticket holders.

![image](https://github.com/armon222/MIST-4600/assets/62662242/0159ff76-5e61-4704-be1c-c9550ef2901e)

Query 3 shows the management team the new Fans of the team and their contact information. This is valuable information because the team now can further contact these Fans with more deals and ways to get them into more games. The Lions also know how much they spend on Merchandise, so they can specifically offer them deals related to the cost of items they tend to purchase. 

### Query 4

Query 4 lists the player's first and last name, and the type of injury sustained only for players who have scored higher than the average amount of goals on the team. 

![image](https://github.com/armon222/MIST-4600/assets/62662242/a45e3b4b-2903-49be-b79f-4b59c8bc5d48)

Query 4 is very important for the coaching staff because this shows the types of injuries being suffered by the team's best scoring threats. The organization needs to know what type of injuries these players sustained, so they figure out how long they need to be replaced. This information is also important to the medical staff so they can properly treat these players to get back on the field as soon as possible.

### Query 5

Query 5 lists player's last name and the average of the sum of player's goals and assists (points). The average is only listed if it is greater than the average points for the team. 

![image](https://github.com/armon222/MIST-4600/assets/62662242/e56d1f9b-8d14-4801-b393-b13e3964ce4a)

Query 5 shows the coaching staff which players produce the most offense for the team. This information is valuable for strategic purposes, because when the team needs a goal the coaching staff knows these players have the best chance to create offense. This query is also good for evaluating player value when players are negotiating new salaries for contracts. 

### Query 6

Query 6 shows the manager's last name, manager's role in the front office, and the average salary of the manager in the front office.

![image](https://github.com/armon222/MIST-4600/assets/62662242/6d73f7fe-7e43-49ce-8326-dd00fb232402)

Query 6 illustrates the value of the top executives to the team. This information could help decision-making when deciding a manager's salary down the line or a comparable to new manager salaries when they are hiring. The numbers listed above can serve as a baseline for negotiations between ownership and the team.

### Query 7

Query 7 lists the first and last name for players that have not been injured yet this season. 

![image](https://github.com/armon222/MIST-4600/assets/62662242/235710a6-adcd-4fd3-89ce-2ccab176b9c9)

Query 7 allows management to determine which players have been the most durable to the team, which helps assess the value of the player to the team. This can be important when the player and team negotiate a salary for future contracts because if the player is durable and avoids getting hurt they bring more value to the team. Query 7 is also valuable to the medical staff because they can see how the players listed above manage to stay healthy and on the field.

### Query 8 

Query 8 lists the company name, match opponent, and the average company contract amount with the club. The average amount has to be greater than 1,000,000.

![image](https://github.com/armon222/MIST-4600/assets/62662242/26cda41b-4792-46c8-aac1-201353b459e0)

Query 8 shows the major sponsors of the club. The club has some smaller sponsors as well, so the having clause makes the average be at least one million to show the major company sponsors. This information helps the Lions prioritize their highest-value customers and prepare for the match dates where they are sponsors. 

### Query 9 

Query 9 lists the match result and match opponent for matches in the Lions' home stadium.

![image](https://github.com/armon222/MIST-4600/assets/62662242/cbe47bec-7337-4fb2-a7c2-62a4b14f9399)

Query 9 is important to the organization because it illustrates how the team is performing on the home field. Even though these matches are worth the same as away games in the standings, these games are more important because our Fans pay good money to attend the games and we want to put on a winning product for them. So it's very important to win lots of games at home to appease the fans, sponsors, and management. 

### Query 10

Query 10 lists the player's last name, player position, coaching role, and the average amount of yellow cards for each player. This information is only shown if the player has an average amount of yellow cards greater or equal to 1.

![image](https://github.com/armon222/MIST-4600/assets/62662242/1d9e9d90-c377-4d9a-b480-c906448a0fe0)

Query 10 demonstrates which players are getting the most yellow cards, and which coach is their position coach. Query 10 is a good way to evaluate which players are the most undisciplined, so the coaching staff can try to help the player fix this issue. Query 10 also shows which coach has the most undisciplined players, which implies this coach may need to change their tactics. Query 10 is also a good tool for player evaluation, especially when negotiating player salaries.

## Database Information

Name of the database: cs_g4p1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();

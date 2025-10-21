# MIST4610Project1
MIST 4610 Project 1 Group 1 Srinivasan Fall 2025

# Team Name:
Group 1 

# Team Members:
1. Pragnya Nallagonda [@PragnyaNal](https://github.com/PragnyaNal)
2. Carter Trent https://github.com/mct29403
3. Kohan Davis https://github.com/krd90067
4. Eric Mied https://github.com/ericmied

# Problem Description:
Our goal was to build a database storing information of a mixed martial arts league. The main entity is the fights and we aim to store data to organize and efficiently compare aspects of the fights. To compare and provide further insight into the data we plan to use queries to filter the data into information.

# Data Model
The highest entity in our model is the event entity. Each eventID represents each fight card or tournament organized by the company, containing information such as event name, date, location, and promotion details. Since each event has multiple fights but a single fight cannot be a part of multiple events it is a one to many relationship.

The Fight entity is central to the model and represents each individual bout that takes place within an event. Each fight includes information such as round schedule, fight result, and the two fighters who compete. Because one fight involves two fighters and a fighter can participate in many fights, the Fight table has two foreign keys referencing the Fighter table to distinguish between competitors. The Fight entity also connects to the Referee, Judge, and FightResult entities, allowing the system to capture the full administrative and scoring details of each bout.

The Fighter entity stores biographical and competitive data about each athlete, including name, nationality, date of birth, height, and weight. Each fighter belongs to a specific WeightClass, establishing a many-to-one relationship between Fighter and WeightClass. Fighters are also associated with a Gym, which represents the training facility or team they belong to. The Gym entity contains gym name and location information and has a one-to-many relationship with the Fighter entity, since each gym can have many fighters.

To record the outcome of each fight, the FightResult entity stores details such as the method of victory, round and time ended, and result description. This data provides transparency for how fights are won or lost. Similarly, the FightJudgeScore entity serves as an associative entity between Fight and Judge, representing the scores assigned by each judge for a specific fight. This allows multiple judges to evaluate the same bout independently, with each score tied to both a judge and a fight.

The Referee entity stores information about referees who oversee fights, and each referee can officiate multiple fights, creating a one-to-many relationship between Referee and Fight.

Finally, the Sponsorship entity represents commercial partnerships between fighters and brands. Each sponsorship record includes brand name, contract start and end dates, and the associated fighter, establishing a many-to-one relationship between Sponsorship and Fighter.

<img width="724" height="236" alt="image" src="https://github.com/user-attachments/assets/6a045835-5b7c-4a34-969e-475baab057ce" />

# Data Dictionary
<img width="532" height="635" alt="Screenshot 2025-10-21 161653" src="https://github.com/user-attachments/assets/6b36c2aa-f7f0-41e1-83b0-65ebdb701867" />
<img width="531" height="661" alt="Screenshot 2025-10-21 161704" src="https://github.com/user-attachments/assets/89dfbba6-ab26-4269-9366-ab2624beb6d6" />
<img width="529" height="571" alt="Screenshot 2025-10-21 161710" src="https://github.com/user-attachments/assets/dca3ed63-4681-4c2e-847c-dda19e2f6e67" />
<img width="540" height="385" alt="Screenshot 2025-10-21 161715" src="https://github.com/user-attachments/assets/de72c664-8793-476b-8394-be77d69b54de" />


# Queries

# Database information
Name of the database: ns_F25MIST4610_15058_Group1

# PHP / Oracle Racing Web Application

## General Description
This project consists of a web application developed using PHP and an Oracle database to manage vehicle racing activities.

The application allows users to register vehicles, participate in races, manage race results, and query race-related data such as participants, times, and ceremonies. It integrates backend logic with database operations and provides a structured interface for interacting with racing events.

The project places special emphasis on:
- Server-side development using PHP
- Database interaction with Oracle (SQL)
- Modular organization of functionality
- Clear separation between logic, interface, and data access

---

## Main Features
- Vehicle registration and management
- Display of registered vehicles
- Registration of users in races
- Entry and management of race times
- Viewing race participants and classifications
- Advanced queries related to ceremonies and Pinky consumption

---

## Project Structure
The project is organized into different files, each with a clear responsibility:

### General Files
- **exemple.css**  
  Defines the visual style and layout of the web interface.

- **funcions.php**  
  Contains common functions used throughout the application.

- **practicaPHP.html**  
  Main home page of the application.

- **errorlogin.php**  
  Displays login-related error messages.

- **menu.php**  
  Displays the main navigation menu.

- **practicaPHP.sql**  
  SQL script used to create the database tables required for options f1) and f2).

---

## Application Options

### a) Register a Vehicle
- **altavehicle.php**  
- **altavehicle_BD.php**

Allows the user to insert a new vehicle by providing information such as description, color, fuel type, price, and consumption.

The vehicle code is automatically generated using the group code and the vehicle description.  
If the generated code already exists, a random three-digit number is added to ensure uniqueness.

---

### b) Display Vehicles
- **mostrarVehicles.php**

Displays a list of all vehicles registered in the database.  
Each entry shows:
- Vehicle code
- Description
- Color
- Fuel type
- Consumption
- Fuel cost per 100 km
- Owner’s name

---

### c) Register in a Race
- **inscripcioCursa1.php**  
- **inscripcioCursa2.php**  
- **inscripcioCursa3.php**  
- **inscripcioCursa4.php**  
- **inscripcioCursa5.php**

Allows users to register character–vehicle pairs in open races.

The system verifies that:
- The user owns both the selected character and vehicle
- Each user can register only one pair per race
- The user has sufficient balance to pay the race fee

Once registered, the race fee is deducted from the user’s balance.  
Multiple registrations are allowed until the user completes participation.

---

### d) Enter Race Times
- **entraTemps1.php**  
- **entraTemps2.php**  
- **entraTemps3.php**

Allows the selection of a closed race to enter finishing times for its participants.

- A `NULL` time indicates that the participant abandoned the race
- After saving times, the best time is calculated and stored
- If enabled, ceremonies or inspections are also updated
- Time entry is blocked if the ceremony or inspection has already been completed

---

### e) View Race Participants
- **consultarParticipants.php**  
- **consultarParticipants_BD.php**

Displays the list of participants for a selected closed race.

- If no times are entered, the list is labeled *“List of participants”*
- If times exist, the list is labeled *“Race classification”* and ordered by finishing time
- Participants who abandoned the race are indicated with a `NULL` time
- Both vehicle and character information is displayed for each pair

---

### f) Additional Options

#### Option F: Select between f1) and f2)
Allows the user to choose between two advanced query options.

---

#### f1) Query Total Pinky by Date (Ceremonies)
- **consultaCerimonies.php**  
- **consultaCerimonies_BD.php**

The user enters a date range.  
The system returns a list of characters who participated in ceremonies during that period, showing the total amount of Pinky consumed per character.

---

#### f2) Query Ceremonies by Character
- **quantitatPinky.php**  
- **quantitatPinky_BD.php**

The user selects a character.  
The system displays all ceremonies in which the character participated, including:
- Race name
- Date
- Finishing position
- Amount of Pinky consumed

Results are ordered from the oldest to the most recent.



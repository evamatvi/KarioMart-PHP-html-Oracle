README – PHP/Oracle Racing Web Application

-**exemple.css**: CSS interface
-**funcions.php**: functions used
-**practicaPHP.html**: home page
-**errorlogin.php**: shows login errors
-**menu.php**: displays menu
-**practicaPHP.sql**: table created for options f1) and f2)

**a) Register a vehicle**

-altavehicle.php

-altavehicle_BD.php

Allows the user to insert a new vehicle with fields like description, color, fuel, price, etc.
The vehicle code is auto-generated from the group code and vehicle description.
If the code already exists, a random 3-digit number is added.


**b) Display vehicles**
-mostrarVehicles.php

Shows a list of all vehicles registered in the database.
Each entry displays the vehicle code, description, color, fuel type, consumption, fuel cost per 
100km, and owner's name.

**c) Register in a race**
-inscripcioCursa1.php

-inscripcioCursa2.php

-inscripcioCursa3.php

-inscripcioCursa4.php

-inscripcioCursa5.php

Lets users register character/vehicle pairs into open races.
Verifies same user owns both character and vehicle.
Each user can only register one pair per race.
Checks if the user has enough balance and deducts the race fee.
Allows multiple registrations until the user finishes.

**d) Enter race times**
-entraTemps1.php

-entraTemps2.php

-entraTemps3.php

Selects a closed race to input finish times for participants.
Null times mean the participant abandoned the race.
After saving times, the best time is calculated and stored.
If enabled, also updates ceremonies or inspections.
Time entry is blocked if the ceremony or revision was already done.

**e) View race participants**
-consultarParticipants.php

-consultarParticipants_BD.php

Shows the list of participants of a selected closed race.
If no times entered: labeled "List of participants".
If times exist: labeled "Race classification" and ordered by time.
Also shows if a participant abandoned the race (time is NULL).
Displays both vehicle and character info for each pair.

**-opcioF: lets the user select between f1) and f2) options** 

**f1) Query total Pinky by date (Ceremonies)**
-consultaCerimonies.php

-consultaCerimonies_BD.php

User enters two dates.
Returns a list of characters who participated in ceremonies during that range.
Shows total Pinky consumed per character.

**f2) Query ceremonies by character**
-quantitatPinky.php

-quantitatPinky_BD.php

User selects a character.
Lists all ceremonies the character participated in.
Shows race name, date, finishing position, and Pinky consumed.
Ordered from oldest to most recent.

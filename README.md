
GeoGame – Turkish Cuisine Location Game 

📌 1. Game Idea and Purpose
This GeoGame is an interactive map-based quiz where the player identifies which Turkish city a displayed famous local dish belongs to.A random dish photo appears on the screen, and the player must click the correct city on the Turkey map.
Goal: Score as many points as possible within 60 seconds.

📌 2. Game Rules
-Correct answer: +5 points
-Wrong answer: –1 point
-Time limit: 60 seconds
-No lives (unlimited attempts before the time ends).
-Dish image is shown on the left panel.
-Player selects the city by clicking on the interactive map.
-New dish appears after each guess.

📌 3. Game Flow
Start Screen:
-Displays game instructions and rules.
-User presses Start.

Game Screen:
-Left panel: Dish image
-Right panel: Interactive Turkey map (Leaflet)
-Top bar: Remaining time + Current score

Gameplay:
-Player clicks a city to guess the origin of the dish.
-System shows correct/incorrect feedback.
-New dish appears automatically.

End Screen (after 60 seconds):
-Shows final score
-Button: Play Again

📌 4. Frontend Layout Sketches

Sketch 1 – Start Screen:

Title: Turkish Cuisine GeoGame

Description:
- A dish image will be shown.
- Click the correct city on the map.
- Earn points and beat the timer!
Rules:
- Correct answer: +5 points
- Wrong answer: -1 point
- Time limit: 60 seconds
[ START BUTTON ]


Sketch 2 – Game Screen:
Left Panel:
- Dish image
Right Panel:
- Interactive Turkey map (Leaflet)
Top Bar:
- Time left: 47 s
- Score: 12


Sketch 3 – End Screen:

GAME OVER
Final Score: 23
[ PLAY AGAIN BUTTON ]





📌 5. Technical Requirements
JavaScript Library
-Leaflet.js (for interactive map)
-GeoJSON file of Turkey’s 81 provinces will be used for click detection.

Data Requirements
Each city will include:
-Name
-Famous local dish
-Dish photo (.jpg, optimized size)

📌 6. Difficulty / Progression
-No difficulty levels.
-Game uses time-based progression:
The player answers as many questions as possible within 60 seconds.

📌 7. Number of Questions
There is no fixed number of questions.
The total depends on how fast the user answers—typically 10–15 questions within one minute.

📌 Full Game Flow Diagram

flowchart TB

%% START SCREEN %%

A1([Start Screen]) --> A2[Show Game Title]
A2 --> A3[Show Description and Rules]
A3 --> A4[START Button Clicked]

%% GAME INITIALIZATION %%

A4 --> B1[Initialize Game]
B1 --> B2[Set Score = 0]
B2 --> B3[Set Time = 60 sec]
B3 --> B4[Load Turkey GeoJSON]
B4 --> B5[Load Food Dataset (City → Dish Image)]
B5 --> B6[Display Game Screen]

%% GAME LOOP %%

B6 --> C1{Time > 0?}

C1 -- Yes --> C2[Select Random City]
C2 --> C3[Show Dish Image in Left Panel]
C3 --> C4[Wait For Player to Click a City on Map]

%% PLAYER GUESS LOGIC %%

C4 --> D1{Clicked City == Correct City?}

D1 -- Yes --> D2[+5 Points]
D2 --> D4[Show “Correct!” Feedback]
D4 --> C1

D1 -- No --> D3[-1 Point]
D3 --> D5[Show “Wrong!” Feedback]
D5 --> C1

%% TIME RUNS OUT %%

C1 -- No --> E1([End Screen])
E1 --> E2[Show Final Score]
E2 --> E3[Show “Play Again” Button]

E3 --> A1


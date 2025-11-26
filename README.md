play game : https://gmt-458-web-gis.github.io/geogame-keklikduygu99/ 


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
<img width="1221" height="348" alt="baş" src="https://github.com/user-attachments/assets/2643a6c6-ecc9-4361-90d6-8e8cec6edf92" />


Game Screen:
-Left panel: Dish image
-Right panel: Interactive Turkey map (Leaflet)
-Top bar: Remaining time + Current score

<img width="1230" height="756" alt="Ekran görüntüsü 2025-11-26 211414" src="https://github.com/user-attachments/assets/b110c153-a5c8-4d8f-9fd3-0f0f4a7bc80f" />


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

Sketch 2 – Game Screen:
Left Panel:
- Dish image
Right Panel:
- Interactive Turkey map (Leaflet)
Top Bar:
- Time left: 47 s
- Score: 12


Sketch 3 – End Screen:

Final Score: 23
[ PLAY AGAIN BUTTON ]

<img width="1221" height="270" alt="son" src="https://github.com/user-attachments/assets/f398ae72-60b9-4ad2-b9c5-800c5bb2794d" />



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




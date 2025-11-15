[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/BhShQpq1)
GeoGame – Turkish Cuisine Location Game (Design Document)
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
Sketch 1 – Start Screen
--------------------------------------------------------
|               Turkish Cuisine GeoGame                |
--------------------------------------------------------
|  Identify the Turkish city of the dish shown on      |
|  the screen by clicking it on the map.               |
|                                                      |
|  + Correct answer: +5 points                         |
|  + Wrong answer: -1 point                            |
|  + Time limit: 60 seconds                            |
|                                                      |
|                      [ START ]                       |
--------------------------------------------------------

Sketch 2 – Game Screen
 -----------------------------------------------------
|   Dish Image       |     Interactive Turkey Map     |
|   (left panel)     |      (Leaflet + GeoJSON)       |
 -----------------------------------------------------
|  Time left: 47 s   |     Score: 12                  |
 -----------------------------------------------------

Sketch 3 – End Screen
 -------------------------------
|           GAME OVER           |
|        Final Score: 23        |
|                               |
|        [ Play Again ]         |
 -------------------------------

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

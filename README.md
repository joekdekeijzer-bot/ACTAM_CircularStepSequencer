# Introduction
For this project I wanted to take something quite standard and give it a unique twist. So I decided to create a drum machine with a circular step sequencer. I got the inspiration from the course "Computer Music: Representations and Models". In this course we watched a video where different rhythms where represented in a circular manner and thought is was a quite intuitive way of looking at rhythm. I also thought it would be fun to play around with different rhythms that way, so this project was a perfect oppurtunity for creating it.

I wanted to focus on making the experience of using the sequencer as user friendly as possible. To achieve this goal I set a few requirements:
* It had to be **intuitive** to use,
* I wanted it to be **visually pleasing**,
* and it had to be **minimalistic**, with few distractions.

On top of that I wanted it to have a electric/futuristic sound, it had to feel like a modern drum machine.

# Technologies Used
HTML Was used for the main content of the project and CSS for the formatting and the graphics for the control center. 
Furthermore, JavaScript was used for:
* Creating the music with help of the Tones.js module.
* The sequencer graphics with the use svg (this makes it easier to work with circular objects)
* Saving/loading through communication with the Firebase database.
* Logic of the control center

## Course Concepts
The course conepts addressed in this web based project are of course the use of HTML, CSS and JavaScript. 
Additionally, Tone.js is used for the creation of music and the project also makes use a database, for which Firebase Firestore is used.

# Descritpion of the project
## Graphics
Two panels: The controls (visuals done with css) and the Step Sequencer (visuals done with JS using svg). 
Angular math (big reason for svg)
## Music
Tones.Js
## Firebase
Used for saving sequences and their settings

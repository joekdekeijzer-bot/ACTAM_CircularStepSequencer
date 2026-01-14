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

How to start (Libraries, code editor, play the first sound using Tones.js)

## Course Concepts
The course conepts addressed in this web based project are of course the use of HTML, CSS and JavaScript. 
Additionally, Tone.js is used for the creation of music and the project also makes use a database, for which Firebase Firestore is used.

# Descritpion of the project
## Graphics
I start with defining the style using CSS, here the graphics of the general app and the control center are defined. The look of the panels, buttons, sliders and tekst are defined, as well as some general colors that are used.
Then, using HTML, two panels are defined: the control panel and the sequencer panel. In the control panel all the buttons and sliders are defined. In the sequencer panel, the trash bin and a few graphics for the use of svg are defined. This is the control panel:
<img width="749" height="478" alt="image" src="https://github.com/user-attachments/assets/5bc2089b-9c3e-4eb1-bbba-b1e851a500b6" />
 
Firstly, some constants and variables are defined, like the bpm, amount of steps and the location and radius of the circle. The circle itself is defined using svg (Scalable Vector Graphics), this makes it easier to work with radial coordinates, which is perfect for this project. The function drawGrid defines a circle and its ticks, these ticks represent the steps where drum sounds can be placed on. Then there's is also a function called drawPlayhead, this function creates a line from the center of the circle to a point on the circle to indicate where we are in time. Lastly, there are the functions makeDraggable and renderNotes, which allow for drum sounds to be placed on the circle. All sounds have their own corresponding color.

<img width="708" height="672" alt="image" src="https://github.com/user-attachments/assets/4c299dcd-a61d-4a3e-af96-547a082ba0fa" />

## Music
All the drum sounds are defined in an array, and send to destination, using the Tones.js module. The sounds can be played using a function called triggerDrum.
When the "Play" button is clicked, it starts the time and the function ```animate``` is triggered. a playhead appears and starts spinning around the circle. A function called processAudioTriggers, checks if the playhead passes a drum sound. When is does, it calls the triggerDrum function to make its corresponding sound(s). 


## Firebase
It starts with the Firebase configuration, this allows for communication with a database where songs can be saved.
Used for saving sequences and their settings

# The Readme - How I Approached Each Problem

## But First, Some Background
Now, I know you might be a bit pissed by how I have this section in my Readme (despite a perfectly good section for this in ), but I feel that this section may help you guys understand why I did what I did.
So, coming the the main point: I am not a Python-first coder (that goes to one of HTML - if you count it, JS or C).
I am also not the most well-acquainted with Arduinos, despite writing code for the same, because of my having been away from that scene for a good amount of time ('Cause JEE - no more needs to be said).
So, some of my moves may feel a bit sneaky, but trust me, that was some of the best I could give in these circumstances (mostly involving remembering what i gleaned of my brother's books and "Now, how the hell did that go?", respectively).
Anyway, thank you for your understanding. The real stuff starts now.

## Problem 1: Data sorting and plotting form a CSV in Python
For this, I had an idea of what tools I wanted to use for the data part - MatPotLib  for plottinga and SciPy/NumPy for data processing and value regeneration.
For the CSV-to-Array transformation, after some light research, I arrived at the native CSV library, which I judged as the most optimal for my use case,and thus chose.
After this, my plan fell into place rather easily :
CSV -> Array with all values -> Filter for valid values -> Array of valid values -> Interpolate by SciPy, completing the array -> Filled up array -> Graph for MatPlotLib
And this (hopefully) reflects in my code. Of course, there were detours and hiccups (mostly in the filtering phase, due to Python's array-manipulation quirks and the data's arrangement in the CSV), but that was the broad pattern which I kept in mind while coding.

##  Problem 2: Multisensor Arduino-based circuit, with LCD output
In this, by contrast, I knew the main problem: Getting the LCD working on an Arduino (because previous exposure to 16x2 LCDs told me that would be quite a pain).
Then, almost by accident (no, but seriously - I was looking for samples), I found the TinkerCAD I2C LCD display example, which I gladly accepted and based my project on (you can see its remenants in the single-line comments in my codes).
So, yeah, that was where I got a leg-up from there.
But that was not the end (because let's be honest, how could it be?).
What do I mean? Well, after help in the circuit, it was the turn of *codeblocks* to come save me. 
Basically, for the ultrasonic sensor, there was a codeblock that handled the distanec calculations, converting the value to centimetres while handling the triggering of the sensor and its reading of the echo for me.
So, after adding this block to my code, I switched to text mode (because let's face it, blocks are cute and...yeah, that's about it - hey, I may know Arduino coding, but even I haven't been near a distance sensor in over 2 years. Please, cut me some slack). then kept the equivalent C++ code in my script (the reason there is a function for distance measurement). After that, it was relatively easy to get the code up and running.
Now, for my thinking, while initially, I was trying to fit all acts in one giant, monolithic conditional block, upon giving the instructions a closer read, I realised the better method: Take inputs, assign status codes to eact given condition, then operate the code based on that, leading to cleaner code and easier debugging. After that, it was honestly a cakewalk (the experince finally came in handy, thank God).
### And with that, I leave you. Hope you enjoyed my Readme and code, and felt it worthy. Hoping to see you all in the next roudd!
### Signing off,
### Vikram Singh (2026AAPS0365H)

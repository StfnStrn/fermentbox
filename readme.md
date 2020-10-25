# Introduction

Baking with sourdough benefits from controlled temperatures. Normal room temperature is usually between 18°C and 22°C. Sourdough requires a wider 
temperature range to develop a rich flavour. While bakeries use professional equipment to provide such a controlled environment, hobbyists as me 
either stick to room temperature, buy a prebuilt solution or build one themselves. After some experiments, I now opt for the latter. 

I plan to use a wooden box where I can put a bowl with sourdough in. In the box, I want to use a heating mat or maybe a Peltier element to heat - 
or even - cool the temperature, so it stays in the desired range. But while a simple thermometer with a switch would do for that, the Arduino solution 
can do more. It would allow to perform a multi-stage environment, where the temperature can be set to different values over time. 

# Contents
## Software
The most important part here will be the software. It should contain both code and documentation for anyone willing to rebuilt the box, adapt or extend
the software. The ideas I have so far:
- Allow to set a temperature and use the heat mat to rise the temperature, if it's too low. 
  - Optionally: use a step motor to open the box lid if the outside is cooler to reduce the temperature. 
- Allow to define stages. One stage has a temperature and a duration. Once set, the program can be started and the software will control head mat and maybe
the lid keep the temperature in range. 
- Allow to define temperature drops, giving start value, end value and how long it takes to reach it. When the program is started, it will aim for the start 
temperature and from there it computes a linear temperature drop to reach the end temperature after the given duration.
- Preset profiles with the known profiles for sourdough treatments. 
- Optionally make it available monitoring via smartphone, so you can monitor the temperatures in your box inside your home net or even online. 
- Optionally make it programmable via smartphone, so you don't need to deal with an LC Display and small buttons, but you can use an app with more comfort from anywhere.
- Make it fail-safe against power loss. Even in case of a power loss, continue where the profile has been left, or use a real time clock to continue at 
the appropriate step in the temperature profile.

## Hardware
If possible, I'll try to build the wooden box myself, so we will have a bill of materials, maybe some layout or ideas, how to improvise most things without buying all 
sorts of new stuff. I want to reuse as much of all-day-things as possible. 

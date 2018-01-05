---
layout: default
---

Welcome. Here I'll include general introductions to various projects and endeavors, and a link for looking into the details.

## [](#header-2)HackerBoxes and Instructables
I really enjoyed getting into the [hackerboxes](https://hackerboxes.com/) when I get time, and I found that I also really enjoyed making simple how-to tutorials to help myself and anyone else who is interested. I've been publishing them on [Instructables](https://www.instructables.com/member/jumson/) and here are some individual links.

### [](#header-3)Hacker Tracker
[The HackerTracker](http://www.instructables.com/id/Hacker-Tracker-in-Depth/) is a device that melds together a GPS module, SD Card Module, an Arduino Nano and a 3-Axis Compass. 

<img src="https://github.com/jumson/jumson.github.io/blob/master/images/HackerTrackerWater.gif?raw=true" 
               width="300" 
               alt="hackertracker"  
        />


### [](#header-3)Circuit Circus
[Assembling](https://www.instructables.com/id/Circuit-Circus-in-Depth-Tech/) and [Operating](https://www.instructables.com/id/How-to-Operate-the-Transistor-Tester-With-AVR-Micr/) the "Circuit Circus" Circuit and Component Tester. 

<table align="center" >
    <tr>
      <td>
        <img src="https://cdn.instructables.com/F6A/LIUW/J7UQS6DE/F6ALIUWJ7UQS6DE.ANIMATED.MEDIUM.gif" 
               width="300" 
               alt="Assembling"  
        />
      </td>
      <td>
        <img src="https://cdn.instructables.com/F8Y/4YEI/J7GGIZ27/F8Y4YEIJ7GGIZ27.ANIMATED.MEDIUM.gif" 
                width="300" 
               alt="Operating"  
        />
      </td>
    </tr>
 </table>


### [](#header-3)A Technique for Soldering SMD components
As I was experimenting with small electronics, I realized I do not really have all the tools I need. I developed this little technique and some people seemed to appreciate it. 

[How to Solder SMD / SMT Components With a Soldering Iron](http://www.instructables.com/id/How-to-Solder-SMD-SMT-Components-With-a-Soldering-/)

<img src="https://cdn.instructables.com/F92/2GBM/J7UQSB73/F922GBMJ7UQSB73.MEDIUM.jpg" 
               width="300" 
               alt="SMD Components"  
        />

### [](#header-3)Tinning Tips
I made this small tutorial to show a way I was using to tin tips of little twisted wires to help with future soldering. I used a different camera this tmie and the image quality was not as good.

[Easy Tip Tinning Technique](http://www.instructables.com/id/Easy-Tip-Tinning-Technique/)

<img src="https://cdn.instructables.com/FKM/0KYC/J98RGUEZ/FKM0KYCJ98RGUEZ.MEDIUM.jpg" 
               width="300" 
               alt="tip tinning"  
        />

* * *
## [](#header-2)Problem Solving....Projects


### [](#header-3)Sewage...a "no fail" situation
So my sewage goes into a little basin at the lowest point in the house, which is below the sewage line at the street. Then it gets pumped up to the sewage line when it reaches a certain level. The pump is controlled by a mechanical float switch that rises and falls with the sewage level. Sometiems it dow not work....and there is no way to know until it comes out and ruins things. Like, weekends. And floores. And my wife's sense of security.
So I had to fix it. Traditionally, when I get down stairs and find the "situation" I unplug the pump from the "piggyback" switch/plug, and plug it directly into the socket, which turns on the pump.
My idea was to make another piggyback plug/switch that could have an alternative sensor to detect when the first switch did not trigger on, and "bypass" it by switching on power directly to the pump until the level goes down.

So I made a thing, that turned into a much bigger thing than I thought it would.

*   There is the old surge protector that did not work anymore, I converted it into the power switching / logic box. This part controls the power and holds the little ESP8266, reading the other sensor, ad which decides when to close the Solid State Relay. It will also/eventually detect when current is flowing through the main switch for later analysis/learning. I'll need to get some pictures on here. [The code programmed into the ESP8266 is found here](https://github.com/jumson/pumpWatcher/tree/master/ESP8266_Code)
*   Then there is the [eTape sensor from Milone Technologies](https://milonetech.com/). This is a solid state pressure sensor designed to be used in "chemical" environments.
*   I was originally using [Blynk](http://www.blynk.cc/) to get the raw data, do some calculation and convert it to inches, and track the water levels with graphs. I made my own server so that i could try out all the bells and whistles without paying anything.
*   To test it out as a proof of concept, I got a small little pond pump, and with the help of the [NPS Makers Club](http://www.npsfoundation.org/makers-club) and the [NPS RoboDojo's](https://my.nps.edu/web/robodojo) Laser Cutter, I made a contraption to perpetually pump / refill so I could fine tune and look for points of failure. (pictures....sometime. And video)
*   Then I thought, why can't I just make my own server and let the device (now dubbed, the PumpWatcher(c)) send GET requests with encoded/formatted information, where I could make logs? [So I did that](https://github.com/jumson/pumpWatcher/tree/master/Server_Code), making a server that recieves that data, saves the data into a CSV file, and converts/streams it to an HTML table and sending it as a webpage for me to look at. 
*   NOW, I'm working on bypassing BLYNK altogether, mainly because I think I can. I'm using Unity to create an app that interfaces with my pumpWatcher device just the way I want. The current prototype is able to send and recieve HTML to / from my server. 
|<img src="https://github.com/jumson/PumpWatchManager/blob/master/appShotLong.png?raw=true" 
               width="400" 
               alt="app"  
        />|<img src="https://github.com/jumson/PumpWatchManager/blob/master/appShot1.png?raw=true" 
               width="250" 
               alt="tip tinning"  
        />|


### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```

---
author: rahil627
comments: true
date: 2012-05-15 12:12:45+00:00
layout: post
link: https://mind.rathewolf.com/pinkies-up/
slug: pinkies-up
title: Pinkies Up
wordpress_id: 1406
categories:
- Game Design
- Game Development
- Game Ideas
- Games
---

## Game Files


[pinkies-up.zip](https://mind.rathewolf.com/wp-content/uploads/2012/05/pinkies-up.zip)



## Instructions


NOTE: Works for iOS 6, not sure about 7. I'm updating everything right now!

This project is really old, but it still seems to work for me. It's an Xcode project.
1. unzip
2. Open PinkiesUp.xcodeproj
3. Run
4. Pray
5. Play
- to play it on multiple devices: run the game on each device to install it, start the game on each device, on one device press host game, on the other devices press join game, press at least 2 buttons on each side to have a minimum of 2v2, press ready on each device, press start on the host device.

To see a play through, see the video below.



## Video


[http://www.youtube.com/watch?v=JqO_Vyc9a1Q](http://www.youtube.com/watch?v=JqO_Vyc9a1Q) via [http://jonstoked.com/pinkies-up](http://jonstoked.com/pinkies-up)



## Design Statement


As Jon often describes the game to others, “it’s basically flip-cup for iPad”.


[![IMG_8911](https://mind.rathewolf.com/wp-content/uploads/2012/05/IMG_8911-1024x557.jpg)](https://mind.rathewolf.com/wp-content/uploads/2012/05/IMG_8911.jpg)


Two teams race, each team having a quirky physics based character code-named Harold. Each player is assigned one button. Each active player group must press their buttons in sequence to add force to Harold. A button pressed out of sequence causes Harold to physically collapse, stopping him for a moment. First Harold to the finish line, which is at the end of the screen of the last device, wins.



## Intentions


A social extensible-multiplayer iPad game with a simple interface. It’s what Jon and I had been gravitating toward for the previous few months.

We intended to maximize the use of iPad’s features: eleven touches, physics, and networking. Oh the possibilities! A single parallax scrolling background over multiple devices as Harold runs across the screen, UI color palettes and silly sounds for each device.
Personal Contribution
The game is Jon’s idea, which constitutes a large portion of the game design. We collaborated to etch out further game design. I programmed everything except the physics of Harold. Jon also handled visual design.



## Lessons Learned


The greatest problem with development was the lack of consistent playtesting. Consistent playtesting is needed to see progress and priority, but also to maintain motivation. A related problem: we were working remotely. Being physically together is important.

I also underestimated the time it takes to write code for Objective-C, Cocos2d, Box2d, and Game Kit. It was at least five times slower than writing code for my previously used game engine: FlashPunk. I also felt that my networking code was poorly written. It takes time.

The lack of feedback caused motivation to wane, and the work sits on my computer, teasing me. Perhaps I just need to bring it out, playtest it to regain motivation, and finish it.

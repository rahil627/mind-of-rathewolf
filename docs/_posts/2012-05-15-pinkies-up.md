---
id: 1406
title: Pinkies Up
date: 2012-05-15T08:12:45-04:00
author: Rahil
layout: post
guid: http://www.rahilpatel.com/blog/?p=1406
permalink: /pinkies-up
medium_post:
  - 'O:11:"Medium_Post":11:{s:16:"author_image_url";s:74:"https://cdn-images-1.medium.com/fit/c/200/200/1*dmbNkD5D-u45r44go_cf0g.png";s:10:"author_url";s:28:"https://medium.com/@rahil627";s:11:"byline_name";N;s:12:"byline_email";N;s:10:"cross_link";s:2:"no";s:2:"id";s:12:"d27aae075692";s:21:"follower_notification";s:3:"yes";s:7:"license";s:19:"all-rights-reserved";s:14:"publication_id";s:2:"-1";s:6:"status";s:6:"public";s:3:"url";s:52:"https://medium.com/@rahil627/pinkies-up-d27aae075692";}'
categories:
  - Game Design
  - Game Development
  - Game Ideas
  - Games
---
<div id="toc_container" class="toc_transparent have_bullets">
  <p class="toc_title">
  </p>
  
  <ul class="toc_list">
    <li>
      <a href="#game_files">Game Files</a>
    </li>
    <li>
      <a href="#instructions">Instructions</a>
    </li>
    <li>
      <a href="#video">Video</a>
    </li>
    <li>
      <a href="#design_statement">Design Statement</a>
    </li>
    <li>
      <a href="#intentions">Intentions</a>
    </li>
    <li>
      <a href="#lessons_learned">Lessons Learned</a>
    </li>
  </ul>
</div>

## <span id="game_files">Game Files</span>

[pinkies-up.zip](http://www.rahilpatel.com/blog/wp-content/uploads/2012/05/pinkies-up.zip)

## <span id="instructions">Instructions</span>

NOTE: Works for iOS 6, not sure about 7. I&#8217;m updating everything right now!

This project is really old, but it still seems to work for me. It&#8217;s an Xcode project.  
1. unzip  
2. Open PinkiesUp.xcodeproj  
3. Run  
4. Pray  
5. Play  
&#8211; to play it on multiple devices: run the game on each device to install it, start the game on each device, on one device press host game, on the other devices press join game, press at least 2 buttons on each side to have a minimum of 2v2, press ready on each device, press start on the host device.

To see a play through, see the video below.

## <span id="video">Video</span>

[www.youtube.com/watch?v=JqO_Vyc9a1Q](http://www.youtube.com/watch?v=JqO_Vyc9a1Q) via [jonstoked.com/pinkies-up](http://jonstoked.com/pinkies-up)

## <span id="design_statement">Design Statement</span>

As Jon often describes the game to others, “it’s basically flip-cup for iPad”.

<p style="text-align: center;">
  <a href="http://www.rahilpatel.com/blog/wp-content/uploads/2012/05/IMG_8911.jpg"><img class=" wp-image-1411 aligncenter" src="http://www.rahilpatel.com/blog/wp-content/uploads/2012/05/IMG_8911-1024x557.jpg" alt="IMG_8911" width="496" height="270" srcset="http://rahilpatel.com/blog/wp-content/uploads/2012/05/IMG_8911-1024x557.jpg 1024w, http://rahilpatel.com/blog/wp-content/uploads/2012/05/IMG_8911-300x163.jpg 300w" sizes="(max-width: 496px) 100vw, 496px" /></a>
</p>

Two teams race, each team having a quirky physics based character code-named Harold. Each player is assigned one button. Each active player group must press their buttons in sequence to add force to Harold. A button pressed out of sequence causes Harold to physically collapse, stopping him for a moment. First Harold to the finish line, which is at the end of the screen of the last device, wins.

## <span id="intentions">Intentions</span>

A social extensible-multiplayer iPad game with a simple interface. It’s what Jon and I had been gravitating toward for the previous few months.

We intended to maximize the use of iPad’s features: eleven touches, physics, and networking. Oh the possibilities! A single parallax scrolling background over multiple devices as Harold runs across the screen, UI color palettes and silly sounds for each device.  
Personal Contribution  
The game is Jon’s idea, which constitutes a large portion of the game design. We collaborated to etch out further game design. I programmed everything except the physics of Harold. Jon also handled visual design.

## <span id="lessons_learned">Lessons Learned</span>

The greatest problem with development was the lack of consistent playtesting. Consistent playtesting is needed to see progress and priority, but also to maintain motivation. A related problem: we were working remotely. Being physically together is important.

I also underestimated the time it takes to write code for Objective-C, Cocos2d, Box2d, and Game Kit. It was at least five times slower than writing code for my previously used game engine: FlashPunk. I also felt that my networking code was poorly written. It takes time.

The lack of feedback caused motivation to wane, and the work sits on my computer, teasing me. Perhaps I just need to bring it out, playtest it to regain motivation, and finish it.
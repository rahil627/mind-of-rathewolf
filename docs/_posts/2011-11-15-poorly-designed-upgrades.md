---
id: 322
title: Poorly Designed Upgrades
date: 2011-11-15T05:21:55-05:00
author: Rahil
layout: post
guid: http://www.rahilpatel.com/blog/?p=322
permalink: /poorly-designed-upgrades
medium_post:
  - 'O:11:"Medium_Post":11:{s:16:"author_image_url";s:74:"https://cdn-images-1.medium.com/fit/c/200/200/1*dmbNkD5D-u45r44go_cf0g.png";s:10:"author_url";s:28:"https://medium.com/@rahil627";s:11:"byline_name";N;s:12:"byline_email";N;s:10:"cross_link";s:2:"no";s:2:"id";s:12:"f47833bbea43";s:21:"follower_notification";s:3:"yes";s:7:"license";s:19:"all-rights-reserved";s:14:"publication_id";s:2:"-1";s:6:"status";s:6:"public";s:3:"url";s:66:"https://medium.com/@rahil627/poorly-designed-upgrades-f47833bbea43";}'
categories:
  - Game Development
  - Games
tags:
  - actionscript game
  - art game
  - Connected-component labeling
  - experimental gameplay project
  - expiremental game
  - expiremental gameplay
  - flashpunk
  - homing missile
  - independent game
  - limit of a function
  - "shoot 'em up"
---
<div id="toc_container" class="toc_transparent have_bullets">
  <p class="toc_title">
  </p>
  
  <ul class="toc_list">
    <li>
      <a href="#play_the_game">Play the game</a>
    </li>
    <li>
      <a href="#instructions">Instructions</a><ul>
        <li>
          <a href="#goal">Goal</a>
        </li>
        <li>
          <a href="#controls">Controls</a>
        </li>
      </ul>
    </li>
  </ul>
</div>

## <span id="play_the_game"><a href="http://www.rahilpatel.com/poorly_designed_upgrades.html">Play the game</a></span>

&nbsp;  
This game is my submission for this month&#8217;s Experimental Gameplay Project competition. The theme is [upgrade](http://experimentalgameplay.com/blog/2011/11/upgrade-in-november-2011/).

I used ActionScript, [FlashDevelop](http://www.flashdevelop.org/wikidocs/index.php?title=Main_Page), and [FlashPunk](http://flashpunk.net/ "FlashPunk") again.

Last time I promised EGP and myself the game would be experimental. It&#8217;s certainly more experimental than my previous games, but not quite enough. The ideas are there but I cheated myself and conveyed them on a shoot &#8217;em up genre game. Never again!

## <span id="instructions">Instructions</span>

### <span id="goal">Goal</span>

Experiment with different upgrade setups to prevent enemies from reaching the bottom of the screen in various challenges.

### <span id="controls">Controls</span>

wasd or arrow keys to move  
space bar to fire  
f to autofire (on by default)

while in sandbox screen:  
&#8211; and + to decrease or increase enemy HP (can hold the key down)  
[ and ] to decrease or increase enemy spawn rate (can hold the key down)  
u to enter the upgrade screen  
1, 2, 3 to start a challenge

while in upgrade screen:  
left click on the canvas to draw the current upgrade. This works similar to the pencil tool in a graphics editing program  
*you can only draw on the ship or a neighboring pixel of the current upgrade  
*you cannot overlap other upgrades  
*protip, each [4-connected neighborhood](http://en.wikipedia.org/wiki/Von_Neumann_neighborhood) is treated as a separate gun  
escape to go back to sandbox screen

while in challenge screen:  
escape to go back to sandbox screen

[Oooone mooore thing](http://www.youtube.com/watch?v=AcmpjIfb0OQ). The boosters and challenges are actually poorly designed. Really, it&#8217;s bad.
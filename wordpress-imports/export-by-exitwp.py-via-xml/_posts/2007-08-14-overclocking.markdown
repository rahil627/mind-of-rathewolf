---
author: rahil627
comments: true
date: 2007-08-14 18:49:24+00:00
layout: post
link: http://rahilpatel.com/blog/overclocking/
slug: overclocking
title: Overclocking a MSI P6N SLI Platinum with a Core 2 Duo E6420
wordpress_id: 923
categories:
- Specific Guides
---

These are my overclocking results with a MSI P6N SLI Platinum with a Core 2 Duo E6420 (and a XIGMATEK HDT-S1283 120mm Rifle CPU Cooler).

how to OC:
increment FSB. if that doesn't work, increment voltage and try again. keep FSB 1:1 to MEM	
in my case, FSB/2 = MEM
when done, prime95 blend test, prime95 small FFTs, intel burn test (very intense!)

BIOS settings:
1) cpu feature
execute bit support	disabled
set limit CPUID		disabled
c1e			disabled	press f4 in this menu

2) chipset feature
HPET			disabled

3) cell menu
D.O.T.			disabled
EIST			disabled
system clock		manual		
	voltages	(see below)
advanced DRAM...	4-4-4-12tRAS-auto tRC-2T @ auto voltage (g.skills were auto'd at 2-3-3-8 @ 375mhz [although i put 4-3-3-8-auto(17)-auto(2t)-auto(1.9)?])
spread spectrum 	disable CPU
CPU ratio				8

results:
before wall
voltages
	FSB	1500
	MEM	750
	CPU	0.000 (stock)
	NB	1.3v (+.05)
	SB	1.5v (stock)
	FSB VTT	0% (stock)

after wall
advanced DRAM...	auto
voltages
	FSB	1700
	MEM	850
	CPU	+.750
	NB	+.2	1.45v
	SB	stock
	FSB VTT	4%

how to flash:
C:
cd\flash
A7350NMS.150
Afud408.exe /P /B /C

GPU				temp after 2 mins of ATI tool artifact test
default		513/792		77 (60 idle)
OC	600/900
		625/1000	80c
		650/1000	83c
		675/1000	[fail?]

1 hour ati tool artifact is a good test

using ATI tool
	find max core - freezes at 669
	find max mem - freezes at 1156

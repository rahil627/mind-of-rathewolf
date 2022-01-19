---
author: rahil627
comments: true
date: 2012-03-13 21:17:04+00:00
layout: post
link: http://rahilpatel.com/blog/replacing-a-hard-disk-drive-with-mac-os-x-and-boot-camp/
slug: replacing-a-hard-disk-drive-with-mac-os-x-and-boot-camp
title: Replacing a Hard Disk Drive with Mac OS X and Boot Camp
wordpress_id: 504
categories:
- Specific Guides
tags:
- A1278
- Samsung 830
---

I wanted to install Unity to create a 3D game I thought of for EGP but I can't because I don't have enough space on my Boot Camp partition! The feeling of being blocked from the things you want to do is awful.

I have MacBook Pro (13" early 2011, Model Number: A1278) with 196GB allocated to the Mac OS X 10.7 (Lion) partition and 42GB allocated to the Windows 7 partition. Bad idea, as I've found I use Windows 95% of the time now. After a searching a little on Google it seems there is no recommended (reliable and popular) way to re-size the partition, instead I must re-install the Boot Camp partition.

While researching I thought this would be a good time to finally upgrade to a solid-state drive and do everything at once.

After little research I've decided to choose the Samsung 830 over the Crucial m4 and Intel 510 (all 256GB versions) based on the few MacRumors threads I read. I calculated my Windows install (applications, but no media) takes the full 37.9GB with 4GB virtual memory, and my Mac OS X install takes around 80GB (or was it 60?*). I don't want to run into this problem of low space again, so I decided on the larger 256GB drives. From what I gather the Samsung 830 controller is newer/better, compatible with Mac OS X, and can update the firmware from within Boot Camp. Normally I'd choose Intel so I don't have to worry about reliability, but I did not see any price or performance competitive options from Intel. Besides, I loves me some Samsung.

Upon reading the current [Best SSDs For The Money article by Tom's Hardware](http://www.tomshardware.com/reviews/ssd-review-benchmark,3115.html) I stumbled upon a [neat solution](http://www.tomshardware.com/reviews/ssd-laptop-upgrade-optical-bay,3102.html) which allows you to install a second hard disk drive in the optical bay. MacRumor users found a [cheap alternative form Amazon](http://www.amazon.com/Drive-Unibody-MacBook-SuperDrive-Replacement/dp/B0058AH2US). I'm thinking about ordering one and placing my hard disk drive in there.

Just thinking ahead of a good video editing system, I could store the original footage on the hard disk (HFS+) and edit on the SSD. My current external hard drive uses NTFS and I use a NTFS driver (NTFS-3G or Paragon, I don't remember) to read it from Mac OS X. I remembered reading something about the exFAT file system. That sounded like the perfect file system for external drives, but after a little research it wasn't. I'll have to do some more reading.

I'll update this post early next month with my results. It might even be separated into two posts, resizing and buying a SSD.

UPDATE:
Success. I was able to clone my Mac and Windows installations. For the most part I followed [this well-written guide](http://johnbeales.com/20110330/transferring-osx-bootcamp-to-new-hard-drive/). It was an overall smooth process.

Here's a tiny list of hurdles I went through:

Before I began I uninstalled NTFS for Mac driver. I'm not sure if this was necessary.



<blockquote>2. Follow the wizard to create a BootCamp partition. This partition does not need to be the same size as your old Boot Camp partition. When Boot Camp Assistant asks you to insert a Windows install disk quit Boot Camp Assistant. Your partition is created.</blockquote>


During this step, when I clicked install in WinClone, it would ask for a Windows disk without creating a partition. I had to insert my Windows 7 disk for it to partition. After that, my PC restarted and booted from the Windows CD. From here I selected the Boot Camp partition and selected format (after clicking advanced options). I don't think this did anything though. I then quit the setup, restarted the PC, held options to boot into Mac, and continued to recover the image from WinClone.


<blockquote>8. Turn on your Mac holding down the Option key on the keyboard. You should see your Boot Camp partition as a boot option, (it’s probably labeled “Windows”). Select it to boot into Windows.</blockquote>



The first time I tried to boot into Windows the PC displayed a blank black screen with a Windows mouse cursor. I had to hard power off. The next boot worked perfectly.

After I was done I was able to use Samsung Magician software to update the solid-state drive's firmware within Boot Camp. I used the Windows update option, as opposed to creating a bootable CD or USB.

I also checked to see if disk defragmenter was turned off in Windows as it is not needed for solid-state drives.

Finally, Mac OS X feels as nimble as Window 7. As I had guessed, the hard drive was the bottleneck. The good old Core 2 Duo lives another day. Also, it's nice not to have to move files around to compensate for the lack of space. So worth the time.

Other Resources:
[http://guides.macrumors.com/Extend/Resize_Boot_Camp_Partition](http://guides.macrumors.com/Extend/Resize_Boot_Camp_Partition)
[http://forums.macrumors.com/showthread.php?t=1056464](http://forums.macrumors.com/showthread.php?t=1056464)
[http://forums.macrumors.com/showthread.php?t=1177020&page=19](http://forums.macrumors.com/showthread.php?t=1177020&page=19)
[http://www.tomshardware.com/reviews/ssd-review-benchmark,3115-6.html](http://www.tomshardware.com/reviews/ssd-review-benchmark,3115-6.html)

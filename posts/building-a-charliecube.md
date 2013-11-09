---
title: 'Building a charliecube'
date: '2013-10-24'
description:
tags: [charliecube, solder, arduino, hardware, project, led, cube]
---

I first learned about Charliecube when I visited [Metrix]. Seeing the color LEDs going through
different patterns was very mesmerizing, and I committed myself to building one. It would be my
first hardware project, and apart from many, many tedious soldering, the project itself isn't very
difficult. Soldering 320 joints consistently and efficiently? Challenge accepted!

Fortunately, the build steps have already been [documented][aglick], so all I need to do is follow
his build steps. I thought about extending to 5x5 cube, but I'd have to redesign the wiring, arduino
programming, and get a board that has 25 pins (i.e. not Uno), I decided to improvise after I got the
basics down.

### Build of Materials
- 64 common cathode color LEDs. (I sourced 100 pcs for $12 on [eBay][ebay-led])
- Steel wires (I bought a spool of 20 AWG at [Lowes][lowes-wire], but I would recommend 24 or 26 AWG)
- Arduino (I used an Uno, but any will do)
- Solder
- Plastic or wood for the base

### Tools and Equipment
- Soldering iron
- Laser cutter (optional)


Throughout the building exercise, I wanted everything done consistently, and there were some
challenges in doing so..

### Step-by-step
#### Step 1: Measure and straighten the wire
I wanted my LEDs to be 36 mm apart, and that same distant apart from the base, I calculated I needed
the steel wires to be at least 144 mm long. Giving myself some room for error, I snipped them at
180 mm. Now comes the hard part - straightening them out. The 20-gauge galvanized steel wire was too
thick to straighten out just by [tensioning][yt-1] it, or [twisting][yt-2] it. Sooo, reluctantly, 
I manually straightened them out with pliers, and to make it all less of a drag, I entertained
myself with a few episodes of Friends while doing it, so I wouldn't mind it so much.

#### Step 2: Bending the LED leads
Because this is a RGB LED, there are [four leads][led] - red, green, blue, and common cathode. I
identified the flat edge, and faced that side up. With a point of reference, I bent the leads
[like so][bent-led]. But honestly, any way will do - just do it consistently. Again, Friends helped
me through this difficult time.

#### Step 3: Soldering
This is arguably the most tedious part. 64 LEDs, soldered onto 64 wires. Each column of LEDs will
have 16 joints. 16 of those columns, you get 256 joints to solder. They all have to be equidistant
from each other, as well as from the steel wire. Marking the wires at 36 mm apart and using helper
hands just ain't gonna cut the accuracy and repeatability I wanted to achieve. I'll spare you the
details, but I've tried using Pringles can, cardboard cutout, and steel plates before coming to a
'workstation', if you will, that I designed and laser cut.

![assembled][struct-assembled]
![disassembled][struct-exploded]

In its simplicity, it is a rectangular box with detachable walls. The top and bottom are cut with
holes to fit a LED and wires. After four solders, one unit of the sides is taken off, and another
round of soldering can commence.

#### Step 4: Snip off excess wires
After a round of hard work comes the easy part - snip off all the excess leads and wires!

![unsnipped][unsnipped]
![snipped][snipped]

#### Step 5: Make a base for all those LEDs
The [build instructions][aglick] I followed used a breadboard. I wanted something more permanent and
more visually appealing. So I laser cut a wooden box:

![wood-box-exploded]
![wood-box]
![wood-box-leds]

(Though it wasn't long after I decided to go with acrylic.)

#### Step 6: Wiring all the spires together
I measured out the distance the spires are apart from the base, then I used hot glue to fix them in
place. After that, I wired the spires together, according to the [build instructions][aglick]

![hot-glued-base]
![hot-glue-closeup]
![wiring-1]
![wiring-2]
Piping hot mess!

#### Step 7: The moment of truth
Up until this point, I had no idea if I did all the solderings correctly. I eagerly hooked all the
wires up to the arduno, and voîla!

![demo]
\(That's Emily in the background. Ross's ex-wife)

#### Step 8: Clean up
Putting the icing on the cake, the bow on the present, I made a clear arclyic case for it

![final-1]
![final-2]

And we're done!

[metrix]: http://metrixcreatespace.com/ "A hackerspace in Captiol Hill"
[aglick]: http://aglick.com/charliecube.html
[ebay-led]: http://www.ebay.com/itm/-/281111473484
[lowes-wire]: http://www.lowes.com/pd_62934-37672-122040_0
[asciiflow]: http://www.asciiflow.com/
[yt-1]: http://www.youtube.com/watch?v=kReKXUwFNmE "How to Straighten Wire"
[yt-2]: http://www.youtube.com/watch?v=l4oUU2uMD4Y "How to Straighten Metal Wires"
[led]: http://aglick.com/charliecube/howtobuild/vlcsnap-2011-12-27-16h05m36s2.png
[bent-led]: http://aglick.com/charliecube/howtobuild/vlcsnap-2011-12-27-16h07m21s74.png
[struct-assembled]:  https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/mLkXJ5kKtx/2013-11-08%2023.05.31.jpg
[struct-exploded]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/xqeoZ5Q6VN/2013-11-08%2023.04.48.jpg
[unsnipped]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/rtdFdey9oD/2013-10-21%2001.13.31-2.jpg
[snipped]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/J3kG49Q2Px/2013-10-27%2020.17.17.jpg
[wood-box-exploded]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/u2InfkPtjw/2013-10-22%2023.40.33.jpg
[wood-box]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/KIcxETH8KI/2013-10-22%2023.41.28.jpg
[wood-box-leds]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/6qgAhW9P05/2013-10-22%2023.49.58.jpg
[hot-glued-base]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/E_Yolbs_R7/2013-10-24%2019.23.33.jpg
[hot-glue-closeup]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/K5Xzn_MkrC/2013-10-24%2020.56.14.jpg
[wiring-1]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/FZzwzP-O4P/2013-10-24%2021.41.18.jpg
[wiring-2]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/bc86kKd8v1/2013-10-24%2022.15.39.jpg
[demo]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/k3amE8Dv4v/2013-10-25%2020.25.30.jpg
[final-1]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/Y6oVNC4WRV/2013-10-29%2001.07.17.jpg
[final-2]: https://dl.dropboxusercontent.com/sh/2fnroo8xhxgsj4h/LCwIWVd7BB/2013-10-29%2001.08.10.jpg

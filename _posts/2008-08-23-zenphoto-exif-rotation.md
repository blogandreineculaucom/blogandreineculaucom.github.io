---
title: ZenPhoto EXIF Rotation
author: Andrei
layout: post
categories:
  - Information Technology
  - Solution
tags:
  - php
---
I'm using [ZenPhoto][1] as a Media Gallery web interface, but it wasn't able to do automatic rotation by reading the EXIF information. I expected that to be public with version 1.2, but no.

After a bit of [searching][2] and thinking and improving, I've ended up updating some core files, and it's now supposed to work flawlessly in this regard. The only thing is that the EXIF information gets read each time from the file, instead of reading it from the database (need to work on that). The changes also support image fliping.



You can download [the patch][3] and just extract that and overwrite the old ZenPhoto files.

PS: All modifications are between "EXIF Rotation" comments

 [1]: http://www.zenphoto.org
 [2]: http://www.zenphoto.org/support/topic.php?id=2559
 [3]: http://files.andreineculau.com/projects/zenphoto/zp-core.zip
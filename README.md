# Not Pron

## Table Of Contents
* [Summary](#summary "Summary Section")
* [Starting The Riddle](#starting-the-riddle "Starting Section")
* [Level 1](#level-1 "Level 1 Section")
* [Level 2](#level-2 "Level 2 Section")
* [Level 3](#level-3 "Level 3 Section")
* [Level 4](#level-4 "Level 4 Section")
* [Level 5](#level-5 "Level 5 Section")
* [Level 6](#level-6 "Level 6 Section")
* [Level 7](#level-7 "Level 7 Section")
* [Level 8](#level-8 "Level 8 Section")
* [Level 9](#level-9 "Level 9 Section")
* [Level 10](#level-10 "Level 10 Section")
* [Hints](#hints "Hints Section")
---

## Summary
Notes relating to the individual levels in the not pron internet riddle created by CEO of [Supra Games](https://deathball.net/supragames/ "Supra Games Wesite") and game developer [David Munnich](https://twitter.com/DavidM1337 "David Munnich Twitter").

Read more about this riddle at the [not pron wikipedia](https://en.wikipedia.org/wiki/Notpron "Not Pron Wiki") page.

---

## Starting The Riddle
The game can be accessed by visiting the website [here](http://www.deathball.net/notpron "Not Pron Website") and clicking the start button which redirects to the [first level](http://notpron.org/notpron/levelone.htm "Not Pron Level 1")

---

## Level 1

Level 1 is pretty straight forward. Just an image with an [html area map](https://www.w3schools.com/tags/tag_area.asp "W3 Info On Area Tag") over the door which when clicked on leads to level 2. One interesting thing to note though is that in the HTML source code there is a comment directed at users all the way at the bottom. This leads me to believe further levels will require reading source code. The comment reads:

```html
<!--good idea, but the source is one screen ahead of this one-->
```

### [Back To Top](#not-pron "Top Of Page")
---

## Level 2

Level 2 contains another image of a door with another area map (on the door knob) that when hovered over triggers the following JavaScript alert...

> The door is closed. Trick it or reach LEVEL3 in a different way! (Address? Where is the hand pointing?)

The hand reffered to in the alert is pointing up at the URL and the alert mentions the word address as a hint.

Logically the next step is URL address changing.

* Going from http://notpron.org/notpron/not/level2.htm
* To http://notpron.org/notpron/not/level3.htm
* Redirects us to http://www.deathball.net/notpron/false/movetotheothersite.php

Some things to note about this level are that the image area map is hidden away within a font tag as seen below. This is also the first time hints have been presented and I will link them within the [hints section](#hints "Hints Section") of this document.

```html
<font color="#FFFFFF">
    <map name="no">
      <area shape="rect" coords="161,350,189,400" onmouseover="returnTruth();return true;" href="../false">
    </map>
    <br>
    <a href="http://deathball.net/notpron/hints.htm" target="_blank"><font size="5" face="Arial">Hints
    and Rules</font></a><br>
    <br>
    <br>
    <br>
    <br>
    <br>
</font>
```

### [Back To Top](#not-pron "Top Of Page")

---

## Level 3

Level 3 contains a GIF that occasionaly flashes the words:

> Stop being so negative

And a comment in the HTML source code that reads:

```html
<!-- read the whole url -->
```

So changing the negative value in the URL into a positive should lead us to level 4.

* Negative URL - http://www.deathball.net/notpron/false/movetotheothersite.php
* Positive URL - http://www.deathball.net/notpron/true/movetotheothersite.php

### [Back To Top](#not-pron "Top Of Page")

---

## Level 4

Level 4 presents us again with another image with an area map within. It can be found on the object in front of the two pillows. When this object is clicked on we recieve a JavaScript alert that reads:

> Password Hint: LightThisPlaceNow

After which a login prompt is shown which asks for our username and password.

These credentials can be found in the photo underneath the light on the nightstand.

Somewhat obscured there are two lines of morse code that read:

> ...- --- --- -.. --- --- -- .- --. .. -.-.

Taking that morse code and plugging it into [CyberChef](https://cyberchef.org/ "Cryptography Tool") reveals the following message:

> voodoo magic

Plugging these values into the login form redirects us to Level 5.

* Login: voodoo
* Password: magic

### [Back To Top](#not-pron "Top Of Page")

---

## Level 5

Level 5 includes an image of a CD case and a remote control on a table with some text at the bottom that reads:

> Eyes like an angel smiles like a devil

The name of the band on the CD case is [Big Bad Voodoo Daddy](https://en.wikipedia.org/wiki/Big_Bad_Voodoo_Daddy "Band Wikipedia")

The image area map can be found over the power button on the remote control.

Again this area map on click produces another login form, the credentials of which can be found by performing a simple google search of those lyrics and using the song name ([simple songs](https://www.youtube.com/watch?v=SCgdCj2myRU "Song On YouTube")) on the form.

* Username: simple
* Password: songs

### [Back To Top](#not-pron "Top Of Page")

---

## Level 6

Level 6 contains an image of pipes with an area map in the lower left corner. Again clicking on this area produces an alert followed by a login form.

The alert reads:

> Password Hint: anagram

So now all we have to do is find the password.

Scrolling down the page you can find the word "up". Hinting at some hidden information above this location. There are 2 ways you can find this...

1. Highlight the page revealing the black text.

2. Read the HTML code realizing there is a second HTML page being loaded in via the [iframe](https://www.w3schools.com/tags/tag_iframe.asp "W3 Iframe Information") tag. This document is trying to obscure the text by setting the body text color to all black. Within this document is a paragraph tag with the hidden information.

The hidden information reads:

> 108 105 108 107 101 122 111 110

These numbers all lay in the range (97-122) of lowercase [ASCII](https://en.wikipedia.org/wiki/ASCII "ASCII Wikipedea") characters.

![ASCII Chart](./Assets/ascii-table.png "ASCII Chart")

Another way to tell that these are ASCII characters is by reading the hidden comment in the HTML source code all the way at the bottom which reads:

```html
<!--ascii is an alternative-->
```

Once translated, these codes reveal the word:

> lilkezon

Rearranged this creates the word:

> killzone

Entering this into our login form redirects us to level 7.

**CREDENTIALS -**
* Login: kill
* Password: zone

### [Back To Top](#not-pron "Top Of Page")

---

## Level 7

Ok, so this level was pretty difficult. It starts with an image of a crumpled twix wrapper in front of a mirror. There is no area map within the image and no text on the page to guide you. There is a new note in the left corner though which reads the following:

> -From now on almost all levels require you to have a look at the source code.

In the HTML source code we can find the following comments:

```html
<!--times have changed in deutschland -->
...
<!--what candy wrapper is it?-->
```

If we take a look at the hint for this level it says:

> Carefully read the URL. It's telling you what to do.

Examining the URL for this level something stands out. The strange names for the directory and file.

> /sdrakcab/tieman.htm

This is just backwards for:

> /backwards/nameit.htm

So at first I thought this level would be easy and the solution would be:

> /sdrakcab/xiwt.htm

But this led to a dead end, so I tried every possible combination of reversing directory and file names I can think of and while some led to 404 errors, others were more interesting. Some of these combinations produced unique messages. These are those links and their messages starting from the Level 7 landing page.

1. http://www.deathball.net/notpron/sdrawkcab/tieman.htm
    > Starting Point

2. http://www.deathball.net/notpron/sdrawkcab/nameit.htm
    > No, name what you see on the pic, go back!

3. http://www.deathball.net/notpron/sdrawkcab/xiwt.htm
    > too new

4. http://www.deathball.net/notpron/sdrawkcab/twix.htm
    > wenoot

5. http://www.deathball.net/notpron/backwards/twix.htm
    > i'd like to have it backwards tho

6. http://www.deathball.net/notpron/backwards/xiwt.htm
    > no, i want backwards backwards

7. http://www.deathball.net/notpron/backwards/tieman.htm
    > no, just name it

8. http://www.deathball.net/notpron/backwards/nameit.htm
    > do it......name IT

At this point I started to wonder what I was doing wrong and decided to rethink this whole process. These messages continue to tell me to "just name it" then there was the weird hint in the HTML source code.

```html
<!--times have changed in deutschland-->
```

Then it hit me, maybe Twix has a different name in Germany.

Which led me to the [Twix Wikipedia](https://en.wikipedia.org/wiki/Twix "Twix Wiki") page.

Apparently Twix used to be called Raider.

Which led to me to the 9th interesting message:

9. http://www.deathball.net/notpron/sdrawkcab/raider.htm
    * dnuorayawrehto

> Backwards for otherwayaround

And finally the way to level 8:

> http://www.deathball.net/notpron/sdrawkcab/rediar.htm

### [Back To Top](#not-pron "Top Of Page")

---

## Level 8

Level 8 contains another image with an area map. This time it's right over the soundhole of the guitar. When clicked on, a JavaScript alert pops up giving us the first hint followed by a login form. The alert reads:

> Password Hint: mom, he formatted my second song

Below the image there is text that reads:

> JAY should PACK his stuff

Interesting things to note on this level are that so far every page has been loading up an mp3 file stored at:

> http://www.deathball.net/notpron/stuff/mus1.mp3

But this time in the HTML source code we can see an attempt at loading a second mp3 stored at:

> http://www.deathball.net/notpron/stuff/mus2.mp3

Suspiciously, the [audio tag](https://www.w3schools.com/TAGS/tag_audio.asp "W3 Docs For Audio Tag") for this second mp3 is broken causing it to never be loaded into the document.

```html
  <audio src="../stuff/mus1.mp3" autoplay loop></audio>
  <au dio src="../stuff/mus2.mp3">
```

Theres also an interesting comment in the HTML:

```html
<!-- water became wine -->
```

Following the link to the second mp3 we get the following error message:

> no video with supported format and mime type found

If we compare both files with "view source" it becomes clear that mus2.mp3 is not an mp3 it's an image. There are clear strings of text referencing Adobe Photshop.

Downloading this file reveals it is a JPEG of the [level 9 login credentials.](./Level-8-Assets/mus2mp3.jpeg "Image Of Login Credentials")

* Login: inverted
* Password: tenthlevel

Additional Information - Running [exiftool](https://en.wikipedia.org/wiki/ExifTool "Exiftool Wikipedia Page") on the downloaded JPEG reveals a ton of metadata. One of which might be a link to another level. You can find a copy in the [metadata.txt](./Level-8-Assets/metadata.txt) file within the Level-8-Assets folder.

### [Back To Top](#not-pron "Top Of Page")

---

## Level 9

Level 9 is under the /notpron/luv2music directory in a file called paulisdead.htm and the document title for this page (name on the tab) is "revolution".

The page contains another JPEG with an image map over the number 9 in the upper left corner. Clicking this area reveals this levels hint followed by the login prompt. The hint reads:

> Password Hint: colorful

Underneath the image we can find the following text:

> tears under john's mad notes of pain
>
> did he answer demon's call now

Looking at the directory name, file name, page title, and text under the image it's clear these are all Beatles references. Even the level number 9 is a reference to the notorious Beatles song "Revolution 9".

But Paul is still alive and changing the URL from:

> http://www.deathball.net/notpron/luv2music/paulisdead.htm

To:

> http://www.deathball.net/notpron/luv2music/paulisalive.htm

Gives us an easter egg that reads:

> yeah i know he is alive, but don't waste your time with the Mc!

And if you Google "[Paul is dead](https://en.wikipedia.org/wiki/Paul_is_dead "Paul Is Dead Wikipedia")" you'll get articles about the infamous conspiracy theory that Paul McCartney died and was replaced by a look alike.

This level is also the first page so far to contain zero comments in the HTML source code.

Instead you'll find something interesting in the repeated use of the [span](https://www.w3schools.com/tags/tag_span.asp "W3 Docs On Span Tag") tags. They wrap around single letters and serve no purpose. They're not being used by a CSS or JavaScript file. They're just suspiciously there.

```html
<span class="not">t</span>ears <span class="not">u</span>nde<span class="not">r</span> joh<span class="not">n</span>'s <span class="not">m</span>ad not<span class="not">e</span>s <span class="not">o</span>f pai<span class="not">n</span>
<br><span class="not">d</span>id h<span class="not">e</span> <span class="not">a</span>nswer <span class="not">d</span>e<span class="not">m</span>on's c<span class="not">a</span>ll <span class="not">n</span>ow
```

Taking every letter within the span tags reveals the following two lines:

> turn me on
>
> dead man

Which happen to be the login credentials for level 10. Additionally these are the lyrics that can be heard when listening to Revolution 9 backwards, according the the "Paul is dead" conspiracy theorists.

* Username: turnmeon
* Password: deadman

### [Back To Top](#not-pron "Top Of Page")

---

## Level 10

Level 10 contains an image of a gold ring on top of a book. The ring has an area map around it. When the ring is clicked on we receive a JavaScript alert with a password hint, followed by a login form.

The password hint reads:

> Password Hint: operator woman said it

The URL for this page is:

> http://www.deathball.net/notpron/wrong/roawr.htm

The document title is:

> he was impatient

Examining the HTML source code reveals some interesting information. An MP3 file we haven't seen yet called mus3.mp3, and two comments.

```html
<audio src="../stuff/mus3.mp3" autoplay loop></audio>
...
<!--quick quick, don't let me wait-->
...
<!--%SystemRoot%\System32\sndrec32.exe can capture "what u hear"-->
```

The second HTML comment tells us to record what we hear. Instead we can just download that MP3 file we found ([mus3.mp3](http://www.deathball.net/notpron/stuff/mus3.mp3 "mus3.mp3 location")).

Now at this point, I knew that there was hidden data within the audio file, but to be honest I had no idea how to get it or what I was looking for. The audio file just sounded like incomprehensible white noise. So I looked up some YouTube videos on how to hide/find data in audio files.

To start I needed a program for working with audio files and ended up choosing [Audacity](https://www.audacityteam.org/ "Audacity Website").

Once I loaded the mus3.mp3 file into Audacity I checked if the info was hidden within the [spectogram](https://en.wikipedia.org/wiki/Spectrogram "Spectogram Wikipedia").

![mus3.mp3 spectograph](./Level-10-Assets/mus3-mp3-spectograph.png "mus3.mp3 Spectograph")

But there was nothing there. Then I remembered the HTML comment and the page title of the level.

> Document Title: He was impatient
>
> HTML Comment: quick quick, don't let me wait

After that I sped up the audio and started to notice that the once incomprehensible audio started to sound more and more like something real.

Then I reversed the audio and in a deep voice the words "Dark Times" could be heard.

It becomes clearer too once the pitch is raised.

Below are the steps needed to hear the words hidden within the audio file. Along with links to the audio files I saved at the different phases.

1. Effect -> Pitch and Tempo -> Change Speed -> Speed Multiplier (5.000)
    * Sounds like [this](./Level-10-Assets/mus3-sped-up.mp3 "mus3.mp3 Sped Up")

2. Effect -> Pitch and Tempo -> Reversed
    * Sounds like [this](./Level-10-Assets/mus3-sped-and-reversed.mp3 "mus3.mp3 Sped Up and Reversed")

3. Effect -> Pitch and Tempo -> Change Pitch -> Percent Change (75.000)
    * Sounds like [this](./Level-10-Assets/mus3-sped-reversed-and-pitch-raised.mp3 "mus3.mp3 Sped, Reversed, Pitch Raised")

This leads us to the following login credentials:
> Username: dark
>
> Password: times

Additional Notes -

The [previous level](#level-9 "Level 9") was about a song played backwards revealing a hidden message. This was foreshadowing the reversal of the mus.mp3 file in level 10.

The word "**roawr**" in the roawr.htm file is an anagram of "arrow".

Switching the /right directory to /wrong reveals an easter egg.

* http://www.deathball.net/notpron/right/roawr.htm
    * its not that easy, fool

### [Back To Top](#not-pron "Top Of Page")

---

## Level 11



---

### [Back To Top](#not-pron "Top Of Page")

## Hints

### [Level 1](#level-1 "Level 1 Notes")

* If this level is too hard, give up and go away. No don't!
Where do you open a door? Click that part in the picture!

### [Level 2](#level-2 "Level 2 Notes")

* The popup is telling you to trick it. Maybe use something else than your mouse to get rid of it, so you get the link that it is covering!

### [Level 3](#level-3 "Level 3 Notes")

* Stop being negative, will ya? Stop trying to click something, there is nothing! Read the address carefully. What can you "turn on"?

### [Level 4](#level-4 "Level 4 Notes")

* Is anything dark here? Light it maybe? How? Got programs for that? Do you see something now? What sort of code could it be?

### [Level 5](#level-5 "Level 5 Notes")

* Carefully read the URL. There are at least 2 things that can help you.
Found the right thing in google? Stop thinking too difficult, just need 2 words for Username/Password!

### [Level 6](#level-6 "Level 6 Notes")

* Make up your mind about the "source code"!
Ever heard of ASCII Code?

### [Level 7](#level-7 "Level 7 Notes")

* Carefully read the URL. It's telling you what to do.

### [Level 8](#level-8 "Level 8 Notes")

* Second song? Which one could it be?
Who (or what) is Jay Pack? Say it loud!

### [Level 9 - 81](#level-9 "Level 9 Notes")

* Now you are on your own. No more help!
But keep in mind that all levels are different from each other!
It's easy to find cheats on the internet, but from the moment of your first cheating on, the whole fun is gone, stay strong!
Don't brag with your level progress, it makes no sense.

---

### [Back To Top](#not-pron "Top Of Page")
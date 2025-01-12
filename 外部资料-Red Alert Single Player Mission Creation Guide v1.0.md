原文链接 : https://groups.google.com/g/comp.sys.ibm.pc.games.strategic/c/himrYrcqnyE?pli=1


> [FAQ] Red Alert Single Player Mission Creation Guide v1.0 (very long)  
> Author : Andrew Griffin  
> 1997年3月4日 16:00:00


# The Red Alert Single Player Mission Creation Guide

Release 1.0
March 5, 1997

Copyright 1997 Andrew Griffin and Charles Francis Harkins.
All Rights Reserved
bu...@adam.com.au
cfh...@msn.com

DISCLAIMER
The purpose of this guide is to aid the public with the creation of
single player missions for the game Command and Conquer: Red Alert, by
Westwood Studios Inc.

The authors claim NO responsibility regarding any illegal activity
concerning this guide, or indirectly related to this guide.

Future updates and add-ons may render parts of this guide obsolete.


TRADEMARK INFORMATION
Command and Conquer: Red Alert is a trademark of Westwood Studios, Inc.,
and is so acknowledged. Any trademarks not directly mentioned are also
acknowledged.


COPYRIGHT NOTICE
This article is Copyright 1997 by Andrew Griffin and Charles Francis
Harkins. All rights reserved. You are granted the following rights:

I. To make copies of this work in original form, so long as
(a) the copies are exact and complete;
(b) the copies include the copyright notice and these paragraphs in
their entirety;
(c) the copies give obvious credit to the authors, Andrew Griffin
and Charles Francis Harkins;
(d) the copies are in electronic form.
II. To distribute this work, or copies made under the provisions above,
so long as
(a) this is the original work and not a derivative form;
(b) you do not charge a fee for copying or for distribution;
(c) you ensure that the distributed form includes the copyright
notice, this paragraph, the disclaimer of warranty in
their entirety and credit to the author;
(d) the distributed form is not in an electronic magazine or
within computer software (prior explicit permission may be
obtained from Andrew Griffin or Charles Francis Harkins);
(e) the distributed form is the NEWEST version of the article to
the best of the knowledge of the distributor;
(f) the distributed form is electronic.

This document is for reading, not taking. You may not distribute this
work by any non-electronic media, including but not limited to books,
newsletters, magazines, manuals, catalogues, and speech. You may not
distribute this work in electronic magazines or within computer software
without prior written explicit permission. These rights are temporary
and revocable upon written, oral, or other notice by Andrew Griffin or
Charles Francis Harkins.

To report a suspected copyright violation, or to request additional
rights beyond those granted above, write to the either of the authors at
"bu...@adam.com.au" or "cfh...@msn.com" on the Internet.

Table of Contents

CHAPTER [1] Introduction
[1-1] Foreword and Introduction
[1-2] What this guide is NOT
[1-3] Getting the guide
[1-3-1] Usenet
[1-3-2] WWW
[1-3-3] BBS
[1-4] Contributing to the guide
[1-5] Acknowledgements
[1-6] Accuracy of Information


-SECTION ONE- GENERAL OVERVIEW

CHAPTER [2] Notes Before You Start
[2-1] Negative numbers - what's the deal?
[2-2] Determining where things go
[2-3] .ini and .mpr files
[2-4] A warning about Red Alert's parser
[2-5] Placing walls around the map
[2-5-1] Fences1.mpr file

CHAPTER [3] Glossary
[3-1] Terms used in this document


-SECTION TWO- SPECIFIC INFORMATION

CHAPTER [4] Mission File Components
[4-1] [Basic] Section
[4-2] [Map] Section
[4-3] Country Specific Information
[4-4] [STRUCTURES] Section
[4-5] [SHIPS] Section
[4-6] [INFANTRY] Section
[4-7] [UNITS] Section
[4-8] [TERRAIN] Section
[4-9] [SMUDGE] Section
[4-10] [Base] Section
[4-11] [Waypoints] Section
[4-12] [CellTriggers] Section
[4-13] [Trigs] Section
[4-13-1] Trigger Information
[4-13-2] Available Trigger Events
[4-13-3] Available Trigger Actions
[4-14] [TeamType] Section
[4-14-1] Available TeamType Actions
[4-15] [MapPack] Section
[4-16] [OverlayPack] Section
[4-17] [Digest] Section

CHAPTER [5] Tables
[5-1] Available Red Alert Movies
[5-2] Available Red Alert Songs
[5-3] Available Red Alert Speeches
[5-4] Available Red Alert Sound Effects
[5-5] Available Red Alert Countries
[5-6] Available Red Alert Buildings
[5-7] Available Red Alert Infantry Units
[5-8] Available Red Alert Vehicles
[5-9] Available Red Alert Aircraft
[5-10] Available Red Alert Ships
[5-11] Available Unit Formations
[5-12] Available Red Alert Special Weapons
[5-13] Available Initial Unit Commands
[5-14] Available Terrain Types
[5-15] Available Smudge Types

CHAPTER [6] Miscellaneous
[6-1] Tutorial.ini
[6-2] Mission.ini
[6-3] Red Alert Mission Tree
[6-3-1] Allied Missions
[6-3-2] Soviet Missions


-SECTION THREE- THEORY

CHAPTER [7] From The Lectern
[7-1] Contributing to the Lectern
[7-2] How to get units appearing out of buildings
[7-3] Changing Red Alert Values
[7-4] How to control where reinforcements come from
[7-5] How to get units to enter buildings
[7-6] Discussion on IQ Levels
[7-7] On the use of Badger Bombers
[7-8] The Global Mission Timer
[7-9] What is the Zone of a cell?


-SECTION FOUR- APPENDICES

CHAPTER [8] Items To Fill

CHAPTER [9] Internet Resources
[9-1] Third Party Programs
[9-2] WWW Pages

CHAPTER [10] Revision History

End Contents


-------------------------
CHAPTER [1] Introduction
-------------------------

[1-1] Foreword and Introduction
================================
This document represents a significant investment of time by the two
authors, the purpose of which is to see the creation of new single player
missions for the game Red Alert. Just as there were hundreds of single
player missions created for the original Command and Conquer, we hope
that the same will be true for Red Alert.

It is a sad fact that this guide has to be created by someone other
than the company that created Red Alert, but for whatever reasons they
had, Westwood Studios decided to supply a terrain editor that could
create new multiplayer missions, but could not create new single player
missions. In order to create a new single player mission, you will use
the terrain editor to create the map, but will also be using a text
editor to do everything else.
That being said, my co-author has this to say (which I agree with, a
least to a limited extent):
I don't have a quarrel with Westwood's policy here. Their bread and
butter is making and selling maps and scenarios. After the host of bad
C&C missions that were made by independents, they should naturally be
cautious about giving the means to make RA scenarios to all and every.
Gresham's Law applies here. They did give us the Rules.ini file,
and they didn't have to do that.

There you have what are essentially the two sides to the story: if
Westwood released their information, then the good mission makers would
be able to create better missions. The flipside to this is that there
would be a lot more poor missions, making it that much harder to sift
through the dross.

The more discerning reader will notice that there are gaps in our
knowledge throughout some sections in this guide. We have made a
significant effort to work out these sections, but there is only so much
that two brains can accomplish in a finite amount of time. If you work
out what one of the missing sections pertains to, or have further
information on something that we have already commented on, then please
get in contact so that we can make this document as accurate as
possible. If you do make a submission, we ask that you test it
thoroughly.

Making single player missions for Red Alert is not easy, even if you
have some previous experience with creating new missions for Command and
Conquer. This is mainly through the increased complexity of the
triggers that you now have access to, which enable you to do some quite
intricate activities. Yes, you can create a mission using just the
simplistic forms of triggers, but it is the opinion of this author that
this is akin to buying a car to drive up and down the driveway.
However, we do recommend that you start off by learning the basics.
Start with a blank map and just experiment until you begin to get the
feel of the way the Red Alert triggers operate.

We wish you the very best in your efforts.

And, yes, we know the title is a bit of a mouthful, but what else
could this be called? And I also know that my typing style tend to the
verbose, but in this case I do not see that as a problem. An effort has
been made to keep all lines to 74 characters or less, but in the case
where I have included sections from an external file, this may not be
possible.


[1-2] What this guide is NOT
=============================
This guide is not meant to tell you what makes a good mission; that
changes from person to person. If I start to preach about what I
feel makes a good mission, I trust you to forgive my lapse.

This guide is also not meant to make everyone into a mission making
guru. If you were good at creating single player missions for Command
and Conquer, then you are already a step ahead, as many of the actions
you must perform are the same. If you have never made a mission before
all I can say is: give it a try, you may be great at it.

This guide will also not tell you that I think story is the most
important part of any mission. Again, the two authors differ in what we
see making a good mission. To quote cfh: "I'm just a nuts-n-bolts
kill-em-all type. Plot be damned."

This guide will not become a 'how do I edit the rules.ini file?'
guide. It will address single player mission creation only.

This guide is not meant to encourage you to email us. My email policy
is based on mass recycling (which means that I delete those emails that
I have no intention of replying to). Do not contact the authors if you
want to ask how to do something with a trigger or teamtype, for you are
likely to end up on the trash heap.


[1-3] Getting the guide
========================
This guide will NOT be sent out by the authors via email, so don't
even bother to ask.

[1-3-1] Usenet
---------------
A pointer to the Red Alert Single Player Mission Creation Guide will
be posted irregularly on the following newsgroups:
(1) alt.games.command-n-conq
(2) comp.sys.ibm.pc.games.strategic
Just how often this is posted depends mainly upon when new versions
are created, and also how lazy I feel. (I do not get the Red Alert
newsgroups on my news server, so can only post to them if I use
dejanews).

[1-3-2] WWW
------------
New releases of this Guide will be found at the following World-wide
Web sites:

http://www.geocities.com/TimesSquare/5458/ra.html

[1-3-3] BBS
------------
I am not responsible for uploading new releases of the Red Alert
Single Player Mission Creation Guide to bulletin board systems. I have
control over neither them nor their naming conventions, and can not
guarantee that a given BBS will hold a copy of the creation guide in
their files area.

ATTENTION: All BBSes, CompuServe, America Online, and all other
information services. PLEASE conform to the naming standard of the Red
Alert Single Player Mission Creation Guide when placing this file on
your system. The file name should be 'racg?.zip' where the '?' is the
revision number of the guide or 'racg?.txt' if the guide is a text file
instead of PKZIPped.


[1-4] Contributing to the guide
================================
If you have something to add to the guide, please send E-mail to
'bu...@adam.com.au' or 'cfh...@msn.com' (no quotes), explaining your
addition. It will be reviewed, and if accepted, edited and added to the
next revision of the strategy guide. In the E-mail, please supply your
name and E-mail address (do not rely on us to extract it from the mail
header). Please be as detailed as possible in your submission.

Please note that all submissions to the guide become property of the
authors (Andrew Griffin and C. Francis Harkins) and that they may or may
not be acknowledged. By submitting to the guide, you grant permission
for use of your submission in any future publications of the guide in
any media. The authors reserve the right to omit information from a
submission or delete the submission entirely.


[1-5] Acknowledgements
=======================
Many thanks to Roger Wong for allowing me to copy the style of his Red
Alert Internet Strategy Guide.


[1-6] Accuracy of Information
==============================
We have made a significant effort to make sure that the information
contained within this guide is as accurate as possible. However, this
is not always possible when it comes to sections such as the teamtypes
section. There seem to be levels of interdependencies in some areas
that remain unexplored.

All information retrieval is subject to personal bias, and it may be
the case that the testbeds that were used in the collection of this
information introduced a bias into what we were seeing.

==============================
-SECTION ONE- GENERAL OVERVIEW
==============================

-----------------------------------
CHAPTER [2] Notes Before You Start
-----------------------------------

[2-1] Negative numbers - what's the deal?
==========================================
If you look at the original Red Alert missions, you will notice
almost immediately that the numbers used in this guide for things such
as speech items, sound effect, etc are completely different from those
used in the missions. However, at a closer glance, you will see that
this is, in fact, not the case. The numbers used in the original
missions are all negative numbers, those used in this guide are all
positive numbers.

To convert from the negative numbers is the original missions to the
positive numbers used in this guide, then you simply do the following:
if the negative number is in the negative hundreds (ie -200, -100, -57
etc), then all you have to do is add 256 to that negative number to get
the positive number. In the rare occasions where the negative number is
is the negative 64,000 range, then you add 65536 to get the respective
positive number.

You may be wondering why we chose to use the positive numbers rather
than the negative numbers. There are two reasons for this. The first
reason is that it is simply more intuitive to use the positive numbers.
The second reason comes from a belief that I have that the use of the
negative numbers in the original mission files comes from a bug in the
Westwood mission creation program. Apparently the parser is competent
enough to deal with this error, which is a possible reason it was never
picked up. Of course, it doesn't matter one way or another, as long as
it works.

If you really want to use negative numbers, then simply subtract 256
from the numbers that we have given you. The only place you don't use
negative numbers (another reason I assume the occurance of negative
numbers is a programming bug) is where the second part of a trigger is
used to specify a specific country. In these cases, the Westwood
missions use the positive country numbers.


[2-2] Determining where things go
==================================
One of the first things you may notice is that you need to specify
cell values for a wide variety of things, but there really isn't an easy
way to get the required cell values when using the terrain editor.
There are a number of ways in which you can use the terrain editor to
provide cell values, although all but one method are work-arounds.
However, all methods require you to load up a file after you have
finished editing the map. For this reason, if you are using Windows 95,
you have a great advantage, as you can just minimise the terrain editor,
and open the required file. For users that only have MS-DOS installed
on their computers, I am afraid that you will exit the terrain editor
(and hence suffer the long load time when you want to use it again).

The easiest way to use the terrain editor to determine the numbering
of a specific cell on the map is to use the flags. When you place the
flags, you are actually creating an entry in the [Waypoints] section of
the map file. It is then very easy for you to get these cell values for
use in other regions of the ini file. However, there are unfortunately
only a limited number of flags, meaning that if you use this method that
you will have to repeatedly save the map file to get further cell
values.

The other method to get cell values is to use something else to
pin-point a cell value. This must be something that appears in a
section like [Terrain], which means trees, or a goldmine. You cannot
use things that appear as an overlay (gold, gems, walls etc), as these
are encoded into the [OverlayPack] section of the ini file. If you
decide to use this method of determining a cell's numbering, you should
do it before you place the rest of the map's terrain features (ie finish
the map in so far as you have all the cliffs and rivers and gold that
you want, but don't put in any trees yet). Use your personal preference
as to whether you want to use a single type of tree for this job, or
whether you want to use multiple type (personally, I find it easier to
use a single type, with a goldmine occasionally thrown in to highlight a
particular cell). Then, place these trees (or etc) around the map where
you want to place things like buildings, units, or that you just want to
specify as waypoints.

Once you have edited your ini file using these cell values to place
your structures and units, you can then edit your .mpr file to get rid
of the now superfluous terrain features.

This is the most tedious part of the whole process.


[2-3] .ini and .mpr files
==========================
When you use the supplied terrain editor to create a map, saving your
map causes it creates a file with a .mpr extension. The name of the
file will correspond to the name you gave the map when it was created,
taking the first seven (at most) letters to create the filename. The
format of a .mpr file is the same as an .ini file, and you should use
this .mpr file as the template of your mission file. Multiplayer files
have the extension .mpr (when you use the terrain editor, you are
actually creating a multiplayer mission).

The files you will be using to create single player missions have the
extension .ini. These files (as do the .mpr files) have the same
format as all .ini files, in that they consist of a number of different
sections. Each section contains a heading enclosed in square brackets
(such as [England]), and consists of a number of entries, one to a line,
after that heading. A ';' (semi-colon) signifies the comment, and
everything after a ';' is ignored.

To create a single player mission, you must give your .ini file a
specific name, corresponding to the mission that you wish to replace.
See the section Red Alert Mission Tree for the internal mission numbers
(ie scg01ea, scg02ea etc); you take this internal mission number as the
first part of the filename, and give the file the extension .ini (so,
you will get scg01ea.ini, scg02ea.ini etc). By using the correct
filename, you are able to replace the original missions in Red Alert by
your new mission.

Because you are able to completely control the units and buildings
that the player will be able to build (through the use of the TechLevel
entry in the country specific information sections), you should always
use the first mission of either the Allied or Soviet sides (ie
scg01ea.ini for Allied mission number 1, or scu01ea.ini for Soviet
mission number 1). This also makes it possible for the player to simply
hit the Start New Game button in order to play your mission.


[2-4] A warning about Red Alert's parser
=========================================
You should be made aware that the parser Red Alert uses to read in the
ini files is case sensitive. This means that if you have a section
called [Terrain], that you will have no trees (you must use [TERRAIN]).
Always use the exact spelling we have given in this document. A single
type can crash this game horribly. It is best to construct the scenario
in small pieces, testing as you go. The DOS version seems to be much
more tolerant of errors than the Windows 95 version.


[2-5] Placing walls around the map
===================================
Unfortunately, you cannot place any type of walls in the terrain
editor, at least not without some work. To place walls on a map, you
first need to copy a wall piece from one map, and paste that into your
new map.

First, open your map file that has some walls on it. Next, select the
tile that you require. You select a section of the map by left clicking
on the map - the tile will be surrounded by a white square. Now, click
the right mouse button and choose Copy from the list of choices.

Load the map you wish to place the wall section onto, and select the
spot into which you wish to place the wall section. Right click and
select Paste. You can now place the wall tiles anywhere around the map.

Do not worry that the graphics of the walls look strange (ie they do
not join up as they are supposed to do), as this will go away once the
map is loaded again. Alternatively, you can force a section of wall to
be redrawn (they will appear normally after the redraw) by placing a map
tile (usually just the bank cell) next to the wall section.

[2-5-1] Fences1.mpr file
-------------------------
For your convenience, here is a very small .mpr file that contains 4
types of walls. It contains the sandbag (SBAG), barbed wire (FENC),
concrete (BRIK), and chain-link (CYCL) wall types. This file has the
name fences1.mpr. In the Windows 95 terrain editor, it is smaller than
the displayed area, so you cannot scroll the map. Simply put this map
into your Red Alert directory, and copy the required fence type.

---cut here--- DO NOT INCLUDE THIS LINE!!!
[Basic]
NewINIFormat=3
Name=fences

[Map]
Theater=TEMPERATE
X=32
Y=32
Width=14
Height=14

[Waypoints]
98=4128

[MapPack]
1=CQAAIIH//v4f/4H/gB8AACCB//5ZAP+CAQD+/gD//+YLWgCCAQDXQA3+oxL/gf+ACQAAII
2=H//v4f/4H/gAkAACCB//7+H/+B/4AJAAAggQD+/h8AgQCACQAAIIEA/v4fAIEAgA==

[OverlayPack]
1=FQAAIIH//qAQ/4cA/xf/Av8B/lcP/4H/gAkAACCB//7+H/+B/4A=
---cut here--- DO NOT INCLUDE THIS LINE!!!

---------------------
CHAPTER [3] Glossary
---------------------

[3-1] Terms used in this document
==================================
The following is a list of terms that are used throughout this
document with which you may not immediately be familiar. This list is
presented so that you are able to grasp the concepts that we discuss
with as little difficulty as possible.

AI A sad joke. (sorry) Any country under computer control.
anchor cell The upper left hand corner of a structure or terrain
feature is the anchor cell. It is in this cell that you
want the upper left hand corner to be positioned.
attached Used when talking about a trigger. Triggers are said to
be attached to units or buildings when the appropriate
part of the unit or building entry has been filled with
that trigger's name.
autocreation Autocreation means that instead of a teamtype being
manually created by a Create Team trigger action, that
it will be subject to the autocreate function. Each
computer country can have its autocreation function
turned on through a trigger action, after which the
creation of the teamtypes that have autocreation turned
on will be subject to being created, at the whim of the
autocreate function. See [TeamType] Section for more
details.
cell A Red Alert map is really a 128x128 square. A cell is
the size of one unit of this square, so the square would
be 128x128 cells in size. See the [Waypoints] section for
a more detailed explanation of the way the map is divided
into cells.
country When we mention a country, we are talking about an
individual entity, much like real countries. They are
either controlled by the human player, or by the
computer. All units and buildings owned by a country
can only be controlled by the controller of that
country (human or computer).
expires When talking about the global timer, we say that the timer
has expired when the timer count has reached zero.
fired trigger A fired trigger is a trigger that has been activated (ie,
its firing conditions were met).
forced trigger A trigger that, on its own, cannot be fired. It can only
be fired by another trigger.
global timer Like a stop watch that works in reverse. It counts down
from a specified time until it expires. There is only one
global timer in Red Alert.
global value Consider this to be a switch, which has an On and Off
position. We say that a global value is 'set' when it is
in the On position, and that is it 'clear' when it is in
the off position.
house See country.
IQ level How 'smart' a particular computer player is, in Red Alert
terms. See Discussion on IQ Levels for a more detailed
description on IQ levels in computer players.
full map The entire 128x128 map. This differs from the map that you
will be using for you mission, which is a subset of the
full map square.
mission map That section of the full map that you are using for your
mission. It is a subsection of the full map.
parameter A value that is being passed to some item.
player Usually referring to the human player.
team Shorthand for a teamtype.
teamtype A collection of units, whether they be vehicles, infantry,
ships, aircraft, or a mixture. It can also refer to a
line in the [TeamTypes] section.
time unit The smallest amount of time in Red Alert. This changes
depending on the speed at which you have Red Alert
running, but is apparently 6 seconds of Red Alert time.
It is only used when talking about the duration you want
an activity to occur for, or to have some action occur
at a specified time in a mission.
trigger An action that Red Alert is to perform, either through a
computer player or independent of any player.
trigger event When talking about trigger events, we mean some *thing*
that has occurred in the Red Alert world (even something
as banal as a certain period of time passing). They are
actually tests made by Red Alert, to see if the condition
specified by the event is True.
trigger action When talking about trigger actions, we are talking about
the action that Red Alert is to take in response to a
fired trigger.

==================================
-SECTION TWO- SPECIFIC INFORMATION
==================================

------------------------------------
CHAPTER [4] Mission File Components
------------------------------------

[4-1] [Basic] Section
======================
The [Basic] section of each mission ini file contains the following
pieces of information (it doesn't have to contain all of these lines,
but these are the valid ones):

Name=In the thick of it
Intro=<none>
Brief=ALLY1
Win=SNOWBOMB
Lose=BMAP
Action=LANDING
Player=Greece
Theme=No theme
CarryOverMoney=0.25
ToCarryOver=no
ToInherit=no
TimerInherit=no
CivEvac=no
NewINIFormat=3
CarryOverCap=0
EndOfGame=no
NoSpyPlane=no
SkipScore=no
OneTimeOnly=no
SkipMapSelect=no
Official=yes
FillSilos=no
TruckCrate=no
Percent=0

These entries will now be explained in a bit more detail.

Name=...
--------
This is used to give the mission a name, whether it be for a
multiplayer mission, or for a later addition to Red Alert. It is likely
that there will be something similar to the system that came with Covert
Operations where you could put missions on the New Mission button.
Default=none

Intro=...
---------
This is the name of the video to play as the introduction movie to
this level. See Available Red Alert Movies for the list of possible
movie names.
A <none> means that no video is being used for the introduction movie.
The introduction movie is played first (before the briefing and
action movies).
Default = <none>

Brief=...
---------
This is the mission briefing movie for the level. See Available Red
Alert Movies for the list of possible movie names.
A <none> means that no video is being used for the briefing movie.
The briefing movie is played second (after the introduction movie but
before the action movie). If the user clicks on the mission briefing
button and presses the Video button, this is the video that gets played.
Default = <none>

Win=...
-------
This is the movie that gets shown when you win the mission. See
Available Red Alert Movies for the list of possible movie names.
A <none> means that no video is being used for the win movie.
Default = <none>

Lose=...
--------
This is the movie that gets shown when you lose the mission. See
Available Red Alert Movies for the list of possible movie names.
A <none> means that no video is being used for the lose movie.
Default = <none>

Action=...
----------
This is the name of the video to play as the action movie for this
level. See Available Red Alert Movies for the list of possible movie
names.
A <none> means that no video is being used for the action movie.
The action movie is played last (after the introduction and briefing
movies).
Default = <none>

Player=...
----------
This tells the computer which country the user will be playing as
during this mission. See Available Red Alert Countries for the listing
of available countries. This uses the full name of the country, not the
number or abbreviation.
You should have a valid Player= section in your ini file. If you do
not have a Player= entry in this section, the player will default to
Greece.

Theme=...
---------
This is the piece of music to play at the start of the mission. See
Available Red Alert Songs for the listing of available music titles to
play at the start.
An entry of 'No theme' means that there is no specific music to play
at the start of the mission, and that Red Alert should use the normal
method of choosing which music to play.
On tests, I have been unable to get this to work. Despite what I put
here, a random piece of music plays at the beginning of the level.
Default=none

CarryOverMoney=...
------------------

ToCarryOver=...
---------------
If 'yes', units and structures at the (victorious) close of this
mission will appear at the start of the next mission where
"ToInherit=yes". They will appear in the exact position and state of
health they where left at the end of the mission. Activities will not
carry over. Guard and harvest seem to be the defaults. Aircraft in
flight will vanish.


ToInherit=...
-------------
If set to 'yes', see ToCarryOver (above).

TimerInherit=...
----------------

CivEvac=...
-----------
This can have the value 'yes' and 'no'.
When 'no', it means that transport helicopters do not take off when
'civilian' units are loaded into them, unless there is a trigger for
this action.
When set to 'yes', transport helicopters will take off once 'civilian'
units are loaded into them.

NewINIFormat=...
----------------
If this item is not present with a valid value, the [Trigs] and
[TeamTypes] sections will not be read. 0 and 1 are not valid. 3 is
always used, and is the value inserted by Red Alert's terrain editor,
which suggests it also has something to do with either the overlays
(OverlayPack) or the map (MapPack)

CarryOverCap=...
----------------

EndOfGame=...
-------------
This can be set to 'yes' or 'no'.
When set to 'yes', when the player has won the mission, after they
see the Win video, they get to see the Red Alert credits, and after
that are taken back to the main menu. The use of 'yes' for this item
signifies that the campaign is finished.
When set to 'no', the next mission is played, as usual.

NoSpyPlane=...
--------------
This can be set to 'yes' or 'no'.
When set to 'no', if the player has an airfield and a sufficiently
high tech. level, then they will be able to use the spy plane.
When set to 'yes', the spy plane will not appear on the side bar, even
if the player has a sufficiently high tech. level.

SkipScore=...
-------------
This can be set to 'yes' or 'no'.
When set to 'no', when the player finished the mission, they are
treated to the score screen, where they see how well they did in that
mission (units killed, money finished with etc).
When set to 'yes', the player does not get this score screen.

OneTimeOnly=...
---------------
This can be set to 'yes' or 'no'.
When set to 'yes', after the mission is won by the player, they are
taken back to the main menu, as if they had finished the entire
campaign. This value does not mean that if the mission is failed that
it cannot be retried - the player still gets the option to retry the
mission if they fail.
When set to 'no', winning the mission takes the player to the next
mission in the campaign, as usual (if possible).

SkipMapSelect=...
-----------------
This can be set to 'yes' or 'no'.
When set to 'no', after the user has finished a mission, they are
given the map of Europe and have to pick one of the flashing boxes for
their next mission.
When set to 'yes', the user does not see the map of Europe. Instead,
Red Alert loads up the next mission FOR THAT LEVEL. This is very
important: if the player just finished scg05ea, then scg05eb will be
loaded, not scg06ea. Note that you can do this even for those levels
that only have a single 'official' mission. eg there is only 1 Soviet
level 1 mission, but if you have an scu01eb.ini file present and this
value set to 'yes', then level scu01eb will be started immediately after
scu01ea is finished. However, it doesn't appear that you can chain
these indefinitely. Adding an scu01ec.ini file didn't work - I would
guess that the only place where a third would be accepted would be
Allied mission 5, where there are already 3 missions (scg05ea eb and
ec).
It would be an unwise thing to have this set for an 'ea' mission if
the map before gave the player a choice of playing either an 'ea' or
'eb' mission, as they may choose the 'eb' mission, hence by-passing the
first stage of the mission and possibly screwing up your storyline. See
Red Alert Mission Tree for the 'official' mission tree structure.
A side effect of setting this to 'yes' is that the player does not get
the 'Mission Accomplished' text on the screen - it just goes straight to
the win video (if there is one).

Official=...
------------
This is always set to 'yes' in the original Red Alert missions.
Giving it a value of 'no' does not seem to have any effect.

FillSilos=...
-------------
This item can be set to 'yes' or 'no'.
When set to 'yes', any country that has silos will have any starting
money they have placed in the silos, rather than starting with those
silos empty. This is useful if you want the player/computer to use
thieves at the very start of a mission, before the first harvester can
come in.
When set to 'no', the silos start empty at the beginning of the
mission.

TruckCrate=...
--------------
This item can be set to 'yes' or 'no'.
When set to 'yes', when a convoy truck (TRUK) is destroyed, it leaves
behind a crate with money in it (a WoodCrate, if you want to change what
is in the crate). Even trucks owned by the player drop crates when
destroyed if this is set to 'yes'.
When set to 'no', a destroyed convoy truck does not drop a crate.

Percent=...
-----------


[4-2] [Map] Section
====================
The [Map] section of the mission's ini file tells Red Alert the size
and shape of the map that you are using. It also tells Red Alert which
tile set to use. For a detailed description of cells and what the full
map looks like, please read the section on Waypoints. The following is
a typical [Map] entry:
[Map]
Theater=SNOW
X=32
Y=32
Width=64
Height=64

Each section of the entry will be described below:

Theater=
--------
This tells Red Alert which tile set to use. The possible choices are
SNOW, TEMPERATE and INTERIOR. The three choices are self-explanatory in
terms of the tile set they represent.
Please note: the INTERIOR tile set is not used in Red Alert's terrain
editor, and if you change the Theater to INTERIOR and try to load up
that map in the terrain editor, the editor will crash.

X=
--
This tells Red Alert how far away from the left edge of the full map
the mission map starts. This must always be at least 1. The distance
is the number of cells from the edge.

Y=
--
This tell Red Alert how far away from the top edge of the full map the
mission map starts. This must always be at least 1. The distance is
the number of cells from the edge.

Width=
------
This tells Red Alert the width of the mission map (in cells). This
width plus the X value plus 1 must NOT be more than 128.

Height=
-------
This tells Red Alert the height of the mission map (in cells). This
height plus the Y value plus 1 must NOT be more than 128.

Each map must have at least a 1 cell buffer around the edge of the
mission map. This means that X and Y must always have the value of at
least 1, and that Width and Height must always have a value no greater
than 126. Note that while 126x126 maps are possible, Red Alert does not
handle them well.


[4-3] Country Specific Information
===================================
For each country you have in your missions, whether they be in
control of a large base or make a cameo role as a single civilian
infantry unit, you should include some information about that country,
even if it is nothing more than the allies of that country.
To include country specific information into your ini file, you first
take the name of a country (the full name), see Available Red Alert
Countries for this information, and place it within square brackets,
such as [Spain], [Ukraine] and [England] for example.
Under each of these headers, you then add the information that you
want to pertain to that country.

The available pieces of information that you can include as country
specific information seem to be the following (given through an example
of a complete entry):

[Greece]
Credits=12
Edge=South
MaxUnit=50
MaxInfantry=50
MaxBuilding=10
MaxVessel=10
TechLevel=10
IQ=3
Allies=USSR,Turkey
PlayerControl=yes

These will now be explained in more detail:

Credits
-------
This is the amount of starting cash for that country for the mission.
To get the real amount of cash, multiply the value by 100 (ie a value of
12 means that that country starts with 1200 cash).
This is cash-in-hand, unless the FillSilos variable (in the [Basic]
section) is set to yes, in which case the cash is stored in any
available silos or refineries.

Edge
----
The available values are North, East, South and West. Contrary to
intuition, this does not control the direction from which reinforcements
will arrive. In fact, it doesn't seem to do anything. Probably a
relic from C&C where it did control the direction of reinforcements.

MaxUnits, MaxInfantry, MaxBuilding, MaxVessel
---------------------------------------------
I'd guess that it limits the number of vehicles, buildings, ships and
infantry units the country can have on the map at one time. Unknown
whether it overrides the values from the rules.ini file.
Untested as yet.

TechLevel
---------
Each building and unit has an associated tech. level at which it can
be built; to be able to build it, the country needs to have a tech.
level of at least that level.
This is mainly used to control what the human player can build in the
mission.

IQ
--
This sets the IQ level of the country. It would be unwise to set the
human's country to any IQ level but 0 (which is the default for human
controlled countries), as the computer would then be controlling the
human's buildings and units.
See Discussion on IQ Levels for more on how IQ levels affect a game.

Allies
------
This is a comma separated list (ie GoodGuy,Greece,Germany,USSR) of the
countries that this country will treat as friends and not attack.
Please note that this is not automatically reciprocated, in that if you
don't want two countries attacking each other, you have to set correctly
set the allies field for both country specific information entries.
You use the full name of the country in this list.

PlayerControl
-------------
By default this is set to 'no', and is rarely seen. However, if it is
set to 'yes', then the human player will be able to control the units
of this country. The human player will not own these units, but will be
able to direct their movement, etc.
In addition to being controllable by the human player, when these
units move (whether by being controlled by the human or the computer),
they remove the shroud from the map as the human's own units would.
Any buildings of this country also remove the shroud around them as if
they were owned by the player.
A player cannot use the buildings of this country for construction.


[4-4] [STRUCTURES] Section
===========================
The [STRUCTURES] section contains those buildings which you want to
appear on the map at the beginning of the mission. See Available Red
Alert Structures for the list of building abbreviations. The following
is a typical entry:

0=USSR,TSLA,256,7623,0,None,1,0

The format of a [STRUCTURES] entry is:
num=side,type,health,cell,facing,trig,???,repair

Each section of the entry will be described below:

num
---
This is the numbering of the structure. While it probably isn't
necessary, the numbering starts at 0 and increments from there. You
cannot have two buildings with the same number (the later will replace
the former).

side
----
This contains the owner of the structure. See Available Red Alert
Countries for the list of country names. You place the full name here,
not the abbreviation.

type
----
This contains the type of building to place on the map. See Available
Red Alert Buildings for the list of building abbreviations (you use the
abbreviation of the building name). Unlike the original C&C, all
buildings can appear in all terrain types, except for those noted in
Available Red Alert Buildings.

health
------
This is the condition that the building starts in, on a scale of 1 to
256. Treat this as a percentage, with 256 being 100%, 128 being 50%,
etc. Remember that some units and buildings have very small amounts of
hit points, so it may not be possible to give them the full range of
numbers (a civilian infantry unit with 5 hit points will only have 2 at
50% and 1 at 25%, roughly)

cell
----
The upper left hand corner of the building is the anchor cell of that
building. This value contains a cell number into which you want Red
Alert to place the anchor of the specified building.

facing
------
This is only useful for those structures which can track enemies (gun
turrets, anti-aircraft guns, and SAM sites); it is the direction you
want the particular structure to face at the beginning of the mission.
The following are the basic directions these buildings can point to: 0 -
North (the top of the screen), 64 - East (right hand side of the
screen), 128 - South (bottom of the screen), and 192 - West (left hand
side of the screen). You can also have a few positions in between these
stages; the numbering goes in steps of 16 (ie valid numbers are 0, 16,
32, 48, 64, etc), with the initial facing of the turret changing with
the appropriate value.
Picture a clock face, and you will more easily be able to picture the
direction the turreted building will face in at the beginning of the
mission.

trig
----
The name of a trigger to attach to the building. If you want to
attach a trigger to a building, you place the name of the trigger you
want to attach in this position. If you don't want a trigger associated
with the building, set this value to None.

??(unknown)??
-------------
Don't know what this is for.

repair
------
This number indicates whether the building will be repaired or
not, provided that the computer player has a sufficiently high IQ level
(normally this would be an IQ level of 1 or more, but this may vary if
you have changed the [IQ] section of the rules.ini file). A value of 1
means it will be repaired. A value of 0 mean it won't be repaired.


[4-5] [SHIPS] Section
======================
This section contains the ships that you want to appear on the map at
the beginning of the mission. See Available Red Alert Ships for the
abbreviations of the ship types that you can use here. A typical entry
would look like:

0=Greece,DD,256,9265,192,Guard,None

The format of a [SHIPS] entry is:
num=side,type,health,cell,facing,action,trig

Each section of the entry will be described below:

num
---
This is the numbering of the ship. While it probably isn't necessary,
the numbering starts at 0 and increments from there. You cannot have
two ships with the same number (the later will replace the former).

side
----
This contains the owner of the ship. See Available Red Alert
Countries for the list of country names. You place the full name here,
not the abbreviation.

type
----
This contains the type of ship to place on the map. See Available Red
Alert Ships for the list of ship abbreviations (you use the abbreviation
of the ship name).

health
------
This is the condition that the ship starts in, on a scale of 1 to 256.
Treat this as a percentage, with 256 being 100%, 128 being 50%, etc.
Remember that some units and buildings have very small amounts of hit
points, so it may not be possible to give them the full range of numbers
(a civilian infantry unit with 5 hit points will only have 2 at 50% and
1 at 25%, roughly)

cell
----
This value contains the cell value into which you wish Red Alert to
place the ship.

facing
------
This value it is the direction you want the ship to face at the
beginning of the mission. The following are the basic directions in
which a ship can face: 0 - North (the top of the screen), 64 - East
(right hand side of the screen), 128 - South (bottom of the screen), and
192 - West (left hand side of the screen). You can also have a few
positions in between these stages; the numbering goes in steps of 16 (ie
valid numbers are 0, 16, 32, 48, 64, etc), with the initial facing of
the ship changing with the appropriate value.
Picture a clock face, and you will more easily be able to picture the
direction the ship will be facing at the beginning of the mission.

action
------
This is the action that you want the ship to perform at the beginning
of the mission. The ship will continue to perform this action until it
is told to do something else (by either the player or the computer), is
destroyed, or the action can no longer be performed. See Available
Initial Unit Commands for the list of commands a unit can be given.
Set this to None if you don't want the ship to perform any action at
the beginning of the mission.
The most common use would be to set the ship to either Guard, Area
Guard, Hunt or None.

trig
----
The name of a trigger to attach to the ship. If you want to attach a
trigger to a ship, you place the name of the trigger you want to attach
in this position. If you don't want a trigger associated with the ship,
set this value to None.


[4-6] [INFANTRY] Section
=========================
This section contains the infantry units that you want to appear on
the map at the beginning of the mission. See Available Red Alert
Infantry Units for the abbreviations of the infantry types you can use
here. The following is a typical entry:

0=Greece,E1,256,6977,2,Sticky,64,None

The format of an [INFANTRY] entry is:

num=side,type,health,cell,sub_cell,action,facing,trig

Each section of the entry will be described below:

num
---
This is the numbering of the infantry entry. While it probably isn't
necessary, the numbering starts at 0 and increments from there. You
cannot have two infantry entries with the same number (the latter will
replace the former).

side
----
This contains the owner of the infantry unit. See Available Red Alert
Countries for the list of country names. You place the full name here,
not the abbreviation.

type
----
This contains the type of infantry unit to place on the map. See
Available Red Alert Infantry Units for the list of infantry
abbreviations (you use the abbreviation of the infantry name).

health
------
This is the condition that the infantry unit starts in, on a scale of
1 to 256. Treat this as a percentage, with 256 being 100%, 128 being
50%, etc. Remember that some units and buildings have very small
amounts of hit points, so it may not be possible to give them the full
range of numbers (a civilian infantry unit with 5 hit points will only
have 2 at 50% and 1 at 25%, roughly)

cell
----
This value contains the cell value into which you wish Red Alert to
place the infantry unit.

sub_cell
--------
For infantry units, each cell is divided up into 5 sub-cells. It is
these sub-cells that allow five infantry units to be located in one
cell. The locations of the sub-cells within the main cell is:
1 2 <--- top of cell
0 <--- middle of cell
3 4 <--- bottom of cell
This value holds the number of the sub-cell into which you want to
place the infantry unit. If you are placing more than one infantry unit
within the same cell, you must make sure that their sub-cells are
different.
Infantry units are the only units that use sub-cells.

action
------
This is the action that you want the infantry units to perform at the
beginning of the mission. The infantry units will continue to perform
this action until it is told to do something else (by either the player
or the computer), is destroyed, or the action can no longer be
performed. See the section Available Initial Unit Commands for the list
of commands a unit can be given.
Set this to None if you don't want the infantry unit to perform any
action at the beginning of the mission.
The most common use would be to set the infantry unit to either Guard,
Area Guard, Hunt or None.

facing
------
This value it is the direction you want the infantry unit to face at
the beginning of the mission. The following are the basic directions to
which a ship can face: 0 - North (the top of the screen), 64 - East
(right hand side of the screen), 128 - South (bottom of the screen), and
192 - West (left hand side of the screen). You can also have a few
positions in between these stages; the numbering goes in steps of 16 (ie
valid numbers are 0, 16, 32, 48, 64, etc), with the initial facing of
the infantry unit changing with the appropriate value.
Picture a clock face, and you will more easily be able to picture the
direction the infantry unit will be facing at the beginning of the
mission.

trig
----
The name of a trigger to attach to the infantry unit. If you want to
attach a trigger to an infantry unit, you place the name of the trigger
you want to attach in this position. If you don't want a trigger
associated with the infantry unit, set this value to None.


[4-7] [UNITS] Section
======================
This section contains the vehicles that you want to appear on the map
at the beginning of the mission. See Available Red Alert Vehicles for
the abbreviations of the vehicles types that you can use here. A
typical entry would look like:
0=Greece,1TNK,256,8246,96,Sticky,None

The format of a [UNITS] entry is:
num=side,type,health,cell,facing,action,trig

Each section of the entry will be described below:

num
---
This is the numbering of the vehicle. While it probably isn't
necessary, the numbering starts at 0 and increments from there. You
cannot have two vehicles with the same number (the latter will replace
the former).

side
----
This contains the owner of the vehicle. See Available Red Alert
Countries for the list of country names. You place the full name here,
not the abbreviation.

type
----
This contains the type of vehicle to place on the map. See Available
Red Alert Vehicles for the list of vehicle abbreviations (you use the
abbreviation of the vehicle name).

health
------
This is the condition that the vehicle starts in, on a scale of 1 to
256. Treat this as a percentage, with 256 being 100%, 128 being 50%,
etc. Remember that some units and buildings have very small amounts of
hit points, so it may not be possible to give them the full range of
numbers (a civilian infantry unit with 5 hit points will only have 2 at
50% and 1 at 25%, roughly)

cell
----
This value contains the cell value into which you wish Red Alert to
place the vehicle.

facing
------
This value is the direction you want the vehicle to face at the
beginning of the mission. The following are the basic directions in
which a vehicle can face: 0 - North (the top of the screen), 64 - East
(right hand side of the screen), 128 - South (bottom of the screen), and
192 - West (left hand side of the screen). You can also have a few
positions in between these stages; the numbering goes in steps of 16 (ie
valid numbers are 0, 16, 32, 48, 64, etc), with the initial facing of
the vehicle changing with the appropriate value.
Picture a clock face, and you will more easily be able to picture the
direction the vehicle will be facing at the beginning of the mission.

action
------
This is the action that you want the vehicle to perform at the
beginning of the mission. The vehicle will continue to perform this
action until it is told to do something else (by either the player or
the computer), is destroyed, or the action can no longer be performed.
See Available Initial Unit Commands for the list of commands a unit can
be given.
Set this to None if you don't want the vehicle to perform any action
at the beginning of the mission.
The most common use would be to set the vehicle to either Guard, Area
Guard, Hunt or None.

trig
----
The name of a trigger to attach to the vehicle. If you want to attach
a trigger to a vehicle, you place the name of the trigger you want to
attach in this position. If you don't want a trigger associated with
the vehicle, set this value to None.


[4-8] [TERRAIN] Section
========================
This section contains various terrain features, such as trees that you
have placed around the map. Most of these items can be placed in the
Red Alert terrain editor.

A typical [TERRAIN] entry would be:
7102=T14
9107=MINE

Each entry in the [TERRAIN] section has the format:
cell=type

cell
----
This is the cell in which the terrain feature is to be anchored.

type
----
This is the type of terrain feature to place in the specified cell.
For the list of available terrain types and the theaters they appear in,
see Available Terrain Types.


[4-9] [SMUDGE] Section
=======================
Additional terrain effects are available in Red Alert, in the form of
craters and scorch marks. To place these effects on the map, you must
use the [SMUDGE] section. See Available Smudge Types for a listing of
the various types of smudge graphics that are available. A typical
[SMUDGE] section would look like:
[SMUDGE]
7723=CR1,7723,3
7724=SC1,7724,0

Each entry in the [SMUDGE] section has the format:
cell=type,cell2,depth

Each section of the entry will be described below

cell
----
This is the cell in which you want the smudge effect to be placed.
However, it seems as though this can be overridden if the cell2 value is
different from this value.

type
----
This is the type of smudge mark to place in the cell. See Available
Smudge Types for a listing of the types of smudge graphics that are
available.

cell2
-----
I honestly do not know what this is for. Every example I have seen
has this value equal to the first cell, and whenever I have put a
different cell value in this position, the smudge would be drawn at this
position instead of the first.

depth
-----
Not an accurate description of what this variable is actually used
for. It can have values from 0 to 3, but cannot be used for the SC type
of smudge effect. For the SC smudges, always set this value to 0
(otherwise strange graphics glitches occur).
When this value is set to 0, the normal graphic for the smudge is
displayed, but when this value is greater than zero, the graphic is
changed slightly. This new graphic depicts a larger crater, the higher
the number the larger the crater (in a very rough sense). A value of 3
seems to be the highest value that this can take.
Note that this effect is more pronounced for some crater types than
others.
When the smudge effect is a BIB, and this value is greater than 0, it
seems as though part of the bib graphic is painted over the bib graphic
as it is laid down. I would recommend not using any number other than 0
if you want to put down a BIB.


[4-10] [Base] Section
======================
The [Base] section is interesting and useful for a number of reasons.
The purpose of the [Base] section is to tell the Red Alert computer
players which buildings they must replace if they get destroyed, and
where they should be placing these buildings. If the computer player is
of sufficiently high IQ (an IQ level of 5 unless you have manually
changed it), then it will be placing its own buildings on the map, but
you can specify in this section buildings which it must place on the
map.
A typical [Base] entry would look like:
Player=Greece
Count=2
000=GUN,7463
001=GUN,7461
The Player= is used to determine which computer controlled country
these buildings are specifying. Because you can have more than one
computer controlled country in a mission, this is used so that the wrong
computer country doesn't build the structure. In the original C&C, the
[Base] entry did not have this functionality, and hence you often ended
up with the computer players constructing buildings in each other's
bases.
The Count= is used to specify the number of entries in this particular
section. If you do not wish to have a [Base] section, set count to 0.
If you just have one entry, set it to 1, etc.
Each entry has the following type:
num=type,cell

num
---
This is the number of the [Base] entry. It must be a 3 digit number,
starting at 000, and incrementing by 1 for each additional entry. Do
not have repeated numbers.

type
----
This is the type of building that you want the computer player to
build. See Available Red Alert Buildings for the list of abbreviations
to use in this area of the entry.

cell
----
This specifies the cell at which you want the building to be placed.
It is the building's anchor cell.

If the anchor cell is obstructed, indeed if any part of the area of
land the building needs is obstructed, then the building will not be
constructed.
As soon as the computer player has had its Production turned on, it
will begin construction of these buildings.

Apart from just replacing destroyed buildings, this section can also
be used to get a computer player to expand their base. The buildings
mentioned in the [Base] section do not need to exist on the map at the
beginning of the mission. You could, for example, construct an entire
base for a computer player but instead of placing it in the [Structures]
section, you could place it in the [Base] section. When that computer
player gets a construction yard, money and a Production order, it would
begin constructing this base.

There is no way of having multiple [Base] entries for different
computer controlled countries. This is a shame, as it means you can't
be creative and create multiple computer controlled bases from scratch.


[4-11] [Waypoints] Section
===========================
Waypoints are used in Red Alert for a number of things, but the most
common is to determine the movement of units. A waypoint is simply a
cell that has been identified as having some significance, and that has
been given an alias.
Waypoint 98 determines which section of the mission map to display at
the beginning of the mission. How it does this is not completely clear,
but it seems, in part, to be determined by whether or not the player has
units or buildings in the area of that waypoint. It may simply be that
the DOS and Windows 95 versions of Red Alert interpret waypoint 98 in a
slightly different way.
A typical [Waypoints] section will look like:
[Waypoints]
1=10298
5=9077
98=5063

Each entry has the format:
alias=cell

alias
-----
The alias of a waypoint is simply a number. This number cannot be
less than 0. As waypoint 98 has special meaning to Red Alert, this
might mean that there is a limit on the total number of waypoints that
you can have. However, if you create a mission that needs more than 99
waypoints, then I salute your perseverance. Personally, I doubt that
anyone would ever need more than 99 waypoints.
You cannot have multiple instances of the same alias for waypoints,
but you do not have to keep the alias you use in order. You could, for
example, use waypoints 0, 1, 2, 30, 35, 40 and 98, and there would be no
problems.

cell
----
This is the cell of the map for which you want to create the alias.

A further description of cells and how they relate to the map follows.

The full Red Alert map is a 128 by 128 square, using cells as the
measurement. The map would look something like this:

+--------------------+ -+-
| | |
| | |
| | 128 cells
| | in height
| | |
| | |
+--------------------+ -+-

| |
+--- 128 cells in ---+
| width |

However, because of the requirement that each map have at least a 1
cell buffer around the entire edge of the map, the maximum mission map
size is 126 by 126. This full map now looks like the following:

********************** -+- *'s represent part of the
*+------------------+* | full map that are not part
*| | |* | of the mission map.
*| 126 cells |* 128 cells
*| in height |* in height In this particular case, the
*| | |* | full map has a single cell
*+------------------+* | boundary around the mission map.
********************** -+-
|--- 126 cells ---|
| in width |
+--- 128 cells in ---+
| width |

You can have any combination of width and height, provided that you
obey the rule that you must have at least a single cell boundary around
the mission map. You could have, for example, the following: map height
of 50 cells, map width of 60 cells, 30 cells from the left, 10 cells
from the top. The map would look like:

********************** 10 -+-
********************** --- |
******* ******* | |
******* ******* 50 128 cells
******* ******* | in height
********************** --- |
********************** 68 |
********************** --- -+-
| 30 | | 38 |
| 60 |

| |
+--- 128 cells in ---+
| width |

Not the prettiest of diagrams, but you should be able to see what I am
trying to explain.

It is easy to determine the cell numbering. The first row in the map
is numbered from 0 to 127. The second row is numbered from 128 to 255,
etc. Use the formula:
row_number*128 + column_number
to determine the cell numbering.
Hence, the top left corner of the full map will be 0 (this will never
be on any map).


[4-12] [CellTriggers] Section
==============================
Celltriggers are used to place various triggers around the map, that
will be fired when the units of some country enter the specified cell.
A typical [CellTriggers] entry looks like:
[CellTriggers]
10204=kill
9076=bob1
9077=bob1

Each entry in the [CellTriggers] section has the format:
cell=trigger

cell
----
This is the cell into which you wish to place the trigger.

trigger
-------
This is the trigger that you want to place into the specified cell.
The name of the trigger must be at most 4 characters in length. The
most common form of triggers that are used as celltriggers are those
that have Player Enters as their trigger event.

You cannot have more than one trigger per cell.


[4-13] [Trigs] Section
=======================
This is the most important part of the ini file, for it determines how
the mission will pan out. It sets the win and lose conditions, and also
controls (to some extent) the way the computer opponents will behave. I
say 'to some extent' because with Red Alert, Westwood has introduced the
notion of giving the computer players some autonomy of the triggers in
the form of variable IQ levels (see Discussion of IQ Levels for more on
this subject).


[4-13-1] Trigger Information
=============================
A trigger (in the [Trigs] section of the ini file has the following
format:
name=1,2,h,i,T1,p1,p2,T2,p1,p2,R1,p1,p2,p3,R2,p1,p2,p3

Each section of the trigger is described below:

name
----
This is simply a name to describe the trigger. It seems as though
there is a maximum trigger name length of 4 characters if you want to
use a particular trigger as a celltrigger. There is probably a limit to
the length of a non-celltrigger trigger name, so it is probably best to
keep the name to a maximum lenght of 6 or 7 letter. The name can be any
combination of letters and numbers, and other symbols (+, _ etc), but
not a 'space' character.

1 (repeatable)
--------------
The first number tells RA whether this is a repeating trigger or not.
If it has the value 0, then the trigger will only ever be activated once
(not strictly true as the trigger can be fired again if associated with
a teamtype). If it has a value greater than 0, then the trigger is a
repeating trigger (ie it will be fired more than once).
For repeating triggers, there are two types. When the repeating
trigger has a value of 1, the trigger will only occur once the trigger
event has happened to all items (units and buildings) to which this
trigger has been attached. This is useful if you want, for example,
some action to occur after a specific set of buildings have been
destroy.
The second type of repeating trigger is the free repeater. When this
item has the value of 2, it will continue to repeat itself whenever its
trigger event is true. This is of use if you want, for example, to have
the trigger activate every 20 time units.

2 (which country trigger applies to)
------------------------------------
If the trigger event requires a country to be specified, then, in some
cases, this holds the country number. Refer to the specific trigger
actions as to which actions require this field to be filled in
correctly. Still, it is probably better to put the correct country in
here in any case, even if only to make it clearer which country this
trigger is being used for.
See Available Red Alert Countries for a listing of country numbers.

h (when to activate trigger)
----------------------------
When 0, only the first trigger event (part 5) must be true for the
trigger to be activated.
When 1, the first (part 5) and second (part 8) must both be true for
the trigger to be activated.
When 2, either the first trigger event or the second trigger event
must be true, whichever comes first.
When 3, either the first trigger event or the second trigger event
must be true.
See the upcoming summary (next) for further details on how this
operates.

i (which actions are triggered)
-------------------------------
When 0, only one trigger action is activated when the event is
triggered. See the summary (next) for which trigger action is
activated, and when.
When 1, both trigger actions are activated when the event is
triggered.

Summary: Combinations of trigger events and trigger actions
-----------------------------------------------------------
h,i
0,0 T1 -> R1
0,1 T1 -> R1 and R2
1,0 T1 and T2 -> R1
1,1 T1 and T2 -> R1 and R2
2,0 T1 or T2 -> R1
2,1 T1 or T2 -> R1 and R2
3,0 T1 -> R1, or T2 -> R2

Now, in words:
0,0 T1 true to activate R1
0,1 T1 true to activate R1 and R2
1,0 T1 and T2 true to activate R1
1,1 T1 and T2 true to activate R1 and R2
2,0 T1 or T2 true to activate R1 (whichever comes first)
2,1 T1 or T2 true to activate R1 and R2 (whichever comes first)
3,0 T1 true to activate R1, or T2 true to activate R2

If either T1 or T2 are time dependent and the trigger is a repeating
trigger, then the test for time passage is measured from the last firing
of any part of the trigger.

T1 (first trigger event)
-----------------------
This is the first event that will cause this trigger to fire. For a
list of trigger events, see Available Trigger Events.
Set to 0 if you don't want a first trigger event (for example, when
you will be forcing the trigger).

p1 (first parameter)
--------------------
This is called the first parameter when discussing trigger events.
Set to -1 if it is not needed.

p2 (second parameter)
---------------------
This is called the second parameter when discussing trigger events.
Set to -1 if it is not needed.

T2 (second trigger event)
------------------------
This is the second event that will cause this trigger to fire. For a
list of trigger events, see Available Trigger Events.
Set to 0 if you don't want a second trigger event.

p1 (first parameter)
--------------------
This is called the first parameter when discussing trigger events.
Set to -1 if it is not needed.

p2 (second parameter)
---------------------
This is called the second parameter when discussing trigger events.
Set to -1 if it is not needed.

R1 (first trigger action)
-------------------------
This number holds the first trigger action. This action will occur
when the trigger event(s) has occurred. For a list of available trigger
actions, see Available Trigger Actions.

p1 (first parameter)
--------------------
This is referred to as the first parameter when talking about trigger
actions (see Available Trigger Actions).
Set to -1 if it is not needed.

p2 (second parameter)
---------------------
This is referred to as the second parameter when talking about trigger
actions (see Available Trigger Actions).
Set to -1 if it is not needed.

p3 (third parameter)
--------------------
This is referred to as the third parameter when talking about trigger
actions (see Available Trigger Actions).
Set to -1 if it is not needed.

R2 (second trigger action)
--------------------------
If this trigger has more than one trigger action associated with an
event, then the second trigger action is held here. It has the same
possible values as the first trigger action (see Available Trigger
Actions for the full listing).
Set this value to 0 if you don't want this trigger to have a secondary
trigger action.

p1 (first parameter)
--------------------
This is referred to as the first parameter when talking about trigger
actions (see Available Trigger Actions).
Set to -1 if it is not needed.

p2 (second parameter)
---------------------
This is referred to as the second parameter when talking about trigger
actions (see Available Trigger Actions).
Set to -1 if it is not needed.

p3 (third parameter)
--------------------
This is referred to as the third parameter when talking about trigger
actions (see Available Trigger Actions).
Set to -1 if it is not needed.


[4-13-2] Available Trigger Events
==================================

Event Text
#'s Version
----------------------------
0 No Event
1 Entered by
2 Spied by
3 Thieved by
4 Discovered by player
5 House Discovered
6 Attacked by anybody
7 Destroyed by anybody
8 Any event
9 Destroyed, Units, All
10 Destroyed, Buildings, All
11 Destroyed, All
12 Credits exceed
13 Elapsed time (1/10th min)
14 Mission timer expired
15 Destroyed, Buildings, #
16 Destroyed, Units, #
17 No factories left
18 Civilians evacuated
19 Build building type
20 Build unit type
21 Build infantry type
22 Build aircraft type
23 Leaves map (team)
24 Zone entry by
25 Crosses horizontal line
26 Crosses vertical line
27 Global is set
28 Global is clear
29 Destroyed, Fakes, All
30 Low power
31 All bridges destroyed
32 Building exists

Descriptions of how these trigger events operate follows:

0 No Event
--------------
Used to denote that this trigger is never activated (there is no
event that will cause this to be activated).
It takes no parameters.
This is of use when you want to have a trigger that will be fired by
another trigger, but that you don't otherwise want fired.

1 Entered by
----------------
Used to have a trigger occur when a player moves a unit into the
cell, it is probably only useful in celltriggers.
The country is specified in the second parameter.

2 Spied by
--------------
This trigger must be attached to a structure for it to work. When a
spy infiltrates the structure, the trigger will be fired. It does not
appear to need a country associated with it; setting the second
parameter to -1 will still cause this trigger to be fired when the
player spies upon this building (as will setting the second parameter to
any other value).
Remember, some buildings can't normally be spied upon, but this can be
changed by setting Capturable=yes in the building's entry (see Changing
Red Alert Values for further information on this).
It doesn't seem to need any parameters.

3 Thieved by
----------------
Cannot seem to get it to work.

4 Discovered by player
--------------------------
This trigger must be attached to something (a structure or some type
of unit) for it to be activated. When the player first encounters this
unit/ structure, the trigger will be activated. Encountered means
getting a unit in close enough so that the unit/structure is revealed.
This cannot be associated with a specific country, as only the player
can fire this trigger. You don't have to specify the player's country,
nor does this event require any parameters.

5 House Discovered
----------------------
This trigger does not need to be associated with anything. It takes
one parameter (the second parameter), which is the number of the country
with which to associate this trigger. When the country specified by the
parameter is discovered, this trigger will fire. Only the player can
fire this trigger, as the visual range of the player and AI countries
are co-extensive.

6 Attacked by anybody
-------------------------
This trigger must be attached to something (a structure or some type
of unit) for it to be activated. When this unit/structure is attacked,
the trigger is fired. It does not matter which country does the
attacking.
It takes no parameters.

7 Destroyed by anybody
--------------------------
This trigger must be attached to something (structure or some type of
unit) for it to get activated. When the attached item is destroyed, by
any country, this trigger will activate.
It requires no parameters.

8 Any event
---------------
This trigger gets fired when any event at all is met. This may be
handy for setting mission start conditions, as it will always be fired
as soon as the mission begins.
It takes no parameters.

9 Destroyed, Units, All
---------------------------
This trigger gets fired when all the units of the specified country
are destroyed. Units included vehicles and infantry.
The country is specified in the second parameter.
Loaded LSTs (when they are not under control) are not included in this
check.

10 Destroyed, Buildings, All
-------------------------------
This trigger gets fired when all the structures of the specified
country have been destroyed. Please note that civilian structures are
not counted for this (ie V05 etc).
The country is specified in the second parameter.

11 Destroyed, All
--------------------
This trigger gets fired when all the units and structures of the
specified country have been destroyed. In essence, it is a combination
of events 9 and 10. Like event 10, civilian structures are not counted
for this (ie V05 etc).
The country is specified in the second parameter.

12 Credits exceed
--------------------
When the number of credits currently held exceeds the value in the
second parameter, this trigger is activated. The second parameter is
the _actual_ number of credits to be exceeded (eg. 5000).
The team for which the credits are tested against is held in
part 2 of the trigger.

13 Elapsed time (1/10th min)
-------------------------------
When the current time of the mission has passed the value in the
second parameter divided by 10, this trigger is activated.

14 Mission timer expired
---------------------------
This trigger gets fired when the global timer has reached zero. It
takes no parameters (so set them to -1).

15 Destroyed, Buildings, #
-----------------------------
This trigger gets fired when the specified number of buildings have
been destroyed. Unlike the Destroyed, All and Destroyed, Buildings, All
trigger events, civilian buildings are included in the count for this
event.
The second parameter holds the number of buildings that need to be
destroyed.
To specify which country's buildings we are talking about, you must
set part 2 of the trigger (Which country the trigger applies to) to the
appropriate country number.
The first parameter is not used (set it to -1).

16 Destroyed, Units, #
-------------------------
This trigger gets fired when the specified number of units have been
destroyed.
The second parameter holds the number of units that need to be
destroyed.
To specify which country's units we are talking about, you must set
part 2 of the trigger to the appropriate country number.
The first parameter is not used (set it to -1).

17 No factories left
-----------------------
When the specified country has no "factories" left, this trigger will
be fired. In Red Alert, a "factory" includes: construction yard (FACT),
air field (AFLD), barracks (BARR and TENT), and weapons factory (WEAP).
Helicopter pads (HPAD), dog kennels (KENN), ship yards (SYRD) and sub
pens (SPEN) are not counted as a "factory".
To specify which country's "factories" we are talking about, you must
set part 2 of the trigger to the appropriate country number.
This trigger event does not use any parameters, so set them to -1.

18 Civilians evacuated
-------------------------

19 Build building type
-------------------------
The trigger is activated when the specified building is constructed.
For the list of available buildings in Red Alert and their associated
numbers, see Available Red Alert Buildings. Note that constructed means
placed on the map, not just purchased but not placed.
The building number is placed in the second parameter.

20 Build unit type
---------------------
The trigger is activated when the specified vehicle is constructed.
Ships are not considered to be a vehicle by Red Alert (indeed, there is
no way to have a trigger fire on the construction of a ship type). For
the list of available vehicle types and their associated numbers,
see Available Red Alert Vehicles.
The unit number is placed in the second parameter.

21 Build infantry type
-------------------------
The trigger is activated when the specified infantry unit is
constructed.
The attack dog is treated as an infantry type by Red Alert. For the
list of available infantry types in Red Alert and the numbers associated
with them, see Available Red Alert Infantry Units
The infantry number is placed in the second parameter.

22 Build aircraft type
-------------------------
The trigger is activated when the specified aircraft is constructed.
For the list of available aircraft types in Red Alert and their
associated numbers, see Available Red Alert Aircraft.
Note that the use of the spy plane, parabombs or paradrop by the
player will not cause this trigger to be activated, as this isn't seen
to be building the aircraft by Red Alert.
The aircraft number is placed in the second parameter.

23 Leaves map (team)
-----------------------
The trigger is activated when the specified teamtype leaves the map.
A teamtype can be programmed to leave the map by having a Move action
that specifies a destination that is off the mission map.
The first parameter takes the number of the teamtype that is set to
leave the map. Remember that teamtype numbering starts from 0.

24 Zone entry by
-------------------
Another trigger that seems to only be usable in celltriggers. When
the "zone" of the cell to which this trigger action is attached is
entered, the trigger gets fired.
The second parameter takes the number of the country which will
activate the trigger when it enters the "zone".
The real question becomes (for this trigger event and the trigger
action Reveal zone of waypoint): what is the "zone"? See the What is
the Zone of a cell? section for an explanation of the "zone".

25 Crosses horizontal line
-----------------------------
Cannot seem to get it to work. Have tried passing waypoints and
absolute cells as parameters, but nothing works. This is not used
in any of the original Red Alert missions.

26 Crosses vertical line
---------------------------
Cannot seem to get it to work. Have tried passing waypoints and
absolute cells as parameters, but nothing works. This is not used in
any of the original Red Alert missions.

27 Global is set
-------------------
The trigger is activated when the specified global value is in the
'set' position.
The second parameter holds the number of the global value to test
against.

28 Global is clear
---------------------
The trigger is activated when the specified global value is in the
'clear' position.
The second parameter holds the number of the global value to test
against.

29 Destroyed, Fakes, All
---------------------------
Cannot get it to work correctly - it always seems to be fired straight
away. This is not used by Westwood in their missions.

30 Low power
---------------
This trigger is fired when the specified country is low on power.
The country to test for low power is specified in the second
parameter.

31 All bridges destroyed
---------------------------
This trigger is fired when all of the bridges on the map have been
destroyed. Naturally, indestructible land bridges are not counted for
this event, only those concrete bridges that can be damaged and
destroyed.
This event does not require any parameters.

32 Building exists
---------------------
This trigger is fired is a particular building is currently on the
map, for a particular country.
The second parameter holds the building number (see Available Red
Alert Buildings for this list).
Part 2 of the trigger holds the country number.


[4-13-3] Available Trigger Actions
===================================
The following are the available trigger actions in Red Alert:

Action Text
#'s Version
------------------------
0 No action
1 Winner is
2 Loser is
3 Production begins
4 Create team
5 Destroy team
6 All to hunt
7 Reinforcement (team)
8 Drop zone flare (waypoint)
9 Fire sale
10 Play movie
11 Text trigger (ID number)
12 Destroy trigger
13 Autocreate begins
15 Allow win
16 Reveal all map
17 Reveal around waypoint
18 Reveal zone of waypoint
19 Play sound effect
20 Play music theme
21 Play speech
22 Force trigger
23 Timer start
24 Timer stop
25 Timer extend (1/10th min)
26 Timer shorten (1/10th min)
27 Timer set (1/10th min)
28 Global set
29 Global clear
30 Auto base building
31 Grow shroud one 'step'
32 Destroy attached building
33 Add 1-time special weapon
34 Add repeating special weapon
35 Preferred target
36 Launch nukes

There is no trigger action number 14.

Descriptions of how these trigger action work, and what they do follows:

0 No action
---------------
No action is associated with this trigger. This is usually used when
you don't want a secondary trigger.

1 Winner is
---------------
The associated country wins the mission. If this country is not the
player's country, then the player will lose if this trigger is fired.
The third parameter holds the country number.

2 Loser is
--------------
The associated country loses the mission. If this country is not the
player's country, then the player will win the mission if this
trigger is fired. However, this also causes the game to crash (at least
in some cases). Only associate the player's country with this action.
The third parameter holds the country number.

3 Production begins
-----------------------
The specified country is able to start production of units and
buildings. If the country does not have production turned on, it cannot
create anything, even if another trigger tells it to. Production cannot
be turned off once it has been turned on. At the beginning of each
mission, production is turned off. Even if "auto-base building" has
been triggered, the country still needs a production trigger before it
can begin producing anything.
The third parameter takes the number of the country.

4 Create team
-----------------
When activated, the country owning the specified teamtype will attempt
to construct the specified teamtype. If it does not have the required
buildings (war factory/barracks) this construction will fail. The
computer player is not required to have the prerequisite buildings
that the human player must have (ie it can build mammoth tanks without
having a service depot build), nor is it limited to what that country
would normally be able to build. The USSR could build light tanks and
mobile gap generators if the teamtype called for it, as England could
produce mammoth tanks.
When creating a team, the computer country will first look around
the map to see if there is currently a unit on the map of the specified
type that is not currently in a teamtype. If there is such a unit, it
will be used as part of the team being created. This includes units
that you place around the map at the beginning of the mission, unless
they have particular starting actions (such as Sticky, Sleep etc).
The computer will always build additional units after it has created
the teamtype. This is usually limited to one of each type of unit in
the teamtype, although occasionally two extra infantry units get
produced.
Note that computer players with high IQ levels will automatically
create units for themselves that are not specified in teamtypes, nor
which are called to be produced by Create Team commands.
The first parameter takes the number of the teamtype that is to be
created.

5 Destroy team
------------------
When activated, the specified teamtype is destroyed, logically. This
means that the units in the specified teamtype no longer perform the
actions of the teamtype, and the computer can use them when creating
new teamtypes. The units in the team will complete the action they were
engaged in when destroyed, and once that action has been completed will
just stay where they were located when the teamtype was destroyed,
presumably in guard mode. All the instances of a particular teamtype
will be destroyed when this trigger action is fired.
The first parameter takes the number of the teamtype to destroy.
Remember, the numbering of teamtypes starts at zero.

6 All to hunt
-----------------
When this trigger action is fired, all of the units of the specified
country are set to the action Hunt. This causes those units to seek out
their enemies and destroy them.
The third parameter holds the country number that should be set to
hunt.

7 Reinforcement (team)
--------------------------
This brings in the specified teamtype to the specified waypoint.
The first parameter holds the teamtype to be used as the
reinforcements. Remember, the first occurrence in the [teamtype]
section is numbered 0, not numbered 1.
If the teamtype includes a transport helicopter (probably also an APC
or LST), then you can specify the waypoint at which to drop them off by
using the third parameter.
See the section 'How to get units appearing out of buildings' on how
to do as the title suggests.

8 Drop zone flare (waypoint)
--------------------------------
This drops a green flare at the specified waypoint, and reveals a
small section of the map around that point. The area revealed is
significantly smaller than that revealed by trigger event 17.
The third parameter takes the waypoint at which to drop the flare.

9 Fire sale
---------------
This has the associated country sell off all of their structures. It
takes as its third parameter the country number that is to sell off
its buildings.
Please note that it is possible to have the player's buildings sold in
this way.
It is only the third parameter that determines which country sells
their buildings, part 2 of the trigger has no effect.

10 Play movie
----------------
This has Red Alert play the specified movie as soon as the trigger is
activated. Be aware that sounds from the mission can persist into the
first few moments of the movie, as they are not stopped (so if you get
reinforcements and play a movie because of it, the "Reinforcements have
arrived" sound will persist into the start of the movie.
See Available Red Alert Movies for the complete listing of movies
available.
The number of the movie to be shown is stored in the third parameter.
If the third parameter holds a movie number that does not exist on the
cdrom that is currently in the drive, then all that will happen is that
the screen will quickly flash to black, and return normally.

11 Text trigger (ID number)
------------------------------
Displays a short text message in the upper left corner of the screen.
The text itself is stored in the tutorial.ini file (see Tutorial.ini).
The third parameter holds the text ID number.

12 Destroy trigger
---------------------
The specified trigger is destroyed. This is especially useful if you
want to have a trigger repeat until some action occurs that will halt
that trigger.
The second parameter holds the number of the trigger to destroy
(remember, trigger numbering starts from 0).

13 Autocreate begins
-----------------------
The specified country has its autocreation ability turned on. The use
of autocreate is tricky, and is controlled through the various teamtypes
used.
The third parameter takes the number of the country for which to turn
on autocreation.

15 Allow win
---------------

16 Reveal all map
--------------------
Reveals the entire map when the trigger is fired.
It takes no parameters.

17 Reveal around waypoint
----------------------------
Reveals the area around the specified waypoint. The area revealed
around the specified waypoint seems to be quite large.
The third parameter holds the waypoint.

18 Reveal zone of waypoint
-----------------------------
Reveals the area that is considered to be the "zone" of the specified
waypoint. See What is the Zone of a cell? for a discussion on what
makes up the "zone".
The third parameter holds the waypoint.

19 Play sound effect
-----------------------
Plays the specified sound effect. See Available Red Alert Sound
Effects for a listing of the available sound effects.
The third parameter holds the sound effect number.

20 Play music theme
----------------------
This does not seem to work.

21 Play speech
-----------------
Plays the specified piece of speech. See Available Red Alert Speeches
for a listing of the available speeches.
The third parameter holds the speech number.

22 Force trigger
-------------------
The specified trigger is fired. The trigger that is pointed to
usually has both trigger events set to 0 (no event) so that it cannot
otherwise be triggered, but this does not have to be the case.
The second parameter holds the trigger number. Remember, the first
trigger in the [Trigs] section is number 0, the second number 1, etc.
A destroyed trigger may still be forced.

23 Timer start
-----------------
The global mission timer is started (the timer is shown).
It takes no parameters (set them to -1).

24 Timer stop
----------------
The global mission timer is stopped (the timer is no longer shown).
It takes no parameters (set them to -1).

25 Timer extend (1/10th min)
-------------------------------
The global mission timer has its duration extended by the specified
duration. The duration specified is in tenths of a minute (ie 60 would
extend the timer by 1 minute, etc).
The third parameter takes the duration to add to the global mission
timer.

26 Timer shorten (1/10th min)
--------------------------------
The global mission timer has its duration decreased by the specified
duration. The duration specified is in tenths of a minute (ie 600 would
shorten the timer by 10 minutes, etc).
The third parameter takes the time to remove from the global mission
timer.

27 Timer set (1/10th min)
----------------------------
This sets the global timer to the specified time, and begins the
count-down immediately.
The third parameter takes the time to set it to, in tenths of a
minute, eg 60 will set the timer to 6 minutes, 600 to 60 minutes, etc.

28 Global set
----------------
The specified global value is placed in the 'set' position.
The third parameter takes the number of the global value to place in
the 'set' position.

29 Global clear
------------------
The specified global value is placed in the 'clear' position.
The third parameter takes the number of the global value to place in
the 'clear' position.

30 Auto base building
------------------------
Having this as a trigger action essentially puts that computer player
into 'skirmish' mode. The computer player will begin to build any new
buildings and units that it feels it ought to have. Given a large
enough supply of money, it will eventually build massive amounts of
units and structures, the result of which is to bring the game to an
incredibly painful level of play. The computer player will not be
limited to constructing structures specified in the [Base] section, nor
building units contained in teamtypes.
The third parameter holds the number of the country you want to put
into this mode.

31 Grow shroud one 'step'
----------------------------
The shroud is increased by one cell all around its border. It takes
no parameters (set them all to -1).

32 Destroy attached building
-------------------------------
All buildings that have this trigger attached to them explode. It
takes no parameters (set them all to -1).

33 Add 1-time special weapon
-------------------------------
This is used to give the specified country access to one of the
special weapons, the list of which is available in the section Red Alert
Special Weapons.
Please note that the country still has to wait for the charge-up
period to pass before they are able to use this special weapon.
The third parameter is used to specify which of the special weapons to
give the team.
You specify which team gets this special weapon through Part 2 of the
trigger.

34 Add repeating special weapon
----------------------------------
This seems not to work. It brings up the sidebar as if it were adding
something to it, but nothing new appears there.

35 Preferred target
----------------------
The third parameter takes the number of the country to use as the
preferred target.
I am unsure of whether this makes any difference, however as I
haven't tested this out yet.

36 Launch nukes
------------------
Contrary to what you might think, this does not cause the computer
players to launch A-Bombs, at least not in the way you would normally
want. When this trigger is fired, all Missile Silos on the map will
open up and fire an A-Bomb (this includes those Missile Silos that are
owned by the human). When these A-Bombs are launched, you get the
normal voice warning about this occuring, but the A-Bombs never land,
and hence do no damage to anything.
When this is action is activated, the A-Bombs will be launched without
thought to whether the country owning the Missile Silo actually has
waited the necessary time to construct the missile. This means that you
could, for example, have this happen every five seconds if you wanted to
annoy the human palyer that much. Having an A-bomb launched this way
does not reset the countdown timer (at least for the human player).
This action takes no parameters (set them all to -1).


[4-14] [TeamType] Section
==========================
Teamtypes are used to tell the computer player what units they should
be building, and how they should be constructing those units. Each
teamtype contains a list of units and a list of commands to carry out,
but also a number of variables, each of which alters the behaviour of
that teamtype, whether it be how the teamtype is created, or how it
behaves after it has been created.
It is these additional behavioural modifiers that make it rather
tricky to completely determine a teamtype's behaviour. There is a lot
more interdependency between these variables than there was in the
original C&C.

An example of a [TeamType] entry is:
satk2=2,1,15,0,1,-1,-1,2,E1:1,E2:1,4,16:13,0:8,0:2,0:1

The form for [TeamType] entries is:
tname=1,2,3,4,5,6,7,8,AA,9,BB

Each section of the teamtype entry is described below:

tname
-----
This is just a name for the teamtype, so that you can know what they
are. It can be any combination of alphanumeric letters and symbols,
except spaces.

1 (country)
-----------
This holds the numeric value of the country that owns this teamtype.
See Available Red Alert Countries for the list of country numbers.

2 (remain hidden, control autocreate)
-------------------------------------
This value is probably one of the hardest items to understand
completely.

This variable seemingly controls both autocreation of the team, and
also whether or not the teamtype will attempt to avoid visible areas
on the map (at least for the actions: Move to waypoint, Attack at
waypoint, and Patrol to waypoint).
When this item is set to an odd value, the teamtype will display the
skirting behaviour.
When this item is set to an even value (0 is counted as even), the
teamtype will not display the skirting behaviour.

Here is a more thorough description of the skirting behaviour:
When set to an odd value, the units in this teamtype will attempt to
stay out of the player's sight. The units will skirt around the visible
areas of the map on the way to their location. This is not 100%
perfect, as the units do not always stay within the black areas of the
map, but they do attempt to stay as close to this boundary as possible.
This works with the following actions: Move to waypoint, Attack at
waypoint and Patrol to waypoint.
If the entire map has been revealed (or maybe even a significant
proportion of it), then the units in the teamtype seem to use the
visual radius of the buildings, rather than the revealed area when
determining which route to take. The teamtype will always attempt to
take the shortest route to their destination, which means that if they
have to cross a revealed area of map, it will do so.
When set to an even value, the units make no attempt to hide, and just
barge straight towards their destination, not caring that the player
will be able to see them.

This value also has another function relating to controlling the
autocreation of the team. If part 5 of the teamtype is a positive
number, autocreation will occur, but it is this value that determines
what type of autocreation takes place.
Depending on this value, turning Autocreate on (using a trigger) has
different effects. The first thing you must know is that the values
that this item occur in groups of 4. The first set of numbers is
{0,1,2,3} while the second set is the set {4,5,6,7}. If you have a
number greater than 7, you determine the set that the number will be
included in by taking that number modulo 8 (ie x mod 8); this will give
you a number in the range zero to seven. So, having this value set to
11 is just the same as having it set to 3. There doesn't seem to be any
reason to use values outside of those within the two sets.

In the following two cases, we assume that part 5 of the teamtype has
a value greater than 0.
When this number is in the set {0,1,2,3} the following behaviour
occurs. As soon as the country owning this teamtype has had its
Production turned on, this teamtype will begin to be produced. If an
instance of this teamtype is destroyed, then it will be created again,
ad infinitum. This continuous production seems to take precedence over
all other types of production.
This continuous production is halted when that country has had its
Autocreation turned on. The teamtype will not be created by the use of
autocreation, although other instances of it may be created through
Create Team commands.

When this number is in the set {4,5,6,7}, the following behaviour
occurs. This teamtype will not be created until both Production and
Autocreation have been turned on. As soon as autocreation is turned on
(and providing that Production has been turned on), this teamtype will
begin to be created, but the creation rate will be left to the
autocreation function to decide. The rate of production is lower than
the continuous production model above.

If the number is within the second set (ie in {4,5,6,7}), then
something additional happens in addition to the teamtype being created
by the autocreate function. No matter which of the four values is used
in this set, the units in this teamtype will automatically repeat the
set of actions that they have been given. This repetition of the set of
actions the teamtype has is not the same as if they were being
explicitly told to repeat the actions. In the case of being explicitly
told to repeat the actions, this occurs almost the instant the last
action has been completed. When they have not been explicitly told and
are relying on this value to get them to repeat, then it seems as though
the teamtype will only begin to repeat the actions after they have been
standing around idle for a random amount of time.
In addition to this repetition of the set of actions, an additional
instance of this teamtype will be created and sent onto the field. This
is an additional teamtype above and beyond the number specified in part
5 of the teamtype. When this additional teamtype has been created, the
other instances of this teamtype will begin to loop their action, except
for one of them. This lonely instance will set in the battlefield doing
nothing. It appears as though the additional instance of the teamtype
takes the place of an existing teamtype.
All four values in the second set produce this behaviour. This
behaviour does not occur when using values from the first set of
numbers.

3 (??unknown??)
----------------------------
Don't know what this does.

4 (unknown)
-----------

5 (maximum number of instances of the teamtype)
-----------------------------------------------
This number, along with part 2 of the teamtype determine whether or
not a teamtype will be subject to autocreation or not. If this value is
0, then the teamtype will not be subject to autocreation. If this value
is non-zero then the teamtype will be subject to autocreation.
If this number is non-zero, the number actually controls how many
instances of that teamtype can be on the battlefield at the same time.
If set to 10, for example, then at most ten instances of that teamtype
will be on the field at the one time, and each time one of those ten
instances is destroyed, a new instance will be created to replace it
(provided the computer player has the cash, of course).

6 (waypoint for team appearance)
--------------------------------
If you are using this team in a Reinforcement trigger, then this holds
the waypoint at which you want the team to appear. You must make sure
that the waypoint you specify here is included in the [Waypoints]
section, otherwise Red Alert will crash (badly).
Set this to -1 if you are not going to use it.

7 (trigger to attach)
---------------------
This value holds the trigger that you want to attach to the teamtype.
If you do not wish to attach a trigger to the teamtype, set this number
to -1. Remember, numbering of triggers starts at 0.
This is useful when you want an action to occur when a teamtype is
attacked or destroyed, for example, although more complicated manoeuvers
are possible.

8 (how many different unit types there are)
-------------------------------------------
This number tells the parser how many different types of units to
expect in this TeamType entry (in section AA).

AA (list of units in the team)
------------------------------
This is a comma-delimited list of the units that will make up this
team. There must be as many entries in this list as was specified in
part 8 of the TeamType. Each entry in this list has the form X:Y where
X is the abbreviated version of the unit, and Y is the number of units
of that type.
For the abbreviations of the units, see sections: Available Red Alert
Vehicles, Available Red Alert Infantry, Available Red Alert Aircraft,
and Available Red Alert Ships.
Each team can be made up of a collection of infantry, vehicles,
aircraft and ships. Trucks will not combine with other types in a team.

9 (how many commands this team has)
-----------------------------------
This number tells the parser how many commands this team is being
assigned (in section BB).

BB (list of commands to the team)
---------------------------------
This is a comma-delimited list of the actions that this team will be
asked to perform. There must be as many entries in this list as was
specified in part 9 of the TeamType. Each entry in this list has the
form X:Y, where X is the number of the action to perform, and Y is the
value passed to this action.
For the available actions that can be performed by the team, see
the section Available Team Actions. This will also tell you what form
the Y value must take.


[4-14-1] Available TeamType Actions
====================================
These are the available actions that teams in the [TeamTypes] section
can perform:

#'s Short Description
----------------------
0 Attack
1 Attack Waypoint
2 Change Formation to
3 Move to waypoint
4 Move to cell
5 Guard area (1/10th min)
6 Jump to line #
7 Attack Tarcom
8 Unload
9 Deploy
10 Follow friendlies
11 Do this
12 Set global
13 Invulnerable
14 Load onto transport
15 Spy on building @ waypoint
16 Patrol to waypoint

These are discussed in more detail now:

0 Attack
-----------
The units in the teamtype will go and attack the specified country.
If the country does not exist on the map (they have all been destroyed,
for example), then the units will just sit around. Unlike the original
C&C attack command, there is no way to tell the teamtype to attack for a
certain period of time before doing something else.
The value passed to this action is the number of the country to attack
(see Available Red Alert Countries for the numbers of specific
countries).

1 Attack Waypoint
--------------------
The units in the team will go and attack the specified waypoint. If
the unit has the Infiltrate ability, then it will attempt to enter the
building. This will happen even if the country owning the units in this
teamtype owns the building at the waypoint.
If the unit has the C4 ability, it will blow up the building at the
specified waypoint.
The value passed to this action is the waypoint at which you want the
teamtype to attack.
If there is no building at the specified waypoint, the teamtype will
not activate correctly (usually they will just sit in their last
position).

2 Change Formation to
------------------------
When given this command, the units in this teamtype will attempt to
change formations to the one specified. See Available Unit Formations
for the listing of formations and their appropriate numbering.
WARNING: changing formations does not appear to work as it should.
Please read the description of this problem in Available Unit Formations
and make sure that you only use Change Formation when you are positive
that you have managed to get it to work correctly, all the time.

3 Move to waypoint
---------------------
The units in the team are to move towards the specified waypoint.
They do not stop to engage in combat on the way to the waypoint, but do
seem willing to snipe at enemies on the way to the waypoint.
The value passed to this action is the waypoint to which the team
is to move.

4 Move to cell
-----------------
The units in the teamtype will move towards the specified cell. Why
you would want to use this over Move to waypoint beats me, but I would
guess that there are some occasions where you may want to specify an
absolute cell.
The value passed to this action is the cell to which the teamtype is
to move towards.

5 Guard area (1/10th min)
----------------------------
The units in the team will stay where they are and be on the look-out
for enemy units that come near them. If an enemy unit comes into their
guard range, they will go and intercept the enemy.
The value passed to this action is the number of time units you want
them to be on guard for (in steps of one tenth of a minute).

6 Jump to line #
-------------------
You use this to get repeating actions for the teamtype. The parameter
passed is the action number of the teamtype that you want to jump to.
The first action of a teamtype is numbered 0, the second 1, etc. If you
jump to number 0, you get the teamtype repeating all the commands it
has, looping forever (good for setting up patrol routes). You don't
have to repeat all the action, of course, you could, for example, skip
to action number 2, which would ignore the first two action commands,
and just go from the third.

7 Attack Tarcom
------------------

8 Unload
-----------
If the team contains units that are currently being stored in a
transport of some type (TRAN, APC, LST etc), then passing the team
this command will make the units inside the transport disembark.
It is not passed a value, so set that to 0.
If the teamtype contains a minelayer, the unload command will cause
the minelayer to lay down a mine at its current position.

9 Deploy
-----------
If the unit in the team is an MCV, sending it this command will cause
it to deploy itself into a construction yard at its present location.
It is not passed a value, so set that to 0.

10 Follow friendlies
----------------------
The unit(s) in this team will follow the nearest friendly unit to it
when that friendly unit starts to move. This following doesn't appear
to be permanent.
It is not passed a value, so set that to 0.

11 Do this
------------
The units in the team will perform the following actions. Not all of
these work, and some are made obsolete by other teamtype action
commands. They are actually the same commands as a units can be given
when being placed on the map. See Available Initial Unit Commands for
the listing of the numbering of the possible values you can use here.

12 Set global
---------------
The specified global variable is placed into the 'set' position. Pass
this command the number of the global variable that you wish to set.

13 Invulnerable
-----------------
The units in this teamtype have the Iron Curtain cast on them. As
long as the country that owns these units has an Iron Curtain, it does
not seem to matter whether there is one unit or five units in the
teamtype; all will have the Iron Curtain cast on them (normal rules
about what can be IC'd still apply).
This means that the side does not have to wait for the Iron Curtain to
recharge like the player must.
It is not passed a value, so set that to 0.

14 Load onto transport
------------------------
If there is a transport unit (such as an APC etc), then infantry
units in this teamtype will attempt to load onto that transport. The
infantry units travel to the transport unit, not the other way around.
If the transport unit is something like an LST, then vehicles will do
the same thing (travel to the transport and load).
It is not passed a value, so set that to 0.
I have not been able to get a teamtype to load onto a transport,
unload somewhere, and then load again. If the teamtype was given a Move
command after the teamtype unloaded, only the transport moved, which
suggests that the infantry units (or vehicle units for an LST) are no
longer considered to be part of the same teamtype.

15 Spy on building @ waypoint
-------------------------------

16 Patrol to waypoint
-----------------------
Similar to Move to waypoint, it takes as its parameter the waypoint to
patrol to. It differs from the Move command in that the units in the
teamtype will move out of their patrol route to actively go and engage
enemy units and buildings that are within their patrol range as they
move to the waypoint.
WARNING: Having the teamtype patrol to a waypoint takes up
considerable processing power, as it scans for enemy units with each
step it takes. If you have more than 1 or 2 teamtypes doing this action
at the same time, it will introduce some jerkiness to Red Alert (on a
P166). If you have a lot of teamtypes performing patrols to waypoint at
the same time, Red Alert will crawl.


[4-15] [MapPack] Section
=========================
This section of the ini file contains the information about the full
map for your mission. It is encoded in base64, but the as the terrain
editor created this section for you, there is not that much to know.


[4-16] [OverlayPack] Section
===========================
Overlays are those sections of the map that are placed on top of the
map, such as gold and gems and walls. I assume that it is also encoded
in base 64. The terrain editor takes care of this section as well.


[4-17] [Digest] Section
======================
This appears to be some form of checksum for the file when it is saved
in the terrain editor. If you edit a file with a [Digest] section, them
Red Alert will pop up an error saying the scenario may be corrupt, but
otherwise behave normally. It is best to delete the [Digest] section.

-------------------
CHAPTER [5] Tables
-------------------

[5-1] Available Red Alert Movies
=================================
These are the names and numbers of all the video clips in RA. The
movie numbers are placed in the third parameter of the trigger action):

Movie Plays on Plays on
Names #'s Soviet Allies Descriptions
--------------------------------------------------
AAGUN 0 yes yes anti-aircraft guns firing at yaks
while barracks get strafed
MIG 1 yes no MIG flying along and shooting tank
SFROZEN 2 yes no dead (Soviet) soldier in bunker in
snow
AIRFIELD 3 yes no yak moving out of hanger onto
airstrip with lots of other yaks
BATTLE 4 no yes destroyed tanks, jeeps etc on field
(ends with tank exploding)
BMAP 5 yes yes dagger falling onto map of Europe,
filling it red (Soviet win video)
BOMBRUN 6 yes no bombing run by badger bomber onto
building
DPTHCHRG 7 yes no depth charge attack on sub
GRVESTNE 8 no yes gravestone of Tanya
MONTPASS 9 no yes convoy of 3 trucks
MTNKFACT 10 yes no construction of heavy/mammoth tank
CRONTEST 11 no yes chronosphere in action (expanding
blue field engulfs units)
OILDRUM 12 no yes looking through binoculars into
base, tank fires shell into barrel
that explodes
ALLYEND 13 no yes allied ending (Stalin found but left
buried)
RADRRAID 14 yes no 2 tanks attacking radar dome and
pillboxes
SHIPYARD 15 no no ****NOT ON EITHER DISK****
SHORBOMB 16 no yes cruiser tactical display and then
bombing shore target
SITDUCK 17 yes no sub attacking cruiser (2 torpedo hits)
SLNTSRVC 18 yes no sub glides past, along ocean floor
SNOWBASE 19 no no ****NOT ON EITHER DISK****
EXECUTE 20 yes no firing squad kills person in snow
REDINTRO 21 yes yes Red Alert's intro movie sequence
NUKESTOK 22 yes no mushroom cloud from A-bomb
V2ROCKET 23 yes no 2 V2 rockets being launched off ledge
SEARCH 24 yes no search lights being trained on
prison complex
BINOC 25 no yes man with binoculars looking at
heavy tanks travelling along road
ELEVATOR 26 no yes soviet lift going down (or up)
FROZEN 27 no yes dead (Allied) soldier in bunker
MCV 28 no yes MCV is snow (stops moving but
doesn't deploy)
SHIPSINK 29 no yes helicopter over water going to
damaged and sinking cruiser
SOVMCV 30 yes no MCV in snow (stops moving but
doesn't deploy)
TRINITY 31 no yes Eiffel Tower in foreground of
nuclear strike
ALLYMORF 32 yes yes morph into Allied symbol (Allied
win animation)
APCESCPE 33 no yes APC running away from burning base
BRDGTILT 34 no yes bridge over a river (snow)
CRONFAIL 35 yes yes chronosphere blowing up while trying
to activate
STRAFE 36 yes no yak strafing jeeps as they cross a
bridge
DESTROYR 37 no yes boats travelling up river (snow)
DOUBLE 38 yes no 2 MCV's travelling across grass field
FLARE 39 yes yes person signalling with flare, then
planes fly overhead (snow)
SNSTRAFE 40 yes no yak making strafing row on people
in village; teddy bear is dropped
LANDING 41 yes yes soviet tech. centre with 2 tesla coils
out front, transport helicopter
lands (snow)
ONTHPRWL 42 yes no sub moving along ocean floor
OVERRUN 43 no yes 2 soldiers in foxhole, they run out
just before tank runs over that
foxhole
SNOWBOMB 44 yes yes cruiser firing at base and hitting it
SOVCEMET 45 yes no gravestone with R.I.P on it
TAKE_OFF 46 yes no transport helicopter lifting off
TESLA 47 yes no tesla coil zapping medium tank
SOVIET8 48 yes no soviet briefing
SPOTTER 49 yes no binocular view of 3 soldiers
ALLY1 50 yes yes allied briefing
ALLY2 51 no yes allied briefing
ALLY4 52 no yes allied briefing
SOVFINAL 53 yes no soviet end video - Kane is the future!
ASSESS 54 no yes man in snow with binoculars watching
base; focuses on Iron Curtain
SOVIET10 55 yes no soviet briefing
DUD 56 no yes bird on nuclear missile that didn't
explode (in London?)
MCV_LAND 57 no yes helicopter landing in snow next to
truck
MCVBRDGE 58 yes no MCV moving across bridge
PERISCOP 59 yes no sub targeting cruiser through
periscope, and launching a torpedo
at it
SHORBOM1 60 no yes cruiser tactical display (see 16,
but it doesn't attack afterwards)
SHORBOM2 61 no yes cruiser pounding shore base
SOVBATL 62 yes no destroyed heavy tanks, APCs,
helicopters, with helicopters
flying overhead
SOVTSTAR 63 yes yes soviet star (Soviet win animation)
AFTRMATH 64 no yes binocular view of destroyed base;
focuses on destroyed Iron Curtain
(see 54)
SOVIET11 65 yes no soviet briefing
MASASSLT 66 no yes view of city, then tanks come
rolling in, followed by
helicopters (city is Soviet)
ENGLISH 67 **no** no ****NOT ON EITHER DISK****
SOVIET1 68 yes yes soviet briefing
SOVIET2 69 yes no soviet briefing
SOVIET3 70 yes no soviet briefing
SOVIET4 71 yes no soviet briefing
SOVIET5 72 yes no soviet briefing
SOVIET6 73 yes no soviet briefing
SOVIET7 74 yes no soviet briefing
PROLOG 75 yes yes Einstein travelling back in time
to get Hitler
AVERTED 76 yes no computer room with 'meltdown
averted' message
COUNTDWN 77 yes no computer room with 'meltdown
imminent' message
MOVINGIN 78 yes no convoy of 3 trucks
ALLY10 79 no yes allied briefing
ALLY12 80 no yes allied briefing
ALLY5 81 no yes allied briefing
ALLY6 82 no yes allied briefing
ALLY8 83 no yes allied briefing
TANYA1 84 no yes Tanya about to be interrogated
(with needle)
TANYA2 85 no yes Tanya getting rescued (shooting guy)
ALLY10B 86 no yes allied briefing
ALLY11 87 no yes allied briefing
ALLY14 88 no yes allied briefing
ALLY9 89 no yes allied briefing
SPY 90 no yes Russian guard getting mugged by spy
TOOFAR 91 no yes bridge being blown up by commandos
in dingy
SOVIET12 92 yes no soviet briefing
SOVIET13 93 yes no soviet briefing
SOVIET9 94 yes no soviet briefing
BEACHEAD 95 yes no turret on beach attacking tanks as
they come out of an LST; pans out
to ocean where more LST wait
SOVIET14 96 yes no soviet briefing
SIZZLE 97 yes yes Land of Lore 2 preview
SIZZLE2 98 yes yes Bladerunner preview

There are 3 videos that are on neither cdrom: SNOWBASE, SHIPYARD, and
ENGLISH.
SNOWBASE and SHIPYARD perform as other videos do when the wrong cdrom
is in the driver, but ENGLISH causes Red Alert to crash (at least the
Windows 95 version) when played from the Soviet cdrom (at least from
the Play Movie trigger).
It is likely for foreign language versions of Red Alert that the
ENGLISH video will have some other name.

When a movie is specified with the Play Movie trigger and it does not
exist on the cdrom that is currently in the drive, there will be a brief
flash of black (if black can be considered to be a 'flashable' colour),
then the mission will resume. The exception is the ENGLISH movie, which
crashes on the Soviet disk. Do not specify a movie name/number that is
not on the current disk.


[5-2] Available Red Alert Songs
================================
The following songs are available in Red Alert:

BIGF226M Bigfoot
CRUS226M Crush
FAC1226M Face the Enemy 1
FAC2226M Face the Enemy 2
HELL226M Hell March
RUN1226M Run For Your Life
SMSH226M Smash
TREN226M Trenches
WORK226M Workmen
DENSE_R Dense
FOGGER1A Fogger
MUD1A Mud
RADIO2 Radio 2
ROLLOUT Roll Out
SNAKE Snake
TERMINAT Terminate
TWIN Twin
VERTOR1A Vector
MAP Map Selection theme
SCORE Score screen theme
INTRO Intro theme
CREDITS End Credits theme

Note that the song "AWAIT" mentioned in the rules.ini file in the
ThemeControl section does not actually exist.
I am unable to get these to play using the hypothetical Play music
theme trigger action, but would guess that, if it worked, the numbering
would start at 0 for Bigfoot, 1 for Crush, etc.


[5-3] Available Red Alert Speeches
===================================
For trigger action 21, the following are the spoken events (the speech
number is placed in the third parameter of the trigger action):

Abbrev. #'s What is said
---------------------------------
MISNWON1 0 "Mission accomplished"
MISNLST1 1 "Mission failed"
PROGRES1 2 "Unable to comply, building in progress"
CONSCMP1 3 "Construction complete"
UNITRDY1 4 "Unit ready"
NEWOPT1 5 "New construction options"
NODEPLY1 6 "Cannot deploy here"
STRCKIL1 7 "Structure destroyed"
NOPOWR1 8 "Insufficient power"
NOFUNDS1 9 "Insufficient funds"
BCT1 10 "Battle control terminated"
REINFOR1 11 "Reinforcements have arrived"
CANCLD1 12 "Cancelled"
ABLDGIN1 13 "Building"
LOPOWER1 14 "Low power"
NOFUNDS1 15 "Insufficient funds"
BASEATK1 16 "Our base is under attack"
NOBUILD1 17 "Unable to build more"
PRIBLDG1 18 "Primary building selected
none 19 (nothing)
none 20 (nothing)
UNITLST1 21 "Unit lost"
SLCTTGT1 22 "Select target"
ENMYAPP1 23 "Enemy approaching"
SILOND1 24 "Silos needed"
ONHOLD1 25 "On hold"
REPAIR1 26 "Repaired" (may be "repairing")
none 27 (nothing)
none 28 (nothing)
AUNITL1 29 "Airborne unit lost"
none 30 (nothing)
AAPPRO1 31 "Allied forces approaching"
AARRIVE1 32 "Allied reinforcements have arrived"
none 33 (nothing)
none 34 (nothing)
BLDGINF1 35 "Building infiltrated"
CHROCHR1 36 "Chronosphere charging"
CHRORDY1 37 "Chronosphere ready"
CHROYES1 38 "Chronosphere test successful"
CMDCNTR1 39 "Command Centre under attack"
CNTLDED1 40 "Control Centre deactivated"
CONVYAP1 41 "Convoy approaching"
CONVLST1 42 "Convoy unit lost"
XPLOPLC1 43 "Explosive charge placed"
CREDIT1 44 "Credits stolen"
NAVYLST1 45 "Naval unit lost"
SATLNCH1 46 "Satellite launched"
PULSE1 47 "Sonar pulse available"
none 48 (nothing)
SOVFAPP1 49 "Soviet forces approaching"
SOVREIN1 50 "Soviet reinforcements have arrived"
TRAIN1 51 "Training"
AREADY1 52 "A-bomb ready"
ALAUNCH1 53 "A-bomb launch detected"
AARRIVN1 54 "Allied reinforcements have arrived from the north"
AARRIVS1 55 "Allied reinforcements have arrived from the south"
AARIVE1 56 "Allied reinforcements have arrived from the east"
AARRIVW1 57 "Allied reinforcements have arrived from the west"
1OBJMET1 58 "First objective met"
2OBJMET1 59 "Second objective met"
3OBJMET1 60 "Third objective met"
IRONCHG1 61 "Iron Curtain charging"
IRONRDY1 62 "Iron Curtain ready"
KOSYRES1 63 "Kosygin rescued"
OBJNMET1 64 "Objective not met"
FLAREN1 65 "Signal flare detected from the north"
FLARES1 66 "Signal flare detected from the south"
FLAREE1 67 "Signal flare detected from the east"
FLAREW1 68 "Signal flare detected from the west"
SPYPLN1 69 "Spy plane ready"
TANYAF1 70 "Tanya freed"
ARMORUP1 71 "Unit armour upgraded"
FIREPO1 72 "Unit firepower upgraded"
UNITSPD1 73 "Unit speed upgraded"
MTIMEIN1 74 "Mission timer initialised"
UNITFUL1 75 "Unit full"
UNITREP1 76 "Unit repaired"
40MINR 77 "Forty minutes remaining"
30MINR 78 "Thirty minutes remaining"
20MINR 79 "Twenty minutes remaining"
10MINR 80 "Ten minutes remaining"
5MINR 81 "Warning, five minutes remaining"
4MINR 82 "Warning, four minutes remaining"
3MINR 83 "Warning, three minutes remaining"
2MINR 84 "Warning, two minutes remaining"
1MINR 85 "Warning, one minute remaining"
TIMERNO1 86 "Timer stopped"
UNITSLD1 87 "Unit sold"
TIMERGO1 88 "Timer started"
TARGRES1 89 "Target rescued"
TARGFRE1 90 "Target freed"
TANYAR1 91 "Tanya rescued"
STRUSLD1 92 "Structure sold"
SOVFORC1 93 "Soviet forces have fallen"
SOVEMP1 94 "Soviet empire selected"
SOVEFAL1 95 "Soviet empire has fallen"
OPTERM1 96 "Operation terminated"
OBJRCH1 97 "Objective reached"
OBJNRCH1 98 "Objective not reached"
OBJMET1 99 "Objective met"
MERCR1 100 "Mercenary rescued"
MERCF1 101 "Mercenary freed"
KOSYFRE1 102 "Kosygin freed"
FLARE1 103 "Signal flare detected"
COMNDOR1 104 "Commando rescued"
COMNDOF1 105 "Commando freed"
BLDGPRG1 106 "Building in progress"
ATPREP1 107 "Atom bomb prepping"
ASELECT1 108 "Allied forces selected"
APREP1 109 "A-bomb prepping"
ATLNCH1 110 "Atom bomb launch detected"
AFALLEN1 111 "Allied forces have fallen"
AAVAIL1 112 "A-bomb available"
AARRIVE1 113 "Allied reinforcements have arrived"
SAVE1 114 "Mission saved"
LOAD1 115 "Mission loaded"


[5-4] Available Red Alert Sound Effects
========================================
These are the sound effects available for trigger action 19 (the sound
effect number is placed in the third parameter of the trigger action):

Abbrev. #'s Type of sound effect
---------------------------------------------
GIRLOKAY 0 Girl's voice: "Ok"
GIRLYEAH 1 Girl's voice "Yeah?"
GUYOKAY1 2 Guy's voice: "Ok"
GUYYEAH1 3 Guy's voice: "Yeah?"
MINELAY1 4 (mine laying sound? couldn't hear anything)
ACKNO 5 Russian voice: "Acknowledged"
AFFIRM1 6 Military voice: "Affirmative"
AWAIT1 7 Military voice: "Awaiting orders"
EAFFIRM1 8 Engineer's voice: "Affirmative"
EENGIN1 9 Engineer's voice: "Engineering"
NOPROB 10 "Of course" (Einstein's voice?)
READY 11 Military voice: "Ready and waiting"
REPORT1 12 Military voice: "Reporting"
RITAWAY 13 Military voice: "At once"
ROGER 14 Military voice: "Agreed"
UGOTIT 15 Military voice: "Very well"
VEHIC1 16 (didn't hear anything)
YESSIR1 17 Military voice: "Yes sir?"
DEDMAN1 18 Man's death sound
DEDMAN2 19 Man's death sound
DEDMAN3 20 Man's death sound
DEDMAN4 21 Man's death sound
DEDMAN5 22 Man's death sound
DEDMAN6 23 Man's death sound
DEDMAN7 24 Man's death sound
DEDMAN8 25 Man's death sound
DEDMAN10 26 Man's death sound
CHRONO2 27 Sound of chronosphere being fired
CANNON1 28 Cannon shot
CANNON2 29 Cannon shot (tinier than #28)
IRONCUR9 30 Iron Curtain being fired
EMOVOUT1 31 Engineer's voice: "Moving out"
SONPULSE 32 Sonar pulse sound
SANDBAG2 33 Sandbag being squashed
MINEBLO1 34 Mine's 'ping' sound
CHUTE1 35 Sound of torpedo being launched?
DOGY1 36 Dog's bark
DOGW5 37 Dog's whine
DOGG5P 38 Dog's growl
FIREBL3 39 Fireball sound (or something very similar)
FIRETRT1 40 Another fire sound?
GRENADE1 41 Sound of grenade being thrown?
GUN11 42 Machine gun sound (5 quick shots)
GUN13 43 Machine gun sound (8 or 9 very quick shots)
EYESSIR1 44 Engineer's voice: "Yes sir"
GUN27 45 Single gun shot
HEAL2 46 Medic's healing sound
HYDROD1 47 don't know (sound a bit like a steam press)
INVUL2 48 don't know
KABOOM1 49 An explosion
KABOOM12 50 An explosion
KABOOM15 51 An explosion
SPLASH9 52 Object falling into water
KABOOM22 53 Really large explosion
AACANON3 54 Sound of AAGun firing?
TANDETH1 55 Tanya death sound
MGUNINF1 56 Machine gun sound (6 or 7 quick shots)
MISSILE1 57 SAM missile firing
MISSILE6 58 missile firing sound
MISSILE7 59 missile firing sound (V2 rocket?)
x 60 (nothing)
PILLBOX1 61 sound of pillbox firing (machine gun sound)
RABEEP1 62 a beep
RAMENU1 63 a very short beep
SILENCER 64 single sniper shot
TANK5 65 cannon shot (very loud)
TANK6 66 cruiser firing sound (or may be artillery sound)
TORPEDO1 67 torpedo being launched
TURRET1 68 turret gun firing sound
TSLACHG2 69 tesla coil charging up
TESLA1 70 tesla coil firing
SQUISHY2 71 something getting squashed
SCOLDY1 72 very short beep
RADARON2 73 sound of radar coming on
RADARDN1 74 sound of radar going off
PLACBLDG 75 sound of building being placed
KABOOM30 76 an explosion
KABOOM25 77 an explosion
x 78 (nothing)
DOGW7 79 dog's whine
DOGW3PX 80 dog's growl
CRMBLE2 81 sound of something falling down/crumbling down
CASHUP1 82 short bleep
CASHDN1 83 short bleep
BUILD5 84 construction sounds
BLEEP9 85 long bleep sound
BLEEP6 86 bleep sound
BLEEP5 87 bleep sound
BLEEP17 88 bleep sound
BLEEP13 89 bleep sound
BLEEP12 90 bleep sound
BLEEP11 91 bleep sound
H2OBOMB2 92 big explosion (A-bomb going off?)
CASHTURN 93 sound of something being sold
TUFFGUY1 94 Tanya: "Chew on this"
ROKROLL1 95 Tanya: "Let's rock"
LAUGH1 96 Tanya laughing
CMON1 97 Tanya: "Shake it baby"
BOMBIT1 98 Tanya: "Cha-ching!"
GOTIT1 99 Tanya: "That's all you got?"
KEEPEM1 100 Tanya: "Kiss it bye-bye"
ONIT1 101 Tanya: "I'm there"
LEFTY1 102 Tanya: "Give it to me"
YEAH1 103 Tanya: "Yeah?"
YES1 104 Tanya: "Yes sir"
YO1 105 Tanya: "What's up?"
WALLKIL2 106 something (concrete wall being destroyed?)
x 107 (nothing)
GUN5 108 single cannon shot
SUBSHOW1 109 submarine 'decloaking'
EINAH1 110 Einstein: "Ya?"
EINOK1 111 Einstein: "Incredible"
EINYES1 112 Einstein: "Yes"
MINE1 113 explosion
SCOMND1 114 spy: "Commander"
SYESSIR1 115 spy: "Yes sir"
SINDEED1 116 spy: "Indeed"
SONWAY1 117 spy: "On my way"
SKING1 118 spy: "For king and country"
MRESPON1 119 medic: "Medic reporting"
MYESSIR1 120 medic: "Yes sir"
MAFFIRM1 121 medic: "Affirmative"
MMOVOUT1 122 medic: "Moving out"
BEEPSLCT 123 a bleep (deepish in pitch)
SYEAH1 124 thief: "Yeah?"
x 125 (nothing)
x 126 (nothing)
SMOUT1 127 thief: "Moving out"
SOKAY1 128 thief: "Ok"
x 129 (nothing)
SWHAT1 130 thief: "What?"
SAFFIRM1 131 thief: "Affirmative"


[5-5] Available Red Alert Countries
====================================
The following countries are available in Red Alert:

Abbrev. Name Number Colour
-----------------------------------
SPN Spain 0 Yellow/gold
GRE Greece 1 Blue-grey
RED USSR 2 Red
ENG England 3 Green
UKA Ukraine 4 Orange
GER Germany 5 Khaki/light brown
FRA France 6 Aqua
TRK Turkey 7 Red-Ochre
GDI GoodGuy 8 Blue-grey
NOD BadGuy 9 Red
CIV Neutral 10 Yellow/gold
JP Special ?11? Yellow/gold
MP1 Multi1 12 Yellow/gold
MP2 Multi2 13 Blue-grey
MP3 Multi3 14 Red
MP4 Multi4 15 Green
MP5 Multi5 16 Orange
MP6 Multi6 17 Khaki/light brown
MP7 Multi7 18 Aqua
MP8 Multi8 19 Red-Ochre

Naturally, these colours are as they appear on my screen. Your
perception of them may differ.


[5-6] Available Red Alert Buildings
====================================
The following buildings are available in Red Alert (although not all
of them can be built):

#'s Abbrev. Name Has Icon
-------------------------------------------------
0 ATEK Allied Technology Centre yes
1 IRON Iron Curtain yes
2 WEAP Weapons Factory yes
3 PDOX Chronosphere yes
4 PBOX Pillbox yes
5 HBOX Camouflaged Pillbox yes
6 DOME Radar Dome yes
7 GAP Gap Generator yes
8 GUN Gun Turret yes
9 AGUN Anti-Aircraft Gun yes
10 FTUR Flame Turret yes
11 FACT Construction Yard yes
12 PROC Ore Refinery yes
13 SILO Ore Silo yes
14 HPAD Helicopter Pad yes
15 SAM SAM Site yes
16 AFLD Airfield yes
17 POWR Power Plant yes
18 APWR Advanced Power Plant yes
19 STEK Soviet Technology Centre yes
20 HOSP Hospital no
21 BARR Barracks (Allied) yes
22 TENT Barracks (Soviet) yes
23 KENN Dog Kennel yes
24 FIX Service Depot yes
25 BIO Bio-Research Laboratory no
26 MISS Technology Centre/Prison no
27 SYRD Ship Yard yes
28 SPEN Sub Pen yes
29 MSLO Missile Silo yes
30 FCOM Forward Command Post no
31 TSLA Tesla Coil yes
32 WEAF Fake Weapons Factory yes
33 FACF Fake Construction Yard yes
34 SYRF Fake Ship Yard yes
35 SPEF Fake Sub Pen no
36 DOMF Fake Radar Dome yes
x SBAG Sandbag yes
x CYCL Chain-link fence no
x BRIK Concrete wall yes
x BARB Barbed-wire fence no
x WOOD Wooden fence no
x FENC Barbed wire (the normal type) yes
43 MINV Anti-vehicle mine no
44 MINP Anti-personnel mine no
x V01 Church no
x V02 Han's and Gretel's no
x V03 Hewitt's Manor no
x V04 Ricktor's House no
x V05 Gretchin's House no
x V06 The Barn no
x V07 Damon's Pub no
x V08 Fran's House no
x V09 Music Factory no
x V10 Toymaker's no
x V11 Ludwig's House no
x V12 Haystacks no
x V13 Haystack no
x V14 Wheat Field no
x V15 Fallow Field no
x V16 Corn Field no
x V17 Celery Field no
x V18 Potato Field no
x V19 Oil Pump no
x *V20 **NO DESCRIPTION** no
x *V21 Abdul's House no
x *V22 Pablo's Wicked Pub no
x *V23 Village Well no
x *V24 **NO DESCRIPTION** no
x *V25 Church no
x *V26 Ali's House no
x *V27 Trader Ted's no
x *V28 Menelik's House no
x *V29 Prestor John's House no
x *V30 Village Well no
x *V31 Witch Doctor's House no
x *V32 Rikitikitembo's Hut no
x *V33 Roarke's Hut no
x *V34 Musaba's Hut no
x *V35 Aksum's Hut no
x *V36 Mambo's Hut no
x *V37 The Studio no
x BARL (single barrel) no
x BRL3 (cluster of 3 barrels) no

While MINV and MINP do cause the trigger to be activated if they are
made buildable, placing a bought mine causes the construction yard to
go berserk and stops the further placement of any other buildings.
Those structures that have an 'x' where their number should be do not
activate the Build Building type trigger.
Any structure without an icon that is made buildable will get a
'hall-of-mirrors' icon when displayed. This means that their icon will
be made up of bits of graphics from whatever was last displayed in
that section of the screen.
The civilian structures marked with a * (V20 to V37) do not have any
graphics displayed on either the SNOW or TEMPERATE theatres. In the
original Command and Conquer, they appeared only in the DESERT theatre,
which was not included in Red Alert. They are a left-over from C&C.
The civilian structure V20 and V24 not only have no description
associated with them, but they also are not selectable.
The two types of barrel and mines are not selectable.


[5-7] Available Red Alert Infantry Units
=========================================
The following infantry units are in Red Alert (note that the attack
dog is treated as an infantry unit by Red Alert):

#'s Abbrev. Name Has Icon
---------------------------------------------
0 E1 Rifle Infantry Yes
1 E2 Grenadier Yes
2 E3 Rocket Soldier Yes
3 E4 Flamethrower Yes
4 E6 Engineer Yes
5 E7 Tanya Yes
6 SPY Spy Yes
7 THF Thief Yes
8 MEDI Field Medic Yes
9 GNRL General No
10 DOG Attack Dog Yes
11 C1 Joe No
12 C2 Barry No
13 C3 Shelly No
14 C4 Maria No
15 C5 Karen No
16 C6 Steve No
17 C7 Phil No
18 C8 Dwight No
19 C9 Erik No
20 C10 Scientist No
21 EINSTEIN Prof. Einstein No
22 DELHPI Special 1 No
23 CHAN Special 2 No

The names of the civilian units are not normally visible, but can be
made visible be setting the NamesCivilians variable to yes in the
[General] section of the rules.ini file (or see the section Changing
Red Alert Values on how to do this for an individual mission).


[5-8] Available Red Alert Vehicles
===================================
The following vehicles are available in Red Alert (please note that
ships are not counted as vehicles):

#'s Abbrev. Name Has Icon
---------------------------------------------------
0 4TNK Mammoth Tank Yes
1 3TNK Heavy Tank Yes
2 2TNK Medium Tank Yes
3 1TNK Light Tank Yes
4 APC Armoured Personnel Carrier Yes
5 MNLY Mine Layer Yes
6 JEEP Ranger Yes
7 HARV Ore Truck Yes
8 ARTY Artillery Yes
9 MRJ Mobile Radar Jammer Yes
10 MGG Mobile Gap Generator Yes
11 MCV Mobile Construction Vehicle Yes
12 2VRL V2 Rocket Launcher Yes
13 TRUK Convoy Truck *Yes*

The convoy truck does have an icon, but it looks nothing like the unit
does in the game. It looks like the ranger's icon, except the rear part
of the ranger is exploding. This is only in the MS-DOS version of Red
Alert. The Window 95 version of Red Alert has a correct icon (the unit
on the icon actually looks like the convoy truck).


[5-9] Available Red Alert Aircraft
=================================
The following aircraft are available in Red Alert:

#'s Abbrev. Names Has Icon
------------------------------------------
0 TRAN Chinook Helicopter Yes
1 BADR Badger Bomber Yes
2 U2 Spy Plane Yes
3 MIG MIG Attack Plane Yes
4 YAK Yak Attack Plane Yes
5 HELI Longbow Helicopter Yes
6 HIND Hind Helicopter Yes

The Badger Bomber and Spy Planes, if made buyable by the player,
cannot be selected and hence cannot be moved off the airfield.


[5-10] Available Red Alert Ships
=================================
The following ships are available in Red Alert (they don't have any
numbers because they cannot be used in triggers):

Abbrev. Names Has Icon
------------------------------------------
SS Submarine Yes
DD Destroyer Yes
CA Cruiser Yes
LST Land-Sea Tank (transport) Yes
PT Gun Boat Yes


[5-11] Available Unit Formations
=================================
These appear to be the formations that teamtypes can form:

#'s Formation
--------------
0 None
1 Tight
2 Loose
3 Wedge North
4 Wedge East
5 Wedge South
6 Wedge West
7 Line N/S
8 Line E/W
9 North
10 East
11 South
12 West
13 Air

There is a problem with getting a teamtype to move into a formation
that you may want to consider before using them. When I tested these
numbers, using anything higher than 2 (Loose) would cause the teamtype
to freeze in that formation at the position on the map where they were
located. They would not continue with their actions.
Additionally, if there were different unit types (such as infantry and
vehicles) together in the teamtype and the teamtype was told to change
formation, it would halt as before (this time it would halt even when
changing to formation 1 or 2).
If you are able to get your teamtype to change formation correctly,
great. However, test it thoroughly to make sure that it continues its
orders.


[5-12] Available Red Alert Special Weapons
===========================================
These are the special weapons that are available in Red Alert that can
be delivered through the use of a 1-time special weapon trigger action.

#'s Name
-------------
0 Sonar Pulse
1 Nuclear Strike
2 Chrono-shift
3 Parabomb
4 Paratroopers
5 Spy Plane
6 Iron Curtain
7 **GPS**

A note on the GPS. While the icon appears as normal and it eventually
becomes active, the satellite will not automatically launch as it does
when the Allied tech. centre is built. If the icon is clicked upon, the
voice will say "Select target", but the cursor does not change into a
target cursor, and hence clicking on the map does not release the
satellite.


[5-13] Available Initial Unit Commands
=====================================
Each unit the appears on the map at the beginning of a mission has an
associated starting command. This command tells the unit what to do in
the time before it is given any orders by either the human player or
a computer player. The available commands are:

#'s Command
--------------
0 Sleep
1 Attack
2 Move
3 Qmove
4 Retreat
5 Guard
6 Sticky
7 Enter
8 Capture
9 Harvest
10 Area Guard
11 Return (unused)
12 Stop
13 Ambush (unused)
14 Hunt
15 Unload
16 Sabotage
17 Construction
18 Selling
19 Repair
20 Rescue
21 Missile
22 Harmless

Numbers 17, 18, 19 and 21 are undertaken by buildings only.
Not all of these commands actually have the unit/building do anything,
just like the original C&C.
The difference between Guard and Area Guard is that, in Area Guard,
the unit is much more vigorous in defending the area around it, and will
follow any units that come into its defending area. The following
behaviour lasts until it can attack its prey, whereupon the unit will
return to its original position (unless it caught up with the prey
within its initial guard zone, when it will attempt to destroy the
invader).


[5-14] Available Terrain Types
===============================
The following are the valid terrain features:

MINE ---} gold mine
BOXES01 ---}
BOXES02 } groups
BOXES03 } of
BOXES04 } boxes
BOXES05 ---}
ICE01 ---}
ICE02 }
ICE03 } ice
ICE04 } flows
ICE05 ---}
T01 ---}
T02 }
T03 }
T04 }
T05 }
T07 }
T07 } single
T08 } trees
T09 }
T10 }
T11 }
T12 }
T13 }
T14 }
T15 }
T16 }
T17 ---}
TC01 ---}
TC02 } clumps
TC03 } of
TC04 } trees
TC05 ---}

The terrain type MINE is the goldmine that is used to stimulate ore
regrowth.
The terrain types T01 to T17 are single trees.
The terrain types TC01 to TC05 are clumps of trees.
The terrain types ICE01 to ICE05 are clumps of ice. They cannot be
walked over, and their graphics make it look like they are meant to be
placed on water. Their graphics are only drawn when using the SNOW
theater (they seem to be totally discarded in the other theaters, as
the space where they are supposed to be can be walked over).

The ICE01 to ICE05 graphics are visible in the terrain editor, but
cannot be placed in the terrain editor. They have the following
dimensions:
ICE01 2x2
ICE02 2x1 (2 cells high)
ICE03 1x2 (2 cells wide)
ICE04 1x1
ICE05 1x1

The terrain types BOXES01 to BOXES05 are various groups of boxes that
are used in the interior missions. Their graphics are only drawn when
using the INTERIOR theater (they seem to be totally discarded in the
other theaters, as the space where they are supposed to be can be walked
over).


[5-15] Available Smudge Types
==============================
The following are the available smudge types:

CR1 ---}
CR2 }
CR3 } craters
CR4 }
CR5 }
CR6 ---}
SC1 ---}
SC2 }
SC3 } scorch
SC4 } marks
SC5 }
SC6 ---}
BIB1 ---}
BIB2 } dirt
BIB3 ---} patches

The smudge effects CR1 to CR6 are various types of small craters.
The smudge effects SC1 to SC6 are various types of scorch marks.
The smudge effects BIB1 to BIB3 are the patches of dirt that appear at
the base of most buildings (the light coloured dirt).

--------------------------
CHAPTER [6] Miscellaneous
--------------------------

[6-1] Tutorial.ini
===================
All of the short text pieces that are displayed during Red Alert
missions are stored in a text file called tutorial.ini. This file is
part of the main.mix file, but if you put a tutorial.ini file in your
Red Alert directory, it will override the one in the redalert.mix file.
I do not know if you would be able to add more items to the
tutorial.ini file, but wouldn't put money on it. You can certainly
change the text of the entries already present without any trouble. I
would keep the text that you want to display to a length of less than
that is specified in the file (41 characters it seems).
The text number is placed in the third parameter of the trigger
actions.

The original tutorial.ini file follows:

----cut here---- DO NOT INCLUDE THIS LINE!
[Tutorial]
1=Objective 1 Complete
2=Objective 2 Complete
3=Objective 3 Complete
4=Defend Command Center
5=Destroy all Allied units and structures
6=Destroy all Soviet units and structures
7=Build your base

;Specific text
;MAX is below! Don't exceed!
;X=XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

8=Find Einstein.
9=Get Einstein to the helicopter
10=Clear the way for the convoy
11=Time is running out!
12=Convoy approaching
13=Destroy all bridges
14=Get Spy into War Factory
15=Destroy all SAM sites
16=Get Tanya to the helicopter
17=Capture Radar Dome
18=Destroy Sub Pens
19=Keep the Chronosphere on-line
20=Restore full power
21=Get a spy into Command Center
22=Bring Kosygin back to your base
23=INCOMING TRANSMISSION
24=Capture the Command center!
25=Get engineers to control computers
26=Clear the naval channel
27=Capture all Tech. centers
28=Destroy the Iron Curtain
29=Use engineers to operate computers
30=Re-program all generator computers
31=Hangar turret powering up. Standby
32=Turret deactivated
33=Acquire money to build your base
34=Destroy civilian forces and town
35=Secure the middle island
36=Get the convoy across the map
37=Run for it!
38=Capture the other tech. centers
39=Don't approach the Chronosphere!
40=Kill the enemy spy
41=Disrupt Allied communications
42=Get trucks to other shore
43=Get engineers to coolant stations!
44=Use main terminal to shut down core
45=Meltdown Imminent!
46=Destroy convoy truck
47=Destroy Allied naval base
48=Destroy Radar domes
49=Capture the Chronosphere!
50=Get spy into enemy tech. center

;Death explanation text

51=Einstein was killed
52=Tanya was killed
53=Radar Dome was destroyed
54=Command Center destroyed
55=Chronosphere self-destructed
56=All Engineers killed
57=Spy escaped
58=Time ran out
59=Convoy destroyed
60=Spy killed
61=Kosygin killed
62=Einstein was in tech. center
63=Not enough available power

;misc

64=Charge placed on Generator
65=Find and Rescue captured Engineers
---cut here--- DO NOT INCLUDE THIS LINE!


[6-2] Mission.ini
==================
Each mission in Red Alert contains a brief text description of the
objective of the mission. These text descriptions are stored in a file
called mission.ini, which is stored in the main.mix file, but which can
be overridden if you place a file called mission.ini into your Red Alert
directory.
If you place a mission.ini file into your Red Alert directory, Red
Alert will use the mission briefings from this file rather than the
default ones found in the main.mix file.
If you are using the SkipMapSelect to add extra missions into the
original mission structure, then you can include the new missions'
briefings by adding sections into the mission.ini file. For example,
say you added a second level 1 Soviet mission (scu01eb) through the
use of SkipMapSelect. To get a briefing, you would add a [SCU01EB]
section to the mission.ini file and fill in the appropriate message.
I do not know the exact maximum length an entry can be.
You may notice the occurence of @'s in some of the briefings. These
are used to have the next bit of text start on the next line. It
appears to be the only piece of formatting available in the briefings
(@ is shift-2). Two @'s in a row will produce a blank line between two
sections of text.

The original mission.ini file follows:

---cut here--- DO NOT INCLUDE THIS LINE
[SCG01EA.INI]
1=Rescue Einstein from the Headquarters inside this Soviet complex. Once
2=found, evacuate him via the helicopter at the signal flare. Einstein and
3=Tanya must be kept alive at all costs. Beware the Soviet's Tesla Coils.
4=Direct Tanya to destroy the westmost power plants to take them off-line.

[SCG02EA.INI]
1=A critical supply convoy is due through this area in 25 minutes, but
2=Soviet forces have blocked the road in several places. Unless you can
3=clear them out, those supplies will never make it to the front. The
4=convoy will come from the northwest, and time is short so work quickly.

[SCG03EA.INI]
1=LANDCOM 16 HQS.@TOP SECRET.@TO: FIELD COMMANDER A9@@INTELLIGENCE
2=RECON SHOWS HEAVY SOVIET MOVEMENT IN YOUR AREA. NEARBY BRIDGES ARE
3=KEY TO SOVIET ADVANCEMENT. DESTROY ALL BRIDGES ASAP. TANYA WILL ASSIST.
4=KEEP HER ALIVE AT ALL COSTS.@@CONFIRMATION CODE 1612.@@TRANSMISSION ENDS.

[SCG03EB.INI]
1=LANDCOM 16 HQS.@TOP SECRET.@TO: FIELD COMMANDER A9@@INTELLIGENCE
2=RECON SHOWS HEAVY SOVIET MOVEMENT IN YOUR AREA. NEARBY BRIDGES ARE
3=KEY TO SOVIET ADVANCEMENT. DESTROY ALL BRIDGES ASAP. TANYA WILL ASSIST.
4=KEEP HER ALIVE AT ALL COSTS.@@CONFIRMATION CODE 1612.@@TRANSMISSION ENDS.

[SCG04EA.INI]
1=Soviet forces are trying to retake the pass you cleared for our convoys.
2=Don't let this happen. Hold the pass and prevent the Soviets from
3=taking this vital area. Destroy all Soviet units and buildings in
4=this region.

[SCG05EA.INI]
1=Rescue Tanya. Your spy can move past any enemy unit, except dogs,
2=without being detected. Direct him into the weapons factory located
3=at a nearby Soviet Base where he will hijack a truck and free Tanya.
4=With Tanya's help, take out the air defenses on the island and a Chinook
5=will arrive to rescue her. Then destroy all remaining Soviet buildings
6=and units.

[SCG05EB.INI]
1=Rescue Tanya. Your spy can move past any enemy unit, except dogs,
2=without being detected. Direct him into the weapons factory located
3=at a nearby Soviet Base where he will hijack a truck and free Tanya.
4=With Tanya's help, take out the air defenses on the island and a Chinook
5=will arrive to rescue her. Then destroy all remaining Soviet buildings
6=and units.

[SCG05EC.INI]
1=Rescue Tanya. Your spy can move past any enemy unit, except dogs,
2=without being detected. Direct him into the weapons factory located
3=at a nearby Soviet Base where he will hijack a truck and free Tanya.
4=With Tanya's help, take out the air defenses on the island and a Chinook
5=will arrive to rescue her. Then destroy all remaining Soviet buildings
6=and units.

[SCG06EA.INI]
1=Priority One is to establish a base and get your spy into one of the
2=Soviet tech. centers in the base across the gulf. Data on the Iron Curtain
3=is in there and we need it. Once you get the data complete your mission...
4=wipe out everything.

[SCG06EB.INI]
1=Priority One is to establish a base and get your spy into one of the
2=Soviet tech. centers in the base across the gulf. Data on the Iron Curtain
3=is in there and we need it. Once you get the data complete your mission...
4=wipe out everything.

[SCG07EA.INI]
1=LANDCOM 16 HQS.@TOP SECRET.@TO: FIELD COMMANDER A9@@INTERCEPTION OF SOVIET
2=COMMUNIQUE INDICATES THEIR IRON CURTAIN RESEARCH WAS SET BACK BY
3=ESPIONAGE. EXCELLENT WORK, COMMANDER!@@COMMUNIQUE WAS TRACED BACK TO
4=SECRET SOVIET BASE IN BORNHOLM. INVESTIGATE POSSIBLE CONNECTION WITH IRON
5=CURTAIN RESEARCH. CAPTURE RADAR CENTER AND DESTROY SUB PRODUCTION
6=CAPABILITY.@@CONFIRMATION CODE 1138.@@TRANSMISSION ENDS.

[SCG08EA.INI]
1=Our latest technology, the Chronosphere, is housed in this research
2=station. The timer represents the appointed time for the completion of a
3=vital experiment. The Soviets have learned of this and are moving in.
4=Protect the Chronosphere and the Advanced-Tech research center. Make sure
5=the base is fully powered at the appointed time. If not, all will be lost!

[SCG08EB.INI]
1=Our latest technology, the Chronosphere, is housed in this research
2=station. The timer represents the appointed time for the completion of a
3=vital experiment. The Soviets have learned of this and are moving in.
4=Protect the Chronosphere and the Advanced-Tech research center. Make sure
5=the base is fully powered at the appointed time. If not, all will be lost!

[SCG09EA.INI]
1=One of Stalin's top atomic strategists, Vladimir Kosygin, wishes to
2=defect. His knowledge of Stalin's atomic strategies is invaluable to us.
3=We wish to "extract" him from the Riga compound, where he is stationed.
4=@@Use a spy to infiltrate the Soviet command center and contact Kosygin.
5=Once he is out of the building, get him back to your base any way you
6=can.

[SCG09EB.INI]
1=One of Stalin's top atomic strategists, Vladimir Kosygin, wishes to
2=defect. His knowledge of Stalin's atomic strategies is invaluable to us.
3=We will extract him from the Riga compound where he is stationed.
4=@@Use a spy to infiltrate the Soviet command center and contact Kosygin.
5=Once he is out of the building, guide him back to your base any way you
6=can.

[SCG10EA.INI]
1=Kosygin has indicated that this is the site of Stalin's main atomic
2=weapons plant. Use extreme care in approaching the Soviet base --
3=we don't know if any atomic bombs are armed yet. Take the
4=facility off-line and then destroy any atomic weapons that exist.

[SCG10EB.INI]
1=Now that the complex has been infiltrated, the launch control centers must
2=be deactivated. Get your engineers to the control centers and deactivate
3=them before the missiles reach their targets.@@Enemy technicians can help
4=in locating the control centers if they are kept alive.

[SCG11EA.INI]
1=Our assault on the USSR is underway, although our efforts are being
2=hindered by large pockets of soviet armor. To counter this we need to
3=move warships up the Volga river, but there is a bottleneck near
4=Volograd which you must clear so our naval vessels can move in.
5=Good Luck.

[SCG11EB.INI]
1=Our assault on the USSR is underway, although our efforts are being
2=hindered by large pockets of soviet armor. To counter this we need to
3=move warships up the Volga river, but there is a bottleneck near
4=Volograd which you must clear so our naval vessels can move in.
5=Good Luck.

[SCG12EA.INI]
1=Rumors abound that the Soviet Iron Curtain is nearing completion. In
2=addition, an even more powerful version of that weapon is also in the
3=works. One research facility is more protected than the rest - find out
4=why. Capture all technology centers, and destroy any
5=Iron Curtain prototype that you encounter.@Our newly developed Longbow
6=Helicopter should be able to assist your attacks.

[SCG13EA.INI]
1=LANDCOM 16 HQS.@TOP SECRET.@TO: FIELD COMMANDER A9@@CONGRATULATIONS.
2=CAPTURING TECH CENTERS HAS REVEALED AN UNDERGROUND WEAPONS FACILITY.
3=PLACE EXPLOSIVE CHARGES ON ALL GENERATORS. RESULTING EXPLOSIONS SHOULD
4=DESTROY FACILITY.@GET OUT BEFORE NERVE GAS IS USED.@@TRANSMISSION ENDS.

[SCG14EA.INI]
1=This is it -- the final confrontation! The Soviets have nowhere to run
2=now. The only thing that remains is to topple the Soviet seat of power.
3=Destroy everything to make sure that no one takes Stalin's place.
4=No sorrow. No pity. No remorse.

[SCU01EA.INI]
1=A pitiful excuse for resistance has blockaded itself in this village.
2=Stalin has decided to make an example of them. Kill them all and destroy
3=their homes. You will have Yak aircraft to use in teaching these rebels
4=a lesson.

[SCU02EA.INI]
1=Tomorrow, the attack on Germany begins, but today, we must protect our
2=facility from Allied attacks. Keep the Command Center intact at all
3=costs, and destroy any Allied fortification you might find.

[SCU02EB.INI]
1=Tomorrow, the attack on Germany begins, but today, we must protect our
2=facility from Allied attacks. Keep the Command Center intact at all
3=costs, and destroy any Allied fortification you might find.

[SCU03EA.INI]
1=An Allied spy has bypassed our security, damaged our base, and is now
2=seeking to escape. Use your attack dogs to track him down and exterminate
3=him. The civilians are aiding the spy and will have set traps for your
4=men. If the spy escapes you, your life is forfeit.

[SCU04EA.INI]
1=The Allied base in this region is proving to be problematic. Your mission
2=is to take it out so that we can begin to move forces through this area.
3=As long as they have communications they will be able to call upon heavy
4=reinforcements. Crush their communications, and they should be easier to
5=remove.

[SCU04EB.INI]
1=The Allied base in this region is proving to be problematic. Your mission
2=is to take it out so that we can begin to move forces through this area.
3=As long as they have communications they will be able to call upon heavy
4=reinforcements. Crush their communications, and they should be easier to
5=remove.

[SCU05EA.INI]
1=Khalkis island contains a large quantity of ore that we need. The
2=Allies are well aware of our plans, and intend to establish their own
3=base there. See to it that they fail. In addition, capture their radar
4=center so we can track Allied activity in this area.

[SCU06EA.INI]
1=There is a special cargo that needs to be transported to a nearby
2=Soviet base in the northeast. Make sure the trucks reach their
3=destination intact. Along the way, there is a bridge which the Allies
4=may have destroyed. If so, use the Naval options at your disposal. Our
5=attack subs will make short work of any Allied boats you discover.

[SCU06EB.INI]
1=There is a special cargo that needs to be transported to a nearby
2=Soviet base in the northeast. Make sure the trucks reach their
3=destination intact. Along the way, there is a bridge which the Allies
4=may have destroyed. If so, use the Navy at your disposal. Our attack
5=subs will make short work of any Allied boats you discover.

[SCU07EA.INI]
1=The Allies have infiltrated one of our nuclear reactors! They
2=have tampered with the core so that a meltdown is imminent within
3=30 minutes. They must not succeed! Enter the base and find any remaining
4=technicians. Guide them to the 4 coolant stations so they can activate
5=them, then activate the main computer. The security systems have been
6=armed so beware. Kill any Allies you find.

[SCU08EA.INI]
1=We have detected Allied activity on Elba island. The Allies plan to use
2=this island to stage an attack on the Soviet Empire. You must ensure
3=that the island ceases to be under Allied control.@@Destroy all Allied
4=units on and around the island. The local population has been aiding the
5=Allies as well. There is only one punishment for helping the enemy - Death.

[SCU08EB.INI]
1=We have detected Allied activity on Elba island. The Allies plan to use
2=this island to stage an attack on the Soviet Empire. You must ensure
3=that the island ceases to be under Allied control.@@Destroy all Allied
4=units on and around the island. The local population has been aiding the
5=Allies as well. There is only one punishment for helping the enemy - Death.

[SCU09EA.INI]
1=The Allied forces have intercepted and destroyed a convoy that carried
2=parts for our secret weapon. One truck remains, but they have captured
3=that last truck and its cargo. This is not acceptable! You are to destroy
4=that truck before the Allies leave the area with it.

[SCU10EA.INI]
1=You must defend a Soviet convoy that is moving through Allied occupied
2=territory. Using the new MIG jet and a complement of Yaks, get the convoy
3=through the area intact.@@Be careful -- your resources for this mission
4=are very limited. If at least one truck makes it through to the other
5=side, the mission will be a success.

[SCU11EA.INI]
1=Intelligence indicates that a large portion of the Allied Naval Fleet
2=will stop for refueling at a base in this area. Destroy the fleet and the
3=base. Beware the long range of their cruisers.

[SCU11EB.INI]
1=Intelligence indicates that a large portion of the Allied Naval Fleet
2=will stop for refueling at a base in this area. Destroy the fleet and the
3=base. Beware the long range of their cruisers.

[SCU12EA.INI]
1=We have learned the location of the Chronosphere weapon, and we want to
2=capture it. @The Allies have boobytrapped the Chronosphere to explode
3=if approached. Capturing the tech. centers BEFORE taking the Chronosphere
4=may allow you to defuse any traps. Use extreme caution.

[SCU13EA.INI]
1=We have another chance to capture the Chronosphere. Take out the Radar
2=Domes to cut the link between them and the Chronosphere. Then capture it!

[SCU13EB.INI]
1=We have another chance to capture the Chronosphere. Take out the Radar
2=Domes to cut the link between them and the Chronosphere. Then capture it!

[SCU14EA.INI]
1=Your final test is at hand. The destiny of the Soviet union rests on the
2=shores of England. Here lies the final resting place of the Allies pitiful
3=resistance. Crush them and attain your place at the right hand of Stalin.
---cut here--- DO NOT INCLUDE THIS LINE!!!


[6-3] Red Alert Mission Tree
=============================
The original Red Alert missions had the following structure (we
present this mainly so you can use the SkipMapSelect variable without
too much of a hassle):

[6-3-1] Allied Missions
------------------------
level 1:
scg01ea
level 2:
scg02ea
level 3:
scg03ea
scg03eb
level 4:
scg04ea
level 5:
scg05ea
scg05eb
scg05ec
level 6:
scg06ea
scg06eb
level 7:
scg07ea
level 8:
scg08ea
scg08eb
level 9:
scg09ea
scg09eb
level 10:
scg10ea->scg10eb (in the original Red Alert missions, scg10eb starts
immediately after scg10ea is finished
- SkipMapSelect is set to yes)
level 11:
scg11ea
scg11eb
level 12:
scg12ea
level 13:
scg13ea
level 14:
scg14ea

[6-3-2] Soviet Missions
------------------------
level 1:
scu01ea
level 2:
scu02ea
scu02eb
level 3:
scu03ea
level 4:
scu04ea
scu04eb
level 5:
scu05ea
level 6:
scu06ea
scu06eb
level 7:
scu07ea
level 8:
scu08ea
scu08eb
level 9:
scu09ea
level 10:
scu10ea
level 11:
scu11ea
scu11eb
level 12:
scu12ea
level 13:
scu13ea
level 14:
scu14ea

WARNING: if you use SkipMapSelect to add a new mission to the original
mission structure, you should make sure that the user understands the
following: if the user takes a savegame of the additional mission and
tries to restart it after they have removed your .ini file, Red Alert
will give the error "Unable to read scenario", and crash. If you are
putting in additional missions using SkipMapSelect, make sure the user
understands that, once they have gotten rid of your missions, that they
will only be able to load that savegame, not restart it.

======================
-SECTION THREE- THEORY
======================

-----------------------------
CHAPTER [7] From The Lectern
-----------------------------

'From the Lectern' is a section intended to bring you some theory
about how to use aspects of Red Alert that may not, at first glance,
appear obvious to the reader. These are not meant to be step-by-step
guides in what you do to have your mission perform action X, but rather
to introduce your mind to some concepts that utilise the knowledge of
this guide in forms that go beyond the simplistic creation of units and
firing of triggers. At least, that is the hope.

[7-1] Contributing to the Lectern
==================================
If you wish to contribute to 'From the Lectern', please email one of
the authors, at either "bu...@adam.com.au" or "cfh...@msn.com" with the
subject of 'For the Lectern'. Include both a short description of what
you are going to describe so that we can determine whether to include it
or not, and also the spell-checked text of your 'From the Lectern'
entry. Include your name and email address, or just name if you don't
want to release your email address, so we can give the correct
attributions.

Try to be as detailed as possible in your submissions. If you need to
refer to parts of external files such as the rules.ini file or a .mpr or
.ini file, do not include all of it. Just include those parts that are
directly referenced in your article. Articles that include massive
amounts of superfluous material will be subject to editing.


[7-2] How to get units appearing out of buildings
==================================================
You may have noticed that in some original Red Alert missions, that
units would run out of buildings. Here is the method to do just that.
If you are using transports to bring units onto the battlefield as
reinforcements, the usual reinforcements trigger looks something like:
blah,7,5,-1,20,blah
where 5 is the teamtype being reinforced, and 20 is the waypoint where
they are going to be dropped off.
However, if you want the units to appear from buildings, then your
trigger would look like this:
blah,7,5,-1,-1,blah
Now all you have to do is to make two further changes, both of which
are very easy. The first is to make an entry in the [Waypoints] section
of the cell in which you want the units to appear. The second is to
change the sixth teamtype value of this team to hold the new waypoint
number.
For example, if I wanted a team to appear at cell 8919, I might set
waypoint 11=8919, so the sixth number in that teamtype would be 11.
That's all, your team will now appear to be coming out of a building.

I haven't managed to get the teamtype to appear out of nowhere; it
seems as though the presence of the building at the spot you want them
to appear from is a requirement.


[7-3] Changing Red Alert Values
================================
When you load up Red Alert, it can look in a file called 'rules.ini'
to read in the values for just about everything in the game. However,
to make changes to these values by using the rules.ini file, you must
restart Red Alert to get them to take effect.
However, you can also place this information into your mission's ini
file, and each time the mission is started, these values will be read
from the mission's ini file and used. Be aware, however, that the
values you set in the mission's ini file do not carry over from one
mission to the next.
This is useful if you only want to make a few small changes, which you
can just add in for a single mission, and have Red Alert revert to the
original values for the other missions. All you have to do is add the
title of the section you want to change (eg [JEEP]), and then the
sections that you want to be altered for this mission.
For example, the following:
[JEEP]
Primary=FireballLauncher
will make all jeeps in that particular mission be armed with the flame
turret's weapon instead of the usual machine gun.
It seems as though you can include any of the sections in the
rules.ini file in a mission's ini file without problems. Be aware,
however, that each time a mission in started or restarted, that the
*entire* mission's ini file is read and decoded. For this reason, you
should only include those pieces of the rules.ini file that you want to
change. Don't do the following if you just want to change the jeep's
weapon:
[JEEP]
Prerequisite=weap
Primary=FireballLauncher
Strength=150
Armor=light
TechLevel=3
Sight=6
Speed=10
Owner=allies
Cost=600
Points=20
ROT=10
Crewed=yes
While there is no noticeable change in the loading time of the
mission if you include even the entire rules.ini file into your
mission's ini file, trying to work out what you changed becomes
impossible. Feel free to include as much of the rules.ini as you want,
but this is one case where I prefer the minimalist approach.


[7-4] How to control where reinforcements come from
====================================================
You have already seen how to get reinforcement teamtype appearing from
buildings, now we will discuss how to control the direction from which
teamtypes come from when you are reinforcing them from off screen. If
you simply set the waypoint at which the reinforcement is to appear as
some location on the map (that is not covered by a building), then the
teamtype will appear from the edge of the map that is closest to their
destination. However, if you want them to appear from some other
section of the map edge, then you have to do a little bit more work.
The first thing you have to do is create a waypoint that is not on the
mission map. This waypoint should be in the row or column of cells that
is immediately outside of the mission map (ie say the mission map
started 34 cells from the left edge of the full map, the waypoint you
will use will be in the 33rd column of the full map). You can do this
easily by changing the X or Y value in the [Map] section by 1, loading
the map in the terrain editor, and determining the waypoint. When you
have determined the cell number that you want to use as a waypoint,
change the X or Y value back to its original value, and enter your new
waypoint. This new waypoint will be where the reinforcements will be
created, and from where they will make their way to their destination
waypoint.


[7-5] How to get units to enter buildings
==========================================
A number of infantry units have the ability to enter buildings
(thieves, engineers, Tanya etc), and these will enter buildings of their
own accord when given the order to attack. This allows them to enter
buildings that the player (or computer player) builds, the positions of
which you don't know at the time of creating the mission. But what if
you want something to happen to a particular building that exists on the
map at the beginning of the mission (or the position of which you know
because it will be built through the [Base] section)?
To get unit to enter a specific building, you give them the Attack at
waypoint command, specifying the waypoint that the anchor cell of the
building is located. If the infantry unit has the Infiltrate ability,
it will attempt to infiltrate that building. Be aware, however, that if
the specified building is an enemy building and the unit sent to
infiltrate it has a weapon, that it will use this weapon to attack the
building, rather than try and enter it.
You can, of course, have infantry units enter buildings that they
already own. This can be used to good effect to give the mission a more
dynamic feeling, if you feel that such would be necessary. You could,
for example, give some civilian units the Infiltrate ability and have
them walk in and out of buildings.
Spies, of course, should be given the Spy at waypoint command rather
than Attack at waypoint.


[7-6] Discussion on IQ Levels
==============================
Unlike the original C&C, Red Alert introduces some basic intelligence
to the computer players. This makes creating a computer opponent for a
single player mission both easier and more difficult than creating one
for C&C. More difficult because in C&C you controlled every single
aspect of the computer players. You can achieve this level of control
by setting the IQ level of the computer players to 0, but this means you
aren't able to use some of the features that IQ levels provide.
However, if you give the computer player a high level of IQ, then it
will begin to perform actions other than those that you are telling it
to perform. This lack of control makes fine tuning missions a
challenge. Setting a high IQ also means that you are able to get a
mission off the ground quicker, but my own personal preference is to
avoid doing this (although your view may differ).

One of the good features of the rules.ini file (and the fact that you
are able to include pieces of it in your mission's ini file is that you
are able to change what each of the IQ levels does. Here is the
original [IQ] entry in the rules.ini file, comments and all:

; ******* IQ setting for computer activity *******
; Each player (computer controlled or otherwise) is given an IQ rating that is
used
; to control what the computer is allowed to automatically control. This is
; distinct from the difficulty setting. The higher the IQ setting, the more
autonomous
; and intelligent the side will behave. Each ability is given a rating that
; indicates the IQ level (or above) that the ability will be granted. Because
such
; abilities are automatically performed by the computer, giving a human
controlled
; country a high IQ is not recommended. Otherwise the player's units will
start to
; automatically "do their own thing"! A human controlled country is presumed
to have
; an IQ rating of zero. A computer controlled country has an IQ of 1 or
higher.
; When in skirmish mode or when multiplayer AIs are active, the computer IQ is
set to
; the maximum.
[IQ]
MaxIQLevels=5 ; the maximum number of discrete IQ levels
SuperWeapons=4 ; super weapons are automatically fired by computer
Production=5 ; building/unit production is automatically controlled by
computer
GuardArea=4 ; newly produced units start in guard area mode
RepairSell=1 ; allowed to choose repair or sell of damaged buildings
AutoCrush=2 ; automatically try to crush antogonists if possible
Scatter=3 ; will scatter from incoming threats [grenades and such]
ContentScan=4 ; will consider contents of transport when picking good
target
Aircraft=4 ; automatically replace aircraft or helicopters
Harvester=2 ; automatically replace lost harvesters
SellBack=2 ; allowed to sell buildings

As you can see, there are a number of items that you can use. For me,
the most useful seem to be the ones to automatically replace lost units.
The Production variable I see as more a curse than a blessing, as you
lose complete control over what the computer will produce - you may as
well be playing a game of skirmish at that level. Remember that you can
change these values in your ini file, so you may want to, for example,
change Aircraft to have an IQ level of 2.

An area that high IQ levels may come in handy is when the computer
player is given access to various 'super weapons'. Instead of having to
program a specific trigger to fire the weapon (eg. firing a nuclear
missile), you would be able to supply them with enough intelligence to
fire it at their own discretion. Far be it from me to be cynical enough
to suggest that this form of intelligence may take the form of firing
the weapon as soon as it was available.


[7-7] On the use of Badger Bombers
===================================
First, a note of warning: you cannot drop vehicles via the Badger
bomber. If you attempt to, Red Alert crashes.

There are two uses for Badger bombers: reinforcing infantry units via
parachute drops, and to drop parachute bomblets. Both of these uses
will be discussed in this section.

It does not appear that the ability to specify a waypoint in the
reinforcement trigger action is utilised when dealing with Badger
bombers. You can either leave it to Red Alert to determine from which
direction the bomber will come from, or you can use part 6 of the
teamtype to specify the waypoint at which you wish them to appear.
Remember, this waypoint should be outside of the mission map. This is
not 100% perfect however, but the bomber will appear within one or two
cells of the waypoint you specified (once it comes onto the map).
If you leave it up to Red Alert to determine where the bomber will
come in from, then you can use the sixth part of the teamtype to
determine where the bomber will drop its payload (whether it be infantry
units or bomblets). In this case, Red Alert will choose the edge
closest to the drop point, and make a bee-line to its target. If you do
leave it up to Red Alert to determine where to come from, then you do
not give the teamtype any actions. So, your teamtype would look like:
reinf=2,0,7,0,0,10,-1,2,E1:5,BADR:1,0
(ie, the drop point will be waypoint 10, which is on the mission map;
Red Alert is left to determine where the plane comes from).
However, if you specify a waypoint off the mission map in the sixth
part of the teamtype, then you need to give the teamtype a command, in
this case, an Attack at waypoint command. Thus, your teamtype would
look like:
reinf=2,0,7,0,0,10,-1,2,E1:5,BADR:1,1,1:20
(ie. the drop point will be waypoint 20, and the bomber should come from
waypoint 10, which is off the mission map).
Unfortunately, the Move to waypoint and Move to cell commands do not
work, for as soon as the bomber gets to the specified cell, it begins a
continual circling of that cell.

Now that you know how to control where the bomber will come from, and
where it will drop its payload, we will discuss the types of payload a
bomber can carry. These payloads are infantry units and bomblets.
Infantry are dealt with in the ordinary way. You can have as many
different types of infantry units in a single bomber as you want, for
example, 6,E1:1,E2:1,E3:1,E7:1,C1:5,BADR:1 would be perfectly
acceptable. When dealing with sending in infantry reinforcements, there
doesn't seem to be a limit to the number of infantry units you can place
within a single bomber.
The infantry units will be dropped at the waypoint determined by one
of the methods shown above.

To get a bomber to drop bomblets rather than infantry, all you have to
do is not give the bomber any payload. This means that the relevant
part of the teamtype will look like this: 1,BADR:1. In this case, the
bomber will drop its payload of bomblets at the specified waypoint.

You can also get multiple bombers coming in just as easily as a single
bomber, but there is something you must be careful of when doing this
with infantry reinforcements.
When the bombers will just be dropping bomblets, nothing extra needs
to be done. All you need to do is to change the teamtype so that
instead of one Badger bomber being brought in, multiple are. Thus, the
relevant section of the teamtype would look like: 1,BADR:5 (to bring in
5 Badger bombers).

However, if you want to use multiple bombers in a teamtype that will
be dropping infantry units, you will have to be careful. This is
because only one bomber will drop infantry. The rest will drop the
bomblets. They will do this at the same time, which usually results in
the immediate death of the infantry units. I have noticed, however,
that if the target cell of bombers is occupied by a building, that the
bombers carrying bombs will drop their load, but the infantry carrying
bomber will not. If the building gets destroyed by the rain of
bomblets, then the infantry carrier will loop back and drop the infantry
where the building was previously situated. Thus, if the teamtype had
the section: 2,E1:5,BADR:4, then one Badger bomber would carry the five
infantry units, whilst the other three would carry the bomblets.


[7-8] The Global Mission Timer
===============================
When the timer has been stopped, using either timer extend or timer
shorten will start the timer again. If the use of timer shorten causes
the timer to expire, then any trigger associated with the timer expires
trigger event will be fired.

The timer warnings are given automatically (ie. it will warn you at
40 minutes, 30 minutes, 20 mintues etc), so there is no reason for you
to add a play speech trigger to play these warnings.

If you want to set the timer but don't want it to start, then your
trigger must have both the set timer and the stop timer trigger events,
both of which should be actiavted at the same time. The stop timer
event must be the second of the two trigger events; if it isn't, the
timer will be stopped then have its time set (having its time set causes
the timer to start counting down).


[7-9] What is the Zone of a cell?
==================================
There appear to be two different forms of "zone" as they refer to
cells. Both of the two types depend on which cell is being used. There
are only two types of cells on the map: those that are passable by a
ground unit, and those that are not.

If the cell being used to determing the "zone" is a passable cell,
then the zone of this cell will be that area of the map that a
ground-based unit can reach. So, if this was a totally blank map, the
"zone" of that cell would be the entire map. If this was a map that had
a cliff wall stretching from one side to the other, the "zone" would be
the half of the map that the cell is in.
Parts of the map like bridges (be they land bridges or concrete
bridges) are included in the category of passable land, so if a map was
separated by a river that had a bridge, the "zone" would be the entire
map, except for those parts of the river that are not passable by ground
units.

The other type of "zone" is where the cell is part of a non-passable
section of land. If this is the case, then the "zone" of this cell will
be the non-passable sections of mission. This includes cliffs and
rivers, and water. Please note the difference between this and the
previous form of "zone", in that this form of "zone" will reveal all
non-passable sections of land, *even if* they are not connected to the
initial cell. That means that a piece of cliff face totally unconnected
to another piece of cliff face will be exposed. Rivers and sections of
water are also counted as part of this "zone".

If you used the first type of "zone" for a Reveal zone of waypoint
trigger action, then the map cells that a ground unit can move to from
that cell will be revealed. This can potentially reveal a very large
amount of the map.
If you used the second type of "zone" for a Reveal zone of waypoint
trigger action, then all the non-passable map cells on the mission map
This means that all the cliff faces will be revealed, as will all
rivers, water sections etc.

Remember that the terrain editor has a function that will show
whether each cell is passable or not. You can use that function to help
determine what makes up the "zone" for a particular cell.

One use of the "zone" would be to determine whether the player has
landed some units on an island or not. This would be better than
putting celltriggers in all of the cells of the island that have an
Entered by event.

=========================
-SECTION FOUR- APPENDICES
=========================

--------------------------
CHAPTER [8] Items To Fill
--------------------------
The following parts need to be filled in, or made clearer:
[Basic] Section (4 items)
CarryOverMoney
TimerInherit
CarryOverCap
Percent
Country Specific Information (2 items)
MaxUnits, MaxInfantry, MaxBuilding, MaxVessel
[STRUCTURES] Section (1 item)
??? (second last item in entry)
[SMUDGE] Section (1 item)
cell2
Available Trigger Events (4 items)
Thieved by
Civilians evacuated
Crosses horizontal line
Crosses vertical line
Available Trigger Actions (4 items)
Allow win
Play music theme
Add repeating special weapon
Preferred target
[TeamType] Section (1 item)
More information needed on the effects of the various numbers
Available TeamType Actions (3 items)
Change Formation to
Attack Tarcom
Spy on building @ waypoint

-------------------------------
CHAPTER [9] Internet Resources
-------------------------------

[9-1] Third Party Programs
===========================
None as of yet.
Hopefully someone will work out how to write a fully-fledged map editor
some time soon.


[9-2] WWW Pages
================
http://www.geocities.com/TimesSquare/5458
Random Particles of Inspiration
The official site of the Single Player Mission Creation Guide.

------------------------------
CHAPTER [10] Revision History
------------------------------
v1.0 March 5, 1997.
First version of the guide.


Andrew Griffin bu...@adam.com.au
http://www.geocities.com/TimesSquare/5458
{\rtf1\ansi\ansicpg1252\cocoartf2867
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\froman\fcharset0 Times-Roman;\f1\fnil\fcharset0 HelveticaNeue;\f2\froman\fcharset0 Times-Bold;
}
{\colortbl;\red255\green255\blue255;\red109\green109\blue109;\red0\green0\blue0;\red0\green0\blue0;
\red201\green206\blue214;\red239\green99\blue114;\red229\green231\blue236;\red191\green94\blue241;}
{\*\expandedcolortbl;;\cssrgb\c50196\c50196\c50196;\cssrgb\c0\c0\c0\c84706;\cssrgb\c0\c0\c0;
\cssrgb\c82745\c84314\c87059;\cssrgb\c95686\c48235\c52157;\cssrgb\c91765\c92549\c94118;\cssrgb\c80000\c48235\c95686;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat0\levelspace360\levelindent0{\*\levelmarker \{disc\}}{\leveltext\leveltemplateid1\'01\uc0\u8226 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listname ;}\listid1}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 \
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf0 \strokec4 markdown\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 #\cf6 \strokec6  Birthday Escape Room \'97 Project Brief
\f0\b0 \cf7 \strokec7 \

\f2\b \cf5 \strokec5 ##\cf6 \strokec6  For Claude Code \'97 Read entirely before writing any code
\f0\b0 \cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0
\cf5 \strokec5 ---\cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 ##\cf6 \strokec6  Concept Overview
\f0\b0 \cf7 \strokec7 \
\
A multi-day personalised birthday experience beginning April 28th \
in Alicante, Spain, culminating in a scuba diving themed escape \
room on May 2nd \'97 his birthday. Delivered via a single URL on a \
handwritten stick note placed in his wallet before April 28th. \
Anonymous \'97 signed "Your (not-so) secret admirer" throughout the \
Spain tasks, revealed as Captain Jack Sparrow at the May 1st \
correct guess response. Tied to a shared inside joke: "You forgot \
one thing mate, I am Captain Jack Sparrow."\
\
Target player device: iPhone. All decisions optimised for Safari \
mobile.\
\
\pard\pardeftab720\partightenfactor0
\cf5 \strokec5 ---\cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 ##\cf6 \strokec6  Tech Stack
\f0\b0 \cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0
\cf5 \strokec5 -\cf7 \strokec7  \cf5 \strokec5 **\cf7 \strokec7 Frontend:\cf5 \strokec5 **\cf7 \strokec7  Single HTML file, CSS, JavaScript\
\cf5 \strokec5 -\cf7 \strokec7  \cf5 \strokec5 **\cf7 \strokec7 Database:\cf5 \strokec5 **\cf7 \strokec7  Supabase free tier\
  \cf5 \strokec5 -\cf7 \strokec7  Stores stage approval status\
  \cf5 \strokec5 -\cf7 \strokec7  Page polls Supabase every 60 seconds\
  \cf5 \strokec5 -\cf7 \strokec7  When approved in Supabase dashboard, page advances \
    automatically \'97 no code sent to player\
\cf5 \strokec5 -\cf7 \strokec7  \cf5 \strokec5 **\cf7 \strokec7 Photo submission:\cf5 \strokec5 **\cf7 \strokec7  Google Form \'97 photo upload only, \
  no other instructions visible to player\
\cf5 \strokec5 -\cf7 \strokec7  \cf5 \strokec5 **\cf7 \strokec7 Hosting:\cf5 \strokec5 **\cf7 \strokec7  Netlify free tier\
\cf5 \strokec5 -\cf7 \strokec7  \cf5 \strokec5 **\cf7 \strokec7 URL shortening:\cf5 \strokec5 **\cf7 \strokec7  bit.ly\
\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 ##\cf6 \strokec6  Safari-Specific Build Rules \'97 Non-Negotiable
\f0\b0 \cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0
\cf5 \strokec5 1.\cf7 \strokec7  Use \cf8 \strokec8 `height: -webkit-fill-available`\cf7 \strokec7  not \cf8 \strokec8 `height: 100vh`\cf7 \strokec7 \
\cf5 \strokec5 2.\cf7 \strokec7  All input fields minimum \cf8 \strokec8 `font-size: 16px`\cf7 \strokec7  \'97 prevents \
   Safari auto-zoom on tap\
\cf5 \strokec5 3.\cf7 \strokec7  All animations use CSS transforms only \'97 not width/opacity\
\cf5 \strokec5 4.\cf7 \strokec7  No hover states anywhere \'97 all interactions tap-based\
\cf5 \strokec5 5.\cf7 \strokec7  Test decoder disk drag events specifically on Safari \
   touch \'97 not just Chrome\
\
\cf5 \strokec5 ---\cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 ##\cf6 \strokec6  Information Architecture \'97 Two Views
\f0\b0 \cf7 \strokec7 \
\
The entire game lives in one HTML file. Two views toggle between \
each other via a persistent button at the bottom of the screen.\
\

\f2\b \cf5 \strokec5 ###\cf6 \strokec6  Ocean View
\f0\b0 \cf7 \strokec7 \
\pard\pardeftab720\partightenfactor0
\cf5 \strokec5 -\cf7 \strokec7  Oxygen bar \'97 sticky at top, always visible\
\cf5 \strokec5 -\cf7 \strokec7  Jack's narrative text for current puzzle\
\cf5 \strokec5 -\cf7 \strokec7  Underwater scene with interactive elements\
\cf5 \strokec5 -\cf7 \strokec7  Answer input field and submit button\
\cf5 \strokec5 -\cf7 \strokec7  Toggle button (compass icon) \uc0\u8594  switches to Decoder View\
\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 ###\cf6 \strokec6  Decoder View
\f0\b0 \cf7 \strokec7 \
\pard\pardeftab720\partightenfactor0
\cf5 \strokec5 -\cf7 \strokec7  Oxygen bar \'97 sticky at top, always visible\
\cf5 \strokec5 -\cf7 \strokec7  Three concentric decoder rings (see below)\
\cf5 \strokec5 -\cf7 \strokec7  Alignment indicator showing current Ring 2 position\
\cf5 \strokec5 -\cf7 \strokec7  Symbol reference guide \'97 all 26 creatures listed with names\
\cf5 \strokec5 -\cf7 \strokec7  Scratchpad \'97 text input for noting decoded letters\
\cf5 \strokec5 -\cf7 \strokec7  Toggle button (eye icon) \uc0\u8594  switches back to Ocean View\
\
Toggle button always reachable by thumb at bottom of screen.\
\
\cf5 \strokec5 ---\cf7 \strokec7 \
\
\pard\pardeftab720\partightenfactor0

\f2\b \cf5 \strokec5 ##\cf6 \strokec6  The Decoder Disk
\f0\b0 \cf7 \strokec7 \
\
Three concentric rings. Only Ring 2 moves.\
\

\f2\b \cf5 \strokec5 ###\cf6 \strokec6  Ring 1 \'97 Outer, Fixed
\f0\b0 \cf7 \strokec7 \
All sea creatures as symbols arranged around the ring.\
Includes: all ten Puzzle 1 creatures, four Puzzle 3 leader \
creatures (Whale, Shark, Dolphin, Manta Ray), two overlapping \
creatures (Turtle, Jellyfish), plus padding creatures to fill \
26 positions total.\
\

\f2\b \cf5 \strokec5 ###\cf6 \strokec6  Ring 2 \'97 Middle, Rotatable
\f0\b0 \cf7 \strokec7 \
Letters A through Z. Player drags to rotate. This is the only \
moving part. Player brings a specific letter to Ring 2 derived \
from the puzzle \'97 no preset alignment needed. Jack never \
instructs a starting position.\
\
Make finding a specific letter fast and smooth \'97 consider an \
alphabetical jump feature so player doesn't hunt through 26 \
positions manually.\
\

\f2\b \cf5 \strokec5 ###\cf6 \strokec6  Ring 3 \'97 Inner, Fixed
\f0\b0 \cf7 \strokec7 \
Digits 0-9 repeating randomly around the ring. Custom \
non-sequential mapping \'97 NOT A=1 through Z=26. Engineered so \
correct creature + letter combinations produce the right \
password digits for all three puzzles.\
\

\f2\b \cf5 \strokec5 ###\cf6 \strokec6  The Decode Chain
\f0\b0 \cf7 \strokec7 \
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 Creature (Ring 1) \uc0\u8594  player finds specific letter on Ring 2 and aligns it opposite that creature \u8594  read digit from Ring 3 at that position \u8594  one character of the password\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### Ring 3 Mapping \'97 Engineering Task\
Must satisfy all of these simultaneously:\
\
**Puzzle 1** (four bright creatures, colour-starting-letters \
\uc0\u8594  digits): produces 0, 2, 0, 5\
\
**Puzzle 2** (four diary sentence first-letters + named \
creatures \uc0\u8594  digits): produces 1, 9, 9, 2\
\
**Puzzle 3** (four letter shapes + leader creatures \uc0\u8594  digits):\
- Whale + T \uc0\u8594  0\
- Shark + Z \uc0\u8594  4\
- Dolphin + N \uc0\u8594  2\
- Manta Ray + H \uc0\u8594  8\
\uc0\u8594  produces 0, 4, 2, 8\
\
Engineer Ring 3 backwards from these constraints. Fill \
remaining positions randomly. Verify all required Puzzle 3 \
letters (T, Z, N, H) are straight-line achievable with \
turtle/jellyfish connections.\
\
---\
\
## Pre-Game \'97 The Stick Note\
\
Handwritten note placed in his wallet before April 28th.\
Contains only the shortened bit.ly URL.\
No name, no explanation.\
Optional: small hand-drawn anchor or wave doodle.\
\
---\
\
## Stage Flow \'97 Supabase Table Structure\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 stages table:\
\pard\tx220\tx720\pardeftab720\li720\fi-720\partightenfactor0
\ls1\ilvl0\cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 id\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 stage_number (1-8)\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 label (text description)\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 approved (boolean, default false)\
\ls1\ilvl0\kerning1\expnd0\expndtw0 \outl0\strokewidth0 {\listtext	\uc0\u8226 	}\expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec4 approved_at (timestamp)\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
**Stage map:**\
1. Opening page \uc0\u8594  Task 1 visible (April 28th)\
2. Task 1 approved \uc0\u8594  Task 2 visible (April 29th)\
3. Task 2 approved \uc0\u8594  Task 3 visible (April 30th)\
4. Task 3 approved \uc0\u8594  Guess mechanic visible (May 1st)\
5. Correct guess \uc0\u8594  May 1st message, escape room unlocks \
   May 2nd by date\
6. May 2nd \uc0\u8594  Escape room entry\
7. All puzzles solved \uc0\u8594  Matching game\
8. All matches complete \uc0\u8594  Final reveal\
\
Tasks revealed sequentially \'97 next task only appears after \
previous stage approved. Escape room unlocks by date \
(May 2nd) not by Supabase approval.\
\
---\
\
## Opening Page \'97 First Load April 28th\
\
Shown immediately when he visits the URL. Before any task.\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "So.\
You found this.\
I have something that you can find. A treasure, mate. Now. There are rules. Because you kind of like them.\
Rule the first: You will complete the tasks I set for you. One per day.\
Rule the second: You will tell no one. Not a soul.\
Rule the third: You will not be smug.\
The first task awaits below.\
Do try to keep up.\
\'97 Your (not-so) secret admirer"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
---\
\
## Spain Tasks\
\
### Design Principles\
- Ocean theme subtle, never stated\
- Tasks feel like natural tourist activities\
- Google Form: photo upload only, no instructions visible \
  to player\
- Soft encouragement to upload at end of day \'97 no hard lock\
- Next task revealed only after previous approved in Supabase\
- Page polls every 60 seconds \'97 advances automatically\
\
---\
\
### Task 1 \'97 April 28th\
**The task:** Find where one ends and the other starts\
\
*Hidden design note (not shown to player): Can be sunset, \
where road meets sea, where sea meets sky. Deliberately open.*\
\
**Page text:**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "The admirer has been watching. Your task today is to find something where one ends and the other starts. Take a picture and share it with me using the link below. It can be time or space, take your pick.\
When the day is done and the light has gone, the admirer will be waiting. So, take your time and get it right. There are quite a few things that do not give bonus points for speed \'97 a fact you know well, as it's not one of your fortes.\
\'97 Your (not-so) secret admirer"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 [Google Form link button]\
\
---\
\
### Task 2 \'97 April 29th\
**The task:** Find something blue on blue\
\
*Hidden design note: Most likely one blue will be water. \
Even if not, blue is still ocean theme.*\
\
**Page text:**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Goooood morning, mate.\
Your task today is to find where blue meets blue. Not one blue. Two. Together.\
Upload when the evening arrives. Not before. Good things require patience. But you already have lots of it, I am sure.\
\'97 Your (not-so) secret admirer"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 [Google Form link button]\
\
---\
\
### Task 3 \'97 April 30th\
**The task:** Find your reflection which is moving\
\
*Hidden design note: "Moving" qualifier forces water. \
Mirror = still reflection. Moving water = moving reflection.*\
\
**Page text:**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Three days now. Three tasks. You are either very dedicated or very curious. Or a stickler for routine. I respect all three.\
Today's task is a peculiar one, but the best ones always are.\
Find your reflection. It should be moving \'97 shifting and refusing to hold still. Capture it.\
The day is yours. The evening is mine.\
\'97 Your (not-so) secret admirer"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 [Google Form link button]\
\
---\
\
### Task 4 \'97 May 1st (Guess Mechanic)\
**Triggered:** Automatically after Task 3 approved in Supabase\
**No Google Form** \'97 text input directly on page\
**No Supabase approval needed** \'97 fuzzy match handles it\
\
**Page text:**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Oh, fish.\
You actually did it. All three. I'll be honest with you \'97 and I am, occasionally, honest \'97 I had a small wager with myself about whether you'd make it this far. I won. Obviously.\
Now. Before the treasure reveals itself \'97 and it will, mate, it absolutely will \'97 your (not-so) secret admirer requires one small thing from you.\
Three tasks. Three clicks. What connects them?\
Type your answer below. Take your time. But not too much time, eh?\
\'97 Your (not-so) secret admirer"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
**Text input field**\
\
Fuzzy match \'97 accept any input containing:\
ocean, sea, water, mediterranean, waves, blue, the sea, \
the ocean, the mediterranean\
\
Case insensitive. Partial match acceptable.\
\
**Wrong answer response:**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Hmm. Close, perhaps. Or perhaps not. Look again, mate. Think about where you've been. What was always present, even when you weren't looking directly at it.\
\'97 Your (not-so) secret admirer"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
**Correct answer response (May 1st message):**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "There it is.\
You saw it.\
And now I have decided that you are ready to find the treasure.\
Tomorrow \'97 May the second, your day, as it happens, which is entirely coincidental (or not) \'97 the path to the treasure is revealed.\
Sleep well, diver.\
Oh, and by the way, you forgot one thing, mate.\
I am Captain Jack Sparrow"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
After this message: escape room unlocks on May 2nd by date.\
\
---\
\
## Escape Room \'97 May 2nd\
\
### Entry Narration\
Shown when he first opens the page on May 2nd.\
Oxygen bar appears and begins depleting immediately.\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Happy birthday.\
Now \'97 there will be time for celebrations later, and I fully intend to attend, but first: there is the small matter of the treasure.\
It is down here. In the deep. Waiting.\
You have \'97 and I would draw your attention to the gauge at the top of your screen \'97 a limited supply of oxygen. However, if you see any cylinders lying around, collect those. Maybe 5 is a lucky charm to live longer.\
Three locks stand between you and what is yours. Each one has a key. Each key is hidden somewhere in the depths around you. Find them. Use them. In that order, mate \'97 this is important \'97 in that order.\
I would help you, but I am Captain Jack Sparrow, and captains do not do puzzles. We delegate.\
The clock is running.\
Off you go.\
\'97 CJS"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
---\
\
## Oxygen Bar\
\
- Sticky at top of screen in BOTH views at all times\
- Total duration: 30 minutes\
- When oxygen runs out: Jack gives a gentle nudge, \
  small refill, game continues \'97 not a hard game over\
- Jack nudge text when oxygen runs out:\
  PLACEHOLDER \'97 to be written\
\
---\
\
## Five Hidden Oxygen Cylinders\
\
- Scattered across all three puzzle scenes\
- Finding individual cylinders: Jack comments \
  (text TBD), nothing else happens\
- Finding all five: single dramatic oxygen burst, \
  significant bar refill\
- Positions: TBD during build\
- Obviousness level: TBD during build\
\
**Jack comment when one cylinder found \'97 PLACEHOLDER**\
**Jack comment when all five found \'97 PLACEHOLDER**\
\
---\
\
## Jack's Diary\
\
- Always accessible from escape room start\
- Diary icon in Ocean View \'97 tap to open\
- Not a reward gate \'97 available immediately\
- Multiple entries, scrollable\
- Aged parchment aesthetic, handwriting font\
- Pages that turn on swipe\
- Two sealed pages \'97 unlock condition TBD\
\
### Entry 1 \'97 Night diving hint (Puzzle 1 clue)\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "A word of advice, mate \'97 and I give advice not-so-rarely, but still listen carefully. The creatures you see in these waters are not always what they appear. Some are merely... decorating. The ocean reveals its true nature only to those who have done the night diving course. The serious divers know this. The others just get wet."\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### Entry 2 \'97 Overlapping creatures hint (Puzzle 3 clue)\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "I have noticed, in my many years navigating these waters, that the creatures who appear most often are not the most numerous \'97 they are the most important. They are the ones who know more about the treasure."\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### Entry 3 \'97 Emotional foreshadowing (no puzzle content)\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "The finest treasure I ever found wasn't gold. It was the faces of the people who were inexplicably pleased to see me return. Food helps. But people matter more."\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### Remaining entries \'97 TBD during build\
- Intro/flavour entry \'97 Jack being Jack, no puzzle content\
- Puzzle 2 clue entry \'97 contains right halves of cave \
  wall symbols as margin illustrations, four sentences \
  engineered to start with specific letters and name \
  specific creatures (written after Ring 3 mapping \
  is finalised)\
- Misdirection entry \'97 looks like a clue, leads nowhere\
- Sealed pages content \'97 TBD\
\
---\
\
## The Mermaid\
\
- Shell icon in corner of Ocean View \'97 tap to call\
- Three hints total across entire game \'97 shared pool\
- Each hint used: Jack comments \
  *"Going to the mermaid, are we. I had every confidence \
  in you. Some confidence. A moderate amount."*\
- First visit: she watches, doesn't speak until tapped\
- Puzzle 3: appears unbidden, shifts from helper to observer\
\
### The Three Hints \'97 TBD\
One hint per puzzle. To be written once puzzles are \
fully built and tested \'97 hints should address the most \
likely sticking point in each puzzle.\
\
### Mermaid voice \'97 warmer and more sincere than Jack\
Visual design: TBD\
\
---\
\
## Puzzle 1 \'97 The Ocean Scene\
\
**Location:** Main Ocean View\
**Password:** 0205\
\
### Scene\
- All visible at once \'97 no scrolling\
- Ten sea creatures in ten different colours\
- Cave visible in background\
- Cave entrance has a lock \'97 tapping prompts \
  4-digit passcode input\
- Oxygen bar running\
- Night mode toggle (moon/torch icon)\
- Diary icon accessible\
- Shell icon (mermaid) accessible\
\
### The Ten Creatures\
Ten species \'97 TBD during build\
Ten distinct colours \'97 four bright creatures engineered \
to produce 0205, six remaining colours must not decode \
to anything meaningful in any order.\
\
### Normal Light\
All ten creatures visible. No brightness difference. \
No tapping mechanic. Colours visible on all creatures.\
\
### Night Mode\
Six creatures appear dull/faded.\
Four creatures remain bright \'97 these are the significant ones.\
No symbols revealed on tap \'97 colours always visible, \
night mode is the only mechanic.\
\
### The Mechanic\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 Bright creature \uc0\u8594  its colour \u8594  first letter of colour name \u8594  find that letter on Ring 2 \u8594  align opposite that creature on Ring 1 \u8594  read Ring 3 digit\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
Four bright creatures, left to right = four digits = 0205\
\
### Puzzle 1 Narrative\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Ah. You found this. Curious. Most people wouldn't have. But then, most people are not you, and most people are not accompanied by the most brilliant mind of this or any other century.\
Now. The treasure \'97 I ramble. Probably a lot. You would know.\
Look around. Observe. The rest, I leave to you.\
\'97 CJS"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### On Correct Entry\
Simple CSS animation \'97 cave entrance opens.\
Cave view loads.\
\
---\
\
## The Cave View\
\
**Accessed:** After correct Puzzle 1 password\
\
### Scene\
- Dark enclosed cave interior\
- Bioluminescent algae on walls\
- Glowing creatures in crevices\
- Oxygen bar still visible and running\
- More enclosed and urgent than open ocean\
\
### Contents\
- Cave wall \'97 four partial sea symbols, left to right\
- Deeper passage \'97 visible but sealed, opens after \
  Puzzle 2 correct password\
- One hidden oxygen cylinder \'97 not obvious\
- Mermaid \'97 present but silent, watching\
\
---\
\
## Puzzle 2 \'97 The Cave Wall and Diary\
\
**Location:** Cave View\
**Password:** 1992\
\
### The Asymmetric Mechanic\
\
**Source A \'97 Cave wall:**\
Four partial symbols carved left to right.\
Left half only of each symbol \'97 clearly incomplete.\
\
The four symbols: Anchor, Shell, Trident, Compass Rose\
\
**Source B \'97 Jack's diary:**\
Right half of each symbol appears as margin illustration \
in a diary entry. Embedded naturally, not labelled. \
One half per entry, four different entries.\
\
### The Connection\
Match cave half \uc0\u8594  diary half = complete symbol.\
\
From the diary entry containing that half:\
1. First letter of the sentence containing it \uc0\u8594  Ring 2\
2. Creature named in that sentence \uc0\u8594  Ring 1\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 Decode chain: Match symbol halves \uc0\u8594  diary sentence identified \u8594  first letter of sentence = Ring 2 input \u8594  creature named in sentence = Ring 1 input\u8232 \u8594  align letter opposite creature \u8594  read Ring 3 digit\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
Four matches, left to right cave wall order = 1, 9, 9, 2\
\
### The Four Diary Sentences\
To be written after Ring 3 mapping is finalised.\
Requirements per sentence:\
- Starts with the specific letter needed\
- Names a specific creature naturally\
- Contains margin illustration of symbol half\
- Sounds natural in Jack's voice\
\
### Puzzle 2 Narrative\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "One down.\
The cave remembers everything, mate. Every captain who sheltered here. Every secret left behind. Look around carefully.\
\'97 CJS"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### On Correct Entry\
Gateway in cave wall opens.\
Ocean floor view loads.\
\
---\
\
## Puzzle 3 \'97 The Ocean Floor Constellation\
\
**Location:** Ocean floor \'97 new view beyond the gateway\
**Password:** 0428 (April 28th \'97 the day it all began)\
\
### Scene\
- Deeper, more dramatic than cave\
- Treasure chest visible in distance\
- Four groups of creatures on the ocean floor\
- Each group has a leader creature above it\
\
### The Two Overlapping Creatures\
**Turtle** and **Jellyfish**\
\
These appear in:\
- Puzzle 1: two of the four bright night-mode creatures\
- Puzzle 2: creatures named in two of the four \
  diary sentences\
- Puzzle 3: appear multiple times within each group, \
  connected by lines forming letters\
\
Their recurrence across all three puzzles is intentional \
and reveals itself here.\
\
### The Four Groups\
\
**Group 1 \'97 Whale leads, forms letter T**\
Turtle and jellyfish instances connected:\
- Horizontal stroke across top (T \'97 T \'97 J or T \'97 J \'97 T)\
- Vertical stroke dropping from centre (J down)\
T shape \'97 unambiguous\
\
**Group 2 \'97 Shark leads, forms letter Z**\
- Horizontal stroke top (T \'97 J)\
- Diagonal dropping to bottom left\
- Horizontal stroke bottom (T \'97 J or J \'97 T)\
Z shape \'97 immediately recognisable\
\
**Group 3 \'97 Dolphin leads, forms letter N**\
- Left vertical (T down to J)\
- Diagonal rising right\
- Right vertical (T down to J)\
N shape \'97 distinct\
\
**Group 4 \'97 Manta Ray leads, forms letter H**\
- Left vertical\
- Horizontal crossbar mid-height\
- Right vertical\
H shape \'97 unmistakable\
\
Additional camouflage creatures fill each group in \
normal light \'97 species TBD. These are not turtles \
or jellyfish. They make the groups look like natural \
clusters rather than deliberate letter shapes.\
\
### The Mechanic \'97 Per Group Independently\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 Trace turtle/jellyfish connections within group \uc0\u8594  identify letter shape formed \u8594  bring that letter to Ring 2 \u8594  align opposite leader creature on Ring 1 \u8594  read Ring 3 digit\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
No global alignment. Each group decoded independently.\
Can be solved in any order.\
\
### Required Outputs\
- Whale + T \uc0\u8594  0\
- Shark + Z \uc0\u8594  4\
- Dolphin + N \uc0\u8594  2\
- Manta Ray + H \uc0\u8594  8\
\
Password: 0428\
\
### Puzzle 3 Narrative\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Remarkable.\
I don't say that often. I usually complain a lot, not compliment. Ask anyone. Well \'97 ask the people who know me well.\
You are deeper now than most people dare to go. The treasure is ahead. Almost within reach.\
One final thing stands between you and it.\
The creatures will show you the way \'97 if you know how to read them.\
\'97 CJS"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### On Correct Entry\
Treasure chest opens.\
Matching game begins.\
\
---\
\
## The Treasure Chest \'97 Matching Game\
\
### Entry Narration\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "You did it.\
I would say I'm surprised but I knew that this would happen.\
The treasure is here. Right here. But a treasure of this particular kind cannot simply be handed over, mate. It must be \'97 recognised.\
Inside this chest are some of your people.\
Each of them has left something for you \'97 a moment they kept, and three words they chose.\
But the chest will only reveal them one by one as you find them.\
Match the face to the memory.\
Take your time. This part, there is no clock for.\
\'97 CJS"\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### The Mechanic \'97 Mobile Card Selection\
1. Photos of contributors shown as grid at top\
2. Player taps a face \'97 it highlights\
3. Memories appear as cards below, scrollable\
4. Player taps memory they think belongs to that face\
5. **Correct:** three words animate in one by one, \
   half-second gap between each word\
6. **Wrong:** gentle shake animation, try again, \
   no penalty, unlimited attempts\
7. Presented in batches of 4-5 people\
8. Each batch completes before next appears\
\
### Contributor Data Structure\
Per person:\
- Photo (image file)\
- One specific shared memory (one sentence)\
- Three words to describe him\
\
### Micro Responses \'97 Rotate Randomly on Correct Match\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "There. You know this one." "Of course. How could you forget." "Ah. That one. Good memory, mate." "See? I told you. You know exactly who loves you." "This one knew you'd get it." "Some things you just know."\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
### Contributor Collection\
Target: 12-15 people\
Deadline to give contributors: April 25th\
Your real deadline from contributors: April 26th\
Buffer day: April 27th to chase late responses\
\
**Message to send contributors:**\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "Hey! I'm doing something secret for [his name]'s birthday and I need two things from you. First, one specific memory you have with him \'97 one sentence, something only you two share. Second, three words you'd use to describe him \'97 the more specific to how YOU see him the better. Not just 'funny' or 'kind' \'97 something only you would say. Send both to me by April 26th and keep it secret! I'll also need a photo of you \'97 candid is great, I might already have one."\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
---\
\
## All Matches Complete \'97 Final Reveal\
\pard\pardeftab720\sa240\partightenfactor0
\cf0 \strokec4 "And there it is.\
That is the treasure.\
Now.\
There is one more thing in the chest.\
From someone who knows you rather better than a mysterious captain perhaps should."\
\pard\pardeftab720\qc\partightenfactor0

\f1\fs22 \cf3 \strokec3 \
\pard\pardeftab720\partightenfactor0

\f0\fs24 \cf7 \strokec7 \
[Button appears: "Open the last thing"]\
\
---\
\
## The Final Message\
\
**Written entirely by you \'97 placeholder in build.**\
\
Suggested structure:\
- One playful sentence acknowledging it was you\
- Why you did this, what you wanted him to feel\
- Something specific to him only\
- The inside joke one final time\
- Happy birthday in your voice\
\
Below the text: your favourite photo of the two of you.\
\
---\
\
## Yet To Decide \'97 Master List\
\
### Urgent \'97 Before Build Starts\
- [ ] Final birthday message from you\
- [ ] Which photo of the two of you for final reveal\
- [ ] Send contributor message by April 25th\
- [ ] Ring 3 custom mapping \'97 engineer during \
      build phase\
\
### During Build\
- [ ] Jack nudge text when oxygen runs out\
- [ ] Jack comment when one cylinder found\
- [ ] Jack comment when all five cylinders found\
- [ ] Five cylinder positions across three scenes\
- [ ] Cylinder obviousness level\
- [ ] Full diary entry set beyond three drafted\
- [ ] Sealed diary pages \'97 unlock condition and content\
- [ ] Three mermaid hints \'97 one per puzzle\
- [ ] Mermaid visual design and voice/tone\
- [ ] Ten creature species for Puzzle 1\
- [ ] Four bright creature colours \'97 engineered \
      for 0205\
- [ ] Six dim creature colours \'97 must not decode \
      to anything meaningful\
- [ ] Camouflage creature species for Puzzle 3 groups\
- [ ] Ocean floor scene visual design\
- [ ] Puzzle 2 diary sentences \'97 after Ring 3 finalised\
\
### Design Still Open\
- [ ] Sealed diary pages unlock condition\
- [ ] Whether treasure box/gateway contains anything \
      beyond passage to Puzzle 3\
- [ ] Exact visual design of ocean floor scene\
\
---\
\
## Build Priority Order\
\
Build in this sequence \'97 do not skip ahead:\
\
1. **Supabase setup + page skeleton** \'97 two-view \
   structure, polling logic\
2. **Spain tasks** \'97 four stages, Google Form links, \
   fuzzy matching, May 1st reveal\
3. **Decoder disk** \'97 three rings, drag rotation, \
   scratchpad, Ring 3 mapping\
4. **Puzzle 1** \'97 ocean scene, night mode, \
   four creatures, cave opening\
5. **Cave view** \'97 scene, partial symbols, diary\
6. **Puzzle 2** \'97 symbol matching, diary halves, \
   gateway opening\
7. **Puzzle 3** \'97 ocean floor, constellation groups, \
   per-group decode\
8. **Matching game** \'97 card selection, word reveal, \
   batched display\
9. **Final reveal** \'97 placeholder for your message \
   and photo\
10. **Polish** \'97 oxygen bar, cylinders, mermaid, \
    diary entries, animations\
\
**Rule:** Spain tasks must work before escape room \
is built. April 28th is the hard deadline.\
\pard\pardeftab720\partightenfactor0
\cf2 \strokec2 \
\pard\pardeftab720\sa240\partightenfactor0
\cf2 \strokec4 Diary icon \'97 fixed at top of screen, accessible in ALL \
views throughout the entire game (Ocean View, Decoder \
View, Cave View, Ocean Floor View). Not just Ocean View.}
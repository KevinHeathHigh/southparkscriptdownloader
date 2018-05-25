
# Download a Single Episode Script and Extract the dialogue from a single character (Cartman)
Exercise to download Southpark scripts from http://southparkwillie.com/ [http://southparkwillie.com/Season1/E101script.htm] and create function to pull the dialogue for a single character from a single script 

* Alternative is PDFs from www.southparkcows.com/scripts/101.pdf [www.southparkcows.com/scripts/101.pdf]
* Also might try with http://southpark.wikia.com/wiki/ [http://southpark.wikia.com/wiki/The_Unaired_Pilot/Script] (another HTML Table) - After digging around more on this side, it appears that only the above mentioned script is actually html script, the rest point to PDF files.


```python
#Season 1, Epsisode 1 URL
script_url = 'http://southparkwillie.com/Season1/E101script.htm'
```


```python
import requests

script_text = requests.get(script_url)
```


```python
print(script_text.text)
```

    <html><head><title>Episode 101 - Cartman Gets An Anal Probe</title></head>
    </STYLE> 
    <style type="text/css"><!-- 
    body { 
    scrollbar-face-color: #ca9876; 
    scrollbar-shadow-color: #543210; 
    scrollbar-highlight-color: #cba987; 
    scrollbar-3dlight-color: #765432; 
    scrollbar-darkshadow-color: #765432; 
    scrollbar-track-color: #dcba98; 
    scrollbar-arrow-color: #765432; } 
    //--></style> 
    </style type="text/css">
    <body bgcolor=fedcba>
    <h2 align=center>Episode 101 - Cartman Gets An Anal Probe</h2>
    <h4 align=center>Cast<p> 
    Kyle Broflovski (boy wearing green duck cap)<br>Kenny McKormick (boy in orange parka)<br>Eric Cartman (the fat one)<br>Stan Marsh (boy wearing blue beanie)<br>Ike<br>Chef<br>Ms. Crabtree<br>Carl<br>Officer Barbrady<br>Mr. Garrison<br>Mr. Hat<br>Pip<br>Train Conductor<br>Wendy Testaburger<br>Ms. Cartman<br>News Reporter<br>Special appearances by several cows and Aliens</h4><hr>
    <table>
    <tr><td><td bgcolor=dcba98><i>[At the bus stop]</i>
    <tr><td>Boys:<td><i>School day, school day, teacher's golden ru</i>
    <tr><td>Kyle:<td>Ah, damn it! My little brother's trying to follow me to school, again.
    <tr><td>Ike:<td>Zeeponanner
    <tr><td>Kyle:<td>Ike, you <i>can't</i> come to <i>school</i> with me. <i>[Ike chortles]</i>
    <tr><td>Cartman:<td>Yeah, go home you little dildo.
    <tr><td>Kyle:<td>Dude, don't call my brother a dildo!
    <tr><td>Stan:<td>What's a dildo?!
    <tr><td>Kyle:<td>Well, I don't know <i>[faces Cartman and points at him]</i> and I'll bet Cartman doesn't know either!
    <tr><td>Cartman:<td>I know what it means!
    <tr><td>Kyle:<td>Well, what?
    <tr><td>Cartman:<td>I'm not telling you.
    <tr><td>Stan:<td>What's a dildo Kenny?
    <tr><td>Kenny:<td>(It's a giant stick that goes inside the mom's vagina) <i>[the others laugh]</i>
    <tr><td>Cartman:<td>Heyeah, that's what Kyle's little brother is all right! <i>[Kyle swings Ike by his feet, knocking Cartman down]</i> Ow! <i>[Ike laughs]</i>
    <tr><td>Stan:<td>Dude! That kicks ass!
    <tr><td>Kyle:<td>Yeah, check this one out. Ready, Ike? Kick the baby!
    <tr><td>Ike:<td>Don't kick the baby.
    <tr><td>Kyle:<td>Kick the baby. <i>[he kicks Ike, and Ike mows down four mailboxes.  Cartman yawns.]</i>
    <tr><td>Stan:<td>Whoa, Cartman, looks like you didn't get much sleep last night.
    <tr><td>Cartman:<td>That's 'cause I was having these bogus nightmares.
    <tr><td>Kyle:<td>Really? What about?
    <tr><td>Cartman:<td>Well, I dreamt that I was lying in my bed <i>[the dream sequence begins]</I> in the dark. When all of a sudden this bright blue light filled the room <i>[through his window, one can see a spaceship land and its light stream in]</i>. Then slowly my bedroom door begin to open <i>[an alien peeks inside]</i> and the next thing I remember I was being drug through a hallway. <i>["Weeaak!"]</i> Then I was lying on a table <i>[face down, and aliens lower his pajamas]</i> and these scary hands wanted to operate on me. And they had big heads and big black eyes
    <tr><td>Stan:<td>Dude! Visitors!
    <tr><td>Kyle:<td>Totally!
    <tr><td>Cartman:<td>What?
    <tr><td>Stan:<td>That wasn't a dream Cartman, those were visitors!
    <tr><td>Cartman:<td>No, it was just a dream, my mom said so.
    <tr><td>Stan:<td>Visitors are real.
    <tr><td>Kyle:<td>Yeah, they abduct people and they mutilate cows.
    <tr><td>Cartman:<td>Oh, shut up guys! You're just trying to make me scared. And it's not working.
    <tr><td>Chef:<td><i>[drives up and gets out of the car]</i> Hello there, children.
    <tr><td>Boys:<td>Hey, Chef.
    <tr><td>Stan:<td>What's gonna be for lunch today, Chef?
    <tr><td>Chef:<td>Well, today it's Salisbury steak with buttered noodles and a choice of green bean casserole or vegetable medley.
    <tr><td>Cartman:<td>Kick ass.
    <tr><td>Chef:<td>Say, did any of you children see the alien space ship last night?
    <tr><td>Cartman:<td>What?
    <tr><td>Kyle:<td>Yeah, fat boy saw it!
    <tr><td>Cartman:<td>Eh, no, that, that was just a dream and I'm not fat, I'm big boned!
    <tr><td>Chef:<td>Oh, was it the ones with the big long heads and the black eyes?
    <tr><td>Cartman:<td>Oh!
    <tr><td>Stan:<td>They took him on their ship.
    <tr><td>Chef:<td>Oh! Did they give you an anal probe?
    <tr><td>Cartman:<td>Oh!
    <tr><td>Kyle:<td>What's an anal probe?
    <tr><td>Chef:<td>That's when they put a big metal hooba-jube up yo' butt.
    <tr><td>Kyle:<td>Whoa! They gave you an anal probe Cartman?
    <tr><td>Cartman:<td>No! Uh-I mean, eh, why would they do that?
    <tr><td>Stan:<td>Dude, they did, huh? Aliens stuck stuff up your ass!
    <tr><td>Cartman:<td>No!
    <tr><td>Ike:<td>Eneh probe
    <tr><td>Cartman:<td>Shut up dildo!
    <tr><td>Chef:<td>Well, I gotta get to the cafeteria. You children watch that fat boy now. He could be under alien control. <i>[Chef walks back to his car, there is a picture of an alien on his shirt.  Chef drives off.]</i>
    <tr><td><th>
    <table>
    <tr><th bgcolor=red><font face=arial>&nbsp;BELIEVE
    </table>
    <tr><td>Cartman:<td>Oh!
    <tr><td>Kyle:<td>We told you they were real Cartman. Sorry to hear about your ass.
    <tr><td>Cartman:<td>God damn it, they didn't do anything to my ass. It was just a dream.
    <tr><td><td><i>[They start to file onto the bus.]</i>
    <tr><td>Kyle:<td>Why are you walkin' so funny Cartman?
    <tr><td>Cartman:<td>Shut up!
    <tr><td>Ike:<td><i>[waddles by.]</i> Oh foonuh bebe.
    <tr><td>Kyle:<td>No, Ike, go home. 
    <tr><td>Ike:<td>Eeeeee!
    <tr><td>Kyle:<td>This is it. This one's for the game.
    <tr><td>Ike:<td>Purplor.
    <tr><td>Kyle:<td>Kick the baby! <i>[He kicks Ike, who flies through the first window of the school bus and crashes out through the other side.]</i>
    
    <tr><td><td bgcolor=dcba98><i>[On The Bus]</i>
    <tr><td><th>
    <table>
    <tr><th bgcolor=yellow><font face=arial><u>____________________________<br>SOUTH PARK ELEMENTARY R-1</u>
    </table>
    <tr><td>Stan:<td>Good morning, Miss Crabtree.
    <tr><td>Ms. Crabtree:<td>Sit down! We're runnin' late! <i>[The bus pulls away, leaving Ike behind at the bus stop. Kyle is kneeling on the seat looking back at him.]</i>
    <tr><td>Kyle:<td>Damn it, he's still there.
    <tr><td>Stan:<td>Oh, don't worry about him.
    <tr><td>Kyle:<td>No, dude, if something happens to him, my parents are gonna blame me.
    <tr><td>Ms. Crabtree:<td>SIDDOWN BACK THERE! AAAAAAAAAAA!!
    <tr><td>Stan:<td>Yeah, whatever, ya fat bitch!
    <tr><td>Ms. Crabtree:<td><i>What did you say?</i>
    <tr><td>Stan:<td>I said I have a bad itch.
    <tr><td>Ms. Crabtree:<td>Oh.
    <tr><td>Kyle:<td><i>[gasps]</i> Oh, my God! <i>[two aliens are holding Ike between them]</i>
    <tr><td>Stan:<td><i>[turning to see]</i> Visitors!
    <tr><td>Kenny:<td>(Oh nooo!)
    <tr><td>Kyle:<td>Ike! <i>[runs to the front of the bus]</i> Stop the bus! Miss Crabtree, you have to stop this bus!
    <tr><td>Ms. Crabtree:<td><i>Do you want an office referral?</i>
    <tr><td>Kyle:<td>No.
    <tr><td>Ms. Crabtree:<td>Then sit down!
    <tr><td>Kyle:<td>But I
    <tr><td>Ms. Crabtree:<td>Aaaah!
    <tr><td>Kyle:<td>Aaaah!
    <tr><td>Kyle, Ms. Crabtree:<td>Aaaah! <i>[Kyle runs back to his seat.  Ms. Crabtree has the last word]</i>
    <tr><td>Stan:<td>Cartman, are those the same visitors you saw?
    <tr><td>Cartman:<td>Shut up you guys it's not working.
    <tr><td>Kyle:<td>We have to do something!
    <tr><td>Stan:<td>Well, we can't do anything for now, that fat bitch won't let us.
    <tr><td>Ms. Crabtree:<td><i>What did you say?</i>
    <tr><td>Stan:<td>Uh, I said that rabbits eat lettuce.
    <tr><td>Ms. Crabtree:<td>Oh. Well, yes, they certainly do. <i>[she makes a hard right,  flinging kids onto the left side of the bus.]</i>
    <tr><td>Kyle:<td>What am I going to do? My little brother's been abducted by aliens. <i>[Stan farts]</i> You farted. <i>[They laugh]</i>
    <tr><td>Cartman:<td>Somebody's baking brownies. <i>[Behind the bus, a space craft rises into the sky, then zoomz away]</i>
    
    <tr><td><th>
    <table>
    <tr><th bgcolor=999977><font face=arial>CATTLE RANCH
    </table>
    <tr><td><td bgcolor=dcba98><i>[Farmer's grazing fields with a mutilated cow]</i>
    <tr><td>Farmer:<td>This is the third cow this month. At this rate all of my cattle are gonna die before the winter's through. <i>[The cows moo questioningly]</i>
    <tr><td>Officer Barbrady:<td>This is nothing out of the unusual. Cows turn themselves inside out all the time. <i>[The cows shake their heads]</i>
    <tr><td>Farmer:<td>People's been saying they've been seeing UFO's around.
    <tr><td>Officer Barbrady:<td>UFO's? <i>[laughs]</i>
    <tr><td>Farmer:<td>Yeah, and black army CIA helicopters and trucks.
    <tr><td>Officer Barbrady:<td>That is the silliest thing I've ever heard. <i>[Helicopters fly by above him]</i>
    <tr><td>Farmer:<td>What was that?
    <tr><td>Officer Barbrady:<td>That, that was a pigeon.
    <tr><td>Farmer:<td>What am I supposed to do, Barbrady? Just stand here and watch my cattle get mutilated one by one? <i>[the cows notice something and raise their heads. One alien waves a piece of hay; another one whistles.  The cows start running away from them.]</i> Hey! My cattle! <i>["Cattle Ranch" sign falls down.]</i> You see, there <i>is</i> somethin' funny goin' on!
    <tr><td>Officer Barbrady:<td>There's nothing funny going on. I'll get those cows back.
    
    <tr><td><th>
    <table>
    <tr><th bgcolor=blue><big>SOUTH PARK ELEMENTARY</big>
    </table>
    <tr><td><td bgcolor=dcba98><i>[Mr. Garrison's class]</i>
    <tr><td>Mr. Garrison:<td>And now children, our friend, Mr. Hat, is going to tell us about Christopher Columbus.
    <tr><td>Mr. Hat:<td>That's right, Mr. Garrison. Christopher Columbus discovered America and was the Indians' best friend. He helped the Indians win their war against Fredrick Douglass and and a freed the Hebrews from Napoleon and discovered France. And then in 1492 
    <tr><td>Kyle:<td><i>[whispering]</i> Oh, man. I can't just sit here, I have to help my stupid brother, or I'll come home without him and my dad will start yelling, "Where's your brother, Kyle?" "You weren't looking out for your little brother, Kyle?"-
    <tr><td>Stan:<td><i>[whispering]</i> Okay, okay, let's ditch school and go find him.
    <tr><td>Kyle:<td><i>[voice rising to an audible level]</i> -"You know he can't think on his own, Kyle!" "Brush and floss, Kyle!" "Where has that finger been, Kyle?"
    <tr><td>Stan:<td>Dude!
    <tr><td>Mr. Garrison:<td>Is there a problem, boys?
    <tr><td>Kyle:<td>Yes, Mr. Garrison, I have to go now.
    <tr><td>Mr. Garrison:<td>Oh, really, Kyle? What is it this time? Another prostate tumor?
    <tr><td>Kyle:<td>No, my little brother's been abducted by aliens. <i>[silence]</i> It's true! Ask Cartman, they gave <i>him</i> an anal probe.
    <tr><td>Cartman:<td><i>[enbarrassed]</i> Heh, heh, that's a, that's, that's a little joke. Heh, heh.
    <tr><td>Kyle:<td><i>[walks up to Mr. Garrison's desk]</i> Mr. Garrison, seriously, I have to go. Can I <i>please</i> be excused from class?
    <tr><td>Mr. Garrison:<td>I don't know, Kyle. Did you ask Mr. Hat?
    <tr><td>Kyle:<td>I don't want to ask Mr. Hat, I'm asking you!
    <tr><td>Mr. Garrison:<td>Oh I think you should ask Mr. Hat.
    <tr><td>Kyle:<td>Mr. Hat, may I please be excused from class?
    <tr><td>Mr. Hat:<td>Well, Kyle. No!! You hear me?! You go to hell! You go to hell and you die!
    <tr><td>Mr. Garrison:<td>Hmm, guess you'll have to take your seat, Kyle.
    <tr><td>Kyle:<td>Damn it!
    <tr><td>Cartman:<td>Hah, hah. Mr. Hat yelled at you. <i>[farts fire.  Poor Pip is stunned]</i> Ow! My ass! <i>[The class gasps]</i>
    <tr><td>Kyle:<td>Dude.
    <tr><td>Stan:<td>Damn, Cartman.
    <tr><td>Cartman:<td><i>[farts fire]</i> Uh Ow! My ass!
    <tr><td>Kyle:<td>Dude, he's farting fire.
    <tr><td>Stan:<td>It's the alien anal probe. It's shooting fire from Cartman's rectum.
    <tr><td>Cartman:<td>No, that was just a dream.
    <tr><td>Mr. Garrison:<td>Eric, do you need to sit in the corner until your flaming gas is under control?
    <tr><td>Cartman:<td>No, Mr. Garrison, I'm fine. <i>[Cartman farts fire again, setting Pip aflame.  Pip runs around the room on fire.]</i>
    
    <tr><td><th>
    <table bgcolor=ffff99>
    <tr><th colspan=2>NEXT TRAIN TO DENVER
    <tr><th>DEPARTS<th><table bgcolor=black cellspacing=1 cellpadding=5><tr><th bgcolor=ffff99>&nbsp;12:30&nbsp;</table>
    <tr><th colspan=2>&nbsp;<br>LINE FORMS HERE
    </table>
    <tr><td><td bgcolor=dcba98><i>[Train station.  Cows flock in from all around and stand in line, waiting to board the train out of town]</i>
    <tr><td><th><table><tr><td bgcolor=yellow><font face=arial><big>South Park Express</table>
    <tr><td>Conductor:<td>Hey, you cows can't get on this train! This is a people train. You cows have no business on a people train, all right? 'Cause you're cows. <i>[The cows are all staring at the conductor]</i> No, no, no. Don't try any of that <i>cow</i> hypnosis on me, all right? 'Cause it's not gonna work.
    <tr><td>Officer Barbrady:<td><i>[drives by with his lights flashing]</i> Hold it right there, cows! <i>[Cows split up and run off mooing]</i> Come back here! Now then! <i>[pursues them]</i>
    
    <tr><td><td bgcolor=dcba98><i>[Cafeteria]</i>
    <tr><td><th>
    <table><tr>
    <td><table><tr><th bgcolor=gray><font face=arial size=-1>THE FOUR FOOD GROUPS</table>
    <td><table><tr><th bgcolor=yellow><font face=arial>OUT</table>
    <td><table><tr><th bgcolor=c0c0c0><font face=arial size=4>HOT</table>
    <td><table><tr><th bgcolor=red><font face=arial size=4>FOOD</table>
    <td><table><tr><th bgcolor=yellow><font face=arial>IN</table>
    <td><table bgcolor=black><tr><th bgcolor=yellow><font face=arial size=-2>SCHOOL FOOD<br>IS<br>GOOD FOOD</table>
    </table>
    <tr><td>Kid 1:<td>So then I had 
    <tr><td>Kid 2:<td>Ya, seriously, killer.
    <tr><td>Cartman:<td><i>[farts fire]</i> Oh!! Dude, I sure am hungry.
    <tr><td>Stan:<td>How can you eat when you're farting fire?
    <tr><td>Cartman:<td>Shut up, dude, you're being totally immature.
    <tr><td>Kyle:<td>Hey, look, there's Wendy Testaburger.
    <tr><td>Stan:<td><i>[gasps]</i> Where? <i>[He finds himself looking right at her.  An epiphany plays while hearts dance around Stan's head.  Stan smiles, and it soon goes from ear to ear]</i>
    <tr><td>Cartman:<td><i>Stan wants to ki-iss Wendy Testabur-ger.</i> 
    <tr><td>Stan:<td>Shut up, fat ass! I don't even like her!
    <tr><td>Cartman:<td>I'm not fat and you obviously like her because you throw up every time she talks to you.
    <tr><td>Stan:<td>I <i>do not</i>.
    <tr><td>Wendy:<td>Hi, guys.
    <tr><td>Kyle, Cartman:<td>Hi, Wendy.
    <tr><td>Wendy:<td>Here, Stan. This is for you. <i>[hands Stan a note]</i>
    <tr><td>Stan:<td>Bluuch!
    <tr><td>Wendy:<td>Eww! <i>[leaves]
    <tr><td>Kyle, Cartman:<td><i>[their eyes follow her out]</i> Bye, Wendy.
    <tr><td>Kyle:<td>Dude, what does the note say?
    <tr><td>Stan:<td><i>[glances at it]</i> Holy crap! It says she wants to meet me at Stark's Pond after school. <i>[a look of wonder comes over his face]</i>
    <tr><td>Kyle:<td>Whoa! Maybe you can kiss her.
    <tr><td>Cartman:<td>Or slip her the tongue.
    <tr><td>Kenny:<td>(or look at the cat on her feet, then touch her)
    <tr><td>Stan:<td><i>[that got his attention]</i> What? How do you know she has a cat? <i>[Silence, Kenny waits to see if the other guys got the message, then laughs.  The rest follow, realizing what Kenny meant]</i>
    <tr><td>Kyle:<td>Come on you guys, we need to figure out how to get out of school so we can get my little brother back.
    
    <tr><td><td bgcolor=dcba98><i>[The cafeteria kitchen. A cook stands behind a food counter, ready to serve up cafeteria food. The boys enter]</i>
    <tr><td>Chef:<td>Hello there, children.
    <tr><td>Boys:<td>Hey, Chef.
    <tr><td>Chef:<td>How are you doing?
    <tr><td>Kyle:<td>Bad.
    <tr><td>Chef:<td>Why bad?
    <tr><td>Kyle:<td>Chef, have you ever had something happen to you, but nobody believed you?
    <tr><td>Chef:<td>Oh, children, children, that's a problem we've <i>all</i> had to face at some time or another. Here, let me sing you a little song. It might clear things up.<p><i>
    I'm gonna make love to ya woman<br>
    gonna lay ya down by the fire<br>
    And caress your womanly body<br>
    make ya moan and perspire<br>
    Gonna-</i>
    <tr><td>Stan:<td>Uh, Chef.
    <tr><td>Chef:<td><i> -get those juices flowin'-</i>
    <tr><td>Stan:<td><i>Chef.</i>
    <tr><td>Chef:<td><i> -we're makin' love gravy-</i>
    <tr><td>Stan:<td>Chef!
    <tr><td>Chef:<td><i> -love gravy, lovelovelovelovelove <sup>GRAVIH</sup>!</i>
    <tr><td>Stan:<td>Chef!!
    <tr><td>Chef:<td><i> Love luh-</i> huh? <i>[Silence. Kenny nods towards Kyle]</i> Do you feel better?
    <tr><td>Kyle:<td><i>No!</i>
    <tr><td>Chef:<td>Oh, come on children, what could be so bad? It's Salisbury steak day.
    <tr><td>Stan:<td>Visitors took Kyle's baby brother.
    <tr><td>Chef:<td>What?! <i>[tosses a food tray aside and runs to the other side of the counter]</i> What the hell do you think you're doing in school eatin' Salisbury steak?! Go find him, damn it!
    <tr><td>Kyle:<td>Mr. Garrison won't let us out of school. He thinks we're making it up.
    <tr><td>Cartman:<td>You <i>are</i> making it up. <i>[farts fire.  The anal probe pops out, moves around and puts its metal arms on its hip, looking annoyed at being exposed]</i>
    <tr><td>Stan:<td>Whoa! <i>[The probe goes back into Cartman's ass.]</i>
    <tr><td>Cartman:<td>What?
    <tr><td>Kyle:<td>That was cool!
    <tr><td>Chef:<td>It's uh some kind of symbiotic, metamorphosis device. <i>[Cartman turns about so Chef can check out the probe]</i> This could mean the visitors want to communicate with us.
    <tr><td>Cartman:<td><i>[turning to face Chef, testily]</i> Oh, I see. Now you're going to join in on the little joke huh?
    <tr><td>Chef:<td>It's no joke, children, this is big!
    <tr><td>Kyle:<td>Please, Chef, if I don't get out of school and get my little brother back from the aliens, my parents are gonna disown me.
    <tr><td>Chef:<td>Uuh, hold on now, hold on now. <i>[To himself]</i> Uhyouyouyou gotta help the children.
    <tr><td>Cartman:<td>Oh, you guys sure are going a long ways to try and scare me. I want my Salisbury steak!
    <tr><td>Chef:<td><i>[pulling on the fire drill]</i> Fire drill! Fire drill! Everybody out! <i>[to the boys]</i> Okay children, this is your chance!
    <tr><td>Stan:<td>Killer! Thanks, Chef.
    <tr><td>Chef:<td>Mahahahahan oh man, first contact with the alien visitors. I've got to get myself ready.
    
    <tr><td><td bgcolor=dcba98><i>[The boys' neighborhood]</i>
    <tr><td>Boys:<td><i>We got out of school! No more school today, we got out of school</i>
    <tr><td>Cartman:<td><i>[interrupting the song with a fiery fart]</i> Oh, you guys, my ass, seriously
    <tr><td>Stan:<td>Okay, Cartman, we got out of school, you can stop farting fire now.
    <tr><td>Cartman:<td>I would if I could you son of a bitch!
    <tr><td>Kyle:<td>Okay, so how do we get my little brother back?
    <tr><td bgcolor=skyblue>Cartman:<td>Uh. Would you stop going on about your little brother? I know it was just a dream, I know I didn't have an anal probe, and I know that I'm not under alien control! <i>[a radio wave strikes Cartman and he gets big blushy cheeks and starts to sing.]</i><p><i>
    I love to singa!<br>
    About the moona and June-a and the springa<br>
    I love to singa<br>
    about a sky of blue-a or a tea for two-a<p>
    [A second radio wave reverts him to normal and all is quiet.  Dogs bark in the background]</i>
    <tr><td>Stan:<td>What the hell was that?
    <tr><td>Kyle:<td>He <i>is</i> under alien control. That thing in his butt is linked up to the visitors!
    <tr><td>Cartman:<td>Ah, son of a bitch! You guys, shut up. I'm not under alien control.
    <tr><td>Kyle:<td><i>[Into Cartman's ear.  His voice echoes]</i> Hey!
    <tr><td>Cartman:<td>Uh.
    <tr><td>Kyle:<td>If you visitors can hear me- <i>[the voice echoes in Cartman's head]</i>
    <tr><td>Cartman:<td>Hey.
    <tr><td>Kyle:<td>-bring me back my little brother, God damnit!
    <tr><td>Cartman:<td>Ow! <i>[faces Kyle]</i> That hurts, you buttlicker!
    <tr><td>Stan:<td><i>[notices a spaceship hovering overhead]</i> Kyle, look! It's them.
    <tr><td>Kyle:<td>Give me back my brother! <i>[throws a rock at the spaceship. It fires back with a flash of light, hitting Kenny and knocking him into the road.]</i>
    <tr><td>Stan:<td>Oh my God! They've killed Kenny!
    <tr><td>Kyle:<td>You bastards! Come back here! Coomme baack! <i>[the spaceship leaves]</i> Damn it, we were so close!
    <tr><td>Stan:<td>Hey look, <i>[Kenny gets up]</i> I think Kenny's okay.
    <tr><td>Kenny:<td>(Don't worry, I'm alright. Aaaah!) <i>[fleeing cows run over Kenny]</i>
    <tr><td>Stan:<td>Owww.
    <tr><td>Kenny:<td><i>[gets up again]</i> (Nope, I'm fine. Ah!) <i>[Officer Barbrady mows him down.  Kenny ends up along the curb, lifeless. The boys approach]</i>
    <tr><td>Stan:<td>Wow, poor Kenny.
    <tr><td>Kyle:<td>Now do you believe us, Cartman?
    <tr><td>Cartman:<td>No!
    <tr><td>Kyle:<td>Cartman, they killed Kenny!
    <tr><td>Cartman:<td>He's not dead.
    <tr><td>Stan:<td>Dude, Kenny is dead! <i>[picks up a stick and hits Kenny's bloody body]</i> See?
    <tr><td>Cartman:<td>Shut up, you guys.
    <tr><td>Kyle:<td>He's dead, Cartman! <i>[Pulls Kenny's head off his body]</i>
    <tr><td>Cartman:<td>God damn it, I didn't have an anal probe! <i>[walks off]</i> Screw you guys, I'm goin' home.
    <tr><td>Kyle:<td>Go on and go home, you fat chicken!
    <tr><td>Cartman:<td><i>[off screen]</i> Dildo!
    <tr><td>Kyle:<td>You're all I have left, Stan.
    <tr><td>Stan:<td>Sorry, dude. I gotta go meet Wendy Testaburger.
    <tr><td>Kyle:<td>You can't! Poor Ike must be so scared, up there all alone. You gotta help me, dude! <i>[Rats feast upon Kenny's body.]</i>
    <tr><td>Stan:<td>Dude, like Chef says, I've gotta get a piece of lovin' while the gettin's hot. <i>[hurries away]</i>
    <tr><td>Kyle:<td><i>[Rats drag Kenny's head off]</i> Rats.
    
    <tr><td><td bgcolor=dcba98><i>[Cartman's house]</i>
    <tr><td>Ms. Cartman:<td>Hello, Eric
    <tr><td>Cartman:<td>Hi, mom!
    <tr><td>Ms. Cartman:<td>How are you doing?
    <tr><td>Cartman:<td>Well, I'm pissed off!
    <tr><td>Ms. Cartman:<td>Here, I made you powdered donut pancake surprise.
    <tr><td>Cartman:<td>I don't want powdered donut pancake surprise. All the kids at school call me fat!
    <tr><td>Ms. Cartman:<td>You're not fat, you're big boned.
    <tr><td>Cartman:<td>That's what I said.
    <tr><td>Ms. Cartman:<td>You can have an eensy weensy bit, can't you?
    <tr><td>Cartman:<td>No!
    <tr><td>Ms. Cartman:<td>Just a weensy geensy woo woo?
    <tr><td>Cartman:<td>No! Leave me alone, mom! <i>[walks past her]</i>
    <tr><td>Ms. Cartman:<td>How about a nice chocolate chicken pot pie, then?
    <tr><td>Cartman:<td><i>[stops in his tracks]</i> What? Well, that does sound pretty good. <i>[returns to sit on the sofa while his mom goes off to get the pie]</i> Uh, mom?
    <tr><td>Ms. Cartman:<td>Yes, hon?
    <tr><td>Cartman:<td>If anybody calls or comes over, I'm not here, okay?
    <tr><td>Ms. Cartman:<td>Sure, hon. You want some cheesy poofs, too?
    <tr><td>Cartman:<td>Yeah, I want cheesy poofs.
    
    <tr><td><td bgcolor=dcba98><i>[Stark's Pond. Kyle decided to join Stan]</i>
    <tr><td>Kyle:<td>Well, it looks like she's not going to show up, Stan. Let's go look for the visitors now.
    <tr><td>Stan:<td>But her note said she'd be here.
    <tr><td>Wendy:<td>Hi, Stan.
    <tr><td>Stan:<td>Bluuch.
    <tr><td>Wendy:<td>Eww!
    <tr><td>Kyle:<td>You can't talk to Stan, Wendy. He throws up when you do.
    <tr><td>Wendy:<td>But why, Stan?
    <tr><td>Stan:<td><i>[tries to hold it in, but]</i> Bluuch.
    <tr><td>Wendy:<td>Eww!
    <tr><td>Kyle:<td>Look, can you guys just get down to business so we can go find my little brother.
    <tr><td>Wendy:<td><i>[turns to Kyle]</i> Huh?
    <tr><td>Kyle:<td>Just make sweet love down by the fire.
    <tr><td>Wendy:<td>What happened to your little brother?
    
    <tr><td><td bgcolor=dcba98><i>[Cartman's house. Cartman is on the sofa watching TV]</i>
    <tr><td>Reporter:<td>As the reports of UFO sightings increase, more mysterious crop circle patterns are appearing in fields all around South Park. These crop circles, when viewed from above, form strange patterns. <i>[a plane circles around a field with odd patterns on it, and a cameraman pans out to reveal the outline of --- Cartman!]</i>
    <tr><td>Cartman:<td>Hey, that kind of looks like Tom Selleck.
    <tr><td>Reporter:<td>Could it be that aliens are trying to make contact with us, here on earth?
    <tr><td>Kitty:<td>Meow.
    <tr><td>Cartman:<td><i>[notices his kitten eyeing his pot pie]</i> No, kitty, this is mah pot pie.
    <tr><td>Kitty:<td>Meow.
    <tr><td>Cartman:<td>No, kitty, that's a bad kitty!
    <tr><td>Kitty:<td>Meow.
    <tr><td>Cartman:<td>No, kitty, it's mah pot pie!
    <tr><td>Kitty:<td>Hiss.
    <tr><td>Cartman:<td>Mom! Kitty's being a dildo!
    <tr><td>Ms. Cartman:<td><i>[peeks in suggestively]</i> Well, then. I know a certain kitty kitty who's sleeping with Mommy tonight.
    <tr><td>Cartman:<td><i>[confused]</i> What?
    
    <tr><td><td bgcolor=dcba98><i>[Stark's Pond. Kyle is explaining what happened to his little brother]</i>
    <tr><td>Kyle:<td>and now I have to go home without him and my parents are going to have me killed.
    <tr><td>Wendy:<td>Well, why don't you go get the fat kid?
    <tr><td>Kyle:<td>Why?
    <tr><td>Wendy:<td>Well, if the fat kid has something implanted in his ass, maybe the visitors are using him as part of their plan. You should use the fat kid as bait to bring them back.
    <tr><td>Kyle:<td>Hey. You're right, Wendy. Come on, Stan, we have to go get Cartman. <i>[moves out]</i>
    <tr><td>Wendy:<td>Come on, Stan. <i>[walks past him, following Kyle]</i>
    <tr><td>Stan:<td>Bluuch.
    <tr><td>Wendy:<td>Eww! <i>[walks away]</i>
    <tr><td>Stan:<td>Hey, wait. When do I get to make sweet love? <i>[A bird flies into his puke and starts waddling around in it.]</i>
    
    <tr><td><td bgcolor=dcba98><i>[Cartman's House, a short time later]</i>
    <tr><td>Kitty:<td>Meow.
    <tr><td>Cartman:<td>No, Kitty, you can't have any!
    <tr><td>Kitty:<td>Meow.
    <tr><td>Cartman:<td>No, Kitty, this is mah pot pie. Bad kitty! <i>[Cartman farts fire, setting the cat ablaze]</i> Eh, 'scuse me, Kitty.
    <tr><td>Ms. Cartman:<td><i>[enters the room with Kyle, Stan and Wendy]</i> Eric, look who's here.
    <tr><td>Cartman:<td>Dude, weak mom.
    <tr><td>Kyle:<td>Come on Eric, we can go play at the bus stop.
    <tr><td>Cartman:<td>I can't, my mom said
    <tr><td>Ms. Cartman:<td>That's okay, Eric, I think you need to go spend time with your little friends.
    <tr><td>Cartman:<td><i>[Quietly]</i> But mom, I don't want to spend time with my little friends.
    <tr><td>Ms. Cartman:<td>Don't be difficult, Eric! Now, you go out and play in the fun snow.
    <tr><td>Cartman:<td>God - damn it! <i>[Kitty then runs by in flames.]</i>
    
    <tr><td><td bgcolor=dcba98><i>[Forest at night. Cartman's right foot is tied to a tree]</i>
    <tr><td>Cartman:<td>You guys, I have to get home.
    <tr><td>Stan:<td>Don't be such a fraidy cat, Cartman. This rope will make sure they can't take you on board again.
    <tr><td>Cartman:<td><i>[kicks his foot to try to get loose]</i> Oh, man, this sucks.
    <tr><td>Kyle:<td>How come the visitors aren't coming for him?
    <tr><td>Stan:<td>I think we have to signal them somehow.
    <tr><td>Cartman:<td><i>[farts fire]</i> Ow!
    <tr><td>Wendy:<td>Hey, he's like Rudolph.
    <tr><td>Kyle:<td>Yeah, all you have to do is fart some more, Cartman! And the visitors are sure to come!
    <tr><td>Cartman:<td>Really? Uh, I don't think I have to fart anymore tonight.
    <tr><td>Kyle:<td>Sure you do!
    <tr><td>Stan:<td>Come on Cartman, fart!
    <tr><td>Cartman:<td>I don't wanna.
    <tr><td>Stan:<td>He can't hold it in forever.
    <tr><td>Kyle:<td>Fart, damn you!
    <tr><td>Cartman:<td>Okay, that's does it! Now listen! Why is it that everything today has involved things either going in or coming out of my ass?! <i>[Farts.  An anal probe comes out of his butt and expands]</I> I'm sick of it! It's completely immature.
    <tr><td>Stan:<td>Hey, it's happening again. <i>[the probe is now a large satellite dish]</i>
    <tr><td>Kyle:<td>Whoa, look at that.
    <tr><td>Stan:<td>Now, do you believe this, Cartman?
    <tr><td>Cartman:<td>You guys can't scare me! I know you're making it all up.
    <tr><td>Stan:<td>Cartman, there's a 80-foot satellite dish sticking out of your ass!
    <tr><td>Cartman:<td>Sure, you guys, what-ever. <i>[the dish sends a radio signal out to space]</i>
    
    <tr><td><td bgcolor=dcba98><i>[Chef's backyard. He's sitting in a lawn chair with a can of ZOOP in his hand. An Igloo cooler is next to him]</i>
    <tr><td><th><table cellpadding=10><tr><th bgcolor=white><font face=arial>WELCOME<br>VISITORS</table>
    <tr><td>Chef:<td>Oh, boy. The aliens are going to make first contact. Hey, down here, we are ready for your wisdom! <i>[looks at his watch]</i> And you've only got 20 minutes before Sanford and Son is on.
    
    <tr><td><td bgcolor=dcba98><i>[Forest]</i>
    <tr><td>Cartman:<td>You guys, I am seriously getting pissed off right now! I know there is no such things as aliens! <i>[Three small ships descend, followed by a mothership.]</i> Oh, God damn it!
    <tr><td>Mr. Garrison:<td><i>[driving by, he stops]</i> What the? I tell you, there's some crazy stuff going on in this town.
    <tr><td>Mr. Hat:<td>You can say that again, Mr. Garrison.
    <tr><td>Kyle:<td>Come down here, you stinking aliens! <i>[Four aliens appear]</i> Uh, uh.
    <tr><td>Stan:<td>Go on, Kyle, ask 'em for your little brother back.
    <tr><td>Kyle:<td>Vi, Visitors, this morning you took my little brother, Ike. He's the little freckled kid that looks like a football. At first, I was happy you took him away. But I've learned something today. That having a little brother is a pretty special thing.
    <tr><td>Stan:<td>Yeah.
    <tr><td>Kyle:<td>Ah, heck, Mr. Visitors, I'm just a kid all alone in this crazy world, but if you could find it in your hearts or whatever you have, to give my brother back to me, it sure would make my life brighter again.
    <tr><td>Stan:<td>That was beautiful, dude.
    <tr><td>Kyle:<td>Did it work?
    <tr><td>Stan:<td>No, they're leaving.
    <tr><td>Kyle:<td>Hey, you scrawny-eyed shithead, what the fuck is wrong with you?! You must be some kind of fucking asshole to be able to ignore a crying child!
    <tr><td>Stan:<td>Whoa, dude!
    <tr><td>Kyle:<td>You know what you assholes like! You like to _____ and sh___ and _____ and _____ and _____ and _____!
    <tr><td>Stan:<td>Hey Wendy, what's a _____? <i>[she shrugs]</i>
    <tr><td>Ike:<td><i>[The spaceship door opens]</i> Help me doy tair.
    <tr><td>Kyle:<td><i>Ike, jump down, now! For the love of God, Ike, JUMP!</i>
    <tr><td>Ike:<td>Don't harm me. <i>[a herd of cows runs away from the ship, but a trio of aliens stops them in their tracks.  The cows moo and quiver with fear until the middle alien raises its hand and addresses them]</i>
    <tr><td>Alien:<td>
    <table><tr><td>Moo MooMooMoo<td><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>GREETINGS, COWS OF EARTH<br>WE COME IN PEACE.</font></table></table>
    <tr><td>Cows:<td>
    <table><tr><td>Moo??<td><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>REALLY??</font></table></table>
    <tr><td>Kyle:<td>Come on, Ike! I promise I'll be nice to you from now on!
    <tr><td>Ike:<td>Don't kick the baby.
    <tr><td>Alien:<td>
    <table>
    <tr><td>Moo moo, moo.<th><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>WE HAVE EXPERIMENTED WITH ALL<br>THE BEINGS OF EARTH,</font></table>
    <tr><td>Moo moo, moo. Moo.<th><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>AND WE HAVE LEARNED THAT YOU</font>
    <tr><th bgcolor=black><font face=arial color=white>ARE THE MOST INTELLIGENT<br>AND WISE.</font></table>
    </table>
    <tr><td>Cartman:<td>What the hell are they talking about?
    <tr><td>Cow:<td>
    <table><tr><td>Moo moo?<td><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>WHY DID YOU TURN SOME OF US<br>INSIDE OUT?</font></table></table>
    <tr><td>Alien:<td>
    <table><tr><td>Moo moo, moo. Moo.<td><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>OH, THAT WAS CARL'S FAULT. HE'S NEW.</font></table></table>
    <tr><td>Alien Carl:<td>
    <table><tr><td>Moomoomoo.<td><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>YEAH, SORRY ABOUT THAT, MY BAD!</font></table></table>
    <tr><td>Kyle:<td>Ike!
    <tr><td>Alien:<td>
    <table>
    <tr><td>Moo moo.<th><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>TAKE THIS DEVICE.</font></table>
    <tr><td>Moo moo. Moo.<th><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>IT'S A GIFT FROM US.</font></table>
    </table>
    <tr><td><td><i>[The cows look at each other and moo in agreement.]</i>
    <tr><td>Kyle:<td>Ike! Do your impersonation of David Caruso's career!
    <tr><td>Ike:<td>It's my turn! <i>[dives into the snow.  The satellite goes back into Cartman's butt.]</i>
    <tr><td>Alien:<td>
    <table><tr><td>Moo moo. Moo moo.<td><table bgcolor=white><tr><th bgcolor=black><font face=arial color=white>FAREWELL COWS, PEACE BE WITH YOU!</font></table></table>
    <tr><td><td><i>[The aliens disappear.  The spaceship pulls Cartman up but the rope keeps him grounded.]</i>
    <tr><td>Cartman:<td>You guys, get me down from here! <i>[farts fire, burns the rope.  The tractor beam takes him into the ship and the spaceship flies away.]</i> Ow! Help! Sons o' bitches! Dildos!
    <tr><td>Stan:<td>Phew, I'm sure glad that's over with.
    <tr><td>Kyle:<td>Yeah. Boy, am I glad to see you, Ike.
    <tr><td>Ike:<td>Oh, he fly out of the sky.
    
    <tr><td><td bgcolor=dcba98><i>[Chef's Backyard.]</i>
    <tr><td>Chef:<td>Wait, where are you going, alien visitors? Come back!
    <tr><td>Blonde:<td><i>[arrives with a brunette]</i> Well, Chef, where's this amazing thing you were going to show us.
    <tr><td>Chef:<td>Well, it's in the bedroom, ladies. Come on in.
    
    <tr><td><td bgcolor=dcba98><i>[Forest]</i>
    <tr><td>Kyle:<td>Come on, Ike, we can make it just in time for dinner. <i>[they leave]
    <tr><td>Stan:<td>Thanks for your help, Wendy.
    <tr><td>Wendy:<td>Whatever, dude.
    <tr><td>Stan:<td>Hey, I didn't throw up.
    <tr><td>Wendy:<td>Cool! <i>[She's happy now. They both look at each other like they're going to kiss, and that music plays again. Wendy puckers up. Stan gets queasy]
    <tr><td>Stan:<td>Bluuch! <i>[right on her face]
    <tr><td>Wendy:<td>Eww!
    <tr><td>Stan:<td>Sorry.
    <tr><td>Wendy:<td>Hey, look. A french fry.
    <tr><td>Stan:<td>Cool.
    <tr><td>Wendy:<td>And what is that?
    <tr><td>Stan:<td>I think it's part of a cheesy poof. <i>[Chef's song starts up and the camera pulls away.]</i>
    <tr><td>Wendy:<td>Hey, what's that?
    <tr><td>Stan:<td>That's uummm a hamburger from that's from, like, two days ago.
    <tr><td>Wendy:<td>Hey, what about that?
    <tr><td>Stan:<td>I don't know <i>what</i> the hell <i>that</i> is!
    
    <tr><td><td bgcolor=dcba98><i>[Bus Stop]</i>
    <tr><td>Stan:<td>Gee, the bus'll be here any minute, and Cartman still isn't around.
    <tr><td>Kyle:<td>Yeh, we're running out of friends.
    <tr><td>Stan:<td>I wonder what that thing was that the visitors gave the cows.
    
    <tr><td><td bgcolor=dcba98><i>[Cows out on a pasture]</i>
    <tr><td>Cows:<td>Mooo.
    <tr><td bgcolor=blue><font color=white>Officer Barbrady:</font><td>Ha ha cows! I've got you cornered. Let's see you get away now. <i>[One of the cows step on the plate on the alien device.  A bolt of lightning strikes Officer Barbrady.  His glasses fly off, and cheeks become rosy.]<p>I love to sing-a<br>about the moon-a and the June-a and the Spring-a<br>I love to sing-a<br>'bout a sky of blue-a or a tea for two-a<p>[Cows begin hopping about gleefully]</i>
    
    <tr><td><td bgcolor=dcba98><i>[Bus Stop, next day. Cartman falls out of the sky, landing on his side next to Kyle and Stan.]</i>
    <tr><td>Cartman:<td>Puh.
    <tr><td>Stan:<td>Oh, hey Cartman.
    <tr><td>Kyle:<td>Wow Cartman, the visitors dropped you off just in time to go to school.
    <tr><td>Cartman:<td>Ah, man, I had this crazy nightmare last night.
    <tr><td>Stan:<td>Really, what about?
    <tr><td>Cartman:<td>Well, I was standing out in a field, and I had this huge satellite dish sticking out of my butt. And then there were hundreds of cows and aliens, and then I went up on the ship and Scott Baio gave me pinkeye.
    <tr><td>Stan:<td>That wasn't a dream, Cartman. That really happened.
    <tr><td>Cartman:<td>Oh, right. Why don't I have pinkeye then?
    <tr><td>Kyle:<td>Cartman, you <i>do</i> have pinkeye!
    <tr><td>Cartman:<td>Ahh, son of a bitch!
    <tr><td><td><i>[End of <b>Cartman Gets An Anal Probe</b>]</i>
    </table></body></html>
    


```python
# Try this with Pandas (given that the scipt is already a table)
import pandas as pd
script_list = pd.read_html(script_url)
print(type(script_list))
script_df = script_list[0]
print(type(script_df))
print(script_df.head())
print(script_df.tail())
```

    <class 'list'>
    <class 'pandas.core.frame.DataFrame'>
          0                                                  1    2    3    4   \
    0    NaN                                  [At the bus stop]  NaN  NaN  NaN   
    1  Boys:       School day, school day, teacher's golden ru…  NaN  NaN  NaN   
    2  Kyle:  Ah, damn it! My little brother's trying to fol...  NaN  NaN  NaN   
    3   Ike:                                        Zeeponanner  NaN  NaN  NaN   
    4  Kyle:  Ike, you can't come to school with me. [Ike ch...  NaN  NaN  NaN   
    
        5    6    7    8    9    10   11   12   13  
    0  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    1  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    2  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    3  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    4  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
               0                                                  1    2    3   \
    453     Stan:  That wasn't a dream, Cartman. That really happ...  NaN  NaN   
    454  Cartman:          Oh, right. Why don't I have pinkeye then?  NaN  NaN   
    455     Kyle:                      Cartman, you do have pinkeye!  NaN  NaN   
    456  Cartman:                               Ahh, son of a bitch!  NaN  NaN   
    457       NaN                [End of Cartman Gets An Anal Probe]  NaN  NaN   
    
          4    5    6    7    8    9    10   11   12   13  
    453  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    454  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    455  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    456  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    457  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  NaN  
    


```python
#Remove NaN Columns from DataFrame
script = script_df.iloc[:,0:2]
print(script.head())
print(script.tail())
```

           0                                                  1
    0    NaN                                  [At the bus stop]
    1  Boys:       School day, school day, teacher's golden ru…
    2  Kyle:  Ah, damn it! My little brother's trying to fol...
    3   Ike:                                        Zeeponanner
    4  Kyle:  Ike, you can't come to school with me. [Ike ch...
                0                                                  1
    453     Stan:  That wasn't a dream, Cartman. That really happ...
    454  Cartman:          Oh, right. Why don't I have pinkeye then?
    455     Kyle:                      Cartman, you do have pinkeye!
    456  Cartman:                               Ahh, son of a bitch!
    457       NaN                [End of Cartman Gets An Anal Probe]
    


```python
#Add column Names
script.columns = ['Character', 'Dialogue']
print(script.head())
print(script.tail())
```

      Character                                           Dialogue
    0       NaN                                  [At the bus stop]
    1     Boys:       School day, school day, teacher's golden ru…
    2     Kyle:  Ah, damn it! My little brother's trying to fol...
    3      Ike:                                        Zeeponanner
    4     Kyle:  Ike, you can't come to school with me. [Ike ch...
        Character                                           Dialogue
    453     Stan:  That wasn't a dream, Cartman. That really happ...
    454  Cartman:          Oh, right. Why don't I have pinkeye then?
    455     Kyle:                      Cartman, you do have pinkeye!
    456  Cartman:                               Ahh, son of a bitch!
    457       NaN                [End of Cartman Gets An Anal Probe]
    


```python
#Remove rows not associated with a Character or Dialogue ()
script = script.dropna()
print(script.head())
print(script.tail())
```

      Character                                           Dialogue
    1     Boys:       School day, school day, teacher's golden ru…
    2     Kyle:  Ah, damn it! My little brother's trying to fol...
    3      Ike:                                        Zeeponanner
    4     Kyle:  Ike, you can't come to school with me. [Ike ch...
    5  Cartman:                    Yeah, go home you little dildo.
        Character                                           Dialogue
    452  Cartman:  Well, I was standing out in a field, and I had...
    453     Stan:  That wasn't a dream, Cartman. That really happ...
    454  Cartman:          Oh, right. Why don't I have pinkeye then?
    455     Kyle:                      Cartman, you do have pinkeye!
    456  Cartman:                               Ahh, son of a bitch!
    


```python
#Iterate through all the rows and pull the 'Cartman:' dialogue and store in a list - there might be a Pandas way to do this better
cartman = []
for row in script.index.values:
    if script.loc[row,'Character'] == 'Cartman:':
        cartman.append(script.loc[row, 'Dialogue'])

print(len(cartman))
print(cartman[0:5])
print(cartman[-5:-1])
```

    85
    ['Yeah, go home you little dildo.', 'I know what it means!', "I'm not telling you.", "Heyeah, that's what Kyle's little brother is all right! [Kyle swings Ike by his feet, knocking Cartman down] Ow! [Ike laughs]", "That's 'cause I was having these… bogus nightmares."]
    ['Puh.', 'Ah, man, I had this crazy nightmare last night.', 'Well, I was standing out in a field, and I had this huge satellite dish sticking out of my butt. And then there were… hundreds of cows and aliens, and then I went up on the ship and Scott Baio gave me pinkeye.', "Oh, right. Why don't I have pinkeye then?"]
    


```python
#Iterate through the list and remove all words in brackets [], these are action notes and not dialogue.  
import re

pattern = '\[.*?\]'
for index in range(len(cartman)):
    #don't make it over work?
    if re.search(pattern, cartman[index]):
        cartman[index] = re.sub(pattern, '', cartman[index])
    
print(len(cartman))
print(cartman[0:5])
print(cartman[-5:-1])
```

    85
    ['Yeah, go home you little dildo.', 'I know what it means!', "I'm not telling you.", "Heyeah, that's what Kyle's little brother is all right!  Ow! ", "That's 'cause I was having these… bogus nightmares."]
    ['Puh.', 'Ah, man, I had this crazy nightmare last night.', 'Well, I was standing out in a field, and I had this huge satellite dish sticking out of my butt. And then there were… hundreds of cows and aliens, and then I went up on the ship and Scott Baio gave me pinkeye.', "Oh, right. Why don't I have pinkeye then?"]
    


```python
#For kicks we will cut and paste and grab 'character', this time also pulling action
#Iterate through all the rows and pull the 'Boys:' dialogue and store in a list - there might be a Pandas way to do this better
#ALos remove all words in brackets [], while we are at it.  

import re

character = 'Chef:'
dialogue = []
pattern = '\[.*?\]'

for row_index in script.index.values:
    if script.loc[row_index,'Character'] == character:
        dialogue.append(re.sub(pattern, '', script.loc[row_index, 'Dialogue']))

print(len(dialogue))
print(dialogue[0:5])
print(dialogue[-5:-1])
```

    25
    [' Hello there, children.', "Well, today it's Salisbury steak with buttered noodles and a choice of green bean casserole… or vegetable medley.", 'Say, did any of you children see the alien space ship last night?', 'Oh, was it the ones with the big long heads and the black eyes?', 'Oh! Did they give you an anal probe?']
    [' Fire drill! Fire drill! Everybody out!  Okay children, this is your chance!', "Mahahahahan oh man, first contact with the alien visitors. I've got to get myself ready.", "Oh, boy. The aliens are going to make first contact. Hey, down here, we are ready for your wisdom!  And you've only got 20 minutes before Sanford and Son is on.", 'Wait, where are you going, alien visitors? Come back!']
    


```python
# Looks like we have function, TODO: remove colon from character

def get_character_dialogue(character, script):
    '''
       Retrieve the 'character' dialogue from the 'script'
       character: string
       script: pandas data frame
       
       Return: list of dialogue strings
    '''
    #TODO: Once more cleaning has been done on the Panda's side, this next line shoule not be required.
    character = character.title() + ":"
    
    #Initialize a list to return
    dialogue = []
    pattern = '\[.*?\]'
    
    for row_index in script.index.values:
        if script.loc[row_index, 'Character'] == character:
            dialogue.append(re.sub(pattern, '', script.loc[row_index, 'Dialogue']))
            
    return dialogue
```


```python
#Test the function
cartman_dialogue = get_character_dialogue('cartman', script)

from pprint import pprint
pprint(cartman_dialogue)
```

    ['Yeah, go home you little dildo.',
     'I know what it means!',
     "I'm not telling you.",
     "Heyeah, that's what Kyle's little brother is all right!  Ow! ",
     "That's 'cause I was having these… bogus nightmares.",
     'Well, I dreamt that I was lying in my bed…  in the dark. When all of a '
     'sudden this bright blue light filled the room . Then slowly my bedroom door '
     'begin to open  and the next thing I remember I was being drug through a '
     'hallway.  Then I was lying on a table  and these scary hands wanted to '
     'operate on me. And they had big heads and big black eyes…',
     'What?',
     'No, it was just a dream, my mom said so.',
     "Oh, shut up guys! You're just trying to make me scared. And it's not "
     'working.',
     'Kick ass.',
     'What?',
     "Eh, no, that, that was just a dream… and I'm not fat, I'm big boned!",
     'Oh!',
     'Oh!',
     'No! Uh-I mean, eh, why would they do that?',
     'No!',
     'Shut up dildo!',
     'Oh!',
     "God damn it, they didn't do anything to my ass. It was just a dream.",
     'Shut up!',
     "Shut up you guys it's not working.",
     "Somebody's baking brownies. ",
     " Heh, heh, that's a, that's, that's a little joke. Heh, heh.",
     'Hah, hah. Mr. Hat yelled at you.  Ow! My ass! ',
     ' Uh… Ow! My ass!',
     'No, that was just a dream.',
     "No, Mr. Garrison, I'm fine. ",
     ' Oh!! Dude, I sure am hungry.',
     "Shut up, dude, you're being totally immature.",
     'Stan wants to ki-iss Wendy Testabur-ger.',
     "I'm not fat… and you obviously like her because you throw up every time she "
     'talks to you.',
     'Or slip her the tongue.',
     'You are making it up. ',
     'What?',
     " Oh, I see. Now you're going to join in on the little joke huh?",
     'Oh, you guys sure are going a long ways to try and scare me. I want my '
     'Salisbury steak!',
     ' Oh, you guys, my ass, seriously…',
     'I would if I could you son of a bitch!',
     'Uh. Would you stop going on about your little brother? I know it was just a '
     "dream, I know I didn't have an anal probe, and I know that I'm not under "
     'alien control!  I love to singa! About the moona and June-a and the springa '
     'I love to singa about a sky of blue-a or a tea for two-a… ',
     "Ah, son of a bitch! You guys, shut up. I'm not under alien control.",
     'Uh.',
     'Hey.',
     'Ow!  That hurts, you buttlicker!',
     'No!',
     "He's not dead.",
     'Shut up, you guys.',
     "God damn it, I didn't have an anal probe!  Screw you guys, I'm goin' home.",
     ' Dildo!',
     'Hi, mom!',
     "Well, I'm pissed off!",
     "I don't want powdered donut pancake surprise. All the kids at school call me "
     'fat!',
     "That's what I said.",
     'No!',
     'No! Leave me alone, mom! ',
     ' What? Well, that does sound pretty good.  Uh, mom?',
     "If anybody calls or comes over, I'm not here, okay?",
     'Yeah, I want cheesy poofs.',
     'Hey, that kind of looks like… Tom Selleck.',
     ' No, kitty, this is mah pot pie.',
     "No, kitty, that's a bad kitty!",
     "No, kitty, it's mah pot pie!",
     "Mom! Kitty's being a dildo!",
     ' What?',
     "No, Kitty, you can't have any!",
     "No, Kitty, this is mah pot pie. Bad kitty!  Eh, 'scuse me, Kitty.",
     'Dude, weak mom.',
     "I can't, my mom said…",
     " But mom, I don't want to spend time with my little friends.",
     'God - damn it! ',
     'You guys, I have to get home.',
     ' Oh, man, this sucks.',
     ' Ow!',
     "Really? Uh, I don't think I have to fart anymore tonight.",
     "I don't wanna.",
     "Okay, that's does it! Now listen! Why is it that everything today has "
     "involved things either going in or coming out of my ass?!  I'm sick of it! "
     "It's completely immature.",
     "You guys can't scare me! I know you're making it all up.",
     'Sure, you guys, what-ever. ',
     'You guys, I am seriously getting pissed off right now! I know there is no '
     'such things as aliens!  Oh, God damn it!',
     'What the hell are they talking about?',
     "You guys, get me down from here!  Ow! Help! Sons o' bitches! Dildos!",
     'Puh.',
     'Ah, man, I had this crazy nightmare last night.',
     'Well, I was standing out in a field, and I had this huge satellite dish '
     'sticking out of my butt. And then there were… hundreds of cows and aliens, '
     'and then I went up on the ship and Scott Baio gave me pinkeye.',
     "Oh, right. Why don't I have pinkeye then?",
     'Ahh, son of a bitch!']
    

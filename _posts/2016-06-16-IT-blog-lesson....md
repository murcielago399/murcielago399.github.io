---
title: IT blog lesson...
layout: post
source-id: 1m94TZEvP-Vzdh3gBEXFT69tyNs2Yhi2L0wxykoo0dME
published: true
---
In the lesson I learned that to update which was what I thought literally an updated chunk of code but actually turned out to be a piece in the chunk of code. my mistake was to put the + or - piece in first… This is how you can find it... You first have to take the piece that says '**Object = update**'  then add the chunk to the object side first, **before** you add the update as the problem is that the boolean piece does not allow you to access the + and the - piece. However do not fear if you do the **object** piece first instead of the **update** piece it allows you to not use the boolean piece but to access the + and  - chunks. I learned this while coding in the lesson when it said **update** the code to - I could just not find the minus. 

In the lesson I still had hope that the BBC microbits could come. But no another week passes and another week that there is no sign of them. The con of the lesson is that went off the tab after coding worst snake ever but when I came back it had all gone all that work a lesson worth  of coding you could say so I had to do all of it again  here's the coding I lost.

Worst snake ever

function onStart(  ) {

	globals.score = 1000;

	globals.posX = 0;

	globals.posY = 4;

	globals.appleX = 4;

	globals.appleY = 3;

	globals.level = 0;

	while (globals.level < 10) {

		

		microbit.on(globals.posX, globals.posY);

		wait(100);

		microbit.off(globals.posX, globals.posY);

		wait(100);

		microbit.on(globals.posX, globals.posY);

		microbit.on(globals.appleX, globals.appleY);

		if (( globals.posX == globals.appleX ) && ( globals.posY == globals.appleY )) {

			

			microbit.draw(Pattern("01010.01010.00000.10001.01110"));

			wait(300);

			globals.level = globals.level + 1;

			globals.appleX = Random.number(0, 4);

			globals.appleY = Random.number(0, 4);

			microbit.clear();

			

		}

		

		if (( microbit.tiltX > 2 ) && ( globals.posX <= 1 )) {

			

			microbit.off(globals.posX, globals.posY);

			globals.posX = globals.posX - 1;

			

		}

		

		if (( microbit.tiltX < 2 ) && ( globals.posX <= 3 )) {

			

			microbit.off(globals.posX, globals.posY);

			globals.posX = globals.posX + 1;

			

		}

		

		if (( microbit.tiltY > 1 ) && ( globals.posY >= 2 )) {

			

			microbit.off(globals.posX, globals.posY);

			globals.posY = globals.posY - 1;

			

		}

		

		if (( microbit.tiltY < 2 ) && ( globals.posY <= 3 )) {

			

			microbit.off(globals.posX, globals.posY);

			globals.posY = globals.posY + 1;

			

		}

		

		globals.score = globals.score - 1;

		

	}

	

	microbit.say(globals.score);

	

}


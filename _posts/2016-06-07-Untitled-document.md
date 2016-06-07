---
title: Untitled document
layout: post
source-id: 1Ehi03H000grcfQH7V_GQlwS-hBOk7lTrcy64pw6-goI
published: true
---
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


---
title: microbit tutorials
layout: post
source-id: 18rafFc3Ae5MesMOeqDE4edALn6FVY8bqP79Zr_qzgP4
published: true
---
At the start of the lesson we received some boxes to do with computing as we carried them out of the store room we were all excited as we opened them we realize that they were not the microbit that we had waited for weeks to get as we unwrapped a box we realize that it was not the microbit's but was infact something that looked abit like a fax machine!

Fortune teller

//      When the BBC micro:bit runs.

function onStart(  ) {

	microbit.say("Press A", 10);

	

}

function onPressA(  ) {

	globals.answer = Random.number(0, 1);

	if (globals.answer == 0) {

		

		microbit.say("no");

		

	}

	

	

}

    


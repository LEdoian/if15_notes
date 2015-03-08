Arduino
=======
Software
--------
- Arduino IDE
	- Je spíš editor
	- Umí nastavit externí editor - pak jen hlídá změny na disku
	- Podporuje rozšíření
	- Umí rozdělit sketch do více souborů
		- Před kompilací si vypíše jména fcí a deklaruje je; poté záložky seřadí podle abecedy (nespolehlivé)
	- Lze jej ovládat z příkaozvé řádky
- CodeBender
	- Webové IDE pro Arduino, pomocí doplňku
	- https://codebender.cc/
	- Umí se např. spojit s účtem GitHubu
- Eclipse
	- Potřebuje k sobě Arduino IDE a plugin
- Visual Pro Micro
	- Placené rozšíření Visual Studia
	- SW Debugger - podporuje přímo Atmel instrukce
		- Breakpointy je potřeba definovat v době kompilace (před kompilací, ne až za běhu)
		- HW debugger - debugWire od Atmelu
			- AVR studio, GDB
			- Kompatibilní s Arduinem

Hardware
--------
- Vlastní shieldy
	- Knihovny přímo pro shieldy
	- Prototypový shield
		- Pozor na I2C a ISP (programování procesoru) piny a napájení (3.3V je proudově omezené)
- Vlastní klon Arduina
	- Minimální Arduino:
		- ATMega, napájení, reset, připojení k PC, ISP
		- Pro Arduino-kompatibilitu je potřeba nahrát bootloader (přes ISP) pro programování ze sériové linky
			- Pro programování lze použít i jiné Arduino, podporováno Arduino IDE

Opouštíme Arduino
-----------------
- Pod Arduino IDE jsou standardní základy
	- Lze používat i jiné nástroje (není potřeba používat Arduino IDE)


# weather
A bash script that reports the weather from Swedish airports

![Screendump of weather.sh](http://fileadmin.cs.lth.se/cs/Personal/Peter_Moller/scripts/bilder/weather2.png)

Note:
-----
Since this script is only applicable in Sweden, the rest of the comments are in Swedish. If you are interested, please email me!

More information is available at http://cs.lth.se/peter-moller/script/weathersh/

#Funktion
Scriptet tar flygplats som inparameter och läser sedan METAR-strängen från `aro.lfv.se`. En METAR-sträng ser ut som `ESMS 230950Z 17009KT CAVOK 16/14 Q1013` och det är väl kryptiskt, varför detta script finns. Dessa uppgifter uppdateras två gånger i timmen av personal på flygplatsen eller (på mindre flygplatser) av automatiska avläsare.

Flygplatsen kan anges enligt `ICAO`(”ESMS”), `IATA`(”MMX”) eller bara flygplatsens namn (”Malmö”).

Följande rapporteras:
 - Temperatur **inklusive** vindavkylning!
 - Vindriktning, både i grader och i bokstäver
 - Relativ fuktighet
 - Lufttryck

*Om flygplatsen är Sturup redovisas f.n. även cykelinformation för de som cyklar till/från Södra Sandby. Detta skall ändras till en generell funktion någon gång i framtiden... :-)*

#Optioner
`-f flygplats` anger vilken flygplats man får rapportering om (ICAO, IATA eller bara flygplatsens namn)  
`-u` uppdaterar scriptet till senaste version  
`-d` slår på debug-information

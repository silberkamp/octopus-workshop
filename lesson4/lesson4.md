# Kapitel 4: Leuchtende LEDs

Wir verlassen mal kurz den Computer und schauen uns die Welt da draußen an. Programmierer sollen schließlich Lösungen für Probleme in der realen Welt finden.

Schauen wir uns ein Auto an. Ein Auto ist ein sogenanntes "Objekt". Jedes Auto hat bestimmte "Attribute". Das sind zum Beispiel:

* Farbe
* Leistung (PS)
* Höchstgeschwindigkeit
* Marke
* ...

Jedes Auto unterscheidet sich von anderen Autos durch diese Attribute. Sicher fallen dir noch weitere ein. Alle Autos haben aber auch Gemeinsamkeiten. Wenn du ein Ding an der Straße siehst, sagt dein Gehirn sofort "Das Objekt ist ein Auto". Man könnte sagen, alle Auto-Objekte gehören zur "Klasse" mit dem Namen "Auto". Sie haben Gemeinsamkeiten: Vier Räder, Fenster, Scheibenwischer, Motor, ...

Alle Auto-Objekte haben auch Funktionen, die man mit ihnen nutzen kann:

* gas geben
* links lenken
* rechts lenken
* bremsen
* ...


Das Konzept von "Klassen" (der gemeinsame Bauplan) und Objekten gibt es auch in der Programmierung. Diese Idee hat sich durchgesetzt, weil man damit im Zusammenspiel mit realen Gegenständen einfach programmieren kann.

### Die LED als Objekt

Das erste Objekt, das wir erzeugen möchten, stammt von der Klasse `neopixel` ab. Das ist der Name der kleinen Lampen, die auf dem Octopus verbaut sind.

Diese Lämpchen bestehen eigentlich aus 4 kleinen Lämpchen, die zusammengebaut sind: Eine für Rot, eine für Grün, eine für Blau und eine für Weiß. Man nennt sie daher RGBW-LED. 

Im folgenden Programmschnipsel musst du nicht sofort alles verstehen. Die ersten Zeilen importieren sogenannte "Bibliotheken". Das sind Programmteile, die andere für uns gebaut haben. So müssen wir uns nicht mit den technischen Details der Lämpchen befassen und können unsere Lampen zum Blinken bringen.

Dann folgt die Erzeugung des Objekts `leds` aus der Klasse `neopixel` (ignoriere die Dinge in den Klammern erstmal).

In den nächsten Zeilen werden in den Klammern die Farbwerte für rot, grün, blau, weiß gesetzt. 0 bedeutet aus, 255 ist die höchste Stufe.

Ganz am Ende des Programms wird die Methode `leds.write()` ausgeführt (denk an das Autobeispiel. `write` ist eine Funktion, die das Objekt beherrscht). 

```python
import time
import machine, neopixel

leds = neopixel.NeoPixel(machine.Pin(13), 2, bpp=4)


leds[0] = (255,255, 0,0)
leds[1] = (255,255,0,0)

leds.write()

```

Jetzt ist es Zeit, mit den Lampen zu experimentieren und dich an die Schreibweise zu gewöhnen. Du kannst dazu die Konsole unten im Programm nutzen. Führe das Programm aus, schreibe dann zum Beispiel

```python
leds[0] = (255,0,0,0)
```

und danach `leds.write()`. Suche dir eine Farbkombination, die du gern anzeigen möchtest.

Im nächsten Kapitel lassen wir die Lampen blinken.

# Kapitel 6: Temperaturen lesen

In diesem Kapitel soll der auf dem Octopus eingebaute Sensor zum Einsatz kommen. Er kann Temperatur, Luftfeuchte und Luftdruck messen. Dafür sind nur wenige Zeilen Code nötig.

Bevor es losgehen kann, brauchen wir eine Bibliothek -- also eine Schnittstelle, um mit dem Sensor zu sprechen. Aber der Reihe nach: Lege in der Programmierumgebung eine Datei an, nenne sie zum Beispiel "sensortest.py". Lege gleich eine weitere Datei und nenne sie "bme.py". Der Sensor heißt BME280, daher der Name.

Öffne jetzt im Browser [diesen Link](https://raw.githubusercontent.com/robert-hh/BME280/master/bme280_float.py). Er führt direkt zur Bibliothek. Markiere alles und kopiere es heraus (Strg+C). Füge den ganzen Inhalt in die Datei "bme.py" ein und speichere. Achte darauf, dass das Board angeschlossen und verbunden ist. Damit die Bibliothek auf den Octopus kommt, musst du sie jetzt hochladen. Während die Datei geöffnet ist, klicke oben im Menü auf "Tools", dann auf "Download". Nach wenigen Sekunden ist die Bibliothek im Speicher des Octopus.

## Daten auslesen

Wechsel jetzt zur anderen Datei. Sie soll unser Programm enthalten. Zu Beginn müssen wir die Module "machine" und "bme" laden. Zweiteres haben wir ja gerade heruntergeladen:

```python
import machine
import bme

i2c = machine.I2C(scl=machine.Pin(5), sda=machine.Pin(4))
bme = bme.BME280(i2c=i2c, address=0x77)
```

In den anderen beiden Zeilen passiert folgendes: Erst erzeugen wir ein Objekt mit dem Namen `i2c`. Das ist der Name für ein Verbindungsstandard für Sensoren. Nichts, worüber wir uns Gedanken mahen müssen -- das haben andere für uns erledigt. Die letzte Zeile erzeug ein neues Objekt `bme` aus der Klasse `BME280()`. Mit dem Objekt können wir jetzt arbeiten.

Wir hatten ja schon gelernt, dass Objekte im Programmcode immer auf Dinge in der realen Welt verweisen, in unserem Fall ist es der Sensor. Du findest ihn auf dem Octopus ganz oben in der Mitte, beschriftet mit "BME280".

Das Auslesen ist jetzt einfach. Wir wollen die Messwerte in die Variable `messwerte` schreiben:

```python
messwerte = bme.values
```

Diese können wir uns jetzt mal auf die Kommandozeile schreiben:

```python
print(messwerte)
```

Das Ergebnis steht in Klammern und enthält drei Werte. Anhand der Einheiten kannst du leicht herausfinden, was was ist. Versuche mal, anhand einer Wetterseite wie "wetter.de" herauszufinden, wie genau der Sensor den Luftdruck gemessen hat (anders als Temperatur und Luftfeuchte ist der Luftdruck drinnen und draußen identisch).

Zum Schluss dieses Kapitels können wir die Werte in drei Variablen speichern. Für die Temperatur geht das so:

```python
temperatur = messwerte[0]
```

Sicherlich schaffst du es, die Variablen `feuchte` und `druck` ebenfalls zu befüllen.


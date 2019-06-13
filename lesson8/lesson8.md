# Kapitel 8: Lautstärke auswerten

Für die Lautstärkeampel müssen wir die Lautstärke irgendwie messen. Dafür gibt es einen Sensor, den wir erst anschließen müssen. Verbinde das Kabel mit dem weißen Stecker (man kann ihn nur in eine Richtung aufstecken). Verbinde dann das Kabel mit der linken Buchse des Octopus.

Das Auslesen ist denkbar einfach. Der Sensor verändert seinen elektrischen Widerstand, wenn es lauter wird. Um diese Information auszuwerten, müssen wir einen sogenannten Analog-Digitalwandler des Octopus nutzen. Dieser gibt uns eine Zahl, mit der wir arbeiten können. Der Code ist schnell geschrieben:

```python
import machine
import time

sensor = machine.ADC(0)

while 1:
    loudness = sensor.read()
    print(loudness)
    time.sleep_ms(500)

```

Zunächst laden wir zwei System-Klassen `machine` und `time`. Dann wird ein Objekt für den Sensor erzeugt. Jetzt beginnt eine Endlosschleife, in der ein Wert aus dem Sensor ausgelesen und ausgegeben wird. Anschließend wartet der Code eine halbe Sekunde.

# Kalibrieren

Die Zahlen haben noch keine Einheit. Ist es still, kommt eine 0 zurück, der maximale Wert wäre 1024. Experimentiert entwas mit verschiedenen Lautstärken. Simuliert einen lauten Unterricht und schaut, was der Sensor misst.

Ihr könnt auch mit dem kleinen Drehregler auf dem Sensor experimentieren. Mit einem kleinen Schraubendreher kann man ihn bewegen. Je weiter er aufgedreht ist, desto höher werden die Zahlwerte.

# Ampel

Eine Ampel könnt ihr mit dem bisherigen Wissen leicht bauen. Tipp: Mit If-Abfragen könnt ihr auf Schwellwerte reagieren und die LEDs einschalten.

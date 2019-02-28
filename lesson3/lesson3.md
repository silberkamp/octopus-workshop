# Kapitel 3

Programmierer sind faul. Bei jeder gestellten Aufgabe überlegt der Programmierer sofort, wie er sie mit möglichst wenig Arbeit lösen kann. Alle Programmiersprachen (auch diese wurden von ebenso faulen Programmierern erfunden) haben deshalb Funktionen, um den Computer die Arbeit machen zu lassen.

Nehmen wir an, wir wollen die Zahlen von 1 bis 10 auf die Kommandozeile schreiben. Das könnten wir so anstellen:

```python
print(1)
print(2)
print(3)
print(4)
print(5)
print(6)
print(7)
print(8)
print(9)
print(10)
```

Selbst mit Kopieren und Einfügen ist das eine sinnfreie Arbeit. Das geht natürlich besser. Python kennt das Konzept der sogenannten "while-Schleife". Die wird solange ausgeführt, wie eine Bedingung erfüllt ist.

Zunächst legen wir eine Variable an `zahl = 1` und geben ihr den Wert 1. Dann kommt `while`, gefolgt von der Bedingung. Schaue dir den folgenden Codeschnipsel an:

``` python

zahl = 1
while zahl < 10:
  print(zahl)
  zahl = zahl + 1

print("Ende")
```

Eigentlich ganz einfach zu verstehen. Die Bedingung lautet `zahl < 10`. Das Programm beginnt, setzt `zahl` auf 1, kommt bei der Schleife an. 1 ist kleiner als 10. Also beginnt der eingerückte Code. Die Zahl wird ausgegeben. Danach bekommt `zahl` einen neuen Wert: `zahl + 1`, also den alten Wert plus 1.

Das Programm fängt wieder bei `while` an und prüft wieder. `zahl` ist jetzt 2, also immer noch kleiner als 10. Die Schleife wird noch einmal ausgeführt. Wenn die Bedingung nicht mehr gilt, hört das Programm auf und führt den Code nach der Schleife aus. Es zeigt "Ende".

### Finde den Fehler

Das Programm hat noch einen Fehler. Die Aufgabe war, die Zahlen von 1 bis 10 anzuzeigen. Bei 9 hört das Programm aber auf. Finde den Fehler und korrigiere ihn.

## Wenn / Dann

Bisher liefen unsere Programme von vorne bis hinten durch. Die Codezeilen werden nacheinander ausgeführt. Das muss aber nicht sein. Programmiersprachen kennen das Konzept `if`. Genau wie bei der `while`-Schleife, überprüft der Computer eine Bedingung und führt den Code danach nur dann aus, wenn sie erfüllt ist. Das folgende Programm soll "volljährig" anzeigen, wenn die Variable `alter` größer als 17 ist:

```python
alter = 15

if alter > 17:
  print("volljährig")
  
print("Ende des Programms")  
```

Ändere `alter` auf eine größere Zahl und plötzlich taucht "volljährig" auf.

## Bedingungen

Neben ">" (größer als) kann man eine Bedingung auch mit "<" (kleiner als) oder mit "==" (ist gleich) zusammenbauen. Achtung: Bei Bedingungen (also in der `if`-Anweisung) musst du auf Gleichheit mit "==" prüfen! Ein einfaches "=" ist beim Programmieren immer eine Variablenzuweisung!

*Aufgabe:* Es gibt auch "<=" und ">=". Kannst du herausfinden, was diese Zeichenkombinationen machen?

Im nächsten Kapitel lassen wir endlich eine Lampe auf dem IoT-Octopus blinken.

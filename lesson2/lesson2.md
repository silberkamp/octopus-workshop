# Kapitel 2: Das erste richtige Programm

Mit unserem Wissen können wir jetzt einen Rauminhalt berechnen. Nehmen wir an, der erste Raum ist 5 Meter breit, 4 Meter lang und 2,5 Meter hoch. Das können wir direkt in die Kommandozeile tippen:

```python
5 * 4 * 2,5
```

Die Schule hat aber nicht nur einen Raum, sondern vielleicht über 60. Wir wollen die Formel nicht immer wieder eingeben, das soll der Computer uns abnehmen.

Computer arbeiten mit sogenannten Variablen. Das sind Platzhalter, die man mit einem Wert füllen kann. Eine solche Variable kann man später immer wieder verwenden und der Computer rechnet mit ihrem Wert. In Python legen wir eine Variable schnell an.

```python
laenge = 4
```

Unser Minicomputer hat hinter dem Namen `laenge` die Zahl 4 gespeichert. Zwei weitere Variablen brauchen wir:

```python
breite = 5
hoehe = 2.5
```

Die Variablennamen können wir uns ausdenken – der Programmierer sollte kann sich da fast frei entfalten. Allerdings: Keine Umlaute wie ä,ö,ü,ß. Das gehört sich einfach nicht! Eine Besonderheit gibt es noch: Programmiersprachen basieren alle auf englischen Ausdrücken. Engländer und Amerikaner verwenden einen Punkt statt des Kommas. Daher `hoehe = 2.5`.

Die drei Variablen liegen jetzt im Speicher, dem sogenannten RAM. Die Computerspieler unter den Lesern wissen: Viel RAM ist wichtig, damit das aufwendige Spiele funktionieren. Jetzt wissen Sie auch, warum: Der Computer legt im RAM alle Werte ab, die während eines Programms benötigt werden. Bei einem Spiel fallen extrem viele Variablen im Speicher an.

Es ist an der Zeit, mit unseren Variablen zu arbeiten:

```python
laenge*breite*hoehe
```

Jetzt sind Sie gefragt: Ändern Sie die Werte der Variablen. Experimentieren Sie mit unterschiedlichen Werten und Rechenoperationen. Wenn Sie sich sicher im Umgang mit Variablen sind, eine kleine Aufgabe: Legen Sie die Variablen `a` und `h` für ein Dreieck an und berechnen Sie den Flächeninhalt für ein Dreieck. Wenn Sie die Formel nicht kennen: Google hilft weiter! Programmierer wissen nicht alles, sie können aber gut googlen...

## Programm speichern

Bisher haben wir die Befehle direkt in die Kommandozeile getippt. Jetzt wollen wir ein Programm abspeichern. In uPyCraft gibt es oben rechts einen Button dafür. Im oberen Bereich können wir jetzt ein Programm schreiben und es anschließend ausführen. Unser ganzes Rauminhaltsprogramm sieht so aus. Kopiert es einfach, statt es abzutippen:

```python
laenge = 4
breite = 5
hoehe = 2.5
inhalt = laenge*breite*hoehe
print(inhalt)
```

Hier kommt gleich ein neuer Befehl zum Einsatz. `print()` schreibt den Inhalt, der in den Klammern steht, auf die Kommandozeile. Führen wir das Programm aus: Rechts in uPyCraft gibt es das Dreieck mit der Spitze nach rechts. Damit startet das Programm. Wir sehen das Ergebnis! Unser Programm können wir mit dem Diskettensymbol speichern.

## Funktionen: Wiederverwendbare Programme

Bisher waren die Variablen nicht sonderlich nützlich. Das soll sich jetzt ändern. Wir wollen eine sogenannte Funktion bauen. Das ist ein Teil innerhalb eines Programms, der eine bestimmte Aufgabe löst. Man könnte sagen: Eine Funktion ist ein Werkzeug für eine Aufgabe. Einer solchen Funktion übergibt man die Daten und bekommt ein Ergebnis zurück. Die erste Funktion soll `rauminhalt()` heißen. Auch Funktionen dürfen wir frei benennen – ein sprechender Name ist hilfreich. Sonderzeichen gehören nicht in den Namen!

Eine Funktion legt man in Python mit dem Begriff `def` an. Alles, was zu der Funktion gehört, wird mit der TAB-Taste eingerückt. So sieht die Funktion `rauminhalt()` aus:

```python
def rauminhalt(l,b,h):
  i = l*b*h
  return(i)
```

Hier sind mehrere Dinge neu. Auf `def` folgt der Name. Anschließend haben wir in Klammern drei Variablen `l,b,h` angegeben. Python weiß damit, dass in die Funktion drei Werte gefüllt werden müssen. Die Werte `l`, `b` und `h` sind nur innerhalb der Funktion bekannt. Wir berechnen `i` mit der bekannten Formel. Danach kommt der Befehl `return()`. Er gibt das Ergebnis der Funktion zurück. In unserem Fall `i`, also den Inhalt.

Schauen wir, was passiert: Speichern und ausführen. Und ... nichts! Aber nicht enttäuscht sein. Bisher haben wir das Werkzeug nur angelegt, aber nicht benutzt. Das können wir ändern. Schreiben Sie am Ende eine weitere Zeile:

```python
print( rauminhalt(1,2,3) )

```

Jetzt sehen wir das Ergebnis. Unsere Funktion können wir jetzt 60, 100 oder 1000 mal mit anderen Werten ausführen. Unser Computer löst ein simples Alltagsproblem.

## Dumm bleibt der Computer dennoch

Errinnern Sie sich noch an die Einführung? Unser Computer ist vermeintlich schlauer geworden. Aber in Wahrheit versteht er nichts von dem, was er da tut. Für ihn sind 4, 5 oder 2.5 nur Zahlen. Er weiß nicht, was ein Meter ist oder ein Rauminhalt. Diese Bedeutung können nur wir Menschen den Zahlen zuweisen.

Eine Aufgabe hätten wir noch: Denken Sie an das Dreieck und bauen Sie die Funktion `dreieck(a,h)`, mit der Sie Flächeninhalte berechnen können.

In [Kapitel 3](../lesson3/lesson3.md) lernen wir, wie der Computer auf unterschiedliche Werte reagieren kann. Außerdem gibt es Tricks, um wiederkehrende Dinge immer wieder zu machen. Dann sind wir endlich bereit für bunte Lampen.

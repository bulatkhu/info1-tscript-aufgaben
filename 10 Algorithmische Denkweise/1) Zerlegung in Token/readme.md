##1) Zerlegung in Token

Unser Ziel in dieser Aufgabe ist es, mathematische Formeln etwa der folgenden Form auszuwerten: "0.3 * 4 - 7.7 / -13 + 5". Die Formel ist als Zeichenkette gegeben. Sie enthält Zahlen und Operatoren. Wir hätten gern eine Funktion function evaluate(formula), welche das Ergebnis der Berechnung zurück gibt.

Dieses Problem zerlegen wir hier in Teilprobleme. Ein wichtiger erster Schritt ist die Zerlegung der Zeichenkette in eine Sequenz von Tokens. Ein Token ist ein Operator ("+", "-", "*", "/") oder eine Zahl. Nachkommastellen sollen erlaubt sein, wissenschaftliche Notation ist optional.

Schreiben Sie eine Funktion

function tokenize(formula)
welche ein Array von Tokens zurück gibt. Die Funktion soll Leerzeichen ignorieren. Operatoren werden als Zeichenketten (etwa "+") und Zahlen als Werte vom Typ Real ausgegeben.

Beispiel: Der obige Aufruf

tokenize("-0.3 * 4 - 7.7 / -13 + 5");
soll das folgende Array zurückgeben:

["-", 0.3, "*", 4, "-", 7.7, "/", "-", 13, "+", 5]
Bei einem fehlerhaften Token wie etwa 13x $ Hallo soll die Funktion eine Exception werfen. Es geht an dieser Stelle nicht darum, die Sinnhaftigkeit der Tokens zu prüfen. Beispielsweise wäre die Eingabe "13 + * /17 --" okay.

Hinweis: Wenn s eine Zeichenkette ist, dann erhalten Sie mit s[3] den ASCII-Code (oder Unicode) des Zeichens mit Index 3. Wenn Sie das Zeichen als Zeichenkette aus nur einem Zeichen erhalten wollen, so schreiben Sie s[3:4].

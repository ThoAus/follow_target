# Aufgabenstellung

Entwicklung einer einfach aufgebauten, fahrenden Plattform, die verschiedene Steuerungssysteme testen kann. Alle für die Fahrfunktion notwendigen Komponenten sollen auf der Plattform integriert sein. Es wird eine Schnittstelle benötigt, die verschiedene Steuerbefehle aufnehmen kann.

# Aufbau

Die Plattform besteht aus:

- Einer einfachen Struktur mit Befestigungsmöglichkeiten für weitere Module
- Zwei Antriebsrädern mit jeweils eigenem Motor für unabhängigen Antrieb und Lenkung; ein drittes, frei bewegliches Rad dient als Stütze
- Einem austauschbaren Akku, der extern geladen werden kann
- Elektronik für die Steuerung und Energieversorgung

Die Abmessungen sollen etwa 100 x 100 mm betragen. Ziel ist eine möglichst kostengünstige und einfache Bauweise, um auch größere Stückzahlen fertigen zu können.

# Steuereinheiten

## Manueller Joystick mit Kabel
Basisfunktion mit einer kabelgebundenen Steuerung: Je zwei Tasten für Geschwindigkeit und Lenkung. Diese Variante dient vor allem zum Testen der Grundfunktionen. Die Taster können eventuell durch Joysticks für eine stufenlose Steuerung ersetzt werden.

## Funk-Joystick mit Lagesensor
Die Steuerung erfolgt kabellos über einen mobilen Joystick. Die Neigung nach vorne/hinten steuert Geschwindigkeit und Fahrtrichtung, seitliche Neigung die Lenkung. Am Joystick befindet sich nur ein Taster zum Zurücksetzen der Lage sowie ein Ein/Aus-Schalter. Die Übertragung zum Fahrzeug erfolgt drahtlos; am Fahrzeug wird ein entsprechendes Empfangsmodul an die Schnittstelle angeschlossen.

## Objektverfolgung mit KI-Modell
Ein Zusatzmodul mit (möglichst Weitwinkel-)Kamera wird angebracht. Darauf läuft ein kompaktes KI-Modell, das ein Zielobjekt lokalisiert. Die Steuerbefehle werden so generiert, dass das Fahrzeug dem Zielobjekt folgt: Die horizontale Position (x-Achse) steuert die Lenkung, die vertikale Position und die Objektgröße im Bild bestimmen die Geschwindigkeit.

So kann das Fahrzeug autonom einem Objekt (z. B. einem Ball) folgen. Die Geschwindigkeit hängt von der Rechenleistung und dem Ressourcenbedarf des KI-Modells ab. Nach der ersten Implementierung können Optimierungen zur Steigerung der Geschwindigkeit erfolgen. Es ist auch möglich, ein Fahrzeug mit einem Zielobjekt am Heck auszustatten, dem ein zweites Fahrzeug autonom folgt – so kann ein Konvoi gebildet werden.

Durch Anpassung des KI-Modells können weitere Szenarien umgesetzt werden, z. B. das Fahren entlang einer Markierung oder einer aufgemalten Straße.


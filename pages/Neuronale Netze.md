- # Lernprozess
	- ## Initialisierung
		- Man muss die Gewichte initialisieren (=Werte setzen). Von diesem _Standpunkt_ aus lernt das Neuronale Netzwerk.
		- Dabei sollte man **die Gewichte nicht mit 0** initialisieren, da das Netzwerk **sonst nicht lernen kann**. $$h_1=w_1 x_1 + w_2 x_2 + ... + w_n x_n$$ => wenn alle $$\vec{w}$$ mit 0 initialisiert werden, werden alle Gewichte bei der Back-Propagation gleich (da der Fehler immer gleich auf die Neuronen rückwärts verteilt wird) verteilt.
		- Man nimmt sich **Gewichte aus der Normalverteilung** **zufällig** => $$A(x_1 w_1 + ... + w_n x_n)$$, man muss Gewichte suchen, die mit der Aktivierungsfunktion $$A$$ zusammenpassen, sodass der Input der Aktivierungsfunktion **nicht zu groß oder nicht zu klein wird**.
		- Weitere Informationen gibt es [hier](https://www.deeplearning.ai/ai-notes/initialization)
		- ### TODO Xavier Initialization
		- ### TODO He Initialization
	- ## Loss function
		- Verwendet die _Loss Functions_ der klassischen Methoden.
		-
- # Aktivierungsfunktionen
	- {{embed [[Activation Functions]]}}
- # Berechnung
	- Man kann auf der CPU oder auf der GPU berechnen
		- CPU => Wenige parallele Verarbeitung, da wenig Kerne
		- GPU => Hohe parellel Verarbeitung, da sehr viele Kerne: **Es können mehrere Neuronen gleichzeitig berechnet werden**
- # Mathematische Begriffe
	- Ein neuronales Netz lässt sich wie eine **Matrix** schreiben => Die Grafikkarte kann sehr gut mit Matrizen rechnen
- # Frameworks und Implementierung
	- Die Frameworks sind der aufwendig und verteilen die Last auf die GPU (inkl. Ermittlung der idealen Berechnung anhand von Modellen).
		- PyTorch
		- **Keras** => Sehr viel wird automatisch gemacht (z.B. Konvertierungen)
		- TensorFlow
- Ist ein Ansatz des [[Supervised Learning]] zur nicht-linearen **Klassifizierung** und kann nur numerische Daten verarbeiten {{cloze deshalb müssen nicht-numerische Daten (z.B. Kategorisch) durch [[Ordinal Encoding]] umgewandelt werden}}.
- Man fügt einen neuen Datensatz in einen bereits klassifizierten Bereichen {{cloze die möglichst gleich viele Daten besitzten, da sonst die Entscheidung immer bei der Klasse mit den meisten Datensätzen liegt}} hinzu.
- Es werden die nächsten **k**-Nachbaren berechnet und dadurch ermittelt, zu welcher Kategorie der Datensatz gehört.
- ![image.png](../assets/image_1649072483326_0.png)
- Hierfür benötigt man eine **Distanzfunktion**, wie z.B. die _Euklidische Distanzfunktion_
	- Wichtig ist hierbei die [[Normierung]] der Trainigsdaten
- # Rechenaufwand
	- Man hat wenig bis keinen Trainingsaufwand {{cloze da die bestehenden Daten bereits Klassifiziert sind}} , jedoch müssen für jede Vorhersage die nächsten Nachbaren bestimmt werden => Bei großen Datensätzen hohe Laufzeitbelastung.
- # Variable k
	- Die Variable _**k**_ kann frei gewählt werden. Daraus ergibt sich folgender Zusammenhang: #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2022-04-15T08:39:25.942Z
	  card-last-reviewed:: 2022-04-11T08:39:25.943Z
	  card-last-score:: 3
		- Wenn _k_ sehr groß => Sehr Rechenaufwendig
		- Wenn _k_ sehr klein => Geringerer Rechenaufwand
	- ![image.png](../assets/image_1649141884181_0.png)
- # Variante: Weighted k-Nearest Neighbor
	- Für alle Klassen gleich viele Datenpunkte vorhanden sein => Ja mehr Punkte einer Klasse es gibt, desto mehr trägt es zum _Voting_ bei.
		- So kann der Stern als Rechteck kategorisiert werden, obwohl er näher an den Kreisen liegt, weil es insgesamt der Rechtecke gibt.
	- ![image.png](../assets/image_1649142402547_0.png)
	- Um das zu lösen, werden die Punkte nach Distanz gewichtet
- # Curse of Dimensionality
	- Der Algorithmus **kann mit hochdimensionalen Daten nicht gut umgehen**. #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-04-15T08:41:15.782Z
	  card-last-reviewed:: 2022-04-11T08:41:15.783Z
	  card-last-score:: 5
	- Je mehr Dimensionen die Datensätze haben, desto mehr Distanz entsteht zwischen den Datenpunken {{cloze exponentiell}} (siehe [[N-M-Problem]]) => Rauschen hat größere Auswirkungen => Mehr Fehler.
	- ![image.png](../assets/image_1649143356132_0.png)
- # Übungsfragen
	- Allgemeine Eigenschaften des k-Nearest Neighbor sind: #card
	  card-last-interval:: 4
	  card-repeats:: 2
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-04-16T07:09:28.465Z
	  card-last-reviewed:: 2022-04-12T07:09:28.465Z
	  card-last-score:: 5
		- Zur Klassifizierung
		- Nicht-linear
		- Nur numerische Wertebereiche
	- k-Nearest Neighbor eignet sich {{cloze nicht}} für Hochdimensionale Daten, da {{cloze nach dem _Curse of Dimensionality_ die Distanzen mit zunehmenden Dimensionen wachsen und Rauschen dadurch mehr Einfluss hat}} #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.36
	  card-next-schedule:: 2022-04-15T08:39:01.594Z
	  card-last-reviewed:: 2022-04-11T08:39:01.596Z
	  card-last-score:: 3
	- Lernt der k-Nearest Neighbor? Antwort: {{cloze Eigentlich nicht, da man nur die Distanz zu den Punkten bereits Klassifizierter Daten berechnet}} #card
	  card-last-interval:: 4
	  card-repeats:: 1
	  card-ease-factor:: 2.6
	  card-next-schedule:: 2022-04-15T08:38:30.372Z
	  card-last-reviewed:: 2022-04-11T08:38:30.373Z
	  card-last-score:: 5
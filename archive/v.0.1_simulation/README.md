# *Drone o Tron* v.0.1

Der ***Drone o Tron*** (DoT) ist einstimmiger Minisynthesizer mit Ribbonklaviatur, welche über ein Monoaudiokabel gesteuert wird. Inspiration hierfür sind der [Monotron]((https://www.korg.com/de/products/dj/monotron/index.php)) von Korg oder die [Pocket Operator](https://teenage.engineering/products/po) von Teenage Engineering. Der Synthesizer soll auf eine einzige, handliche Platine passen und mit zwei AAA-Batterien betrieben werden. Außerdem soll es einige einstellbare Effekte geben, über welche der Sound verändert werden kann.

Schritte im Projektmanagement:
- [x] Ideen sammeln
- [ ] konkrete Schaltungen finden 
- [ ] Teilschaltungen in LTSpice simulieren, um erste Konfiguration zu erhalten.

### konkrete Schaltungen finden
Als Herz des DoT soll der NE555 (Präzisionsschmitttrigger IC) fungieren, welcher in einer astabilen Kippstufenkonfiguration als VCO (voltage controlled oscillator = Spannung abh. von Eingangsspannung) über den *CV/CTRL*-Eingang betrieben wird. Die Kontrollspannung (=engl. *control voltage*, kurz *CV*) soll von einer Klaviatur kommen, welche über einen Spannungsteiler für jeden Ton eine andere Spannung erzeugt. Anschließend sollen Rechteck- (Ausgang) und Dreieckspannung (am Kondensator) abgegriffen und über ein Potentiometer gemischt werden. Schließlich soll das Signal durch einen zweipoligen Tiefpassfilter laufen, bei welchem über zwei Potentiometer Grenzfrequenz und die Stärke der Resonanz am Knickpunkt des Filters eingestellt werden können.

### Teilschaltungen in LTSpice simulieren, um erste Konfiguration zu erhalten.

Im Folgenden habe ich die Schaltungsideen in [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) in der `Simulation.asc`-Datei aufgebaut und werde hier noch ein bisschen den Aufbau erläutern.
(*Hinweis*: LTSpice ist ein Schaltungssimulationsprogramm von Analog.com, Tutorials dazu finden sich bspw. auf YouTube.)

Der NPN-BJT Q1 hat die Aufgabe, den NE555 ein- und auszuschalten.
(als krude Hüllkurve - der Ton kommt nur, wenn eine Taste gedrückt wird)
Durch die Idealität des NE555-Models kann bei der Verschaltung von Q1 
LTSpice keine Startbedingung finden, weshalb der IC direkt an GND 
hängt und nicht an Q1.
Es gibt:

- zwei Trimpotentiometer, um Feinjustierungen der Maximal- und Minimaltonhöhe vorzunehmen. (in der Simulation zwei feste Widerstandspaare)
- Potentiometer, um Tastgrad des Signals zu verändern (0-50 %)
- Potentiometer für Fade zwischen Dreieck- und Rechtecksignal
- Potentiometer für Knickfrequenz eines 2-Pol-Tiefpassfilters
- Potentiometer, um Resonanz des Filters zu ändern
- mithilfe der .param-Befehle lassen sich die Stellungen der verschiedenen Poteiometer von 0 (links) bis 1 (rechts) einstellen
- mithilfe von .step param lassen sich mehrere Simualtionen mit unterschiedlichen Parametern für die Potentiometer simulieren
- mit dem .wave Befehl wird eine .wav-Datei des Ausgangssignals erzeugt, um sich das Ergebnis anhören zu können

Die Wahl einiger Zeitkonstanten scheint vielleicht nicht sinnvoll, zielt
 aber auf eine Effizienz bei der Simulationszeit ab. 
 *Nachtrag:* Das kann auch durch einen späteren Start der Datenaufnahme in der Transientenanalyse geschehen.

Damit ist die Simulation beendet und als nächster Schritt werde ich die Schaltung auf de Steckbrett aufbauen und weiter testen und gegebenfalls erweitern.

### Achtung
Mit jegllicher Änderung am Schaltplan erlischt 
die Nutzungserlaubnis meines Namens sowie der Verwendung meiner Referenzen. Eine Nennung des Originalurhebers ist jedoch unbedingt erwünscht und entsprechend zu kennzeichnen. Eine Veröffentlichung der veränderten Schaltung muss unter derselben Creative Commons Lizens CC BY-NC-SA erfolgen. Die 
kommerzielle Nutzung ist ausgeschlossen. Alles frei nach dem Motto: Fair use only! ;-)

Open hardware FTW <3

---

## EN:
The ***Drone o Tron*** (DoT) is monophonic mini synthesizer with ribbon keyboard, which is controlled by a mono audio cable. Inspiration for this is the [Monotron]((https://www.korg.com/de/products/dj/monotron/index.php)) by Korg or the [Pocket Operator](https://teenage.engineering/products/po) by Teenage Engineering. The synthesizer is supposed to fit on a single, handy circuit board and run on two AAA batteries. There shall also be some adjustable effects through which the sound can be changed.

Steps in project management:
- [x] collect ideas
- [ ] find concrete circuits 
- [ ] simulate partial circuits in LTSpice to get first configuration.

## find concrete circuits 
The heart of the DoT will be the NE555 (precision Schmitt trigger IC), which will be operated in an astable toggle configuration as a VCO (voltage controlled oscillator) via the *CV/CTRL* input. The control voltage (*CV*) shall come from a keyboard, which generates a different voltage for each tone via a voltage divider. Subsequently, square wave (output) and triangle voltage (at the capacitor) are to be tapped and mixed via a potentiometer. Finally, the signal is to pass through a two-pole low-pass filter, where two potentiometers can be used to set the cutoff frequency and the amount of resonance at the filter's inflection point.

### simulate partial circuits in LTSpice to get first configuration

In the following I have built the circuit ideas in [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) in the `Simulation.asc` file and will explain a bit more about the setup here.
(*Note*: LTSpice is a circuit simulation program from Analog.com, tutorials can be found on YouTube for example).

The NPN-BJT Q1 has the task to switch the NE555 on and off.
(as a crude envelope - the sound only comes when a key is pressed).
Due to the idealistic nature of the NE555 model, when connecting Q1 
LTSpice can't find a start condition,so the IC is connected directly to GND 
and not to Q1.
There are:

- two trimpoteniometers to make fine adjustments of maximum and minimum pitch. (in the simulation two fixed resistor pairs)
- potentiometer to change duty cycle of the signal (0-50%)
- potentiometer for fade between triangle and square wave signal
- potentiometer for kink frequency of a 2-pole low pass filter
- potentiometer to change resonance of the filter
- using .param commands you can set the positions of different poteiometers from 0(left) to 1 (right)
- use .step param to simulate several simualtions with different parameters for the potentiometers
- with the .wave command a .wav file of the output signal is created to be able to listen to it

The choice of some time constants may not seem reasonable, but it aims at
 but aims at efficiency in simulation time. 
 *Supplement:* This can also be done by starting the data recording later in the transient analysis.

This is the end of the simulation and as a next step I will build the circuit on a breadboard and test it further and extend it if necessary.

### Attention
With any change to the schematic the permission to use 
the permission to use my name and my references.
references. A naming of the original author is however absolutely desired
and must be marked accordingly. A publication of the modified circuit must be made under the same Creative Commons license CC BY-NC-SA. A 
commercial use is excluded. All according to the motto: Fair use only ;-)

More info at: https://creativecommons.org

Open hardware FTW <3

# *Drone o Tron*

## DE:
Der ***Drone o Tron*** (DoT) ist einstimmiger Minisynthesizer mit Ribbonklaviatur, welche über ein Monoaudiokabel gesteuert wird. Inspiration hierfür sind der [Monotron]((https://www.korg.com/de/products/dj/monotron/index.php)) von Korg oder die [Pocket Operator](https://teenage.engineering/products/po) von Teenage Engineering. Der Synthesizer soll auf eine einzige, handliche Platine passen und mit zwei AAA-Batterien betrieben werden. Außerdem soll es einige einstellbare Effekte und Filter geben, über welche der Sound verändert werden kann.

Im ersten Schritt habe ich mich für einen ersten groben Aufbau der Gesamt- und Teilschaltungen, bestehend aus Klaviatur, VCO, Timbrepotentiometer und Filter, entschieden und diese mithilfe von [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) simuliert, um zum einen die Idee zu verifzieren und einen groben Aufbau zu erhalten. Die entsprechen Infos befinden sich im `.archive`-Ordner. Wer etwas Hilfe beim Verständnis für die Schaltungen benötigt, den kann ich unter anderem auf mein [praxisorierntiertes OPV-Grundlagentutorial](https://www.youtube.com/playlist?list=PLFoTc99xXplpeMX_rCe2f8oruM441F54b) auf YouTube verweisen. Nun gehts es weiter im Projektmangement:

Schritte im Projektmanagement:
- [x] Ideen sammeln, Recherche, Simulation
- [ ] Steckbrettaufbau
 
### Steckbrettaufbau
  
Grob gesagt habe ich die Schaltung einfach mal auf dem Steckbrett aufgebaut, Bauteile geändert, weitere Teilschaltungen hinzugefügt und allgemein so lange rumprobiert, bis mir die Sounds gefallen haben. Die konkreten Änderungen befinden sich in der `CHANGELOG.md`. Außerdem habe ich einige Hörbeispiele aufgenommen und mit dem Oszilloskop visualisiert, welche sich auf YouTube in meiner [*Drone o Tron*-Playlist](https://youtube.com/playlist?list=PLFoTc99xXplrwt37A0d1chDFaE8vJPAfo) befinden. Ein Bild des Steckbrettaufbaus findet sich in `beadboard_steckbrett.HEIC`. Den bisherigen Schaltplan (`schematic_schaltplan.kicad_sch`) habe ich dann noch zur besseren Übersicht mit der Schaltplan- und Boarderstellungssoftware [KiCad](kicad.org/) erstellt. Eine Playlist mit einem einfachen Grundlagentutorial findet sich -> [hier](https://www.youtube.com/playlist?list=PLFoTc99xXplq-vwjNqq9S3VKb1se5qiRt) <-

### Disclaimer
Mit jegllicher Änderung am Schaltplan erlischt 
die Nutzungserlaubnis meines Namens sowie der Verwendung meiner
Referenzen. Eine Nennung des Originalurhebers ist jedoch unbedingt erwünscht
und entsprechend zu kennzeichnen. Eine Veröffentlichung der veränderten Schaltung muss unter derselben Creative Commons Lizens CC BY-NC-SA erfolgen. Die 
kommerzielle Nutzung ist ausgeschlossen. Alles frei nach dem Motto: Fair use only! ;-)

Mehr Informationen unter: https://creativecommons.org

Open hardware FTW <3

-------

## Drone o Tron

## EN:
The ***Drone o Tron*** (DoT) is monophonic mini synthesizer with ribbon keyboard, which is controlled by a mono audio cable. Inspiration for this is the [Monotron]((https://www.korg.com/de/products/dj/monotron/index.php)) by Korg or the [Pocket Operator](https://teenage.engineering/products/po) by Teenage Engineering. The synthesizer is supposed to fit on a single, handy circuit board and run on two AAA batteries. There should also be some adjustable effects and filters through which the sound can be changed.

In the first step I decided on a first rough construction of the total and partial circuits, consisting of keyboard, VCO, timbre potentiometer and filter, and simulated these with the help of [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html), in order to verify the idea on the one hand and to get a rough construction on the other hand. The corresponding info can be found in the `.archive` folder. If you need some help to understand the circuits, I can refer you to my [praxisorierntiertes OPV-Grundlagentutorial](https://www.youtube.com/playlist?list=PLFoTc99xXplpeMX_rCe2f8oruM441F54b) on YouTube. Now it goes on in the project management:

Steps in Project Management:
- [x] Collect ideas, research, simulation
- [ ] breadboard construction
 
### breadboard construction
  
Roughly speaking, I simply built up the circuit on the breadboard, changed components, added more subcircuits and generally tried things out until I liked the sounds. The concrete changes can be found in the `CHANGELOG.md`. I also recorded some audio samples and visualized them with the oscilloscope, which are on YouTube in my [*Drone o Tron* playlist](https://youtube.com/playlist?list=PLFoTc99xXplrwt37A0d1chDFaE8vJPAfo). A picture of the breadboard can also be found under `beadboard_steckbrett.HEIC`. I then created the previous schematic (`schematic_schaltplan.kicad_sch`) with the schematic and board creation software [KiCad](kicad.org/) for a better overview. A playlist with a simple basic tutorial can be found -> [here](https://www.youtube.com/playlist?list=PLFoTc99xXplq-vwjNqq9S3VKb1se5qiRt) <-

### Disclaimer
With any change of the schematic the permission to use 
the permission to use my name and my references.
references. A naming of the original author is however absolutely desired
and must be marked accordingly. A publication of the modified circuit must be made under the same Creative Commons license CC BY-NC-SA. The 
commercial use is excluded. Everything freely after the slogan: Fair use only! ;-)

More information at: https://creativecommons.org

Open hardware FTW <3
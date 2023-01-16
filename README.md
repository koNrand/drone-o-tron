# *Drone o Tron*

Für Neulinge: Lade dieses Repository herunter, um die Dateien zu benutzen. Ein Öffnen über den Browser funktioniert in der Regel nicht! Klicke dazu auf den grünen Button 'Code' und dann auf 'Sownload ZIP'.

For newbies: Download this repository to use the files. Opening them via the browser usually does not work! Click on the green button 'Code' and then on 'Download ZIP'.

----------

english below


## DE:

Der ***Drone o Tron*** (DoT) ist einstimmiger Minisynthesizer mit Ribbonklaviatur, welche über ein Monoaudiokabel gesteuert wird. Inspiration hierfür sind der [Monotron]((https://www.korg.com/de/products/dj/monotron/index.php)) von Korg oder die [Pocket Operator](https://teenage.engineering/products/po) von Teenage Engineering. Der Synthesizer soll auf eine einzige, handliche Platine passen und mit zwei AAA-Batterien betrieben werden. Außerdem soll es einige einstellbare Effekte und Filter geben, über welche der Sound verändert werden kann.

In den Pre-Versionen bestehen aus der Simulation in [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) und dem Testaufbau auf dem Steckbrett. Wer Interesse am kompletten Prozess des Projektes hat, oder Erklärungen zu den Teilschaltungen sucht, kann im `.archive`-Ordner vorbeischauen. Ich habe dort in den `README.md` die entsprechenden Infos und auch Erklärvideos zu den groben Grundlagen verlinkt. 

Als finalen Schritt im Projektmanagement und erste Hauptversion nach Simulation und Steckbrettaufbau habe ich nun  den Drone o Tron in [KiCad](kicad.org/) Schaltplaneditor und anschließend im Boardeditor aufgebaut. Ich habe auch hier nochmal einige Änderungen vorgenommen, neue Funktionen hinzugefügt und diese in einem selbst illustrierten Platinenlayout zusammenkommen lassen.

Eine Auflistung aller Änderungen findet sich in der `CHANGELOG.md`.

Die voll funktionsfähige Platine lässt sich für den eigenen Gebrauch mithilfe der `gerberfiles_drone_o_tron_v_1_0_rev0.zip`-Dateien und dem KiCad-Projekt finden. Die Platine lässt sich damit dann bei PCB-Produzenten wie JLCPCB bestellen. Eine interaktive Aufbauhilfe (`interactive_assembly_list.html`) in Form einer .html Datei ist auch vorhanden, sodass die benötigen Bauteile auch keine Hürde darstellen. Mögliche Händler hier sind LCSC, (zugehörig zu JLCPCB, einfachste Lösung) Mouser, Reichelt, TME, uvm.

### Außer dem KiCadprojekt sind enthalten:
- einige gerenderte Aufnahmen aus der 3D-Ansicht von KiCad, welche alle 3D-Bauteilmodelle, die Illustrationen und meien favorisierte Farbe für den Lötstoplack (lila) enthalten.
- S/W Vektorgrafikaufnahmen des Boards, welceh mithilfe des Board2Pdf-Plugins erstellt wurden
- eine BOM-Tabelle (Bill of Material) aller benötigter Bauteile
- eine aussführliche Bescheibung der Berechnungen, die ich für den Spannungsteiler der Klaviatur vorgenommen habe, sodass der NE555 als wohltemperierter VCO für tonale Musik verwendet werden kann

## Disclaimer
Mit jegllicher Änderung am Schaltplan oder dem Boarddesign erlischt 
die Nutzungserlaubnis der Board-Artworks, meines Logos sowie der Verwendung meiner
Referenzen. Eine Nennung des Originalurhebers ist jedoch unbedingt erwünscht
und entsprechend zu kennzeichnen. Eine Veröffentlichung der veränderten Schaltung muss unter derselben Creative Commons Lizens CC BY-NC-SA erfolgen. Die 
kommerzielle Nutzung ist ausgeschlossen. Alles frei nach dem Motto: Fair use only! ;-)

Mehr Informationen unter: https://creativecommons.org

Open hardware FTW <3

-------

## EN:
The ***Drone o Tron*** (DoT) is monophonic mini synthesizer with ribbon keyboard, which is controlled by a mono audio cable. Inspiration for this is the [Monotron]((https://www.korg.com/de/products/dj/monotron/index.php)) by Korg or the [Pocket Operator](https://teenage.engineering/products/po) by Teenage Engineering. The synthesizer is supposed to fit on a single, handy circuit board and run on two AAA batteries. There are also supposed to be some adjustable effects and filters through which the sound can be changed.

In the pre-versions consist of the simulation in [LTSpice](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) and the test setup on the breadboard. If you are interested in the complete process of the project, or if you are looking for explanations of the subcircuits, you can have a look in the `.archive` folder. I have linked there in the `README.md` the corresponding info and also explanatory videos to the rough basics. 

As a final step in the project management and first main version after simulation and board assembly I have now built the Drone o Tron in [KiCad](kicad.org/) schematic editor and afterwards in the board editor. Again, I made some changes, added new features and let them come together in a self-illustrated board layout.

A list of all changes can be found in the `CHANGELOG.md`.

The fully functional board can be found for your own use with the help of the `gerberfiles_drone_o_tron_v_1_0_rev0.zip` files and the KiCad project. The board can then be ordered from PCB producers like JLCPCB. An interactive assembly help (`interactive_assembly_list.html`) in form of a .html file is also available, so that the needed components are no hurdle. Possible distributors here are LCSC, (belonging to JLCPCB, simpliest solution) Mouser, Reichelt, TME, and many more.

### Besides the KiCad project, included are:
- some rendered shots from the 3D view of KiCad, containing all 3D component models, the illustrations and my favorite color for the solder mask (purple).
- B/W vector graphic images of the board, which were created using the Board2Pdf plugin
- a BOM table (Bill of Material) of all needed components
- a detailed description of the calculations I did for the keyboard voltage divider, so that the NE555 can be used as a well-tempered VCO for tonal music

## Disclaimer
With any change to the schematic or the board design the usage permission of the 
the permission to use the board artwork, my logo and the use of my references.
references. A naming of the original author is however absolutely desired
and must be marked accordingly. A publication of the modified circuit must be made under the same Creative Commons license CC BY-NC-SA. The 
commercial use is excluded. Everything freely after the slogan: Fair use only! ;-)

More information at: https://creativecommons.org

Open hardware FTW <33

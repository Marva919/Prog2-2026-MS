# Blatt 01: Git Basics, Gradle

## Aufgaben

### Git

#### Git Status erklären:

Die Aussage von git Status sagt einem, das es 2 veränderte Dateien und eine neue Datei gibt, die noch nicht von der Versionskontrolle erfasst ist
und es aktuell keine geaddedten Veränderungen gibt.
Außerdem schlägt git einem vor, die Änderungen an CONTRIBUTING.md und homework/b03.md zu adden oder zu restoren und die neue Datei foo.java zu adden.

Um die Änderungen an foo.java zu commiten muss folgende Befehlssequenz ausgeführt werden:

1. git add foo.java
2. git commit -m "Topic: Added foo.java"
3. git push

#### Git-Spiel:

##### Was passierte an Tag 1:
Questlog:

In einer düsteren und mysteriösen Welt wagte sich ein furchtloser Held namens Markus in einen gefährlichen Dungeon. Es wurde erzählt, dass in diesem Dungeon Monster lauerten, die die Kerkerebenen terrorisierten. Markus war jedoch fest entschlossen, die Monster zu besiegen und das Amulet zu finden.
Mit seinem Schwert in der Hand und und einer leichten Rüstung bekleidet stieg Markus tapfer in den Dungeon ein. Schon bald stieß er auf die ersten Monster - grässliche, rattenähnliche Wesen. Mit all seiner Kraft und Entschlossenheit kämpfte Markus gegen sie und besiegte sie schließlich. Doch der Dungeon war voller Gefahren, und Markus musste tiefer absteigen, um seine Aufgabe zu erfüllen.

Hero:
Uh oh, da vorn ist eine seltsame Ratte. Sie kommt auf mich zu und greift mich an. Ich ziehe mich hinter einen Vorsprung zurück. Als sie mir nachsetzt, besiege ich sie mit meinem Schwert.
Es riecht hier irgendwie seltsam, abgestanden und moderig. Von irgendwo kommt eine schwache Beleuchtung her. Ich schleiche vorsichtig die Gänge entlang und sehe in der Ferne eine Tür.
Vorsichtig öffne ich die Tür. Direkt dahinter ist wieder eine Ratte - aber sie schläft. Ich merke, dass mein Schwert gegen ein schlafendes Monster wirkungsvoller ist.
Ich schleiche weiter, immer auf der Hut vor Monstern. Irgendwo muss es doch hier tiefer in den Dungeon gehen? Langsam bekomme ich Hunger.

Stats:
 |------------|---------------|
 | health     | 10            |
-| experience | 0             |
+| experience | 4             |
-| hunger     | 0             |
+| hunger     | 4             |
 | weapon     | sword (3 dmg) |
 | armor      | light (2 dmg) |

##### Wann hat der Held zum ersten Mal 4 experience Punkte?:
An Tag 01.3

##### Wann hat der Held zum ersten Mal 10 hunger Punkte?:
An Tag 02

##### Wie viele Heiltränke hat der Held insgesamt in seinem Rucksack gehabt?:
An Tag 03.14 1
An Tag 04.4  1
Also insgesamt 2 

#### Was hat der Held im Shop gekauft? Und wie viel Gold hat er dafür bezahlt?:
An Tag 03.9 ein Brot für 5 Gold
An Tag 03.14 ein Heiltrank für 5 Gold

#### Was passierte zwischen tag 03 und tag 04, d.h. was änderte sich zwischen diesen Commits?:
Zwischen Tag 3 und Tag 4 trift er einen Händler und kauft nach Verhandlungen bei ihm erst ein Brot und dann einen Heiltrank für jeweils 5 Gold.

#### Hat der Held etwas gegessen? Falls ja, was und wann?:
Er hat das Brot gegessen, als nachdem er es gekauft hat/von Markt weggegangen  ist an Tag 03.17

### Gradle

Über den Befehl "gradle task" kann man sich alle verfügbaren Task anzeigen lassen. 
Die Projekt stucktur ist, dass es im Hauptverzeichniss parallel zur .gitignore der Gradle Ordner und die anderen gradle Datein wie z.B. gradle.prperties liegen.
außerdem liegen auf dieser Ebene die Ordner mit den Temporären Datein. im app Ordner findet man dann den build Ordner für dei src, welche im Src Ordner liegen. 
Als dritte Datei liegt hier noch die build.gradle wodrinnen gradle konfiguriert wird.
Im Src Ordner gibt es dann noch die main und test unterordner in welchen dann wirklich die Java Klassen des Projektes und die testKlassen liegen.

Das generierte Buildskript ist in plugins, repositories, dependencies, testing, java, application und bei mir noch spotless als Plugin.
Plugins: Hier werden Erweiterungen geladen. Plugins bringen vorgefertigte Logik, Konfigurationen und neue Tasks (Befehle) in das Projekt ein.
repositories:Legt fest, wo Gradle nach externen Bibliotheken suchen soll. mavenCentral() ist das Standard-Repository für Java-Software weltweit.
dependencies: Hier werden die benötigten Bibliotheken definiert. libs.guava wird über einen Version-Catalog eingebunden und steht der Anwendung zur Laufzeit zur Verfügung.
testing: Konfiguriert die Testumgebung. Hier wird explizit JUnit 4 als Framework festgelegt.
java: Definiert die Java-Version (Toolchain). Gradle stellt so sicher, dass unabhängig vom lokalen System Java 25 zum Kompilieren genutzt wird.
spotless: Ein Plugin zur Code-Formatierung, das sicherstellt, dass der Code dem "Google Java Format" entspricht
application: Spezifische Konfiguration für das Application-Plugin (festlegen der Start-Klasse). Außerdem stellt dieses Plugin die ecessiellen Task wie run zur Verfügung und legt den Einstiegspunkt (Main) mit mainClass = 'org.example.App' fest. Diese Task werden auch mit über "gradle task" angezeigt.

Die unterschieldichen Task könne entweder über das Terminal oder in Intellij über die Pluginübersicht auf der Rechten Seite.

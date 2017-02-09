# Epidemie in Github Pages 

<h2> Gliederung </h2>
<ul>
<li><a href="#Sta">1. StarLogoTNG</a></li>
<li><a href="#Hom">2. Homogene Epidemie</a></li>
<li><a href="#Inf">3. Infektionsherd</a></li>
<li><a href="#Ans">4. Ansteckungsrate</a></li>
<li><a href="#Imm">5. Immunität</a></li>
<li><a href="#Ges">6. Gesundheitszustand</a></li>
</ul>

<h3> 
<a id="Sta">1. StarLogoTNG </a> 
</h3>
<p> StarLogoTNG ist ein Simulationsprogramm für die Blockprogrammiersprache.     
Es ist übersichtlich aufgebaut und besteht aus zwei Feldern, dem Programmierfeld und dem Spaceland, wo man die Aktionen und Fortschritte der Agenten verfolgen kann. </p>

<p> Die Agenten können mehrere Formen annehmen und so individuell eingestellt werden.      
Auch die Umgebung kann durch Gebäude, Pflanzen und andere Gegenstände ergänzt werden.      
Durch das Zusammensetzen verschiedener Böcke, die in Ordnern am Rande des Programmierfeldes untergebracht sind, kann man die Agenten zu verschiedenen Handlungen bewegen. <br>     
Diese Blöcke, welche man bei StarLogoTNG als "Variablen" bezeichnet, sind nach Verwendungszweck sortiert, zum Beispiel findet man Variablen für Gleichungssysteme im Ordner "math", der Ordner für Farben nennt sich "colors" etc. </p>

<p> Dadurch hat man also diverse Möglichkeiten, dem Spiel eine bestimmte Richtung zu geben. </p>

<p> Man kann also wie in unserem folgenden Projekt Epedemien mit Infektionsherden, Ansteckungen, Immunität und Gesundheitszuständen entstehen zu lassen, den Agenten bestimmte Aufgaben zu geben, wie etwa einen Baum in der Umgebung hochzuklettern, oder Unterhaltungen zwischen Agenten bei einer Kollision zu starten. </p>

<p> Zur vielfältigeren Gestaltung kann man die "Agenten" mischen und verschiedene Tiere und Farben einsetzen sowie im Spaceland die Sicht des Agenten und des Betrachters ein- und verstellen. <br>   
Ebenfalls im Spaceland kann man bei Betätigung des "forever"- Buttons die aktuellen Änderungen sichern und die "Agenten" beliebig agieren lassen sowie die vorher im Programmierfeld eingestellten Aktionen beobachten und Verbesserungen vornehmen. </p>

<p> Fehler in der Programmierung machen sich also gleich bemerkbar, wenn sich im Spaceland keine Änderungen zeigen oder eine Variable nicht kompatibel für einen bestimmten Block ist. Durch dieses "Schlüssel-Schloss- Prinzip" ist das Programm für Anfänger geeignet und gut verständlich. <br> 
Auch die gut sortierten Variablen und Ordner machen das Programmieren einfach. </p>

<p> Durch die vielen Gestaltungsmöglichkeiten ist StarLogoTNG sehr vielfältig nutzbar, wird aber nicht unübersichtlich, da das Programmierfeld am rechten oberen Rand nochmal in kleinerer Ausfühtung angezeigt wird, um den Überblick zu wahren, wenn die Variablen und Blöcke zu komplex werden. </p> 


<h3>
<a id="Hom">2. Homogene Epidemie </a>
</h3>
<p> Um eine homogene Epidemie zu erstellen, müssen wir zunächst eine boolsche Agentenvariable für den Zustand "ist krank" und "ist immun" einrichten. </p>

<p> Als nächsten Schritt muss eine Ansteckungswahrscheinlichkeit festgelegt werden, nach der ein gewisser Prozentsatz der Population erkrankt sein soll. <br>     
Dazu erstellen wir einen "slider"- Block, mit dem wir die "Ansteckungsrate" festlegen können. <br>
Danach setzen wir an den "slider"-Block die globale Variable "shared number" und benennen sie in "Ansteckungsrate" um.     
Den maximalen Wert setzten wir dazu auf "100". <br>     
Im Kontrollzentrum des "Spacerland" kann man nun über einen Schieberegler die Ansteckungsrate einstellen. </p>

<p> Wie mit der Ansteckungsrate, fahren wir mit der Anzahl der Giraffen, also der Populationsgröße fort.     
Mithilfe eines "Slider"-Blocks und der Bedingung "Number Agents", setzen wir die maximale Populationsgröße auf 100 Giraffen/"Agenten".   
Dafür fügen wir an den "slider"-Block an die globale Variable "shared number" und benennen sie in "Number Agents" um.       
Wie die Ansteckungsrate kann die Populationsgröße im Kontrollzentrum des "Spaceland" eingestellt werden. </p>

<p> Nun können wir mit der Programmierung der homogen verteilten Epidemie beginnen.      
Hierzu erstellen wir zunächst einen "setup"-Block, den wir in "Homogen" umbenennen.      
Damit wir bei jedem Neustart mit einer neuen Population beginnen können, setzen wir zuerst den Befehl 
"clear everyone" ein. <br>   
Somit wird bei jedem Neustart über den "Homogen"-"setup"-Block im Kontrollzentrum die alte Population gelöscht.  
Als nächstes setzen wir einen "create Agent-number-do"-Block ein. <br>    
Über das "number"-Feld können wir die Größe der kreierten "Agenten" einstellen. <br>    
Dazu setzen wir den "number Agents"-Block ein, bei dem wir die Anzahl über den Schieberegler im "Spaceland" einstellen können.      
In das "do"-Feld setzen wir zuerst den Befehl "set color"-"red" ein, damit alle gesunden "Agenten" die Farbe rot annehmen.      
Danach haben wir die Befehle "set ist krank"-"false" und "set ist immun"-"false" verwendet, um die boolschen Agentenvariabeln zu initialisieren. <br>      
Denn diese sollen für die gesunden/roten "Agenten" als falsch eingestellt sein.    
Damit ein bestimmter Prozentsatz, homogen über die Population verteilt, krank werden kann, setzen wir einen "if-test-then"-Block ein. </p>



<h3> 
<a id="Inf">3. Infektionsherd </a>
</h3>

<h3>
<a id="Ans">4. Ansteckung </a>
</h3>

<h3> 
<a id="Imm">5. Immunität </a>
</h3>

<h3>
<a id="Ges">6. Gesundheitszustand  </a>
</h3>

# Epidemie in Github Pages 

<h2><b> Gliederung</b> </h2>
<ul>
<li><a href="#Sta">1. StarLogoTNG</a></li>
<li><a href="#Hom">2. Homogene Epidemie</a></li>
<li><a href="#Inf">3. Infektionsherd</a></li>
<li><a href="#Ans">4. Ansteckungsrate</a></li>
<li><a href="#Imm">5. Immunität</a></li>
<li><a href="#Ges">6. Gesundheitszustand</a></li>
</ul>

<h3> 
<a id="Sta">1. <b>StarLogoTNG</b> </a> 
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
<a id="Hom">2. <b>Homogene Epidemie</b> </a>
</h3>
<p><img src="images/Boolsche.PNG" alt="Boolsche" style="width:172px;height:110px;border:0;"></p>

<p> Um eine homogene Epidemie zu erstellen, müssen wir zunächst eine boolsche Agentenvariable für den Zustand "ist krank" und "ist immun" einrichten. </p>

<p><img src="images/Ansteckungsrate.PNG" alt="Ansteckungsrate" style="width:268px;height:59px;border:0;"></p>

<p> Als nächsten Schritt muss eine Ansteckungswahrscheinlichkeit festgelegt werden, nach der ein gewisser Prozentsatz der Population erkrankt sein soll. <br>     
Dazu erstellen wir einen "slider"- Block, mit dem wir die "Ansteckungsrate" festlegen können. <br>
Danach setzen wir an den "slider"-Block die globale Variable "shared number" und benennen sie in "Ansteckungsrate" um.     
Den maximalen Wert setzten wir dazu auf "100". <br>     
Im Kontrollzentrum des "Spacerland" kann man nun über einen Schieberegler die Ansteckungsrate einstellen. </p>

<p><img src="images/Giraffen.PNG" alt="Giraffen" style="width:251px;height:70px;border:0;"></p>

<p> Wie mit der Ansteckungsrate, fahren wir mit der Anzahl der Giraffen, also der Populationsgröße fort.     
Mithilfe eines "Slider"-Blocks und der Bedingung "Number Agents", setzen wir die maximale Populationsgröße auf 100 Giraffen/"Agenten".   
Dafür fügen wir an den "slider"-Block an die globale Variable "shared number" und benennen sie in "Number Agents" um.       
Wie die Ansteckungsrate kann die Populationsgröße im Kontrollzentrum des "Spaceland" eingestellt werden. </p>

<p><img src="images/Homogen.PNG" alt="Homogen" style="width:608px;height:432px;border:0;"></p>

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

<p> In die "test"-Spalte setzen wir die Bedingung "random"-"100" "ist kleiner oder gleich" "Ansteckungsrate".     
In die "then"-Spalte setzen wir den Befehl "set color"-"blue" und setzen die boolsche Agentenvariabel mit "set ist krank"-"true" auf "wahr". <br>      
Wenn also die Bedingung in der "test"-Spalte zutrifft wird der Agent krank/blau. </p>

<p><img src="images/movement.PNG" alt="movement" style="width:494px;height:231px;border:0;"></p>
 
<p> Damit sich die Krankheit ausbreiten kann, erstellen wir einen "forever"-Block und setzen einen Befehl für die Bewegung nach Vorne mit 1 bis 10 Schritten durch "forward"-"random"-"10" ein. <br>    
Für die Drehung nach rechts in einem Winkel von 1-30 Grad setzen wir den Befehl "right"-"random"-"30" ein. </p>


<h3> 
<a id="Inf">3. <b>Infektionsherd</b> </a>
</h3>
<p><img src="images/Infektionsherd.PNG" alt="Infektionsherd" style="width:413px;height:248px;border:0;"></p>

<p> Um einen Agenten die Epedemie auslösen zu lassen, brauchten wir einen Infektionsherd. <br> 
Zuerst erstellten wir einen neuen Block, den wir "Infektionsherd" nannten und fügten die Variablen "clear everyone" hinzu, um mit einer neuen Population bei einem Neustart beginnen zu können. </p>

<p> Danach setzten wir unter diese Variable den Block "create agent", um den Auslöser der Epidemie zu kreieren.
Zu diesem Block kamen die Variablen "number Agent", damit wir wie bei der homogenen Epidemie die Anzahl der Agenten im Spaceland einstellen konnten. <br>
Dazu setzten wir mit "set color"-"red" die Farbe der gesunden Agenten auf rot. </p>

<p> Außerdem war ein "if then test"- Block nötig, da die Farbe sich bei einer Ensteckung ändern sollte. </p>

<p><img src="images/Gleichung Infektionsherd.PNG" alt="Gleichung Infektionsherd" style="width:1032px;height:48px;border:0;"></p>

<p> Nachdem wir dies getan hatten, erstellten wir eine lange Variable nach Vorlage des des Satzes des Pythagoras.
Sie bewirkt, dass sich nur die Agenten infizieren, die sich in einem bestimmten Bereich des "Spaceland" aufhalten. </p>

<p><img src="images/Ansteckungsrate.PNG" alt="Ansteckungsrate" style="width:268px;height:59px;border:0;"></p>

<p> Dies geschieht in Verbindung mit der Ansteckungsrate, welche wir ja im Spaceland variabel verwenden können. Wie diese Kollision zu programmieren ist, beschreiben wir im nächsten Schritt noch genauer. </p>


<h3>
<a id="Ans">4. <b>Ansteckung</b> </a>
</h3>
<p><img src="images/Ansteckung.PNG" alt="Ansteckung" style="width:558px;height:274px;border:0;"></p>

<p> Um sich gegenseitig anstecken zu können, müssen sich ein kranker und ein gesunder "Agent" begegnen.     
Wir mussten also einen "Collisions"-Blog für eine Kollision zwischen zwei Agenten verwenden.     
Um eine Bedingung für die Ansteckung einstellen zu können, setzten wir einen "if-test-then"-Block in eine freies Feld des "Collision"-Blocks. <br>     
Da sich nur "Agenten" unterschiedlicher Farbe, also unterschiedlicher Gesundheitszustände, anstecken sollen, setzten wir in das "test"-Feld die Bedingung "color of ID"-"collidee" "ungleich" "color of ID"-"ID". <br>    
Als nächstes sollen sich die "Agenten" nur zu einer bestimmten Wahrscheinlichket anstecken. Also setzten wir einen weiteren "if-test-then"-Block in die "test"-Spalte des anderen "if-test-then"-Blocks. <br>   
In die "test"-Spalte setzten wir die Bedingung "random"-"100" "ist kleiner oder gleich" "Ansteckungsrate".  
Somit erhalten wir eine Ansteckunswahrscheinlichkeit in Prozent.   
Trifft diese Bedingung zu, soll der "Agent" erkranken.   
Also setzten wir in die "then"-Spalte den Befehl "set color"-blue" und die boolsche Agentenvariable "ist krank" mit "set ist krank" auf "true". </p>

<p><img src="images/Ansteckungsrate.PNG" alt="Ansteckungsrate" style="width:268px;height:59px;border:0;"></p>

<p> Die Ansteckungsrate ist mit einem "slider"-Block im Kontrollzentrum des "Spaceland" durch einen Schieberegler einstellbar.   
Dafür setzen wir an den "slider"-Block die globale Variable "shared number" und benennen sie in "Ansteckungsrate" um. </p>

<h3> 
<a id="Imm">5. <b>Immunität</b> </a>
</h3>
<p><img src="images/Homogen.PNG" alt="Homogen" style="width:608px;height:432px;border:0;"></p>
<p><img src="images/Boolsche.PNG" alt="Boolsche" style="width:172px;height:110px;border:0;"></p>

<p> Damit wir eine Immunität einrichten zu können müssen wir eine boolsche Agentenvariable für den Zustand "ist immun" erstellen. </p>

<p><img src="images/movement.PNG" alt="movement" style="width:494px;height:231px;border:0;"></p>

<p> Die kranken Agenten sollen nach einiger Zeit zu einer bestimmten Wahrscheinlickeit wieder gesund werden.   
Daraufhin sollen sie immun sein. <br>   
Dazu setzen wir in den "forever"-Block einen "if-test-then"-Block ein. <br>    
In die "test"-Spalte setzen wir die Bedingung "random"-"100" "ist kleiner oder gleich" "Heilingschance".    
Trifft dieser ZUstand bei einem "Agenten" ein, soll er die Befehle aus der "then"-Spalte ausführen.   
Diese wären: <br> 
"Set color"-"green" und "set ist immun"-"true".  
Er soll also die Farbe "grün" für immun annehmen, weshalb wir die boolsche Agentenvariable für "ist immun" auf "true" eingestellt haben. </p>

<p><img src="images/Heilungschance.PNG" alt="Heilungschance" style="width:267px;height:57px;border:0;"></p>

<p> Die Heilungschance soll wieder mit einem Schieberegler im Spacland einstellbar sein.   
Hierzu erstellen wir einen "slider"-Block für die Heilunschance ein und setzen wieder den maximalen Wert auf "100".   
Dafür setzen wir an den "slider"-Block die globale Variable "shared number" und benennen sie in "Heilungschance" um. </p>


<h3>
<a id="Ges">6. <b>Gesundheitszustand</b>  </a>
</h3>
<p><img src="images/Gesundheitszustand.PNG" alt="Gesundheitszustand" style="width:641px;height:125px;border:0;"></p>

<p> Die "Agenten" in der Epidemie-Simulation nehmen nun nach und nach unterschiedliche Farben an (rot, blau, grün).
Damit wir die Verteilung der unterschiedlichen Gesundheitszustände (Gesund, Krank, Immun) im Blick haben können,
erstellten wir ein Säulendiagramm, in dem wir die unterschiedlichen Mengen der Gesundheitszustände mittels Säulen
in den entsprechenden Farben ablesen können. <br>   
Hierzu mussten wir zunächst einen "bar graph"-Block erstellen, den wir zuerst in "Gesundheitszustand" umbenannten.   
In den offenen "socks" konnten wir nun die Bedingungen für die einzelnen Säulen eingeben.  
Wir erstellten zuerst die Säule, die die Menge der gesunden "Agenten" angibt. <br>  
Hierzu setzten wir an der "Gesundheitszustand"-Block den Befehl "count Agent with" an. 
Die Bedingung sollte in diesem Fall sein: <br> 
"color red" "=" "color of ID"-"ID". Die Farbe des Agenten sollte also der Farbe "rot" entsprechen, um in dieser Säule gezählt zu werden.    
Ähnlich fuhren wir bei den weiteren freien Feldern des "Gesundheitszustand"-Blocks fort.    
Wir setzten wieder den Befehl "count Agent with" ein. <br>   
In dieser Säule sollte aber die Anzahl der kranken "Agenten" dargestellt werden.   
Hierzu setzten wir als Bedingung "blue" "=" "color of ID"-"ID" ein. <br>    
Für die immunen Agenten fuhren wir genau so fort, setzten jedoch als Bedingung "green" "=" "color of ID"-"ID" ein.     
Nun konnte man zu Beginn der Simulation und im laufe der Simulation die Anzahl der gesunden, kranken und immunen Agenten im "Kontrollzentrum" des "Spaceland" ablesen. <br>   
Durch Anklicken der Grafik kann der Zahlenbereich der Y- bzw. X-Achse ablesen. </p>

<p><img src="images/Grafik.PNG" alt="Grafik" style="width:620px;height:436px;border:0;"></p>

<p> Startet man die Simulation einer homogenen Epidemie sieht das Bild mit den 
<p style= "color:red;">gesunden (rot)</p> 
<p style= "color:blue;"> kranken (blau)</p>
<p style= "color:green;">immunen (grün)</p> 
"Agenten" im "Spaceland" so aus: </p>

<p><img src="images/Epidemie Grafik.PNG" alt="Epidemie Grafik" style="width:937px;height:575px;border:0;"></p>

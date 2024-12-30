Neuerungen und Bugfixes Application Shell MSS52
------------------------------------------------


32-Bit Version 2.1 /200 (09.02.2002)  
-------------------------------------

- Bugfix

    Maske "Start Application":
	
    Auf vielen Windows NT-Rechner gab es Probleme
    beim Starten von GREDI, in der Art, dass die Binär-files
    nicht gefunden wurden (Ursache : Kopplung Application Shell
    - GREDI über interne Timer).
    NEU: Kopplung GREDI - Application Shell über eine Win-API
    Funktion, welche allerdings voraussetzt, dass GREDI ein
    32Bit Programm ist. 
    BITTE: Gredi-Version 2.506 1999 oder neuer benutzen!


32-Bit Version 2.1 /199 (06.02.2001)  
-------------------------------------

- Bugfix

    Maske "Start Application":
	
    Die zuletzt eingestellte 'Data Version' wurde
    nicht gespeichert. In der Liste 'Data Version' 
    war immer 'work' eingestellt.



32-Bit Version 2.1 /198 (10.10.2000)  
-------------------------------------

- Bugfix
    Work-Verzeichnis wurde doppelt in die Liste
    "Data Version" eingetragen, wenn im Ini-File 
    der Eintrag "DataVariantDir" auf "\*.*" gesetzt war.



32-Bit Version 2.1 /197 (29.09.2000)  
-------------------------------------

- Bugfix
    diverse kleinere Fixes


Setup-Skript (06.06.2000)  
-------------------------------------

-   Neues Setup-Skript 
    (Windows95/98, Windows NT und Windows 2000 konform)


32-Bit Version 2.1 /196 (17.05.2000)  
-------------------------------------

- Neu

    Über das Menü File->Edit Configuration File kann das 
    Ini-File "appshell.ini" direkt editiert werden.
    (Voraussetzung: notepad.exe muss im Windows-Verzeichnis
    vorhanden sein.)
    


32-Bit Version 2.1 /195 (18.04.2000)  
-------------------------------------

- Bugfix

    Maske "Start Application":
    
    Es werden die Namen der Rob-Dateien für ROM1 und ROM2
    automatisch in das Gredi Set-File eingetragen, so dass auch
    ein durch einen Notabruch von Gredi beschädigtes Set-File
    verwendet werden kann. (Die Namem der Rob-Dateien werden aus
    den Namen der Binär-Files abgeleitet.)




32-Bit Version 2.1 /191 (04.01.2000)  
-------------------------------------

- Bugfix

    Maske "Start CDMS":
    
    Beim Importieren eines Datenstandes in das CDMS aus dem "Work"-
    Verzeichnis wurden die Binärfiles "mss52_m.bin" und "mss52_s.bin" 
    aus diesem Verzeichnis gelöscht.


32-Bit Version 2.1 /190 (10.12.1999)  
-------------------------------------

- Neuerung

    Maske "Select":
    
    Neue Schaltfläche zum Starten des D-Tools S54.
 
    Das D-Tool S54 muss im Ordner "c:\mss52\tools\d-tool.54\d-tool.exe"	
    installiert sein! Änderungen sind im File "c:\mss52\tools\appahell.ini"
    im Abschnitt 'RunApplication', Eintrag 'ApplicationDir2_1' möglich.


32-Bit Version 2.1 /188 (30.11.1999)  
-------------------------------------

- Neuerung

    Maske "Start M-Tool":
    
    Neuer "Program Mode" MSS52 Recycling.


    Maske "Start Application":

    Wenn ein UserRobFile angegeben ist, wird nicht mehr
    überprüft, ob sich tatsächlich auch ein Binärfile in 
    diesem Verzeichnis befindet. Wird das UserRobFile nicht
    gefunden, wird das erste Robfile verwendet, das sich
    in diesem Verzeichnis befindet.



32-Bit Version 2.1 /186 (23.11.1999)  
-------------------------------------

- Bugfix

    Maske "Start Application":
    
    Wurde in der Liste 'Selected Data Version' UMS2A oder UMS2AB
    angewählt, konnte GREDI nicht über die Schaltfläche 'Start
    Application' aufgerufen werden. Eine Fehlermeldung wurde nicht
    ausgegeben.




32-Bit Version 2.1 /185 (17.11.1999)  
-------------------------------------

- Neuerung

    Maske "Start Application":
    
    Wird das UMS mit einem GREDI-Setfile verwendet, in dem
    nur 2 ROM'S definiert sind, erfolgt jetzt eine 
    automatische Erweiterung auf 4 ROM's (das einmalige manuelle 
    Hinzufügen der UMS-Rob ist nicht mehr erforderlich).
    Soll k e i n e UMS-Rob verwendet werden, die Liste "VT"
    auf leeren Eintrag setzen. (Die Konvertierung 4 ROM's -> 2 ROM's 
    wird vom GREDI ausgeführt)

    

- Bugfix
    
    Setup:

    Beim Arbeiten unter Windows NT (Service Pack 3) trat folgender 
    Fehler auf:
    Beim Starten der Application Shell kam die Meldung:
    "oleaut32.dll out of date !"  
    -> Abhilfe Installation des Service Pack 5 für Windows NT
    Das Service Pack 5 befindet auf folgendem Server:
    \\smuc0000\win_inst\os\NT4.0\ServicePack\Sp5\I386\UPDATE\Update.exe
    (Zum Installieren des Service Packs sind Administrator-Rechte er-
     forderlich!) 

    Beim Überinstallieren der Application Shell wird nun ein Backup-
    Verzeichnis angelegt, in dem sich alle überschriebenen Dateien
    befinden, z.B. auch das File "Appshell.ini".


32-Bit Version 2.1 /180 (11.11.1999)  
-------------------------------------

- Neuerung
    Maske "Start Application":
    Um dem Anwender den Pfad für die UMS-Rob Dateien zu vereinfachen
    gibt es den folgenden neuen Eintrag im Konfigfile "Appshell.ini" 
    (im Installationsverzeichnis 'C:\mss52\tools\appshell')

    'UseShortUMSPath=0' ;
      die UMS Robdateien müssen sich im folgendem Verzeichnis befinden
      <ProjectDir>\<UMSX>\<SoftwareVariantDir>\<VTBezeichnung>\<WorkDir>
      z.B.: C:\MSS52\CDMS\UMS2ab\Bindatei\VS-k44\work\
      (wie bisher, etwas kompliziert zu merken)
    UseShortUMSPath=1':
      die UMS Robdateien müssen sich im folgendem Verzeichnis befinden
      <ProjectDir>\<UMSX>\<VTBezeichnung>\
      z.B.: C:\MSS52\CDMS\UMS2ab\VS-k44\
      (neu, etwas einfacher zu merken)

    Die Einstellung 'UseShortUMSPath=0' ist der Default und wird
    auch benutzt, wenn kein Eintrag vorhanden ist, somit können alte
    Konfigurationen ohne Änderungen weiter benutzt werden.

- Bugfix
    
    Maske "Start Application":	
    Beim Arbeiten unter Windows NT trat folgender Fehler auf:
    Bestand der Versuchsträgername "VT" aus mehr als 8 Zeichen,
    kam in der NT-Gredi Version die Meldung "Pfad ungültig !".
    (Ursache die NT-Gredi Version kann nicht mit langen Dateinamen
    umgehen.)



32-Bit Version 2.1 /173 (04.10.1999)  
-------------------------------------

- Bugfix

    Existierte das Verzeichnis "Work" nicht und wurde trotzdem 
    die Option "Save current Data Version In Work" gewählt, wurden 
    die Datenfiles nicht gespeichert. 
    Eine Fehlermeldung wurde nicht generiert!


32-Bit Version 2.1 /172 (15.09.1999)  
-------------------------------------

- Neuerungen

    Wird versucht eine zweite Instance der Application Shell zu
    starten, kommt nicht mehr die Meldung "Application Shell is
    already running!", sondern das Fenster, der bereits laufende 
    App. Shell wird angezeigt.



32-Bit Version 2.1 /164 (08.06.1999)  
-------------------------------------

- Ergänzung zu Bugfix 2.1 /163

    Timining Probleme beim Start einer 16Bit Applikation auf
    einigen NT-Rechnern.
    Über den Registry-Eintrag: 'TimerApplInterval' ist ein Timer-
    intervall frei konfigurierbar. Das Intervall ist in Millisekunden
    anzugeben. Sinnvolle Werte liegen zwischen 500 und 1000ms.
    
    Die Einstellungen werden in der Windows Registry unter
    "HKEY_CURRENT_USER\Software\VB and VBA Program Settings\Application 
    SHELL MSS52\Settings" abgelegt. 
    Der Schlüsselname ist: 'TimerApplInterval'.

    Ist in der Registry kein Eintrag gemacht, wird ein Default von
    500ms verwendet.



32-Bit Version 2.1 /163 (02.06.1999)  
-------------------------------------

- Bugfix

    Timining Probleme beim Start einer 16Bit Applikation auf
    schnellen NT-Rechnern. Beim Start von GREDI wurde das Fenster
    der Application-Shell sofort wieder geöffnet, bevor GREDI voll-
    ständig geladen war. Dieser Effekt trat zufällig auf.
     


32-Bit Version 2.1 /162 (31.05.1999)  
-------------------------------------

- Bugfix

    Maske "Start Application", unter bestimmten Umständen konnte
    GREDI ohne Auswahl eines Set-Files gestartet werden. Es wurde
    folgende Fehlermeldung ausgegeben:
          "Can't edit C:\mss52\cdms\vers320\mcs\"
    



32-Bit Version 2.1 /161 (21.05.1999)  
-------------------------------------

- Neuerungen

    Über das neue Menü "Select" kann direkt eine Maske
    gewählt werden (mit Tastatur möglich).



32-Bit Version 2.1 /160 (19.05.1999)  
-------------------------------------

- Bugfix

    Die Fehlermeldung im M-Tool: "Programmierung nicht möglich,
    da keine oder die falschen Dateien angegeben wurden. Bitte
    zuerst gültige Dateien auswählen !" erschien, wenn der Pfad-
    name für den Engine-Type länger als 8 Zeichen war.
    z.B S62B50F0001 (Das M-Tool unterstützt nur 8 Zeichen)


- Neuerungen

    Button-Leiste entspricht dem allgemeinem Windows-
    Erscheinsbild (flach, monochrom).
    


32-Bit Version 2.1 /156 (30.04.1999)  
-------------------------------------

- Bugfix


    Wurde eine User-Robdatei verwendet, ist der Pfad für 
    das Binfile in das GREDI-Setfile eingetragen wurden, obwohl
    kein Binfile verwendet wird (vergl. Neuerung 2.1/155)


32-Bit Version 2.1 /155 (29.04.1999)  
-------------------------------------

- Neuerungen
    
    Über den Eintrag:

      [User]
      UserRobFile=mk2.rob

    im Konfigfile "Appshell.ini" (im Installationsverzeichnis)
    kann eine bestimmte Robdatei für das UMS ausgewählt werden;
    in diesem Beispiel die "mk2.rob". Ein Binärfile ist nicht mehr
    erforderlich.

    (Die Neuerung von Version 2.1/154 wurde rückgängig gemacht.) 



32-Bit Version 2.1 /154 (28.04.1999)  
-------------------------------------

- Neuerungen
     
    Im GREDI-Setfile werden vorhandene Einträge für das ROM4
    nicht mehr gelöscht. 


32-Bit Version 2.1 /153 (20.04.1999)  
-------------------------------------

- Neuerungen
     
     Interne Umstellung auf Visual Basic Version 6.0,
     sollte keinerlei Auswirkung auf die Funktionalität 
     haben.

32-Bit Version 2.1 /152 (01.03.1999)  
-------------------------------------

- Bugfix

     Unter Windows NT gab es Probleme mit langen Dateinamen
     für die GREDI-Setfiles. Beim Starten von GREDI kam die 
     Fehlermeldung: das Set-File wurde nicht gefunden.	


32-Bit Version 2.1 /151 (24.02.1999)  
-------------------------------------

- Bugfix

     In der Konfigurationsdatei "appshell.ini" können im Abschnitt
     'RunApplication' die Einträge:
                                      ApplicationDir
                                      ApplicationDir1
                                      ApplicationDir2
                                      ApplicationDir3
     nun mit Kommandozeilenparameter angegeben werden. Zum Beispiel ist die 
     Angabe: "ApplicationDir2=C:\MSS52\TOOLS\D_TOOL\D_TOOL.EXE 4000" 
     jetzt möglich.


32-Bit Version 2.1 /150 (11.02.1999)  
-------------------------------------

- Bugfix

     Es wurden nicht alle Schaltflächen angezeigt (Maske "Start 
     Application"), wenn folgende Bildschirmeinstellungen gewählt
     wurden:   
     
            1024 x 768 Pixel, Schriftgrad: "Große Schriftarten" 120dpi
             800 x 600 Pixel, Schriftgrad: "Große Schriftarten" 120dpi

     Es wird jetzt bei jedem Neustart der "Application Shell" der ein-
     gestellte Schriftgrad und die Bildschirmauflösung ermittelt und 
     danach die Oberflächenelemente angepasst.

32-Bit Version 2.1 /143 (11.01.1999)  
-------------------------------------

- Bugfix

     Maske "Start Application": Beim Starten von GREDI kam die Fehler-
     meldung "Can't find 16Bit Loader !". Ursache hierfür war eine
     fehlende Systembibliothek (mfc42.dll). Dieser Fehler trat auf allen
     Rechnern auf, auf denen die Systembibliothek nicht installiert war.
     Das Setup überprüft nun, ob diese Systembibliothek installiert ist
     und kopiert diese gegebenenfalls. 


32-Bit Version 2.1 /142 (11.12.1998)  
-------------------------------------

 - Maske "Start Application" 
     Die UMS-Rob- und UMS-Binärdateien befinden sich nun an zentraler
     Stelle im Verzeichnis: "\mss52\cdms\ums*\bindatei\vt*\work".
     In diesem Verzeichnis sollte sich jeweils nur eine Rob- und eine 
     Binärdatei befinden.
     Mit der Liste "UMS" wird der UMS-Typ ausgewählt (UMS2A, UMS2AB,
     ... UMSXXXX).
     Mit der Liste "VT" kann ein Versuchsträger gewählt werden (z.B.
     VT-316).	
     Die gewählten Dateien werden in das ausgewählte GREDI-Setfile
     mit relativem Pfad eingetragen.
     W I C H T I G: Im GREDI-Setfile müssen 4 ROM'S definiert sein,
     wenn das nicht der Fall ist, erfolgt eine Hinweismeldung.	

32-Bit Version 2.1 /140 (09.12.1998)  
-------------------------------------

 - Maske "Start CDMS" 
     Es ist nunmehr möglich den Pfad für die Datenbank über die 
     Oberfläche einzustellen, damit ist es möglich eine zentrale
     Datenbank zu nutzen (Der eingestellte Pfad wird beim Verlassen
     der Maske gespeichert und beim erneuten Aufruf wieder ein-
     gestellt).	

- Bugfix

   - Eingestellte Bildschirmauflösung wurde nicht richtig erkannt,
     wenn Office-Schnellstartleiste am oberem Bildschirmrand plaziert
     wurde.

   - Logo "E-Power" wird bei einer Farbauflösung von 8 Bit (256 Farben)
     nicht mehr dargstellt (Probleme mit Farbpalettenumschaltung
     bei dieser Farbauflösung).


32-Bit Version 2.1 /135 (04.12.1998)  
-------------------------------------

- Neuerungen

    - Überarbeitete Maske "About" (mit System- und Benutzerinformationen)	


32-Bit Version 2.1 /132 (30.11.1998)  
-------------------------------------

- Neuerungen

   - Maske "Start Application" 
     
     Über die Checkbox "Download Binary Files" kann der Download der 
     Binärfiles gesteuert werden.
     - Ist diese Checkbox aktiviert ist die Bedienung wie bisher möglich.
     (Das MCS führt nach dem Online-Befehl einen Download aus.)
     - Ist diese Checkbox deaktiviert, kann nur noch die Software Variante
     in der Oberfläche ausgewählt werden (z.B Vers318). Das MCS geht nach 
     dem Online-Befehl sofort in den Meßmodus. 
     (-> Verstellen ist nicht möglich !)

     Über die Liste UMS-Rob kann eine UMS-Robdatei ausgewählt werden, die
     dann in das entsprechende GREDI-Setfile eingetragen wird. Die UMS-Robs
     müssen sich im Verzeichnis "vers*.*\ums_rob" befinden. (z.B. für den
     Programmstand 405 im Verzeichnis: "\mss52\cdms\vers405\ums_rob")
     Der Verzeichnisname "ums_rob" kann über das Konfigurationsfile 
     "C:\mss52\tools\appshell\appshell.ini" geändert werden. Dazu ist der 
     Eintrag "MeasRobFileDir" im Abschnitt "RunApplication" anzupassen !
     
     W I C H T I G: 
     Enthält das GREDI-Setfile nur zwei ROM's, so muß in dieses
     Setfile einmal die UMS-Rob manuell eingefügt werden.
     In GREDI über den  Befehl "Datei->Projekt->Beschreibungsdatei laden".
     (Die UMS-Rob braucht nicht kopiert zu werden!)
	 
 
   - Maske "Start CDMS" 
     Import von Binärfiles in CDMS:	
     Ist die Checkbox "Import Data Version into CDMS" angewählt wird das CDMS
     im Automatik-Modus gestartet. Die Maske "Datenstand importieren" ist im
     CDMS schon vorausgefüllt und muß nur noch mit OK bestätigt werden.	
     Ist die Checkbox "Import Data Version into CDMS" nicht angewählt wird das
     CDMS wie bisher gestartet.

   - Maske "Select"
     Die Schaltflächen zum Starten der Applikationen sind nur noch dann aktiv, 
     wenn auch das entsprechende Programm installiert ist.

32-Bit Version 2.1 /108 (05.11.1998)  
-------------------------------------

- Neuerungen

   - Es werden jetzt wieder alle Bildschirmauflösungen unterstützt
     (640x480, 800x600, 1024x768 Pixel)


32-Bit Version 2.1 /101 (02.11.1998)  
-------------------------------------

- Neuerungen

   - Maske "Start Application" 
     Über die Schaltfläche "Print Comment" wird die Kommentardatei
     des ausgewählten Datenstandes auf dem eingestellten Standard-
     drucker ausgegeben. 
 
   - Maske "Start M-Tool" 
     Über die Schaltfläche "Data Version Info" wird die Kommentardatei
     für den ausgewählten Datenstand angezeigt. Diese Datei kann nun auch
     über die Schaltfläche "Print Comment" auf dem eingestellten Standard-
     drucker ausgegeben werden.

 

32-Bit Version 2.1 /090 (22.10.1998)  
-------------------------------------

- Bugfixes  
   
   - Beim Laden der Maske "New Dataversion " zum Erzeugen eines neuen 
     Datenstandes kam die Fehlermeldung "Runtime Error 48, Error in 
     Loading DLL". Danach ist das Programm abgestürzt (aufgetreten auf
     Toschiba Tecra 730CDT).

- Neuerungen

   - Maske "Start M-Tool" 
     Über die Schaltfläche "Data Version Info" wird die Kommentardatei
     für den ausgewählten Datenstand angezeigt. Diese Schaltfläche ist 
     deaktiviert, wenn kein Datenstand ausgewählt ist. 

32-Bit Version 2.1 /080 (21.10.1998)  
-------------------------------------

- Bugfixes  
   
   - Beim Anwählen der Schaltfläche "Start Gredi" zum Auswählen eines
     Datenstandes kam mehrmals die Fehlermeldung "Unexpected Error".
     Nach Bestätigen dieser Meldung wurde die Maske "Start Application"
     nicht angezeigt.

- Neuerungen

   - Die Abfrage "Exit Application Shell ?" beim Schließen der 
     Application Shell wurde wieder entfernt.



32-Bit Version 2.1 /064 (20.10.1998)  
-------------------------------------

- Bugfixes  
   
   - Beim Versuch die Application Shell ein zweites Mal zu
     starten kommt die Meldung: "Application Shell is already running"	
     und danach die Frage: "Exit Application Shell ?". Wurde die zweite
     Meldung mit Nein beantwortet, ist die Application Shell trotzdem ein
     zweites Mal gestartet wurden.

32-Bit Version 2.1 /063 (15.10.1998)  
-------------------------------------

- Bugfixes  
   
   - die Liste der Gredi-Set-Files wurde nach Verlassen von GREDI und
     Erzeugen eines neuen Set-Files nicht sofort aktualisiert (Maus-
     Click auf einen Datenstand war erforderlich)	

   - Gredi-Set-File Namen dürfen mehr als 8 Zeichen, aber
     keine Leerzeichen enthalten (gültig für Windows 95)

- Neuerungen

   - Beim Start des M-Tools kann ausgewählt werden, ob "MSS52 Serie  
     Programm und Daten" oder nur "MSS52 Serie Daten" programmiert
     werden soll (Die Kreuze für die benötigten Daten im M-Tool
     werden automatisch gesetzt)

   - Über das Menü Help->ReadMe wird dieses File angezeigt (dazu muß
     der Editor 'notepad.exe' im Windowsverzeichnis vorhanden sein)


32-Bit Version 2.1 /057 (12.10.1998)  
-------------------------------------

- Bugfixes  
   
   - bei Aufruf des M-Tools wurde der Pfad für die Fixdaten nicht gesetzt 
     (MSS52 Serie -> nur Daten programmieren)	



32-Bit Version 2.1 /040 (02.10.1998)  
-------------------------------------

Für die Benutzung der 32-Bit Version ist eine Bild-
schirmauflösung von 800x600 Pixel erforderlich.
(Bei allen Toschiba Satellite Pro und Tegra möglich.)

- Bugfixes  
   
   - bei Aufruf von M-Tool und D-Tool Fehlermeldung 
     "Datei nicht gefunden", die Tools wurden aber 
     trotzdem gestartet

- Neuerungen

  - Über den Eintrag in der Konfigurationsdatei "appshell.ini"
    "ApplicationDir3=C:\Mss52\CDMS\CDMS.EXE" kann eine vierte
    Schaltfläche zum Starten der Datenbank CDMS aktiviert 
    werden, fehlt dieser Eintrag ist die Schaltfläche nicht 
    sichtbar (Istzustand nach Installation).

  - Maske "Start M-Tool" 
    Das M-Tool kann mit oder ohne eine Auswahl eines Programm- 
    und Datenstandes gestartet werden.
    Ist die Checkbox "Select Files for ECU Programming" aktiviert,
    können in gewohnter Weise wie beim Start des Applikation-
    systems "GREDI" Programm- und Datenstände ausgewählt werden.
    Ist diese Checkbox nicht angewählt, kann das M-Tool sofort ge-
    startet werden, um zum Beispiel das EWS zu synchronisieren.
    Die Programmstände werden im Verzeichnis 
    "C:\mss52\cdms\versXXX\code" erwartet und müssen mit
    "mss52_m.abs" und "mss52_s.abs" bezeichnet sein. Der Name des 
    Unterverzeichnisses "\code" ist über die Konfigurationdatei 
    "appshell.ini" einstellbar. Dazu ist der Eintrag: 
    "ProgFileDir=\code" entsprechend anzupassen. 
    Danach muß die Application Shell neu gestartet werden, damit 
    die Einstellungen übernommen werden.
    Über die Liste "Program Mode" ist die Art der Programmierung
    wählbar (MSS52 Serie, MSS52 Bootstrap, MSS52 Bootstrap+Daten).
    Ist die Checkbox "Overwrite M_Tool configurations 1/2" aktiviert,
    werden die eigenen Einstellungen überschrieben, die mit "Merke 1/2"
    im M-Tool abgespeichert wurden. Beim Aufruf von "Hole 1/2" werden 
    die Einstellungen geladen, die in der Application Shell ausgewählt
    wurden.
    
    
  -	Maske "Start M-Tool" und "Start Application" (GREDI)
  	
    Die letzten Einstellungen werden generell gespeichert, so daß entweder
    beim erneuten Aufruf der Maske und nach einem Neustart der Application
    Shell alle vorher gemachten Einstellungen wiederhergestellt werden. 
    (Die Einstellungen werden in der Windows Registry unter
    "HKEY_CURRENT_USER\Software\VB and VBA Program Settings\Application 
    SHELL MSS52" abgelegt.)  

 
  -	Maske "Start Application" (GREDI)

    Die Liste "Gredi Set File" ist vergrößert (klappt nach unten auf) und ist
    alphabetisch geordnet.
    Das Textfeld "Comment" ist vergrößert und scrollt automatisch an das Ende
    des Kommentars.

  -	Maske "Data Version" (Erzeugen eines neuen Datenstandes)

    Das Textfeld "Comment ist vergrößert und scrollt automatisch an das Ende
    des Kommentars.
    Das Datum und die Uhrzeit kann nun über die Schaltfläche "Insert Date" an
    eine beliebige Stelle des Textes eingefügt werden (Dafür den Cursor auf 
    die entsprechende Stelle setzen.)	

  
  - Maske "Select"

    Beim Starten des DS2-Tools wird das Fenster der Application Shell verkleinert. 
    Somit kann das DS2-Tool nicht doppelt gestartet werden. Nach Beendigung des
    DS2-Tools wird das Fenster der Application Shell wiederhergestellt.	


  - Beenden der Application Shell

    Eine Abfrage, ob das Programm tatsächlich geschlossen werden soll,
    wird angezeigt. Damit wird ein versehentliches Schließen vermieden.



16-Bit Version 1.0.6  (19.10.1998)  
---------------------------------

-       Über das Menü Help->ReadMe wird dieses File angezeigt (dazu muß
        der Editor 'notepad.exe' im Windowsverzeichnis vorhanden sein)

 -      Maske "Start Application" (GREDI)
  	
        Die letzten Einstellungen werden generell gespeichert, so daß entweder
        beim erneuten Aufruf der Maske und nach einem Neustart der Application
        Shell alle vorher gemachten Einstellungen wiederhergestellt werden. 

        Das Textfeld "Comment" ist vergrößert und scrollt automatisch an das Ende
        des Kommentars.


-       Maske "Data Version" (Erzeugen eines neuen Datenstandes)

        Das Textfeld "Comment ist vergrößert und scrollt automatisch an das Ende
        des Kommentars.
        Das Datum und die Uhrzeit kann nun über die Schaltfläche "Insert Date" an
        eine beliebige Stelle des Textes eingefügt werden (Dafür den Cursor auf 
        die entsprechende Stelle setzen.)
    

16-Bit Version 1.0.5  (01.10.1998)  
---------------------------------

-	Maske "Start Application" (GREDI)

        Die Liste der Gredi-Set-Files ist nun alphabetisch und nicht mehr 
        zufällig geordnet.




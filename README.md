DV4MF2 - MultiFunction Dualmode Control Panel for HAM DV modes
==============================================================

This repository contains Language support, Add-On files and other sample files for the DV4MF2 DMR Controlpanel.

To use DV4MF2 with additional languages, please create a folder "\languages" inside the program folder and download and copy the standard english language and any of your favorite languages to this folder.

The Controlpanel dynamically loads at startup available languages, the current language can be selected in the gateway tab, when language files were found in the specific folder, the program offers a selectlist instead of the default language buttons.

Starting from V2.0.0.10 the DV4MF2 control panel supports up to 10 GUI languages. Due to many requests this is just under development again, the next version 2.0.0.11 will add support for up to <b>20 languages</b> and <u>the format has been extended</u> to <b>add 35 additional customizable text elements</b>:

<b>Available languages (complete and ready for download here):</b>
- English    (build-in + language file)
- German     (build-in + language file)
- Italiano   (language file) tnx to Franco, HB9OAB
- Espaniol   (language file) tnx to Iñigo, EA2CQ
- Nederlands (language file) tnx to Rudy, PD0ZRY and Walter, PD2WGN

- native support starting from V2.0.0.11 (soon available):
- Português  (language file) tnx to José, CT1JIB
- Norsk      (language file) tnx to Gaute, LB6YD and Kai, LA3QMA
- user defined - built your own individual language file

<b>Soon available languages (under revision):</b>
- Francais   (language file) tnx to Bernard, F1UGZ (in progress, coming soon)
- Suomi      (language file) tnx to Johanna (in progress, coming soon) *update V2.0.0.11 needed, coming soon

<b><i>Languages we are looking for contributors (simply take the english file as your template):</b></i>
- Vlaams    (language file) *looking for a contributor
- Svenska   (language file) *looking for a contributor
- Dansk     (language file) *looking for a contributor
- Polski    (language file) *looking for a contributor
- русский   (language file) *looking for a contributor
- your file - please send us your translation

Installation:
==============================================================
To use DV4MF2 with foreign languages, simply create a folder "/languages" inside the program directory and copy the english language file and any language of your own choice to this folder. When running Linux please keep in mind, the folder name (lower case) and filenames (mixed case) must be written exactly in this way like the original files.

When running DV4MF2 Control Panel you'll notice, the language selection radio buttons on the "Gateway & Settings" Tab has changed to a dropdown listbox. Select your favorite language and the program will change the GUI description. Some elements have not been translated, these are either very deep coded into the program sources or this messages are replies from the DV4mini firmware.

To create your own language file please use "DV4MF2_us-ER.lng" as a template and overwrite the text elements. The syntax of the textfile is very simple, please keep in mind the following rules:
- You may use up to 20 header lines with your own comments, starting with a single hashtag '#'.
- The double hashtag '##' is being used as a line break, like for opmode and helptext elements. 
- The textarea must start with 'language:description', this is being displayed inside the dropdown list
- The file must end with '***END***' as an end tag after the last text line.

When you have finished your own textfile, please save the DV4MF2_us-ER.lng to your language directory and enjoy your own GUI.


Changelog:
==============================================================

Version 2.0.0.10a - 20160326 Easter release II coming soon!
...........................................................
- NEW:   New GUI language support (see above) for up to 20 languages!
- This release is prerequisite for using Português, Suomi, Norsk, Dansk and some more future languages.

Version 2.0.0.10 - 20160326 "Easter release" 
............................................
- NEW:   New GUI language support (see above) for up to 10 languages 
- NEW:   display UTC time in status bar now also on all windows clients
- ADDED: check for compatible dv_serial when starting program
- ADDED: important status messages (during startup) logged into info section
- FIXED: C4FM reflector display info for FCS001/FCS002 users
- FIXED: reconnect to last operating mode improved
- FIXED: better recognition when running on Debian/Raspbian

Version 2.0.0.9a - 20160902
...........................
- FIXED: talkgroup bug from first V2.0.0.9a fixed again - sorry ;-)
- FIXED: frequency display was sometimes corrupt when running with mono/linux
- FIXED: use fix IP could not be checked when local USB was selected and unchecked

Version 2.0.0.9 - 20160126
..........................
- FIXED: connect to fusion reflector FCS002 didn't work correctly

Version 2.0.0.8 - 20160124
..........................
- UPDATE: XTG Extended Talkgroup routing now available for all BM Master-Gateways
          no more need to login to the german master!

Version 2.0.0.6 - 20160123
..........................
- FIXED: Rewrite "CONNECT" to buttontext if mode changed has been fixed
- NEW:   Extended Talkgroup routing has been added, this is a complete new feature!
- NEW:   New logfile feature, log your QSO and program actions of DV4mini to a textfile
- NEW:   Additional new nice color template for GUI can be optional selected
- NEW:   Advanced debug feature, log your BER% rate to a debug file for later analysis
- ADDED: FCS0002 has been added to C4FM reflector list
- FIXED: automatic reconnect to Brandmeister at new program startup if last mode was BM
- FIXED: sometimes debug window appeared after startup
- FIXED: sometimes mode switched to compact at startup
- improved USB connect option for local USB DV4mini and windows 10
- better display of reflector names in compact mode
- optional disable reload of reflector/gateway tables
- debug option rejects program termination on missing LAN connect

Version 1.64.23.1 - 20160109
............................
- fixed a bug causing double loading of gateway masterlists for DMRplus and Brandmeister
- fixed callsign and DMRID listed in infobox correct and REFL. for reflector status msgs
- fixed button size for "Brandmeister" when language german selected, text was cut off

Version 1.64.23 - 20160108
..........................
- fixed a bug in DV Operation tab. When using on touch devices, opmode selection was improper
- connected reflector name being displayed in rx/tx status line
- show own hotspot callsign in windows status together with stick ID
- support for xref.ip (from dv4mini.exe) or DV4MF2_xref.ip for DStar XReflectors
- better highlighting of current opmode, changed color of active button
- user defined opmode logos are supported (place logos in \images folder, see sample)


Version 1.64.22.1 - 20160104
............................
- fixed an issue with opmode status display when DStar was the last active mode

Version 1.64.22 - 20160103
..........................
- first public release

----------------------------------------------------------------------------------------------
Die Funktionen des DV4Mini, die mit der DV4MF2.exe gesteuert werden können, 
sind weitestgehend identisch mit der Originalversion der DV4mini.exe (Stand: 12/2015)
Voraussetzung zum Betrieb ist der Firmware-Stand 1.6x auf dem DV4mini.

Support zur Nutzung in Verbindung mit einem Hotspot in den deutschen DMR-Amateurfunknetzen unter:
https://de.groups.yahoo.com/neo/groups/Dmrplus/info
https://de.groups.yahoo.com/neo/groups/Brandmeister/info

Installationshinweise:
http://www.dl2mf.de/blog/?p=1297

Mit der Nutzung der DV4MF2 Control Panel Software erklärt der Benutzer in allen
folgenden Punkten sein uneingeschränktes Einverständnis zu den Bedingungen für
die Nutzung und Überlassung der DV4MF2.exe, im folgenden Software genannt:

- Die hier bereitgestellte Software darf auf beliebig vielen Rechnern
  (PC, Tablet, Raspberry Pi, Banana Pi, Odroid, Thinclient, usw.) 
  installiert und verwendet werden.

- Eine Nutzung ist ausschließlich zu nicht kommerziellen Hobbyzwecken
  und nicht für sicherheitsrelevante Aufgaben oder Bereiche zulässig.
    
- Die persönliche, kostenlose Weitergabe dieser Software an Dritte ist zulässig,
  soweit der Empfänger ebenfalls uneingeschränkt diesen Bedingungen zustimmt.

- Es ist unzulässig, ohne Zustimmung des Autors DL2MF diese Software oder
  Kopien davon in elektronischen Medien, auf Internetplatformen oder in Foren
  zum Download bereitzustellen.

Alle dem Sinn dieser Regelungen zuwiderlaufenden Handlungen sind nicht zulässig, 
der Autor der Software haftet nicht für Schäden, entgangenen Gewinn oder erforderliche 
Aufwendungen, die aus der Nutzung und/oder dem Gebrauch der Software und damit 
in Verbindung stehenden Folgen entstehen oder entstehen können.

Das Urheberrecht für die Anwendung DV4MF2.EXE liegt bei Meinhard Günther, DL2MF.

Die verwendeten Markenzeichen, Herstellerlogos und Produktnamen dienen der Funktionsbeschreibung im Programm, aus deren Verwendung ist kein freier Gebrauch abzuleiten.

Das Urheberrecht an den zur Nutzung dieser Software erforderlichen Komponenten und der dazugehörigen Software oder Teilen davon liegt bei Torsten Schultze, DG1HT, Kurt Moraw, DJ0ABR, Stefan Reimann, DG8FAC.


==============================================================================================

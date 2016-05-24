DV4MF2 - Control Panel for HAM DV modes
=======================================


This repository contains Language support, Add-On files and other sample files for the popular DV4MF2 DMR Controlpanel.


Current version V2.0.0.12 supports up to 20 languages. Starting with V2.0.0.10 the DV4MF2 control panel supports dynamically loaded GUI language files which can be selected, modified and exchanged by the user. 

To use DV4MF2 with additional languages, please create a folder "\languages" inside the program folder and download and <b>copy the standard english language and any of your favorite languages</b> to this folder.

The control panel dynamically loads at startup available languages, the available languages can be selected and switched during run-time by the user in the programs gateway tab. When no language files were found in the specific folder, the program offers two default language buttons for english/german (build-in support).

Announcement:
===================
The new release V2.0.0.12 has been released May 21th, 2016 and does require a change of the default english language file, that must be named now with the standard ISO-code en-GB (instead of en-EN). The program checks and will display a warning, if the default file could not be found. All available language files have been prepared to support ISO language codes (nb-NO Norsk, en-US American english and some more).


Compatibility note:
===================
With V2.0.0.11 the language file format changed (see below)!. It has been extended and is <b>offering 35 additional customizable text elements</b>, the new program version checks compatibility of the language file.

Running <b>Linux</b> currently caused a <b>compatibilty issue</b> up to V2.0.0.11 with english and norwegian language file. This is because of the language codes (en-EN / no-NO) currently used for compatibility. With release V2.0.0.12 the control panel now supports the official extensions of the Microsoft country code table (en-GB, nb-NO) to avoid any problems with Mono/Linux (see "Naming conventions" below).

<h2>New language files are no more compatible with V2.0.0.10, please update if you are using this release before!</h2>

<b>Available language files V2.0.0.12 (complete and ready for download here):</b>
- en-GB*- English    (build-in + language file)
- en-US - English US (build-in + language file)- 
- de-DE - German     (build-in + language file)
- fr-FR - Francais   tnx to Frederic, F4EED 
- it-IT - Italiano   tnx to Franco, HB9OAB
- es-ES - Espaniol   tnx to Iñigo, EA2CQ
- pt-PT - Português  tnx to José, CT1JIB
- nl-NL - Nederlands tnx to Rudy, PD0ZRY and Walter, PD2WGN
- nl-BE - Flemisch   tnx to Bas, ON2HB    - NEW!
- sv-SE - Swedish    tnx to Johan, SM0TSC
- nb-NO - Norsk      tnx to Gaute, LB6YD 
- us-ER - User       a template available to create your own language

*to use one of this language please try V2.0.0.10 (with old language file format) or upgrade to V2.0.0.12 when available, english also available as built-in language, rename or delete /languages folder to use built-in languages!

<b>Soon available languages (under revision):</b>
- pl-PL - Polish     tnx to Sebastian, SP2FRN (in progress, under translation)
- fi-FI - Suomi      tnx to Johanna (in progress, under translation)

<b>Other optional languages and modifications:</b> 
- Norsk      based on Gaute, LB6YD with some modifications by Kai, LA3QMA

<b><i>Languages we are looking for contributors (simply take the english file as your template):</b></i>
- be-NL - Belgium   (language file) *looking for a contributor
- da-DK - Dansk     (language file) *looking for a contributor
- cs-CZ - Czech     (language file) *under translation 
- ru-RU - русский   (language file) *looking for a contributor
- your file - please send us your translation

Installation:
==============================================================
To use DV4MF2 with foreign languages, simply create a folder "/languages" inside the program directory and copy the english language file and any language of your own choice to this folder. When running Linux please keep in mind, the folder name (lower case) and filenames (mixed case) must be written exactly in this way like the original files.

When running DV4MF2 Control Panel you'll notice, the language selection radio buttons on the "Gateway & Settings" Tab has changed to a dropdown listbox. Select your favorite language and the program will change the GUI description. Some elements have not been translated, these are either very deep coded into the program sources or this messages are replies from the DV4mini firmware.

To create your own language file please use "DV4MF2_us-ER.lng" as a template and overwrite the text elements. The syntax of the textfile is very simple, please keep in mind the following rules:
- You may use up to 20 header lines with your own comments, starting with a single hashtag '#'.
- The double hashtag '##' is being used as a line break, like for opmode and helptext elements. 
- The textarea must start with 'language::description', this is the text being displayed in the dropdown list*
- The file must end with '***END***' as an end tag after the last text line.

*the language parameter has changed from 2.0.0.10 (language:) to 2.0.0.11 (language::", the program checks this.

When you have finished your own textfile, please save the DV4MF2_us-ER.lng to your language directory and enjoy your own GUI.

Naming conventions:
==============================================================
Most supported language files are following to Microsofts Table of Language Culture Names: https://msdn.microsoft.com/en-us/library/ee825488%28v=cs.20%29.aspx

This is necessary to support other formatting options, like date and time format for the logfiles when changing the language. The number of direct supported languages is limited to 20 and will be follow the countries with the most DMR-Repeaters.

Before V2.0.0.12 there were two exceptions from standard, to be compatible with earlier versions and avoid too much different files for one language:
- en-EN - being used for en-US and en-GB
- no-NO - being used for nb-NO and ny-NO

Any additional language can be used by the option of the user-defined language file.


Changelog:
==============================================================

Version 2.0.0.12 - 20160521 "Dayton"
...........................................................
- NEW:   Support for all GUI language files in new format now with 150 text elements for all supported languages
- NEW:   Two additional languages announced soon after this release (polish and finnish)
- ADDED: Many new XTG talkgroups for BrandMeister (update to 228xx Swiss groups, 230 Czech Republic, 231 Slovak Republic, 302 Canada)
- ADDED: Program version check for outdated Control Panel version and incompatible dv_serial.exe
- CHG: Standard ISO codes implemented for en-GB, en-US, no-NB, nl-BE, da-DK, sv-SE - keep in mind to update your languages!
- CHG:   Some code optimization and internal changes
- FIXED: minor fixes for use of control panel when running on Linux with mono

Version 2.0.0.11 - 20160401 "April joke"
...........................................................
- NEW:   New GUI language file format (see above), up to 20 languages and 45 new text elements!
- This release is prerequisite for using Português, Suomi, Norsk, Dansk and all future languages.
- FIXED: Reflector info in Mode DStar was corrupt due to the FCS/C4FM changes, now both work
- FIXED: Statusline information RX/TX and UTC clock display
- FIXED: special character display for foreign languages fixed

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
All functions controlled by DV4MF2 are based on the communication API to the hardware modem.
To oerate a DV4mini with this software, the original firmware and dv_serial (latest 2016-01-12, newer version not supported!) is prerequisite and all available functions are depending on the firmware.

Please check also the support forums for the hardware you are using for your hotspot:

- https://de.groups.yahoo.com/neo/groups/Dmrplus/info
- https://de.groups.yahoo.com/neo/groups/Brandmeister/info


Hints and tips for installation of DV4MF2 control panel (Windows/Linux):
- http://www.dl2mf.de/blog/?p=1297


Lizenzbedingungen
==============================================================
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

Copyright & Disclaimer
==============================================================
Das Urheberrecht für die Anwendung DV4MF2.EXE liegt bei Meinhard Günther, DL2MF. Alle Ergänzugen und Erweiterungen inklusive der Sprachdateien sind OpenSource.

Die verwendeten Markenzeichen, Herstellerlogos und Produktnamen dienen der Funktionsbeschreibung im Programm, aus deren Verwendung ist kein freier Gebrauch abzuleiten.

Das Urheberrecht an Teilen der zur Nutzung dieser Software erforderlichen ClosedSource-Komponenten und der dazugehörigen Software wurde eingeräumt und liegt bei Torsten Schultze, DG1HT, Kurt Moraw, DJ0ABR, Stefan Reimann, DG8FAC.


==============================================================================================

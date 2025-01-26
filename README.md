[HowTo's: Inhaltsverzeichnis](https://github.com/toafez/Tutorials)

# HowTo: AutoPilot - Herunterladen. Installieren. Einrichten.

## AutoPilot herunterladen

- Wechsle zum [AutoPilot GitHub Repository](https://github.com/toafez/AutoPilot) und klicke entweder auf **Releases** in der rechten Seitenleiste, um dir alle AutoPilot-Versionen anzeigen zu lassen, oder klicke direkt darunter auf die aktuellste AutoPilot-Version. Zum Zeitpunkt der Veröffentlichung dieser Anleitung ist AutoPilot v1.1-800 das aktuellste Release.

![10_AutoPilot-Download](/images/10_AutoPilot-Download.png)

- Wähle aus der Tabelle direkt unter den Release Notes das Paket bzw. die Installationsdatei mit dem Namen AutoPilot, gefolgt von der zur Zeit aktuellesten Versionsnummer und der Dateiendung **.spk**, um die Datei herunterzuladen.

![11_AutoPilot-Download](/images/11_AutoPilot-Download.png)

## AutoPilot installieren

- Melde dich am DistStation Manager (kurz DSM) deines Synology NAS mit einem Konto an, das zur Gruppe der Administratoren (administrators) gehört. Navigiere anschließend zu **DSM-Hauptmenü > Paket-Zentrum** und klick rechts auf die Schaltfläche **Manuelle Installation**

![20_AutoPilot-Installation](/images/20_AutoPilot-Installation.png)

- Klicke in dem sich öffnenden Fenster auf die Schaltfläche **Durchsuchen** und wähle die zuvor heruntergeladene Installationsdatei von AutoPilot aus. 

![21_AutoPilot-Installation](/images/21_AutoPilot-Installation.png)

- Akzeptiere den Hinweis, das dieses Paket von einem Dritthersteller angeboten wurde und du selbst für etwaige Schäden oder Datenverluste verantwortlich bist.

![22_AutoPilot-Installation](/images/22_AutoPilot-Installation.png)

- Akezeptiere im nächsten Fenster die Lizenzbedingungen von AutoPilot, indem du das Kontrollkästchen (1) aktivierst. Klicke anschließend auf die Schaltfläche **Weiter** (2)

![23_AutoPilot-Installation](/images/23_AutoPilot-Installation.png)

- Schließe die Installation ab, indem du auf die Schaltfläche **Fertig** klickst. 

![24_AutoPilot-Installation](/images/24_AutoPilot-Installation.png)

- AutoPilot wurde nun erfolgreich auf deinem Synology NAS installiert.

## AutoPilot einrichten

- Starte AutoPilot über das **DSM-Hauptmenü** und klicke auf das neu hinzugefügte Icon **AutoPilot**

![25_AutoPilot-Installation](/images/25_AutoPilot-Installation.png)

### App-Berechtigung erweitern
- Unter DSM 7 ist ein 3rd_Party Paket wie AutoPilot mit stark eingeschränkten Benutzer- und Gruppenrechten ausgestattet. Dies hat unter anderem zur Folge, dass systemnahe Befehle nicht ausgeführt werden können. Für den reibungslosen Betrieb von AutoPilot werden jedoch erweiterte Systemrechte benötigt, um z.B. auf die Ordnerstruktur des Systems zugreifen zu können. Um die App-Berechtigung zu erweitern, muss AutoPilot in die Gruppe der Administratoren aufgenommen werden, was jedoch nur durch den Benutzer selbst erfolgen kann. Klicke daher als erstes bitte auf die Schaltfläche **Berechtigung erweitern** (1)

![26_AutoPilot-Installation](/images/26_AutoPilot-Installation.png)

- Folge nun den Anweisungen auf dem Bildschirm. Du hast die Möglichkeit, den Befehl zum erweitern der App-Berechtigung entweder direkt auf der Konsole oder über den DSM-Aufgabenplaner auszuführen.

- **Hinweis:** Wie du dich über ein Terminalprogramm per SSH als root auf der Konsole des Synology NAS einloggen kannst, beschreibt Synology u.a. in der Anleitung: [Wie kann ich mich über SSH mit Root-Berechtigung bei DSM/SRM anmelden?](https://kb.synology.com/de-de/DSM/tutorial/How_to_login_to_DSM_with_root_permission_via_SSH_Telnet) 

- Während der Erweiterung der App-Berechtigung erscheint am rechten oberen Bildschirmrand für kurze Zeit ein Popup-Fenster mit einer Benachrichtigung, die die erfolgreiche Einrichtung bestätigt.

- Nachdem du die Anweisungen befolgt hast, kannst du das angezeigte Fenster schließen. Damit die Änderungen in AutoPilot angezeigt werden, musst du entweder den Inhalt der AutoPilot-Seite über die Schaltfläche oben links auf dem Bildschirm aktualisieren (2) oder die App neu starten.

### UDEV-Gerätetreiber installieren
- Damit AutoPilot externe Datenträger erkennen kann, nachdem sie an das Synology NAS angeschlossen wurden, muss ein Gerätetreiber in Form eines kleines Script installiert werden, das sich an die bereits vorhandene permanente Überwachung der USB- und eSATA-Anschlüsse durch den DSM anhängt und Informationen an AutoPilot sendet, sobald ein externer Datenträger angeschlossen wird. Um den Gerätetreiber zu installieren, klicke bitte auf die Schaltfläche **Installieren** (1)

![27_AutoPilot-Installation](/images/27_AutoPilot-Installation.png)

- Folge nun den Anweisungen auf dem Bildschirm. Du hast wieder die Möglichkeit, den Befehl zum installieren des UDEV-Gerätetreibers entweder direkt auf der Konsole oder über den DSM-Aufgabenplaner auszuführen.

- Während der Installation des UDEV-Gerätetreibers erscheint am rechten oberen Bildschirmrand für kurze Zeit ein Popup-Fenster mit einer Benachrichtigung, die die erfolgreiche Einrichtung bestätigt.

- Nachdem du die Anweisungen befolgt hast, kannst du das angezeigte Fenster schließen. Damit die Änderungen in AutoPilot angezeigt werden, musst du entweder den Inhalt der AutoPilot-Seite über die Schaltfläche oben links auf dem Bildschirm aktualisieren (2) oder die App neu starten.

- AutoPilot ist nun vollständig eingerichtet, alle Meldungen sollten verschwunden sein und die Benutzeroberfläche sollte wie folgt aussehen.

![28_AutoPilot-Installation](/images/28_AutoPilot-Installation.png)

- Während der Erweiterung der App-Berechtigung und der Installation des UDEV-Gerätetreibers erschien im rechten oberen Bilschirmrand jeweils ein Popup-Fenster, welches dir die Aktion bestätigt hat. Diese Benachrichtigungen kannst du dir bei Bedarf noch einmal anzeigen lassen und sollten so aussehen. 

![29_AutoPilot-Installation](/images/29_AutoPilot-Installation.png)

## Einen externen Datenträger an AutoPilot binden

- Wenn du bereits einen externen Datenträger mit AutoPilot verbunden hast, entferne diesen zuerst, indem du auf das entsprechende Symbol in der Taskleiste des DSM oben rechts klickst. Starte anschließend AutoPilot über das **DSM-Hauptmenü** und klicke auf das Icon **AutoPilot**.

- Klicke auf das Dropdown-Menü `Externe Datenträger`. Solange kein externer Datenträger an deiner Synology NAS angeschlossen ist, wird die folgende Meldung angezeigt.

![30_AutoPilot-Einrichtung](/images/30_AutoPilot-Einrichtung.png)

- Wenn du jetzt einen externen Datenträger an dein Synology NAS anschließt, erkennt die Benutzeroberfläche von AutoPilot dies zunächst nicht. Deshalb musst du zuerst die Seite aktualisieren, indem du auf das entsprechende Symbol oben links klickst (1). Nachdem die Seite aktualisiert wurde, klicke erneut auf das Dropdown-Menü `Externe Datenträger` (2). Du solltest verschiedene Informationen über den externen Datenträger sehen.

- Um den angezeigten Datenträger mit AutoPilot zu verbinden, klicke auf das Link-Symbol (3) auf der rechten Seite. Wenn mehr als ein Datenträger mit dem Synology NAS verbunden ist oder der verbundene Datenträger mehrere Partitionen enthält, klicke auf das entsprechende Link-Symbol hinter der entsprechenden Partition oder dem entsprechenden Datenträger.

![31_AutoPilot-Einrichtung](/images/31_AutoPilot-Einrichtung.png)

- Lies zunächst die Informationen in dem sich nun öffnenen Fenster, um zu verstehen, was im Folgenden geschieht. Als Speicherort für das Shell-Skript, das später noch genauer erklärt wird, wähle aus dem Dropdown-Menü einen `Freigegebenen Ordner` und gib optional im rechten Textfeld daneben ein weiteres Zielverzeichnis an. Beachte auch die Informationen, die du erhältst, wenn du auf das Symbol `i` klickst. Gib im Textfeld darunter einen eindeutigen Namen für das Shell-Skript ein und beachte auch hier die Informationen, die sich hinter dem Symbol `i` verbergen. Nachdem alle Einstellungen vorgenommen wurden, klicke auf die Schaltfläche "Speichern".

![32_AutoPilot-Einrichtung](/images/32_AutoPilot-Einrichtung.png)

- Nach einem erneuten Klick auf das Dropdown-Menü Externe Datenträger` werden nun weitere Informationen zum Speicherort und Dateinamen des Shell-Skripts für den zuvor ausgewählten Datenträger angezeigt (1).

- Das Link-Symbol auf der rechten Seite wurde durch ein Terminal-Symbol und ein Mülleimer-Symbol ersetzt. Durch Klicken auf den Mülleimer wird die Verbindung zum Shell-Skript getrennt, das Shell-Skript selbst wird jedoch nicht gelöscht.

![33_AutoPilot-Einrichtung](/images/33_AutoPilot-Einrichtung.png)

- Um den Inhalt des Shell-Skripts anzuzeigen, klicke auf das Terminal-Symbol (3). Außer der Information über den Speicherort und den Dateinamen gibt es noch nicht viel zu sehen, da das Skript noch keinen Inhalt hat.

![34_AutoPilot-Einrichtung](/images/34_AutoPilot-Einrichtung.png)

- Zusätzlich wird im Stammverzeichnis des externen Datenträgers eine leere Datei mit dem Namen `autopilot` erstellt. Diese Datei wird später vom UDEV-Gerätetreiber, der während der Einrichtung von AutoPilot installiert wird, als Indikator verwendet. Zusammen mit der eindeutigen UUID jedes Datenträgers bzw. jeder Partition wird so die Verbindung zum eigentlich ausführenden Shell-Skript hergestellt.

![35_AutoPilot-Einrichtung](/images/35_AutoPilot-Einrichtung.png)

- Damit ist das Einrichten bzw. Verbinden eines externen Datenträgers mit AutoPilot und das Ausführen eines Shell-Skripts beim Anschließen des Datenträgers an das Synolgoy NAS vorerst abgeschlossen. 

Nun ist es jedem selbst überlassen, was das Shell-Skript machen soll. Da es zur Zeit noch leer ist, kann nun damit begonnen werden, es mit individuellen Inhalten zu füllen. Wer möchte, kann dazu auch ein "Benutzerdefiniertes Script Template" als Vorlage verwenden, das über die Benutzeroberfläche von AutoPilot ausgewählt werden kann. Wer an dieser Stelle lieber eine Hyper Backup Aufgabe mit AutoPilot verknüpfen möchte, kann dies ebenfalls über die Benutzeroberfläche von AutoPilot tun. Die Vorgehensweise ist in beiden Fällen identisch. Der einzige Unterschied zu einem "Benutzerdefiniertes Script Template" besteht darin, dass das Shell-Skript für eine Hyper Backup Aufgabe bereits komplett vorgefertigt ist und nur noch übernommen werden muss.

## Eine Hyper Backup Aufgabe an AutoPilot binden.

- Vergewissere dich, dass der externe Datenträger, das mit einem Hyper Backup-Auftrag verbunden werden soll, bereits an dein Synolgy NAS angeschlossen ist.

- Starte AutoPilot über das **DSM-Hauptmenü** und klicke auf das neu hinzugefügte Icon **AutoPilot** und kicke anschließend auf das Dropdown-Menü `Hyper Backup Aufaben`. Es werden dir daraufhin sämtliche Aufgaben anzeigt. In diesem Beispiel möchten wir die Aufgabe `Backup-Home-Verzeichnisse` mit AutoPilot verbinden. Klicke daher auf das Link-Symbol hinter der Aufgabe, die du verwenden möchtest. 

![36_AutoPilot-Einrichtung](/images/36_AutoPilot-Einrichtung.png)

- In dem sich öffnenden Fenster werden weitere Informationen zu der ausgewählten Hyper Backup Aufgabe angezeigt und man wird aufgefordert, aus dem Dropdown-Menü einen `Dateinamen des Shell-Skripts` auszuwählen. Hier ist zu beachten, dass nur Shell-Skripte ausgewählt werden können, die bereits von AutoPilot mit einem externen Datenträger oder einer Partition verbunden wurden. In diesem Beispiel lautet der Dateiname für das Shell-Skript `HB-Backup-Home-Verzeichnisse-auf-64GB-USB-Stick.sh`. Klicke anschließend auf `Speichern`

![37_AutoPilot-Einrichtung](/images/37_AutoPilot-Einrichtung.png)

- Nach dem Speichern öffne das Dropdown-Menü `Externe Datenträger` und lasse dir den Inhalt des Shell-Skripts anzeigen, indem du auf das Terminal-Symbol klickst.

![38_AutoPilot-Einrichtung](/images/38_AutoPilot-Einrichtung.png)

- In dem sich nun öffnenden Fenster wird dir neben der Information über den Speicherort und den Dateinamen des Shell-Skripts auch der eigentlich Script-Code angezeigt. Gleich zu Beginn siehst du, dass das Skript genau die Hyper Backup Aufgabe ausführen soll, die du zuvor ausgewählt hast.

![39_AutoPilot-Einrichtung](/images/39_AutoPilot-Einrichtung.png)

- Damit hast du erfolgreich eine Hyper Backup Aufgabe mit AutoPilot verknüpft. Damit die Aufgabe in Zukunft automatisch beim Einstecken des externen Datenträgers in dein Synology NAS ausgeführt wird, musst du noch die Überwachung in AutoPilot aktivieren. Außerdem kannst du auswählen, wie sich AutoPilot nach der Ausführung der Aufgabe verhalten soll und ob ein optisches und akustisches Signal ausgegeben werden soll.

![40_AutoPilot-Ausfuehrung](/images/40_AutoPilot-Ausfuehrung.png)

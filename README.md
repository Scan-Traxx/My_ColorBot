Gerne! Eine gute `README.md` ist die Visitenkarte deines Projekts. Sie hilft anderen (und dir selbst in sechs Monaten), zu verstehen, wie der Bot funktioniert und wie man ihn sicher nutzt.


---

# 🚀 Advanced AHK ColorBot (Spiral Search Edition)

Ein hochperformanter, pixelbasierter Aimbot für AutoHotkey, der durch eine intelligente spiralförmige Suchlogik besticht. Im Gegensatz zu herkömmlichen Bots scannt dieser von der Mitte des Bildschirms nach außen, um das Ziel mit der höchsten Priorität (das nächste zum Fadenkreuz) sofort zu finden.

## 🛠 Funktionsweise

### 🌀 Die Spiral-Suche (Efficiency Mode)
Der Kern des Bots liegt in der `Pixelmittesuche`. Statt den gesamten Bildschirm oder große Quadranten gleichzeitig zu scannen, nutzt dieser Bot konzentrische Suchringe:
1. Er beginnt mit einem winzigen Quadrat direkt an deinem Fadenkreuz.
2. Wenn kein Ziel gefunden wird, vergrößert er den Suchradius schrittweise (definiert durch `step`).
3. **Der Clou:** Sobald der erste Pixel der Ziel-Farbe gefunden wird, bricht die Suche sofort ab (`return`). 
4. Das spart massiv CPU-Ressourcen und garantiert, dass du immer das Ziel anvisierst, welches deinem Fadenkreuz am nächsten ist.



### 📦 Komponenten
* **`colorbot.ahk`**: Das Hauptskript mit der GUI-Steuerung und dem Hotkey-Management.
* **`OVclass.ahk`**: Die "Engine" des Bots. Hier liegen die mathematischen Berechnungen, die ESP-Logik und die Grafik-Funktionen.
* **`config.ini`**: Hier werden deine individuellen Einstellungen (Farbe, FOV, Tastenbelegung) dauerhaft gespeichert.

---

## 🚀 Installation & Start
1. Installiere [AutoHotkey v1.1+](https://www.autohotkey.com/).
2. Lade das Repository herunter und entpacke es.
3. Stelle sicher, dass der Ordner `img/` existiert und die `mcircle.bmp` enthält.
4. Starte die `colorbot.ahk` per Doppelklick.

---

## ⚙️ Konfiguration & Bedienung

| Taste | Funktion |
| :--- | :--- |
| **INSERT** | Menü anzeigen / verstecken |
| **STRG + X** | Farbe unter dem Mauszeiger übernehmen |
| **F1** | Hilfe-Fenster öffnen |
| **END** | Bot komplett beenden |

### Wichtige Parameter:
* **Smoothing:** Bestimmt, wie "menschlich" die Mausbewegung ist. Höhere Werte bewegen die Maus langsamer und sanfter.
* **FOV (Field of View):** Der Radius in Pixeln, in dem der Bot nach Zielen sucht.
* **Farbvariante:** Die Toleranz der Farberkennung. Erhöhe diesen Wert, wenn das Ziel im Schatten steht oder die Beleuchtung sich ändert.

---

## ⚠️ Was man beachten sollte (Sicherheit & Fairness)

1. **Spiel-Modus:** Der Bot funktioniert am besten im **Windowed Borderless** (Fenstermodus ohne Rand). Im exklusiven Vollbildmodus können manche Spiele den Zugriff auf den Screen-Buffer blockieren.
2. **Anti-Cheat:** Pixel-Bots gelten oft als "sicherer" als Memory-Cheats, sind aber nicht unsichtbar. Nutze immer ein gewisses Maß an **Smoothing**, um extrem ruckartige, roboterhafte Bewegungen zu vermeiden.
3. **Farbauswahl:** Wähle eine Farbe, die im Spiel selten vorkommt (z. B. lila Outlines), um Fehlschüsse auf die Umgebung (Blumen, Kleidung) zu minimieren.
4. **Admin-Rechte:** Wenn der Bot im Spiel keine Mausbewegungen ausführt, versuche, die `colorbot.ahk` per Rechtsklick **als Administrator** auszuführen.

---

## 📜 Disclaimer
Dieses Projekt dient ausschließlich zu Bildungszwecken. Die Nutzung in Online-Spielen kann gegen die Nutzungsbedingungen verstoßen und zu einem permanenten Ausschluss (Ban) führen. Die Entwickler übernehmen keine Haftung für Schäden oder Sperren.


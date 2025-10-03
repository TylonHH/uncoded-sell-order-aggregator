# @peorsp_bot – Pending Orders Splitter Bot

Der Bot hilft dir dabei, deine offenen Verkaufs-Orders aus dem alten **[unCoded Bot](https://t.me/unCoded_bot?start=ref_1203406052)** übersichtlich aufzubereiten.  
Statt hunderte einzelner Orders manuell zu sortieren, kannst du mit diesem Bot die Orders automatisch in Preisbereiche ("Splits") zusammenfassen.  
Das Ergebnis ist eine saubere Liste mit Stückzahl, Limitpreis und Gesamtwert, die du dann in der Börse nachbauen kannst.

---

## Vorbereitung: Export der Orders als CSV

Damit der Bot funktioniert, musst du ihm deine offenen Orders als **CSV-Datei** zur Verfügung stellen.  
Die Daten stecken in der Datenbank `tradingbot.db`, die im Ordner des unCoded Bots liegt.

So kommst du an die CSV:

1. **DB Browser for SQLite** herunterladen und installieren  
   👉 [https://sqlitebrowser.org/dl/](https://sqlitebrowser.org/dl/)

2. Im Programm die Datei `tradingbot.db` öffnen  
   - Standardmäßig findest du die Datei im gleichen Ordner wie `unCoded.exe`.

3. Links in der Liste der Tabellen **`activeOrders`** auswählen.

4. Rechtsklick auf die Tabelle → **"Als CSV-Datei exportieren"** wählen.

5. Datei speichern (z. B. `activeOrders.csv`).

6. <img width="811" height="374" alt="grafik" src="https://github.com/user-attachments/assets/c16eea1a-7747-474d-b885-68a80b67cc26" />


---

## Nutzung im Bot

1. Öffne den Telegram-Bot **[@peorsp_bot](https://t.me/peorsp_bot)**.  
2. Lade die `activeOrders.csv` hoch.  
3. Wähle, wie viele Splits (Preisgruppen) du haben möchtest.  
4. Entscheide, ob die Gruppierung nach Minimum oder Maximum-Preis erfolgen soll.
5. Wähle das gewünschte Dezimaltrennzeichen (Punkt oder Komma), je nachdem ob du die Daten im Browser oder in der App verwenden willst.
6. Der Bot zeigt dir eine Liste mit den zusammengefassten Orders an, inklusive Gesamtsumme.

---

## Beispielausgabe

```

📊 Orders gesplittet (10 Gruppen, Limit=max)

#1 57.190.339 x 0,00001232 = 704,58
#2 64.865.551 x 0,00001267 = 821,85
#3 29.839.938 x 0,00001302 = 388,52
...
Gesamt: 1.115.786.724 = 15.644,64

```

So kannst du deine Orders viel einfacher manuell an der Börse eintragen.

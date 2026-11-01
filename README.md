# Sachkunde34a Android Lern-App – Entwicklungsstand 0.1

## Öffnen und bauen
Android Studio (JDK 17) → Open → diesen Ordner auswählen → Gradle-Synchronisierung → Build > Build APK(s). Android SDK 35 erforderlich. Das Projekt enthält keinen Gradle-Wrapper; Android Studio kann eine passende lokale Gradle-Installation verwenden.

## Bereits implementiert
Native Android-Java-App, Offline-Fragen in `assets/questions.json`, HTTPS-Update beim Start und auf Knopfdruck, Validierung des JSON-Schemas, lokale Speicherung, getrennte Themen, Einzelanzeige, Antworten prüfen, Weiter-Button, einfacher 120-Minuten-Timer, lokale letzte Punktzahl.

## Wichtige Grenzen
Nur 3 klar als Demo markierte Fragen. Noch kein produktionsreifer 82-Fragen-Prüfungsmodus, keine IHK-Teilpunktewertung, kein serverseitig bereitgestellter Update-Endpunkt, keine signierten Fragepakete und keine fertige APK. Ein Update funktioniert erst, wenn `https://www.sachkunde34a.info/app/questions.json` tatsächlich ein gültiges JSON bereitstellt. Die App aktualisiert beim Start, nicht zuverlässig im Hintergrund. Nicht als amtliche IHK-Prüfung ausgeben.

## Update-Datei
`app/src/main/assets/questions.json` als Vorlage nutzen und nach rechtlicher Prüfung auf der Homepage unter `/app/questions.json` per HTTPS veröffentlichen. Bei Änderungen `version` erhöhen. Antworten sind nullbasiert und müssen genau 1 oder 2 Indizes enthalten. Einmal vollständig getestete neue Fragepakete verwenden.

## Nächste Schritte
1. Geprüften Fragenpool der Homepage übernehmen und je Thema trennen. 2. Korrekte IHK-Punktewertung und Prüfungszusammenstellung ergänzen. 3. Server-Updatepfad veröffentlichen und signierte Pakete implementieren. 4. Android Studio APK bauen und auf Smartphone testen. 5. Datenschutz/Impressum in der App ergänzen.

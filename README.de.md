# DRVCAM

[English](README.md) | [Español](README.es.md) | [العربية](README.ar.md) | **Deutsch** | [Français](README.fr.md) | [Italiano](README.it.md) | [日本語](README.ja.md) | [简体中文](README.zh-hans.md)

**Eine virtuelle Kamera für kompatible, gerootete Android-Geräte.** Wähle ein Foto oder Video aus und nutze es als Kamerabild der Apps deiner Wahl – mit Live-Wiedergabe und Bildausschnitt-Steuerung.

[![Neueste Version](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.droidrooter.virtualcamera?label=neueste%20version)](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases/latest)
[![Plattform](https://img.shields.io/badge/plattform-Android-3DDC84)](#voraussetzungen)
[![Root erforderlich](https://img.shields.io/badge/root-erforderlich-critical)](#voraussetzungen)
[![Lizenz](https://img.shields.io/badge/lizenz-proprietär-lightgrey)](#lizenz)

> **Alpha-Version.** DRVCAM wird aktiv weiterentwickelt, und das Verhalten kann je nach Gerät variieren.

Dieses Repository ist der **Modul-Eintrag** für DRVCAM. Es enthält keinen Quellcode. Produktseite, Preise und vollständige Dokumentation: **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**.

## Inhaltsverzeichnis

- [Screenshots](#screenshots)
- [Was es leistet](#was-es-leistet)
- [Voraussetzungen](#voraussetzungen)
- [Herunterladen](#herunterladen)
- [Installieren](#installieren)
- [Kostenloser und bezahlte Tarife](#kostenloser-und-bezahlte-tarife)
- [Datenschutz-Grundlagen](#datenschutz-grundlagen)
- [Häufig gestellte Fragen](#häufig-gestellte-fragen)
- [Haftungsausschluss](#haftungsausschluss)
- [Lizenz](#lizenz)
- [Support](#support)
- [Änderungsprotokoll](#änderungsprotokoll)

## Screenshots

| Start | Schwebende Steuerung |
|---|---|
| ![DRVCAM-Startbildschirm: Vorschau der Live-Quelle, Auswahl der Ziel-App, Medienquelle und Schnellzugriff](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-home.webp) | ![Schwebende Steuerung über einer Kamera-App](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-controller.webp) |

| Medien-Editor | Presets |
|---|---|
| ![Medien-Editor: Wiedergabe, Schleife, Zoom und Drehung](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-editor.webp) | ![Presets-Tab der Bibliothek](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-presets.webp) |

## Was es leistet

- Nutzt ein Foto oder Video, das du importierst, als Kameraquelle einer von dir gewählten App – sofern Gerät, Kamera-API und App das unterstützen.
- Du wählst die Ziel-Apps aus und passt Wiedergabe, Drehung, Spiegelung, Zoom und Bildausschnitt an. Eine Main-Quelle und zwei Presets lassen sich speichern und wechseln.
- Du kannst ein eingerichtetes Ziel zwischen virtuellem Bild und echter physischer Kamera umschalten. Manche Apps müssen ihre Kamera neu öffnen, bevor eine Änderung sichtbar wird; DRVCAM weist dich darauf hin.
- Bietet eine optionale schwebende Steuerung, die über der genutzten App bleibt (benötigt die Overlay-Berechtigung).
- Lässt das echte Mikrofon unverändert – DRVCAM ersetzt oder verarbeitet kein Audio.

## Voraussetzungen

- Ein gerootetes Android-Gerät (Magisk oder KernelSU), Android 9 oder neuer. Der Kameraersatz benötigt Root; ohne Root öffnet sich die App, der Ersatz ist dann aber nicht verfügbar.
- Ein Framework aus der Xposed-Familie mit Unterstützung für libxposed API 102 – getestet wird DRVCAM mit [Vector](https://github.com/JingMatrix/Vector) (dem Nachfolger von LSPosed), einem Zygisk-basierten Framework aus der LSPosed-Familie. Ein Framework ohne API-102-Unterstützung lädt das Modul nicht.
- Ausreichend Decoder- und Grafikleistung für die gewählten Medien und die gewählte App.

## Herunterladen

Dieser Eintrag enthält den **Phone-Build für Android 12 und neuer** (arm64). Die übrigen Builds – Android 9 bis 11 sowie die Emulator-Images – findest du auf **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**, mit einem Auswahlassistenten, der dir den passenden empfiehlt.

Jede Version hier enthält ihre SHA-256-Prüfsumme in den Versionshinweisen – prüfe deinen Download vor der Installation.

## Installieren

1. Lade die zu deiner Android-Version und deinem Gerätetyp passende APK herunter und installiere sie (siehe oben).
2. Öffne deinen Framework-Manager und aktiviere DRVCAM; starte neu, falls gefordert.
3. Öffne DRVCAM und erteile Root-Zugriff, wenn danach gefragt wird. DRVCAM verwaltet den Geltungsbereich der gewählten Apps direkt in der eigenen App – im Framework-Manager muss nichts von Hand ergänzt werden.
4. Melde dich an oder wähle **Kostenlos testen** (siehe [Kostenloser und bezahlte Tarife](#kostenloser-und-bezahlte-tarife)).
5. Importiere ein Foto oder Video in die Bibliothek, wähle es aus, wähle eine Ziel-App und tippe auf **Enable**. Öffne die Kamera der Ziel-App selbst.
6. Prüfe das Ergebnis in der Ziel-App. Die Vorschau von DRVCAM hilft bei der Medienauswahl; sie allein belegt nicht, dass die Ziel-App das Bild tatsächlich erhalten hat.

**Disable** entfernt den Geltungsbereich von DRVCAM für das Ziel wieder.

## Kostenloser und bezahlte Tarife

DRVCAM benötigt ein DRVCAM-Konto und eine Internetverbindung für Anmeldung, Geräteregistrierung und Verlängerung. Nach der Anmeldung kann die App für eine begrenzte Zeit auch offline weiterlaufen.

- **Kostenlos testen** (kostenlos): Bildquellen, eine Ziel-App.
- **Bezahlte Tarife**: Videoquellen, mehrere Ziel-Apps, die schwebende Steuerung und das Umschalten über Camera Source.

Aktuelle Tarife, Gerätelimits und Preise: **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/#pricing)**.

## Datenschutz-Grundlagen

- Deine Medien bleiben für den Kamera-Ablauf auf deinem Gerät – der Konto-Dienst benötigt deine Medien oder Kamerabilder nicht für die Anmeldung.
- Der Konto-Dienst verarbeitet Konto-, Geräte- und Abonnementdaten, damit Anmeldung und Lizenzierung funktionieren. Diagnosedaten werden nur auf deine Anforderung gesendet.
- Eine Ziel-App kann weiterhin speichern, auswerten oder übertragen, was ihre Kamera zeigt; es gelten die Datenschutzpraktiken dieser App.
- Vollständige Richtlinie: [droidrooter.com/privacy](https://www.droidrooter.com/privacy).

## Häufig gestellte Fragen

**Wird Root benötigt?**
Ja. Der Kameraersatz erfolgt über einen Hook auf Systemebene, der Root und ein kompatibles Framework aus der Xposed-Familie benötigt.

**Funktioniert es auf meinem Gerät?**
Nur geprüfte Kombinationen sind auf der Produktseite aufgeführt. Gerät, Firmware und Kamera-App unterscheiden sich zu stark, um Kompatibilität im Voraus zuzusichern.

**Kann ich es ohne Anmeldung nutzen?**
Ja, mit **Kostenlos testen** (Bildquellen, eine Ziel-App). Video und die übrigen Funktionen benötigen einen bezahlten Tarif.

**Ich habe mein Passwort verloren – was nun?**
Die Kontowiederherstellung erfolgt derzeit manuell; nutze die Links unter [Support](#support).

**Wo ist der Quellcode?**
Er wird hier nicht veröffentlicht. Dieses Repository ist ein Modul-Eintrag, der ausschließlich signierte Release-Binärdateien verteilt.

## Haftungsausschluss

DRVCAM ist Alpha-Software, bereitgestellt „wie besehen“ ohne jegliche Gewährleistung. Das Rooten eines Geräts und die Installation eines systemlosen Frameworks erfolgen auf eigenes Risiko und können Garantie oder Stabilität deines Geräts beeinträchtigen.

Du bist allein verantwortlich für die von dir genutzten Medien, für die Anwendungen, mit denen du DRVCAM einsetzt, und für die Einhaltung der für dich geltenden Gesetze und Bedingungen. Der Entwickler übernimmt keine Verantwortung für eine rechtswidrige, unbefugte oder anderweitig unsachgemäße Nutzung dieser Software.

## Lizenz

DRVCAM ist proprietäre Software mit geschlossenem Quellcode. Es wird keine Lizenz zum Kopieren, Verändern, Zurückentwickeln oder Weiterverbreiten der Anwendung erteilt. Download und Installation unterliegen den auf der Produktseite veröffentlichten [Nutzungsbedingungen](https://www.droidrooter.com/terms).

## Support

- Telegram: [@DroidRooter](https://t.me/DroidRooter)
- Kontaktformular der Website: [droidrooter.com/contact](https://www.droidrooter.com/contact)

## Änderungsprotokoll

Die Änderungen stehen jeweils in den Hinweisen zu den einzelnen [Versionen](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases).

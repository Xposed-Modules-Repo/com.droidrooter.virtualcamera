# DRVCAM

[English](README.md) | [Español](README.es.md) | [العربية](README.ar.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | **Italiano** | [日本語](README.ja.md) | [简体中文](README.zh-hans.md)

**Una fotocamera virtuale per dispositivi Android compatibili con root.** Scegli una foto o un video e presentalo come immagine della fotocamera delle app che selezioni, con riproduzione dal vivo e controlli di inquadratura.

[![Ultima versione](https://img.shields.io/github/v/release/Xposed-Modules-Repo/com.droidrooter.virtualcamera?label=ultima%20versione)](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases/latest)
[![Piattaforma](https://img.shields.io/badge/piattaforma-Android-3DDC84)](#requisiti)
[![Root necessario](https://img.shields.io/badge/root-necessario-critical)](#requisiti)
[![Licenza](https://img.shields.io/badge/licenza-proprietaria-lightgrey)](#licenza)

> **Versione alpha.** DRVCAM è in sviluppo attivo e il comportamento può variare da dispositivo a dispositivo.

Questo repository è la **scheda del modulo** per DRVCAM. Non contiene codice sorgente. Pagina del prodotto, prezzi e documentazione completa: **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**.

## Indice

- [Screenshot](#screenshot)
- [Cosa fa](#cosa-fa)
- [Requisiti](#requisiti)
- [Scaricare](#scaricare)
- [Installare](#installare)
- [Piano gratuito e piani a pagamento](#piano-gratuito-e-piani-a-pagamento)
- [Informazioni di base sulla privacy](#informazioni-di-base-sulla-privacy)
- [Domande frequenti](#domande-frequenti)
- [Esclusione di responsabilità](#esclusione-di-responsabilità)
- [Licenza](#licenza)
- [Assistenza](#assistenza)
- [Changelog](#changelog)

## Screenshot

| Home | Controller mobile |
|---|---|
| ![Schermata Home di DRVCAM: anteprima della sorgente dal vivo, selezione dell'app di destinazione, sorgente multimediale e controlli rapidi](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-home.webp) | ![Controller mobile sovrapposto a un'app fotocamera](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-controller.webp) |

| Editor multimediale | Preset |
|---|---|
| ![Editor multimediale: controlli di riproduzione, loop, zoom e rotazione](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-editor.webp) | ![Scheda preset della libreria](https://raw.githubusercontent.com/saadnahid7/drvcam-releases/main/screenshots/screen-presets.webp) |

## Cosa fa

- Usa una foto o un video che importi come sorgente della fotocamera di un'app che scegli, dove dispositivo, API fotocamera e app lo consentono.
- Ti permette di scegliere le app di destinazione e regolare riproduzione, rotazione, effetto specchio, zoom e inquadratura. Una sorgente Main e due preset possono essere salvati e scambiati.
- Ti permette di far passare una destinazione configurata tra l'immagine virtuale e la fotocamera fisica reale. Alcune app devono riaprire la fotocamera prima che il cambio sia visibile; DRVCAM te lo segnala quando accade.
- Offre un controller mobile opzionale che resta sopra l'app in uso (richiede il permesso di sovrapposizione).
- Lascia invariato il microfono reale — DRVCAM non sostituisce né elabora l'audio.

## Requisiti

- Un dispositivo Android con root (Magisk o KernelSU), Android 9 o successivo. La sostituzione della fotocamera richiede il root; senza di esso l'app si apre ma la sostituzione non è disponibile.
- Un framework della famiglia Xposed compatibile con libxposed API 102 — DRVCAM viene testato con [Vector](https://github.com/JingMatrix/Vector) (il successore di LSPosed), un framework della famiglia LSPosed basato su Zygisk. Un framework privo del supporto API 102 non caricherà il modulo.
- Capacità di decodifica e grafica sufficiente per il contenuto e l'app scelti.

## Scaricare

Questa scheda include la **build per telefono per Android 12 e versioni successive** (arm64). Le altre build — Android da 9 a 11 e le immagini per emulatore — si trovano su **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/)**, con un selettore che consiglia quella adatta al tuo dispositivo.

Ogni versione qui riporta il proprio SHA-256 nelle note di rilascio — verifica il download prima di installare.

## Installare

1. Scarica e installa l'APK corrispondente alla tua versione di Android e al tipo di dispositivo (sopra).
2. Apri il gestore del tuo framework e attiva DRVCAM, quindi riavvia se richiesto.
3. Apri DRVCAM e concedi il root quando richiesto. DRVCAM gestisce l'ambito delle app scelte direttamente dalla propria interfaccia — non serve aggiungere nulla manualmente nel gestore del framework.
4. Accedi, oppure scegli **Prova gratis** (vedi [Piano gratuito e piani a pagamento](#piano-gratuito-e-piani-a-pagamento)).
5. Importa una foto o un video nella Libreria, selezionalo, scegli un'app di destinazione, poi tocca **Enable**. Apri tu stesso la fotocamera dell'app di destinazione.
6. Controlla il risultato all'interno dell'app di destinazione. L'anteprima di DRVCAM aiuta a scegliere il contenuto; da sola non dimostra che l'app di destinazione abbia ricevuto l'immagine.

**Disable** rimuove nuovamente l'ambito di DRVCAM dalla destinazione.

## Piano gratuito e piani a pagamento

DRVCAM richiede un account DRVCAM e una connessione internet per l'accesso, la registrazione del dispositivo e il rinnovo. Dopo l'accesso, l'app può continuare a funzionare offline per un periodo limitato.

- **Prova gratis** (senza costi): sorgenti immagine, un'app di destinazione.
- **Piani a pagamento**: sorgenti video, più app di destinazione, il controller mobile e il cambio di Camera Source.

Piani, limiti dei dispositivi e prezzi attuali: **[droidrooter.com/drvcam](https://www.droidrooter.com/drvcam/#pricing)**.

## Informazioni di base sulla privacy

- I tuoi contenuti restano sul tuo dispositivo per il funzionamento della fotocamera — il servizio account non ha bisogno dei tuoi contenuti o dei fotogrammi della fotocamera per farti accedere.
- Il servizio account elabora dati di account, dispositivo e abbonamento per far funzionare accesso e licenza. I dati diagnostici vengono inviati solo su tua richiesta.
- Un'app di destinazione può comunque salvare, analizzare o trasmettere ciò che mostra la sua fotocamera; si applicano le pratiche sulla privacy di quell'app.
- Informativa completa: [droidrooter.com/privacy](https://www.droidrooter.com/privacy).

## Domande frequenti

**Serve il root?**
Sì. La sostituzione della fotocamera avviene tramite un hook a livello di sistema che richiede il root e un framework compatibile della famiglia Xposed.

**Funzionerà sul mio dispositivo?**
Nella pagina del prodotto sono elencate solo le combinazioni verificate. Dispositivo, firmware e app fotocamera variano troppo per garantire compatibilità in anticipo.

**Posso usarlo senza accedere?**
Sì, con **Prova gratis** (sorgenti immagine, un'app di destinazione). Il video e le altre funzioni richiedono un piano a pagamento.

**Ho perso la password, cosa faccio?**
Per ora il recupero dell'account è manuale; usa i link in [Assistenza](#assistenza) qui sotto.

**Dove si trova il codice sorgente?**
Non è pubblicato qui. Questo repository è una scheda di modulo che distribuisce solo binari di versione firmati.

## Esclusione di responsabilità

DRVCAM è software alpha, fornito "così com'è" senza garanzie di alcun tipo. Eseguire il root di un dispositivo e installare un framework senza sistema sono azioni che compi a tuo rischio e possono incidere sulla garanzia o sulla stabilità del dispositivo.

Sei l'unico responsabile dei contenuti che utilizzi, delle applicazioni con cui usi DRVCAM e del rispetto delle leggi e dei termini a te applicabili. Lo sviluppatore non è responsabile di alcun utilizzo illegale, non autorizzato o altrimenti improprio di questo software.

## Licenza

DRVCAM è software proprietario e a codice chiuso. Non viene concessa alcuna licenza per copiare, modificare, decompilare o ridistribuire l'applicazione. Download e installazione sono disciplinati dai [Termini d'uso](https://www.droidrooter.com/terms) pubblicati sul sito del prodotto.

## Assistenza

- Telegram: [@DroidRooter](https://t.me/DroidRooter)
- Modulo di contatto del sito: [droidrooter.com/contact](https://www.droidrooter.com/contact)

## Changelog

Consulta le note di ogni [versione](https://github.com/Xposed-Modules-Repo/com.droidrooter.virtualcamera/releases) per i dettagli sulle modifiche.

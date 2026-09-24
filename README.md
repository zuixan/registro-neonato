# 🍼 Registro Neonato

**L'app di famiglia per seguire poppate, pannolini, nanne e crescita del tuo bebè.**
Niente cloud. Niente account. Niente pubblicità. I dati vivono solo sul telefono.

![Build APK](../../actions/workflows/android-apk.yml/badge.svg)

---

## ✨ Cosa sa fare

| | |
|---|---|
| 🤱 **Poppate** | seno destro / sinistro / entrambi, durata manuale o con timer (con pausa!) |
| 💧 **Pipì** e 💩 **Cacca** | con colore, per tenere d'occhio tutto |
| 😴 **Sonno** | nanne con timer dedicato |
| 📏 **Misure** | peso e altezza, con storico cliccabile |
| 🔔 **Promemoria** | "sono passate X ore dall'ultima poppata", personalizzabile |
| ⏱️ **Notifica timer** | persistente nel tendino, come il timer di sistema |
| 🔢 **Contatori di oggi** | tutti cliccabili per aprire lo storico completo |
| 🗓️ **Filtri per data** | tutti / oggi / ieri / giorno specifico |
| ✏️ **Modifica tutto** | tocca un evento per correggere durata, note e dettagli |
| 🌙 **Tema scuro** | pensato per le poppate notturne |
| ☁️ **Backup automatico** | file JSON sempre aggiornato in Documenti + export CSV/JSON |
| 👶 **Nome personalizzato** | il titolo dell'app diventa "🍼 Lea" (o come si chiama!) |

---

## 📲 Installala in 2 minuti

1. Vai su **[Releases → ultima versione](../../releases/latest)** e scarica `registro-neonato.apk`.
2. Apri il file sul telefono e consenti l'installazione da origini sconosciute.
3. Se compare l'avviso di **Play Protect**, leggi la sezione qui sotto e procedi serenamente.
4. *(Consigliato)* Installa [Obtainium](https://github.com/ImranR98/Obtainium) e aggiungi questo repository: da quel momento gli aggiornamenti arrivano come su un vero store, con un tap e senza perdere i dati.

---

## 🛡️ Play Protect: perché compare l'avviso e come procedere

Google Play Protect avvisa per **qualsiasi** app non scaricata dal Play Store.
Non sta dicendo "questa app è pericolosa": sta dicendo "non la conosco".
Quest'app è firmata con una chiave personale e distribuita da GitHub, quindi l'avviso è **atteso e innocuo**.

**Come installare comunque:**

1. Scarica l'APK da Releases e aprilo.
2. Alla schermata *"App non riconosciuta"* / *"Play Protect non può verificare quest'app"*:
   - tocca **Altri dettagli** (o "Mostra dettagli");
   - tocca **Installa comunque** (su alcuni dispositivi: "Installa senza scansione").
3. Fatto: l'app è installata e si aggiorna normalmente.

Le diciture possono variare leggermente tra versioni di Android e produttori (Samsung, Motorola, ecc.), ma il senso è sempre lo stesso: *dettagli → installa comunque*.

### Perché è sicura davvero

- **Codice aperto**: tutto il codice è in questo repository, leggibile riga per riga.
- **Build trasparente**: l'APK è compilata da GitHub Actions con il workflow pubblico `.github/workflows/android-apk.yml`, esattamente dal codice che vedi qui.
- **Zero server**: l'app non ha backend, non chiama API, non manda dati da nessuna parte. I dati stanno nella memoria privata del telefono.
- **Permessi minimi**: notifiche (solo se le attivi) e accesso ai file soltanto per i backup/export che chiedi tu.
- **Niente SDK di tracciamento o pubblicità**: solo Capacitor, il wrapper open source che impacchetta la web app in APK.

---

## 🔐 I vostri dati restano vostri

- Tutto è salvato **solo sul dispositivo**.
- **Backup automatico**: a ogni modifica l'app scrive `registro-neonato-autobackup.json` nella cartella Documenti.
- **Export manuale**: CSV (per Excel/Google Sheets) e JSON (backup completo re-importabile).
- **Import**: ripristini un backup in un tap, anche su un altro telefono.
- Gli aggiornamenti (via Obtainium o APK nuova) **non toccano i dati**: si installano sopra e resta tutto.
- Se disinstalli l'app i dati vengono rimossi: fai prima un export JSON se vuoi conservarli.

---

## 🧑‍💻 Note tecniche (per chi sviluppa)

- Web app vanilla (HTML/CSS/JS in un solo file: `www/index.html`) impacchettata con **Capacitor 6**.
- Build APK automatica su GitHub Actions a ogni push su `main`; release versionate `v1.0.<numero build>` con APK allegata.
- Firma stabile con keystore personale conservato nei secrets del repository:
  `KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`, `KEY_ALIAS`.
- **CHANGELOG.md si aggiorna da solo** a ogni push (workflow `changelog.yml`).
- I commit del bot changelog non scatenano nuove build (messaggio con `[skip ci]` + token del bot).

---

## 📜 Changelog

Generato automaticamente dai commit: vedi **[CHANGELOG.md](CHANGELOG.md)**.
Le release con l'APK scaricabile: **[Releases](../../releases)**.

---

## 💝 Licenza

MIT — prendi il codice, modificalo, regalalo.
Nato per una famiglia in una notte insonne; felice se serve ad altre. 🍼

---

*Fatto con ❤️, caffè e nanne interrotte.*

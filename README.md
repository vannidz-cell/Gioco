# 🌠 Meteor AR

Un gioco in **realtà aumentata** che gira nel browser del telefono: inquadri la stanza con la fotocamera, i meteoriti ti "cadono addosso" e li fai esplodere con il mirino!

## ▶️ Gioca ora

**https://vannidz-cell.github.io/Gioco/** — apri dal telefono e consenti la fotocamera.

## 🎮 Come si gioca

1. Apri il gioco sul telefono e tocca **GIOCA**
2. **Consenti l'accesso alla fotocamera** (necessario per la modalità AR)
3. **Muovi il telefono** per puntare il mirino al centro dello schermo
4. **Tocca lo schermo** per sparare: il colpo colpisce il meteorite sotto il dito
5. Distruggi i meteoriti **prima che diventino troppo grandi** e ti colpiscano
6. Hai **3 vite** ❤️ — la difficoltà aumenta a ogni ondata

Se neghi il permesso alla fotocamera, il gioco parte comunque con uno sfondo spaziale.

## 📱 Provalo sul telefono

La fotocamera funziona **solo su HTTPS**. Il modo più semplice è pubblicarlo su **GitHub Pages** (il repository deve essere **pubblico** sui piani gratuiti):

1. Vai su **Settings → Pages** del repository
2. In *Build and deployment → Source* scegli **Deploy from a branch**
3. Seleziona **Branch: `main`** e cartella **`/ (root)`**, poi **Save**
4. Dopo ~1 minuto l'URL `https://<utente>.github.io/Gioco/` è online — aprilo dal telefono

### Provarlo in locale (dallo stesso Wi-Fi)

`getUserMedia` richiede HTTPS anche in locale (tranne su `localhost`). Un modo rapido:

```bash
# dalla cartella del progetto
npx http-server -S -C cert.pem -K key.pem   # con un certificato self-signed
# oppure usa un tunnel:  npx localtunnel --port 8080
```

Su `localhost` (stesso dispositivo) basta un semplice server:

```bash
python3 -m http.server 8080
# apri http://localhost:8080
```

## 🛠️ Come è fatto

- **HTML + Canvas 2D**, tutto in un unico file `index.html`, zero dipendenze
- Fotocamera posteriore come sfondo via `getUserMedia({ facingMode: 'environment' })`
- Meteoriti che crescono simulando l'avvicinamento, esplosioni a particelle, onde d'urto
- Effetti sonori generati in tempo reale con la **Web Audio API** (nessun file audio)
- Vibrazione al colpo subìto (dove supportata)

## 💡 Idee per il futuro

- Meteoriti speciali (bonus, corazzati, che si dividono)
- Power-up (scudo, colpo multiplo, rallenta il tempo)
- Classifica dei punteggi
- Livelli e boss di fine ondata

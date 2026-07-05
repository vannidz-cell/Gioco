# 🌠 Meteor Space

Un gioco arcade nello spazio che gira nel browser (telefono o desktop): navighi tra le **costellazioni**, i meteoriti ti "cadono addosso" e li fai esplodere toccandoli. Attento agli **UFO**!

## ▶️ Gioca ora

**https://vannidz-cell.github.io/Gioco/**

## 🎮 Come si gioca

1. Apri il gioco e tocca **GIOCA**
2. **Tocca un meteorite** per farlo esplodere (mira precisa: colpisci quello che tocchi)
3. I **meteoriti cristallo** (verde-azzurro) si **frantumano in schegge** che rimbalzano sui bordi: toccale per punti bonus
4. Gli **UFO** emergono dallo spazio, si muovono a caso e ti sparano: toccali **3 volte** per abbatterli (+120)
5. Distruggi i meteoriti **prima che diventino troppo grandi** e ti colpiscano
6. Hai **3 vite** ❤️ — la difficoltà aumenta a ogni ondata
7. Sullo sfondo scorrono varie **costellazioni** con i loro nomi

## 🛠️ Come è fatto

- **HTML + Canvas 2D**, tutto in un unico file `index.html`, zero dipendenze
- Campo stellato in movimento con **costellazioni** (Orione, Orsa Maggiore, Cassiopea, Scorpione, Leone, Croce del Sud…)
- Meteoriti che crescono avvicinandosi, tipo speciale che si frantuma in schegge rimbalzanti
- Nemico UFO con comparsa animata, movimento casuale e attacchi
- Esplosioni a particelle, onde d'urto, effetti sonori generati con la **Web Audio API** (nessun file audio)
- Vibrazione al colpo subìto (dove supportata)

## 📱 Pubblicazione (GitHub Pages)

Il gioco è statico: basta servire `index.html` su HTTPS. Con GitHub Pages (repository **pubblico** sui piani gratuiti):

1. **Settings → Pages**
2. In *Build and deployment → Source* scegli **Deploy from a branch**
3. **Branch: `main`**, cartella **`/ (root)`**, poi **Save**
4. Dopo ~1 minuto l'URL `https://<utente>.github.io/Gioco/` è online

### In locale

```bash
python3 -m http.server 8080
# apri http://localhost:8080
```

## 💡 Idee per il futuro

- Cristalli di colori diversi con effetti (rallenta il tempo, punti tripli, scudo)
- Boss di fine ondata
- Classifica dei punteggi
- Asteroidi che si dividono a catena

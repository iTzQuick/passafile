# Passafile

Mini app web per trasferire file tra telefono e PC (in entrambe le direzioni), senza installare niente.
È una sola pagina (`index.html`) che si pubblica gratis su GitHub Pages.

## Come funziona

- I file passano **direttamente** da un dispositivo all'altro (WebRTC, tramite PeerJS): non vengono caricati su GitHub né su altri server.
- GitHub serve solo a ospitare la pagina. Il server pubblico di PeerJS serve solo a far "trovare" i due dispositivi all'inizio.

## Pubblicare su GitHub Pages

1. Su github.com crea un nuovo repository (es. `passafile`), pubblico.
2. **Add file → Upload files**, carica `index.html` (e questo README), poi **Commit changes**.
3. **Settings → Pages**: in *Build and deployment* scegli *Deploy from a branch*, branch `main`, cartella `/ (root)`, **Save**.
4. Dopo un minuto la app è su `https://<tuo-utente>.github.io/passafile/`.

## Uso

1. Sul **PC** apri l'indirizzo: compare un QR code.
2. Sul **telefono** inquadra il QR con la fotocamera e apri il link.
3. Quando lo stato diventa verde ("Collegato"), scegli i file da inviare da uno qualunque dei due dispositivi.
4. Sul dispositivo che riceve il file si scarica da solo; se il browser lo blocca, tocca **Salva**.

## Note

- Tieni aperte entrambe le pagine finché il trasferimento non finisce.
- Ogni volta che ricarichi la pagina sul PC il QR cambia: va inquadrato di nuovo.
- I file ricevuti restano in memoria finché non li salvi: per file molto grandi (vari GB) meglio dividerli.
- Su alcune reti aziendali/scolastiche con firewall rigidi il collegamento diretto può non riuscire.

# citatesi-addin

Hosting statico dei file del Word add-in di [CitaTesi](https://github.com/meccanicastefano-cloud/SoftwareTesi).

Office richiede HTTPS per caricare un taskpane add-in; i file HTML/JS/CSS/icone
vivono qui (GitHub Pages) perché il repo principale è privato e il piano free
di GitHub non supporta Pages su repo privati.

**Questo repo contiene solo artefatti di build**: il codice sorgente è in
`word-addin/` del repo principale. Ogni aggiornamento si fa via:

```powershell
# Nel repo principale SoftwareTesi:
cd word-addin
npm run build
# copia dist/* qui, commit, push
```

I dati dell'utente CitaTesi **non passano mai** da questo hosting: Word comunica
direttamente col server locale `http://localhost:19627` per fonti, citazioni e
bibliografia. Qui viaggiano solo asset statici pubblici.

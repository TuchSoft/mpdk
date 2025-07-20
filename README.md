# Sviluppo Moodle
In questa cartella sono contenute diversioni di Moodle usate per lo sviluppo.
La struttura della cartella è come segue:
- `moodle-docker`: contiene il repo `moodlehq/moodle-docker` (usato per il testing)
- `phpmoodle`: contiene il repo `tuchsoft/phpmoodle` (usato per lo sviluppo)
- `zip`: contiene i pacchetti zip originali delle varie versioni
- `xxx`: contiene una versione di moodle per lo sviluppo/test manuali
- `xxx_testing`: contiene una versione di moodle per i test automatici
- `run`: eseguibile per lanciare una piattaforma

## Per lanciare una piattaforma
Lanciare il comando:
```bash
./run <version[_testing]> <port>
```

Se il nome include `_testing` verra lanciata con `oodlehq/moodle-docker`, pronta per essere utilizzata per con `moodle-plugin-ci`.
Altrimenti viene lanciata con `tuchsoft/phpmoodle`.

## Per terminare una piattaforma
Usare la GUI di docker.


## Utilizzo
- I plugin vanno sviluppati nella cartella `~/Progetti` .
- Vanno nominati `moodle-plugintype_pluginname`.
- Clonare i file utili da `tuchsoft/moodle-plugin_template`.
- Impostare il deploy locale con PhpStorm nelle versioni di Moodle desiderate
- Sviluppare il plugin usando la versione con `tuchsoft/phpmoodle`
- Quando si è pronti per iniziare i test
- Fare il deploy su una versione `_testing`
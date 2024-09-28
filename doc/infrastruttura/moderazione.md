# Comandi di moderazione
## Sintassi
### Attraverso username
`/comando @username [motivazione]`\
Il modo più semplice di usare un comando di moderazione. La motivazione è
opzionale ma utile inserirla anche per l'auditing nel caso ce ne fosse bisogno.

### Attraverso menzione
`/comando menzione [motivazione]`\
Sintassi analoga per gli utenti senza username.

### Attraverso ID
`/comando ID [motivazione]`\
Questo per gli utenti che sono senza username e cercano di fare ban evasion
cambiando nome. L'ID si può trovare andando a vedere il canale dei log.

### Per risposta
`/comando [motivazione]`\
Sintassi utilizzata in risposta al messaggio di target. Questa è la più
utilizzata perchè la più comoda.

## Comandi
### `/claim`
Nel caso il bot non avesse automaticamente assegnato i poteri all'utente, può
richiedere manualmente la concessione di questo poteri dal bot.

### `/info`
Riceve dal bot tutte le informazioni riguardanti il target. Per poter usufruire
di questa feature bisogna però iniziare un conversazione in privato col bot,
questo perchè telegram non permette ai bot di iniziare una conversazione privata
con utenti.

### `/mute`
Toglie il potere di mandare messaggi sul gruppo

### `/del`
Elimina il messaggio. Questo comando esiste perchè per motivi di auditing i
moderatori non hanno accesso diretto al privilegio di eliminare messaggi
attraverso l'interfaccia di telegram (e questo è vero per anche altri poteri).

### `/warn`
Ammonisce il target.

### `/kick`
Espelle l'utente dal gruppo.

### `/ban`
Bandisce un utente dal gruppo.

### `/superban`
Bandisce un utente da tutti i gruppi del Network.

### `/free`
Toglie le limitazioni imposte da `mute` e `ban` sul gruppo.

### `/superfree`
Toglie le limitazioni imposte da `superban`.

### Sintassi con asterisco
`/comando*`\
Da utilizzare solo se si utilizza la sintassi per risposta. Serve per i comandi
di moderazione come `warn`, `mute`, etc. Con questa sintassi oltre a eseguire il
comando, come può essere il `warn`, poi esegue anche il comando `del`. Questo
perchè molto spesso l'intenzione è cancellare il messaggio che necessitava
moderazione.

**TORNEO DI SCACCHI**
RICHIESTA:
Si vuole progettare una base di dati per gestire un torneo di scacchi.
--------------------------------------
ANALISI:
Dobbiamo creare uno schema er che possa gestire le partite di scacchi programmate, in corso e finite. Oltre alle partite dobbiamo anche salvare i giocatori e le aperture.
---------------------------------------
Entità che voglio usare:
1. giocatore: nome, cognome, titolo, nTorneiVinti, idGiocatore; 
*Chiave*: idGiocatore;
2. partita: idPartita;
*Chiave*: idPartita;
3. partitaFinita: coloreGiocatore, risultato;
*Chiave*: (FK) idPartita;
4. partitaProgrammate: ?;
*Chiave*: (FK) idPartita;
5. partitaInCorso: scacchiera (rappresentato in una stringa);
*Chiave*: (FK) idPartita;
6. apertura: nome, variante;
*Chiave*: (composta) nome, variante;
-------------------------------------
ESEMPIO:
Magnus Carlsen (GM che ha vinto 500 tornei) giocherà questo sabato contro Levy Rozman (IM che ha vinto 100 tornei).
Quando la partita sarà in corso, il database sarà costantemente aggiornato con la posizione della scacchiera, rappresentata da una stringa divise in righe nelle quali troviamo il nome del pezzo e la posizione divisi da uno spazio, e salverà il nome delle aperture quando sarà finita la teoria.
-------------------------------------
SCHEMA ER:


# Telegram Bot per Screenshot del Bilancio Scommesse

Un bot Telegram che utilizza Selenium e Python per catturare uno screenshot del bilancio delle scommesse dalla pagina di Bet Analytix e inviarlo automaticamente agli utenti tramite Telegram. Il bot include anche una descrizione che riassume il bilancio degli ultimi tre mesi, con l'aggiunta di emoji che indicano visivamente il risultato positivo o negativo.

## Caratteristiche

- Utilizza Selenium per navigare sul sito e fare lo screenshot della pagina del bilancio.
- Invia lo screenshot tramite Telegram all'utente che richiede le statistiche.
- Mostra i risultati del bilancio degli ultimi tre mesi con emoji:
  - ✅ Bilancio positivo.
  - 🔝 Se il bilancio supera i 200 euro.
  - ❌ Bilancio negativo.
- Utilizza il bot Telegram per richiedere le statistiche rapidamente.

## Tecnologie Utilizzate

- **Python**: linguaggio principale per la logica del bot.
- **Selenium**: per l'automazione del browser e la cattura dello screenshot.
- **Pillow (PIL)**: per ritagliare l'immagine ottenuta.
- **Telegram Bot API**: per interagire con gli utenti su Telegram.
- **WebDriver Manager**: per gestire automaticamente l'installazione del driver di Chrome.

## Requisiti

- **Python 3.7+**
- **Chromedriver**: utilizzato da Selenium per pilotare il browser Chrome. Viene gestito automaticamente con WebDriver Manager.
- **Token Telegram**: ottieni un token per il tuo bot tramite [BotFather](https://t.me/botfather) su Telegram.

## Installazione

1. Clona il repository:
   ```bash
   git clone https://github.com/tuo-username/telegram-bot-betting-screenshot.git
   cd telegram-bot-betting-screenshot
   ```

2. Crea un ambiente virtuale e attivalo:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Su Windows usa `venv\Scripts\activate`
   ```

3. Installa le dipendenze:
   ```bash
   pip install -r requirements.txt
   ```

4. Configura il token del bot Telegram nel file Python principale (`TELEGRAM_TOKEN`).

5. Esegui il bot:
   ```bash
   python main.py
   ```

## Utilizzo

Dopo aver eseguito il bot, puoi interagire con esso su Telegram tramite il comando `/statistiche` per ricevere lo screenshot del bilancio delle scommesse.

## Struttura del Progetto

- **main.py**: Il file principale che contiene la logica del bot.
- **requirements.txt**: Elenco delle dipendenze richieste dal progetto.

## Emoji nel Bilancio

- **Bilancio Positivo**: Il bilancio verrà accompagnato da un'emoji verde `✅`.
- **Bilancio Maggiore di 200€**: Verrà aggiunta anche l'emoji `🔝`.
- **Bilancio Negativo**: Verrà visualizzata un'emoji con croce rossa `❌`.

## Note Importanti

- Il bot utilizza Selenium in modalità headless per evitare l'apertura della finestra del browser durante l'esecuzione.
- Assicurati che il tuo ambiente abbia accesso a Google Chrome.

## Problemi Comuni

- **Il browser si apre ogni volta**: Verifica che l'opzione `--headless` sia attiva nelle impostazioni di Selenium.
- **Errore di compatibilità del driver**: Utilizza `webdriver-manager` per gestire l'installazione e l'aggiornamento del driver di Chrome.

## Contribuzione

Le contribuzioni sono benvenute! Sentiti libero di aprire un problema o fare una pull request con nuove funzionalità o miglioramenti.

## Licenza

Questo progetto è rilasciato sotto la licenza MIT. Vedi il file [LICENSE](LICENSE) per maggiori dettagli.


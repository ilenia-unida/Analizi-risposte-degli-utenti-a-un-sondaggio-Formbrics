# 💬 Flusso Automatico: Sentiment Analysis e Risposta Email Personalizzata

Un workflow di **CRM Automation** essenziale, costruito con **n8n**, che sfrutta l'Intelligenza Artificiale per analizzare il tono del feedback dei clienti e attivare una risposta personalizzata e mirata. Questo assicura che i clienti che esprimono frustrazione o problemi ricevano una rapida azione di "Follow-up", mentre i clienti soddisfatti ricevano una mail di "Cortesia".

## Caratteristiche & Funzionalità

* **Webhook Trigger:** 📥 Il flusso è avviato da un **Webhook**, tipicamente collegato a un form di feedback o a un sistema di sondaggio (es. Typeform, Google Form, o un'API esterna).
* **AI Sentiment Analysis:** 🧠 Il nodo **Sentiment Analysis** utilizza un modello AI (come Gemini) per classificare il testo non strutturato (es. il campo "Motivazione" del feedback) in positivo, negativo o neutro.
* **Logica Condizionale Dinamica:** ⚖️ L'output dell'AI alimenta un nodo **IF** che biforca il flusso, instradando le risposte in base alla classificazione del sentiment.
* **Risposta Personalizzata:** 📧 Invia email diverse tramite **Gmail**: una per il sentiment negativo (per un rapido follow-up operativo) e una per il sentiment positivo o neutro (un ringraziamento di cortesia).

## Struttura del Flusso

Questo flusso è un eccellente esempio di logica condizionale avanzata:

* **Webhook:** 👂 Riceve i dati in tempo reale.
* **Estrai payload (Code):** 🧹 Pulisce e formatta i dati in ingresso.
* **Sentiment Analysis:** 💡 Classificazione del testo tramite AI.
* **IF - Sentiment Analysis:** 🚦 Logica di smistamento (es. se Negativo va a Follow-up, altrimenti a Cortesia).
* **Prepara mail (Negativo) & Follow-up (Gmail):** Ramo per la gestione dei problemi.
* **Prepara mail (Positivo) & Cortesia (Gmail):** Ramo per la gestione dei ringraziamenti.

## Video di Spiegazione

Per una spiegazione dettagliata del funzionamento del Webhook, del nodo Sentiment Analysis di n8n e della logica condizionale che personalizza la risposta, guarda il video qui sotto:

[Spiegazione dettagliata del Flusso Sentiment Analysis su YouTube](https://youtu.be/3iqY0xf6BTo)

## Requisiti

Per utilizzare questo flusso, è necessario configurare le credenziali per il seguente servizio:

* **Gmail Account** (per l'invio delle email automatiche).

---


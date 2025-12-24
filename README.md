# 📓 Dziennik Wdzięczności z AI (n8n Workflow)

Automatyczny system do prowadzenia dziennika wdzięczności, który łączy **n8n**, **Telegram**, **Google Sheets** oraz model **Google Gemini AI**.

## 🚀 Funkcjonalności

Workflow realizuje dwa kluczowe zadania:

### 1. Codzienne zbieranie wpisów
* **Harmonogram:** Codziennie o godzinie **20:00** bot inicjuje kontakt.
* **Interakcja:** Bot wysyła wiadomość na Telegramie z pytaniem: *"Za co jesteś wdzięczny?"* i oczekuje na odpowiedź użytkownika.
* **Archiwizacja:** Treść odpowiedzi jest zapisywana w arkuszu **Google Sheets** wraz z precyzyjną datą i czasem (strefa czasowa `Europe/Warsaw`).

### 2. Inteligentne podsumowanie miesiąca
* **Harmonogram:** Raz w miesiącu o godzinie **07:00**.
* **Analiza AI:** System pobiera wszystkie wpisy z ostatniego okresu, a następnie przesyła je do modelu **Gemini 1.5 Flash**.
* **Raport:** AI generuje podsumowanie Twoich sukcesów i pozytywnych chwil, które jest wysyłane bezpośrednio na Telegram w czytelnym formacie Markdown.

## 🛠️ Stos technologiczny

| Narzędzie | Rola |
| :--- | :--- |
| **n8n** | Automatyzacja i logika workflow |
| **Telegram Bot** | Interfejs komunikacji z użytkownikiem |
| **Google Sheets** | Przechowywanie danych (baza wpisów) |
| **Google Gemini** | Analiza treści i generowanie podsumowań |
| **JavaScript** | Przetwarzanie i formatowanie danych |

## ⚙️ Konfiguracja

Aby uruchomić ten workflow, wymagane jest skonfigurowanie następujących poświadczeń (Credentials) w n8n:
1.  **Telegram API:** Token bota stworzony przez `@BotFather`.
2.  **Google Sheets OAuth

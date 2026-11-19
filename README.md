# Projekt1-Grupp2
# Projektbeskrivning (PRO1): Studiero-kollen (Ljudnivåmätning)

## 1. Från sensor till visualisering och kunskap
* **Sensor:** Ljudsensor (mikrofon) placerad i studieytor/läsesalar på MDU. Sensorn mäter endast ljudstyrka i decibel (dB) – inga samtal spelas in.
* **Visualisering (Webbsida med Bootstrap & Chart.js):**
  * **Aktuellt värde:** En tydlig statusruta med trafikljusfärger:
    * 🟢 **Grön (< 45 dB):** Tyst – bra för djupfokus.
    * 🟡 **Gul (45–60 dB):** Lågt sorl – passar grupparbete.
    * 🔴 **Röd (> 60 dB):** Högljutt – välj en annan plats.
  * **Historiska värden:** Ett diagram (Chart.js) som visar ljudnivån timme för timme under dagen och veckan.
* **Kunskap:** Studenten får direkt kunskap om **vilken studieplats som är lugnast just nu** samt **vilka tider på dygnet det brukar vara tystast**.

## 2. Användaranalys
* **Användare:** Studenter på MDU som söker en lugn studieplats inför eget plugg eller grupparbete.
* **Behov:** Vill snabbt se var det är ledigt och tyst utan att behöva gå runt i hela byggnaden eller tolka svåra siffror.
* **Hur användaren påverkar vår design:**
  * Eftersom användaren vill ha svar på några sekunder använder vi **tydliga färgblock (grönt/gult/rött)** och stora ikoner i stället för bara råa decibelsiffror.
  * Vi lägger till en enkel rekommendation i text (t.ex. *"Just nu: Lugnt i Biblioteket plan 2"*).

## 3. Kontextanalys
* **Kontext (miljö):** Används ofta på språng i mobilen (på väg till campus eller i korridoren) eller på en informationsskärm utanför läsesalen. I läsesalen måste det dessutom vara tyst.
* **Hur kontexten påverkar vår design:**
  * **Mobilanpassad (Responsiv med Bootstrap):** Eftersom studenter kollar i mobilen på väg till en sal måste kort och grafer anpassa sig till små skärmar.
  * **Helt tyst gränssnitt:** Inga ljudnotiser i gränssnittet, bara visuella varningar, så att man inte stör i en tyst läsesal.
  * **Integritet:** Endast dB-siffror sparas och visas. Inga ljudinspelningar sker. 

# Projekt1-Grupp2
# Projektbeskrivning (PRO1): Studiero-kollen (Ljudnivåmätning)

## 1. Från sensor till visualisering och kunskap
Vi kallar vårt projekt **Studiero-kollen**. Det handlar om något som jag tror att de flesta studenter känner igen. Man behöver plugga och letar efter en lugn plats, kanske i biblioteket eller i någon av skolans studiesalar. Men när man väl kommer dit märker man att det är mycket prat och ljud. Då måste man kanske leta efter en annan plats.

Så vi började fundera: **Tänk om man kunde se hur lugnt det är på en studieplats innan man ens går dit?**

### Hur fungerar det?

Vi vill placera små ljudsensorer på olika studieplatser i biblioteket på MDU i Eskilstuna. En ljudsensor mäter hur högt eller lågt ljudet är. Ljudnivån mäts i **decibel (dB)**. Ju högre värde, desto högre är ljudnivån. En viktig sak är att sensorn inte ska spela in vad människor säger. Den ska bara mäta ljudnivån, inte själva samtalen.

**Sensorn vi kommer använda är:** https://www.amazon.se/-/en/Youmile-Microphone-Sensitivity-Detection-Arduino/dp/B087R83YGB/ref=sr_1_2?crid=3I2ZWGUKWII18&dib=eyJ2IjoiMSJ9.AVZoq8S53bai2Dsq5RT63EM6lL_0rB8aSf-MNRu1NVZ7X38Fy-cSSIhD9jIwaWPfAlR3W6enAvEZh9B4jMOf_2N_iAWwhm2HH3OWTBu_4XIEI8flaEFH1VtrUQDJYSY5hU608vpvu9GXg8Dua3JOVZ35F10HQGOEbDF7o_K7N6HBMl0mw9O_hWSMmdjayizDQH2wlWeqwuew-6gjQI8c4_rEx4WhJSx6XuFPvmUGkZFVK3FFdlP0fgy_19SCtForVvT3jsRItBGcgzZSyF1HNMTA1dtkWf6uiNocQWQ7blE.Bwm_LsnU4Ym782CulaKktGjdSAzbIqFIJcCRDsH_C-s&dib_tag=se&keywords=ljud+sensor+arduino&qid=1795763441&sprefix=ljud+sensor+arduino%2Caps%2C166&sr=8-2 

### Hur visas ljudnivån?

Ljudnivån ska visas på en webbsida. Vi vill göra det så enkelt som möjligt för studenten att förstå, utan att behöva tolka en massa siffror.
Därför använder vi samma princip som ett trafikljus:

🟢 **Grönt (under 45 dB):** Det är lugnt och tyst. Det passar bra för den som vill plugga ostört och koncentrera sig.

🟡 **Gult (45–60 dB):** Det är lite mer ljud. Folk kanske pratar eller arbetar i grupper. Platsen kan därför passa bättre för grupparbete.

🔴 **Rött (över 60 dB):** Här är det ganska högljutt. Om man behöver lugn och ro kan det vara bättre att välja en annan studieplats.

### Diagram – Chart.js

Vi vill också använda ett **diagram med Chart.js** som visar hur ljudnivån förändras under dagen och veckan.
Det betyder att studenten inte bara kan se hur högt ljudet är just nu, utan också hur det har sett ut tidigare.
Till exempel kanske en plats är lugnare på morgonen men mer högljutt på eftermiddagen. Genom diagrammet kan studenten upptäcka sådana mönster och lättare planera när och var det passar bäst att plugga.
På det här sättet vill vi göra det enklare för studenter att hitta en studieplats som passar deras behov.

### Kunskap
Kunskap uppstår hos en person när den kan förstå och ta till sig information på ett sätt som gör att den lär sig något. I detta fall ska studenter få kunskap om vilken eller vilka studieplatser som passar dem.

## 2. Användaranalys
* **Användare:** Studenter på MDU som söker en lugn studieplats inför eget plugg eller grupparbete.
* **Behov:** Vill snabbt se var det är ledigt och tyst utan att behöva gå runt i hela byggnaden eller tolka svåra siffror.
* **Hur användaren påverkar vår design:**
  * Eftersom användaren vill ha svar på några sekunder använder vi **tydliga färgblock (grönt/gult/rött)** och stora ikoner i stället för bara råa decibelsiffror.
  * Vi lägger till en enkel rekommendation i text (t.ex. *"Just nu: Lugnt i Biblioteket plan 2"*).

## 3. Kontextanalys
* **Kontext:** Används ofta på språng i mobilen (på väg till campus eller i korridoren) eller på en informationsskärm utanför läsesalen. I läsesalen måste det dessutom vara tyst.
* **Hur kontexten påverkar vår design:**
  * **Mobilanpassad (Responsiv med Bootstrap):** Eftersom studenter kollar i mobilen på väg till en sal måste kort och grafer anpassa sig till små skärmar.
  * **Helt tyst gränssnitt:** Inga ljudnotiser i gränssnittet, bara visuella varningar, så att man inte stör i en tyst läsesal.
  * **Integritet:** Endast dB-siffror sparas och visas. Inga ljudinspelningar sker. 

## 4. Syfte och mål
Syftet med studierokollen är att snabbt visa för studenter vilken ljudnivå det är på olika platser i biblioteket på MDU Eskilstuna. Det ska ge dem kunskap om var det finns en studieplats som passar just deras arbete. Detta ska göras med ett human centered design-perspektiv för att skapa bästa möjliga användarupplevelse. 

## 5. Avgränsningar 
* Mäter och visar endast studieplatser i biblioteket på MDU Eskilstuna.
* Ljudnivån visas genom färger, grön, orange och röd, tillsammans med ikoner.
* Mäter ljudnivån efter mänskligt tal.
* Spelar inte in ljud.
* Mäter och visar inte hur många som befinner sig på platsen.

## 6. Förslag på visualiseringar 
* En karta med olika cirklar, som representerar olika studieplatser, och som byter färg efter aktuell ljudnivå på platsen. Klickar man på en cirkel får man fram en ruta som visar en ikon som symboliserar ljudnivån samt en text likt: "passande för grupparbete". Ett kryss i hörnet av rutan finns för att kunna stänga ner den. 

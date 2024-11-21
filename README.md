<details>
  <summary>Tema 3: Quick Time</summary>
 
  # Descrierea task-ului:
În acest proiect, vom dezvolta un joc competitiv de reflexe pentru doi jucători, care vor concura pentru a obține cel mai mare punctaj. Jocul testează viteza de reacție și include mai multe runde. 
 
- **Fiecare jucător:** are propriile LED-uri și butoane. LED-urile RGB indică culoarea activă, iar scopul este ca jucătorul să apese rapid butonul corespunzător culorii afișate.
- **Afișarea scorurilor:** se realizează pe un LCD și este actualizată în timp real.
- **Finalul jocului:** jucătorul cu cel mai mare punctaj este declarat câștigător.
 
---
 
## **Componente utilizate**
- **6x LED-uri** (2 grupuri a câte 3 LED-uri, fiecare grup cu culori diferite)
- **2x LED RGB** (1 pentru fiecare jucător)
- **6x Butoane** (3 pentru fiecare jucător)
- **1x LCD**
- **1x Servomotor** (pentru indicarea progresului sau timpul final)
- **2x Breadboard**
- **Fire de legătură**
- **2x Arduino UNO**
 
---
 
## **Implementare**
 
### **1. Inițializare joc**
- Jocul începe cu afișarea unui mesaj de bun venit pe LCD.
- Apăsarea unui buton declanșează startul jocului. Posibilități pentru implementare:
  - Apăsarea oricărui buton.
  - Buton dedicat pentru startul jocului (marcat pe breadboard).
  - Buton suplimentar pentru start/resetare.
 
---
 
### **2. Desfășurarea rundelor**
- **Fiecare jucător:** are asociate 3 butoane și un LED RGB.
- **La începutul fiecărei runde:** LED-ul RGB al jucătorului activ se aprinde într-o culoare specifică.
- **Jucătorul activ:** apasă cât mai rapid butonul corespunzător culorii afișate. Punctajul este acordat pe baza vitezei de reacție.
- **Actualizarea scorului:** pe LCD după fiecare rundă.
 
---
 
### **3. Timpul și finalizarea jocului**
- **Servomotorul:** indică progresul rundelor și se rotește complet la sfârșitul jocului.
- **La final:** LCD-ul afișează numele câștigătorului și scorul final.
 
---
 
## **Detalii tehnice**
 
### **1. Comunicarea SPI între 2 plăci Arduino**
- **Master Arduino UNO:** Controlează LCD-ul și servomotorul, monitorizând punctajele.
- **Slave Arduino UNO:** Controlează butoanele și LED-urile jucătorilor, trimițând informații către master.
 
### **2. Implementarea butoanelor**
- Fiecare jucător are 3 butoane corespunzătoare celor 3 LED-uri de culori diferite.
- Multiplexarea butoanelor se poate realiza pentru a reduce numărul de pini utilizați.
 
### **3. LED-urile**
- LED-urile RGB indică culorile pentru butoanele jucătorilor.
- LED-urile trebuie să se stingă când nu este rândul unui jucător.
 
### **4. LCD**
- Utilizează biblioteca `LiquidCrystal` pentru control.
- Afișează punctajele în timp real.
 
### **5. Servomotorul**
- Indică progresul jocului prin rotații.
 
---
 
## **Libertatea de personalizare**
- Punctajele acordate pe baza vitezei de reacție.
- Intervalul de timp dintre runde.
- Durata totală a jocului.
 
---
 
## **Schema electrică**
Urmează să fie realizată o schemă electrică detaliată utilizând Fritzing pentru conectarea tuturor componentelor (Arduino UNO, butoane, LED-uri, LCD, servomotor).
 
---
 
## **Concluzii**
Proiectul "Quick Time" este un joc de reflexe care testează viteza de reacție a jucătorilor și include multiple componente hardware pentru funcționalități interactive. Acesta reprezintă o oportunitate excelentă de a lucra cu comunicarea SPI între două plăci Arduino și de a integra mai multe module într-un singur sistem.
 
 
  # Video cu funcționalitatea montajului fizic
  [Watch the demo video](https://github.com/EduardDobrin123/Robotica-Tema3/blob/main/Tema%203/media/Clip%20video%20WhatsApp%202024-11-21%20la%2022.10.01_f74493dd.mp4)
 
  # Schema electrică
  ![image](https://github.com/EduardDobrin123/Robotica-Tema3/blob/main/Tema%203/media/Imagine%20WhatsApp%202024-11-21%20la%2022.11.42_3cfa221f.jpg)
 
 
</details>

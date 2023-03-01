# [TEMPLATE] Cybersecurity/Cybersäkerhet
Här är alla instruktioner till momentet plus lite olika resuser. Ni kommer behöva skriva egna anteckningar i en README så antingen döper ni om denna och skapar en egen eller så slänger ni in era anteckningar rakt i denna README. Gör det gärna tydligt då vart era anteckningar är.

[Länk till Github Classroom](https://classroom.github.com/a/-4vRRdBP)

## Del 1 - Påläsning
Kommer lite genomgångar men här är en del bra länkar för egen påläsning.
* [Ethical Hacking in 100 Seconds](https://www.youtube.com/watch?v=v969_M6cWk0)
* [Cybersecurity 101](https://medium.com/edureka/what-is-cybersecurity-778feb0da72)
* [Mini kurser](https://www.edureka.co/blog/?utm_source=medium&utm_medium=content-link&utm_campaign=what-is-cybersecurity)
* [Cybersecurity for small buissnesses](https://www.ftc.gov/system/files/attachments/cybersecurity-small-business/cybersecuirty_sb_factsheets_all.pdf)


![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*lAcruAVFzMelVQYvyaB00A.png)

![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*9Fv6GRawoVVcp4c6zm_EiQ.png)


### Vad är cybersäkerhet?
*"Computer security, cybersecurity (cyber security), or information technology security (IT security) is the protection of computer systems and networks from attack by malicious actors that may result in unauthorized information disclosure, theft of, or damage to hardware, software, or data, as well as from the disruption or misdirection of the services they provide."*
  
*"Datasäkerhet är den delen av IT-säkerhet som avser att skydda datorsystem. I detta ingår förebyggande, upptäckt och åtgärdande av obehöriga användare av datorsystem, bland annat hackers och virus. Men datasäkerhet innebär också att man skyddar datorsystem mot andra risker, som till exempel förlust av data på grund av en hårddiskkrasch."*

## Del 2 - Kryptografi
Länk till kort medium artikel om grundläggande kryptografi: [What is Cryptography? — An Introduction to Cryptographic Algorithms](https://medium.com/edureka/what-is-cryptography-c94dae2d5974)  
TL/DR: Kryptografi är studien och tillämpningen av tekniker som används för att säkra kommunikation och data från obehöriga. Kryptografi använder kryptering för att omvandla läsbara meddelanden till oläsliga former för att skydda meddelandets konfidentialitet.   
Krypteringsalgoritmer är uppdelade i två kategorier: Symmetrisk nyckelkryptografi och Asymmetrisk nyckelkryptografi.  
- *Symmetrisk nyckelkryptografi* är uppdelad i Klassisk kryptografi, vilket inkluderar Transpositionschiffer och Substitutionschiffer, och Modern kryptografi, vilket inkluderar Strömkryptering och Blockkryptering.
- *Asymmetrisk nyckelkryptografi* eller Offentlig nyckelkryptografi använder olika nycklar för att kryptera och dekryptera information, och RSA är den mest använda formen av offentlig nyckelkryptering.
![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*-ZubnDvcxP7cy8JUgUX4Eg.png)

### Några enklare chiffer som är bra att känna till:  
* **Vigenère chiffer:** Detta är en annan symmetrisk chiffer som är en utveckling av Caesar chiffer. I stället för att använda en fast nyckel för att koda texten, använder Vigenère chiffer en nyckel som är en sekvens av bokstäver.
* **ROT13 chiffer:** Det är en enkel symmetrisk chiffer som flyttar varje bokstav 13 steg i alfabetet. Precis som caesar chiffret förutom med ett bestämt antal steg.  
```
Hello World -> Uryyb Jbeyq    // ROT13 chiffer
```
*P.S. Det är viktigt att notera att dessa chiffer inte är särskilt säkra eftersom de är enkla att knäcka.*

* **AES (Advanced Encryption Standard):** en symmetrisk krypteringsstandard. AES fungerar genom att dela in informationen i små block och använder en serie matematiska operationer på blocken och nyckelinformationen för att konvertera dem till en okänd form. Denna form kan bara dekoderas med hjälp av samma nyckel som användes vid kodningen. AES har nyckelstorlekar på 128, 192 eller 256 bitar.
* **RSA (Rivest-Shamir-Adleman):** en asymmetrisk krypteringsalgoritm. När informationen kodas med hjälp av en offentlig nyckel, kan den bara dekoderas med hjälp av den motsvarande privata nyckeln. Detta gör RSA till en mycket säker metod för kryptering, eftersom det är svårt att dekoda informationen utan tillgång till den privata nyckeln. Nyckelstorleken i RSA kan vara upp till 4 096 bitar, vilket gör den lämplig för kryptering av mycket känslig information.  
* **Blowfish:** en symmetrisk krypteringsalgoritm. Blowfish är känt för sin snabbhet och säkerhet. Det är en robust algoritm med en stor nyckelstorlek (upp till 448 bitar) och är därför lämplig för kryptering av stora mängder data. 
### Uppgift för kryptografi momentet
Välj en egen algoritm att implementera i Python eller C#. Ni får välja fritt vilken men här är lite förslag och motsvarande uppskattad svårhetsgrad:
- Lätt: [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher)
- Medium: [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem))
- Svår: [Enigma](https://en.wikipedia.org/wiki/Enigma_machine)
  - Den är egentligen inte den mest komplicerade krypteringstekniken men den ligger till grund för mycket inom området.
  - [Code Bullets video om hans implementering](https://www.youtube.com/watch?v=2D2bJWHvqJo&t=459s)

Jag vill att ni implementerar *minst* en av dessa algoritmer och lägger i mappen "cryptography", filen ska ha samma namn som algoritmen ni implementerat. Kommentera koden och förklara stegvis med egna ord hur algoritmen fungerar. Skriv även en kort analys i er README över algoritmens styrkor och svagheter.
## Del 3 - Backup and error detection
### - Hamming codes
3Blue1Brown har en bra liten miniserie:  
1. [How to send a self-correcting message (Hamming codes)](https://www.youtube.com/watch?v=X8jsijhllIA)
2. [Hamming codes part 2, the elegance of it all](https://www.youtube.com/watch?v=b3NxrZOu_CE)
  
Ben Eaters video om hur det fungerar i hårdvaran:
1. [What is error correction? Hamming codes in hardware](https://www.youtube.com/watch?v=h0jloehRKas)

#### Exempel på hur Hamming codes kan användas:
```
message = 11000011
```
1. Determine the number of parity bits needed
   1. The number of parity bits required is calculated by finding the smallest integer (r) that satisfies the following condition:
   2. `2^r >= r + m + 1`, where `m` is the number of message bits.
   3. Here, `m = 8`, so we have:
   4. `2^r >= r + 8 + 1`
   5. `2^r >= r + 9`
   6. By trying different values of `r`, we find that `r = 4` satisfies this condition.
2. Position the parity bits
   1. The next step is to position the parity bits within the Hamming code. The positions of the parity bits are given by the powers of 2, counting from the left, starting with position 1. Therefore, the positions of the parity bits in the Hamming code are: 1, 2, 4, and 8.
3. Determine the values of the parity bits
   1. The values of the parity bits are calculated as follows:
   2. For each parity bit position i, determine the set of data bits whose binary representation includes a 1 in the i-th position.
   3. Add up the values of the data bits in each set.
   4. If the sum of the data bits in a set is even, the value of the parity bit in that position is 0. If the sum is odd, the value of the parity bit is 1.

Using these steps, we can generate the Hamming code for the message `11000011`:
1. Message bits: 1 1 0 0 0 0 1 1
2. bit 1 - parity: 1 (covers bits 1,3,5,7,9,11)
3. bit 2 - parity: 1 (covers bits 2,3,6,7,10,11)
4. bit 3 - message: 0
5. bit 4- parity: 0 (covers bits 4,5,6,7)
6. bit 5 - message: 0
7. bit 6 - message: 0
8. bit 7 - message: 1
9. bit 8 - message: 1

Thus, the Hamming code for the message `11000011` is:
`111000010011`

#### TL/DR
Hamming codes are a type of error-correcting code used in digital communication to detect and correct errors in data transmission. They were developed by Richard Hamming in the 1950s. Hamming codes add extra bits, known as parity bits, to a message to allow errors to be detected and corrected.

There are several types of Hamming codes, but the most common is the (7,4) code, which adds three parity bits to a four-bit message. The resulting seven-bit code can detect and correct single-bit errors, as well as detect some double-bit errors.

Hamming codes are widely used in computer memory systems, as well as in communication systems such as satellite transmissions, digital television, and voice over IP (VoIP) applications.
### - Turbo Codes
[What are turbo codes?](https://imtech.imt.fr/en/2016/09/16/what-are-turbo-codes/)
#### TL/DR
Turbo codes are a type of error-correcting code used to improve the reliability of data transmission over noisy communication channels. They were invented in the 1990s and are based on the use of parallel concatenated convolutional codes.  
  
Convolutional codes are a type of error-correcting code used in digital communication systems to detect and correct transmission errors. They work by processing a stream of input data through a shift register, which performs a convolution operation on the data using a set of predefined coefficients. The resulting output is then transmitted along with the input data. At the receiver, the transmitted data is processed through a similar shift register, and the resulting output is compared with the received data to detect and correct errors.

Turbo codes offer significant improvements in error correction compared to traditional codes and have been used in a wide range of applications, including satellite and mobile communications, digital television, and optical storage. The decoding process of turbo codes involves the use of an iterative algorithm that improves the accuracy of the correction with each iteration, making them highly effective at correcting errors in noisy communication channels.
### - Error korrigering i kvantdatorer.
[Quantum error correction: Shor code in QISKIT](https://quantumcomputinguk.org/tutorials/quantum-error-correction-shor-code-in-qiskit)
#### TL/DR
Shor codes are a type of quantum error-correcting code that can detect and correct errors in quantum data. They were invented by mathematician Peter Shor in 1995. Shor codes work by encoding a quantum state into a larger number of qubits, which allows errors in the state to be detected and corrected through a process called syndrome measurement. Shor codes are important for quantum computing because quantum information is fragile and can be easily corrupted by environmental noise. With the help of error-correcting codes like Shor codes, quantum computers can perform complex computations with greater accuracy and reliability.


### - Uppgift
Implementering av Hamming Codes:
1. Implementera Hamming code algoritmen för det givna meddelandet.
2. Demonstrera hur man kan detektera och korrigera fel med hjälp av Hamming codes.
3. Jämför det korrigerade meddelandet med orginalet.
```
message = 10101011
```
Lägger er kod i mappen "error_correction", filen ska ha samma namn som algoritmen ni implementerat. Kommentera koden och förklara stegvis med egna ord hur algoritmen fungerar. Skriv även en kort analys i er README över algoritmens styrkor och svagheter.

## Del 4 - Blandad träning (CTF)
* [CTFLearn](https://ctflearn.com/dashboard)
  * Hemsida med flertal övningar inom cybersäkerhet.
### Uppgift
Välj minst 3 uppifter från sidan, gärna inom olika fält, att lösa. Lägg era lösningar i mappen "ctf" och kommentera er lösning så att den är lätt att följa. Skriv en kort text i README:n där ni förklarar uppgiften, er tankeprocess och lösning. Lägg också till en länk till uppgiften.

Några förslag på enklare utmaningar:
* [Cryptography - RSA Noob](https://ctflearn.com/challenge/120)
* [Cryptography - Character Encoding](https://ctflearn.com/challenge/115)
* [Forensics - Forensics 101](https://ctflearn.com/challenge/96)
* [Programming - Simple Programming](https://ctflearn.com/challenge/174)
* [Web - Basic Injection](https://ctflearn.com/challenge/88)
  * Deras guide till SQL Injections: [SQL Injection Part 1](https://ctflearn.com/lab/sql-injection-part-1)
* [Reverse Engineering - Reykjavik](https://ctflearn.com/challenge/990)
* [Miscellaneous - QR Code](https://ctflearn.com/challenge/228)

*P.S. Jag tycker personligen att Cryptography uppgifterna är enklast att lista ut, även på lite svårare nivåer.*

---

# Bonus/Extras
Här under finns lite saker ni kan utforska ifall ni har tid och lust.
### Kali Linux
[Kali Linux](https://www.kali.org/) är en Linux-distribution som är speciellt utvecklad för penetration testing och säkerhetsverktyg. Den innehåller ett brett utbud av verktyg för sådant som penetrationstest, sårbarhetsskanning, avlyssning, webbsäkerhet och mycket mer.

Kali Linux är baserad på Debian-operativsystemet och kan köras på flera olika plattformar, inklusive PC, Mac och Android-enheter. Det finns också stöd för virtualisering, så det kan köras som en virtuell maskin.

---
# Resurser
## Vanliga hot och säkerhetsbrister
### - Backdoor -
En *backdoor* är en säkerhetsbrist i ett system (ex. datorprogram, dator) som gör det möjligt för en utomstående att få obehörig åtkomst till systemet. Backdoors kan vara avsedda från början, till exempel för fjärrstyrning, eller införas av attackerare efter ett intrång i systemet. De kan användas för att få tillgång till konfidentiell information, utföra handlingar som skadar systemet eller användas som en startpunkt för att komma åt andra kopplade system.

### - Denial-of-service attack -
En *Denial-of-service (DoS) attack* är en typ av cyberattack som syftar till att göra en tjänst eller en resurs otillgänglig för de som ska använda den. Attacken kan utföras på olika sätt, men vanligtvis involverar det att attackeraren skickar en massa förfrågningar till en server eller en tjänst, vilket överbelastar den och gör den otillgänglig för legitima användare. En annan typ av DoS-attack är Distributed Denial-of-service (DDoS) där attackeraren använder en armé av komprometterade enheter (ofta kallade "botnät") för att skicka förfrågningar till målet, vilket gör det svårt att skydda sig mot attacken. DDoS-attackerna är svåra att blockera och kan orsaka allvarliga skador på tillgängligheten och tillförlitligheten för de drabbade systemen och tjänsterna.

### - Direct-access attacks -
*Direct-access attacks*, även kallade "tillgångsangrepp", är en typ av cyberattack som syftar till att få obehörig åtkomst till en dator eller ett nätverk. Dessa attacker riktar sig direkt mot sårbarheter i systemet och försöker utnyttja dem för att få åtkomst till känslig information eller utföra handlingar som skadar systemet. Direct-access attacks kan utföras på många olika sätt, inklusive genom att gissa lösenord, utnyttja sårbarheter i programvaran eller använda social engineering-tekniker för att få användare att avslöja sina inloggningsuppgifter.  
  
En vanlig typ av Direct-access attack är Remote Code Execution (RCE) där attackeraren kan utföra kod på ett målsystem via en sårbarhet i ett program eller en tjänst.

### - Eavesdropping -
*Eavesdropping* innebär att en attacker lyssnar på kommunikation mellan enheter eller system utan att vara en del av den. Det kan ske genom att använda tekniker som packet sniffing eller man-in-the-middle-attacker för att fånga och avlyssna trafik.
#### Packet sniffing
Packet sniffing är en teknik där en attacker använder sig av verktyg för att analysera och avlyssna trafik på ett nätverk.
#### Man-in-the-middle-attack
Man-in-the-middle-attack innebär att en attacker placerar sig mellan två enheter och kan läsa, ändra eller blockera trafik mellan dem utan att någon av enheterna är medveten om det.

### - Multi-vector, polymorphic attacks -
*Multi-vector, polymorphic attacks* är en typ av cyberattack som använder flera olika metoder för att tränga in i ett system eller en tjänst. Dessa attacker kan använda en kombination av olika angreppssätt, såsom social engineering, utnyttjande av sårbarheter i programvaran eller direkt-access angrepp, för att få åtkomst.  
  
Polymorphic attacks är särskilt svåra att skydda mot eftersom de ofta ändrar sig eller anpassar sig för att undvika detektion av säkerhetssystem. De kan använda olika tekniker som kryptering, mutering eller kamoufleringsmetoder för att dölja sig.

### - Phishing -
*Phishing* är en typ av social engineering-attack som syftar till att få användare att avslöja känslig information, som till exempel lösenord eller bankkontouppgifter, genom att lura dem till att tro att de kommunicerar med en pålitlig källa.

### - Privilege escalation -
*Privilege escalation* innebär att en användare eller program får ökade privilegier på en dator eller ett nätverk, oftast genom att utnyttja sårbarheter i systemet eller genom att använda en befintlig autentiseringsuppgift. Det kan leda till att en attacker får tillgång till känslig information eller möjlighet att utföra åtgärder som normalt kräver högre privilegier.

### - Reverse engineering -
*Reverse engineering* syftar på processen att analysera och förstå hur en datorprogramvara, en elektronisk enhet eller en algoritm fungerar genom att studera dess källkod eller binary-kod. Det kan användas för att identifiera sårbarheter i systemet, för att förstå hur en angripare kan ha komprometterat en enhet eller för att skapa patcher eller kontra-angrepp mot angripare. Reverse engineering kan också användas för att skapa kopia av program.

### - Side-channel attack -
En *side-channel attack* inom cybersäkerhet är en typ av angrepp som utnyttjar information som läcks ut från en säkerhetskänslig enhet eller system, såsom information som läcks ut via strömförbrukning, ljud, elektromagnetiska vågor eller tidtagning. Dessa attacker utnyttjar information som inte är tänkt att vara tillgänglig för en angripare, men som kan användas för att få insikt i systemet eller för att bryta säkerheten. Exempel på detta kan vara att använda information om strömförbrukningen för att gissa en krypterad nyckel eller att använda tidtagningen för att avslöja information om en krypterad session.

### - Social engineering -
Social engineering inom cybersäkerhet är en metod för att manipulera människor till att avslöja känslig information eller utföra handlingar som skadar säkerheten.  
  
Det kan ske genom olika tekniker såsom phishing-meddelanden, falska samtal eller försök att skapa förtroende genom att utge sig för att vara en person man inte är. Social engineering kan också ske i person genom att prata med människor och få dem att ge bort information eller genom att utnyttja mänskliga instinkter såsom nyfikenhet eller godtrohet.  
  
Målet med social engineering är ofta att få tillgång till känslig information såsom lösenord eller kreditkortsnummer eller få människor att utföra handlingar som skadar säkerheten såsom att öppna en skadlig bilaga eller besöka en skadlig webbplats.

### - Spoofing -
*Spoofing* innebär att en attacker förfalskar sin identitet eller källa för att dölja sin verkliga identitet och få tillgång till en enhet eller ett system. Det finns olika typer av spoofing såsom IP-spoofing, MAC-spoofing, DNS-spoofing och ARP-spoofing.
#### IP-spoofing/MAC-spoofing
IP-spoofing/MAC-spoofing innebär att en attacker förfalskar sin IP-adress för att dölja sin verkliga position/identitet och få tillgång till en enhet eller ett system/nätverk.
#### DNS-spoofing
DNS-spoofing innebär att en attacker förfalskar DNS-svar för att omdirigera användare till en skadlig webbplats.
#### ARP-spoofing
ARP-spoofing innebär att attacker förfalskar ARP-meddelanden för att associera sin egen IP-adress med en annan enhets MAC-adress i ett nätverk.

### - Tampering -
*Tampering* innebär att en attacker ändrar eller manipulerar data för att skada ett system eller för att få tillgång till känslig information. Det kan ske genom att ändra data på en hårddisk eller i en databas, genom att ändra konfigurationsinställningar eller genom att ändra källkoden för ett program. Tampering kan också ske genom att införa skadlig kod i ett system för att skapa en bakdörr eller för att stjäla information.  
  
Ett exempel på detta kan vara en attacker som ändrar ett inloggningsformulär på en webbsida för att samla in användarnas lösenord.

### - Malware -
*Malware* är en förkortning av "malicious software" (skadlig programvara) och innebär all form av programvara som är skapad med syfte att skada ett system eller stjäla information. Malware kan sprida sig på olika sätt, som via e-post, skadliga webbplatser, eller sårbara programvaror. Målet med malware är ofta att skada systemet eller stjäla information, eller tjäna pengar genom att visa annonser eller kräva lösensumma.  
  
Det finns olika typer av malware, inklusive: Virus, trojaner, rootkits, ransomware och adware.
#### Virus
En typ av malware som sprider sig från fil till fil genom att infoga sig i existerande program och filer.
#### Trojaner
En typ av malware som döljer sig bakom legitima program och öppnar en bakdörr för attacker att få tillgång till systemet.
#### Rootkits
En typ av malware som gömmer sig i systemet och gör det svårt att upptäcka och ta bort.
#### Ransomware
En typ av malware som krypterar användarnas data och kräver en lösensumma för att låsa upp den.
#### Adware
En typ av malware som visar annonser och oönskade pop-ups på användarnas enheter.


## Extra material
* [IT-Säkerhet (Wikipedia)](https://sv.wikipedia.org/wiki/IT-s%C3%A4kerhet)
* [Datasäkerhet (Wikipedia)](https://sv.wikipedia.org/wiki/Datas%C3%A4kerhet)
  * Underkategori av IT-Säkerhet
* [Computer Security (Wikipedia)](https://en.wikipedia.org/wiki/Computer_security)
  * Innehåller mer information än den svenska.
* [CTFLearn](https://ctflearn.com/dashboard)
  * Hemsida med flertal övningar inom cybersäkerhet.
### Verktyg
* [CyberChef](https://gchq.github.io/CyberChef/)

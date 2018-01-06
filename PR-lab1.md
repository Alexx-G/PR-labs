## TCP

Elaborarea unei aplicații Client - Server cu scopul studierii
protocolului de la nivelul de transport - TCP.

### Prerequisites

- VCS (Version Control System) Git - vezi [info din procesul de susținere](submission-process.md);
- Limbajul de programare: nu este restricționat. Însă să recomandă un limbaj dinamic cu REPL*.
- Cunoștințe despre: modelul OSI, IP

Note:
- Informație despre git și linkuri utile găsești în [procesul de sustinere](submission-process.md);

### Obiective

- Studierea nivelului de transport în rețea și TCP/IP;
- Studierea BSD sockets API;
- Elaborarea unei aplicații client-server.

### Sarcina de bază (5 - 7)

Primul pas logic este să studiați interfața oferită de limbaj 
pentru lucru cu BSD sockets. # TODO: Add references

Scopul este să implementați o aplicație [client-server](), deci 
următorul pas este stabilirea protocolului de comunicare între 
client și server.

Pentru a ușura acest proces, se stabilește următorul format al mesajelor:
- Comenzile de la client încep cu `/`
- Comanda poate contine `A-Za-z0-9_`
  De exemplu: `/help`
- Daca comanda accepta parametri, atunci dupa comanda urmeaza spatiu si restul datelor.
  Exemplu: `/helo John`
- Dacă serverul primește o comandă invalidă - se răspunde cu un mesaj informativ.

Aceasta și este prima sarcină - să descrieți protocolul de comunicare între client și server.
Acest document trebuie păstrat în repozitoriu și inclus în raport.
Documentul trebuie să conțină:
- Formatul mesajelor
- Comenzile suportate de server
- Exemple de răspuns la fiecare comandă

**Comenzile obligatorii care trebuie să le implementeze serverul:**
- `/help` - răspunde cu o listă a comenzilor suportate și o descriere a fiecărei comenzi;
- `/helo Text` - raspunde cu textul care a fost expediat ca paremetru<
- + alte 3 comenzi cu funcțional diferit (e.g. timpul curent, generator de cifre, flip the coin etc)

Cerințele de bază pentru aplicație sunt destul de simple:
- O aplicație client care se conectează la server și transmite careva comenzi;
  - Comenzile sunt introduse de utilizator de la tastatură;
  - Răspunsul primit de la server este afișat utilizatorului.
- O aplicație server care:
  - Acceptă conexiunea de la client la un careva port;
  - Primește comenzile de la client;
  - Transmite un răspuns clientului.

**Constrîngeri:**
- Să se utilizeze **doar** interfața BSD sockets oferită de limbaj/platformă.

### Sarcini adiționale (+1 pentru fiecare sarcină)
- ...
- ...
- ...

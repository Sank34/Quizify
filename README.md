# Quizify
*proiect realizat de:*
- Lascu Andrei - clasa a 9-a, Colegiul National "Gheorghe Munteanu Murgoci"
-  Stefania Florentina Radu - clasa a 9-a, Colegiul National "Gheorghe Munteanu Murgoci"

*prof. îndrumător Ciausu Liliana, Paul Prus, Gina Stanciu*

## **Problema**

Fiecare persoana are propriul mod de a invata, insa toata lumea este de acord ca, pentru a intelege concepte, acestea trebuie testate regular. Mai mult, un feedback legat de raspunsuri gresite, curba de invatare si aspecte unde ar trebui sa mai aprofundeze pot fi foarte de ajutor pentru ceilalti, astfel facandu-i sa realizeze cat mai au de invatat, in timp real.

In cazul programarii, care necesita gandire critica si exercitiu constant, feedback-ul este esential. Totusi, multi utilizatori ai aplicatiilor educationale in domeniul programarii se confrunta cu lipsa unui feedback prompt si detaliat. Aplicatiile existente ofera adesea feedback limitat sau intarziat, ceea ce incetineste progresul si reduce eficienta evaluarii si invatarii.

## **Soluția**

Ideea de la care porneste Quizify este integrarea unui modul de feedback automat, personalizat si sistematizat, folosindu-ne de inteligenta artificiala (AI).

Astfel, Quizify utilizeaza tehnologia OpenAI pentru a oferi feedback instant si detaliat asupra codului scris de utilizatori. Acest modul AI analizeaza codul in timp real, identifica erorile, ofera sugestii de corectare si explica conceptele necesare pentru a intelege si remedia problemele intalnite.

## **Publicul țintă**


Publicul tinta este format din:

-   Elevi
    
-   Persoane doritoare sa invete mai multe despre domeniul programarii

**Aplicatia poate fi folosita dupa scoala, pentru elevii care vor sa isi testeze cunostiintele inainte de o testare sau inainte sa inceapa un proiect. De asemenea, poate fi o unealta pentru cei interesati de programare, dar care nu au gasit un mediu de invatare pe placul lor pana acum.**

### ***Opinia și utilitatea personală:***

- Ca **elevi**, aceasta platforma poate ajuta la o intelegere profunda a lacunelor pe care le am in invatare, pentru a nu mai pierde din timp repetand concepte pe care le cunosc deja, astfel concentrandu-ma pe punctele slabe.

- Ca **programator**, daca nu as stii nimic, o platforma din care aflu informatii, iar dupa le testez ar fi un punct de inceput foarte bun, astfel ajutandu-ma in drumul meu in lumea programarii.

## **Arhitectura aplicației**

### ***Funcționalitățile aplicației:***

- **Analiza Codului în Timp Real**: Modulul AI analizează codul utilizatorului pe măsură ce acesta este scris, oferind sugestii de corectare imediat.

- **Feedback Personalizat**: Feedback-ul este adaptat la nivelul de cunoștințe al utilizatorului, oferind explicații detaliate și resurse suplimentare pentru a înțelege conceptele.

- **Sugestii de Îmbunătățire**: Pe lângă corectarea erorilor, AI-ul oferă sugestii pentru optimizarea și îmbunătățirea codului.

- **Exemple Practice**: Modulul AI furnizează exemple practice relevante și soluții alternative pentru problemele întâmpinate.

- **Istoric de Feedback**: Utilizatorii pot accesa un istoric al feedback-ului primit pentru a-și urmări progresul și a revizui conceptele învățate anterior.

**Beneficii:**

- Învățare Rapidă și Eficientă, astfel incat utilizatorii primesc feedback instantaneu, ceea ce accelerează procesul de învățare și corectare a erorilor.
- **Claritate și Înțelegere** Explicațiile detaliate ajută utilizatorii să înțeleagă conceptele și să aplice corecturile în mod conștient.
- **Îmbunătățire Continuă**: Sugestiile de optimizare încurajează utilizatorii să-și îmbunătățească continuu abilitățile de programare.
- **Motivație și Angajament**: Feedback-ul prompt și detaliat menține utilizatorii motivați și implicați în procesul de învățare.

## ***Unelte folosite***

- **React** - este o bibliotecă JavaScript pentru construirea interfețelor de utilizator rapide și eficiente, datorită performanței ridicate oferite de virtual DOM.

- **Appwrite** - este o platformă backend open-source care simplifică gestionarea autentificării, bazelor de date și stocării de fișiere, reducând complexitatea dezvoltării. React Query - este o bibliotecă pentru gestionarea datelor server-side în aplicațiile React, optimizând performanța prin caching, refetching și actualizări în timp real. 

- **TypeScript** - permite scrierea codului intr-un mod eficient, reducând erorile.

- **Shadcn** - este un set de componente UI predefinite și personalizabile, care accelerează dezvoltarea interfețelor utilizator moderne și responsive.

- **Tailwind CSS** - este un framework utilitar care facilitează dezvoltarea rapidă și personalizată a interfețelor, menținând un design consistent și modern.

***Justificarea folosirii React***



Exemplu:

```jsx
// Fișierul App.js
import React from 'react';

function App() {
  return (
    <div>
      <h1>Bun venit la Quizie!</h1>
    </div>
  );
}

export default App;

```

***Justificarea folosirii Typescript***

Exemplu:
```jsx
// Fișierul App.tsx
import React from 'react';

const App: React.FC = () => {
  return (
    <div>
      <h1>Bun venit la Quizie!</h1>
    </div>
  );
};

export default App;
```

***Justificarea folosirii Shadcn***
Exemplu:
```jsx
// Fișierul Button.js
import React from 'react';
import { Button } from 'shadcn';

const CustomButton = () => {
  return <Button color="primary">Click Me</Button>;
};

export default CustomButton;
```

***Justificarea folosirii TailwindCSS***
Exemplu:
```jsx
// Fișierul App.js
import React from 'react';
import 'tailwindcss/tailwind.css';

function App() {
  return (
    <div className="min-h-screen flex items-center justify-center bg-gray-100">
      <h1 className="text-3xl font-bold text-blue-500">Bun venit la Quizie!</h1>
    </div>
  );
}

export default App;
```

***Justificarea folosirii ReactQuery***
Exemplu:
```jsx
// Fișierul DataComponent.js
import React from 'react';
import { useQuery } from 'react-query';

const fetchData = async () => {
  const res = await fetch('https://api.example.com/data');
  return res.json();
};

const DataComponent = () => {
  const { data, error, isLoading } = useQuery('data', fetchData);

  if (isLoading) return <div>Loading...</div>;
  if (error) return <div>Error: {error.message}</div>;

  return <div>Data: {JSON.stringify(data)}</div>;
};

export default DataComponent;
```

***Justificarea folosirii Appwrite***

Un exemplu simplu de cod pentru integrarea Appwrite într-o aplicație React. Acest exemplu demonstreaza cum putem să configuram Appwrite și să creezi un utilizator nou.

### Configurarea Appwrite și Crearea unui Utilizator Nou

1.  **Instalare:** Asigură-te că ai instalat SDK-ul Appwrite pentru JavaScript.

```bash
npm install appwrite` 
```

2.  **Configurare Appwrite:** Creeam un fișier `appwriteConfig.js` pentru a configura Appwrite.

```js

`// Fișierul appwriteConfig.js
import { Client, Account } from 'appwrite';

// Configurare client Appwrite
const client = new Client()
  .setEndpoint('https://[HOSTNAME_OR_IP]/v1') // URL-ul endpoint-ului Appwrite
  .setProject('YOUR_PROJECT_ID'); // ID-ul proiectului tău Appwrite

// Instanța Account pentru gestionarea utilizatorilor
const account = new Account(client);

export { client, account };
```
3.  **Crearea unui Utilizator Nou:** Creează un component React pentru a înregistra un utilizator nou folosind Appwrite.

```jsx

`// Fișierul Register.js
import React, { useState } from 'react';
import { account } from './appwriteConfig';

const Register = () => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');
  const [name, setName] = useState('');

  const handleRegister = async (e) => {
    e.preventDefault();
    try {
      const user = await account.create('unique()', email, password, name);
      console.log('User created successfully:', user);
    } catch (error) {
      console.error('Error creating user:', error);
    }
  };

  return (
    <div className="min-h-screen flex items-center justify-center bg-gray-100">
      <form onSubmit={handleRegister} className="bg-white p-6 rounded shadow-md">
        <h2 className="text-2xl font-bold mb-4">Register</h2>
        <input
          type="text"
          value={name}
          onChange={(e) => setName(e.target.value)}
          placeholder="Name"
          className="mb-2 p-2 border border-gray-300 rounded w-full"
        />
        <input
          type="email"
          value={email}
          onChange={(e) => setEmail(e.target.value)}
          placeholder="Email"
          className="mb-2 p-2 border border-gray-300 rounded w-full"
        />
        <input
          type="password"
          value={password}
          onChange={(e) => setPassword(e.target.value)}
          placeholder="Password"
          className="mb-2 p-2 border border-gray-300 rounded w-full"
        />
        <button type="submit" className="bg-blue-500 text-white p-2 rounded w-full">
          Register
        </button>
      </form>
    </div>
  );
};

export default Register;
```
### Explicație

1.  **Configurare Appwrite (`appwriteConfig.js`):**
    
    -   Se configurează clientul Appwrite cu URL-ul endpoint-ului și ID-ul proiectului.
    -   Se creează o instanță a clasei `Account` pentru gestionarea operațiunilor legate de utilizatori.
2.  **Componenta React pentru Înregistrare (`Register.js`):**
    
    -   Utilizăm `useState` pentru a gestiona starea câmpurilor de input (nume, email, parolă).
    -   Funcția `handleRegister` este apelată la trimiterea formularului și folosește metoda `account.create` pentru a crea un utilizator nou în Appwrite.
    -   Formularul este stilizat folosind Tailwind CSS pentru a fi estetic și ușor de utilizat.

Acest exemplu demonstrează cum să integrezi Appwrite într-o aplicație React și să implementezi funcționalitatea de înregistrare a utilizatorilor.

## **Cum ne comparam fata de solutiile existente?**


Principalii nostri competitori:

-   Google Classroom
    
-   Pbinfo

### ***Cu ce este diferit?***
Fata de competitori, noi oferim analiza completa a codului și feedback in timp real legat de ceea ce poate fi îmbunătățit. Astfel, nu conteaza numai scorul pe care il ai, ci si ce ai facut bine si ce mai este de imbunatatit.

Mai mult, nu sunt oferite in limba romana multe resurse din domeniul web development, astfel fiind un lucru inovativ in Romania, mai ales avand si partea de testare si evaluare a codului.

De asemenea, aplicatia este disponibila in limba romana, dar si in limba engleza!

## **Ghidul de instalare**
Pasii pentru instalare a aplicatiei in sistemul local **(metoda1)**

**Requirements**

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)

**Clonarea Repo-ului**

```bash
git clone https://github.com/Sank34/Quizify.git
cd /path/...
```

**Instalare**

Instalarea dependentelor utilizand npm:

```bash
npm install
```

**Rularea proiectului**

```bash
npm run dev
```

Acum putem deschide [http://localhost:5173](http://localhost:5173) in browser pentru a vedea proiectul.

## **Testimoniale**
*In curand*...


<div style="page-break-after: always;"></div>

## **Imagini aplicatie**
*In curand*...

## **Statistici elevi**
*In curand*...
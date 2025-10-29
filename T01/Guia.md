# 📘 Guia d’Ús Tècnica: Bitwarden per a l’Equip Tècnic

Aquesta guia descriu els passos essencials per instal·lar, configurar i utilitzar **Bitwarden** com a gestor de contrasenyes dins d’un entorn tècnic. Inclou instruccions pas a pas i recomanacions de seguretat.

---

## 🔧 1. Instal·lació i Configuració Inicial

### 1.1 Descàrrega i instal·lació

Accedeix a [bitwarden.com/download](https://bitwarden.com/download) perer al teu sistema operatiu o navegador.

Opcions disponibles:

- Aplicació d’escriptori (Windows, macOS, Linux)  
- Aplicació mòbil (Android, iOS)  
- Extensió de navegador (Chrome, Firefox, Edge)  
- Aplicació web (en línia)

📷 <img width="274" height="271" alt="image" src="https://github.com/user-attachments/assets/11c884c7-3d96-4c74-88e3-457e399eec2f" />


---

### 1.2 Creació del compte mestre

Un cop instal·lada l’eina, cal crear un compte mestre:

- Fes clic a “Crear compte”
- Introdueix el correu electrònic, nom d’usuari, contrasenya mestra segura i una pista de recordatori

📷 <img width="281" height="277" alt="image" src="https://github.com/user-attachments/assets/827a7900-5819-45b6-9159-9280965ba0c5" />


---

## 🔐 2. Generació de Contrasenyes Segures

Bitwarden inclou un generador integrat que permet crear contrasenyes robustes.

### 2.1 Accés al generador

- A l’aplicació o extensió, fes clic a “Generador de contrasenyes”

📷 <img width="605" height="298" alt="image" src="https://github.com/user-attachments/assets/2e45c21b-9487-40b6-b945-eb788b40e1e8" />


---

### 2.2 Paràmetres configurables

- Longitud recomanada: mínim 16 caràcters  
- Opcions disponibles: majúscules, minúscules, números i caràcters especials  
- Opcional: generació de frases de pas (passphrases)

📷 <img width="472" height="313" alt="image" src="https://github.com/user-attachments/assets/98da45f4-3256-4bf7-bb83-9df7e09a21c8" />


---

## 🧪 3. Exemples d’Ús i Emplenament Automàtic

### 3.1 Desar una credencial de correu electrònic

- Crea un nou element → Tipus: Login  
- Nom: “Compte Gmail”  
- URL: https://mail.google.com  
- Introdueix l’usuari i la contrasenya corresponents

📷 <img width="573" height="757" alt="image" src="https://github.com/user-attachments/assets/f1bb4854-7ea6-4fae-8648-533fa52f478f" />


---

### 3.2 Desar una credencial d’aplicació o servei web

- Repeteix el procés anterior, modificant el nom i la URL segons el servei (p. ex. GitHub, Moodle)

📷 <img width="372" height="588" alt="image" src="https://github.com/user-attachments/assets/0d6c8a1f-e2d1-45cd-b3f3-53f3609f05e2" />


---

### 3.3 Emplenament automàtic amb l’extensió

- Instal·la l’extensió del navegador  
- Inicia sessió al teu compte Bitwarden  
- Accedeix a un lloc web amb credencials guardades  
- Bitwarden oferirà l’opció d’emplenar automàticament els camps

📷 <img width="1340" height="761" alt="image" src="https://github.com/user-attachments/assets/b8ea6618-985a-40e1-bdca-8df4ffd1e90d" />

---

## 💾 4. Gestió de Còpies de Seguretat (Backup)

### 4.1 Exportació de la base de dades

- A l’aplicació web: Configuració → Eines → Exportar Vault  
- Format recomanat: `.json` (xifrat si es desitja)

📷 <img width="941" height="428" alt="image" src="https://github.com/user-attachments/assets/99fd4203-f33f-422b-bf7b-25a3de2ff6ec" />


---

### 4.2 Recomanacions de seguretat
- No deixis l’arxiu exportat sense xifrar  
- Desa’l en ubicacions segures, com ara:
  - Una clau USB xifrada
  - Un servei d’emmagatzematge al núvol amb xifrat (p. ex. Tresorit, Proton Drive)
  - Alternativament, utilitza eines com VeraCrypt per xifrar manualment

📷 <img width="794" height="484" alt="image" src="https://github.com/user-attachments/assets/d1c98540-535b-4c7b-ab14-26239cb5eefa" />


---

## ✅ Conclusions

Bitwarden és una eina segura, transparent i fàcil d’utilitzar per a la gestió de contrasenyes. Aquesta guia proporciona una base sòlida perquè l’equip tècnic la pugui implementar correctament i protegir les credencials de manera eficaç.

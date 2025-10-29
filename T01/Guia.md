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

📷 *img/instal·lacio.png*

---

### 1.2 Creació del compte mestre

Un cop instal·lada l’eina, cal crear un compte mestre:

- Fes clic a “Crear compte”
- Introdueix el correu electrònic, nom d’usuari, contrasenya mestra segura i una pista de recordatori

📷 *img/instal·lacio.png*

---

## 🔐 2. Generació de Contrasenyes Segures

Bitwarden inclou un generador integrat que permet crear contrasenyes robustes.

### 2.1 Accés al generador

- A l’aplicació o extensió, fes clic a “Generador de contrasenyes”

📷 *img/generador.png*

---

### 2.2 Paràmetres configurables

- Longitud recomanada: mínim 16 caràcters  
- Opcions disponibles: majúscules, minúscules, números i caràcters especials  
- Opcional: generació de frases de pas (passphrases)

📷 *img/generador.png*

---

## 🧪 3. Exemples d’Ús i Emplenament Automàtic

### 3.1 Desar una credencial de correu electrònic

- Crea un nou element → Tipus: Login  
- Nom: “Compte Gmail”  
- URL: https://mail.google.com  
- Introdueix l’usuari i la contrasenya corresponents

📷 *img/exemple_email.png*

---

### 3.2 Desar una credencial d’aplicació o servei web

- Repeteix el procés anterior, modificant el nom i la URL segons el servei (p. ex. GitHub, Moodle)

📷 *img/exemple_web.png*

---

### 3.3 Emplenament automàtic amb l’extensió

- Instal·la l’extensió del navegador  
- Inicia sessió al teu compte Bitwarden  
- Accedeix a un lloc web amb credencials guardades  
- Bitwarden oferirà l’opció d’emplenar automàticament els camps

📷 *img/extensio_navegador.png*

---

## 💾 4. Gestió de Còpies de Seguretat (Backup)

### 4.1 Exportació de la base de dades

- A l’aplicació web: Configuració → Eines → Exportar Vault  
- Format recomanat: `.json` (xifrat si es desitja)

📷 *img/backup.png*

---

### 4.2 Recomanacions de seguretat
- No deixis l’arxiu exportat sense xifrar  
- Desa’l en ubicacions segures, com ara:
  - Una clau USB xifrada
  - Un servei d’emmagatzematge al núvol amb xifrat (p. ex. Tresorit, Proton Drive)
  - Alternativament, utilitza eines com VeraCrypt per xifrar manualment

📷 *img/backup.png*

---

## ✅ Conclusions

Bitwarden és una eina segura, transparent i fàcil d’utilitzar per a la gestió de contrasenyes. Aquesta guia proporciona una base sòlida perquè l’equip tècnic la pugui implementar correctament i protegir les credencials de manera eficaç.

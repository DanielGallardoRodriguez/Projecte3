# Tasques d'Implementació i Configuració del Servidor LDAP

La **Consultora EverPia** ha de complir estrictament amb les següents tasques d'instal·lació i configuració:

---

## 1. Instal·lació i Configuració Base d'OpenLDAP

### Instal·lació del servei OpenLDAP
Per instal·lar el servei LDAP i les eines necessàries, executem:

Fem la instal·lació:

<img width="771" height="553" alt="Captura de pantalla 2025-10-21 160837" src="https://github.com/user-attachments/assets/1bd0aa49-1e1c-4d1b-a53a-b73f744da4c1" />
<img width="638" height="670" alt="Captura de pantalla 2025-10-21 161044" src="https://github.com/user-attachments/assets/e816daf2-e915-46ef-bf4b-6f0882c013b8" />

<img width="719" height="398" alt="Captura de pantalla 2025-10-21 161118" src="https://github.com/user-attachments/assets/bc6f4a70-13cc-48c7-bc7c-8ee6bfd2cbfc" />
<img width="659" height="329" alt="Captura de pantalla 2025-10-28 165317" src="https://github.com/user-attachments/assets/38e95677-082f-4f0e-9f6f-30505a80db9b" />


Comanda per instalar ldap:
sudo apt install slapd ldap-utils -y



Despres de introduir la comanda fiquem la contraseña p@ssw0rd i com a nom de l'organització inovatechXX.test, per exemple, en el meu cas es innovatech06.test

Verificacio de la instalacio base:
sudo slapcat
<img width="461" height="264" alt="Captura de pantalla 2025-10-22 183124" src="https://github.com/user-attachments/assets/214fa022-5423-4025-9418-e8633223a6e6" />

systemctl status slapd
<img width="822" height="227" alt="image" src="https://github.com/user-attachments/assets/fc34eea7-bdd0-4033-aea4-de972602a7ab" />


Configuració de la base de dades. Nom del Domini: innovatech06.test
<img width="743" height="246" alt="Captura de pantalla 2025-10-21 165524" src="https://github.com/user-attachments/assets/7aeb4d21-8cab-4ef4-954e-06027b06bf40" />


Configuració de la contrasenya d'administrador. Contrasenya: p@ssw0rd
<img width="775" height="188" alt="Captura de pantalla 2025-10-21 165530" src="https://github.com/user-attachments/assets/b722f7ca-deae-4701-8c09-03cbf276a441" />
<img width="767" height="203" alt="Captura de pantalla 2025-10-21 165845" src="https://github.com/user-attachments/assets/dc7907e2-b270-4dd7-91fd-b76ff380a095" />

En cas de equivocacio utilitzarem la seguent comanda:

sudo dpkg-reconfigure slapd
Diem que no volem cancel·lar la configuracio de la BDD, atès que és el que volem fer.

Posem el nom corresponent al directori que volem crear.

 

Introduim el nom de l'organització que a de ser innovatechXX.test.



Contrasenya de l'adrministrador que ha de ser p@ssw0rd



I acceptem les dos seguents opcions de configuració

Creació d'Unitats Organitzatives inicials. S'han de crear dues OUs: users i groups mitjançant un fitxer .ldif.

Creem els fitxers:
<img width="655" height="113" alt="Captura de pantalla 2025-10-28 153258" src="https://github.com/user-attachments/assets/572496b4-5c9d-4feb-a65f-075298dc7e84" />

<img width="570" height="199" alt="Captura de pantalla 2025-10-28 163024" src="https://github.com/user-attachments/assets/b1440bc6-5b4c-43cb-8c57-543a3a27fd52" />

Els afegim:

<img width="659" height="329" alt="Captura de pantalla 2025-10-28 165317" src="https://github.com/user-attachments/assets/c76e2eb2-ca5f-4272-b77a-3010387e5e15" />


Validació de les Unitats Organitzatives.

Consultem:


<img width="943" height="833" alt="Captura de pantalla 2025-10-28 160614" src="https://github.com/user-attachments/assets/b8a58ea2-41a7-424f-9ce1-77bda3f402aa" />


Gestió i Administració
Instal·lació del Gestor d'Usuaris LDAP (LAM). S'ha de documentar la comanda d'instal·lació.

<img width="576" height="31" alt="Captura de pantalla 2025-10-28 165436" src="https://github.com/user-attachments/assets/51173082-21f6-4d42-9b01-28695d04f143" />
Accés Remot i Configuració. Connectar a LAM des de la màquina física utilitzant l'adreça IP de la interfície Host-Only.

Ip que hem de utilitzar:

<img width="818" height="374" alt="image" src="https://github.com/user-attachments/assets/d2705b8d-3051-4da0-adad-cd244ddb7538" />



Anem a un navegador i introduim la ip seguidament de /lam, un cop dins anem a LAM configurations, despres a Edit server profiles e introduim la contrasenya lam per poder entrar:


<img width="409" height="229" alt="Captura de pantalla 2025-10-28 165713" src="https://github.com/user-attachments/assets/8aeb2bb4-9b44-4fb2-9c18-4def02a7ebe9" />

Configuració per defecte. Establir la configuració predeterminada perquè els nous usuaris s'ubiquin a l'OU users i els nous grups a l'OU groups.

Primer canviem el idioma i regio:

<img width="800" height="440" alt="Captura de pantalla 2025-10-28 165807" src="https://github.com/user-attachments/assets/9f867f3b-cfff-4cf6-bfe0-02b75ecfc00b" />


Ara anem al tool settings e fiquem el nostre domini i extensio:

<img width="811" height="510" alt="Captura de pantalla 2025-10-28 165914" src="https://github.com/user-attachments/assets/df9c8895-5697-4984-9ee4-3a6b744bf4ee" />


I ara nomes queda guardar la configuracio i tornar a la pantalla de login e iniciar sessio amb l'usuari admin i contrasenya p@ssw0rd
Creació de Grups. Crear dos grups de seguretat al directori: tech i manager.

Per crear els grups es sencill, simplement anirem a Nuevo grupo, fiquem el nom necesari tech o manager i creem el grup.

<img width="1863" height="315" alt="Captura de pantalla 2025-10-29 172727" src="https://github.com/user-attachments/assets/1baa1b05-a4b4-4610-ba55-ea0ae0dac842" />


Creació d'Usuaris de Prova. Crear un usuari per a cada grup: tech01 (membre de tech) i manager01 (membre de manager).

Introduim els noms corresponents (tech01 o manager01), anem a l'apartat de Unix i seleccionem Crear grupo con mismo nombre:

<img width="1891" height="353" alt="Captura de pantalla 2025-10-29 180033" src="https://github.com/user-attachments/assets/776a90b0-1dc0-4f3c-a52e-1b89707d9a8e" />



Un cop creat entrem a Editar grupos e introduim en Grupos seleccionados el grup corresponent en aquest cas el grup sera el manager:

<img width="667" height="276" alt="Captura de pantalla 2025-10-29 180337" src="https://github.com/user-attachments/assets/a3f5a94b-222b-4b95-a980-1d89818741c3" />

Si volem comprovar si s'ha configurat correctament anem als grups i entrem a l'opcio de Editar miembros



I repetim el mateix proces amb l'usuari tech01.

Integració de Client (Client Ubuntu Desktop)

Configurem el client que ho hem fet el linux v17 ja que no tenim el ubuntu desktop i l'hem configurat de tal manera per poder accedir als usuaris que hem creat desde la WEB.

<img width="1255" height="465" alt="Captura de pantalla 2025-11-11 164935" src="https://github.com/user-attachments/assets/ec401348-554b-4eb9-8ddf-5c3da6e57a1e" />

<img width="627" height="393" alt="Captura de pantalla 2025-11-11 165513" src="https://github.com/user-attachments/assets/efa30b34-f09a-440c-86d9-f30b7758034c" />


Despres d'haver fet tots els passos mencionats podrem accedir desde el client als usuaris que hem creat desde la web.
<img width="537" height="356" alt="image" src="https://github.com/user-attachments/assets/2fa88e87-dc37-49c7-a993-bc6407ace74d" />

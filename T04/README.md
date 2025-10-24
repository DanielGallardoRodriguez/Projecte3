# Tasca 04 – Serveis de Directori amb OpenLDAP

## Context

La start-up tecnològica **Innovatech** està experimentant un creixement accelerat, però pateix greus problemes en la gestió d’usuaris i accessos. Cada servei intern utilitza la seva pròpia base de dades d’usuaris, i els equips clients funcionen amb autenticació local, fet que genera:

- **Ineficiència operativa**: gestió manual de comptes en múltiples sistemes.
- **Risc de seguretat**: reutilització de contrasenyes entre serveis.
- **Manca d’escalabilitat**: dificultat per integrar nous serveis.

Per resoldre aquesta situació, EverPia ha proposat implementar una solució d’autenticació centralitzada basada en **OpenLDAP**, una tecnologia robusta i de codi obert compatible amb els sistemes GNU/Linux que utilitza Innovatech.

## Objectiu de la tasca

Implementar un servidor **OpenLDAP** en Linux que permeti:

- Instal·lar i configurar el servei LDAP.
- Definir el domini base i la jerarquia d’unitats organitzatives.
- Crear usuaris i grups dins del directori.
- Configurar un equip client per autenticar-se mitjançant el directori.

## Estructura del lliurament
Dins la carpeta `tasca04` s’han d’incloure els següents arxius:

- `README.md` → Descripció general de la tasca (aquest document).
- `ldap_implementacio.md` → Documentació tècnica de la implementació del servidor LDAP.
- Carpeta `img/` → Imatges utilitzades en la documentació.

## Requisits tècnics

- **Instal·lació del servei**: Paquets necessaris i configuració inicial.
- **Configuració del domini base**: Definició de l’estructura DN.
- **Creació de la jerarquia**: Unitats organitzatives (OU), usuaris i grups.
- **Integració client**: Configuració d’un equip Linux per autenticar-se via LDAP.

## Recursos de suport

- UD04.AA1 Serveis de Directori (Moodle)
- UD04.AA2 Instal·lació OpenLDAP (Moodle)
- UD04.AA3 Configuració del directori (Moodle)
- UD04.AA5 Agregar client al directori (Moodle)

---

> **Tasca individual** – Cal demostrar capacitat d’implementació i documentació tècnica clara.  
> **Projecte crític** – La solució proposada serà presentada al client com a part del servei d’EverPia.


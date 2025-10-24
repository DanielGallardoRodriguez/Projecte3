# Tasca 07 – Instal·lació d’un servidor de noms (DNS intern)

## Context

Després de la formació rebuda, el client **DigiCore** ha confiat en EverPia per implantar un **sistema DNS intern** que permeti accedir als seus serveis mitjançant noms de domini amigables, en lloc d’adreces IP.

Els problemes actuals inclouen:

- **Usabilitat deficient**: ús d’IPs difícils de recordar.
- **Manteniment feixuc**: canvis d’IP requereixen actualitzacions manuals.
- **Manca de professionalitat**: absència de noms de domini personalitzats.

## Objectiu de la tasca

Implementar un servidor DNS **primari (màster)** amb **BIND9** en un sistema Linux, configurant:

- Una **zona directa** per al domini `digicore-XX.test`.
- Una **zona inversa** per a la xarxa local.
- **Transferència de zona** a un servidor secundari.
- **Consultes recursives** amb reenviador a 8.8.8.8.

## Estructura del lliurament

Dins la carpeta `tasca07` s’han d’incloure els següents arxius:

- `README.md` → Descripció general de la tasca (aquest document).
- `dns_configuracio.md` → Documentació tècnica amb captures i explicacions.
- Carpeta `zones/` → Arxius de configuració de les zones DNS.
- Carpeta `img/` → Captures de pantalla de la configuració i comprovacions.

## Requisits tècnics

### Preparació del servidor

- Ubuntu Server amb 4 GB de RAM i 20 GB de disc.
- Interfície en **adaptador pont** i **host-only**.
- Instal·lació de **BIND9** i **SSH**.

### Configuració del servidor DNS

1. **named.conf.options**:
   - Activar consultes recursives des de la xarxa local.
   - Configurar reenviador: `8.8.8.8`.

2. **named.conf.local**:
   - Definir zona directa per `digicore-XX.test`.
   - Definir zona inversa per la xarxa local.

3. **Zona directa** (`db.digicore-XX.test`):
   - Registres: SOA, NS, A (server, dbserver), CNAME (data).

4. **Zona inversa** (`db.XXX.rev`):
   - Registres: SOA, NS, PTR (server, dbserver).

5. **Transferència de zona**:
   - Permetre transferència a companys.
   - Configurar zona secundària i forçar sincronització.

### Verificació

- Consultes `dig` i `nslookup` des del client Zorin.
- Proves de resolució directa i inversa.
- Confirmació de transferència de zona.

## Activitat d’avaluació

- Prova pràctica final amb ús exclusiu d’un **full manuscrit** com a material de suport.
- Cal demostrar competència tècnica i comprensió del servei DNS.

---

> **Tasca individual** – Cal documentar amb rigor tècnic i claredat.  
> **Projecte real** – La configuració serà la base del sistema DNS intern de DigiCore.

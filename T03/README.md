# Tasca 03 – Gestió flexible de discos (LVM i Espais d’emmagatzematge)

## Context

El bufet d’advocats **Garriga i Associats**, reconegut per la gestió de gran quantitat d’informació legal sensible, ha contractat EverPia per renovar els seus sistemes d’emmagatzematge. Els requisits del client són clars: **alta disponibilitat**, **redundància** i **escalabilitat**, amb capacitat d’ampliació sense interrupcions.

Com a tècnics d’EverPia, se us ha encarregat dissenyar i documentar dues solucions d’emmagatzematge, una per entorns **Linux** i una altra per **Windows**, que compleixin amb aquests requisits. El treball es realitzarà mitjançant màquines virtuals per facilitar la demostració.

## Objectiu de la tasca

- Dissenyar i documentar una solució amb **LVM** en Linux (Zorin OS).
- Dissenyar i documentar una solució amb **Espais d’emmagatzematge** en Windows 11.
- Demostrar la configuració, gestió i escalabilitat de cada sistema.
- Preparar la documentació tècnica per presentar al client.

## Estructura del lliurament

Dins la carpeta `tasca03` s’han d’incloure els següents arxius:

- `README.md` → Descripció general de la tasca (aquest document).
- `linux_lvm.md` → Documentació de la solució amb LVM en Zorin OS.
- `windows_storage.md` → Documentació de la solució amb Espais d’emmagatzematge en Windows.
- Carpeta `img/` → Imatges utilitzades en les dues documentacions.

## Requisits tècnics

### Part Linux – LVM amb Zorin OS

- **Configuració inicial**: Crear VG i LV amb dos discos de 10 GB. Muntar automàticament via `/etc/fstab`.
- **Alta disponibilitat**: Implementar mirall (lvm_mirror).
- **Instantànies**: Crear LV, afegir dades, generar snapshot i demostrar restauració.
- **Escalabilitat**: Ampliar volum utilitzant espai lliure del VG.

### Part Windows – Espais d’emmagatzematge

- **Configuració inicial**: Crear Storage Pool amb tres discos de 10 GB.
- **Resiliència**:
  - Mirroring amb dos discos.
  - Mirall triple amb tres discos.
  - Paritat amb discos addicionals.
- **Gestió**: Visualitzar estat dels discos i del pool des de la consola de gestió.

## Metodologia de treball

- **Treball en grup**: Divisió en dos equips (Linux i Windows).
- **Treball individual**: Preparació del guió i recerca de comandes.
- **Demostració**: Execució pràctica en parelles.
- **Documentació**: Revisió conjunta i pujada als repositoris individuals.

## Recursos de suport
- LVM Linux (Moodle)
- Espais d’emmagatzematge (Windows) (Moodle)

---

> **Nota conjunta** – La qualitat del treball dependrà de la col·laboració i la claredat de la documentació.  
> **Presentació final** – Les conclusions s’hauran de presentar al client en una exposició conjunta.

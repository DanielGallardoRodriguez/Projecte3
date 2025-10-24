# P04 – Documentació del servidor DNS

## Context

Després de configurar un servidor DNS com a prova de concepte per al client **DigiCore**, és moment de **documentar i publicar** les configuracions realitzades. L’objectiu és garantir que aquestes es puguin **replicar fàcilment** en futurs entorns, simplement descarregant els arxius i reiniciant el servei.

Aquesta pràctica reforça la importància de la **repetitibilitat** i la **gestió documental** en entorns professionals.

## Objectius
- Assegurar la **connectivitat** entre la màquina virtual (Ubuntu Server) i la màquina física.
- **Exportar** els arxius de configuració del servidor DNS mitjançant SCP.
- **Organitzar i pujar** els arxius al repositori de GitHub.
- Documentar el procés i els fitxers implicats.

## Estructura del lliurament

Dins la carpeta `producte04` s’han d’incloure:

- `README.md` → Descripció general del producte (aquest document).
- Carpeta `zones/` → Arxius de configuració de les zones DNS.
- Carpeta `img/` → Captures de pantalla del procés de configuració i exportació.
- Arxius principals:
  - `named.conf.options`
  - `named.conf.local`

## Fases del treball

### Fase 1 – Preparació i Extracció

1. **Configurar interfície Host-Only** a la màquina virtual.
2. **Verificar connectivitat** amb la màquina física.
3. **Transferir arxius** amb SCP:
   ```bash
   scp usuari@ip_vm:/etc/bind/named.conf.options .
   scp usuari@ip_vm:/etc/bind/named.conf.local .
   scp usuari@ip_vm:/etc/bind/zones/* ./zones/
   ``

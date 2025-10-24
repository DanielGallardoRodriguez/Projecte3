# Tasca 06 – Fonaments del servei DNS

## Context

El client **DigiCore**, una empresa de màrqueting digital, pateix errors de connectivitat en algunes aplicacions. L’equip tècnic sospita que la causa principal és una resolució de noms (DNS) incorrecta o lenta.

EverPia ha rebut l’encàrrec de realitzar una **auditoria teòrica i pràctica** del servei DNS, amb l’objectiu de formar el personal del client i proporcionar eines de diagnosi eficients.

## Objectius de la tasca

- Elaborar una **sessió formativa** sobre els fonaments del servei DNS.
- Realitzar una **auditoria pràctica** mitjançant eines CLI en sistemes Linux/macOS i Windows.
- Documentar els resultats i explicacions en un informe tècnic.

## Estructura del lliurament

Dins la carpeta `tasca06` s’han d’incloure els següents arxius:

- `README.md` → Descripció general de la tasca (aquest document).
- `guia.md` → Documentació amb resultats i anàlisi de les comandes CLI.
- Carpeta `img/` → Captures de pantalla de les comandes executades.

## Fase Teòrica – Sessió Formativa
La formació ha d’incloure els següents conceptes:

- **Jerarquia i estructura del DNS**: Root, TLDs, domini de segon nivell.
- **Procés de resolució**: Consultes iteratives i recursives, servidors autoritatius.
- **Tipus de zones**: Directa, inversa, primària, secundària.
- **Registres DNS clau**: A, CNAME, MX, NS, SRV.
- **Conceptes essencials**:
  - Resposta autoritativa
  - TTL (Time To Live)
  - SOA (Start of Authority)
  - Reenviadors (condicionals i incondicionals)
  - Resolució local amb mDNS

> Activitat: Crear una **píndola formativa en vídeo** (10–15 minuts) explicant aquests conceptes de forma clara i concisa.

## Fase Pràctica – Diagnosi amb CLI

### Diagnosi amb `dig` (Linux/macOS)

1. **Consulta A**: `dig xtec.cat A`  
   → IP, TTL, servidor de resposta

2. **Consulta NS**: `dig tecnocampus.cat NS`  
   → Servidors autoritatius

3. **Consulta SOA**: `dig escolapia.cat SOA`  
   → Correu de l’administrador, número de sèrie

4. **Resolució inversa**: `dig -x 147.83.2.135`  
   → Informació de registre PTR
### Diagnosi amb `nslookup` (Multiplataforma)

1. **Consulta no autoritativa**:  
   → `set type=A` i consulta a `tecnocampus.cat`

2. **Consulta autoritativa**:  
   → `server IP` (IP obtinguda anteriorment) i nova consulta A

### Resolució local

- Verificació del funcionament de **mDNS** en xarxa local sense servidor DNS.

> Activitat: Documentar totes les comandes, resultats i explicacions en el fitxer `guia.md`, amb captures de pantalla.

## Recursos de suport

- UD04.AA1 Serveis de Directori (Moodle)
- UD04.AA2 Instal·lació OpenLDAP (Moodle)
- UD04.AA3 Configuració del directori (Moodle)
- UD04.AA5 Agregar client al directori (Moodle)

---

> **Tasca individual** – Cal demostrar domini teòric i pràctic del servei DNS.  
> **Documentació clara** – La guia ha de ser útil per formar el personal tècnic del client.
